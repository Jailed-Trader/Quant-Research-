````markdown
# 🛰 Mission Control Dashboard

---

## 📌 Recently Added Topics
```dataview
TABLE file.cday AS "Created"
FROM #concept
SORT file.cday DESC
LIMIT 10
````

---

## ✅ Recently Completed

```dataview
TABLE file.mday AS "Completed"
FROM ""
WHERE status = "done"
SORT file.mday DESC
LIMIT 10
```

---

## 💡 Fleeting Ideas

```dataview
LIST
FROM "Inbox/Fleeting"
SORT file.cday DESC
```

---

## ❓ Questions to Research

```dataview
LIST
FROM ""
WHERE contains(tags, "#question")
SORT file.cday DESC
```

---

## 📚 Reading Queue

```dataview
TABLE author AS Author, year AS Year, status AS Status
FROM #literature
WHERE status = "queued"
SORT file.cday ASC
```

