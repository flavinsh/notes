---
level:
  - "[[CFA Level 1]]"
  - "[[CFA Level 2]]"
  - "[[CFA Level 3]]"
topic:
  - "[[Fixed Income]]"
---
```dataview

TABLE WITHOUT ID 
	file.link as Reading,
	level as Level

WHERE topic = this.file.name
WHERE file.path != this.file.path

SORT file.name ASC

```