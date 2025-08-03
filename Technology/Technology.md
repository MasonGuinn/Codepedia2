---
order: 1
cssclasses:
  - nav-menu
tags:
  - section
---


```dataview
LIST WITHOUT ID
file.link
FROM "Technology"
WHERE length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name = display(link(file.folder))
SORT order ASC
```


