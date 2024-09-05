---
summary: Introduction to Linux shell, file system, commands
tags:
  - coursenote
---
# Linux Shell
The original user interface of Linux, in the form of a command-line interface
### Commands
Commands can be inputted to and thus executed by the shell. 
These commands can do a wide range of things, from file management and system config to running programs and processes.

Here is a list of the basic ones: [[Basic Linux Commands]]
### Scripts
Scripts are sequences of commands saved in a script file which can be used to automate series of tasks.

# Linux File System
Linux allows the organization of files through the use of directories (you can think of these as folders). The highest level directory, which contains all other directories, is called the root directory.
- This structure creates a hierarchical tree-like structure starting with the root directory.
- Folders contained in a directory are called its subdirectories. All directories are subdirectories of the root or subdirectories of those.

The shell can be used to navigate the computer's directories and create, copy, move, and delete files and directories. Other file management tasks are also available.

Additionally, each file has permissions attributed to it which control who has permissions to read, write, and execute that file. For more information on this, as well as to change permissions, see here: [[Linux File Permissions]].