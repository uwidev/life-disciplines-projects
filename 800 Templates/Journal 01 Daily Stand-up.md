---
tags: [ note/data ]
---
[[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %>> Stand-up]] | [[<% tp.file.title.split(" ")[0] %>|Ramblings]] | [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %> Stand-up]]
# <% tp.date.now("YYYY-MM-DD dddd", 0, tp.file.title, "YYYY-MM-DD") %> Stand-up
## Review
### Projects you touched yesterday
```dataview
TABLE status as "Status",
	due as "Due",
	priority as "Priority"
FROM #note/project
WHERE file.mtime >= date(<% tp.file.title.split(" ")[0] %>) - dur(1 days) and file.mtime < date(<% tp.file.title.split(" ")[0] %>) and due != null
SORT status, due asc, urgent asc, important asc
```

### Tasks you completed yesterday
```tasks
done <% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %> 
description includes #p11
description does not include #exclude 
```
```tasks
done <% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %> 
description includes #p10
description does not include #exclude 
```
```tasks
done <% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %> 
description includes #p01
description does not include #exclude 
```
```tasks
done <% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %> 
description includes #p00
description does not include #exclude 
```
![[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %> Stand-up#Alignment]]

### Notes you dealt with yesterday
#### Created
```dataview
LIST
FROM -"Journal"
WHERE file.ctime > date(<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %>) and file.ctime < date(<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %>) + dur(1 days)
```

#### Last Modified
```dataview
LIST
FROM -"Journal"
WHERE file.mtime > date(<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %>) and file.mtime < date(<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %>) + dur(1 days)
limit 20
```

### Review your blocked items
```tasks
not done
description includes #blocked
```
```tasks
not done
description includes #blocking
```
![[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %> Stand-up#Is anything blocking your work? If so, why?]]

### Ramblings you did yesterday
![[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title.split(" ")[0], "YYYY-MM-DD") %>#<% tp.date.now("YYYY-MM-DD dddd", -1, tp.file.title, "YYYY-MM-DD") %> Ramblings]]

## Stand-up
### What did you manage to get done yesterday?
[[Tasks Completed Yesterday]]

`Explicitly respond here.`

### What is your focus today?
[[Tasks Ongoing]] [[OLD Backlog]]

`Answere here. This should be a general focus, not specific tasks.`

#### Alignment
[[Ongoing Project Reference]]
**Does this focus still Align to its Project's Objective? How and why?**
`Answer here.`

**Does this Project's Completion Criteria still Align with its Objective?**
`Answer here.`

### Is anything blocking your work? If so, why?
[[00 🏠 Main Dashboard#Blocked]]



## Next Steps
- [ ] #task #p01 #15m Complete [[<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %> Stand-up]]

Mark as completed and adjust time to reflect how long this took you. Then proceed to [[<% tp.file.title.split(" ")[0] %>|Today's Ramblings]].