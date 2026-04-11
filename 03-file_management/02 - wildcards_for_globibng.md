# Globbing in Linux

## What is Globbing?

**Globbing** is a feature in Linux that allows you to use **special characters (wildcards)** to match multiple files or patterns.
Instead of typing full file names, you can use patterns.

## Simple Example
Instead of typing:
```bash
file1.txt file2.txt file3.txt
```

You can use:
```bash
*.txt
```

This selects all `.txt` files

## Common Wildcards

| Symbol | Meaning |
|--------|--------|
| `*` | Matches any number of characters |
| `?` | Matches exactly one character |
| `[]` | Matches specific characters |

---

## 1. Asterisk `*`

Matches **zero or more characters**

### Example:
```bash
ls *.txt
```

Shows all `.txt` files

```bash
ls file*
```

Shows all files starting with `file`

---

## 2. Question Mark `?`

Matches **exactly one character**

### Example:
```bash
ls file?.txt
```

Matches:
- file1.txt  
- file2.txt  

Does NOT match:
- file10.txt  

## 🔹 3. Square Brackets `[]`

Matches **specific characters**

### Example:
```bash
ls file[123].txt
```

👉 Matches:
- file1.txt  
- file2.txt  
- file3.txt  

## Range Example

```bash
ls file[a-c].txt
```

👉 Matches:
- filea.txt  
- fileb.txt  
- filec.txt  

## Combine Patterns

```bash
ls *.log
```

All `.log` files

```bash
rm file*.txt
```

Deletes all files starting with `file`

---

## Important Notes

- Globbing is done by the **shell (bash, zsh)**  
- It works before the command runs  
- Be careful with `rm *` ⚠️ (can delete everything)

---

## Real-Life Use Cases

```bash
cp *.txt /backup/
```
Copies all `.txt` files to backup folder
