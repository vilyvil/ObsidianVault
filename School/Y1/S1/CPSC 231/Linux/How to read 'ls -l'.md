---
summary: How to read the information given by ls -l
tags:
  - coursenote
---
^ [[Basic Linux Commands]] |
# Explanation of ls -l information
```shell
username:~/Desktop$ ls -l
-r--r--r-- 1 username username 1000 Sep 13 14:48 untitled.txt
drwxrw-r-- 1 username username 4096 Sep 12 13:20 'Test'
```
Each file is given its own line. In order, the file's information is listed:

| No  | Column Name                                         | Description                                                                                                          |
| --- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| 1   | [Permissions](Linux%20File%20Permissions.md)           | First character shows file type (d for directory and - for file). <br> The rest show file permissions in u/g/o order |
| 2   | [File Links in Linux](File%20Links%20in%20Linux.md) | Number of hard links to this file or directory                                                                       |
| 3   | Owner                                               | User owner of file or directory                                                                                      |
| 4   | Group                                               | Group owner of file or directory                                                                                     |
| 5   | Size                                                | Size, default bytes                                                                                                  |
| 6   | Date                                                | Last modification date                                                                                               |
| 7   | Time                                                | Last modification time                                                                                               |
| 8   | Name                                                | Name of the file/directory                                                                                           |