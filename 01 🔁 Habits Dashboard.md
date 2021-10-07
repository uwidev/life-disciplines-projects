---
aliases: 🔁 Habits Dashboard
tags: [ note/dashboard, habit ]
---
# 🔁 Habits Dashboard
```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, file.name)) as "Habit",
	status as "Status",
	when as "When"
FROM #note/habit
WHERE contains(list("00 Ongoing", "01 Blocked", "02 Planned"), status)
```

## Habits Today
```tasks
not done
due today
description includes #hb
```

## Habits in the next 3 days
Does not include repeated tasks
```tasks
not done
due after today
due before in 3 days
description includes #hb
```

## Backlog
```dataview
TASK
FROM #note/habit 
WHERE !contains(text, "#hb") and contains(text, "#task")
```