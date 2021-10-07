```dataview
TABLE WITHOUT ID
	"Last 1 Months" as "Timeframe",
	sum(default(rows.work_minutes_completed, 0)) as "Work Minutes"
FROM "Journal/00 Daily/Ramblings"
WHERE date(file.name) >= date(today) - dur(1 month) and date(file.name) < date(today)
GROUP BY file.folder as "logs"
```
