---
tags:
  - type/topic
order: 1
cssclasses:
  - dashboard-feed
backward: "[[SQL Server Admin]]"
parent: "[[SQL Server Admin]]"
forward: "[[SSMS, System DBs & Physical Structure]]"
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*


> [!abstract] Study Materials
> ```dataviewjs
> const folderPath = dv.current().file.folder;
> const currentFileName = dv.current().file.name;
> const folder = app.vault.getAbstractFileByPath(folderPath);
> if (folder && folder.children) {
> 	const links = folder.children
> 		.filter(file => {
> 			if (file.name === currentFileName || file.name === currentFileName + ".md") return false;
> 			const isPdf = file.name.toLowerCase().endsWith(".pdf");
> 			const isFlashcard = dv.page(file.path)?.tags?.includes("type/flashcard");
> 			return isPdf || isFlashcard;
> 		})
> 		.map(file => dv.fileLink(file.path));
> 	if (links.length > 0) {
> 		dv.list(links);
> 	} else {
> 		dv.paragraph("No study materials found in this folder.");
> 	}
> } else {
> 	dv.paragraph("Error: Could not find folder path.");
> }
> ```

## Lecture Notes