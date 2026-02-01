# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

An Obsidian vault for tracking LeetCode (NeetCode 150) study progress, technical learning, and interview preparation. There is no build system, test suite, or application code — this is a collection of Markdown files rendered by Obsidian with plugins.

## Architecture

- **Dashboard/** — Dataview-powered dashboards. `MainPanel.md` is the central hub; `LeetCodeProgress.md` has spaced repetition review queues; `WeeklyKanban.md` is a Kanban plugin board.
- **LeetCode/{Topic}/** — 16 topic folders (Arrays, TwoPointers, SlidingWindow, Stack, BinarySearch, LinkedList, Trees, Tries, Backtracking, Graphs, DynamicProgramming, Heap, Intervals, Greedy, BitManipulation, Math). Each problem note lives here.
- **PhasePlans/** — Four phase markdown files (Foundation → Core → Practice → Sprint) with Dataview progress queries.
- **Templates/** — `LeetCodeTemplate.md` defines the frontmatter schema and note structure for problem notes. `WeeklyPlanTemplate.md` and `BehavioralTemplate.md` for other note types.
- **TechLearning/**, **TestEngineering/**, **EnglishAndInterview/** — Supplementary study areas.

## Key Conventions

**Problem note naming**: `LeetCode/{Topic}/LC{number}-{Title}.md` (e.g., `LeetCode/Arrays/LC1-TwoSum.md`)

**Frontmatter schema** (defined in `Templates/LeetCodeTemplate.md`):
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

**Status emoji meanings**: 🔴 = not solved (review after 1 day), 🟡 = solved with difficulty (review after 3 days), 🟢 = solved independently (review after 7 days). Dashboards query these values directly — use the exact emoji characters.

**Topic values must match folder names exactly** — Dataview queries in PhasePlans and Dashboard filter by `topic` field matching folder names like `"Arrays"`, `"TwoPointers"`, `"DynamicProgramming"`.

## Plugins in Use

Dataview, Kanban, Obsidian Git, Custom Attachment Location, Table Editor. Theme: Obsidian Nord. Plugin configs live in `.obsidian/plugins/`.

## When Creating New Problem Notes

1. Use `Templates/LeetCodeTemplate.md` as the base
2. Place in the correct `LeetCode/{Topic}/` folder
3. Fill all frontmatter fields — incomplete frontmatter breaks Dataview queries
4. The `topic` field value must exactly match the folder name
