# **Core components of a Linux**

<p align="center">
  <img src="https://github.com/user-attachments/assets/c20f93fd-2879-4977-8516-d35c0b810e90" height="500" width="400">
</p>

## Linux Architecture (Easy Explanation)

### (a) Hardware Layer

- Hardware means the physical parts of a computer:
  - CPU
  - RAM
  - Hard Disk
  - Network Card
- The OS communicates with hardware using *device drivers*

### (b) Kernel (Core of Linux OS)

- The *Linux Kernel* is the heart of the operating system
- It connects software with hardware

####  Main Functions:

- *Process Management* → Handles running programs and multitasking  
- *Memory Management* → Uses RAM efficiently  
- *Device Drivers* → Communication with hardware  
- *File System Management* → Organizes data storage  
- *Network Management* → Handles networking  

### (c) Shell (Command Line Interface - CLI)

- The *Shell* allows users to interact with the system using commands  
- Acts as a bridge between *user ↔ kernel*

####  Examples:
- Bash  
- Zsh  
- Fish  
- Dash  
- Ksh  

 Converts user commands into instructions for the kernel

###  (d) System Libraries & Utilities

- *System Libraries*:
  - glibc
  - libc  
   Provide ready-made functions for programs  

- *System Utilities*:
  - ls  
  - grep  
  - systemctl  
   Used for daily tasks  

###  (e) User Applications

- Programs used by users:

  - Text Editors → Vim, Nano  
  - Web Servers → Apache  
  - DevOps Tools → Docker  

 Applications interact with OS using system calls  

##  Key Points to Remember

- *Kernel* → Core of Linux  
- *Shell* → Interface between user and kernel  
- *Libraries & Utilities* → Support system  
- *Applications* → What users use  
- *Hardware* → Physical components
