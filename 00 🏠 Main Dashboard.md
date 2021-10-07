---
aliases: 🏠 Main Dashboard
tags: [ note/dashboard ]
---
# 🏠 Main Dashboard
## Ikigai
```dataview
TABLE WITHOUT ID
	link(file.name, default(aliases, file.name)) as "Discipline",
	dynamic as "Dynamic"
FROM #note/ikigai
```

## Projects
```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, file.name)) as "Project",
	status as "Status",
	default(due, "Not Set") as "Due",
	padleft(string(priority), 2, "0") as "Priority",
	date(today) - date(start) as "Duration"
FROM #note/project and !#note/ikigai WHERE status = "00 Ongoing" or status = "01 Blocked" or status = "02 Planned" or status = "03 On-Hold" and file.name != "Dashboard Project" and !contains(tags, "note/habit") 
SORT status, "Due" asc, priority desc
```

## Resume Work
```query
tag:resume
```

## Habits
```tasks
not done
due today
description includes #hb
```

## Ongoing Tasks (4)
### Filter Priority
```tasks
not done 
description includes #ongoing
description includes #p11
description does not include #exclude 
description does not include #hb
hide task count
```
```tasks
not done
description includes #ongoing 
description includes #p10 
description does not include #exclude 
description does not include #hb
hide task count
```
```tasks
not done
description includes #ongoing 
description includes #p01 
description does not include #exclude 
description does not include #hb
hide task count
```
```tasks
not done
description includes #ongoing 
description includes #p00
description does not include #exclude 
description does not include #hb
hide task count
```

### Filter Due
```tasks
not done
description includes #ongoing 
description does not include #exclude 
description does not include #hb 
hide task count
```

## Blocked
```tasks
not done
description includes #p11
description includes #block
description does not include #exclude 
description does not include #hb
hide task count
```
```tasks
not done
description includes #p10 
description includes #block
description does not include #exclude 
description does not include #hb
hide task count
```
```tasks
not done
description includes #p01 
description includes #block
description does not include #exclude 
description does not include #hb
hide task count
```
```tasks
not done
description includes #p00
description includes #block
description does not include #exclude 
description does not include #hb
hide task count
```