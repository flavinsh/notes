📝 [[Scratchpad]]
# Areas
1. 💰 [[Finance]]
2. 🌍 [[Geopolitics]]
3. 🤓 [[Maths]]
4. 🏛️ [[CFA]]
	- [[CFA Level 1]]
	- [[CFA Level 2]]
	- [[CFA Level 3]]
1. ℹ️ [[Documentation]]


# MOCs
```dataview
LIST
FROM #MOC 
SORT file.name ASC
```
# Daily Notes
```dataview
  LIST
  WHERE 
	  contains(file, "day")
  SORT 
	  file.mtime DESC
  LIMIT 5 
  ``` 

# Vault maintenance
- [[Broken links]]
- [[Empty files]]
- [[Files without tags]]
- [[Vault management/Orphaned files]]

> [!links]- Backlinks
> ```dataview
> LIST FROM [[#]] WHERE file != this.file
> SORT file.created ASC
> ```