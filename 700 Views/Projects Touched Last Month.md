```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, file.name)) as "Project",
	objective as "Objective",
	link(discipline, link(discipline).aliases) as "Discipline"
FROM #note/project
WHERE file.mtime >= date(today) - dur(1 month) and file.mtime < date(today)
SORT due asc
```