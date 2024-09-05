---
summary: List of Basic Linux Commands used for navigating file system and creating/deleting files and directories
tags:
  - coursenote
---
^ [[Linux Overview]] | 
# Basic Linux Commands
##### 'pwd' (print working directory): prints current directory
```
username:~$ pwd
/home/username
```
The first slash represents the root directory. 'home' represents a subdirectory of the root directory named home. 'username' represents a subdirectory of the home directory.

| **Command**                                              | **Function**                                                   | **notable arguments**                                                                                                                                                                                                                  |
| -------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| '[ls](#ls%20example)' (list)                                              | lists contents of current directory                            | -l (L) argument which displays detailed information about listed files and directories: permissions, owner, size, modification date. [See here for information on how to interpret this](How%20to%20read%20'ls%20-l'.md) |
| 'clear'                                                  | clears terminal                                                |                                                                                                                                                                                                                                        |
| '[cd](#cd%20example)' (change directory)                                  | changes directory to home directory                            | 'cd ..' moves one layer out of the current directory <br> 'cd -' goes back to the previous directory <br> 'cd {directory}' moves to the given directory                                                                                |
| 'exit'                                                   | closes terminal                                                |                                                                                                                                                                                                                                        |
| '[mkdir](#mkdir%20example) {directory}'                                      | creates a new directory in current dir ==only if it is empty== | -r deletes everything in the directory as well as the directory itself                                                                                                                                                                 |
| 'touch {file_name}''                                     | creates file with given name                                   |                                                                                                                                                                                                                                        |
| '[rm](#rm%20example) {file_name}'                                         | deletes given file                                             |                                                                                                                                                                                                                                        |
| '[cp](#cp%20command%20example) {file_name} {directory_name}'                        | copies given file to given directory                           |                                                                                                                                                                                                                                        |
| 'mv {file_name} {directory_name}'                        | moves given file to given directory                            |                                                                                                                                                                                                                                        |
| '[chmod {u/g/o} {+/-} {file_name}](Linux%20File%20Permissions.md)' | changes permissions of given file according to args            |                                                                                                                                                                                                                                        |

##### ls example
```
username:~$ ls
poop      username      desktop        templates
```

##### cd example
```
username:~$ pwd
/home/username/poop/test/pee
username:~$ cd
username:~$ pwd
/home/username
```

##### 'mkdir example
- 'rmdir {directory_name}': deletes directory ==only if it is empty==
- 'rm -r {directory_name}': deletes everything in the directory as well as the directory itself
```
username:~$ mkdir pee
username:~$ ls
poop      username      desktop        templates       pee
username:~$ rmdir pee
username:~$ ls
poop      username      desktop        templates
```

##### rm example
```
username:~$ ls
home
username:~$ touch chungus
username:~$ ls
home        chungus
username:~$ rm chungus
username:~$ ls
home
```

##### cp command example
```
username:~$ mkdir pee
username:~$ touch poop
username:~$ ls
home        pee       poop
username:~$ cp poop /pee
username:~$ cd '/pee'
username:~$ ls
poop
```