---
title: "Assignment 4 On (geo)AI and Spatial Humanities"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Assignments
  - metadata
  - LLMs
  - F26 
  - spatial
  - geoAI
---

# Guidelines for the Assignment (Draft): 

## The Assignment

The On (geo)AI and Spatial Humanities Assignment is an assignment in one step. It builds upon the work we have done in class all semester, but particularly since 12 Nov. You will replicate one of the assignments (A1, A2 or A3), extending it using the LLM(s) of your choice. 

- **Format**: Individual or pairs (maximum 2 people)
- **Length**: Approximately 1500 words (about an 8-minute read).
- **Due Date**: Monday, 14 December 2026. 
- **Medium**: a post in Github pages, with screenshots and an interactive map 
- **Credit**: If you have only completed two assignments so far, this exercise will count as the third required one, that is, 30%. If you have completed three assignments, this assignment can replace one of the others if the grade is higher, or count for up to 5 points of extra credit on the semester's grade. 

If you work in pairs, it can be written together, but should be posted on each of the team member's course site. 

**Background** 

In Assignment 1, we created an interactive visualization in three layers of three different features in GeoNames data for the country of your choice. 

In this optional Assignment, number 4, you will focus on identifying linguistic or toponymic patterns in placenames in maps. 

Below is a map of India in which places with the expression is used. We created it in a spatial humanities seminar at IIT Delhi in January 2026.  

<div style="width:100%; height:70vh;">
  <iframe
    src="{{ '/assets/maps/india_toponymic_suffixes.html' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy">
  </iframe>
</div>


You will create a similar map using three clickable layers with three different linguistic traits found in placenames in a GeoNames data dump. For example, "spring," "farm," and "dale" in the UK. 

Or this example for the UAE, using " ", " ", and " ".

**Pre-exercise readings**

Toponymy 

**Main Elements**

In this assignment, you will recreate your choice of one of the assignments, focusing on changing map design.  

 has seven main elements: (1) read two guiding articles (2) choosing a source, (3) choosing a portion of the source material and identifying the spatial elements of this humanities source material (4) modeling a spatial dataset based on those elements as they are represented in the sources, (5) prompting the LLM of your choice to extract and organize the data according to the desired structured output, assessing the output and perhaps re-prompting AND/OR correcting the data manually (6) designing an interactive map and visualizing the data, and finally (7) discussion of both process and product using some readings data modeling in the humanities and LLM approaches.


**Step 1**: Read two articles 

