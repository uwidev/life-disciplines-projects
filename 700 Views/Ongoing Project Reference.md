### Ongoing Project Reference
```dataview
TABLE objective as "Objective"
FROM #note/project and -"888 Templates"
WHERE status = "00 Ongoing" or status = "02 Planned" and file.name != "Dashboard Project"
SORT due asc, urgent asc, important asc
```
### CC
```dataview
TASK
FROM #note/project and !"Templates"
WHERE file.status = "00 Ongoing" or file.status = "01 Blocked" or file.status = "02 Planned" or file.status = "03 On-Hold" and name != "Dashboard Project"
```