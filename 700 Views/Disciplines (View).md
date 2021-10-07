```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, link(file.name).name)) as "Discipline",
	pillars as "Pillars",
	dynamic as "Dynamic"
FROM #note/discipline and -"900 Archive" and -"Templates"
SORT due asc
```