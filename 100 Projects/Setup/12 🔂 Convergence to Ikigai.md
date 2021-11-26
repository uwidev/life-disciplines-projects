---
aliases: [▶ Convergence to Ikigai,98 ▶ Convergence to Ikigai,Convergence to Ikigai]
tags: [ data ]
---
# 🔂 Convergence to Ikigai
This document serves to condense your disciplines and define your single (or very small set) of [[Ikigai]]. 

> Make sure you view this in preview mode so the dataview plugin renders codeblocks properly.

To start, for each discipline, make sure you defined their relevance and importance.

## Setup
### Required
At the top of the discipline's dashboards, add the following to the YAML frontmatter.
```
ikigai:
  - 
```

> Note that the indent is two spaces, not a tab.
> 
> If you're unfamiliar with YAML, press F1 and check out the `[[YAML front matter]]` note.

Now start to list values to mirror its Ikigai characteristics as noted under [[11 🔀 Divergence to Disciplines#Finalizing]]. For example, if you have a discipline you `love` and can be compensated for in `money`, it should look like the following on the top of the note.

```YAML
---
ikigai:
  - love
  - money
---
```

Other valid values you can list are `world` and `skill`.

### Suggested
You should also add a field for your dynamic so they can be queried. This will give better context to how a discipline resonates with you.

```YAML
dynamic: "This is the discipline's dynamic that I defined earlier."
```

Your final YAML should look something like this.

```YAML
ikigai:
  - love
  - world
dynamic: "To explore, discover, and perfect pancakes."
```

## Your Life Through Disciplines
### Fundamental
This is the basis of what gives meaning. Everything else will build on these fundamentals.

#### Love
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love")
```
#### World
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "world")
```
#### Money
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "money")
```
#### Skill
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "skill")
```

### Dynamic 1
This is the first layer of the emerging effect of 2 fundamental characteristics. They will not filter out the extra characteristics on that Discipline.

This section is meant to give you an understanding of the Discipline in the context of the bigger picture.

#### Mission 
Defined as what you love and what the world needs.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love") and contains(ikigai, "world")
```
#### Vocation
Defined as what the world needs and what you can be paid for.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "money") and contains(ikigai, "world")
```
#### Profession
Defined as what you can be paid for and what you are skilled at.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "skill") and contains(ikigai, "money")
```
#### Passion
Defined as what you are skilled at and what you love.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love") and contains(ikigai, "skill")
```

### Dynamic 2
These are the second emerging layer of 3 fundamental characteristics. These are Disciplines that are almost there, but are missing something to feel complete. Nothing will appear if you're missing something to achieve that section. 

This is meant to get you to understand the potential for success if you discover that missing element.

#### Useless Satisfaction
These are the cool things in life that don't serve a higher purpose other than being cool. You love these things, they make you money, and you're skilled in it, but that's all to it.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love") and contains(ikigai, "skill") and contains(ikigai, "money") and !contains(ikigai, "world")
```

#### Empty Comfort
You can think of these as things you need to do, but aren't particularly fond of. They get the bills paid, you're genuinely being useful to others, and you just happen to be good at it.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "world") and contains(ikigai, "skill") and contains(ikigai, "money") and !contains(ikigai, "love")
```

#### Uncertain Excitement
These are things that you know are genuinely useful, that you love, and that you know you can be compensated for. However, you have yet to acquire the skills required to do so. **This is something you can aim for with sufficient training.**
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "world") and contains(ikigai, "love") and contains(ikigai, "money") and !contains(ikigai, "skill")
```

#### Valueless Delight
You love doing these things. People understand its significance and recognize that you're a pioneer at this. However, this is something that isn't really sustainable financially.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "skill") and contains(ikigai, "love") and contains(ikigai, "world") and !contains(ikigai, "money")
```

### Potential Ikigai
Below are your primary driving forces of life, your Ikigai(s). They are things you love, what the world needs, what you get money for, and what you are skilled at.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline", dynamic as "Dynamic"
FROM "200 Disciplines"
WHERE contains(tags, "discipline") and length(ikigai) = 4
```

## Selecting your Ikigai(s)
You may have multiple potential Ikigais. However, it's important to set focus to only one, if not a very sparse amount. 

Ikigai is your direction, and if the Ikigais point towards a similar direction, you may find yourself not reaching full potential. Lots of time and effort could be wasted.

> While it's possible to choose disciplines that are not potential Ikigais, understand that it will require the initial investment of time and effort to fulfill the missing Ikigai characteristics.

Now's the time to also reflect the potential Ikigais **`Importance and Relevance`** section.

**So, what will be your primary Ikigai(s)?**
`Answer`

> I suggest you add a note tag: `#ikigai` to that discipline's dashboard, or at least note it under [[400 💗 Life|💗 Life]] what your Ikigai is.

## Next Steps
Your Ikigai is now set. This will be your focus moving forwards.

Your Ikigai may change in the future, and if so you can always run through this or a similar process.

For now, we need to further understand what makes this Ikigai discipline resonate for you. See [[13 🎎 Ikigai Expansion|🎎 Ikigai Expansion]]