---
type: Weekly Note
created: 2025-11-26
tags:
---

# 📆 Weekly Note — {{date:GGGG-[W]WW}}

---

## 🎯 1. Weekly Objectives  
Your 3–5 non‑negotiable outcomes for this week.

-  
-  
-  

---

## 📚 2. Research / Study Goals  
What topics, papers, or problems you want to understand or advance.

- [[ ]]  
- [[ ]]  

---

## 🧪 3. Ongoing Projects / Pipelines  
What you’ll push forward this week.

- [[Research Pipeline A]]  
- [[Project B]]  

---

## 📝 4. Key Tasks (High‑Impact Only)  
A short list of tasks that meaningfully move things forward.

- [ ]  
- [ ]  
- [ ]  

---

## 📈 5. Progress Summary (Auto‑Pulled Daily Notes)  
Shows your daily notes from this week for easy review.

```dataview
LIST
FROM #daily
WHERE date(file.day) >= date(this.start)
AND date(file.day) <= date(this.end)
SORT file.day ASC
````

---

## 🧠 6. Insights & Learnings

New ideas, techniques, or concepts learned this week.

---

## 🔗 7. New Notes Created This Week

Auto‑lists any new notes, regardless of type.

```dataview
LIST
WHERE file.cday >= date(this.start)
AND file.cday <= date(this.end)
SORT file.cday ASC
```

---

## 📉 8. Challenges

Where you got stuck or slowed down.

---

## 🎯 9. Goals for Next Week

Set yourself up with momentum.

```

---
```