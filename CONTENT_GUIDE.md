# Content Guide for DHS Website

This guide explains how to add and edit content on the Data and Human Space course website.

---

## Quick Overview

- **Pages** (`_pages/`) — Static pages like Overview, Schedule, Resources
- **Posts** (`_posts/`) — Blog posts, announcements, assignments, tutorials
- **Navigation** (`_data/navigation.yml`) — Menu items
- **Configuration** (`_config.yml`) — Site-wide settings

---

## Pages: Course Information & Structure

Pages are for relatively static content that doesn't change frequently.

### Where Pages Go

All pages go in the `_pages/` directory.

### Current Pages

| Page | File | Purpose |
|------|------|---------|
| Overview | `overview.md` | Course info, description, projects |
| Outcomes | `outcomes.md` | Learning objectives |
| Schedule | `schedule.md` | Weekly schedule & dates |
| Principles | `principles.md` | Course values and approach |
| Resources | `resources.md` | Tools, data, and links |
| Archive | `archive.md` | Previous offerings |

### How to Edit a Page

1. Open the `.md` file in your text editor
2. Edit the content (everything after `---`)
3. Save the file
4. Refresh your browser to see changes

### How to Create a New Page

1. Create a new file in `_pages/` with a `.md` extension
2. Add front matter at the top:

```markdown
---
layout: single
title: "Page Title"
permalink: /page-slug/
author_profile: false
---

# Your Page Title

Your content here in Markdown...
```

3. Add the page to `_data/navigation.yml` to make it appear in the menu:

```yaml
- title: "Page Title"
  url: /page-slug/
```

### Front Matter Explained

| Field | Purpose |
|-------|---------|
| `layout: single` | Uses the single-column layout |
| `title` | Page title (appears in browser tab & header) |
| `permalink` | URL slug (must match navigation.yml) |
| `author_profile: false` | Don't show author sidebar |

---

## Posts: Announcements, Assignments, Blog

Posts are for content with dates. They're displayed in reverse chronological order (newest first) and can be tagged and categorized.

### Where Posts Go

All posts go in the `_posts/` directory.

### File Naming Convention

Posts **must** be named: `YYYY-MM-DD-title.md`

Examples:
- `2022-09-06-Welcome.md`
- `2022-09-20-Project1-OpenStreetMap.md`
- `2022-10-15-Lab-Tutorial-QGIS.md`

**Important:** Jekyll only processes files with the correct date format.

### Post Structure

```markdown
---
title: "Assignment: Project 1"
date: 2022-09-20
categories: Blog Assignments
tags:
  - F22
  - Projects
  - OpenStreetMap
---

## Your Post Title

Your content goes here...
```

### Front Matter Explained

| Field | Purpose |
|-------|---------|
| `title` | Post title |
| `date` | Publication date (YYYY-MM-DD) |
| `categories` | Broad categories (Blog, Assignments, etc.) |
| `tags` | Specific tags for filtering |

### Example Posts

**Announcement:**
```markdown
---
title: "Lab Session Rescheduled"
date: 2022-10-05
categories: Blog Announcements
tags:
  - F22
---

The lab session on October 6 has been rescheduled to October 7 due to university closure.
```

**Assignment:**
```markdown
---
title: "Assignment: Complete OSM Tutorial"
date: 2022-09-13
categories: Blog Assignments
tags:
  - F22
  - OpenStreetMap
---

## Assignment: Complete OSM Tutorial

Please complete the LearnOSM tutorial by September 20...

[Link to tutorial](https://learnosm.org)
```

**Tutorial/Blog Post:**
```markdown
---
title: "How to Use ArcGIS Online for Mapping"
date: 2022-10-01
categories: Blog Tutorials
tags:
  - F22
  - Tools
  - ArcGIS
---

## Getting Started with ArcGIS Online

Here's a step-by-step guide...
```

---

## Common Content Patterns

### Linking to Other Pages

```markdown
[Link Text]({{ site.baseurl }}/path-to-page/)

# Examples:
[Course Overview](/overview/)
[View the Schedule](/schedule/)
[Resources Page](/resources/)
```

### Linking to External Sites

```markdown
[Link Text](https://example.com)
```

### Embedding Images

```markdown
![Alt text for accessibility](/assets/images/filename.jpg)
```

### Creating Lists

