# Quick Setup Guide

## 1. Clone and Open
```bash
git clone <your-repo-url>
cd marp-template
code .
```

## 2. Install Marp Extension
- Open VS Code
- Go to Extensions (`Ctrl+Shift+X`)
- Search for "Marp for VS Code"
- Install the extension

## 3. Configure VS Code Settings
Add these settings to your VS Code settings.json:

```json
{
    "markdown.marp.html": "all",
    "markdown.marp.themes": [
        ".vscode/extra.css",
        ".vscode/a4.css"
    ]
}
```

## 4. Start Creating
- Open `template_slides.md` to see examples
- Create your own `.md` file
- Use the preview button (top-right) to see your slides
- Export to PDF using "Marp: Export Slide Deck"

## 5. Add Your Content
- Place images in the `imgs/` folder
- Replace the logo in `logos/` with your institution's logo
- Customize the themes in `.vscode/extra.css` and `.vscode/a4.css`

## Quick Start Template
```markdown
---
marp: true
theme: extra
paginate: true
html: true
footer: Your Course Name
---

# Your Slide Title

Your content here...

---

## Second Slide

![center w:400px](imgs/your-image.png)

More content...
```
