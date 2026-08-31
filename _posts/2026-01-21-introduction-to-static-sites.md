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

Static sites are web pages that are delivered directly to the user's browser exactly as they are stored. Unlike dynamic sites that generate content on-the-fly using databases and server-side processing, static sites consist of fixed HTML, CSS, and JavaScript files. This simplicity offers numerous advantages for digital humanities and sustainable web practices.

This course site is an example of a very simple static site built in [Jekyll](https://jekyllrb.com/) in [Github Pages](https://docs.github.com/en/pages). 

Here are some customized ones: 
- [The Programming Historian](https://programminghistorian.org/) - also Jekyll and in Github.
- [Stanford Literary Lab](https://litlab.stanford.edu/) - they explain why they adopted a static site [here](https://litlab.stanford.edu/techne/new-litlab-website/)
- [Models Of and For](https://lib-static.github.io/models/) - A curated directory of projects using a static web approach (Models Of), templates / frameworks for creating new projects (Models For), and helpful utilities for Lib-Static development (Tools).
- [Collection Builder](https://collectionbuilder.github.io/) - an open source framework for creating digital collection and exhibit websites that are driven by metadata and powered by modern static web technology -- templates that work from Google Sheets!
- [Jekyll Themes for the Academic](https://jekyll-themes.com/category/academic)

<!--more-->

## Advantages of Static Sites

**Speed**: Static files load quickly since there are no server-side processing or database queries.

**Cybersecurity**: They have fewer moving parts and no dynamic backend processing, so static sites have fewer vulnerabilities.

**Simplicity**: Static sites are straightforward to understand, maintain, and deploy. No complex server configurations or database management required.

**Version Control**: Because static sites are typically .txt (plain text) files (often Markdown), they integrate with version control systems, enabling collaborative development. Both of the examples above are collaboratively managed.

**Sustainability**: Minimal server requirements mean lower resource consumption for more sustainable digital humanities projects.

**Inexpensive**: Hosting static sites is inexpensive, with many platforms offering free hosting options like GitHub Pages. What is required is some basic know how in versioning systems and Markdown.

## Static Sites and GitHub Pages

[GitHub Pages](https://pages.github.com/) is a hosting service that makes it easy to publish static sites directly from a GitHub repository. You can

- Write content in Markdown
- Version your entire site in VSCode
- Deploy changes with a simple push in VSCode or Github Desktop (for an added sanity check)
- Use themes for your site's appearance, and when you grow more confident, pass on to customization
- Maintain a complete history of all changes

## Elements required:

1. A GitHub account
2. A text editor (we will use VS Code, etc.)
3. Git and GitHub Desktop installed
4. Familiarity with Markdown


## Sustainability, Static Sites and Digital Humanities

As Wikle and Williamson argue in their [Code4Lib Journal article](https://journal.code4lib.org/articles/18372), static web methodology represents a shift in how digital humanities practitioners approach infrastructure. 

This philosophy aligns with principles of minimal computing in the digital humanities—asking what is truly necessary when developing digital scholarship under real-world constraints.

> **To read**: <br> -[Static Web Methodology as a Sustainable Approach to Digital Humanities Projects](https://journal.code4lib.org/articles/18372) by Olivia Wikle and Evan Peter Williamson (Code4Lib Journal, 2025). This article provides insight into why static web approaches are gaining traction in academic and digital humanities contexts, over web publishing methods such as WordPress or Drupal. <br> -[The Questions of Minimal Computing](https://dhq-static.digitalhumanities.org/pdf/000646.pdf) by Roopika Risam and Alex Gil (DHQ, 2022). The introduction to a special issue of _DHQ_ frames “minimal computing” as a way of thinking about digital humanities that prioritizes necessary and sufficient technologies under real-world constraints, using four questions (what is needed, what is available, what must be prioritized, and what can be sacrificed) to foreground practices that resist equating innovation with scale or resource intensity.

## Exploring the Components of the Minimal Mistakes Template

The [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Jekyll theme, which powers this course site, is built from several key components:

- **Layout Files** (`_layouts/`): HTML templates that define the structure of different page types (default, post, archive, etc.)
- **Include Files** (`_includes/`): Reusable HTML snippets (navigation, footer, header) that are embedded into layouts to avoid repetition
- **Assets** (`assets/`): Stylesheets (CSS), JavaScript files, and images that control the site's appearance and functionality
- **Configuration** (`_config.yml`): The main settings file controlling site title, theme, plugins, and other global behaviors
- **Content** (`_posts/`, `_pages/`): Your actual content files written in Markdown that Jekyll processes into HTML pages
- **Data Files** (`_data/`): YAML or JSON files containing structured information (like navigation menus) that templates can access and display

When you start with Minimal Mistakes, these components work together without issue. If you change things too quickly in the beginning you can break the site. As you gain confidence, however, you can customize individual pieces—changing colors in the CSS, modifying navigation structure in `_data/navigation.yml`, or adjusting layouts to create unique page designs—all without needing to rebuild the entire system.

Let's start by looking at a few elements `_data/navigation.yml`, `_pages`, `_posts` and `_config.yml`