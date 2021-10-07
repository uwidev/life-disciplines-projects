---
aliases: ✨ Example Habit
tags: [ note/dashboard, note/project, note/habit, example_discipline ]
discipline: [[110 🎀 Example Discipline]]
status: [ 02 Planned ]
start: 
due: .inf
end: 
objective: blah blah blah 
when: 
---
> On the frontmatter above, turn the value under Discipline into a regular string. Then delete this.

[[110 🎀 Example Discipline]] | [[01 🌊 Tasks Example Habit]] | [[02 💡 Ramblings Example Habit]]
# ✨ Example Habit
```dataview
TABLE WITHOUT ID objective as "Objective", default(date(end), date(today)) - date(start) as "Ongoing"
WHERE file.name = this.file.name
```

## Abstract
Brief description of what is this habit, why it's important and came to be, and what will happen.

## Habit
Quick and concrete explanation of what will be done for this Habit.

## Frequency
How often this Habit is to occur and why.

## Formation
### Cue
**Where will this Habit take place?**


**What time will this Habit be enacted?**


**How does this Habit stack with other Habits?**


**What will be in place to remind you to do this? Are they passive or active reminders?**


### Craving
**How will you increase temptation and reduce friction? Is there a habit you like doing that you can do during or immediately after this?**


**What social communities will you join to push further commitment?**


### Response
**When the time comes, will there be any additional setup? What will you do to stop lower this friction?**


**When you do this habit, how long engage in it? How long now, a week from now, a month, etc.**


### Reward
**Will this be tracked some other way besides within Obsidian?**


**What are the results of this Habit? How long do you think until these results become rewarding?**


## YAML Field
How the data will be tracked within Obsidian. Defined as its own dictionary below, it should be added to [[Journal 00 Daily]]'s YAML.
```YAML
NAME_OF_HABIT:
  done: false
  stacked: false
  bundled: false
  duration: 
```

`done` (bool): Did you do it today?
`stacked` (bool): Did this habit proceed the intended stacking habit?
`bundled` (bool): Did you do a *want* habit after or during this habit?
`duration` (int): How long did you engage in it (in minutes)?

## [[01 🌊 Tasks Example Habit|Tasks]]
### Ongoing (3)
#### Filter Priority
```tasks
not done
path includes 00 Habit - Example Habit
description includes #ongoing
description includes #p11
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #ongoing
description includes #p10
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #ongoing
description includes #p01
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #ongoing
description includes #p00
description does not include #exclude 
```

#### Filter Due
```tasks
not done
path includes 00 Habit - Example Habit
description includes #ongoing
description does not include #exclude 
```

### Backlog
#### Filter Priority
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p11
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p10 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p01 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p00
description does not include #ongoing
description does not include #exclude 
```

#### Filter Duration
```tasks
not done
path includes 00 Habit - Example Habit
description includes #15m
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #30m 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #01h 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #02h 
description does not include #ongoing
description does not include #exclude 
```

### Blocked
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p11
description includes #block
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p10 
description includes #block
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p01 
description includes #block
description does not include #exclude 
```
```tasks
not done
path includes 00 Habit - Example Habit
description includes #p00
description includes #block
description does not include #exclude 
```

### Completed
#### Filter Today
```tasks
done today
path includes 00 Habit - Example Habit
```