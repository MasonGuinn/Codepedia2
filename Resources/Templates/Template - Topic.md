---
tags:
  - type/topic
  - status/draft
order: 
parent: "[[<% tp.file.folder(true).split('/').pop() %>]]"
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*


> [!abstract] Study Materials
> ```dataview
>  LIST WITHOUT ID 
>  "🔗 " + file.link 
>  FROM #type/flashcard
>  WHERE file.folder = this.file.folder
>  ```


## Lecture Notes