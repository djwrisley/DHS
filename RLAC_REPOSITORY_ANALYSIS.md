# RLAC Repository Structure Analysis
## For DHS Course Website Adaptation

**Repository:** https://github.com/djwrisley/RLAC  
**Theme:** Minimal Mistakes Jekyll Theme (Remote)  
**Purpose:** Course site for CDAD-UH 1024Q "Reading Like a Computer" at NYU Abu Dhabi  
**License:** CC BY-SA-NC 4.0 International (OER)

---

## 1. COMPLETE DIRECTORY STRUCTURE

```
RLAC/
├── README.md                          # Repository description
├── _config.yml                        # Main Jekyll configuration
├── Gemfile                            # Ruby dependencies
├── index.html                         # Home page redirect
├── .gitignore                         # Git ignore file
├── .DS_Store                          # macOS metadata (ignore)
│
├── _data/
│   ├── navigation.yml                 # Navigation menu configuration
│
├── _includes/
│   ├── footer/                        # Footer includes directory
│   ├── head/                          # Head includes directory
│   ├── masthead                       # Navigation/header template
│   └── nav_list                       # Navigation list template
│
├── _pages/
│   ├── 404.md                         # 404 error page
│   ├── archive.md                     # Archive/history page
│   ├── category-archive.md            # Category archive page
│   ├── tag-archive.md                 # Tag archive page
│   ├── year-archive.md                # Year archive page
│   ├── index.md                       # Home/welcome page
│   ├── outcomesS26.md                 # Course learning outcomes
│   ├── scheduleS26.md                 # Course schedule
│   ├── assessmentS26.md               # Assessment information
│   ├── rubricsS26.md                  # Grading rubrics
│   ├── responsesS26.md                # Responses guidelines
│   ├── materialsS25.md                # Course materials (previous semester)
│   ├── ufo.md                         # Unknown Flying Objects page (sample)
│   ├── assignment-1-guidelinesS26.md  # Assignment 1 guidelines
│   ├── assignment-2-guidelinesS26.md  # Assignment 2 guidelines
│   ├── assignment-3-guidelinesS26.md  # Assignment 3 guidelines
│
├── _posts/
│   ├── 2023-01-05-Assignment2.md
│   ├── 2024-02-13-guidelines-extra-credit.md
│   ├── 2025-01-28-customizing-your-static-siteS25.md
│   ├── 2025-01-29-disclosure-generative-AIS25.md
│   ├── 2025-01-30-sustainability-daahS25.md
│   ├── 2025-02-28-DOT-sensitive-historical-archives.md
│   ├── 2026-01-20-creating-a-static-siteS26.md
│   ├── 2026-01-21-introduction-to-static-sites.md
│   ├── 2026-02-12-assignment-1-corpus-analysisS26.md
│   ├── 2026-02-26-Response1-S26.md
│   ├── 2026-02-26-oralreflectionquestions.md
│   └── 2026-04-09-Assignment2-S26.md
│
└── assets/
    ├── css/                           # Custom CSS files directory
    ├── images/                        # Image assets
    │   └── bio-photo.jpg
    │   └── *.png (course screenshots)
    └── post templates/                # Post template examples
```

---

## 2. KEY CONFIGURATION FILES

### 2.1 `_config.yml` (Full Configuration)

```yaml
# Site settings
title: CDAD-UH 1024Q 
email: daahnyuad@gmail.com
description: >- 
  Course site for CDAD-UH 1024Q @ NYUAD
twitter_username: username
github_username: daahnyuad
minimal_mistakes_skin: dirt
search: true

# Build settings
markdown: kramdown
remote_theme: mmistakes/minimal-mistakes

# Outputting
permalink: /:categories/:title/
paginate: 5 # amount of posts to show
paginate_path: /page:num/
timezone: # https://en.wikipedia.org/wiki/List_of_tz_database_time_zones

include:
  - _pages

# Plugins
plugins:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jemoji
  - jekyll-include-cache

# Author configuration
author:
  name   : "NYU Abu Dhabi"
  avatar : "/assets/images/bio-photo.jpg"
  bio    : "Course site for Introduction to Digital Arts and Humanities."
  links:
    - label: "Website"
      icon: "fas fa-fw fa-link"
      url: "https://"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/daahnyuad"
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      url: "https://instagram.com/"

# Footer links
footer:
  links:
    - label: "Twitter"
      icon: "fab fa-fw fa-twitter-square"
      url: "https://twitter.com/"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/daahnyuad"
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      url: "https://instagram.com/"

# Default front matter for posts and pages
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: false
      read_time: true
      comments: false
      share: false
      related: true
  # _pages
  - scope:
      path: "_pages"
      type: pages
    values:
      layout: single
      author_profile: false

# Archive configuration
category_archive:
  type: liquid
  path: /categories/
tag_archive:
  type: liquid
  path: /tags/
```

