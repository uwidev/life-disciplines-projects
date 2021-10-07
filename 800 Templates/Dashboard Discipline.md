---
aliases: {{VALUE:Source Emoji}} {{VALUE:Source Base Name}}
tags: [ note/dashboard, note/discipline, {{VALUE:Source Tag (no hashtag)}} ]
ikigai: 
  - love
  - skill
  - money
  - world
pillars: List 3-8 key values that you want to uphold or eventually uphold to. They should be numbered to indicate priorities. This should also be in the YAML, but in the same order as an unordered list.
dynamic: This is the emerging result of the pillars when viewed together.
---
> Make sure you set the YAML pillars and disciplines once realized. Delete this when afterwards.

[[00 🏠 Main Dashboard]] | [[{{VALUE:Number Prefix}}1 🌊 Tasks {{VALUE:Source Base Name}}]] | [[{{VALUE:Number Prefix}}2 💡 Ramblings {{VALUE:Source Base Name}}]]
# {{VALUE:Source Emoji}} {{VALUE:Source Base Name}}
## Abstract
What is the definition of this Discipline?

Continue with a brief description of what this discipline entails.

## Importance and Relevance
How is this Discipline important and relevant to you? How and why did you choose the Ikigai characteristics above under the frontmatter YAML? What is your purpose of having this as a Discipline?

## Core
```dataview
TABLE WITHOUT ID pillars as "Pillars"
WHERE file.name = this.file.name
```
```dataview
TABLE WITHOUT ID dynamic as "Dynamic"
WHERE file.name = this.file.name
```

## Projects
### Active
```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, file.name)) as "Project",
	status as "Status",
	due as "Due",
	padleft(string(priority), 2, "0") as "Priority",
	default(date(end), date(today)) - date(start) as "Duration"
FROM #note/project and #{{VALUE:Source Tag (no hashtag)}}
WHERE contains(list("00 Ongoing", "01 Blocked", "02 Planned", "03 Blocked"), status)
SORT status, due asc, priority desc
```

### Inactive
```dataview
TABLE WITHOUT ID
	link(file.name, default(link(file.name).aliases, file.name)) as "Project",
	status as "Status",
	end as "End",
	padleft(string(priority), 2, "0") as "Priority",
	default(date(end), date(today)) - date(start) as "Duration"
FROM #note/project and #{{VALUE:Source Tag (no hashtag)}}
WHERE !contains(list("00 Ongoing", "01 Blocked", "02 Planned", "03 Blocked"), status)
SORT status, file.mtime desc
```

## [[01 🌊 Tasks {{VALUE:Source Base Name}}|Tasks]]
### Ongoing
#### Filter Priority
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing
description includes #p11
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing
description includes #p10 
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing
description includes #p01 
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing
description includes #p00
description does not include #exclude 
```

#### Filter Duration
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing 
description includes #15m
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing 
description includes #30m 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing 
description includes #01h 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #ongoing 
description includes #02h 
description does not include #ongoing
description does not include #exclude 
```

### Backlog
#### Filter Priority
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p11
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p10 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p01 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p00
description does not include #ongoing
description does not include #exclude 
```

#### Filter Duration
```tasks
not done
path includes <% tp.file.folder() %>
description includes #15m
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #30m 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #01h 
description does not include #ongoing
description does not include #exclude 
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #02h 
description does not include #ongoing
description does not include #exclude 
```

#### Filter Due
```tasks
not done
path includes <% tp.file.folder() %>
description does not include #ongoing
description does not include #exclude 
```

### Blocked
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p11
description includes #block
description does not include #exclude 
hide task count
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p10 
description includes #block
description does not include #exclude 
hide task count
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p01 
description includes #block
description does not include #exclude 
hide task count
```
```tasks
not done
path includes <% tp.file.folder() %>
description includes #p00
description includes #block
description does not include #exclude 
hide task count
```

## Resources
```dataview
LIST
FROM #{{VALUE:Source Tag (no hashtag)}}
	AND -"200 Alignment" 
	AND -"800 Templates" 
	AND -"999 Stale"
	AND -#note/project
```