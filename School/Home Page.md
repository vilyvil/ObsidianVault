### Unfinished Notes
```dataview
table 
summary as "Summary", substring(file.folder, 19, 27) as "Subject Name", file.ctime as "Creation time"
from "repo/School/Y2" and -#finished and -#exception
where file.name != "Note Template"
sort file.ctime desc
```
---

| Course Pages |
| ------------ |
| [[CPSC 355]] |
| [[PHIL 314]] |
| [[CPSC 331]] |
| [[CPSC 329]] |
# Notes Marked Important (Overviews, Summaries, etc.)
```dataview
table 
summary as "Summary", substring(file.folder, 19, 27) as "Subject Name"
from #important and "Notes/School/Y2"
where file.name != "Note Template"
sort file.ctime desc
```

# Mistakes?
```dataview
table
from "Y2" and -#coursenote and -#exception
```