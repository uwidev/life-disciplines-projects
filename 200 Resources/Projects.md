---
aliases: Project
tags: [note/info, original, productivity]
---
# Projects
**Projects** are derived from [[Disciplines]] and has some Objective that requires some set of  [[Tasks]] complete. These Projects should make progress towards or uphold some [[Pillars|Pillar]] from the parent Discipline.

Projects should strongly fit into one Discipline, and if it seems a Project could fit in multiple, the Disciplines need to be reorganized to prevent overlapping dependency, where too many items from one Discipline belong in another Discipline. Just combine the two or figure out some other way to have them clearly different.

Projects may also have [[Ceremonies (Scrum)|Ceremonies]] and a method of tracking [[Habits]].

## Scoping
Projects will be of varying sizes and should be longer than 2 hours, as this is the arbitrary maximum length of [[Tasks]]. Since Tasks make up a Project, it's a given that Projects should be bigger than a Task.

While there isn't a real maximum on how big a Project is, it's suggested to be no longer than a month, averaging several weeks. This duration is based on the general duration of a [[Sprints (Scrum)|Sprint]]. **And this is under the assumption that this Project is the ONLY thing you're working on.** Plan your Projects and focus according to your available TIme.

## Relations
Projects are immediately derived from [[Disciplines]], as a Project's Objective should be related to said Discipline's Pillars and/or Dynamics.

Tasks are largely derived from Projects to make lee-way towards meeting the Objective, which in term, meets the Discipline's Pillars and/or Dynamics.

## Important Setup
Projects must be tagged under YAML with `#note/project` and its corresponding Discipline Tag in order to be properly queried by Dataview.

## Objective
An Objective comes in two parts: Core and Abstract. All Objectives should answer the following questions.
- What will come to fruition?
- Why does this need to happen? 
	- What happens when it comes into fruition? What does it effect or mitigate?
- How? What main methods or tools will be used to do this?

### Core
Should be concise enough to Display well on tables or lists during Alignment sessions. Optimally, you want to put it in a single sentence.

### Abstract
Expands on the Objective, generally discussing the following.
- Origins of what prompted this project
- Repeating why this needs to come into fruition, as well as chaining into why what follows is important, and why what follows that is also important... etc
- Other things that can result from this project

## Completion Criteria
Unlike [[Disciplines]], Projects should eventually come to an end and shouldn't run any longer than 1 month. Since there usually isn't a time-based ending point ([[True Deadlines|True Deadline]]), an end must be defined through some other means.

For Projects, Completion Criteria is as a Well-Defined checklist that cumulate to a shift in the environment or creation of an object. 

Well-Defined as in Requirements can be clearly answered `Yes` or `No` if they have been met. These Requirements should align with the Core.

While there is not hard limit of Completion Criteria count, it should be noted that these are essentially groupings for [[Tasks|Tasks]]. Having too much may hint at a Project that may take longer than 1 month, vice versa.

**All Projects should have Completion Criteria, but the Objective should come first.**

### Groups
Completion Criteria should also be categorized, or at least tagged under, some broad tagline under the Tag Group `#cc/`. How you group your Completion Criteria, or not at all, is up to you, but for a Project with many [[Tasks]], it's important to be able to Align tasks to at least one Completion Criteria or it's corresponding Group.

## Alignment
Projects should be routinely reviewed to ensure that they progress towards some [[Pillars|Pillar]] denoted under its corresponding [[Disciplines|Discipline]]. It's suggested to do this review weekly.

### Big Projects
There may be rare times in which a Project must take longer than a month. With a similar reasoning as to why Tasks are no longer than 2 hours, the size of these Projects may create friction and reluctance in their undertaking.

If a Project is believed to be longer than such, deconstruct it into clearly different Projects to make it more approachable. If it's sequential, set the later Projects On-Hold or as a Task under that Discipline.

If deconstructing it into clearly different Projects is not possible, **your last resort** would be to have a Big Project and Sub-Projects to denote phases and milestones. Project Folders should be nested accordingly.

## Folders and Organization
Projects should have their own dedicated folder. [[Projects#Big Projects|Big Projects]] also have their own dedicated folder.

## YAML
Projects will always have YAML on the top of them, denoting which Discipline they belong on, among other things. All of these values you must update manually.

### discipline
Denotes the Discipline that this Project belongs to. It should also be in its corresponding folder. Do not assign a link as a value.

### status (YAML)
Denotes the current Status of this Project. See [[Projects#Status]].

### start
Denotes when the Project is set to **00 Ongoing**, NOT when the Dashboard was created.

### due
When the deadline of a project is. 

Similar to [[Tasks#Creation#Due Date]], due dates should only be assigned for [[True Deadlines]].

This value should also NOT be infinite. Being infinite indicates that this Project is infinitely large, and should have been a [[Disciplines|Discipline]]. This also lowers drive, as the deadline is infinitely far.

It should also NOT be -infinite. Being -infinite logically means that this project is way infinitely over its deadline. Whether that brings dead or immense hustle, either is doomed to despair.

### end
Denotes when the Project is set to **Done** or **Stale**.

### objective (YAML)
This should be exactly the same as the Project Objective's one sentence summary.

### priority
This should follows the same methodology as [[Tasks#Priority]].

## Status
Projects will have the following Statuses as values in their Status YAML field. Ignore `inline` formatting and only use plain text.

### Active
#### 00 Ongoing
Defined as a Project that has been setup to do immediate work. If it's still in the setup phase, it should be `02 Planned`.

#### 01 Blocked
Defined as a Project that was *unwillingly* put stalled. Clearing this blockage takes urgency as resuming the project becomes top priority.

#### 02 Planned
Defined as a Project that is *Ongoing*, but real work has not started. We are still defining what this Project is, and maybe if we're actually going to execute it to begin with.

### Inactive
#### 03 On-Hold
Defined a Project that was *willingly* put stalled, which may or may not be resumed. Reviews and Alignments will judge whether the project stays alive. Reasons why vary on a Project may be put on Hold, with some reasons listed below.
	-  Lost relevancy towards a Discipline
	-  Lost Velocity or Motivation

#### 04 Done
Defined as a Project that has all of it's Completion Criteria. With regards to Polish tag `#cc/poi`, this Criteria does not have to be completed, as polishing a Project is subjective and can be infinitely demanding.

#### 99 Stale
Defined as a project that is no longer relevant.

## Ceremonies
Ceremonies might be used to prepare one's self for adversity that is this Project's work. 

A simple example of a Ceremony is a set of movements to warm up before a session on a new workout schedule.

See [[Ceremonies]] for full details on how they operate.