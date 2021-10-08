---
aliases: [ Task, Task (Concept), Tasks (Concept) ]
tags: [note/info, original, productivity]
---
# Tasks
**Tasks** are Actionable items with a clearly defined completion. You should be able to read this Task and trivially answer `Yes` or `No` as to if this Task is complete. 

Tasks should work towards some Objective denoted in the corresponding [[Projects|Project]]; or uphold or works towards some [[Disciplines|Discipline]]. Tasks that do not to this are considered [[#Casual Tasks|Casual Tasks]].

Tasks are Pull-based, meaning pull a task into your *Working On* list as you have more free hands, up to the [[#Ongoing]] limit. This concept of Pulling is similar to [[Kanban (Agile)|Kanban]]'s task management.

## Relation
Tasks are largely related to [[Projects]] as Tasks make lee-way towards its Objectives.

Tasks may also be a part of Disciplines and Life as needed.

## Alignment
It's highly suggested to routinely review all ongoing tasks to make sure they align with the corresponding Project. Do this on a daily basis. Backlogged tasks may not need to be reviewed, but should be groomed to prevent [[Feature Creep]].

## Aggregation
Task queries aggregate all tasks within its own folder and sub folders.

## Formatting
The format of tasks should follow the following format.

> - [ ] #task `<#priority_tag>` `<#est_duration>` `[#hb]` task description with clear language of doneness `[#cc/group` `[#ongoing]` `[#exclude[/tag][reason]]` `[📅 YYYY-MM-DD]`

`< >` - required
`[ ]` - optional

`#task` and the Due Date `[📅 YYYY-MM-DD]` can be automatically handled by the Task Plugin.

Ongoing and exclude can go in any order.

`#hb` tags this Task as a Habit.

A tempate [[task]] is included that quickly sets up a template.

## Completion Criteria Tag
All tasks under a Project should be tagged with one or more `#cc/group`, where `group` defines the Completion Criteria Group.

Tasks tagged with this Completion Criteria Group are related to these groups. See [[Projects#Completion Criteria]] for more details on the Groups.

## Dealing with Blocked Tasks
Both a [[Tasks#blocking|Blocking]] Task and its corresponding [[Tasks#blocked|Blocked]] should be given a `/key` on it's `#blocking`/`#blocked` to link them together. This is to easily relate the two by query or visual confirmation.

Ideally Blocked and Blocking Tasks should already be close together, but sometimes that's just not the case.

> We can't nest Tasks because it breaks workflow support from plugins, so since all Tasks are on the same level it may be difficult to discern related Blocked/Blocking Tasks, hence the Tagging.

**Once Blocked/Blocking items are complete, you must remove the `/key` (or just remove the entire block tag).** This is to ensure these keys can be reused.

## Due Date
Similar to [[Projects#YAML#due]], this should only be set for [[True Deadlines]].

## Location
In order for proper aggregation, Tasks should be created in locations as follows.
- Tasks relating to a Project should be placed somewhere in its Project folder. Preferably it goes into it's `[[Tasks Project#Raw]]` Note.
- Tasks related to a Discipline and not ongoing Project should be placed within the `[[Tasks Discipline#Raw]]` Note.
- Casual Tasks, ones that don't relate to a Discipline or Project, should be placed in the generic Tasks Casual Note on root.

All tasks, when complete and *need to be out of the way*, should be moved to it's respective `Archived` section, usually located in the `[[Tasks <Whatever>]]` Note.

## Priority
Tasks will always have a Priority Tag. Priority follows the [[Eisenhower Matrix]].

To reduce overhead, Priority will be represented with bits.

| Urgent | Important | Result |
| ------:|:--------- | ------ |
|      1 | 1         | 11     |
|      1 | 0         | 10     |
|      0 | 1         | 01     |
|      0 | 0         | 00     |

This also sorts well descending.
11 > 10 > 01 > 00

Since tags cannot only be numbers, a `p` will be prepended to the bits.

With this, allowed Priority Tags are as follows.
- `#p11`
- `#p10`
- `#p01`
- `#p00`

## Estimated Duration
Tasks will always have an Estimated Duration tag. This is NOT a due date. Allowed duration tags are as follows.
- `#15m`
- `#30m`
- `#01h`
- `#02h`

Estimated should round up. Tasks should never be longer than 2 hours.

## Ongoing
The Task is currently being worked on should have the `#ongoing` Tag on it.

All `#ongoing` Tasks will be aggregated onto a [[Pillars, Pipelines, Vaults (PPV)#Dashboards|Dashboard]]. 

There should be no more than 3 `#ongoing` tasks per Project, with a **global limit** of 4. That is, there should never be 4 tasks you queue to wok for at once.

See [[Ongoing Tasks]] on what constitutes as an `#ongoing` task.

## Status
Status indicate the current status of a note.

### (no status)
The task is normal. Handle this task based on its priority and whenever your hands are free.

### blocked
This Task is unwillingly stalled because of something. It should have nested tasks below it with  at least an Urgent priority. This Task Blocked Task should also be tagged with `#blocked`.

### blocking
This Task is Blocking some Task. It usually should be nested above some other Task, which means it is Blocking that Blocked task, which should have the `#blocked` tag. 

These Blocking tasks should have the `#blocking` task, and their priority should be at least Urgent `#p10`, if not Urgent and Important `#p11`.

### exclude/on-hold
These Tasks share similarities with the `03 On-Hold` status under [[Projects#status|Projects]]. For Tasks, it means that it was willingly put stalled and may or may not be resumed. If not, it will become Stale. These Tasks should be marked as `#exclude/on-hold`.

### exclude/stale
Tasks may be come irrelevant due to the passage of time and or a change in interest. A Task that has become irrelevant should be marked as `#exclude/stale` AND checked off as "Done". This will append a Completion Date and will be used for aggregation and analysis.

There is something wrong if you find that during a Alignment, you find that you have a lot of Stale Tasks. Projects will shift direction from time to time and many Tasks going stale may be expected, but if you find yourself consistently Stale'ing Tasks, it's possible you are not thinking before putting down a Task or you can't stabilize a Project's Objective.

> Grouped under exclude to reduce overhead queries.

## Size
Tasks themselves should be broken down such that they take no longer than 2 hours to complete. This 2 hour duration is an arbitrary cutoff, and is based on the idea that if a task is expected to take longer than that, there will be some [[Friction]] and reluctance to its undertaking.