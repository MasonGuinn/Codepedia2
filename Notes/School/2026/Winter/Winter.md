---
tags:
  - type/hub
order: 1
year: 2026
cssclasses:
  - nav-menu
parent: "[[School]]"
forward: "[[Spring]]"
backward: "[[Notes/School/2025/Fall/Fall|Fall]]"
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


