---
aliases: 🎁 Example Project
tags: [ note/dashboard, note/project, example_discipline ]
discipline: [[110 🎀 Example Discipline]]
status: 00 Ongoing
start: 2021-10-02
due: 
end: 
priority: 00
objective: one sentence explaining what this project is, why it is needed, and how it's to be done
---
[[110 🎀 Example Discipline]] | [[01 🌊 Tasks Example Project]] | [[02 💡 Ramblings Example Project]]
# 🎁 Example Project
```dataview
TABLE WITHOUT ID objective as "Objective", default(date(end), date(today)) - date(start) as "Ongoing"
WHERE file.name = this.file.name
```

## Abstract
Brief description of what is this project, why it came to be, and how it's going to be conducted.

## Completion Criteria
**This project is considered complete when the following Requirements are met.**
Create a general Completion Criteria checklist and then start grouping them under `#cc/` tags to later tag related Tasks.

## [[01 🌊 Tasks Example Project|Tasks]]
### Ongoing (3)
#### Filter Priority
```tasks
not done
path includes Example Project
description includes #ongoing
description includes #p11
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #ongoing
description includes #p10
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #ongoing
description includes #p01
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #ongoing
description includes #p00
description does not include #exclude 
```

#### Filter Due
```tasks
not done
path includes Example Project
description includes #ongoing
description does not include #exclude 
```

### Backlog
#### Filter Priority
```tasks
not done
path includes Example Project
description includes #p11
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #p10 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #p01 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #p00
description does not include #ongoing
description does not include #exclude 
```

#### Filter Duration
```tasks
not done
path includes Example Project
description includes #15m
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #30m 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #01h 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #02h 
description does not include #ongoing
description does not include #exclude 
```

#### Filter CC
##### #cc/
```tasks
not done
path includes Example Project
description includes #cc/
description does not include #exclude 
```
##### Untagged
```tasks
done
path includes Example Project
description does not include #cc/
```

### Blocked
```tasks
not done
path includes Example Project
description includes #p11
description includes #block
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #p10 
description includes #block
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #p01 
description includes #block
description does not include #exclude 
```
```tasks
not done
path includes Example Project
description includes #p00
description includes #block
description does not include #exclude 
```

### Completed
#### Filter Today
```tasks
done today
path includes Example Project
```

## Resources
This is where you can link all the notes and resources you may need to do this project.

## Retrospection
**What worked well with on this Project?**


**What didn't work well on this Project?**


**How can the next Project work better?**


**In the end, does this Project align well and make progress towards a Discipline?**
