---
title: "Assignment 1: Building a Map of Chosen Features for the Country of Your Choice F26"
excerpt: "Use a computational notebook to filter country data to show features of your choice"
last_modified_at: 2026-02-12T12:00:00-05:00
tags:
  - Assignments
  - Markdown
  - Interactive Map
  - R
  - GeoNames
  - F26
---

## DRAFT OF ASSIGNMENT 1 

## Overview

Assignment 1 invites you to download some data about a country you know something about and to filter that dataset such that you show some of its features of interest to you. This assignment builds on concepts and tools we've discussed in class and a "computational notebook" in posit.cloud. Not only will you create a map of the features, place it into your own site you created for the course, but you will be also asked to comment on the visualization you create using the readings from the course.

- **Type:** Individual  
- **Length:** Approximately 1500 words (about an 8-minute read), plus maps
- **Format:** This assignment will be completed in Markdown and posted on your individual Github pages site, including the interactive map.   
- **Due Date:** 28 September 2026, 11:59pm

## Three Main Elements

This assignment has five core components:

1. **Downloading or querying data:** You will acquire data from an open site on the web (mainly GeoNames) about a place in the world of interest to you. 
2. **Choosing the features of interest to you:**  You will use the country download from the GeoNames webservice to begin this assignment.
3. **Filtering for these Features:** Use a combination of Rmd Notebooks to conduct exploratory data analysis (EDA) with your part of the world. You will compare up to up to 5 feature classes from the GeoNames ontology. 
4. **Using Pre-written Code to Generate Maps in Layers** Using the notebook you will generate a map in layers. You will push it to Github and embed it in your assignment. 
5. **Written Synthesis:** In your essay you will assess what data is available in GeoNames about your country of choice. Assemble your evidence, analysis, and visuals in a web-published essay in the form of a post that tells a coherent story about your findings. Make sure to relate what you have found to the Do Maps Lie video and the reading by Kitchin & Lauriault on Critical Data Studies (in Drive).

## More detailed instructions

### Step 1: **Downloading or querying data:**

Check out [GeoNames](https://www.geonames.org/) for your country manually to see what kinds of places show up and what don't. Go to the [GeoNames Webservice](https://download.geonames.org/export/dump/) and download the data for the country of your choice (use only one). 

## Step 2: **Choosing the features of interest to you:**

You need to pick between 3-5 feature [codes]((https://www.geonames.org/export/codes.html) to show for your geospatial visualization. It will be good to justify your choice (frequency, personal or research interests, etc). 

## Step 3: **Filtering for these Features:**

You will insert the feature codes into the notebook and generate the map. You can customize the colors of your points on the map.  

## Step 4: **Using Pre-written Code to Generate Maps in Layers**

The notebook will create it as an html file. You will insert this html file into a new repository you create in Github, as shown in class. The notebook will default to creating each of the feature codes in a separate clickable layer. 

## Step 5: **Written Synthesis:**

## Guiding Questions

As you write, consider (but don't feel obligated to answer) all of these questions:

- **Background & Expectations:** What did you know about your location before beginning analysis? Did you have any hypothesis about you have about the kinds of features described in the dataset? How many rows of data do you have? What are the major periods for its update? What are the main feature codes available? Why did you choose the ones you did?

- **Computational Insights:**  What interesting patterns emerged? Which parts of the country were best represented? Which parts least? Can you relate these questions of coverage to Kitchin and Lauriault? Were there unexpected findings or surprises? 

- **Methodological Questions:**  How might you say that GeoNames is a data assemblage? If you go to the [Team tab](https://www.geonames.org/team.html) does the country you chose have an ambassador? What can you tell about the provenance of the data in GeoNames for your country--try to do some web research? How difficult was it to generate the webmap using the notebook? How difficult was it to put it on Github and to embed it in your page?

- **Transferability:** How might you use this workflow in other courses, disciplines, or projects like a capstone?

## Assessment

Your work will be assessed according to the following criteria located [here]():

## Tips for Success

**Use of AI for this assignment:** You should not use AI to analyze the GeoNames dataset for this assignment or to create the map. You should pick geographical and features of interest to you. You can use AI tools to clarify language or to brainstorm. You can also use AI to tweak the code if you want to be adventurous--although this is not a required part of the assignment. Do not use it to do web research on the data provenance question above. Please include an generative AI statement at the end of your assignment explaining how you use it.  

**Writing:** You can use tools like [Markdown Live Preview](https://markdownlivepreview.com/) to view what your page will look like or you can use the preview function in Visual Studio Code itself. The [Hemingway App](https://hemingwayapp.com/) is useful to refine your prose for clarity and legibility. 

**Visualization:** Your assignment should have the clickable layered map visible in it. You can also make screenships to show interesting observations. Make your screenshots speak. Use clear captions that explain what readers are seeing and why it matters to your argument. Your visualizations should support and enhance your analysis, not merely decorate it or fill space. Feel free to annotate on top of the visuals (like putting arrows or circles).

**Publishing:** Post your assignment to your Github pages site as a post so instructors and classmates can read and engage with your work It is fine to publish your assignment iteratively, but when you finish the final version of your assignment, write at the bottom of it "READY FOR GRADING". 

Good luck with your analysis!


