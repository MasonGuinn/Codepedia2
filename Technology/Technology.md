---
order: 1
cssclasses:
  - nav-menu
tags:
  - section
bg: https://i.pinimgproxy.com/?url=aHR0cHM6Ly9jZG4taWNvbnMtcG5nLmZsYXRpY29uLmNvbS8yNTYvOTAyOC85MDI4Njk3LnBuZw==&ts=1763350073&sig=4ef23ecee8259c4ea035b7e03c577f46f5a50f07a1bbd7f25889057ae0333856
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

```dataview
LIST WITHOUT ID
file.link
FROM "Technology"
WHERE length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name = display(link(file.folder))
SORT order ASC
```


