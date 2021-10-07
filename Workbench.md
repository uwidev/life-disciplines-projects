```dataview
TABLE WITHOUT ID "," + join(rows.file.name, ",") as "Ongoing Projects QuickAdd String"
FROM #note/project 
WHERE contains(list("00 Ongoing", "01 Blocked", "02 Planned"), status)
GROUP BY file.ext
```
[[112 💡 Ramblings 110 Game Dev]]