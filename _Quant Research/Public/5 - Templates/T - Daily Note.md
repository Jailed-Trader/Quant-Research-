---
type: Daily Note
created: 2025-11-26
tags:
  - todo
---

# 📅 {{date}} — Daily Note

---

## 🎯 1. Top 3 Priorities  
The only things that truly matter today.

1.  
2.  
3.  

---

## 📋 2. Tasks  
Quick list of everything else.

- [ ]  
- [ ]  
- [ ]  

---

## 📚 3. Research / Study Focus  
What concepts, papers, or problems you’re tackling today.

- [[ ]]  
- [[ ]]  

---

## 🧠 4. Notes / Ideas / Observations  
Freeform notes, thoughts, or insights from the day.

-  

---

## 📈 5. Progress Log  
Short updates on what you actually did (quant, reading, coding, etc.)

-  

---

## 💬 6. Journal (Optional)  
Brief reflections, frustrations, or wins.

-  

---

## 🔗 7. Links Created Today  
Auto‑generated: any notes created today.

```dataview
LIST FROM "" 
WHERE file.cday = date("{{date}}")
SORT file.name ASC
````
