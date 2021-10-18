---
aliases: [▶ Convergence to Ikigai,98 ▶ Convergence to Ikigai,Convergence to Ikigai]
tags: [ data ]
---
# 🔂 Convergence to Ikigai
This document serves to condense your Disciplines and define your single (or very small set) of [[Ikigai]]. 

> Make sure you view this in preview mode so the dataview codeblocks render properly.

To start with, for each Discipline, please make sure you answer the section **`Importance and Relevance.`**

## Required Setup
From the previous step [[11 🔀 Divergence to Disciplines#Finalizing]], for each Discipline you should have defined their ikigai characteristics.

In the top of the Discipline Dashboards, add the following to the YAML frontmatter.
```
ikigai:
  - 
```

> Note that the indent is two spaces, not tab.

Now start to list values to mirror what you its ikigai characteristics. For example, if you have a discipline you `love` and can be paid in `money`, it should look like the following on the to top of the note

```YAML
---
ikigai:
  - love
  - money
---
```

Other valid values you can list are `world` and `skill`.

Once you've done this for all disciplines, you are now ready to gain insight on your Disciplines towards your Ikigai.

## Your Life Through Disciplines
### Fundamental
This is the basis of what gives meaning to you. Everything else will build off of these fundamentals.

#### Love
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love")
```
#### World
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "world")
```
#### Money
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "money")
```
#### Skill
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "skill")
```

### Dynamic 1
This is the first layer of the emerging effect of 2 fundamental characteristics.

#### Mission 
Defined as what you love and what the world needs.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love") and contains(ikigai, "world")
```
#### Vocation
Defined as what the world needs and what you can be paid for.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "money") and contains(ikigai, "world")
```
#### Profession
Defined as what you can be paid for and what you are skilled at.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love") and contains(ikigai, "money")
```
#### Passion
Defined as what you are skilled at and what you love.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love") and contains(ikigai, "skill")
```

### Dynamic 2
These are the second emerging layer of 3 fundamental characteristics. These are Disciplines that are almost there, but are missing something to feel complete.

#### Useless Satisfaction
These are the cool things in life that don't serve a higher purpose other than being cool. You love these things, they make you money, and you're skilled in it, but that's all to it.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "love") and contains(ikigai, "skill") and contains(ikigai, "money") and !contains(ikigai, "world")
```

#### Empty Comfort
You can think of these as things you need to do, but aren't particularly fond of. They get the bills paid, you're genuinely being useful to others, and you just happen to be good at it.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "world") and contains(ikigai, "skill") and contains(ikigai, "money") and !contains(ikigai, "love")
```

#### Uncertain Excitement
These are things that you know are genuinely useful, that you love, and that you know you can be compensated for. However, you have yet to acquire the skills required to do so. **This is something you can aim for with sufficient training.**
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "world") and contains(ikigai, "love") and contains(ikigai, "money") and !contains(ikigai, "money")
```

#### Valueless Delight
You love doing these things. People understand its significance and recognize that you're a pioneer at this. However, they this is something that isn't really sustainable financially.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and contains(ikigai, "skill") and contains(ikigai, "love") and contains(ikigai, "money") and contains(ikigai, "money") and !contains(ikigai, "world")
```

### Potential Ikigai
Below are your primary driving forces of life, your Ikigai. They are things you love, what the world needs, what you get money for, and what you are skilled at.
```dataview
TABLE WITHOUT ID link(file.name, file.aliases) as "Discipline"
FROM "100 Disciplines"
WHERE contains(tags, "discipline") and length(ikigai) = 4
```

## Selecting your Ikigai(s)
You may find that you have multiple Ikigai. However, it's important to direct your attention to one, if not a very sparse amount, at a time. Truly touching and exercising all fundamental characteristics of a Discipline to sustain Ikigai takes commitment, requiring your limited time and effort. If you find you have multiple, it's best they share at some common ground, whether it be context or skillset.

> While it's possible to choose Disciplines that are not Potential Ikigais, understand that it will require the initial investment of time and effort to fulfill the missing Ikigai characteristics.

Now's the time to also reflect on what you wrote down under the Discipline's **`Importance and Relevance`** section.

**So, what will be your Primary Ikigai(s)?**
`Answer`

> I suggest you add a note tag: `#ikigai` to that dashboard, or at least note it under [[99 💗 Life|700 Life]] what your Ikigai is.

## Next Steps
Your Ikigai is now set. This will be your focus moving forwards. Your Ikigai may change in the future, and if so you can always come back here. But we need to take action now. We need to further understand what makes this Ikigai Discipline resonate with us. See [[13 🎎 Ikigai Expansion|🎎 Ikigai Expansion]]