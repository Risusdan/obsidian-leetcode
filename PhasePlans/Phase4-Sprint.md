# Phase 4 — Sprint

## Goals

- Complete all 150 NeetCode problems
- Daily timed practice under interview conditions
- Polish behavioral stories
- Full mock interview cycles
- Final review of all 🔴/🟡 problems

## Monthly Breakdown

### Final Month
- [ ] Complete remaining problems to reach 150
- [ ] Hard problems focus
- [ ] Daily spaced repetition reviews
- [ ] 2 full mock interviews per week
- [ ] Finalize all STAR stories
- [ ] System design basics (if applicable)

## Milestones

- [ ] 150/150 NeetCode problems completed
- [ ] All problems at 🟢 status
- [ ] Confident in top 3 behavioral stories
- [ ] Ready for interview

## Progress — All Problems

```dataview
TABLE
  length(filter(rows, (r) => r.status = "🟢")) AS "🟢",
  length(filter(rows, (r) => r.status = "🟡")) AS "🟡",
  length(filter(rows, (r) => r.status = "🔴")) AS "🔴",
  length(rows) AS "Total"
FROM "LeetCode"
WHERE leetcode_number != null
GROUP BY topic
SORT topic ASC
```
