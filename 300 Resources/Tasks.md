---
aliases: [ Task, Task (Concept), Tasks (Concept) ]
tags: [ info, productivity ]
---
# Tasks
**Tasks** are Actionable items with a clearly defined completion. You should be able to read this Task and trivially answer `Yes` or `No` as to if this Task is complete. 

Tasks should work towards some Objective denoted in the corresponding [[Projects|Project]]; or uphold or works towards some [[Disciplines|Discipline]].

Tasks are Pull-based, meaning pull a task into your *Working On* list as you have more free hands, up to the [[#Ongoing]] limit. This concept of Pulling is similar to [[Kanban (Agile)|Kanban]]'s task management.

## Relation
Tasks are largely related to [[Projects]] as Tasks make lee-way towards its Objectives.

Tasks may also be a part of Disciplines and Life as needed.

## Alignment
It's highly suggested to routinely review all ongoing tasks to make sure they align with the corresponding Project. Do this on a daily basis. Backlogged tasks may not need to be reviewed, but should be groomed to prevent Feature Creep.

## Formatting
The format of tasks should follow the following format.

> - [ ] #task `<contents>` `[📅 YYYY-MM-DD]` `[#ongoing]`

`< >` - required
`[ ]` - optional

`#task` and the Due Date `[📅 YYYY-MM-DD]` can be automatically handled by the [Obsdian Tasks](https://github.com/schemar/obsidian-tasks) or with the [[Due]] template and [Natural Language Dates in Obsidian](https://github.com/argenos/nldates-obsidian)

### Due Date
Similar to [[Projects#YAML#due]], this should only be set for [[True Deadlines]].

### Ongoing
The Task is currently being worked on should have the `#ongoing` Tag on it.

All `#ongoing` Tasks will be aggregated by Tasks query.

There should be no more than 4 `#ongoing` tasks at any time. This is to reduce friction.

See [[Ongoing Tasks]] on what constitutes as an `#ongoing` task.

## Size
Tasks themselves should be broken down such that they take no longer than 2 hours to complete. This 2 hour duration is an arbitrary cutoff, and is based on the idea that if a task is expected to take longer than that, there will be some [[Friction]] and reluctance to its undertaking.