### 2.2 `Gemfile` (Dependencies)

```ruby
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins
gem "tzinfo-data"
gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Jekyll plugins
group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
  gem "jemoji"
  gem "jekyll-include-cache"
  gem "jekyll-algolia"
end
```

### 2.3 `_data/navigation.yml` (Navigation Structure)

```yaml
main:
  - title: "Home"
    url: /
  - title: "Outcomes"
    url: /outcomes/
  - title: "Schedule"
    url: /schedule/
  - title: "Assessment"
    url: /assessment/
  - title: "Rubrics"
    url: /rubrics/
  - title: "Archive"
    url: /archive/
  - title: "Tags"
    url: /tags/
```

---

## 3. PAGES STRUCTURE AND FORMAT (`_pages/`)

### 3.1 Home Page (`index.md`) - Example

```markdown
---
layout: single
title: "Welcome"
permalink: /
---

<div style="background-color: #57068C; padding: 40px 20px; margin: 0 0 30px 0; text-align: center; border-radius: 0;">
  <h1 style="color: white; margin: 0; font-size: 2.5em; font-weight: 300; letter-spacing: 2px;">Reading Like a Computer</h1>
</div>

## Course Information 

- **Spring 2026 (19958) Section 1**
- **Number of credits**: 4 (14 weeks)
- **Instructor**: David Wrisley (djw12@)
- **Pre-requisites or co-requisites**: none

## BRIEF COURSE DESCRIPTION:

How can computers be said to "read" text, and how can computer-assisted analysis of texts give us new access to information about ourselves and the cultural legacies we have inherited? How well do LLMs do these tasks?

[Additional content...]

| **Element** | **Day** | **Timing** | **Location** | 
| Class | Tu | 11:20AM-12:35PM | Campus Center L00 W009 |
| Class | Th | 11:20AM-12:35PM | Campus Center L00 W009 | 
| Office hours | Tu / Th or by appt | between 1 and 3pm | A6 L01 1151 |

To see an archive of previous versions of this course, see [here](/archive/)
```

**Front Matter Pattern:**
- `layout: single` (most common for pages)
- `title: "Page Title"`
- `permalink: /custom-url/` (optional, defaults to filename)
- `author_profile: false` (usually disabled for pages)

### 3.2 404 Page (`404.md`) - Example

```markdown
---
title: "Page Not Found"
excerpt: "Page not found. Your pixels are in another canvas."
sitemap: false
permalink: /404.html
---

Sorry, but we can't find the page you were trying to view. Try the course [archive](/archive/), 
use the search box or check the tags tabs for a site-defined list of tags.
```

### 3.3 Archive Page (`archive.md`) - Example

```markdown
---
title: "Archive"
permalink: /archive/
author_profile: false
---

<div style="background-color: #57068C; padding: 40px 20px; margin: 0 0 30px 0; text-align: center; border-radius: 0;">
  <h1 style="color: white; margin: 0; font-size: 2.5em; font-weight: 300; letter-spacing: 2px;">Reading Like a Computer</h1>
</div>

## RLAC Archive

CDAD UH-1024 Reading Like a Computer is a course within the Data and Discovery branch 
of the Core Curriculum at NYU Abu Dhabi.

These syllabi are provided as open educational resources with a CC BY-SA-NC 4.0 International license. 

- [Before 2020](https://wp.nyu.edu/rlac/) 
- [Fall 2020](https://sites.google.com/nyu.edu/rlac)
- [Fall 2021](https://sites.google.com/nyu.edu/rlac-f21)
- [Fall 2022](https://sites.google.com/nyu.edu/rlac-f22/home) 

**Suggested Citation**: 
NYU Abu Dhabi. (semester/year). CDAD UH-1024: Reading Like a Computer. Abu Dhabi, UAE: David Joseph Wrisley.
```

### 3.4 Page Naming Conventions

- **Semester-specific pages**: `nameS26.md`, `nameS25.md` (S = Spring)
- **Archive pages**: `archive.md`, `category-archive.md`, `tag-archive.md`, `year-archive.md`
- **No subdirectories** - all pages stored flat in `_pages/`
- **Multiple versions** of same content (e.g., schedule for different semesters)

