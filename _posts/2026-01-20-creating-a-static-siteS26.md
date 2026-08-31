---
title: "Creating a Static Site in GitHub Pages S26"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - lab
  - S26
  - Github Pages
---

## Guidelines for Setting up Github Pages: 

Today in class one of the things we will be doing is to beginning to create your own site at GitHub Pages in which you will do your coursework. Creating such a site will require us to set up GitHub, GitHub Desktop and a text editor, to learn and practice some Markdown and to get comfortable with editing on our own machine and then push slowly our materials to the web. 

Knowing how to create such a "[static site](https://kinsta.com/knowledgebase/what-is-a-static-website/)" is an important skill in minimal and sustainable digital arts and humanities. It is also the place you will author and submit your course materials.  

> This course site is created in GitHub Pages in three ways, using an imported repository, then forking the Minimal Mistakes theme, then from scratch. When you gain more confidence you will be able to change to other themes and customize to your own liking.

## GitHub and GitHub Pages Terminology

Before we begin, here are some new terms you'll encounter when working with GitHub:

| Term | Definition |
|------|------------|
| **Repository (Repo)** | A folder/project containing all your files and their revision history. Can exist locally on your computer and/or remotely on GitHub. |
| **Fork** | Creating a copy of someone else's repository in your own GitHub account. You can modify your fork without affecting the original. |
| **Clone** | Downloading a copy of a repository from GitHub to your local computer so you can work on it offline. |
| **Commit** | Saving a snapshot of your changes with a descriptive message. Think of it as a checkpoint in your project's history. |
| **Push** | Uploading your local commits to the remote repository on GitHub, making your changes visible online. |
| **Fetch** | Downloading changes from the remote repository to your local copy to stay up-to-date. |
| **Versioning** | The practice of tracking and managing changes to files over time. Git stores a complete history of every version of your project, allowing you to revert to previous versions if needed. |
| **Static Site** | A website composed of fixed HTML, CSS, and JavaScript files that don't change unless you edit them directly. Static sites are fast, secure, and require no database or server-side processing. |
| **GitHub Pages** | A free hosting service provided by GitHub that automatically publishes websites directly from a repository. Perfect for static sites, portfolios, and documentation. |
| **Template** | A pre-designed structure and styling for a website that you can customize with your own content. Templates like Minimal Mistakes provide a foundation so you don't start from scratch. |
| **Jekyll** | A static site generator that transforms your Markdown and template files into HTML. GitHub Pages uses Jekyll to automatically build your site. |
| **Markdown** | A simple, human-readable format for writing content that gets converted to HTML. Uses symbols like # for headings, ** for bold, and - for lists. |
| **Build** | The process where Jekyll converts your Markdown files and templates into the final HTML website that visitors see. GitHub Pages builds automatically when you push changes. |


STEP 1:

1.  Make sure you have a [Github account](https://github.com/signup) in which there is not already a repository {yourusername}.github.io.  If you have this one set up already, you have a few options: 
   
- you can delete the repository if you do not want it anymore and start afresh.
- you can create an empty repository named, for example RLAC, and then install the template inside of it.
- you can create a new Github account for the purposes of this course.

These instructions will guide you through the second option. If this is your first time working with GitHub, you don't have to do anything special. 

<img src="/assets/images/creatingacct.png" style="zoom:50%;" />

NB: Your account and your page does not need to reveal your identity in any way. Feel free to consider this account a "burner" account for the purposes of this semester. Once you have gotten your grade, feel free to delete it or to repurpose the Markdown files for another site. If you have already created a GitHub account using your name or something identifiable, feel free to create another now. 

Github may require you to have multifactor authentication (2FA). We will not cover that here. It works somewhat like DUO used at NYU.

1.  Make sure you have downloaded a text editor of your choice. This lab write up will explain with [Visual Studio Code](https://code.visualstudio.com/download). Others (such as Sublime Text) are possible, but not explained here.

2.  Make sure you have downloaded [Github Desktop](https://desktop.github.com/). In the beginning, we will edit in VSCode and save (ie, make our commits to GitHub using GitHub Desktop), but you will learn that you can also commit directly from VSCode. If the class feels comfortable with that second step, we will transition to it later. If you already know how, don't worry about GitHub Desktop. 
    
STEP 2: 

Importing a repository, or “Forking a repo."
  
Detailed general instructions for forking can be found [here](https://liamodwyer.github.io/github-pages/5-templates.html)

1. Once you have completed 1 and 2 of Step 1, you can proceed with making a duplicate of the template we will be using. We do this by navigating to the main page of an existing GitHub page of minimal-mistakes and will be using their starter template: https://github.com/mmistakes/mm-github-pages-starter

2. With your GitHub account open, navigate to this page, above the file list, click `Use This Template` (If you do not see it, you may have to go to Settings to click it on). Select `create a new repository`. This will take what is at `minimal-mistakes` and bring it over into your account. Duplicate. Copy. Move over to your GitHub account. This is all forking. 

3. On the page `create a new repository` you need to give the repository a name. You should see under general your username. Next to it you can choose a repository name (for example, `rlacs26`). Give it a description Make sure you set the repository to public and then click on the green button `create repository`.

4. Once the repository has been created you need to activate the “build and deploy” function for that page. Go to Settings > Pages and select the `master` branch and save. You can tell that something is working in the repository you just create when you go back and you see the brown dot. A green check mark means the process is done.

> Note that the repo we have forked is a simplified version of `minimal-mistakes.` If you want to tap into all the options of the full version, you will have to download the full theme and do more work!

We will use the starter website (and customize it) for our work in CDAD-UH 1024Q, including the creation of both pages and posts.

STEP 3:

Connecting the cloud-based Github to your own machine.

1.   Cloning this repository with Github Desktop

Open GitHub Desktop and log into it with your credentials from your GitHub account. Setting > Accounts. 

In Github Desktop make sure you are in the current repository {username}.github.io. Then, go to File > Clone Repository or with the abovementioned repository, click on the `add` button and pull down for `clone repository.`

It may come up automatically, alternatively you can select URL, paste that URL into the repository URL blank and click clone. 

<img src="/assets/images/clonerepo.png" style="zoom:50%;" />

When done, you should be able to see it in the current repository tab at left in Github Desktop. 

2.  Editing the repository on your own machine. 

Now that you have a copy of the repository on your laptop you can edit it there (even offline) and then when you are ready, "push" the changes to the web. 

When you edit and save (and sometime enter a commit message), you will see a blue button to transfer these changes to the web. 

<img src="/assets/images/pushing.png" style="zoom:50%;" />

> NB: You can do some editing in the GitHub web interface itself, but I recommend editing in Github Desktop with your text editor, and certainly not mixing the web-based interface and the text editor, since you end up with a versioning nightmare. If you do make a change in the GitHub web interface, make sure that you fetch the origin.

Let's make some changes in the Sublime Text and push them. 

<img src="/assets/images/pushing.png" style="zoom:50%;" />

1. Use the button in Github Desktop to open in external editor (choosing Visual Studio Code), we can now move on to editing any of the pages. 

Let’s make some changes in VSCode and push them.

> Remember that every time you push to the web, the compiler works to make your page’s updates. Be patient and look for the green arrow which indicates that your site has been rebuilt with the changes you made. If you see a brown dot next to the last commit message in the repository holding the site, the compiler has not finished. Go have some tea or a quick walk–it will be done soon.

The areas in the forked repository of the `minimal-mistakes` template we will want to look at next include: 

- `navigation.yml`
- `config.yml`
- /assets/images/

Enjoy!


Follow up posts:

- Committing directly in VSCode – coming soon
- Connecting your VSCode to CoPilot and Customizing your GitHub page -- coming soon




