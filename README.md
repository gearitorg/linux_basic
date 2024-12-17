# Basic Linux Commands with Examples

In this Linux cheat sheet, we cover essential commands ranging from basic to advanced. Whether you're a beginner or an experienced professional, this cheat sheet can help you work more efficiently with the Linux operating system.

## 1. File and Directory Operations Commands

File and directory operations are fundamental in working with Linux. Here are some commonly used commands:

| Command | Description | Options | Examples |
|---------|-------------|---------|----------|
| `ls` | List files and directories | `-l`: Long format listing<br>`-a`: Include hidden files<br>`-h`: Human-readable file sizes | `ls -l`: Displays files with detailed information<br>`ls -a`: Includes hidden files<br>`ls -lh`: Shows file sizes in a human-readable format |
| `cd` | Change directory | N/A | `cd /path/to/directory`: Changes to the specified directory |
| `pwd` | Print working directory | N/A | `pwd`: Displays the current working directory |
| `mkdir` | Create a new directory | N/A | `mkdir my_directory`: Creates a directory named "my_directory" |
| `rm` | Remove files and directories | `-r`: Remove directories recursively<br>`-f`: Force removal without confirmation | `rm file.txt`: Deletes "file.txt"<br>`rm -r my_directory`: Deletes "my_directory" and its contents<br>`rm -f file.txt`: Force deletes "file.txt" |
| `cp` | Copy files and directories | `-r`: Copy directories recursively | `cp file.txt destination`: Copies "file.txt" to destination<br>`cp -r directory destination`: Copies directory to destination |
| `mv` | Move/rename files and directories | N/A | `mv file.txt new_name.txt`: Renames "file.txt" to "new_name.txt"<br>`mv file.txt directory`: Moves "file.txt" to the specified directory |
| `touch` | Create an empty file or update file timestamps | N/A | `touch file.txt`: Creates an empty file named "file.txt" |
| `cat` | View the contents of a file | N/A | `cat file.txt`: Displays the contents of "file.txt" |
| `head` | Display the first few lines of a file | `-n`: Specify the number of lines to display | `head file.txt`: Displays the first 10 lines<br>`head -n 5 file.txt`: Shows the first 5 lines |
| `tail` | Display the last few lines of a file | `-n`: Specify the number of lines to display | `tail file.txt`: Shows the last 10 lines<br>`tail -n 5 file.txt`: Displays the last 5 lines |
| `ln` | Create links between files | `-s`: Create symbolic (soft) links | `ln -s source_file link_name`: Creates a symbolic link named "link_name" pointing to "source_file" |
| `find` | Search for files and directories | `-name`: Search by filename<br>`-type`: Search by file type | `find /path/to/search -name "*.txt"`: Finds all ".txt" files in the specified directory |

## 2. File Permission Commands

File permissions in Linux control access to files and directories. Here are commands for managing file permissions:

| Command | Description | Options | Examples |
|---------|-------------|---------|----------|
| `chmod` | Change file permissions | `u`: User/owner permissions<br>`g`: Group permissions<br>`o`: Other permissions<br>`+`: Add permissions<br>`-`: Remove permissions<br>`=`: Set permissions explicitly | `chmod u+rwx file.txt`: Grants read, write, and execute permissions to the owner of "file.txt" |
| `chown` | Change file ownership | N/A | `chown user file.txt`: Changes the owner of "file.txt" to "user" |
| `chgrp` | Change group ownership | N/A | `chgrp group file.txt`: Changes the group ownership of "file.txt" to "group" |
| `umask` | Set default file permissions | N/A | `umask 022`: Sets default file permissions to rw-r--r-- |

## 3. File Compression and Archiving Commands

These commands help in file compression and archiving.

