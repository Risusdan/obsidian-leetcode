# Main Dashboard

## Overall Progress

```dataview
TABLE
  length(rows) AS "Count",
  round(length(rows) / 150 * 100, 1) + "%" AS "of NeetCode 150"
FROM "LeetCode"
WHERE leetcode_number != null
GROUP BY status
SORT status ASC
```

## By Difficulty

```dataview
TABLE length(rows) AS "Count"
FROM "LeetCode"
WHERE leetcode_number != null
GROUP BY difficulty
SORT difficulty ASC
```

## By Topic

```dataview
TABLE length(rows) AS "Count"
FROM "LeetCode"
WHERE leetcode_number != null
GROUP BY topic
SORT topic ASC
```

## Recent Completions

```dataview
TABLE difficulty, topic, status, date_solved
FROM "LeetCode"
WHERE leetcode_number != null
SORT date_solved DESC
LIMIT 10
```

## Needs Review (🔴 or 🟡)

```dataview
TABLE difficulty, topic, date_attempted
FROM "LeetCode"
WHERE status = "🔴" OR status = "🟡"
SORT date_attempted ASC
```

## 最近日誌

```dataview
TABLE mood, energy, focus_rating
FROM "Journal/Daily"
WHERE type = "daily-journal"
SORT date DESC
LIMIT 5
```

## Quick Links

- [[WeeklyKanban]]
- [[LeetCodeProgress]]
- [[Phase1-Foundation]]
- [[Phase2-Core]]
- [[Phase3-Practice]]
- [[Phase4-Sprint]]
