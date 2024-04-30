This Basic Linux Commands Cheat Sheet provides a comprehensive overview of essential commands and shortcuts for navigating and managing Linux systems efficiently. It covers topics from file management and viewing to system information, process management, and more. Ideal for both beginners and experienced users, this guide serves as a quick reference to enhance productivity and simplify everyday tasks on Linux.

## File Management

### ls – List Directory Contents
- **Usage:** `ls [options] [directory]`
- **Common Options:**
  - `-l`: Long listing format
  - `-a`: Include hidden files
  - `-h`: Human-readable sizes

### cp – Copy Files or Directories
- **Usage:** `cp [options] source destination`
- **Common Options:**
  - `-r`: Recursively copy directories
  - `-i`: Prompt before overwrite
  - `-v`: Verbose mode, show files as they are copied

### mv – Move or Rename Files or Directories
- **Usage:** `mv [options] source destination`
- **Common Options:**
  - `-i`: Prompt before overwrite
  - `-u`: Move only when the source file is newer than the destination file or when the destination file is missing

### rm – Remove Files or Directories
- **Usage:** `rm [options] file`
- **Common Options:**
  - `-r`: Recursively remove directories and their contents
  - `-f`: Force removal without prompt
  - `-v`: Verbose mode, show files as they are removed

### mkdir – Create New Directories
- **Usage:** `mkdir [options] directory`
- **Common Options:**
  - `-p`: Make parent directories as needed
  - `-v`: Verbose mode, show directories as they are created

### rmdir – Remove Empty Directories
- **Usage:** `rmdir [options] directory`
- **Common Options:**
  - `-p`: Remove directory and its empty ancestors
  - `-v`: Verbose mode, show directories as they are removed

### touch – Create an Empty File or Update the Access and Modification Times of a File
- **Usage:** `touch [options] file`
- **Common Options:**
  - `-a`: Change only the access time
  - `-m`: Change only the modification time
  - `-t`: Set a specific time (`touch -t 202012101830 file`)


## File Viewing & Editing

### cat – Concatenate and Display Files
- **Usage:** `cat [options] [file...]`
- **Common Options:**
  - `-n`: Number all output lines
  - `-b`: Number non-empty output lines
  - `-s`: Squeeze multiple adjacent empty lines

### more – View File Contents Interactively
- **Usage:** `more [options] [file]`
- **Description:** Allows file content to be viewed one screen at a time
- **Navigation:**
  - `Space`: Next page
  - `Enter`: Next line
  - `q`: Quit more

### less – View File Contents Interactively with Improved Features
- **Usage:** `less [options] [file]`
- **Description:** Like `more`, but allows backward movement in the file as well as forward movement
- **Navigation:**
  - `Space`: Next page
  - `b`: Previous page
  - `/`: Search for a string
  - `n`: Repeat previous search
  - `q`: Quit less

### nano – Simple Text Editor
- **Usage:** `nano [options] [file]`
- **Description:** Easy-to-use, modeless text editor
- **Common Shortcuts:**
  - `Ctrl+O`: Save file
  - `Ctrl+X`: Exit editor
  - `Ctrl+K`: Cut current line
  - `Ctrl+U`: Paste cut text

### vi / vim – Advanced Text Editor
- **Usage:** `vi [options] [file]`
- **Description:** Modal text editor with multiple modes for editing and command input
- **Common Modes:**
  - `Normal`: For navigating and editing text
  - `Insert`: For inserting text
  - `Command`: For performing commands like saving and exiting
- **Common Commands:**
  - `i`: Enter insert mode
  - `Esc`: Return to normal mode
  - `:w`: Save file
  - `:q`: Quit (use `:q!` to quit without saving)
  - `:wq`: Save and quit


## System Information

### uname – Print System Information
- **Usage:** `uname [options]`
- **Common Options:**
  - `-a`: Display all available system information
  - `-r`: Print the kernel release
  - `-m`: Display the machine hardware name

### top – Display Active Processes
- **Usage:** `top`
- **Description:** Provides a dynamic real-time view of a running system, showing system summary and a list of tasks currently managed by the kernel
- **Key Commands:**
  - `Shift + p`: Sort by CPU usage
  - `Shift + m`: Sort by memory usage
  - `k`: Kill a process
  - `q`: Quit top

### df – Report File System Disk Space Usage
- **Usage:** `df [options] [file...]`
- **Common Options:**
  - `-h`: Human-readable, shows sizes in GB, MB, or KB
  - `-T`: Show file system type
  - `-i`: Show inode information

