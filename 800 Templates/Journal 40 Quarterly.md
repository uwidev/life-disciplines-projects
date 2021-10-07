---
tags: [ note/data ] 
---
[[<% tp.date.now("YYYY-[Q]Q", "P-3M", tp.file.title, "YYYY-[Q]Q") %>]] | [[<% tp.date.now("YYYY-[Q]Q", "P3M", tp.file.title, "YYYY-[Q]Q") %>]]
# <% tp.date.now("YYYY-[Q]Q", 0, tp.file.title, "YYYY-[Q]Q") %> 
## Fun
**Copy and paste the first quote within last quarter (<= 3 months ago) from [/r/quotes: For your favorite quotes](https://www.reddit.com/r/quotes/top/?t=year).
**
> Quote goes here
> — <cite>Author</cite>

`Your opnions on this quote here. Why do you think became the quarterly top?`

## Performance
### Projects
```dataview
TABLE WITHOUT ID
	link(file.name, default(aliases, file.name)) as "Project",
	start as "Start",
	end as "End",
	status as "Status",
	link(discipline, default(link(discipline).aliases, file.name)) as Discipline
FROM #note/project 
WHERE start >= date(<% tp.date.now("YYYY-MM-DD", "P-3M", tp.file.title, "YYYY-[Q]Q") %>) 
	and start < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-[Q]Q") %>) + dur(1 day)
	or end >= date(<% tp.date.now("YYYY-MM-DD", "P-3M", tp.file.title, "YYYY-[Q]Q") %>)
	and end < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-[Q]Q") %>) + dur(1 day)
	or file.mtime > date(<% tp.date.now("YYYY-MM-DD", "P-3M", tp.file.title, "YYYY-[Q]Q") %>)
	and file.mtime < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-[Q]Q") %>) + dur(1 day)
sort end, status
```

## Alignment
```dataview
TABLE WITHOUT ID
	pillars as "Life Pillars"
FROM "/"
WHERE contains(file.aliases, "💗 Life")
```
```dataview
TABLE WITHOUT ID
	dynamic as "Life Dynamic"
FROM "/"
WHERE contains(file.aliases, "💗 Life")
```
```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, link(file.name).name)) as "Discipline",
	dynamic as "Dynamic"
FROM #note/discipline and -"900 Archive" and -"Templates"
```
**For each Discipline, are they still relevant and important towards at least one Life Pillars? Do they allow mobility towards them? Which Life Pillars? How and Why?**

### Discipline 1
`Answer`

### Discipline 2
`Answer`

## Adjustment
**Are there any changes that need to be made to your Disciplines? What will be changed, if anything? How and why? If not needed, why?**
`Answer`

## Ramblings
`Random quarterly ramblings go here`