---

## 4. POSTS STRUCTURE AND FORMAT (`_posts/`)

### 4.1 Post Naming Convention

```
YYYY-MM-DD-post-title-with-hyphens.md
```

Examples:
- `2026-01-20-creating-a-static-siteS26.md`
- `2026-02-26-Response1-S26.md`
- `2026-04-09-Assignment2-S26.md`

### 4.2 Sample Post 1: Assignment Guidelines (`2026-02-26-Response1-S26.md`)

```markdown
---
title: "Response 1: On the Importance of Context for Visual Communication"
excerpt: "Using an LLM to Interpret without Context"
tags:
  - Responses
  - Corpora
  - Markdown
  - R
  - Voyant Tools
  - S26
---

## Overview - FINAL

Response 1 is an open-ended short essay style assignment that invites you to reflect on the importance of context for computational text analysis and the potential pitfalls of visualization-based interpretation for the corpus you chose.

- **Format:** Individual (maximum 1 person) 
- **Length:** Approximately 750 words, plus visuals (screenshots from LLM chat, prompts)
- **Due Date:** Sunday, 15 March 2026, 11:59pm

## Three Main Elements

This response has three core components:

1. **Going back to your visuals:** For the purposes of Assignment 1, you generated a few visuals...

2. **Interacting with the LLM(s) of your choice:** Use any LLM of your choice and in any language of your choice...

3. **Thinking and Interpreting the Results:** Include selective prompts you used in asking about the visuals...

Reference **at least one (1)** other readings or resources from this course...

## Guiding Questions

As you write, consider (but don't feel obligated to answer) all of these questions:

- Do visuals speak on their own? 
- If you looked at visuals created by a fellow student...
- Without context, what does an LLM say about your visuals?

## Assessment

Your work will be assessed according to the following criteria located [here](/rubrics/)

## Tips for Success

**Writing:** Use tools like [Markdown Live Preview](https://markdownlivepreview.com/) 
and [Hemingway App](https://hemingwayapp.com/)...

**Publishing:** Post your assignment to your course site as a post so instructors 
and classmates can read and engage with your work.
```

**Front Matter Pattern:**
```yaml
---
title: "Full Title Here"
excerpt: "Brief description for post preview"
categories:
  - Blog
tags:
  - tag1
  - tag2
  - semester
---
```

### 4.3 Sample Post 2: Tutorial/Lecture (`2026-01-21-introduction-to-static-sites.md`)

```markdown
---
title: "Introduction to Static Sites S26"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - S26
  - Github Pages
  - static sites
---

## What are Static Sites?

Static sites are web pages that are delivered directly to the user's browser exactly 
as they are stored. Unlike dynamic sites that generate content on-the-fly using databases 
and server-side processing, static sites consist of fixed HTML, CSS, and JavaScript files.

This course site is an example of a very simple static site built in [Jekyll](https://jekyllrb.com/) 
in [Github Pages](https://docs.github.com/en/pages). 

Here are some customized ones: 
- [The Programming Historian](https://programminghistorian.org/)
- [Stanford Literary Lab](https://litlab.stanford.edu/)

<!--more-->

## Advantages of Static Sites

**Speed**: Static files load quickly since there are no server-side processing or database queries.

**Cybersecurity**: They have fewer moving parts and no dynamic backend processing...

**Simplicity**: Static sites are straightforward to understand, maintain, and deploy...

**Version Control**: Because static sites are typically .txt (plain text) files (often Markdown), 
they integrate with version control systems...

## Elements required:

1. A GitHub account
2. A text editor (we will use VS Code)
3. Git and GitHub Desktop installed
4. Familiarity with Markdown

## Exploring the Components of the Minimal Mistakes Template

The [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Jekyll theme 
includes several key components:

- **Layout Files** (`_layouts/`): HTML templates
- **Include Files** (`_includes/`): Reusable HTML snippets
- **Assets** (`assets/`): Stylesheets (CSS), JavaScript files, and images
- **Configuration** (`_config.yml`): Main settings file
- **Content** (`_posts/`, `_pages/`): Your actual content files
- **Data Files** (`_data/`): YAML or JSON files
```

**Key Feature:** `excerpt_separator: "<!--more-->"` allows you to control where the preview cuts off in post listings.

### 4.4 Post Categories Used

- **Blog** (main category for all posts)