### du – Estimate File Space Usage
- **Usage:** `du [options] [directory]`
- **Common Options:**
  - `-h`: Human-readable, show sizes in GB, MB, or KB
  - `-s`: Summarize total for each argument
  - `-a`: Show disk usage for all files, not just directories

### free – Display Memory Usage
- **Usage:** `free [options]`
- **Common Options:**
  - `-h`: Human-readable, show sizes in GB, MB, or KB
  - `-m`: Show output in MB
  - `-g`: Show output in GB
- **Description:** Shows the total amount of free and used physical and swap memory in the system, as well as the buffers and caches used by the kernel



## Process Management

### ps – Report a Snapshot of Current Processes
- **Usage:** `ps [options]`
- **Common Options:**
  - `-e`: List all processes
  - `-f`: Full format listing
  - `-u user`: List processes owned by `user`

### kill – Send a Signal to a Process
- **Usage:** `kill [options] [pid]`
- **Common Options:**
  - `-9`: Force kill process
  - `-SIGTERM`: Graceful stop
  - `-SIGKILL`: Immediate termination
- **Description:** Send a signal specified by `pid`. The default signal is `SIGTERM`.

### pkill – Send a Signal to a Process Based on Name or Other Attributes
- **Usage:** `pkill [options] pattern`
- **Common Options:**
  - `-u user`: Kill processes owned by `user`
  - `-SIGTERM`, `-SIGKILL`: Specify the signal to send
- **Description:** Kills processes based on a name or other attributes, making it easier to target multiple processes at once.

### jobs – List Active Jobs
- **Usage:** `jobs`
- **Description:** Displays status of jobs in the current session, showing their job number, state (e.g., running, stopped), and command.

### bg – Resume Suspended Jobs in the Background
- **Usage:** `bg [job_specification]`
- **Description:** Continues suspended jobs by running them in the background, as if they had been started with `&`.

### fg – Resume Suspended Jobs in the Foreground
- **Usage:** `fg [job_specification]`
- **Description:** Moves jobs to the foreground, making them the current active task, and allows for direct interaction.



## Permissions & Ownership

### chmod – Change File Access Permissions
- **Usage:** `chmod [options] mode file`
- **Description:** Changes the permissions of a file or directory.
- **Common Usage:**
  - `chmod 755 file`: Sets read, write, and execute permissions for the owner, and read and execute permissions for others.
  - `chmod u+x file`: Adds execute permission for the owner.

### chown – Change File Owner and Group
- **Usage:** `chown [options] owner[:group] file`
- **Description:** Changes the owner and/or group of one or more files.
- **Common Usage:**
  - `chown user file`: Changes the owner of `file` to `user`.
  - `chown user:group file`: Changes both the owner and group of `file` to `user` and `group`.

### umask – Set the Default File Permissions
- **Usage:** `umask [mask]`
- **Description:** Sets the default permission or file creation mask for the session.
- **Common Usage:**
  - `umask 022`: Sets the default creation permissions to 755 (rwxr-xr-x).
- **Note:** The umask value subtracts permissions from the system default, typically `666` for files and `777` for directories.



## Networking

### ping – Check Network Connection to Another Host
- **Usage:** `ping [options] hostname_or_ip`
- **Description:** Sends ICMP ECHO_REQUEST packets to a network host to measure how long messages take to come back.
- **Common Options:**
  - `-c count`: Stop after sending (and receiving) count ECHO_RESPONSE packets
  - `-i interval`: Wait interval seconds between sending each packet

### ifconfig / ip – Configure or Display Network Interface Parameters
- **Usage for ifconfig:** `ifconfig [options]`
- **Usage for ip:** `ip [options]`
- **Description:**
  - `ifconfig`: Used to configure, manage, and query network interface parameters.
  - `ip`: More powerful and preferred tool in modern Linux systems for routing and network interface management.
- **Common Usage:**
  - `ifconfig`: Shows all active interfaces when used without parameters.
  - `ip addr show`: Lists all interfaces and their IP addresses.

### netstat – Display Network Connections, Routing Tables, Interface Statistics
- **Usage:** `netstat [options]`
- **Description:** Displays various network related information such as network connections, routing tables, interface statistics, masquerade connections, multicast memberships, etc.
- **Common Options:**
  - `-r`: Shows the routing table
  - `-t`: Show TCP connections
  - `-u`: Show UDP connections

