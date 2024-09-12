# Working with the Shell - I

### Shell Basics
- **Shell**: Text-based interface for interacting with Linux.
- **Home Directory**: The default directory for each user, represented by `~`.

#### Key Commands:
- `pwd`: Prints the current working directory.
- `ls`: Lists files and directories.
  - Use `ls -l` for detailed info, `ls -a` to show hidden files.
- `cd [directory]`: Changes the current directory.
  - `cd ..`: Goes up one level.
  - `cd ~`: Goes to the home directory.
  
#### File & Directory Management:
- `mkdir [dir_name]`: Creates a new directory.
- `rmdir [dir_name]`: Removes an empty directory.
- `rm -r [dir_name]`: Removes a directory and its contents.
- `touch [file_name]`: Creates a new empty file.
- `cp [file] [destination]`: Copies a file.
- `mv [source] [destination]`: Moves or renames a file/directory.
- `rm [file_name]`: Removes a file.
  - `rm -r [dir_name]`: Removes a directory and its contents recursively.

#### Text Editing:
- `cat [file_name]`: Displays the contents of a file.
- `vim [file_name]`: Opens a file in Vim for editing.

### Vi Commands:
#### Modes:
1. **Normal Mode** (default mode for navigation and commands):
   - `Esc`: Return to normal mode.
   - `h`, `j`, `k`, `l`: Move left, down, up, right (or use arrow keys).
   - `dd`: Delete a line.
   - `yy`: Copy (yank) a line.
   - `p`: Paste below.
   - `u`: Undo the last action.
   - `:`: Enter command-line mode (e.g., `:wq` to save and quit).
  
2. **Insert Mode** (for editing text):
   - `i`: Insert at cursor.
   - `I`: Insert at the beginning of the line.
   - `a`: Insert after the cursor.
   - `A`: Insert at the end of the line.
   - `Esc`: Return to normal mode.

3. **Visual Mode** (for selecting text):
   - `v`: Start visual selection (character-wise).
   - `V`: Start visual selection (line-wise).
   - `Ctrl+v`: Block visual selection.
   - `Esc`: Exit visual mode.

4. **Command-Line Mode** (for saving, quitting, searching):
   - `:w`: Save the file.
   - `:q`: Quit.
   - `:wq`: Save and quit.
   - `:q!`: Quit without saving.
   - `/pattern`: Search for a pattern.

#### Output Redirection:
- `>`: Redirects command output to a file, overwriting it.
  - Example: `ls > files.txt` saves the list of files to `files.txt`.
- `>>`: Appends command output to a file without overwriting.

---

# Linux Core Concepts

### Linux Kernel
- **Kernel**: Manages memory, processes, and devices.
- **Kernel Version**: Use `uname -r` to check the version.

### File Permissions:
- `chmod [permissions] [file]`: Changes file permissions.
  - `chmod +x [file]`: Makes a file executable.
- `chown [user]:[group] [file]`: Changes file ownership.

---

# Common Commands for Files and Scripts

#### File Viewing & Editing:
- `head [file_name]`: Displays the first few lines of a file.
- `tail [file_name]`: Displays the last few lines of a file.
- `nano [file_name]`: Simple text editor for files.

#### Running Python Files:
- `python3 [script.py]`: Runs a Python script.

#### System Info:
- `df -h`: Displays disk usage.
- `free -h`: Displays memory usage.
- `top`: Shows real-time system processes (install with `sudo dnf install procps-ng` if missing).

#### Process Management:
- `ps aux`: Lists running processes.
- `kill [PID]`: Kills a process by its Process ID (PID).

---

# Lab - Linux Kernel

- **Kernel Messages**: Use `dmesg` to check system messages.
- **List Block Devices**: `lsblk`
- **Check Cores**: `lscpu`
- **Check Online Memory**: `lsmem`
