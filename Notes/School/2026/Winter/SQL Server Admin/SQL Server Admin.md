---
tags:
  - type/course
order: 2
cssclasses:
  - nav-menu
backward: "[[Network Security]]"
parent: "[[Winter]]"
forward: "[[Network Security]]"
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*


# <span class="nav-title">Modules</span>
```dataview
LIST WITHOUT ID
file.link
FROM #type/module
WHERE contains(file.folder, this.file.folder)
SORT order ASC
```

# <span class="nav-title">Tests</span>
```dataview
LIST WITHOUT ID file.link FROM #type/test-prep WHERE contains(file.folder, this.file.folder) SORT order ASC
```
# <span class="nav-title">Other</span>
```dataview
LIST WITHOUT ID
file.link
FROM ""
WHERE contains(file.folder, this.file.folder) 
  AND !contains(file.tags, "type/module") 
  AND !contains(file.tags, "type/test-prep")
  AND !contains(file.tags, "type/flashcard")
  AND file.name != this.file.name
SORT file.name ASC
```