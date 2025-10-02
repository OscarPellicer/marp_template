---
marp: true
theme: a4
paginate: true
html: true
# footer: Marp template setup guide
---

# A Marp template for academic courses

This repostory contains a template for creating academic presentations using **Marp** (Markdown Presentation Ecosystem) with **VS Code**, two custom themes (`extra.css` and `a4.css`), and a guide for setting up VS Code for Marp and start using these themes. The template includes:

- **Two custom themes**: `extra.css` (presentations) and `a4.css` (documents)
- **Pre-configured settings** for optimal development experience
- **Example slides** demonstrating all available features
- **Comprehensive documentation** for easy customization

Why Marp?

- **Markdown-based**: Write presentations in familiar Markdown syntax (including $\LaTeX$ for mathematical expressions, highlighting for code blocks, tables, etc.)
- **Version control friendly**: Easy to track changes with Git
- **Consistent styling**: Professional appearance across all slides
- **Zero compilation time**: The preview updates instantly, unlike other tools like $\LaTeX$
- **Extensible**: Easily add your own themes and features using HTML and CSS
- **AI-friendly**: Easy to integrate with AI tools since it is a Markdown file

## Prerequisites

Before setting up this template, ensure you have installed VS Code with the following extensions:
- **Marp for VS Code** (essential)
- **Markdown All in One** (helpful for editing)
- **markdownlint** (helpful for linting)

## Repository setup

Clone the Repository and open it in VS Code

```bash
git clone https://github.com/OscarPellicer/marp_template.git
cd marp_template
code .
```

## VS Code configuration

<div class="columns">
<div><br>

By default, the `.vscode/settings.json` file is already configured for you, but in case it is not working or you want to modify it, you can do so by opening the settings file (`Ctrl+Shift+P` $\rightarrow$ `Preferences: Open User Settings (JSON)`).

</div>
<div>
<br>

```json
{
    "markdown.marp.html": "all",
    "markdown.marp.themes": [
        ".vscode/extra.css",
        ".vscode/a4.css"
    ]
}
```

</div>
</div>

---

## Creating your first slides

Create a new markdown file in your repository, add the frontmatter and start writing your slides:

```markdown
---
marp: true
theme: extra
paginate: true
html: true
footer: Your Course Name
---

# Your Slide Title

- Bullet point 1
- Bullet point 2
- Bullet point 3

---

## Second Slide

![center w:400px](imgs/your-image.png)

Your content here...
```

Alternatively, you can use my other repository https://github.com/OscarPellicer/pptx2marp to convert PowerPoint (`.pptx`) presentations to Marp slides, and start from there:

```bash
pip install -e git+https://github.com/OscarPellicer/pptx2marp.git
pip install -e git+https://github.com/OscarPellicer/python-pptx.git
```

## Available themes

<div class="columns">
<div>

<br>

Extra Theme (`extra.css`)
- **Purpose**: Presentation slides
- **Features**: 
  - Multi-column layouts
  - Image positioning
  - Custom fonts
  - Professional styling
- **Best for**: Course presentations, lectures

</div>
<div>
<br>

A4 Theme (`a4.css`)
- **Purpose**: Document-style pages
- **Features**:
  - A4 page size (210mm × 297mm)
  - Justified text
  - Academic formatting
  - Print-friendly layout
- **Best for**: Handouts, documentation, reports

</div>
</div>

---

## Template features

- **Multi-column grids**: 2 and 3 column layouts
- **Absolute positioning**: Precise element placement
- **Floating images**: Left, right, and center alignment
- **Figure containers**: Professional image captions
- **Custom fonts**: Open Sans (presentation), Libre Baskerville (A4), etc.
- **Text sizing**: Small, smaller, smallest classes
- **Mathematical expressions**: LaTeX-style math support
- **Code highlighting**: Syntax highlighting for code blocks
- **Custom classes**: No-footer, small text, etc.
- **Reference styling**: Professional citations
- **Responsive design**: Adapts to different screen sizes
- **Print optimization**: A4 theme optimized for printing

## Advanced features

Multi-Column Layouts

```html
<div class="columns">
<div>

  * First column content
  * Can contain lists, paragraphs, etc.

</div>
<div>

  * Second column content
  * Each column is equally sized

</div>
</div>
```

Figure Containers

```html
<div class="figure-container align-right" style="width: 300px;">
  <img src="imgs/image.png" alt="Description" width="300">
  <p class="figcaption">Your caption here.</p>
</div>
```

Absolute Positioning

```html
<div class="abs-pos" style="left: 400px; top: 100px; width: 300px; height: 200px; z-index: 1;">
  <img src="imgs/image.png" alt="Positioned image" style="width: 100%; height: 100%; object-fit: cover;">        
</div>
```

## Exporting to PDF


1. Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac)
2. Type "Marp: Export Slide Deck"
3. Choose PDF format
4. Select save location
