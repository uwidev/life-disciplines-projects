```dataview
TABLE WITHOUT ID
	link(file.name, default(aliases, name)) as "Ikigai(s)",
	dynamic as "Dynamic"
FROM #note/ikigai 
```
```dataview
TABLE WITHOUT ID
	link(file.name, default(aliases, name)) as "Ikigai(s)",
	pillars as "Pillars"
FROM #note/ikigai 
```