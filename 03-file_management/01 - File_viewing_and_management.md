# File Management in Linux

## File and Directory Management
1. **`ls`** – Lists files and directories
2. **`cd /path/to/directory`** – Change directory
3. **`pwd`** – Show current directory
4. **`mkdir new_folder`** – Create a directory
5. **`mkdir -p dir1/dir2`** – Create nested directories
6. **`rmdir empty_folder`** – Remove empty directory
7. **`rm file.txt`** – Delete a file
8. **`rm -r folder`** – Delete a directory and its contents
9. **`rm -rf folder`** – Force delete directory
10. **`cp file1.txt file2.txt`** – Copy a file
11. **`cp -r dir1 dir2`** – Copy a directory
12. **`mv old_name new_name`** – Move or rename
13. **`touch file.txt`** – Create empty file

## Find Commands
14. **`find . -empty -delete`** – Delete empty files
15. **`find . -type f -size +10M`** – Find files larger than 10 MB
16. **`find . -type f -mtime -7`** – Find files modified in last 7 days
17. **`find . -type f -name "*.log"`** – Find all .log files

## File Viewing and Editing
18. **`cat file.txt`** – Display file content
19. **`tac file.txt`** – Display file content in reverse
20. **`less file.txt`** – View file with scrolling
21. **`more file.txt`** – View file (forward only)
22. **`head -n 10 file.txt`** – Show first 10 lines
23. **`tail -n 10 file.txt`** – Show last 10 lines
24. **`tail -f file.txt`** – View live updates
25. **`nano file.txt`** – Open simple editor
26. **`vi file.txt`** – Open advanced editor
27. **`echo 'Hello' > file.txt`** – Overwrite file content
28. **`echo 'Hello' >> file.txt`** – Append to file

## File Information and Counting
29. **`stat file.txt`** – Show detailed file info
30. **`file file.txt`** – Show file type
31. **`du -sh folder`** – Show folder size
32. **`df -h`** – Show disk usage
33. **`wc file.txt`** – Count lines, words, and characters
34. **`wc -l file.txt`** – Count number of lines
35. **`wc -w file.txt`** – Count number of words

## Input and Output (stdin, stdout)
36. **`command > file.txt`** – Redirect output (stdout) to file (overwrite)
37. **`command >> file.txt`** – Append output to file
38. **`command < file.txt`** – Take input (stdin) from file
39. **`command1 | command2`** – Pipe output of one command to another

## Permissions and Ownership
40. **`chmod 755 file.txt`** – Change file permissions
41. **`chown user:user file.txt`** – Change file owner

## Compression and Archive
42. **`tar -cvf archive.tar folder/`** – Create archive
43. **`tar -xvf archive.tar`** – Extract archive
44. **`gzip file.txt`** – Compress file
45. **`gunzip file.txt.gz`** – Decompress file

## Search and Filter
46. **`grep "text" file.txt`** – Search text in file
47. **`grep -r "text" .`** – Search text in directory
