# Welcome to Your Knowledge Vault

This vault is designed to be a dynamic and organized personal knowledge base for tracking courses, tutorials, and notes, primarily for development and cybersecurity studies.

The core philosophy is to use **simple folders** for broad categories and **powerful metadata** (properties) within notes to create flexible, automated navigation and organization.

---

## How It Works: The Core Components

This system relies on a few key parts working together:

1. **Folder Structure**: A simple, high-level structure to keep content organized.
    
2. **Note Properties (Frontmatter)**: The "brains" of the system, used for tagging, sorting, and creating dynamic connections.
    
3. **Dashboard Notes**: Hub pages that use Dataview queries to automatically generate navigation menus.
    
4. **Custom CSS**: A snippet (`navigation.css`) that makes the dashboards and navigation look clean and modern.
    
5. **Templates**: A Templater script to automate the creation of new notes.
    

---

## 1. Folder Structure

The $\color{Green}{\textsf{Green}}$ color represents a folder note (a folder that is also a note) using the folder-note plugin

- $\color{Green}{\textsf{`Resources/`}}$ -
	- $\color{Green}{\textsf{`Attachments/`}}$ - 
	- `Templates/` - 
- `School/` - 
	- `Fall 2025/` - 
	- `Spring 2026/`
	- `Winter 2026/`
- `Technology/`
	- `Computer Science/`
	- `Cybersecurity/`
		- `Certificates/`
			- `Network+/`
				- `OSI Model`
				- `Subnet`
	- `Development/`
		- `C/`
		- `Cpp/`
		- `CSharp/`
		- `Python/`
- `Home`


---

## 2. Creating and Organizing Notes

### Creating a New Lesson/Topic Note

This is for a single piece of knowledge, like a chapter or a concept.

- **Workflow**: Use the **Templater** plugin to create a new note from your `Dev Topic Template`.
    
- **Key Properties**:
    
    - `order`: This is automatically calculated by the template to set the sort order.
        
    - `certification`: (Optional) The certification it belongs to (e.g., `"CompTIA Network+"`).
        
    - `provider`: (Optional) The source of the information (e.g., `"Professor Messer"`).
        
    - `domain`: (Optional) The specific exam domain (e.g., `"1.0 Networking Fundamentals"`).
        
    - `tags`: (Optional) Add relevant tags for searching (e.g., `network`, `python`).
        

### Creating a New Dashboard Note

This is for a navigation page that links to other notes or dashboards.

- **Workflow**: Create a new note and add the following frontmatter.
    
- **Key Properties**:
    
    - `cssclasses: nav-hub`: **This is essential.** It activates your custom CSS styling for this page.

---

## 3. The Navigation System

Your navigation is powered by a combination of a CSS class, a custom CSS snippet, and Dataview queries.

#### The `nav-hub` Class

Adding `cssclasses: nav-hub` to a note's frontmatter "turns on" all the custom styling for navigation bars and titles on that page.

#### The Styled Title

To create a large, styled header that matches your navigation buttons, use this format in your note:

Markdown

```
### <span class="nav-title">My Title Here</span>
```

#### The Dynamic Button Bar

This is the core of your navigation. This code creates the button bar by finding all the main "index" notes within a folder specified in the frontmatter.

**For a list of sub-topics (like in `Development.md`):**

Code snippet

```
TABLE WITHOUT ID
file.link
FROM "Content/Development"
WHERE file.name = display(link(file.folder))
SORT order ASC
```

**For a list of lessons (like in `Network+ Dashboard.md`):**

Code snippet

```
dv.table([],
    dv.pages(dv.current().source_folder)
      .sort(p => p.file.name, 'asc')
      .map(p => [p.file.link])
);
```

---

Happy note-taking!

Sources
