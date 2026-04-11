# Shell Concepts in Linux

## 1. What is a Shell?

The **shell** is a program that allows users to interact with the Linux system using commands.

👉 It acts as a bridge between:
- User → Shell → Kernel

### Examples:
- bash (most common)
- sh
- zsh

👉 When you type a command, the shell:
1. Reads the command
2. Processes it
3. Sends it to the system

## 2. Environment Variables

Environment variables are **key-value pairs** used to store system information.

### Examples:
- `HOME` → user home directory
- `PATH` → list of directories for commands
- `USER` → current username

### Check variables:
```bash
printenv
```

### Access variable:
```bash
echo $HOME
```

### Create variable:
```bash
export MY_VAR="hello"
```

## 3. Startup Files

Startup files are scripts that run automatically when a shell starts.

### Common files:
- `~/.bashrc` → runs for interactive shells
- `~/.bash_profile` → runs at login
- `~/.profile` → general startup file

## 4. How to Edit Startup File

### Open file:
```bash
nano ~/.bashrc
```

### Add configuration:
```bash
export MY_NAME="devops"
```

### Apply changes:
```bash
source ~/.bashrc
```

👉 Now changes are active

## 5. Aliases

Aliases are shortcuts for long commands.

### Create alias:
```bash
alias ll='ls -la'
```

### Use:
```bash
ll
```

### Remove alias:
```bash
unalias ll
```

👉 Add aliases in `.bashrc` to make them permanent

## 6. Configuring the Shell

### set command

Used to configure shell behavior

```bash
set -o noclobber
```

👉 Prevents overwriting files

### shopt command

Used to enable/disable shell options

```bash
shopt -s nocaseglob
```

👉 Makes filename matching case-insensitive

## 7. PS1 (Shell Prompt)

PS1 defines how your terminal prompt looks.

### Example:
```bash
PS1="[\u@\h \W]\$ "
```

👉 Shows:
- username
- hostname
- current directory

## 8. Command Sequences

You can run multiple commands together:

### Sequential:
```bash
command1 ; command2
```

### Run if success:
```bash
command1 && command2
```

### Run if failure:
```bash
command1 || command2
```

## 9. Bash Expansion

Bash expansion means the shell **expands patterns before executing commands**.

### Examples:

```bash
echo {1..5}
```

👉 Output:
```
1 2 3 4 5
```

```bash
echo file{1,2,3}.txt
```

👉 Output:
```
file1.txt file2.txt file3.txt
```

## 10. Word Splitting

Word splitting happens when the shell splits input into words.

### Example:
```bash
VAR="hello world"
echo $VAR
```

👉 Output:
```
hello world
```
Shell splits based on spaces (IFS variable)
