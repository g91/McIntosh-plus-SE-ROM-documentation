# HFS B*-Tree & Catalog Internals

## 1. Deep Dive into the HFS B*-Tree Implementation

The Hierarchical File System (HFS) relies on an optimized B*-Tree implementation (`plus/os/file_mgr_btree.s` and `se/os/file_mgr_btree.s`). In classic HFS, all directory hierarchies, filenames, thread records, and overflow extent allocations are maintained in two balanced B*-Trees:
1. **The Catalog B*-Tree File**: Stores folder relationships, filenames, and file metadata.
2. **The Extents Overflow B*-Tree File**: Stores allocation records for fragmented files possessing more than 3 extent fragments.

---

## 2. Low-Level B*-Tree Node Architecture (512 Bytes)

Every B*-Tree node is exactly 512 bytes in size. Records within a node are allocated contiguously from the front of the node (offset 14 onward), while an array of 16-bit **Record Offsets** grows backward from the very end of the node (offset 512).

```
+---------------------------------------------------------------+ Offset 0
| Node Descriptor (14 bytes):                                   |
| - ndFLink (Long): Forward node pointer (same level)           |
| - ndBLink (Long): Backward node pointer (same level)          |
| - ndType  (Byte): Node Type ($00=Index, $01=Hdr, $02=Map, $FF=Leaf)
| - ndNHeight (Byte): Current node tree depth / level           |
| - ndNRecs (Word): Number of active records stored in node    |
+---------------------------------------------------------------+ Offset 14
| Record 0 (Key + Data Payload)                                 |
+---------------------------------------------------------------+
| Record 1 (Key + Data Payload)                                 |
+---------------------------------------------------------------+
| ... Free Space (Unallocated bytes) ...                        |
+---------------------------------------------------------------+
| Offset of Record 2 (Word)                                     |
+---------------------------------------------------------------+ Offset 508
| Offset of Record 1 (Word)                                     |
+---------------------------------------------------------------+ Offset 510
| Offset of Record 0 (Word = 14)                                |
+---------------------------------------------------------------+ Offset 512
```

### Fast Record Addressing Formula
To locate the byte offset of record $i$ (where $0 \le i < \text{ndNRecs}$):
$$\text{Offset}_i = \text{WordAt}(512 - 2 \cdot (i + 1))$$
This allows $O(1)$ random access to any record within a 512-byte node without parsing variable-length keys.

---

## 3. Node Types and Tree Topology

1. **Header Node (Node 0)**:
   - Always located at physical block 0 of the B-Tree file.
   - Contains tree metadata:
     - `bthDepth`: Current height of the tree (1 for single root leaf, up to 8).
     - `bthRoot`: Node number of the active root node.
     - `bthNRecs`: Total count of leaf records across the entire tree.
     - `bthFNode`: Node number of the first (leftmost) leaf node.
     - `bthLNode`: Node number of the last (rightmost) leaf node.
     - `bthNodeSize`: Node size in bytes (always 512).
     - `bthKeyLen`: Maximum key length (37 bytes for Catalog, 7 bytes for Extents).
     - `bthNNodes`: Total number of nodes allocated in file.
     - `bthFree`: Count of free nodes available.
2. **Map Node**:
   - Contains an allocation bitmap tracking which 512-byte nodes in the tree file are free or in use. If the file grows beyond 4,000 nodes, multiple map nodes are chained together via `ndFLink`.
3. **Index Nodes**:
   - Intermediate branch nodes. Every record in an index node consists of a **Search Key** followed by a 4-byte **Child Node Number**.
4. **Leaf Nodes (`ndType = $FF`)**:
   - Reside at level 1 (bottom of tree). Contain actual Catalog records (file/folder metadata) or Extent descriptors.
   - All leaf nodes are linked horizontally via `ndFLink` and `ndBLink`, enabling fast sequential range scans (`CatSearch`) without returning to parent index nodes.

---

