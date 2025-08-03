---
backward: "[[Computer Science]]"
parent: "[[Technology]]"
forward: "[[Development]]"
cssclasses:
  - nav-hub
order: 2
---

```dataview
TABLE WITHOUT ID
file.link
FROM "Technology/Cybersecurity"
WHERE length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name = display(link(file.folder))
SORT order ASC
```


