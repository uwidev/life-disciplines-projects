```dataview
TABLE WITHOUT ID
	"Last 7-14 days" as "Timeframe",
	sum(default(rows.general.work_minutes_completed, 0)) as "Total Work Minutes"
FROM "300 Alignment/301 Daily"
WHERE date(file.name) >= date(today) - dur(14 days) and date(file.name) < date(today)  - dur(7 days)
GROUP BY file.folder as "logs"
```