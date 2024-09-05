^ [[Home Page]] | 
[[#Todo]] | [[#List of Course Notes]] | [[#List of all Notes]]
# To do
```dataview
table
summary as "Summary", file.cday as "Date"
from "Notes/School/Y1/S1/CPSC 231" and #coursenote and #todo
where file.name != "CPSC 231"
sort file.ctime desc
```

# List of Course Notes
```dataview
table
summary as "Summary", file.cday as "Date"
from "Notes/School/Y1/S1/CPSC 231" and #coursenote
where file.name != "CPSC 231"
sort file.ctime desc
```

# List of all Notes
%% Begin Waypoint %%
- **Introductory Notes**
	- [[History of Computers]]
	- [[Operating Systems]]
	- [[Problem Solving]]
- **Introductory Notes (admin)**
	- [[Academic Integrity in Computer Science]]
	- [[How to be Successful]]
	- [[Introduction Info]]
- **Linux**
	- [[Basic Linux Commands]]
	- [[File Links in Linux]]
	- [[How to read 'ls -l']]
	- [[Linux File Permissions]]
	- [[Linux Overview]]

%% End Waypoint %%

#exception