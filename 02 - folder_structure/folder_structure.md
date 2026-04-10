# 📁 Understanding Linux Folder Structure

Linux uses a **fixed directory structure** where everything is organized in folders starting from `/` (root).

Think of it like a tree:
- `/` = main root  
- All folders come under it  

## 🔗 Symbolic Links (Shortcuts)

These are like **shortcuts** pointing to actual folders.

| Directory | Meaning |
|----------|--------|
| `/sbin → /usr/sbin` | System admin commands (shortcut to `/usr/sbin`) |
| `/bin → /usr/bin` | Basic user commands (shortcut to `/usr/bin`) |
| `/lib → /usr/lib` | Libraries needed by programs (shortcut to `/usr/lib`) |

👉 These are not real folders, just links.

## ⚙️ Important System Directories

| Directory | Purpose |
|----------|--------|
| `/boot` | Files needed to start (boot) the system |
| `/usr` | Applications and libraries installed by user |
| `/var` | Logs, cache, and frequently changing data |
| `/etc` | System configuration files |

👉 These are core system folders.

## 👤 User & Application Directories

| Directory | Purpose |
|----------|--------|
| `/home` | Stores user files (documents, downloads, etc.) |
| `/opt` | Optional third-party software |
| `/srv` | Data used by services (like web servers) |
| `/root` | Home folder of root (admin user) |

👉 `/home` is where normal users work.

## 🔄 Temporary & System Runtime Directories

| Directory | Purpose |
|----------|--------|
| `/tmp` | Temporary files (deleted after reboot) |
| `/run` | Data for currently running processes |
| `/proc` | Information about running processes (virtual) |
| `/sys` | Hardware and kernel info (virtual) |
| `/dev` | Device files (like disk, USB, etc.) |

👉 These are dynamic and change frequently.

## 💾 Mount Points

| Directory | Purpose |
|----------|--------|
| `/mnt` | Temporary mount for external storage |
| `/media` | Auto-mount for USB, CD, etc. |
| `/data` | Custom mount (example: Windows shared folder) |

👉 Used to connect external storage to Linux.

## 🎯 Simple Summary

- `/` → Root of everything  
- `/home` → User files  
- `/etc` → Configuration  
- `/var` → Logs & changing data  
- `/usr` → Applications  
- `/tmp` → Temporary files  
- `/dev`, `/proc`, `/sys` → System-related  

💡 **Easy Way to Remember:**
- System files → `/etc`, `/usr`, `/var`  
- User files → `/home`  
- Temporary → `/tmp`  
- Hardware & system → `/dev`, `/proc`, `/sys`  

🚀 Now you understand how Linux organizes files and folders!
