# 📥 Quick Notes Inbox

A clean workspace to process your quick notes and convert them into tasks, concepts, projects, or research items.

---

## 🧠 Unprocessed Quick Notes
```dataview
TABLE file.link AS "Note", created AS "Created"
FROM #quick
WHERE processed = false
SORT created DESC
