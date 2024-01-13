---
tags:
  - MOC
  - "#TODO"
cssclasses:
  - title-hide
---
# #TODO

## Tasks

- [ ] Clean tags
- [ ] Clean properties
- [ ] Refactor [[Documentation]]

## Create notes
```dataview
LIST
FROM #TODO  
WHERE file.name != this.file.name
SORT file.ctime DESC
```

## Continue notes 
```dataview
LIST
FROM #WIP  
WHERE file.name != this.file.name
SORT file.created DESC
```


## Refactor notes
```dataview
LIST
FROM #Refactor 
WHERE file.name != this.file.name
SORT file.created DESC
```





k