## 4. Key Comparison and Sorting Algorithms

### The Catalog Key (`CatKey`)
```
Offset  Field       Type      Description
------  ----------  --------  -------------------------------------------------------------
$00     ckrKeyLen   Byte      Total key length in bytes (excluding this length byte)
$01     ckrResrv1   Byte      Reserved padding (must be 0 for word alignment)
$02     ckrParID    LongInt   Catalog Node ID (CNID) of parent folder
$06     ckrCName    Str31     Pascal string: length byte + up to 31 uppercase/lowercase chars
```

### Case-Insensitive String Sorting
Keys in the Catalog B-Tree are sorted primarily by `ckrParID` (unsigned 32-bit integer comparison). If two keys share the same parent folder ID, they are sorted alphabetically by filename using Apple's diacritical-sensitive case-folding table:
- Case differences (e.g. "System" vs "SYSTEM") are treated as identical to guarantee case-insensitive filename uniqueness.
- Diacritical marks (e.g. accented vowels) are sorted according to international collation rules.

---

## 5. Node Splitting and Tree Balancing (`SplitNode`)

When a new file or directory is created (`_Create`, `_DirCreate`), the Catalog Manager attempts to insert the record into the appropriate leaf node. If the combined size of the new record and its 2-byte offset exceeds available free space in the node:

```
[ Full Node (512 Bytes Exceeded) ]
                 |
                 v
[ 1. Allocate New Free Node from Map Node ]
                 |
                 v
[ 2. SplitNode Algorithm ]
  - Determine optimal split boundary near the 256-byte median.
  - Move upper 50% of records into the newly allocated sibling node.
  - Update ndFLink and ndBLink pointers across both nodes to preserve horizontal chain.
                 |
                 v
[ 3. Promote Pivot Key ]
  - The first key of the new sibling node is promoted upward into the parent Index Node.
  - If the parent Index Node is also full:
    - Recursively split parent index node!
    - If the root node splits: allocate a new Root Node, increasing bthDepth by 1.
```

---

## 6. Catalog Records and CNode Structure

Every leaf record in the Catalog B*-Tree begins with a 2-byte **Record Type**:

### 6.1 Directory Record (`dirRec` - Type `$0001`)
- `dirFlags`: Attribute flags.
- `dirVal`: Number of files and folders directly contained within this directory.
- `dirDirID`: Unique 32-bit Catalog Node ID (CNID) assigned to this directory.
- `dirCrDat`, `dirMdDat`, `dirBkDat`: Creation, modification, and backup timestamps.
- `dirUsrInfo`: 16-byte Finder `DInfo` record (window scroll position, icon view rectangle).

### 6.2 File Record (`fileRec` - Type `$0002`)
- `filFlags`: Bit 7 = file locked, bit 0 = record in use.
- `filTyp`: File type byte.
- `filUsrInfo`: 16-byte Finder `FInfo` (4-byte Type like `'APPL'`, 4-byte Creator like `'MACS'`).
- `filFlNum`: Unique 32-bit CNID of this file.
- `filStBlk`: Logical starting block.
- `filLgLen`: Logical End-of-File (data fork size in bytes).
- `filPyLen`: Physical End-of-File (allocated block capacity).
- `filRStBlk`: Logical starting block of Resource Fork.
- `filRLgLen`: Logical EOF of Resource Fork.
- `filRPyLen`: Physical EOF of Resource Fork.
- `filExtRec`: Array of 3 Extent Descriptors for Data Fork.
- `filRExtRec`: Array of 3 Extent Descriptors for Resource Fork.

### 6.3 Thread Records (`dirThdRec` `$0003` & `fileThdRec` `$0004`)
- Used for instantaneous reverse lookup (mapping a CNID back to its parent CNID and filename).
- Key for thread record: `ckrParID` = CNode's own ID, `ckrCName` = empty string `""`.
- Data payload: `thdParID` = Parent folder ID, `thdCName` = Actual file or folder name.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)
