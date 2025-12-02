---
type: Literature Hub
created: 2025-11-26
tags:
  - todo
---

# 📚 Literature Hub : Kalman Filter for Pairs Trading


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
FROM #Kalman_Filter
WHERE status = "queued"
SORT year ASC
```

---

## 📖 In Progress

```dataview
TABLE author AS Author, year AS Year
FROM #Kalman_Filter
WHERE status = "reading"
SORT file.mtime DESC
```

---

## ✅ Completed

```dataview
TABLE author AS Author, year AS Year
FROM #Kalman_Filter
WHERE status = "done"
SORT file.mtime DESC
```

---

## 🧠 Most Recent Notes

```dataview
LIST
FROM #Kalman_Filter
SORT file.mtime DESC
LIMIT 10
```

---

## 🗂️ By Type

```dataview
TABLE author AS Author, year AS Year
FROM #Kalman_Filter
GROUP BY source-type
```

---

## 🏷️ By Tag / Topic

```dataview
TABLE file.link AS Note
FROM #Kalman_Filter
FLATTEN file.tags AS tag
GROUP BY tag
```

---

## 🔗 Related Hubs

- [[Research Hub]]
- [[Project Hub]]
- [[People Hub]]