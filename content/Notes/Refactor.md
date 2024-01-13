---
tags:
  - Obsidian
aliases:
---
```dataview
LIST
FROM #Refactor 
WHERE file.name != this.file.name
SORT file.created DESC
```