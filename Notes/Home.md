---
tags:
  - type/hub
cssclasses:
  - dashboard-feed
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*


> [!note-toolbar] Home Tools
> - [:RiBrushFill:]()<data data-ntb-menu="91d0f70f-7985-49d5-8077-e1fd8ff325ce"/> <!-- Appearance -->
> - [:RiMenuSearchLine:]()<data data-ntb-menu="08ce42c6-2584-4733-8f55-711730ce0061"/> <!-- Search -->
# <div class="feed-section-header">Recently Updated</div>
```dataview
LIST WITHOUT ID file.link + "<span class='feed-meta'>Updated: " + dateformat(file.mtime, "MMM dd") + "</span>" FROM "" WHERE file.name != this.file.name AND !contains(file.folder, "Templates") SORT file.mtime DESC LIMIT 7
```
# <div class="feed-section-header">Needs Cleanup</div>
```dataview
LIST WITHOUT ID
file.link + "<span class='feed-meta'>" + split(file.folder, "/")[length(split(file.folder, "/")) - 1] + "</span>"
FROM #status/draft
WHERE !contains(file.folder, "Templates")
SORT file.mtime DESC
```
# <div class="feed-section-header">Study Queue</div>
```dataview
LIST WITHOUT ID
file.link + "<span class='feed-meta'>" + split(file.folder, "/")[length(split(file.folder, "/")) - 1] + "</span>"
FROM #status/review
WHERE !contains(file.folder, "Templates")
SORT file.mtime ASC
```