| Command | Description | Options | Examples |
|---------|-------------|---------|----------|
| `tar` | Create or extract archive files | `-c`: Create a new archive<br>`-x`: Extract files from an archive<br>`-f`: Specify archive file name<br>`-v`: Verbose mode<br>`-z`: Compress with gzip<br>`-j`: Compress with bzip2 | `tar -czvf archive.tar.gz files/`: Creates a compressed archive |
| `gzip` | Compress files | `-d`: Decompress files | `gzip file.txt`: Compresses "file.txt" to "file.txt.gz" |
| `zip` | Create compressed zip archives | `-r`: Recursively include directories | `zip archive.zip file1.txt file2.txt`: Creates "archive.zip" |

## 4. Process Management Commands

Linux process management commands monitor and control processes.

| Command | Description | Options | Examples |
|---------|-------------|---------|----------|
| `ps` | Display running processes | `-aux`: Show all processes | `ps aux`: Shows all processes with detailed info |
| `top` | Monitor system processes in real-time | N/A | `top`: Displays real-time system processes |
| `kill` | Terminate a process | `-9`: Forcefully kill a process | `kill PID`: Terminates the process with the specified ID |
| `pkill` | Terminate processes by name | N/A | `pkill process_name`: Kills all processes with the given name |
| `pgrep` | List processes by name | N/A | `pgrep process_name`: Lists all processes with the name |

## 5. System Information Commands

These commands display system information.

| Command | Description | Options | Examples |
|---------|-------------|---------|----------|
| `uname` | Print system information | `-a`: All system information | `uname -a`: Displays all system information |
| `whoami` | Show the current username | N/A | `whoami`: Displays the current username |
| `df` | Show disk space usage | `-h`: Human-readable sizes | `df -h`: Displays disk space in a human-readable format |
| `du` | Estimate file and directory sizes | `-h`: Human-readable sizes<br>`-s`: Display total size only | `du -sh directory/`: Shows total size of the specified directory |
| `free` | Display memory usage | `-h`: Human-readable sizes | `free -h`: Shows memory usage in a human-readable format |
| `uptime` | Show system uptime | N/A | `uptime`: Displays current system uptime |
| `lscpu` | Display CPU information | N/A | `lscpu`: Shows detailed CPU information |
| `lspci` | List PCI devices | N/A | `lspci`: Lists PCI devices |
| `lsusb` | List USB devices | N/A | `lsusb`: Lists USB devices |

## 6. Networking Commands

Use these commands to manage network connections.

| Command | Description | Examples |
|---------|-------------|----------|
| `ifconfig` | Display network interface information | `ifconfig`: Displays details of network interfaces |
| `ping` | Send ICMP echo requests to a host | `ping google.com`: Checks connectivity to "google.com" |
| `netstat` | Display network connections and statistics | `netstat -tuln`: Shows TCP and UDP connections |
| `ss` | Display network socket information | `ss -tuln`: Shows listening TCP and UDP connections |
| `ssh` | Securely connect to a remote server | `ssh user@hostname`: Initiates an SSH connection |
| `scp` | Securely copy files between hosts | `scp file.txt user@hostname:/path/to/destination`: Copies "file.txt" to remote host |
| `wget` | Download files from the web | `wget http://example.com/file.txt`: Downloads "file.txt" |
| `curl` | Transfer data to or from a server | `curl http://example.com`: Retrieves a webpage's content |

## 7. IO Redirection Commands

These commands handle input/output redirection in Linux.

| Command | Description | Examples |
|---------|-------------|----------|
| `cmd < file` | Input of cmd is taken from file | `cat < file.txt`: Displays the content of "file.txt" |
| `cmd > file` | Standard output (stdout) is redirected to file | `echo "Hello" > output.txt`: Writes "Hello" to "output.txt" |
| `cmd 2> file` | Error output (stderr) is redirected to file | `ls non_existent_file 2> error.log`: Redirects error to "error.log" |
| `cmd &> file` | Redirects both stdout and stderr to file | `ls &> output.log`: Redirects all output to "output.log" |
| `cmd >> file` | Appends stdout to a file | `echo "New line" >> file.txt`: Appends "New line" to "file.txt" |

## 8. Environment Variable Commands

Set and display environment variables.

