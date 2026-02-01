# LeetCode Progress

## Full Problem List

```dataview
TABLE leetcode_number AS "#", difficulty, topic, status, date_attempted, date_solved
FROM "LeetCode"
WHERE leetcode_number != null
SORT leetcode_number ASC
```

## Spaced Repetition Review

### 🔴 Review Tomorrow (1-day interval)

```dataview
TABLE leetcode_number AS "#", title, topic
FROM "LeetCode"
WHERE status = "🔴" AND date_attempted != null AND date(today) - date(date_attempted) >= dur(1 day)
SORT date_attempted ASC
```

### 🟡 Review in 3 Days

```dataview
TABLE leetcode_number AS "#", title, topic
FROM "LeetCode"
WHERE status = "🟡" AND date_solved != null AND date(today) - date(date_solved) >= dur(3 days)
SORT date_solved ASC
```

### 🟢 Review in 7 Days

```dataview
TABLE leetcode_number AS "#", title, topic
FROM "LeetCode"
WHERE status = "🟢" AND date_solved != null AND date(today) - date(date_solved) >= dur(7 days)
SORT date_solved ASC
```

## Navigation

- [[MainPanel]]
- [[WeeklyKanban]]
