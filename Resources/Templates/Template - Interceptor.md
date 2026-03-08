<%*
// 1. Prompt for the real name immediately
let title = await tp.system.prompt("Enter Note Name:");

// Get the actual file Templater is running on (the Untitled.md file)
let currentFile = tp.config.target_file;

// 2. If you hit cancel or press ESC, delete the accidental 'Untitled' file and stop
if (!title) {
    await app.vault.trash(currentFile, true);
    return;
}

// 3. Determine the path for the new file
let folderPath = currentFile.parent.path;
let newPath = folderPath === "/" ? title + ".md" : folderPath + "/" + title + ".md";

// 4. Create the NEW file. (This action tells Obsidian a new file was born, triggering your Regex!)
let newFile = await app.vault.create(newPath, "");

// 5. Open the new file so you can start typing
await app.workspace.getLeaf(false).openFile(newFile);

// 6. Clean up by deleting the dummy 'Untitled' file after a tiny delay to prevent errors
setTimeout(async () => {
    await app.vault.trash(currentFile, true);
}, 100);
%>