| Command | Description | Examples |
|---------|-------------|----------|
| `export VARIABLE=value` | Set an environment variable | `export PATH=/usr/local/bin:$PATH`: Adds a directory to the PATH |
| `echo $VARIABLE` | Display the value of an environment variable | `echo $PATH`: Displays the PATH environment variable |
| `env` | List all environment variables | `env`: Displays all environment variables |
| `unset VARIABLE` | Remove an environment variable | `unset PATH`: Removes the PATH variable |
| `export -p` | Show all exported environment variables | `export -p`: Lists all exported variables |
| `env VAR1=value COMMAND` | Set an environment variable for a specific command | `env VAR1=value command`: Runs a command with modified environment variables |

## 9. User Management Commands

Manage user accounts and groups.

| Command | Description | Examples |
|---------|-------------|----------|
| `who` | Show who is currently logged in | `who`: Displays the current logged-in users |
| `sudo adduser username` | Create a new user | `sudo adduser john`: Creates a new user named "john" |
| `finger` | Display information about users | `finger`: Displays user details |
| `last` | Show the recent login history | `last`: Displays login history |
| `sudo userdel -r username` | Delete a user account | `sudo userdel -r john`: Deletes the user "john" and their files |
| `su - username` | Switch to another user account | `su - john`: Switches to the "john" user account |
| `sudo usermod -a -G GROUPNAME USERNAME` | Add user to a group | `sudo usermod -a -G admin john`: Adds "john" to the "admin" group |

---

## 10. Shortcuts Commands

There are many shortcuts commands in Linux that can help you be more productive. Here are a few of the most common ones:

### 10.1: Bash Shortcuts Commands

| **Navigation** | **Description** | **Editing** | **Description** | **History** | **Description** |
|----------------|-----------------|-------------|-----------------|-------------|-----------------|
| **Ctrl + A** | Move to the beginning of the line. | **Ctrl + U** | Cut/delete from the cursor position to the beginning of the line. | **Ctrl + R** | Search command history (reverse search). |
| **Ctrl + E** | Move to the end of the line. | **Ctrl + K** | Cut/delete from the cursor position to the end of the line. | **Ctrl + G** | Escape from history search mode. |
| **Ctrl + B** | Move back one character. | **Ctrl + W** | Cut/delete the word before the cursor. | **Ctrl + P** | Go to the previous command in history. |
| **Ctrl + F** | Move forward one character. | **Ctrl + Y** | Paste the last cut text. | **Ctrl + N** | Go to the next command in history. |
| **Alt + B** | Move back one word. | **Ctrl + L** | Clear the screen. | **Ctrl + C** | Terminate the current command. |
| **Alt + F** | Move forward one word. |  |  |  |  |

---

### 10.2: Nano Shortcuts Commands

| **File Operations** | **Description** | **Navigation** | **Description** | **Editing** | **Description** | **Search and Replace** | **Description** |
|---------------------|-----------------|----------------|-----------------|-------------|-----------------|------------------------|-----------------|
| **Ctrl + O** | Save the file. | **Ctrl + Y** | Scroll up one page. | **Ctrl + K** | Cut/delete from the cursor position to the end of the line. | **Ctrl + W** | Search for a string in the text. |
| **Ctrl + X** | Exit Nano (prompt to save if modified). | **Ctrl + V** | Scroll down one page. | **Ctrl + U** | Uncut/restore the last cut text. | **Alt + W** | Search and replace a string in the text. |
| **Ctrl + R** | Read a file into the current buffer. | **Alt + \** | Go to a specific line number. | **Ctrl + 6** | Mark a block of text for copying or cutting. | **Alt + R** | Repeat the last search. |
| **Ctrl + J** | Justify the current paragraph. | **Alt + ,** | Go to the beginning of the current line. | **Ctrl + K** | Cut/delete the marked block of text. |  |  |
|  |  | **Alt + .** | Go to the end of the current line. | **Alt + 6** | Copy the marked block of text. |  |  |

---

### 10.3: VI Shortcuts Commands

