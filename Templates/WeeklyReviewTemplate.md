---
week: ""
start_date: "{{date:YYYY-MM-DD}}"
end_date: ""
type: weekly-review
total_problems_solved: 0
overall_mood: ""
---

# Weekly Review — {{date:YYYY-[W]ww}}

## Weekly Summary

```dataview
TABLE mood, energy, focus_rating
FROM "Journal/Daily"
WHERE type = "daily-journal" AND date >= this.start_date AND date <= this.end_date
SORT date ASC
```

## Problem Solving Stats

- **Problems solved this week**:
- **Status distribution**: 🔴  / 🟡  / 🟢
- **Most insightful problem**:

## Technical Learning Review

> Key learnings this week



## Interview Prep Progress

- **STAR stories count**:
- **English practice frequency**:

## Mood Review

> This week's mood / energy trends



## Next Week Goals

- [ ]
- [ ]
- [ ]

## Notes for AI

> What advice should AI give next time (optional)

