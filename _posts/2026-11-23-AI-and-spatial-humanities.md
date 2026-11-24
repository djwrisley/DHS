---
title: "Assignment 4 Prompt Cartography and Spatial Humanities"
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

The On Prompt Cartography and Spatial Humanities Assignment is an assignment in one step. It builds upon the work we have done in class all semester, but particularly since 12 Nov. You will work with GeoNames data as in A1, to design a different kind of map using the LLM(s) of your choice. This exercise focuses on the contextual knowledge that informs prompting, so doing background research will be an important first step. 

- **Format**: Individual or pairs (maximum 2 people)
- **Length**: Approximately 1500 words (about an 8-minute read).
- **Due Date**: Monday, 14 December 2026. 
- **Medium**: a post in Github pages, with screenshots and interactive maps 
- **Credit**: If you have only completed two assignments so far, this exercise will count as the third required one, that is, 30%. If you have completed three assignments, this assignment can replace one of the others if the grade is higher, or count for up to 5 points of extra credit on the semester's grade. 

If you work in pairs, it can be written together, but should be posted on each of the team member's course site. 

**Background** 

In Assignment 1, we created an interactive visualization in three layers of three different features in GeoNames data for the country of your choice. 

In this optional Assignment, number 4, you will focus on identifying linguistic or toponymic patterns in placenames and visualizing them using data from a Geonames dump. 

Below is a draft map of India in which places containing specific patterns are used. It is based on a map I created during a spatial humanities seminar at IIT Delhi in January 2026. It communicates how certain placenames contain features pointing to language, religion and culture. 

<div style="width:100%; height:70vh;">
  <iframe
    src="{{ '/assets/maps/india_toponymic_suffixes.html' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy">
  </iframe>
</div>

Or there is the following draft map for the UAE shows how certain places use Gulf and Bedouin topographic categories, using words like "Tawi", "Sayh", and "Khor". It has a slider separating the water lexicon and landform lexicon. 

<div style="width:100%; height:70vh;">
  <iframe
    src="{{ '/assets/maps/uae_topographic_lexicon_swipe_map.html' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy">
  </iframe>
</div>

Both maps are designed to be seen on a laptop screen, and have important flaws to them. Using the github URL ask your favorite LLM how they might not communicate optimally (suggestion: responsive design, visual clarity, searchability, popup information, UI, etc.). Ask a second LLM and compare the advice.

**Main Elements of the Assignment**

In this assignment, you will work with the country data dump from GeoNames of your choice. It can be another one than what you worked on in A1. You will create a map via prompts instead of using scripts in R, focusing on data enrichment and map design.

The assignment has six main elements: (1) doing the pre-exercise readings and research, (2) choosing a country, (3) exploring the coverage of the data in that country, (4) using directive prompts to create a map in leaflet, (5) tweaking your prompt for clarity and communication until you are satisfied with your map (6) discussion of both process and product using any of the pre-readings or other readings from the course.

**Step 1**: Choose your country. Do not use more than one country. 

**Step 2**: Pre-exercise readings

- Find and skim a few articles related to toponymy or place names in your country of choice. What kinds of characteristics of place names do you find interesting? Do they come from different languages? different historical moments in time?
- Explore some resources about the leaflet package. What kinds of elements of map design do you find interesting (marker clustering, heatmaps, slider maps, hexbin aggregation)? Which ones might help the visual display of your data?
- Read chs 1-2 of _Prompt Cartography_, "From Web Cartographer to Prompt Cartography Director" and "Learning to Speak via Prompt". 
- Reviewing the advice of Ghandi's "Agentic Coding for GIS".

**Step 3**: Exploring the data. 

For this you could use the first notebook, or kepler.gl. This exploration is to designed to give you an idea of the full extent of the data. You may even use the LLM to explore the data, but your prior research contextualization will be important for directing such brainstorming and analysis.

**Step 4**: Prompting

Muehlenhaus writes that prompting literacy is "about learning how to express design intent precisely enough that it can be delegated without being distorted" (25). So before you begin "blind" prompting as in the cases of India and the UAE above, you have to think about all the pieces of the design of your maps you want to implement. 

Based on your desired linguistic features in the placenames, you will include in your prompt to filter these and represent the different categories in whatever visual way makes the most sense to you. Here leaning into elements of the map design you researched will be important. 

**Step 5**: Reprompting & Tweaking

It is unlikely that you will get it right the very first time. In your writeup of the assignment, use code blocks to share the step-wise prompting that you used, along with explanations of why you changed them the way you did. 

**Step 6**: Reflection

The last step is reflecting on the entire process, what you were able to create from your source, how it might be interesting to someone studying in the humanities as well as the challenges of the process. 

## Guiding questions for this assignment:

You do not need to answer all of these questions; instead, use them to think through the assignment. 

- How well do you know this country? 
- When you mapped the data, did you see any interesting or surprising patterns? Were there areas of concentration of points? Did mapping lead to any visible clusters? 
- What kinds of linguistic and toponymic features did you learn about typical of this place?
- How did any suggestions about relevant features in the dataset given by the LLM match (or not match) your research?
- How much of your work do you feel  you outsourced to a machine?
- What kind of human judgment remains in an assignment such as this one?  
- How did you create prompt(s) for ChatGPT, Gemini, Mistral or other tool to automate the creation and revision of maps? What kind of "engineering" did you have to do to get better results with the prompts?
- Did diagnosing issues in the India or UAE maps help you understand issues in yours? If so, how?
- Do you agree with Muehlenhaus that anticipating the audience for a given map is a key design principle? Why? 
- Can you think of any specific disadvantages of using this "prompt cartographic" method?
- Based on the idea of the "[Turing test](https://en.wikipedia.org/wiki/Turing_test)," a test of how indistinguable human and machine performance capacity can be, did the LLM as cartographer pass this test? or was too much human input required to give it a pass?
- How much (or how little) freedom did prompting give you compared to the RMarkdown notebooks we used earlier in the course?
- How does the way you filtered the data to reveal some of its features affect how it might be understood (you could refer back to any of the readings, perhaps Kitchin and Lauriault)? 