| **Command** | **Description** |
|-------------|-----------------|
| **cw** | Change the current word. Deletes from the cursor position to the end of the current word and switches to insert mode. |
| **dd** | Delete the current line. |
| **x** | Delete the character under the cursor. |
| **R** | Enter replace mode. Overwrites characters starting from the cursor position until you press the Escape key. |
| **o** | Insert a new line below the current line and switch to insert mode. |
| **u** | Undo the last change. |
| **s** | Substitute the character under the cursor and switch to insert mode. |
| **dw** | Delete from the cursor position to the beginning of the next word. |
| **D** | Delete from the cursor position to the end of the line. |
| **4dw** | Delete the next four words from the cursor position. |
| **A** | Switch to insert mode at the end of the current line. |
| **S** | Delete the current line and switch to insert mode. |
| **r** | Replace the character under the cursor with a new character entered from the keyboard. |
| **i** | Switch to insert mode before the cursor. |
| **3dd** | Delete the current line and the two lines below it. |
| **ESC** | Exit from insert or command-line mode and return to command mode. |
| **U** | Restore the current line to its original state before any changes were made. |
| **~** | Switch the case of the character under the cursor. |
| **a** | Switch to insert mode after the cursor. |
| **C** | Delete from the cursor position to the end of the line and switch to insert mode. |

---

### 10.4: Vim Shortcuts Commands

#### Normal Mode

| **Command** | **Description** |
|-------------|-----------------|
| **i** | Enter insert mode at the current cursor position. |
| **x** | Delete the character under the cursor. |
| **dd** | Delete the current line. |
| **yy** | Copy the current line. |
| **p** | Paste the copied or deleted text below the current line. |
| **u** | Undo the last change. |
| **Ctrl + R** | Redo the last undo. |
| **:w** | Save the file. |
| **:q** | Quit Vim. |
| **:q!** | Quit Vim without saving changes. |
| **:wq** or **:x** | Save and quit Vim. |
| **:s/old/new/g** | Replace all occurrences of “old” with “new” in the file. |
| **:set nu** or **:set number** | Display line numbers. |

#### Command Mode

| **Command** | **Description** |
|-------------|-----------------|
| **:w** | Save the file. |
| **:q** | Quit Vim. |
| **:q!** | Quit Vim without saving changes. |
| **:wq** or **:x** | Save and quit Vim. |

#### Visual Mode

| **Command** | **Description** |
|-------------|-----------------|
| **v** | Enter visual mode to select text. |
| **y** | Copy the selected text. |
| **d** | Delete the selected text. |
| **p** | Paste the copied or deleted text. |

---

## 11. tmux - Terminal Multiplexer

`tmux` is a terminal multiplexer that allows you to manage multiple terminal sessions within one window. It’s great for running multiple programs simultaneously and for managing long-running processes.

### Basic `tmux` Commands

| Command | Description | Examples |
|---------|-------------|----------|
| `tmux` | Start a new tmux session | `tmux`: Starts a new tmux session |
| `tmux new-session -s session_name` | Start a new tmux session with a specific name | `tmux new-session -s my_session`: Starts a new session named "my_session" |
| `tmux attach -t session_name` | Attach to an existing tmux session | `tmux attach -t my_session`: Attaches to the session named "my_session" |
| `tmux ls` | List all tmux sessions | `tmux ls`: Lists all available tmux sessions |
| `tmux kill-session -t session_name` | Kill a specific tmux session | `tmux kill-session -t my_session`: Kills the "my_session" tmux session |
| `tmux detach` | Detach from the current tmux session | Press `Ctrl + b`, then `d`: Detaches from the current session |
| `tmux kill-session` | Kill the current tmux session | `tmux kill-session`: Kills the current session |

### Window and Pane Management

- **Windows**: Each tmux session can have multiple windows (like tabs in a browser).
- **Panes**: Each window can be split into multiple panes (like dividing your terminal screen).

