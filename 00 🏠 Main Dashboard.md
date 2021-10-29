---
aliases: 🏠 Main Dashboard
tags: [ dashboard ]
---
[[99 🗃️ Master Backlog|🗃️ Master Backlog]]
# 🏠 Main Dashboard
## Ongoing Tasks
```tasks
not done 
description includes #ongoing
path does not include 800 Templates
```

## Planned
```tasks
not done 
description includes #planned
description does not include #ongoing
description does not include #hb
path does not include 800 Templates
```
## Habits
```tasks
not done
description includes #hb
due today
```

## Projects
```dataview
TABLE WITHOUT ID
	file.link as "Discipline",
	status as "Status"
FROM #project 
```

## Disciplines
```dataview
LIST
FROM #discipline 
```

## Completed
```tasks
done
```