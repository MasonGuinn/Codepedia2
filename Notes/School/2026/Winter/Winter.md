---
parent: "[[School]]"
forward: "[[Spring]]"
backward: "[[Notes/School/2025/Fall/Fall|Fall]]"
order: 1
cssclasses:
  - nav-menu
tags:
  - topic
year: "2026"
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

```dataview
LIST WITHOUT ID
file.link
FROM "Notes/School/2026/Winter"
WHERE length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name = display(link(file.folder))
SORT order ASC
```


