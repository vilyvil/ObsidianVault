---
summary: Explanation of Soft and Hard file links
tags:
  - coursenote
---
^ [[How to read 'ls -l']] | 

# File Links
Pointers to files. Like creating a shortcut to a file, links allow more than one file to refer to the same binary file.

## Hard Link
Reference the same physical file locations. If the file is moved or DELETED, hard link will still remain linked. Hard links cannot be created for directories.
Hard links contain the contents of the original file, and as such have the same size and contents. ==If one of the hard links' contents are updated, all the rest are too.==
Cannot be shared across file systems.

## Soft Link
Most like file shortcuts
Holds the path name of the target file. As a result, does not follow the file when it is moved or renamed.
Require less space than hard links, as the file doesn't have to be duplicated.