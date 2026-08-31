---
title: "Customizing your Static Site in GitHub Pages S25"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - lab
  - S25
  - Github Pages
  - markdown
  - sustainability
---

## Customizing your Github Pages site: 


> Knowing how to create and customize such a "[static site](https://kinsta.com/knowledgebase/what-is-a-static-website/)" is an important skill in minimal and sustainable digital arts and humanities. The site is free, maintenance is minimal and it can also sit alongside examples of code or data that you have created. Curating a tidy, clear site creates a web presence for yourself. 

This post follows the post "[Creating A Static Site in Github Pages]()" and it explains some of the basic manipulations you will want to make in order to turn the generic template into your course site for Intro to DAAH. In it, we look at how to make some basic structural changes to the site. You want to be careful not to change too much of the basic architecture of the templates, as things can also break. 

## Basics

1.  Make sure you have a basic `minimal-mistakes` template installed and that you are able to use Github Desktop to edit it. 

2.  You do not have to delete anything that comes with the `minimal-mistakes`starter template that we installed. In particular, the `_posts` folder has some different templates which demonstrate possible layouts that could be interesting. You can leave them, since only what you specify will actually show up on your site.  

## 


you can remove something from the list of tabs in the navigation.yml list and it can be in your repository but won't show 

2.  A Markdown cheatsheet can be found [here](https://www.markdownguide.org/cheat-sheet/).

3.  

4.  

5.   

You can play around with making subtle changes to your site, but be careful not to change too much of the basic architecture of the templates, as things can break. 

6. 



So here are a few possibilities for gentle customization of Minimal Mistakes: 
-- check out lines 16-23 in the `_config.yml file (specifically for line 22 you can check out the Minimal Mistakes documentation for different colors). 
-- take any of the posts in the template download, duplicate the file in the _posts folder and change the date (paying attention to the exactly formatting of the title). Put in some placeholder content and let the site render. Do you get a new post? 
-- rewrite your 404 message. Try to figure out how to add a custom photo. Hint: look at line 50 of the [tutorial](https://daahnyuad.github.io/blog/creating-a-static-siteS24/). You can use this tutorial to redo the whole creating a static site process from scratch if you want  
-- check out a markdown cheatsheet and see if you can learn how to make an unnumbered list or a footnote or an embedded link or (advanced!) a new tab rather than a redirect. There is one such cheatsheet linked to the syllabus for yesterday's class. Hint: often inserting some html will do the trick
 
Here is my last hint in case you would like to structure your Github site so that you can plug in the work over the semester. 

The assessment page lists the following assignments:
https://daahnyuad.github.io/assessment/

--a digital literacy narrative (needs a page all by itself)
--three assignments (requires three posts) 
--final presentation (needs a page all by itself) 

So, I would create an about page, two blank pages for the DLN and FP, and  three blank assignments (to the roll of posts).  Then, I would figure out how to make the navigation.yml file create tabs that link to all of those. 

That is already a lot--and it not necessary to complete for tomorrow--but since some people asked I am sharing it now.  Remember that you can check out how I did it in the course site and copy that.  If you find a better way to do something, you can let us know (or even create a How To page that guides any future reader of your site how to replicate the work for themselves).


## Being more sustainable with your Github site: 

> Remember that every time you push to the web, the compiler works to make your page's updates.  As mentioned in the previous document, you have to be patient and look for the green arrow which indicates that your site has been rebuilt with the changes you made. If you see a brown dot next to the last commit message in the repository holding the site, the compiler has not finished. Go have some tea or a quick walk.

If you would like to be more sustainable about your use of computing resources, you can test your markdown in a live viewer such as this [one](https://markdownlivepreview.com/) before sending it to the compiler. This way you spend time offline testing the markdown to see that it displays as you like before compiling the site.



## Some general stuff about your Github Site: 

Your account and your page does not need to reveal your identity in any way. Feel free to consider this account a "burner" account for the purposes of this semester. Once you have received your grade at the end of the semester, feel free to delete it or remove the Markdown files or repurpose them for another site. Note that unless you fully delete the Github site there may be a trace of your work, making the 4th option the one to chose if you want to wipe the slate clean. 

At some point in the near future, Github will require you to have multifactor authentication (2FA). We will not cover that here, but you can refer to the [docs](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication) about it. Two factor authentication is a good security strategy.  



Enjoy the space you have created for yourself!