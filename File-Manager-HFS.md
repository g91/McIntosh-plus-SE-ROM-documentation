# File Manager & Hierarchical File System (HFS)

## 1. Overview of Macintosh Storage Architecture

When the original 128K Macintosh debuted in 1984, it used the **Macintosh File System (MFS)**, a flat single-directory file system designed for 400 KB single-sided floppy disks. With the arrival of the 20 MB Hard Disk 20 (HD20) and the 800 KB double-density drives on the Macintosh Plus, Apple introduced the **Hierarchical File System (HFS)**, integrated into the 128 KB ROM (`plus/os/file_mgr_*.s`) and continued in the 256 KB SE ROM (`se/os/file_mgr_*.s`).

HFS replaced flat directories with a balanced B*-tree directory catalog, supporting nested folders, large multi-megabyte hard drives, dynamic block allocation, extent records, and multi-fork files (Data Fork and Resource Fork).

---

## 2. Core On-Disk Data Structures

Every HFS disk volume is structured into five distinct geometric regions:

```
+---------------------------------------------------------------+
| Logical Block 0 & 1: Boot Blocks ('LK' signature, system boot)|
+---------------------------------------------------------------+
| Logical Block 2: Master Directory Block (MDB / VCB)           |
+---------------------------------------------------------------+
| Volume Allocation Bitmap (1 bit per allocation block)         |
+---------------------------------------------------------------+
| Extents Overflow File (B*-Tree: overflow extent descriptors)  |
+---------------------------------------------------------------+
| Catalog File (B*-Tree: directory hierarchy, files, threads)   |
+---------------------------------------------------------------+
| User File Data & Resource Forks (Allocation Blocks)           |
+---------------------------------------------------------------+
| Logical Block N-1: Alternate Master Directory Block (Backup)  |
+---------------------------------------------------------------+
```

### 2.1 Volume Control Block (`VCB`)
When a volume is mounted, its MDB is loaded into a RAM-based `VCB` structure:
- `vcbSigWord` (`$00`): Volume signature (`$4244` = 'BD' for HFS, `$D2D7` for MFS).
- `vcbCrDate`, `vcbLsMod`: Creation and last modification timestamps.
- `vcbAtrb`: Volume attributes (write-protected, dirty flag).
- `vcbNmAlBlks`: Total number of allocation blocks on the volume.
- `vcbAlBlkSiz`: Size of each allocation block in bytes (always a multiple of 512).
- `vcbClpSiz`: Default file clump size (allocation chunk size).
- `vcbAlBlSt`: Starting physical block offset of the allocation block pool.
- `vcbNxtCNID`: Next available Catalog Node ID (CNID).
- `vcbFreeBks`: Number of free allocation blocks remaining.
- `vcbVN`: Pascal string storing volume name.
- `vcbExtTree`, `vcbCatTree`: In-memory B-tree control blocks for Extents and Catalog files.

### 2.2 File Control Block (`FCB`)
Low-memory global `FCBSPtr` (`$034E`) points to an array of open file control blocks:
- `fcbFlNm`: File Catalog Node ID (CNID).
- `fcbMdDat`: Modification timestamp.
- `fcbTyp`: File type / fork flag (Data fork = 0, Resource fork = non-zero).
- `fcbSBlk`: Starting allocation block of file.
- `fcbEOF`: Logical end-of-file byte count.
- `fcbPLen`: Physical end-of-file allocation byte count.
- `fcbCrPs`: Current read/write mark byte offset.
- `fcbExtRec`: First 3 extent records for immediate mapping without B-Tree lookup.

---

## 3. The B*-Tree Engine (`file_mgr_btree.s`)

Both the **Catalog File** and the **Extents Overflow File** are implemented as B*-Trees. The ROM B-tree engine manages fixed 512-byte nodes:

```
Node Layout (512 bytes):
+---------------------------------------------------------------+
| Node Descriptor (14 bytes):                                   |
| - ndFLink (4 bytes): Forward link to next node at same level  |
| - ndBLink (4 bytes): Backward link to previous node           |
| - ndType  (1 byte):  $00=Index, $01=Header, $02=Map, $FF=Leaf |
| - ndNHeight (1 byte): Height/level in tree                    |
| - ndNRecs (2 bytes): Number of active records in this node   |
+---------------------------------------------------------------+
| Key / Data Record 1                                           |
+---------------------------------------------------------------+
| Key / Data Record 2                                           |
+---------------------------------------------------------------+
| ...                                                           |
+---------------------------------------------------------------+
| Record Offsets Array (grown backwards from offset 512)        |
+---------------------------------------------------------------+
```