| Command | Description | Examples |
|---------|-------------|----------|
| `Ctrl + b c` | Create a new window | `Ctrl + b c`: Creates a new window in the current session |
| `Ctrl + b n` | Switch to the next window | `Ctrl + b n`: Switches to the next window |
| `Ctrl + b p` | Switch to the previous window | `Ctrl + b p`: Switches to the previous window |
| `Ctrl + b 0-9` | Switch to a specific window | `Ctrl + b 2`: Switches to window 2 |
| `Ctrl + b w` | List all windows | `Ctrl + b w`: Lists all windows in the session |
| `Ctrl + b %` | Split the current window vertically | `Ctrl + b %`: Splits the window into two vertical panes |
| `Ctrl + b "` | Split the current window horizontally | `Ctrl + b "`: Splits the window into two horizontal panes |
| `Ctrl + b o` | Switch between panes | `Ctrl + b o`: Moves to the next pane |
| `Ctrl + b x` | Close the current pane | `Ctrl + b x`: Closes the current pane |
| `Ctrl + b {` | Move the current pane left | `Ctrl + b {`: Moves the current pane to the left |
| `Ctrl + b }` | Move the current pane right | `Ctrl + b }`: Moves the current pane to the right |

### Session and Window Management

| Command | Description | Examples |
|---------|-------------|----------|
| `Ctrl + b d` | Detach from the session | `Ctrl + b d`: Detaches from the session and leaves it running in the background |
| `Ctrl + b &` | Close the current window | `Ctrl + b &`: Closes the current window |
| `Ctrl + b ,` | Rename the current window | `Ctrl + b ,`: Renames the current window to a new name |
| `Ctrl + b s` | List all sessions | `Ctrl + b s`: Lists all active tmux sessions |
| `Ctrl + b l` | List the last window | `Ctrl + b l`: Switches to the last active window |

### Resizing Panes

You can resize tmux panes to allocate more space for one particular pane.

| Command | Description | Examples |
|---------|-------------|----------|
| `Ctrl + b :` | Enter command mode | `Ctrl + b :`: Enter command mode to type tmux commands |
| `resize-pane -D` | Resize pane down | `Ctrl + b :resize-pane -D`: Shrinks the pane downward |
| `resize-pane -U` | Resize pane up | `Ctrl + b :resize-pane -U`: Shrinks the pane upward |
| `resize-pane -L` | Resize pane left | `Ctrl + b :resize-pane -L`: Shrinks the pane left |
| `resize-pane -R` | Resize pane right | `Ctrl + b :resize-pane -R`: Shrinks the pane right |

### Saving and Restoring Sessions

You can save your tmux sessions and restore them later.

| Command | Description | Examples |
|---------|-------------|----------|
| `tmux save-buffer /path/to/file` | Save the buffer contents to a file | `tmux save-buffer output.txt`: Saves the buffer to a file named "output.txt" |
| `tmux load-buffer /path/to/file` | Load content from a file into the buffer | `tmux load-buffer output.txt`: Loads content from "output.txt" into the tmux buffer |

### Copy and Paste Mode

You can enter copy mode in tmux to scroll through the terminal output and copy text.

| Command | Description | Examples |
|---------|-------------|----------|
| `Ctrl + b [` | Enter copy mode | `Ctrl + b [`: Enter copy mode |
| `Up/Down Arrow` | Scroll through the terminal output | Use the arrow keys to scroll through the terminal |
| `Space` | Start selection | `Space`: Starts selecting text |
| `Enter` | Copy selected text | `Enter`: Copies the selected text |
| `Ctrl + b ]` | Paste the copied text | `Ctrl + b ]`: Pastes the copied text into the current pane |

---

These are some of the basic and advanced `tmux` commands that will help you get started with terminal multiplexing. You can create, manage, and navigate between multiple terminal sessions with ease, making tmux an invaluable tool for anyone working in the terminal.


## Conclusion

In conclusion, Linux is a widely used operating system for development, and as a developer, you should have knowledge of Linux and its basic commands. In this Cheat Sheet, we covered all commands like creating directories, file compression and archiving, process management, system information, networking, and more. In addition to that, this Linux Cheat Sheet is organized and categorized, making it easy for developers to quickly find the commands they need for specific use cases. By utilizing this resource, developers can enhance their productivity and efficiency in working with Linux, leading to smoother and more successful development projects.
