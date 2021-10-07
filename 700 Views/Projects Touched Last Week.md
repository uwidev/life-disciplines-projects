```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, file.name)) as "Project",
	objective as "Objective",
	link(discipline, link(discipline).aliases) as "Discipline"
FROM #note/project
WHERE file.mtime < date(today) + dur(1 days) and file.mtime > date(today) - dur(7 days)
SORT due asc
```