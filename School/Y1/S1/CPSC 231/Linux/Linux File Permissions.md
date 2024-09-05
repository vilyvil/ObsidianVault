---
summary: Explanation of file permissions and how to change them
tags:
  - coursenote
---
^ [[Linux Overview]] | [[How to read 'ls -l']]
## File Permission
### u/g/o
- user
	- you
- group
	- people who belong in a specific group
- other
	- everyone with access to this computer
### r/w/x
- r
	- read perms
- w
	- write perms
- x
	- execute file or go into directory
# Command to change file perms
### chmod \[u/g/o] \[+/-] \[file_name]
```shell
username:~/Desktop$ ls -l
-rw-rw-r-- username username {size} {datetime} untitled.txt
username:~/Desktop$ chmod u+rwx untitled.txt
username:~/Desktop$ ls -l
-rwxrw-r-- username username {size} {datetime} untitled.txt
```
[See here](How%20to%20read%20'ls%20-l'.md) for more information on how to readthe information given by ls -l