---
type: Literature Hub
created: 2025-11-26
tags:
  - todo
---

# 📚 Literature Hub : Heston Stochastic Volatility Model Calibration


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
FROM #Heston
WHERE status = "queued"
SORT year ASC
```

---

## 📖 In Progress

```dataview
TABLE author AS Author, year AS Year
FROM #Heston 
WHERE status = "reading"
SORT file.mtime DESC
```

---

## ✅ Completed

```dataview
TABLE author AS Author, year AS Year
FROM #Heston 
WHERE status = "done"
SORT file.mtime DESC
```

---

## 🧠 Most Recent Notes

```dataview
LIST
FROM #Heston 
SORT file.mtime DESC
LIMIT 10
```

---

## 🗂️ By Type

```dataview
TABLE author AS Author, year AS Year
FROM #Heston 
GROUP BY source-type
```

---

## 🏷️ By Tag / Topic

```dataview
TABLE file.link AS Note
FROM #Heston 
FLATTEN file.tags AS tag
GROUP BY tag
```

---

## 🔗 Related Hubs

- [[Research Hub]]
- [[Project Hub]]
- [[People Hub]]