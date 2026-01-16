
# Linux File Operations

This section covers **file and directory management** in Linux, including creation, deletion, viewing, editing, and moving files. All commands are presented in clean Markdown with code blocks.

---

## File and Directory Management

### List files and directories

```bash
ls
```

> Lists files and directories in the current location.

---

### Change working directory

```bash
cd /path/to/directory
```

> Changes the current working directory.

---

### Print working directory

```bash
pwd
```

> Shows the full path of the current directory.

---

### Create a new directory

```bash
mkdir new_folder
```

> Creates a new folder named `new_folder`.

---

### Remove an empty directory

```bash
rmdir empty_folder
```

> Removes a directory only if it is empty.

---

### Delete a file

```bash
rm file.txt
```

> Deletes the file named `file.txt`.

---

### Delete a folder and its contents

```bash
rm -r folder
```

> `-r` recursively deletes the folder and all its contents.

---

### Copy a file

```bash
cp file1.txt file2.txt
```

> Copies `file1.txt` to `file2.txt`.

---

### Copy a directory recursively

```bash
cp -r dir1 dir2
```

> Copies the directory `dir1` and all its contents to `dir2`.

---

### Move or rename a file or directory

```bash
mv old_name new_name
```

> Moves a file or directory, or renames it.

---

## File Viewing and Editing

### Display file content

```bash
cat file.txt
```

> Prints the full content of `file.txt`.

---

### Display file content in reverse

```bash
tac file.txt
```

> Shows the file content from last line to first.

---

### Open file for scrolling view

```bash
less file.txt
```

> Opens the file with scrolling support (forward and backward).

---

### Open file for forward-only view

```bash
more file.txt
```

> Similar to `less` but only allows moving forward.

---

### Display the first N lines of a file

```bash
head -n 10 file.txt
```

> Shows the first 10 lines of the file.

---

### Display the last N lines of a file

```bash
tail -n 10 file.txt
```

> Shows the last 10 lines of the file.

---

### Open file in simple text editor

```bash
nano file.txt
```

> Opens `file.txt` in Nano editor.

---

### Open file in powerful text editor

```bash
vi file.txt
```

> Opens `file.txt` in Vi editor (modal editor with advanced features).

---

### Write text to a file (overwrite)

```bash
echo 'Hello' > file.txt
```

> Writes `Hello` to the file, replacing existing content.

---

### Append text to a file

```bash
echo 'Hello' >> file.txt
```

> Adds `Hello` to the end of the file without overwriting existing content.

---