### Node Types
- **Header Node (Node 0)**: Contains tree height, root node number, total node count, and free node count.
- **Map Node**: Contains allocation bitmap indicating which tree nodes are free or allocated.
- **Index Nodes**: Contain Search Keys and child node block pointers for navigating tree levels.
- **Leaf Nodes**: Contain actual payload data records. All leaf nodes are linked horizontally via `ndFLink` / `ndBLink` for fast sequential traversal.

### B-Tree Core Routines
- **`SearchNode`**: Performs binary search on node records using key comparison callbacks.
- **`InsertNode`**: Inserts a new key/data record. If node overflows 512 bytes, initiates **Node Splitting**, promoting the middle key up to the parent index node.
- **`DeleteNode`**: Removes a record and collapses empty nodes.

---

## 4. The Catalog Hierarchy (`file_mgr_catalog.s`)

The Catalog B*-Tree organizes the nested directory hierarchy using **Catalog Keys (`CatKey`)**:

```
CatKey Record:
+-----------------------------------+
| Key Length (1 byte)               |
+-----------------------------------+
| Reserved Byte                     |
+-----------------------------------+
| Parent Directory CNID (4 bytes)   |
+-----------------------------------+
| CNode Name (Pascal String: 1-31 B)|
+-----------------------------------+
```

Because every search key starts with the **Parent Directory CNID**, all files and subfolders within the same directory share the same prefix in the B-Tree, ensuring that directory listings (`_GetCatInfo`) execute with maximum locality of reference!

### CNode Record Types
1. **Directory Record (`dirRec`)**: Stores folder flags, directory CNID, creation date, modification date, and Finder info (`DInfo`).
2. **File Record (`fileRec`)**: Stores file flags, file CNID, 4-byte Creator, 4-byte Type, Finder info (`FInfo`), and the first 3 extent descriptors for both the Data Fork and Resource Fork.
3. **Directory Thread Record (`dirThdRec`)**: Maps a directory's own CNID back to its parent CNID and folder name, enabling instant upward navigation (`cd ..`).
4. **File Thread Record (`fileThdRec`)**: Maps an open file CNID back to its parent directory and filename.

---

## 5. Extents Allocation Engine (`file_mgr_alloc.s`)

Files on HFS volumes are allocated in contiguous clumps of allocation blocks. Each allocation chunk is represented by an **Extent Descriptor**:
- `xdrStABN`: Starting allocation block number.
- `xdrNumABlks`: Number of contiguous allocation blocks.

### Three-Extent Optimization
Because most files require fewer than three contiguous fragments, the first three extent descriptors for both forks are stored directly in the catalog `fileRec`. Only if a file fragments into 4 or more pieces does the File Manager consult the **Extents Overflow B*-Tree**.

---

## 6. The Block Cache Engine (`file_mgr_cache.s`)

To minimize slow physical floppy and SCSI disk access, the ROM includes a unified block cache:
- Holds an array of 512-byte buffer headers (`BufTbl`).
- Employs a Least-Recently-Used (LRU) buffer replacement algorithm.
- Implements delayed dirty-block write-backs (`MarkBufDirty` and `FlushCache`).

---

## 7. High-Level File Manager API

- **`Create` / `_Create`** (`$A008`): Creates a new file entry in the catalog without opening forks.
- **`OpenRF` / `_OpenRF`** (`$A00A`): Opens the Resource Fork of a file.
- **`GetFileInfo` / `_GetFileInfo`** (`$A00C`) & **`SetFileInfo` / `_SetFileInfo`** (`$A00D`): Reads or updates Finder 4-character Type/Creator codes and flags.
- **`MountVol` / `_MountVol`** (`$A00F`): Reads volume MDB, verifies signature, mounts VCB in queue.
- **`GetEOF` / `_GetEOF`** (`$A011`) & **`SetEOF` / `_SetEOF`** (`$A012`): Reads or extends logical file length.
- **`Allocate` / `_Allocate`** (`$A010`): Allocates additional contiguous blocks to an open file.
- **`OpenWD` / `_OpenWD`** (`$A200`): Opens an HFS Working Directory (creates a temporary virtual VRefNum mapping a directory CNID).
- **`CloseWD` / `_CloseWD`** (`$A201`): Closes a Working Directory.
- **`CatMove` / `_CatMove`** (`$A205`): Moves a file or folder between directories on the same volume without copying file data blocks (simply updates Parent CNID in Catalog B-Tree).


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)
