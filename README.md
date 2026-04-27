# Data and Human Space (CDAD-UH 1033EQ)

This repository contains the Jekyll-based website for **CDAD-UH 1033EQ: Data and Human Space** at NYU Abu Dhabi.

## About the Course

This course explores the intersection of technology, geography, and human space through the lens of digital mapping, geospatial analysis, and data visualization. Students engage with tools like OpenStreetMap, ArcGIS Online, ESRI Storymaps, and R to understand how maps represent (and misrepresent) our world.

**For complete course information, visit:** [https://djwrisley.github.io/DHS](https://djwrisley.github.io/DHS) (when deployed)

## Repository Structure

```
DHS/
├── _config.yml           # Jekyll configuration
├── _data/
│   └── navigation.yml    # Main navigation menu
├── _pages/               # Course pages
│   ├── overview.md       # Course overview and information
│   ├── outcomes.md       # Learning outcomes
│   ├── schedule.md       # Weekly course schedule
│   ├── principles.md     # Course principles and values
│   ├── resources.md      # Tools, data, and resources
│   └── archive.md        # Archive of previous offerings
├── _posts/               # Blog posts and announcements
├── assets/               # Images, CSS, and other static files
├── Gemfile               # Ruby dependencies for Jekyll
├── .gitignore           # Git ignore file
└── index.html           # Homepage
```

## Building and Running Locally

### Prerequisites

- Ruby 2.7.0 or higher
- Bundler

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/djwrisley/DHS.git
   cd DHS
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Run the Jekyll development server:
   ```bash
   bundle exec jekyll serve
   ```

4. Open your browser and visit: `http://localhost:4000`

## Deployment

This site is deployed using GitHub Pages. Simply push changes to the `main` branch, and the site will rebuild automatically.

## Based On

This course site is built with:
- **Jekyll** — Static site generator
- **Minimal Mistakes theme** — Beautiful, minimal Jekyll theme
- **GitHub Pages** — Free hosting for static sites

## Course Information

- **Semester:** Fall 2022
- **Meeting Times:** TuTh 15:35 - 16:50
- **Location:** C2 W008, NYUAD
- **Instructor:** David Wrisley ([djw12@nyu.edu](mailto:djw12@nyu.edu))
- **Credits:** 4 (14 weeks)
- **Core Requirement:** Data and Discovery (Q) & Experimental (E)

## Previous Versions

This course has been offered in previous semesters:
- [Fall 2022 (Google Sites)](https://sites.google.com/nyu.edu/dhs-f22)
- [Spring 2021](https://sites.google.com/nyu.edu/dhs-s2021/)
- [Fall 2020](https://sites.google.com/nyu.edu/dhs-f2020)
- [Earlier iterations at wp.nyu.edu](http://wp.nyu.edu/dhs)

## License

This course syllabus and materials are shared under a **Creative Commons CC BY-SA-NC 4.0 International License**.

**Citation:**
> NYU Abu Dhabi. (2022). CDAD-UH 1033EQ: Data and Human Space course syllabus. Abu Dhabi, UAE: David Joseph Wrisley. CC BY-SA-NC 4.0.

## Questions?

For questions about the course or this website, please contact David Wrisley at [djw12@nyu.edu](mailto:djw12@nyu.edu). 
