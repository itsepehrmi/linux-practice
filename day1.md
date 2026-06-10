# Day 1 - [Day 1 - 05-06-2026]

Today I completed Chapter 1 of "Linux Basics for Hackers".
I learned essential Linux commands for navigating the filesystem, finding files, and managing processes.

## Commands I learned:

### Navigation & Directory
- `pwd` - print current working directory
- `cd` - Change directory
- `ls`, `ls -la` - List files (with details and hidden files)

### Getting Help
- `-h`, `--help` - Show help for a command
- `man` - Display the manual page for a command

### Finding Files & Programs
- `locate` - Quickly find files by name (uses database)
- `whereis` - Locate binary, source, and manual page for a command
- `which` - Show full path of a cammand's executable

### Processes
- `ps` - Display current processes

### Working with Files & Directories
- `cat` - Display file content
- `touch` - Create an empty file or update timestamp
- `mkdir` - Create a new directory
- `cp` - Copy files or directories
- `mv` - Move or rename files/directories
- `rm`, `rmdir`, `rm -r` - Remove files or directories recursively

## Examples I ran in my terminal:

pwd
/home/user/linux-practice

mkdir myfolder
touch myfile.txt
cp myfile.txt /myfolder
mv myfile.txt newfile.txt
rm newfile.txt

Notes:

. ls -la shows hidden files (starting with .)
which is useful for finding configuration files.
.Always use man before googling-it's faster
and builds memory.
.rm -r is dangerous;double-check your path
before using it.

Next goal:

. learn about TEXT MANIPULATION
from Chapter 2.