### 4.5 Common Tags Used

- `S26`, `S25` (Semester identifiers - Spring 2026, Spring 2025)
- `Responses`, `Assignments`
- `Github Pages`, `static sites`, `Markdown`
- `R`, `Voyant Tools`
- `Lab`, `tutorial`

---

## 5. INCLUDES (`_includes/`)

### 5.1 Masthead Template (`masthead` - no extension)

```liquid
{% if site.data.navigation.main %}
  <nav class="greedy-nav">
    <button class="greedy-nav__toggle hidden" type="button">
      <span class="visually-hidden">{{ site.data.ui-text[site.locale].menu_label | default: "Toggle menu" }}</span>
      <div class="navicon"></div>
    </button>
    <ul class="visible-links">
      {%- for link in site.data.navigation.main -%}
        <li class="masthead__menu-item">
          {%- if link.url -%}
            <a href="{{ link.url | relative_url }}" class="masthead__menu-link" 
               {%- if page.url == link.url %} class="active"{% endif %}>
              {{ link.title }}
            </a>
          {%- elsif link.children -%}
            <span class="masthead__menu-link masthead__menu-parent">{{ link.title }}</span>
            <ul class="submenu">
              {%- for child in link.children -%}
                <li>
                  <a href="{{ child.url | relative_url }}" class="submenu__link"
                     {%- if page.url == child.url %} class="active"{% endif %}>
                    {{ child.title }}
                  </a>
                </li>
              {%- endfor -%}
            </ul>
          {%- else -%}
            <span class="masthead__menu-link">{{ link.title }}</span>
          {%- endif -%}
        </li>
      {%- endfor -%}
    </ul>
    {%- if site.data.navigation.main.size > 0 -%}
      <button class="greedy-nav__toggle-all hidden" type="button">
        {{ site.data.ui-text[site.locale].menu_label | default: "Menu" }}
      </button>
      <ul class="hidden-links hidden"></ul>
    {%- endif -%}
  </nav>
{% endif %}
```

**Purpose:** Renders the navigation menu from `_data/navigation.yml`

### 5.2 Directory Structure

- `_includes/footer/` - Footer include files (empty/collapsed)
- `_includes/head/` - Head include files (empty/collapsed)
- `_includes/masthead` - Main navigation template
- `_includes/nav_list` - Navigation list template

**Note:** The repository has a "flattened structure" - most custom includes have been removed, relying instead on the Minimal Mistakes theme defaults.

---

## 6. OVERALL ORGANIZATION & LINKING STRATEGY

### 6.1 Navigation Flow

```
Home (/)
├── Outcomes (/outcomes/ → outcomesS26.md)
├── Schedule (/schedule/ → scheduleS26.md)
├── Assessment (/assessment/ → assessmentS26.md)
├── Rubrics (/rubrics/ → rubricsS26.md)
├── Archive (/archive/ → archive.md)
└── Tags (/tags/ → tag-archive.md)
```

### 6.2 URL Permalink Strategy

From `_config.yml`:
```yaml
permalink: /:categories/:title/
```

This means:
- Posts in "Blog" category: `/blog/post-title/`
- Pages use their filename with permalink override (e.g., `permalink: /schedule/`)

### 6.3 Cross-Linking Patterns

**Within Pages:**
```markdown
[Link Text](/path/) 
[Archive](/archive/)
[Rubrics](/rubrics/)
```

**Within Posts:**
```markdown
[related page](/outcomes/)
[rubrics](/rubrics/)
```

**External Links:**
```markdown
[The Programming Historian](https://programminghistorian.org/)
[GitHub Repo](https://github.com/username/repo)
```

### 6.4 Semantic Versioning for Semesters

All course-specific content uses semester suffixes:
- `S26` = Spring 2026
- `S25` = Spring 2025

This allows:
1. Multiple versions of same page (e.g., `scheduleS26.md`, `scheduleS25.md`)
2. Easy navigation to archives
3. Filtering posts/pages by semester using tags

### 6.5 Content Organization Principles

1. **Core pages** in `_pages/`: Always available (Home, Archive, About)
2. **Course content pages** in `_pages/`: Semester-specific (Schedule, Assessment, Rubrics)
3. **Posts** in `_posts/`: Class notes, announcements, tutorials
4. **Guidelines** in `_pages/`: Assignment guides (can also be posts)
5. **No subdirectories** in `_pages/` or `_posts/` - flat file structure

---