[Stewart Spencer Dean and Sanskriti Sinha. 2025. "Retrieving information from unstructured historical sources using large language models" Computational Humanities Research, 1:e17](https://doi.org/10.1017/chr.2025.10019)

[Ian Gregory et al. "Modeling Space in Historical Texts" The Shape of Data. ch 5.](https://www.taylorfrancis.com/books/edit/10.4324/9781315552941/shape-data-digital-humanities-julia-flanders-fotis-jannidis) 

Optional: You can also read 

**Step 2**: Choose your source and choose a portion of that source to work with. Do not use more than one source. You should aim to create a dataset which has about 300+ data points total (if working alone 200). This may mean that you put together two parts of the same directory (embassies and business offices, for example, as in the case of the Cairo directory) or a portion of one directory (only the letter A).  

**Step 3**: Modeling the data. You will need to choose what data you are going to extract from the source and imagine a structured data table into which it is set. Is there a key in the source that can help you understand some of its abbreviations or the structure of its data? One way of doing this is to ask the vision-capable LLM of your choice what it understands from a snippet of your source and to create a `parsing prompt` for you. 

It could be helpful to review some of the principles from an article we read earlier this term: [Data Organization in Spreadsheets](https://doi.org/10.1080/00031305.2017.1375989).

**Step 4**: you will semi-automate the process of data collection by using the screenshots of the pdf along with your parsing prompt. (NB: you will need to supervise this process looking at the outlook and adjusting the prompt if necessary). Do not upload the entire pdf to an LLM. Instead extract individual pages, or use screenshots of portions of pages containing the information as we did in class. Having uploading the relevant pages, prompt the LLM to extract the data for you as we did in class on 12 and 17 November. This portion of the exercise may require some trial and error. For Step 4, you can use any tools that you feel comfortable with: chatGPT, Gemini, Mistral, Claude, etc. None of the available tools will be perfect for historical materials. You can even compare the performance of the different AI tools and will give insight into the iterative way that you went about creating the data collaboratively. You could also use the same AI company, but different versions.   

One of my former students, R.K., who works for an AI company in Canada said to me "I find the new models are the best and then they tend to deteriorate or hallucinate more often as they are trained on new noisy data or the engineers stop paying attention to them while they focus on newer versions." Feel free to comment on this point if it is relevant. In other words, you can use the age of model as a point of comparison. 

Part of the exercise has to do with how you prompt and refine your prompts. Keep track of what you prompted and include them in your discussion and analysis below. Please provide the best prompts you use to extract the data. A callout (with the > sign in markdown) or code block would be an excellent way to do this. 

There will be some cleaning that is required to bring your dataset into shape so that it can be visualized. Please comment on what was required, what the model(s) understood and what they did not understand. 

**Step 5**: There are many ways that you can arrive at a final dataset. In particular, it may be interesting to combine some of the elements with bespoke tags (such as professions in a city directory). This possible enriching of the data will be different according to the source you have chosen.  

Finally, you have a few options for geocoding: you can use the script I will provide in a notebook or a plugin for Google Workplace like InstaMaps or Google Apps Script so that you have latitude and longitude columns. 

**Step 6**:  Visualizing the data.  

Use the notebook from Assignment 2 for creating a multilayered map or use kepler to visualize the map with layers.

When you have created an self-contained HTML file, by saving the map, create a folder in your `assets` folder called `maps` and push the html file to it.  Instructions for embedding the map can be found [here](https://daahnyuad.github.io/going-further-static-siteF26/#inserting-an-interactive-map-using-an-iframe).

**Step 7**:

The last step is reflecting on the entire process, what you were able to create from your source, how it might be interesting to someone studying in the humanities as well as the challenges of the process. 

# Guiding questions for this assignment:

- How have we outsourced our analysis?  
- Are there any ethical reasons that this source should not be used? and its derived data made public? (e.g. are the people still alive?)
- What can you find out about the place and time that are represented by the source? 
- What kinds of data does that source provide? Were you surprised by any of the data that was available in printed sources? 
- Why did you choose specific pages? 
- Was the data directly or indirectly communicated? In other words, did you have to assume anything if you created new columns? 
- How did you create prompt for ChatGPT, Gemini, Mistral or other tool to automate thse extraction of the information? What kind of "engineering" did you have to do to get better results with the prompts?
- How good was the automation? What did you have to change in order to clean the data? 
- Can you think of any disadvantages of using this semi-automated method?
- what issues mentioned in the "Data Organization in Sheets" article did you encounter? 
- How does the way you created data shape how it might be used (you could refer back to any of the readings, perhaps Kitchin and Lauriault)? 
- When you mapped the data, did you see any interesting patterns? Were there areas of concentration of points? Did mapping lead to any visible clusters?
- If you were to do this over many more pages then you did for this assignment (say, look at the entire source or multiple sources over time), what kind of results do you think the different scale would give?
- If you were to do this assignment with a source not included here, what would your ideal source be?  


Your assignment should be about 1500 words long, with relevant several images, embedded links. Please place your data table into your assets folder (or other location in the repository where you host your GitHub site) and link to it in your assignment. Use a markdown cheatsheet such as this [one](https://www.markdownguide.org/cheat-sheet) to stylize your post, adding different layout features and embedded links if needed. You can refer to other readings if you want to, but this is not necessary for this assignment. 
