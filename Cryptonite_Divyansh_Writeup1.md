1. HELLO

1) The first task was very basic as we were given a command to just copy paste into the terminal
2) In the second task we were told about the difference between a command and arguments

	basically the first keyword is the command and all the other words following it are the 	arguments.

2. PONDERING PATHS

1) Very basic as we just had to do ‘/pwn’ and got the flag
2) here we had the executable file inside another directory so we again had a basic comman ‘/challenge/run’ and got the flag
3)        cd /challenge
	./run
6) Here we learned the difference between relative and absolute paths
7) here we got to knwo about explicit relavite paths amd how things like ‘././.../’ might work
8)

3. COMMANDS

In-Depth Overview of Linux Commands

1. cat
   - Usage: `cat [options] [file...]`
   - Basic Arguments:
     - `<filename>`: Displays the contents of the specified file.
     - `-n`: Numbers all output lines.
     - `-E`: Displays a `$` at the end of each line.
   - Example: 
     ```bash
     cat -n file.txt
     ```

2. grep
   - Usage: `grep [options] [pattern] [file...]`
   - Basic Arguments:
     - `<pattern>`: The text or regular expression to search for.
     - `<filename>`: The file(s) to search within.
     - `-i`: Ignores case distinctions.
     - `-r`: Recursively searches through directories.
   - Example:
     ```bash
     grep -i "error" logfile.txt
     ```

3. Listing Files
   - Command: `ls`
   - Basic Arguments:
     - `-l`: Displays detailed information about each file.
     - `-a`: Lists all files, including hidden files.
     - `-h`: Formats file sizes in a human-readable way.
   - Example:
     ```bash
     ls -la
     ```

4. Touching Files
   - Usage: `touch [options] [file...]`
   - Basic Arguments:
     - `<filename>`: Creates a new, empty file or updates the timestamp.
     - `-c`: Does not create files; only updates timestamps.
   - Example:
     ```bash
     touch newfile.txt
     ```

5. Removing Files
   - Usage: `rm [options] [file...]`
   - Basic Arguments:
     - `<filename>`: Specifies the file(s) to delete.
     - `-r`: Recursively deletes directories and their contents.
     - `-f`: Forces deletion without prompting for confirmation.
   - Example:
     ```bash
     rm -rf directory_name
     ```

6. Making Directories
   - Usage: `mkdir [options] [directory...]`
   - Basic Arguments:
     - `<directory>`: The name of the directory to create.
     - `-p`: Creates parent directories as needed.
   - Example:
     ```bash
     mkdir -p /home/user/newfolder/subfolder
     ```

7. Finding Files
   - Usage: `find [path] [options] [expression]`
   - Basic Arguments:
     - `<path>`: The directory path to start the search.
     - `-name`: Searches for files matching a specific name pattern.
     - `-type`: Searches for a specific type (e.g., `f` for files, `d` for directories).
   - Example:
     ```bash
     find /home/user -name "*.txt"
     ```

8. Linking Files
   - Usage: `ln [options] <target> [link_name]`
   - Basic Arguments:
     - `<target>`: The file you want to link to.
     - `<link_name>`: The name of the new link.
     - `-s`: Creates a symbolic link instead of a hard link.
   - Example:
     ```bash
     ln -s /path/to/original_file link_name
     ```

-- there are 2 kinds of link: 
1. hard link – 2 addresses that lead to the same place
2. soft link

symbolic link- (ln -s)

4. DIGESTING DOCUMENTATION -

This module was all about how to use man and –help. It was very basic commands 
	
we can do ‘man [name of command]’ to get a list of possible arguments with their description

/ - used to search for a keyword in man description
n – used to move down
N- sed to move up


5. FILE GLOBBING

‘*”-  When linux encounters a ‘*’ character in any argument, the shell will treat it as "wildcard" and try to replace that argument with any files that match the pattern.

‘?’ is simial to * but it only matches that one character in that specified place

[] is like ? That matches a possible subsets of potential characters within the set

in [] we can use ! Or in newer versions ^ to exclude certain characters

6. PIPPING

Piping in Linux is a way to connect the output of one command directly into the input of another command.

‘>’ can be used to redirect the stdout to other files

‘>>’ can be used to append the stdout to other files

File Descriptor- 
	FD0-stdin
	FD1-stdout
	FD2-stderror


by default when we use > we mean 1>

6) /challenge/run > /tmp/data.txt
grep "pwn.college{" /tmp/data.txt

7) /challenge/run | grep "pwn.college{"

8) /challenge/run 2>&1 | grep "pwn.college{"

9)

