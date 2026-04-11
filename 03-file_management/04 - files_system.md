# Advanced Linux Concepts

## 1. Symbolic Link (Soft Link)

A symbolic link (symlink) is a special type of file that points to another file or directory by its path.

### Key Characteristics:
- Stores the path of the target file
- Can link across different filesystems
- Can link to directories
- If the original file is deleted, the symlink becomes broken

### Create symlink:
```bash
ln -s target_file link_name
```

### Example:
```bash
ln -s file.txt link.txt
```

### Behavior:
- Accessing link.txt actually accesses file.txt
- If file.txt is deleted, link.txt becomes invalid

---

## 2. Hard Link

A hard link is another name for the same file (same inode).

### Key Characteristics:
- Points directly to the same inode as the original file
- Cannot span across different filesystems
- Cannot link directories (usually restricted)
- If the original file is deleted, the data still exists via the hard link

### Create hard link:
```bash
ln file.txt hardlink.txt
```

### Behavior:
- Both names refer to the same data
- Deleting one does not remove the data unless all links are deleted

---

## Difference Between Symlink and Hard Link

| Feature | Symlink | Hard Link |
|--------|--------|----------|
| Type | Path reference | Direct inode reference |
| Cross filesystem | Yes | No |
| Works for directories | Yes | No |
| Breaks if original deleted | Yes | No |
| Inode shared | No | Yes |

---

## 3. Buffered vs Unbuffered I/O

### Buffered I/O

Buffered I/O uses a temporary memory area (buffer) to store data before writing to disk.

### Characteristics:
- Data is collected in memory first
- Written to disk in chunks
- Faster performance
- Less system calls

### Example:
Standard file operations in most programs use buffered I/O

### Advantages:
- Efficient
- Reduces disk access
- Improves performance

### Disadvantages:
- Data loss possible if system crashes before buffer flush

---

### Unbuffered I/O

Unbuffered I/O writes data directly to disk without using a buffer.

### Characteristics:
- Immediate write to disk
- No intermediate storage
- More system calls
- Slower compared to buffered I/O

### Example:
```bash
sync
```

### Advantages:
- Data safety
- Real-time write

### Disadvantages:
- Slower performance

---

## Key Difference

| Feature | Buffered I/O | Unbuffered I/O |
|--------|-------------|----------------|
| Speed | Faster | Slower |
| Memory usage | Uses buffer | No buffer |
| Safety | Less safe | More safe |
| Disk operations | Fewer | More |

---

## 4. Filesystem Hierarchy Standard (FHS)

The Filesystem Hierarchy Standard defines how directories are structured in Linux.

### Root Directory

`/` is the top-level directory. All files and directories exist under it.

---

### Important Directories

#### `/bin`
- Essential user commands
- Example: ls, cp, mv

#### `/sbin`
- System administration commands
- Example: fdisk, reboot

#### `/etc`
- Configuration files
- Example: passwd, hosts

#### `/home`
- User home directories

#### `/root`
- Home directory of root user

#### `/var`
- Variable data (logs, cache)
- Example: /var/log

#### `/usr`
- User applications and libraries

#### `/boot`
- Boot loader files and kernel

#### `/dev`
- Device files (hardware representation)

#### `/proc`
- Virtual filesystem for process information

#### `/sys`
- Virtual filesystem for kernel and hardware

#### `/tmp`
- Temporary files

#### `/run`
- Runtime data for processes

#### `/opt`
- Optional third-party software

#### `/mnt`
- Temporary mount points

#### `/media`
- Removable media (USB, CD)
