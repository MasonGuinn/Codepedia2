---
tags:
  - area
cssclasses:
  - nav-menu
order: 1
backward:
parent:
forward:
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

```dataview
LIST WITHOUT ID
file.link
FROM "Technology/Development"
WHERE file.name != this.file.name
SORT order ASC
```


