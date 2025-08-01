---
tags: hub
cssclasses:
  - nav-hub
---

```dataview
TABLE WITHOUT ID
file.link
FROM "Content/School"
WHERE file.name = display(link(file.folder))
SORT file.name ASC
```