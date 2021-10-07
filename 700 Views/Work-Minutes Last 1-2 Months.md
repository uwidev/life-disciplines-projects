```dataview
TABLE WITHOUT ID
	"Previous 1 Months" as "Timeframe",
	sum(default(rows.work_minutes_completed, 0)) as "Work Minutes"
FROM "Journal/00 Daily/Ramblings"
WHERE date(file.name) >= date(today) - dur(2 months) and date(file.name) < date(today) - dur(1 months)
GROUP BY file.folder as "logs"
```