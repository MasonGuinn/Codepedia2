---
backward: "[[SQL Server Admin]]"
parent: "[[Winter]]"
forward: "[[SQL Server Admin]]"
order: 2
tags:
  - topic
cssclasses:
  - nav-menu
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

# <span class="nav-title">Modules</span>
```dataview
LIST WITHOUT ID
file.link
FROM "Notes/School/2026/Winter/Network Security"
WHERE contains(file.name, "Module")
SORT order ASC
```


# <span class="nav-title">Other</span>
```dataview
LIST WITHOUT ID
file.link
FROM "Notes/School/2026/Winter/Network Security"
WHERE !contains(file.name, "Module")
AND file.name != this.file.name SORT order ASC
```

