---
aliases: 
tags: [info, alignment]
---
[[00 ❗ Readme]]
## Simple Integration Into Obsidian
### Why Obsidian?
Obsidian is an enhanced, bare-bones markdown text editor. What makes it optimal is that users can use community plugins to customize and personalize functionality far beyond what it initially intended for. You are building your own system after all.

There's the added plus that all documents are stored locally on your computer as plain text. There is no dependence on a cloud proprietary software, the only dependence is you (and your computer). The sense of ownership and historical documentation is also satisfying. Everything is yours; just yours.

And that just felt right.

### Some Assumptions
I will assume that you are familiar with the basics of Obsidian. If not, please press F1 and take a look at the manual. Also consider some Youtube videos. Moving on!

### Demo
A sparse example of LDP's organization is already set up. You should have noticed that the following organization.

> 📁`100 Disciplines` > 📁`100 🎀 Well-being (EXAMPLE)` = [[110 🎀 Well-being (EXAMPLE)]] > 📁`Setup` = [[00 🧰 Setup]]

In more general terms.

> 📁`Disciplines` > 📁`Discipline` = Discipline Dashboard > 📁`Project` = Project Dashboard

### Folder Naming
You've probably noticed by now, but the folders on the left have a numbered prefix. This is a concept borrowed from the Dewey-Decimal System, where libraries organize their books by numbers. In our case, it organizes our folders.

Notice how `Inbox` comes first, not `Archive` when sorted alphabetically. This can also be used to sticky notes to the top of a folder, like `🏠 Main Dashboard`.

Not all folders should follow this system. I recommend you do this for Disciplines so your most important one, your [[Ikigai]] Discipline, pushed to the top. I do not recommend this for Projects as they have little to no value in ordering. They also always get pushed to the top anyways.

> tl;dr - Dewey-Decimal System for when grouping and ordering matters.

### Folder Hierarchy
Projects are placed within Disciplines, and Disciplines are placed within Life, which is the root of the vault.

> Life > Disciplines > Projects

### Dashboards
See [[Dashboards]].

### Obsidian Plugins
If there's some extra functionality you want, it probably exists. Here are some important plugins I consider core. These plugins have been included for this demo.
- [Obsidian Tasks](https://github.com/schemar/obsidian-tasks) for managing all your tasks
- [Obsidian Dataview](https://github.com/blacksmithgu/obsidian-dataview) for aggregating information for dashboards
- [obsidian-calendar-plugin](https://github.com/liamcain/obsidian-calendar-plugin) for visual routine alignment
- [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes) for routine alignment
- [Templater](https://github.com/SilentVoid13/Templater) to reduce friction and quickly set up new disciplines, projects, tasks, etc (which reduces friction)
- [Natural Language Dates in Obsidian](https://github.com/argenos/nldates-obsidian) for inserting dates in natural English

There are many, many other plugins that you might find useful. Do your own research.

> Obsidian Tasks has been extended to support [[300 Resources/Ongoing Tasks]]. Tasks can be tagged with `#ongoing` to mark them as an ongoing. Queries will look for that tag. See [[00 🏠 Main Dashboard|🏠 Main Dashboard]] for demo.

### Alignment
Routine alignment is done through [obsidian-calendar-plugin](https://github.com/liamcain/obsidian-calendar-plugin) and [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes). They are placed under `200 Alignment`. Check out the calendar on the right panels.

### Personal Knowledge Base (PKM)
Obsidian is known to be a link-based note-taking platform. Most follow some form of Zettelkasten or other graph-based organization. Your PKM should stand next to LDP, not tightly integrated.

I recommend you create a folder at the root of your vault, completely dedicated to your PKM. You can then *pull* these notes into a project, create further notes, and then push them back into your PKM. How you *pull* them is up to you.

Your PKM will maintain whatever structure it currently is.

For this demo, they are placed under `300 Resources`.

### Organizing Tasks
There's a command to swap a line of text up or down. I bound it to `alt+w` and `alt+s`. Use this to quickly move a task up and down the To-do list. You can also just highlight a line and click and drag it to where you want it to go. 

Friction is lowered. You can now keep your To-Do list clean. 

Optionally, there's a [plugin](https://github.com/ivan-lednev/obsidian-task-archiver) to automatically move all completed tasks to some archived header. Even less friction!