---
tags: [ note/data ] 
---
[[<% tp.date.now("YYYY-MM", "P-1M", tp.file.title, "YYYY-MM") %>]] | [[<% tp.date.now("YYYY-MM", "P1M", tp.file.title, "YYYY-MM") %>]]
# <% tp.file.title %> Ramblings
## Fun
**Copy and paste the first quote from [/r/quotes: For your favorite quotes](https://www.reddit.com/r/quotes/top/?t=month)**

> Quote goes here
> — <cite>Author</cite>

`Your opnions on this quote here. Why do you think became the monthly top?`

## Review
![[<% tp.date.now("YYYY-MM", "P-1M", tp.file.title, "YYYY-MM") %>#Analysis]]
![[<% tp.date.now("YYYY-MM", "P-1M", tp.file.title, "YYYY-MM") %>#Reflection]]
![[<% tp.date.now("YYYY-MM", "P-1M", tp.file.title, "YYYY-MM") %>#Concerns]]
![[<% tp.date.now("YYYY-MM", "P-1M", tp.file.title, "YYYY-MM") %>#Ramblings]]

## Performance
### Projects
```dataview
TABLE WITHOUT ID
	file.link as "Project",
	status as "Status",
	objective as "Objective",
	start as "Start",
	end as "End"
FROM #note/project and -"999 Stale" and -"Templates"
WHERE end >= <% tp.date.now("YYYY-MM-DD", "P-1M", tp.file.title, "YYYY-MM") %> 
	or start >= <% tp.date.now("YYYY-MM-DD", "P-1M", tp.file.title, "YYYY-MM") %> 
	or end < <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
	or start < <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %>
	or file.mtime >= date(<% tp.date.now("YYYY-MM-DD", "P-1M", tp.file.title, "YYYY-MM") %>)
	or file.mtime < date(<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %>)
SORT end desc, start desc, status
```

### Tasks
##### Filter None
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description does not include #note/project
hide edit button
```

##### Filter Priority
###### p11
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #p11
description does not include #note/project
hide edit button
```
###### p10
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #p10
description does not include #note/project
hide edit button
```
###### p01
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #p01
description does not include #note/project 
hide edit button
```
###### p00
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #p00
description does not include #note/project 
hide edit button
```

##### Filter Duration
###### 02h
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #02h 
description does not include #note/project 
hide edit button
```
###### 01h
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #01h 
description does not include #note/project 
hide edit button
```
###### 30m
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #30m 
description does not include #note/project 
hide edit button
```
###### 15m
```tasks
done after <% tp.date.now("YYYY-MM-DD", "P-1M-1D", tp.file.title, "YYYY-MM") %>
done before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM") %> 
description includes #15m 
description does not include #note/project 
hide edit button
```

### Analysis
**How much work in minutes did it did you complete last month? Does this amount seem realistic?**
> If you worked every day for 8 hours in a 28 month-day, you would have worked 13,440 minutes. If you had part-time for 4 out of 7 days of the week in that 28 day month, and those part-time days only allowed for 4 hours of work, you would have worked 10,560 minutes.

[[Work-Minutes Last 1 Months]]
`Answer here.`

**How does this work compare to the previous months? Do you think this difference is significant?**
[[Work-Minutes Last 1-2 Months]]
`Answer here.`

### Reflection
**What do you think worked this month to get that much work done?**
`Answer here.`

**What do you think didn't work well this month to get that much work done?**
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
	link(file.name, default(link(file.name).aliases, link(file.name).name)) as "Discipline",
	pillars as "Pillars",
	dynamic as "Dynamic"
FROM #note/discipline and -"999 Stale" and -"Templates"
SORT due asc
```
**For each Discipline, how are you feeling about them at the moment? Do they still feel relevant and important through your Life Pillars?**
### `Discipline 1`
`Answer here.`

### `Discipline 2`
`Answer here.`

- [ ] #task #p01 #30m Complete [[<% tp.date.now("YYYY-MM", 0, tp.file.title, "YYYY-MM") %> Retrospection]]

## Concerns
**What are at least two things to worry about next month?**
1. What's the likelihood of this concern occurring? 
2. How would this impact you? 
3. What will you do to prevent this from happening, or at least mitigate the damage when it occurs?

### Concern 1: `Title of Concern`
`Elaborate concern here`

### Concern 2: `Title of Concern`
`Elaborate concern here`

## Ramblings
`Other Ramblings go here.`

- [ ] #task #p01 #30m Complete [[<% tp.date.now("YYYY-MM", 0, tp.file.title, "YYYY-MM") %>]]