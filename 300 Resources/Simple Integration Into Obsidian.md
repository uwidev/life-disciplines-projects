---
aliases: 
tags: [ info ]
---
## Simple Integration Into Obsidian
### Why Obsidian?
Obsidian is an enhanced, barebones markdown text editor. What makes it optimal is that users can use community plugins to customize and personalize functionality far beyond what it initially intended for. You are building your own system after all.

There's the added plus that all documents are locally stored on your computer as plain text. There is no dependence on a cloud or server, the only dependence is you (and your compluter). There's also the sense of ownership and historical documentation. Everything is yours; just yours.

And that just felt right.

### Some Assumptions
I assume that you are familar with the basics of Obsidian. If not, please press F1 and take a look at the manual. Also consider some Youtube videos. Moving on!

### Folder Naming
You've probably noticed by now but the folders on the left have a numbered prefix. This is a concept borrowed from the Dewey-Decimal System, where libraries organize their books by numbers. It's modified to do just that, within the digital world, it also organizes the notes. Notice how `Inbox` comes first, not `Archive`. This can also be used to sticky notes to the top of a folder, like `🏠 Main Dashboard`.

Not everything follows this system; it isn't consistent. I recommend you do this for Disciplines so your most important one, your [[Ikigai]], is the first thing you see. I do not recommend this for projects since order has little to no value.

> tl;dr - Dewey-Decimal System for when grouping and ordering matters.

### Folder Hierarchy
Projects are placed within Disciplines, and Disciplines are placed within Life, which is the root of the vault.

> Life > Disciplines > Projects

### Dashboards
Dashboards are as the master note for whatever it serves. A dashboard for Life [[99 💗 Life]] is where you would define everything related to your Life under the premise of LDP.

You want one for Life, all Disciplines, and all Projects. They can also be used in tandem with [[#Obsidian Plugins]].

They can also be used as a portal to see what you need to do right now. See [[00 🏠 Main Dashboard|🏠 Main Dashboard]] for an example.

### Obsidian Plugins
If there's some extra functionality you want that can make your personalized system easier, it probably exists.

Here are some important plugins I consider core. These plugins have been included for this demo.
- [Obsdian Tasks](https://github.com/schemar/obsidian-tasks) for managing all your tasks
- [obsidian-calendar-plugin](https://github.com/liamcain/obsidian-calendar-plugin) for visual routine alignment
- [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes) for routine alignment
- [Templater](https://github.com/SilentVoid13/Templater) to reduce friction and quickly set up new disciplines, projects, and tasks (which reduces friction)
- [Natural Language Dates in Obsidian](https://github.com/argenos/nldates-obsidian) for inserting dates in natural english

There are many, many other plugins that you might find useful. Do your own research.

> A simple implementation of Obsidian Tasks has already been implemented. Tasks can be tagged with `#ongoing` to mark them as an Ongoing task.

### Alignment
Routine alignment is done through [obsidian-calendar-plugin](https://github.com/liamcain/obsidian-calendar-plugin) and [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes). They are placed under `200 Alignment`.

### Personal Knowledge Base (PKM)
Obsidian is known to be a link-based note taking platform. Most follow some form of Zettelkasten or other graph-based organization of notes. Your PKM should stand next to LDP, but should not be tightly integreted. 

I recommend you create a folder the root of your vault, completely dedicated to your PKM. You can then pull these notes into Projects, create further notes, and then push them back into your PKM. Your PKM will maintain whatever structure it currently is.

For this demo, they are placed under `300 Resources`.