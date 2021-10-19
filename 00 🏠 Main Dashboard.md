---
aliases: 🏠 Main Dashboard
tags: [ dashboard ]
---
# 🏠 Main Dashboard
## Disciplines
```dataview
LIST
FROM #discipline 
```

## Projects
```dataview
TABLE WITHOUT ID
	file.link as "Discipline",
	status as "Status"
FROM #project 
```

## Ongoing Tasks
```tasks
not done 
description includes #ongoing
path does not include 800 Templates
```

## To-do
```tasks
not done
description does not include EXAMPLE
path does not include 800 Templates
```
```tasks
not done 
description includes EXAMPLE
path does not include 800 Templates
```

## Completed
```tasks
done
```