**Unordered list:**
```markdown
- Item 1
- Item 2
- Item 3
```

**Ordered list:**
```markdown
1. First item
2. Second item
3. Third item
```

### Creating Tables

```markdown
| Column 1 | Column 2 |
|----------|----------|
| Data 1   | Data 2   |
| Data 3   | Data 4   |
```

### Code Blocks

**Inline code:**
```markdown
Use the `git add` command to stage changes.
```

**Code block:**
````markdown
```python
# Python code
print("Hello, World!")
```
````

### Emphasis

```markdown
*Italic* or _italic_
**Bold** or __bold__
***Bold and italic***
```

---

## Organizing Content

### Suggested Post Categories

- **Blog** — General posts
- **Announcements** — Course updates
- **Assignments** — Assignment descriptions
- **Tutorials** — How-to guides
- **Resources** — Tool guides and links

### Suggested Tags

- Semester: `F22`, `S23`, etc.
- Type: `Projects`, `Assignments`, `Tools`, `Readings`
- Tools: `OpenStreetMap`, `ArcGIS`, `QGIS`, `R`, etc.
- Topics: `Mapping`, `Data`, `Bias`, `GIS`, etc.

Tags make content discoverable on the `/tags/` page.

---

## Updating the Schedule

The Schedule page (`_pages/schedule.md`) should be updated each semester with:

- Course dates
- Weekly topics
- Assignment deadlines
- Important dates (breaks, exams, etc.)
- Office hours

Use this template:

```markdown
**Week 1 (Date Range):** Topic Title
- Topic detail
- Topic detail

**Week 2 (Date Range):** Topic Title
- Topic detail
```

---

## Adding Course Announcements

Create a new post with:
- **Date**: Today's date or future date
- **Category**: Announcements
- **Content**: Clear, actionable information

Example:

```markdown
---
title: "Lab Session Tomorrow: Introduction to OpenStreetMap"
date: 2022-09-12
categories: Blog Announcements
tags:
  - F22
---

Tomorrow's lab session (Tuesday, September 13) will cover:
- OpenStreetMap basics
- Creating an account
- Making your first edits

Please come with:
- Your laptop
- Create an OSM account before class

See you there!
```

---

## Updating Resources

The Resources page lists tools, datasets, and references. To add a new resource:

1. Open `_pages/resources.md`
2. Add it to the appropriate section with:
   - **Name** — Bold title
   - **URL** — Link in [brackets](url)
   - **Description** — What it is and why it's useful

Example:

```markdown
#### Tool Name
- **Website:** [toolname.com](https://toolname.com)
- **Description:** What this tool does and how we use it
- **Documentation:** [Link to docs](https://docs.example.com)
```

---

## Markdown Syntax Cheat Sheet

```markdown
# Heading 1
## Heading 2
### Heading 3

**Bold text**
*Italic text*
***Bold and italic***

- Bullet 1
- Bullet 2

1. Numbered 1
2. Numbered 2

[Link text](https://url.com)
![Alt text](/path/to/image.jpg)

`inline code`

> Blockquote text

---
(Horizontal line)
```

---

## Tips for Good Content

1. **Be clear and concise** — Course materials should be easy to understand
2. **Use headings** — Break content into scannable sections
3. **Add links** — Reference related pages and external resources
4. **Use images** — Visual materials help learning
5. **Include due dates** — For assignments, make deadlines very clear
6. **Provide context** — Explain why students are doing something
7. **Offer resources** — Link to tutorials, tools, and help materials

---

## Testing Content Locally

Before deploying, test content locally:

1. Create or edit your files
2. Run `bundle exec jekyll serve`
3. Go to `http://localhost:4000`
4. Check:
   - Is the page/post visible?
   - Do links work?
   - Are images displayed?
   - Does formatting look correct?

---

## Deploying Changes

When you're happy with your changes:

```bash
git add .
git commit -m "Descriptive message about what you changed"
git push origin main
```

Your changes will appear on GitHub Pages within a few minutes.

---

## Questions?

- Contact David Wrisley: [djw12@nyu.edu](mailto:djw12@nyu.edu)
- Check Jekyll documentation: [jekyllrb.com](https://jekyllrb.com/)
- Check Markdown guide: [markdownguide.org](https://www.markdownguide.org/)

---

**Happy writing!** ✍️