### scp – Secure Copy (Remote File Copy Program)
- **Usage:** `scp [options] source_file destination_file`
- **Description:** Copies files between hosts on a network. It uses SSH for data transfer and provides the same authentication and same level of security as SSH.
- **Common Usage:**
  - `scp file.txt user@remote:/path`: Copies `file.txt` to the specified path on the remote host.

### ssh – Secure Shell to Connect to a Remote Machine
- **Usage:** `ssh [options] user@host`
- **Description:** SSH is a protocol for securely logging into remote machines across a network. It provides secure encrypted communications.
- **Common Options:**
  - `-p port`: Connect to the specified port
  - `-i key_file`: Use the specified SSH key for authentication



## Archiving and Compression

### tar – Archive Files
- **Usage:** `tar [options] [archive-file] [files or directories]`
- **Description:** Combines multiple files into a single archive file and can restore files from this archive.
- **Common Options:**
  - `-c`: Create a new archive
  - `-x`: Extract files from an archive
  - `-v`: Verbosely list files processed
  - `-f`: Use archive file or device ARCHIVE
  - `-z`: Filter the archive through gzip
  - `-j`: Filter the archive through bzip2

### gzip – Compress or Decompress Files
- **Usage:** `gzip [options] [files]`
- **Description:** Compresses files using the Lempel-Ziv coding (LZ77), replacing them with a gzipped compressed version.
- **Common Options:**
  - `-d`: Decompress
  - `-l`: List compression information
  - `-r`: Recursively compress files in directories

### zip / unzip – Compress and Decompress Files
- **Usage for zip:** `zip [options] [archive-file] [files]`
- **Usage for unzip:** `unzip [options] [archive-file]`
- **Description:**
  - `zip`: Package and compress (archive) files.
  - `unzip`: Extract files from ZIP archives.
- **Common Options for zip:**
  - `-r`: Recursively zip everything in a directory
  - `-e`: Encrypt the contents of the zip file (will prompt for password)
- **Common Options for unzip:**
  - `-l`: List the contents of a ZIP file without extracting
  - `-d directory`: Extract files into `directory`



## Search
### find – Search for Files in a Directory Hierarchy
- **Usage:** `find [path...] [expression]`
- **Description:** Locates files in a directory hierarchy based on conditions specified such as name, size, modification time, etc.
- **Common Options:**
  - `-name 'pattern'`: Search for files that match the pattern
  - `-type f`: Only search for files
  - `-type d`: Only search for directories
  - `-size +2M`: Find files larger than 2 megabytes
  - `-mtime -10`: Find files modified within the last 10 days

### grep – Search Text Using Patterns
- **Usage:** `grep [options] pattern [file...]`
- **Description:** Searches for text within files. It can use simple text, strings, or regular expressions to match patterns.
- **Common Options:**
  - `-i`: Ignore case distinctions in both the pattern and the input files.
  - `-r`: Recursively search subdirectories listed.
  - `-v`: Invert the sense of matching, to select non-matching lines.
  - `-l`: Only display filenames of files where the content matches the pattern.




## Shortcuts and Tips

### Useful Bash Shortcuts
- **Ctrl + C**: Terminate the current command.
- **Ctrl + Z**: Suspend the current command.
- **Ctrl + D**: Exit the current shell (when no process is running).
- **Ctrl + L**: Clear the screen.
- **Ctrl + A**: Move cursor to the beginning of the line.
- **Ctrl + E**: Move cursor to the end of the line.
- **Ctrl + U**: Clears the typing before the cursor and copies it to the clipboard.
- **Ctrl + K**: Clears the typing after the cursor and copies it to the clipboard.
- **Ctrl + W**: Delete the word before the cursor and copy it to the clipboard.
- **Ctrl + Y**: Paste the last thing to be cut (with Ctrl+U/K/W).

### Command History Tricks
- **history**: Show command history.
- **!n**: Execute the nth command in the history list.
- **!!**: Execute the last command again.
- **!pattern**: Execute the last command that starts with 'pattern'.
- **Ctrl + R**: Search through previous commands (type to search, press Ctrl+R to cycle through matches, Enter to execute).
- **^old^new^**: Repeat the last command, replacing 'old' with 'new'.

### Useful Links
- [Linux Command Line Basics](https://linuxjourney.com/lesson/the-shell): An introductory guide to the Linux command line.
- [GNU Core Utilities Documentation](https://www.gnu.org/software/coreutils/manual/coreutils.html): Official documentation for GNU core utilities.
- [Explain Shell](https://explainshell.com/): Type in a command to see the help text that matches each argument.
