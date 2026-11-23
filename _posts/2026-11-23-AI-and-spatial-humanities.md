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

The On (geo)AI and Spatial Humanities Assignment is an assignment in one step. It builds upon the work we have done in class all semester, but particularly since 12 Nov. You will replicate one of the assignments (A1, A2 or A3), extending it using the LLM(s) of your choice. This exercise focuses on contextual knowledge that informs prompting, so doing background research will be an important first step. 

- **Format**: Individual or pairs (maximum 2 people)
- **Length**: Approximately 1500 words (about an 8-minute read).
- **Due Date**: Monday, 14 December 2026. 
- **Medium**: a post in Github pages, with screenshots and interactive maps 
- **Credit**: If you have only completed two assignments so far, this exercise will count as the third required one, that is, 30%. If you have completed three assignments, this assignment can replace one of the others if the grade is higher, or count for up to 5 points of extra credit on the semester's grade. 

If you work in pairs, it can be written together, but should be posted on each of the team member's course site. 

**Background** 

In Assignment 1, we created an interactive visualization in three layers of three different features in GeoNames data for the country of your choice. 

In this optional Assignment, number 4, you will focus on identifying linguistic or toponymic patterns in placenames in maps using data from a Geonames dump. 

Below is a draft map of India in which places containing specific patterns are used. It is based on a map I created during a spatial humanities seminar at IIT Delhi in January 2026.  

<div style="width:100%; height:70vh;">
  <iframe
    src="{{ '/assets/maps/india_toponymic_suffixes.html' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy">
  </iframe>
</div>

Or, the following draft map for the UAE shows how certain places use Gulf and Bedouin topographic categories, using words like "Tawi", "Sayh", and "Khor". It has a slider separating the water lexicon and landform lexicon. 

<div style="width:100%; height:70vh;">
  <iframe
    src="{{ '/assets/maps/uae_topographic_lexicon_swipe_map.html' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy">
  </iframe>
</div>

Both maps are designed to be seen on a laptop screen, and have important flaws to them. Ask you favorite LLM how they might not communicate optimally (suggestion: responsive design, visual clarity, searchability, popup information, UI, etc.). Ask a second LLM and compare the advice.

**Main Elements of the Assignment**

In this assignment, you will work with the country data dump from GeoNames of your choice. It can be another one than what you worked on in A1. You will create a map via prompts instead of using scripts in R, focusing on data enrichment and map design.

The assignment has six main elements: (1) doing the pre-exercise readings and research, (2) choosing a country, (3) exploring the coverage of the data in that country, (4) using prompts to create a map in leaflet, (5) tweaking your prompt for clarity and communication (6) discussion of both process and product using any of the pre-readings or other readings from the course.

**Step 1 Pre-exercise readings**:

- Find and skim a few articles related to toponymy or place names in the country of choice. What kinds of characteristics of place names do you find interesting? 
- Explore some resources about the leaflet package. What kinds of elements of map design do you find interesting? 
- Read ch 2 of _Prompt Cartography_, "Learning to Speak via Prompt". 
- Reviewing the advice of Ghandi's "Agentic Coding for GIS"

**Step 2**: Choose your country. Do not use more than one country. I would suggest working with a country that does not have a very large dataset, such as Iran. This will make the process slow and potentially create issues for your LLM limits.  

**Step 3**: Exploring the data. 

**Step 4**: Prompting

**Step 5**: Reprompting & Tweaking

**Step 6**:  Reflection

The last step is reflecting on the entire process, what you were able to create from your source, how it might be interesting to someone studying in the humanities as well as the challenges of the process. 

# Guiding questions for this assignment:

- How well do you know this country? 
- What kinds of linguistic and toponymic features did you learn about typical of this place?
- Why did you choose specific features?
- Can we say that we outsourced our analysis to a machine? If so, how?   
- What kind of human judgment remains in an assignment such as this one?  
- How did you create prompt(s) for ChatGPT, Gemini, Mistral or other tool to automate the creation and revision of maps? What kind of "engineering" did you have to do to get better results with the prompts?
- How did diagnosing issues in the India or UAE maps help you understand issues in yours?
- Can you think of any specific disadvantages of using this "prompt cartographic" method?
- How does the way you created data shape how it might be used (you could refer back to any of the readings, perhaps Kitchin and Lauriault)? 
- When you mapped the data, did you see any interesting patterns? Were there areas of concentration of points? Did mapping lead to any visible clusters?
- 
-   

Your assignment should be about 1500 words long, with relevant several images, embedded links and discussion of your initial and revised prompts.
