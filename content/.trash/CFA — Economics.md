---
course: "[[CFA]]"
topic: "[[Economics]]"
Tags: CFA, ECO, Topic
Aliases: 
--- 

```dataview

TABLE WITHOUT ID 
	file.link as Reading,
	level as Level

WHERE topic = this.file.name
WHERE level = [[CFA Level 1]]
WHERE file.path != this.file.path

SORT file.name ASC

```

# CFA Level 2
```dataview

TABLE WITHOUT ID 
	file.link as Reading,
	level as Level

WHERE topic = this.file.name
WHERE level = [[CFA Level 2]]
WHERE file.path != this.file.path

SORT file.name ASC

```

# CFA Level 3
```dataview
TABLE Subject
FROM #CFA3 AND #ECO 
```