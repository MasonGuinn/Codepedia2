---
order: 1
cssclasses:
  - nav-hub
tags:
  - hub
---


```dataview
TABLE WITHOUT ID
file.link
FROM "Technology"
WHERE length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name = display(link(file.folder))
SORT order ASC
```


