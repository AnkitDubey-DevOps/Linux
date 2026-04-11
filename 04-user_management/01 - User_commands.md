# User Management in Linux

## Introduction to User Management in Linux
Linux is a multi-user operating system, meaning multiple users can operate on a system simultaneously. Proper user management ensures security, controlled access, and system integrity. 

Key files involved in user management:
- `/etc/passwd` – Stores user account details.
- `/etc/shadow` – Stores encrypted user passwords.
- `/etc/group` – Stores group information.
- `/etc/gshadow` – Stores secure group details.

## Creating Users in Linux
To create a new user in Linux, use:

### `useradd` Command (For most Linux distributions)
```bash
useradd username
```
This creates a user without a home directory.

To create a user with a home directory:
```bash
useradd -m username
```

To specify a shell:
```bash
useradd -s /bin/bash username
```

### `adduser` Command (For Debian-based systems)
```bash
adduser username
```
This is an interactive command that asks for a password and additional details.

## Managing User Passwords
To set or change a user’s password:
```bash
passwd username
```

### Enforcing Password Policies
- **Password expiration**: Set password expiry days
  ```bash
  chage -M 90 username
  ```
- **Lock a user account**
  ```bash
  passwd -l username
  ```
- **Unlock a user account**
  ```bash
  passwd -u username
  ```

## Modifying Users
Modify an existing user with `usermod`:
- Change the username:
  ```bash
  usermod -l new_username old_username
  ```
- Change the home directory:
  ```bash
  usermod -d /new/home/directory -m username
  ```
- Change the default shell:
  ```bash
  usermod -s /bin/zsh username
  ```

## Deleting Users
To remove a user but keep their home directory:
```bash
userdel username
```
To remove a user and their home directory:
```bash
userdel -r username
```

## Working with Groups
### Creating Groups
```bash
groupadd groupname
```

### Adding Users to Groups
```bash
usermod -aG groupname username
```

### Viewing Group Memberships
```bash
groups username
```

### Changing Primary Group
```bash
usermod -g new_primary_group username
```

## Sudo Access and Privilege Escalation
### Adding a User to Sudo Group
On Debian-based systems:
```bash
usermod -aG sudo username
```
On RHEL-based systems:
```bash
usermod -aG wheel username
```

### Granting Specific Commands with Sudo
Edit the sudoers file:
```bash
visudo
```
Then add:
```bash
username ALL=(ALL) NOPASSWD: /path/to/command
```


## Kill Command

### Terminate process
```bash
kill PID
```
### Force kill process

```bash
kill -9 PID
```
### List all signals

```bash
kill -l
```

## File Permissions in Linux
Each file has:
- Owner
- Group
- Others

Permissions:
- r = read
- w = write
- x = execute

### View permissions
```bash
ls -l
```

## Changing Permissions
### Set permissions

```bash
chmod 755 file.txt
```

### Add execute permission
```bash
chmod u+x file.txt
```

## Changing Ownership
```bash
chown user:group file.txt
```

## Advanced File Permissions
### SUID
#### Runs file with owner privileges
```bash
chmod u+s file
```

### SGID
#### New files inherit group
```bash
chmod g+s directory
```

### Sticky Bit
#### Only owner can delete files
```bash
chmod +t directory
```

## Directory Permissions
- r → list files
- w → create/delete files
- x → enter directory

## Signals in Linux
Signals are used to control processes.

Common signals:
- SIGTERM (15) – Graceful stop
- SIGKILL (9) – Force stop
- SIGINT (2) – Interrupt (Ctrl+C)

## Temporary Privilege Escalation
### Run command as root
```bash
sudo command
```
### Start root shell
```bash
sudo -i
```

## Sudo Configuration
### Debian-based systems
```bash
usermod -aG sudo username
```
### RHEL-based systems
```bash
usermod -aG wheel username
```
### Edit sudo configuration
```bash
visudo
```
