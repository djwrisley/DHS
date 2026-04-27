# Getting Started with the DHS Jekyll Site

This guide will help you set up, build, and deploy the Data and Human Space course website locally and on GitHub Pages.

## What Is This?

This is a Jekyll-based static website for the CDAD-UH 1033EQ course. It's built with:
- **Jekyll** — A static site generator
- **Minimal Mistakes theme** — A clean, minimal theme
- **GitHub Pages** — Free hosting

The site structure mirrors the RLAC course site but is customized for the Data and Human Space course.

---

## Prerequisites

Before getting started, you'll need:

- **Ruby** (version 2.7.0 or higher)
  - Check your version: `ruby --version`
  - Install from [ruby-lang.org](https://www.ruby-lang.org/) if needed
  
- **Bundler** (for managing Ruby gems)
  - Install: `gem install bundler`
  - Check version: `bundle --version`

- **Git** (for version control)
  - Check: `git --version`
  - Install if needed

---

## Local Development Setup

### 1. Clone the Repository

```bash
git clone https://github.com/djwrisley/DHS.git
cd DHS
```

### 2. Install Dependencies

```bash
bundle install
```

This reads the `Gemfile` and installs all required Ruby gems (Jekyll, the Minimal Mistakes theme, plugins, etc.)

### 3. Build and Serve Locally

```bash
bundle exec jekyll serve
```

You should see output like:
```
Configuration file: /path/to/DHS/_config.yml
            Source: /path/to/DHS
       Destination: /path/to/DHS/_site
 Incremental build: enabled
      Generating... 
       Jekyll Feed: Generating feed for posts
                    done in 0.456 seconds.
 Auto-regeneration: enabled for '/path/to/DHS'
    Server address: http://127.0.0.1:4000
  Server running...
  Press Ctrl-C to stop.
```

### 4. View the Site

Open your web browser and go to: **http://localhost:4000**

You should see the DHS course homepage!

---

## Making Changes

### Edit Pages

Pages are in the `_pages/` directory. They're written in Markdown:

- `overview.md` — Course overview
- `outcomes.md` — Learning outcomes
- `schedule.md` — Weekly schedule
- `principles.md` — Course principles
- `resources.md` — Tools and resources
- `archive.md` — Links to previous offerings

To edit a page, open it in your text editor, make changes, save it. Jekyll will automatically regenerate the site (watch for "Regenerating: " in your terminal).

**Refresh your browser** to see the changes.

### Add Blog Posts

Blog posts go in the `_posts/` directory. They must be named: `YYYY-MM-DD-title.md`

Example: `2022-09-30-Assignment-Due.md`

Blog post structure:

```markdown
---
title: "Your Post Title"
date: YYYY-MM-DD
categories: Blog
tags:
  - F22
  - tag2
  - tag3
---

Your content goes here in Markdown.
```

### Update Navigation

The main navigation menu is in `_data/navigation.yml`. To add or change menu items:

```yaml
main:
  - title: "Page Name"
    url: /page-url/
  - title: "Another Page"
    url: /another-page/
```

### Configuration

Site-wide settings are in `_config.yml`:
- `title` — Site title
- `description` — Site description
- `author` — Author information
- `footer` — Footer links
- Theme settings

---

## Directory Structure

```
DHS/
├── _config.yml              # Jekyll configuration
├── _data/
│   └── navigation.yml       # Main navigation menu
├── _pages/                  # Pages (about, outcomes, etc.)
│   ├── overview.md
│   ├── outcomes.md
│   ├── schedule.md
│   ├── principles.md
│   ├── resources.md
│   └── archive.md
├── _posts/                  # Blog posts and announcements
│   ├── 2022-09-06-Welcome.md
│   ├── 2022-09-06-Tech-Setup.md
│   └── ...
├── _site/                   # Generated site (don't edit)
├── assets/                  # Images, CSS, etc.
├── 404.md                   # 404 page
├── Gemfile                  # Ruby dependencies
├── Gemfile.lock            # Locked versions (auto-generated)
├── README.md               # Repository README
├── GETTING_STARTED.md      # This file
└── index.html              # Homepage
```

---

## Deploying to GitHub Pages

### Prerequisites

- Repository on GitHub: `djwrisley/DHS`
- Repository set to public (for free hosting)

### Deployment Steps

1. **Commit and push your changes:**

```bash
git add .
git commit -m "Update course content"
git push origin main
```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
   - Click "Save"

3. **GitHub will automatically build and deploy!**

Your site should be live at: `https://djwrisley.github.io/DHS/`

(It may take a few minutes for changes to appear.)

### Troubleshooting Deployment

If the site doesn't appear:

1. Check GitHub Actions
   - Go to Actions tab on your repository
   - Look for any failed builds
   - Click on failed builds to see error messages

2. Check Settings
   - Go to Settings → Pages
   - Verify the source is set correctly
   - Verify the branch exists

3. Check the repo is public
   - Settings → General
   - Repository visibility should be "Public"

---

## Customization

### Change the Theme Skin

In `_config.yml`, change:
```yaml
minimal_mistakes_skin: dirt
```

Options: `air`, `aqua`, `contrast`, `dark`, `default`, `dirt`, `neon`, `mint`, `plum`, `sunrise`

### Add Custom CSS

Create `assets/css/style.scss`:

```scss
---
---

@import "minimal-mistakes/skins/{{ site.minimal_mistakes_skin | default: 'default' }}";
@import "minimal-mistakes"; // main stylesheet

// Your custom CSS here
```

### Add Images

1. Place images in `assets/images/`
2. Reference them in Markdown:
   ```markdown
   ![Alt text](/assets/images/filename.jpg)
   ```

---

## Useful Jekyll Commands

```bash
# Build the site (generates _site/)
bundle exec jekyll build

# Build and serve locally (with auto-regeneration)
bundle exec jekyll serve

# Build with drafts included (for testing unpublished posts)
bundle exec jekyll serve --drafts

# Clean build (removes _site/ and rebuilds from scratch)
bundle exec jekyll clean
bundle exec jekyll build
```

---

## Common Issues and Solutions

### "Bundler could not find compatible versions of gem"

**Solution:** Update bundler
```bash
bundle update
```

### Changes not showing up

**Solution:** 
1. Stop the Jekyll server (Ctrl+C)
2. Run: `bundle exec jekyll clean`
3. Run: `bundle exec jekyll serve` again

### "Jekyll not found" or "bundle not found"

**Solution:** Reinstall dependencies
```bash
bundle install
```

### Port 4000 already in use

**Solution:** Use a different port
```bash
bundle exec jekyll serve --port 4001
```

---

## Learning More

### Jekyll Documentation
- [Jekyll Docs](https://jekyllrb.com/docs/)
- [Jekyll Front Matter](https://jekyllrb.com/docs/front-matter/)
- [Jekyll Markdown](https://jekyllrb.com/docs/liquid/tags/)

### Minimal Mistakes Documentation
- [Minimal Mistakes Setup Guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
- [Minimal Mistakes Configuration](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

### Markdown Syntax
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/)

### GitHub Pages
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Troubleshooting GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-common-issues-with-github-pages)

---

## Questions?

- Contact David Wrisley: [djw12@nyu.edu](mailto:djw12@nyu.edu)
- Open an issue on GitHub (if you have a GitHub account)

---

**Happy editing!** 🎉
