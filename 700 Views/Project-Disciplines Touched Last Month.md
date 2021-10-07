```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, link(file.name).name)) as "Discipline",
	pillars as "Pillars",
	dynamic as "Dynamic"
FROM #note/discipline and -"Templates"
WHERE end < date(today) + dur(1 days) or start > date(today) - dur(7 days) or (file.mtime < date(today) + dur(1 days) and file.mtime > date(2021-09-27) - dur(7 days))
SORT due asc
```