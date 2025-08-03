# Welcome to Codepedia2

This vault is a dynamic knowledge base for tracking courses, tutorials, and notes on development and cybersecurity.

The core philosophy is to combine a simple **folder structure** with powerful **note properties** (metadata). This allows for flexible, automated navigation menus powered by the **Dataview** plugin and styled with custom **CSS**.

---

## Table of Contents

- [Plugins](#plugins)
- [Folder Structure](#folder-structure)
- [The Navigation System](#the-navigation-system)
	- [The Global Toolbar](#the-global-toolbar)
	- [Dynamic Content Menus](#dynamic-content-menus)
- [Creating](#creating)
	- [Creating a new Navigation Menu](#creating-a-new-navigation-menu)
	- [Creating a Content Note](#creating-a-content-note)

---

# Vault Details

## Plugins

- Dataview
- Folder notes
- Hider
- Homepage
- Iconize
- Lazy Plugin Loader
- Minimal Theme Settings
- Note Toolbar
- Style Settings

## Folder Structure

This vault uses the **Folder Note** plugin, allowing folders to also function as notes. This is used extensively to create hierarchical menus.

The folder structure is organized into broad categories called "Sections" e.g. `Technology` which contain more specific "Topics" e.g. `Cybersecurity` that contains "Subtopics" e.g. `Certificates`.

**Current Structure:**

```
- 📁 Resources/
  - 📁 Attachments/
  - 📁 Templates/
- 📁 School/
  - 📁 Fall 2025/
- 📁 Technology/
  - 📁 Computer Science/
  - 📁 Cybersecurity/
    - 📁 Certificates/
      - 📁 Network+/
        - 📄 OSI Model.md
        - 📄 Subnet.md
  - 📁 Development/
    - 📁 C/
    - 📁 Cpp/
    - 📁 CSharp/
    - 📁 Python/
- 📄 Home.md
```

## The Navigation System

This vault uses two types of navigation: a global toolbar at the top of every page and dynamic content menus inside specific notes.

### The Global Toolbar

This navigation bar appears at the top of every note and is powered by the **Note Toolbar** plugin.

- **Standard Links**: Always displays links to your sections: `Home`, `Technology`, and `School`.
    
- **Contextual Links**: A special `Back`, `Parent`, and `Forward` menu will automatically appear **only if** the current note has one of the following properties in its frontmatter: `prop_backward`, `prop_parent`, or `prop_forward`.
    

### Dynamic Content Menus

These are the styled menus found within your area notes and main topics created automatically using **Dataview**.

- **How to Style**: To style a Dataview query as a styled menu, add this property to the note's frontmatter:
    
    ```
    cssclasses: nav-menu
    ```
    
- **How it Works**: The `nav-menu` class activates the styles in `navigation.css`, turning a Dataview query into a styled menu. The query below, for example, automatically finds and displays the topics within the "Technology" folder.
    
    ```
    LIST WITHOUT ID
    file.link
    FROM "Technology"
    WHERE length(split(file.folder, "/")) = length(split(this.file.folder, "/")) + 1 AND file.name = display(link(file.folder))
    SORT order ASC
    ```
    
    This makes it so when you create a note, it automatically creates a navigation button within the menu. For more details on how to use this effectively, continue reading below.
    
---

## Creating

Below are some tips on how to create new menus and content.

### Creating a new Navigation Menu

A folder note is a note that serves as a navigation menu for a section, topic, and/or subtopic

1. Create a new folder (e.g., `Development`).
2. Ctrl+Left-Click on the folder or Right-Click -> Folder Note Commands -> Create Folder Note.
3. Add `cssclasses: nav-menu` to the frontmatter.
4. Add new folders/notes inside of the newly created `Development` folder note.
5. Add a styled title: `# <span class="nav-title">My Title</span>`.
6. Add a Dataview query to generate the links. 

**NOTE:** Make sure to change the `FROM "Technology/Development"` to where your new `Development` folder is located
```dataview
LIST WITHOUT ID
file.link
FROM "Technology/Development"
WHERE file.name != this.file.name
SORT order ASC
```
6. And that's it, for now on, any new notes or folders you add to the `Development` folder will automatically get populated on the menu. Look through the vault for examples.

**TIP:** You can do this quicker by Inserting the `Area Template` onto the note you created.

### Creating a Content Note

This is for a single piece of knowledge, like a chapter or concept.
1. **Workflow**: Insert a template (like `Note Template`) to create a new note with default properties.
2. **Key Properties**:
    - `order`: (Optional - number) Sets the sort order for menus.
    - `tags`: (Optional - text) Sets the category  e.g., `"Topic"`.
    - `prop_backward`: (Optional - obsidian note) Sets the backward note, and displays the contextual link button
    - `prop_parent`: (Optional - obsidian note) Sets the parent note, and displays the contextual link button
    - `prop_forward`: (Optional - obsidian note) Sets the forward note, and displays the contextual link button
        

---