## 7. TEMPLATE & LAYOUT PATTERNS

### 7.1 Default Front Matter for Pages

```yaml
---
layout: single
title: "Page Title"
permalink: /custom-url/
author_profile: false
---
```

### 7.2 Default Front Matter for Posts

```yaml
---
title: "Post Title"
excerpt: "Brief description"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - tag1
  - tag2
  - semester
---
```

### 7.3 Custom HTML Patterns

**Purple header banner** (used throughout):
```html
<div style="background-color: #57068C; padding: 40px 20px; margin: 0 0 30px 0; text-align: center; border-radius: 0;">
  <h1 style="color: white; margin: 0; font-size: 2.5em; font-weight: 300; letter-spacing: 2px;">
    Reading Like a Computer
  </h1>
</div>
```

**Embedded images**:
```markdown
<img src="/assets/images/filename.png" style="zoom:50%;" />
```

**Tables**:
```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
```

---

## 8. ASSETS STRUCTURE

```
assets/
├── css/                          # Custom CSS (currently unused/empty)
├── images/                       # Image repository
│   ├── bio-photo.jpg            # Author photo
│   ├── creatingacct.png         # Tutorial screenshots
│   ├── clonerepo.png
│   └── pushing.png
└── post templates/              # Template examples for content
```

**Image referencing:**
```markdown
![Alt text](/assets/images/filename.png)
<img src="/assets/images/filename.png" style="zoom:50%;" />
```

---

## 9. README CONTENT

The repository README indicates this is a minimal-mistakes remote theme starter template. Key information:

```markdown
# Minimal Mistakes remote theme starter

Contains basic configuration to get you a site with:

- Sample posts.
- Sample top navigation.
- Sample author sidebar with social links.
- Sample footer links.
- Paginated home page.
- Archive pages for posts grouped by year, category, and tag.
- Sample about page.
- Sample 404 page.
- Site wide search.
```

---

## 10. KEY TAKEAWAYS FOR REPLICATION

### For Your DHS Course Website:

1. **Start with Minimal Mistakes template** - Use "Use this template" from https://github.com/mmistakes/mm-github-pages-starter

2. **Configuration priorities:**
   - Update `_config.yml` with your site title, description, author info
   - Modify `_data/navigation.yml` for your site structure
   - Set appropriate theme (e.g., `minimal_mistakes_skin: dirt` or choose another)

3. **Content structure:**
   - Create `_pages/` for static course content (syllabus, schedule, rubrics, assessment)
   - Use `_posts/` for class announcements, tutorials, assignment guidelines
   - Keep flat file structure - no subdirectories

4. **Semester versioning:**
   - Adopt naming convention like `S26` (Spring 2026) or `F25` (Fall 2025)
   - Use suffixes in filenames: `scheduleS26.md`, `assignmentF25.md`
   - Use tags to filter by semester

5. **Front matter standardization:**
   - All pages: `layout: single`, `title:`, `permalink:`, `author_profile: false`
   - All posts: `title:`, `excerpt:`, `categories: [Blog]`, `tags: [...]`

6. **Cross-linking strategy:**
   - Use relative URLs: `[link](/page-name/)`
   - Reference external resources with full URLs
   - Build hierarchical structure through `_data/navigation.yml`

7. **Visual consistency:**
   - Create custom header banner in HTML/CSS
   - Use consistent image sizing with inline style: `style="zoom:50%;"`
   - Implement tables for structured information

8. **Plugin enablement:**
   - Include pagination, sitemap, feed, emoji support, and include caching

---

## 11. DEPLOYMENT

**GitHub Pages Settings:**
1. Go to repository Settings > Pages
2. Select `master` (or `main`) branch
3. Watch for green checkmark indicating successful build
4. Site becomes available at `https://username.github.io/repository-name/`

**Push workflow:**
- Edit locally in text editor (VSCode recommended)
- Commit changes in GitHub Desktop or via terminal
- Push to remote repository
- GitHub Pages automatically rebuilds site (typically 1-2 minutes)

---

## LICENSE & CITATION

**Original Minimal Mistakes Theme:** MIT License  
**RLAC Course Content:** CC BY-SA-NC 4.0 International

**Suggested Citation Format:**
```
NYU Abu Dhabi. (Semester/Year). [Course Number]: [Course Title]. 
Abu Dhabi, UAE: [Instructor Name].
```

---

**Document Generated:** April 27, 2026  
**Analysis Based On:** djwrisley/RLAC repository (master branch, current state)
