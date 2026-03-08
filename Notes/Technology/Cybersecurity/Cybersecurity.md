---
tags:
  - type/hub
order: 2
cssclasses:
  - nav-menu
backward: "[[Computer Science]]"
parent: "[[Technology]]"
forward: "[[Development]]"
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

```dataview
LIST WITHOUT ID
file.link
FROM "Notes/Technology/Cybersecurity"
WHERE length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name = display(link(file.folder))
SORT order ASC
```


