---
tags:
  - type/hub
cssclasses:
  - nav-menu
order:
backward:
parent: "[[<% tp.file.folder(true).split('/').slice(-2, -1) %>]]"
forward:
---
> *Created: <% tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <% tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*


# <span class="nav-title"><% tp.file.title %></span>
```dataview
LIST WITHOUT ID file.link FROM "" WHERE contains(file.folder, this.file.folder) AND length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name != this.file.name SORT order ASC
```