# Obsidian LeetCode & Technical Interview Preparation Tracker

An Obsidian vault for tracking a one-year LeetCode study plan based on the NeetCode 150 list, along with technical learning and behavioral interview preparation.

## Vault Structure

```
obsidian-leetcode/
├── Dashboard/
│   ├── MainPanel.md            # Central hub — overall progress, stats by difficulty/topic
│   ├── LeetCodeProgress.md     # Full problem list + spaced repetition review queues
│   └── WeeklyKanban.md         # Kanban board for weekly task management
├── LeetCode/
│   ├── Arrays/
│   ├── TwoPointers/
│   ├── SlidingWindow/
│   ├── Stack/
│   ├── BinarySearch/
│   ├── LinkedList/
│   ├── Trees/
│   ├── Tries/
│   ├── Backtracking/
│   ├── Graphs/
│   ├── DynamicProgramming/
│   ├── Heap/
│   ├── Intervals/
│   ├── Greedy/
│   ├── BitManipulation/
│   └── Math/
├── PhasePlans/
│   ├── Phase1-Foundation.md    # Month 1 — easy problems, build habits
│   ├── Phase2-Core.md          # Month 2-3 — medium problems, all topics
│   ├── Phase3-Practice.md      # Month 4-5 — remaining problems, timed practice
│   └── Phase4-Sprint.md        # Final month — complete 150, mock interviews
├── Templates/
│   ├── LeetCodeTemplate.md     # Frontmatter + solution template for each problem
│   ├── WeeklyPlanTemplate.md   # Weekly planning template
│   └── BehavioralTemplate.md   # STAR story template
├── TechLearning/
│   ├── Python/
│   ├── Cpp/
│   ├── SQL/
│   ├── Pytest/
│   └── RobotFramework/
└── EnglishAndInterview/
    ├── BehavioralInterview/
    └── EnglishPractice/
```

## Preparation Plan Overview

| Phase | Timeframe | Focus | Milestone |
|-------|-----------|-------|-----------|
| **Phase 1 — Foundation** | Month 1 | Easy problems in Arrays, Two Pointers, Stack, Binary Search; Python setup; daily habit | 30 problems solved |
| **Phase 2 — Core** | Month 2-3 | Medium problems across all NeetCode topics; Trees, Graphs, DP deep dive; behavioral prep | 80 problems solved |
| **Phase 3 — Practice** | Month 4-5 | Remaining topics (Heap, Intervals, Greedy, Backtracking, Bit Manipulation, Math); timed sessions; mock interviews | 120 problems solved |
| **Phase 4 — Sprint** | Final month | Complete 150/150; hard problems; daily spaced repetition; full mock interviews | All problems at 🟢 |

## Daily Workflow

1. Open **MainPanel** — check overall progress and identify problems needing review
2. Check **WeeklyKanban** — pick today's task from the Todo column, move it to InProgress
3. Solve the LeetCode problem — write solution in the corresponding `LeetCode/{Topic}/` note using the template
4. Update frontmatter status (`🔴` → `🟡` → `🟢`) and fill in complexity analysis + key takeaways
5. Move the Kanban card to Done
6. **Weekend**: review the week in LeetCodeProgress, revisit 🔴/🟡 problems via spaced repetition queues

## Creating New Problem Notes

1. Use `Templates/LeetCodeTemplate.md` as the base
2. Place in the correct `LeetCode/{Topic}/` folder
3. Fill all frontmatter fields — incomplete frontmatter breaks Dataview queries
4. The `topic` field value must exactly match the folder name
5. Use `[[wiki-links]]` in the Related Problems section (e.g., `[[LC1-TwoSum]]`) — this powers graph view connections
6. Update the `## Phase` section to link to the correct phase (e.g., `[[Phase2-Core]]` for medium problems)

## Conventions

### Naming Convention

All LeetCode problem notes follow this pattern:

```
LeetCode/{Topic}/LC{number}-{Title}.md
```

Examples:
- `LeetCode/Arrays/LC1-TwoSum.md`
- `LeetCode/Trees/LC226-InvertBinaryTree.md`
- `LeetCode/DynamicProgramming/LC70-ClimbingStairs.md`

### Frontmatter Schema

Each problem note uses this frontmatter (defined in `Templates/LeetCodeTemplate.md`):

```yaml
leetcode_number:    # integer
title:              # string
difficulty:         # Easy | Medium | Hard
topic:              # must match folder name exactly (e.g., "Arrays", "DynamicProgramming")
status:             # 🔴 | 🟡 | 🟢
date_attempted:     # YYYY-MM-DD
date_solved:        # YYYY-MM-DD
time_complexity:    # e.g., O(n)
space_complexity:   # e.g., O(1)
```

**Topic values must match folder names exactly** — Dataview queries in PhasePlans and Dashboard filter by `topic` field matching folder names like `"Arrays"`, `"TwoPointers"`, `"DynamicProgramming"`.

### Status Legend

| Emoji | Meaning | Spaced Repetition |
|-------|---------|-------------------|
| 🔴 | Not solved / needs help | Review after 1 day |
| 🟡 | Solved with hints or difficulty | Review after 3 days |
| 🟢 | Solved independently | Review after 7 days |

## Bidirectional Links & Graph View

This vault uses `[[wiki-links]]` extensively for Obsidian's graph view:
- **Related Problems**: Use `[[LC1-TwoSum]]` style links in the Related Problems section of each problem note to create topic clusters
- **Phase links**: Each problem note links to its phase plan; phase plans link to adjacent phases
- **Navigation**: Dashboards and weekly plans link back to `[[MainPanel]]` and each other

Open Graph View (`Cmd+G`) to visualize connections between problems, phases, and dashboards.

## Plugins & Theme

| Plugin                         | Purpose                                          |
| ------------------------------ | ------------------------------------------------ |
| **Dataview**                   | Powers all dashboard queries and progress tables |
| **Kanban**                     | Weekly task board (WeeklyKanban.md)              |
| **Obsidian Git**               | Auto-commit and sync vault to GitHub             |
| **Custom Attachment Location** | Organize attachments per folder                  |
| **Table Editor**               | Easier markdown table editing                    |

See https://youtu.be/IlNOhNeWGgY?si=kCzXCEmpc_PAVIec for plugin setup instructions.

**Theme**: Obsidian Nord
