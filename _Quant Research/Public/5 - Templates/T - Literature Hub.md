---
type: Literature Hub
created: 2025-11-26
tags:
  - todo
---

# 📚 Literature Hub

A central place to manage **everything you read** — books, papers, articles, notes, and summaries.

---

## 🔍 Quick Stats
```dataview
TABLE status AS Status, length(rows) AS Count
FROM #literature
GROUP BY status
````

---

## 📚 Reading Queue

```dataview
TABLE author AS Author, year AS Year, status AS Status
FROM #literature
WHERE status = "queued"
SORT year ASC
```

---

## 📖 In Progress

```dataview
TABLE author AS Author, year AS Year
FROM #literature
WHERE status = "reading"
SORT file.mtime DESC
```

---

## ✅ Completed

```dataview
TABLE author AS Author, year AS Year
FROM #literature
WHERE status = "done"
SORT file.mtime DESC
```

---

## 🧠 Most Recent Notes

```dataview
LIST
FROM #literature
SORT file.mtime DESC
LIMIT 10
```

---

## 🗂️ By Type

```dataview
TABLE author AS Author, year AS Year
FROM #literature
GROUP BY source-type
```

---

## 🏷️ By Tag / Topic

```dataview
TABLE file.link AS Note
FROM #literature
FLATTEN file.tags AS tag
GROUP BY tag
```

---

## 🔗 Related Hubs

- [[Research Hub]]
- [[Project Hub]]
- [[People Hub]]