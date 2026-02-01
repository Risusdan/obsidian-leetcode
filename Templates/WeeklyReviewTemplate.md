---
week: ""
start_date: "{{date:YYYY-MM-DD}}"
end_date: ""
type: weekly-review
total_problems_solved: 0
overall_mood: ""
---

# Weekly Review — {{date:YYYY-[W]ww}}

## 本週總結

```dataview
TABLE mood, energy, focus_rating
FROM "Journal/Daily"
WHERE type = "daily-journal" AND date >= this.start_date AND date <= this.end_date
SORT date ASC
```

## 刷題統計

- **本週解題數**：
- **狀態分布**：🔴  / 🟡  / 🟢
- **最有收穫的題目**：

## 技術學習回顧

> 本週學到的重點



## 面試準備進度

- **STAR 故事數量**：
- **英文練習頻率**：

## 情緒回顧

> 本週 mood / energy 趨勢



## 下週目標

- [ ]
- [ ]
- [ ]

## 給 AI 的備註

> 希望 AI 下次給什麼建議（可選）

