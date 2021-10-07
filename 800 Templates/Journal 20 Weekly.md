---
tags: [ note/data ] 
---
[[<% tp.date.now("gggg-[W]ww", "P-1W", tp.file.title, "gggg-[W]ww") %>]] | [[<% tp.date.now("gggg-[W]ww", "P1W", tp.file.title, "gggg-[W]ww") %>]]
# <% tp.date.now("gggg-[W]ww", 0, tp.file.title, "gggg-[W]ww") %> 
## Fun
**Copy and paste the first quote within last quarter (<= 3 months ago) from [/r/quotes: For your favorite quotes](https://www.reddit.com/r/quotes/top/?t=year).
**
> Quote goes here
> — <cite>Author</cite>

`Your opnions on this quote here. Why do you think became the weekly top?`

## Review
![[<% tp.date.now("gggg-[W]ww", "P-1W", tp.file.title, "gggg-[W]ww") %>#Analysis]]
![[<% tp.date.now("gggg-[W]ww", "P-1W", tp.file.title, "gggg-[W]ww") %>#Reflection]]
![[<% tp.date.now("gggg-[W]ww", "P-1W", tp.file.title, "gggg-[W]ww") %>#Concerns]]
![[<% tp.date.now("gggg-[W]ww", "P-1W", tp.file.title, "gggg-[W]ww") %>#Ramblings]]

## Performance
### Projects
```dataview
TABLE WITHOUT ID
	link(file.name, default(aliases, file.name)) as "Project",
	status as "Status",
	file.mtime as "Last Modified"
FROM #note/project 
WHERE start >= date(<% tp.date.now("YYYY-MM-DD", "P-1W", tp.file.title, "gggg-[W]ww") %>) 
	and start < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>) + dur(1 day)
	or end >= date(<% tp.date.now("YYYY-MM-DD", "P-1W", tp.file.title, "gggg-[W]ww") %>)
	and end < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>) + dur(1 day)
	or file.mtime > date(<% tp.date.now("YYYY-MM-DD", "P-1W", tp.file.title, "gggg-[W]ww") %>)
	and file.mtime < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>) + dur(1 day)
SORT file.mtime desc
```

### Tasks
##### Filter None
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description does not include #note/project
hide edit button
```

##### Filter Priority
###### p11
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #p11
description does not include #note/project
hide edit button
```
###### p10
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #p10
description does not include #note/project
hide edit button
```
###### p01
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #p01
description does not include #note/project 
hide edit button
```
###### p00
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #p00
description does not include #note/project 
hide edit button
```

##### Filter Duration
###### 02h
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #02h 
description does not include #note/project 
hide edit button
```
###### 01h
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #01h 
description does not include #note/project 
hide edit button
```
###### 30m
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #30m 
description does not include #note/project 
hide edit button
```
###### 15m
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1W-1D", tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
description includes #15m 
description does not include #note/project 
hide edit button
```

### Analysis
**How much work in minutes did it did you complete last week? Does this amount seem realistic? If you worked every day for 8 hours for 7 days, you would have worked 56 hours, or 3,360 minutes.  If you had part-time for 4 days which cut working hours down to 4 hours, you would have worked 1,920 minute.**
[[Work-Minutes Last 7 Days]]
`Answer here.`

**How does this work compare to the previous week? Do you think the difference is significant?**
[[Work-Minutes Last 7-14 Days]]
`Answer here.`

### Reflection
**What do you think worked this week to get that much work done?**
`Answer here.`

**What do you think didn't work well this week to get that much work done?**
`Answer here.`

**How can you potentially increase Velocity (get more work done)?**
`Answer here.`

**What would stunt this increase, or even lower Velocity?**
`Answer here.`

**What's the likelihood of this concern occurring?**
`Answer here.`

**How much of an impact would this stunt or lowering Velocity?**
`Answer here.`

**What will you do to prevent or mitigate the stunting or lowering when it happens?**
`Answer here.`

## Alignment
```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, file.name)) as "Project",
	objective as "Objective",
	link(discipline, link(discipline).aliases) as "Discipline"
FROM #note/project and -"Templates"
WHERE file.mtime >= date(<% tp.date.now("YYYY-MM-DD", "P-1W", tp.file.title, "gggg-[W]ww") %>) and file.mtime < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>) + dur(1 day)
SORT due asc
```
```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, link(file.name).name)) as "Discipline",
	pillars as "Pillars",
	dynamic as "Dynamic"
FROM #note/discipline and -"Templates"
WHERE file.mtime >= date(<% tp.date.now("YYYY-MM-DD", "P-1W", tp.file.title, "gggg-[W]ww") %>) and file.mtime < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>) + dur(1 day)
SORT due asc
```
**For each [[Projects|Project]] that you touched last week, does its Objective still align with most of its [[Disciplines|Discipline]] [[Pillars]]? Does the Objective align with the Discipline Dynamic? How and why?**
[[Projects Touched Last Week]]
[[Project-Disciplines Touched Last Week]]
### `Project 1`
`Answer here.`

### `Project 2`
`Answer here.`

## Concerns
**What are at least two things to worry about next week?**
1. What's the likelihood of this concern occurring? 
2. How would this impact you? 
3. What will you do to prevent this from happening, or at least mitigate the damage when it occurs?

### Concern 1: `Title of Concern`
`Elaborate concern here`

### Concern 2: `Title of Concern`
`Elaborate concern here`

- [ ] #task #p01 #30m Complete [[<% tp.date.now("gggg-[W]ww", 0, tp.file.title, "gggg-[W]ww") %>]]

## Ramblings
`Other Ramblings go here.`

