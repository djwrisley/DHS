---
title: "Assignment 1: Working with a Corpus S26"
excerpt: "Apply computational text analysis methods to a corpus of your choice"
last_modified_at: 2026-02-12T12:00:00-05:00
tags:
  - Assignments
  - Corpora
  - Markdown
  - R
  - Voyant Tools
  - S26
---

## Overview

Assignment 1 invites you to apply computational text analysis methods to a corpus of texts you select. This assignment builds on concepts and tools we've discussed in class—particularly exploratory data analysis (EDA) in Voyant Tools and the two notebooks in posit.cloud-and asks you to choose a subset of either the Harry Potter and Harry Potter fan fiction corpus or the Colonial South Asian Corpus and to synthesize your findings in a web-facing written essay with supporting visualizations.

- **Format:** Individual or pairs (maximum 2 people) 
- **Length:** Approximately 1500 words (about an 8-minute read), plus visuals  
- **Due Date:** Sunday, 15 March 2026, 11:59pm

## Three Main Elements

This assignment has three core components:

1. **Corpus Selection:** Choose three or more texts that you'd like to work with. This choice will require a bit of research. 
2. **Exploratory Analysis:** Use a combination of Voyant Tools and the Rmd Notebooks to conduct exploratory data analysis (EDA) with your corpus
3. **Written Synthesis:** Assemble your evidence, analysis, and visuals in a web-published essay in the form of a post that tells a coherent story about your findings. Make sure that one of your Voyant Tools visualization is a live widget embedded in your post. 

## Step 1: Select Your Corpus

You have several options for corpus selection. Choose one approach below, or consult with your instructor if you'd like to create a custom corpus.

Choose five or more texts from either corpus that you'd like to work with. 

- If you choose Harry Potter, choose two or more texts by Rowling and three or more from the fandom.

- If you choose the Colonial South Asian corpus, choose five or more of the texts. 

## Step 2: Research Your Texts

Before you begin analysis, research the texts themselves: Who are the authors? What is the publication context? What are the general themes and contents? You will want to do background research using something like Wikipedia or other reliable web sources. This research may actually inform your choice of corpus. 

By becoming familiar with your texts, you'll be able to:
- Justify your selection meaningfully
- Contextualize your findings rather than studying the corpus in isolation
- Make connections between distant reading insights and close reading knowledge
- Recognize what makes your corpus interesting

_This contextual knowledge is essential for meaningful analysis._

## Step 3: Conduct Your Analysis

You must use **both** of the following methods. 

- **Voyant Tools** (https://voyant-tools.org/): A web-based suite for exploratory text analysis. Provides visualizations like word clouds, trend graphs, and concordances. Works well for smaller corpora (a handful of texts to a dozen or so).

- **RMarkdown notebooks in `posit.cloud`:** Use computational analysis to create word clouds or heatmaps using custom words. 

Other tools are acceptable if they serve your research question. Please justify your use of them.

## Step 4: Build a Collection of Visualizations

Create at least **two (2) screenshots** showing the results of your exploratory analysis from Voyant and **a selection of screenshots** from ggplot in R. These might include:
- Word frequency charts or tables
- Wordcloud visualizations
- Trend graphs showing word usage over time or across texts
- Concordance results
- etc.

Ensure each screenshot well chosen to illustrate a point and that each is clearly labeled and contextualized.

## Step 5: Include an Interactive Visualization

Embed **at least one interactive iframe** from Voyant Tools in your essay. This allows readers to explore the data themselves. You can obtain an iframe by:
1. Running your analysis in Voyant Tools
2. Going to the Export tab
3. Copying the HTML snippet

**Sample iframe:**

```
<iframe style='width: 444px; height: 408px;' src='https://voyant-tools.org/tool/Cirrus/?corpus=8d8c7ce89087801d676ff4f77d5391fc'></iframe>
```

and it looks like this: 

<iframe style='width: 444px; height: 408px;' src='https://voyant-tools.org/tool/Cirrus/?corpus=8d8c7ce89087801d676ff4f77d5391fc'></iframe>

The size is adjustable using the width and height values in the iframe.

## Step 6: Integrate Course Materials

Read the chapter "The Risks of Distant Reading" (pp 143-169) from Ted Underwood's [_Distant Horizons_](https://search.abudhabi.library.nyu.edu/permalink/01NYU_AD/indfm6/alma990074332960107871), available as an e-book. Refer to Underwood's chapter in your assignment where appropriate. 

Reference **at least two (2)** other readings or resources (podcasts, articles) from this course in your essay. You may also draw on external sources as appropriate. Be sure to cite what you use include LLMs. 

## Guiding Questions

As you write, consider (but don't feel obligated to answer) all of these questions:

- **Background & Expectations:** What did you know about your subject before beginning analysis? What hypotheses did you have about the language contained in the text?

- **Computational Insights:** What does computational analysis reveal that a linear read would not? Would reading all texts cover-to-cover have been feasible in your timeline? What interesting patterns emerged?

- **Comparative Insights:** What did Voyant Tools allow you to do that the Rmd Notebooks did not? How was working with the two methods different? similar? 

- **Trends & Surprises:** What trends can you identify across your corpus? Were there unexpected findings? How do your results compare to your initial hypotheses?

- **Methodological Questions:** If you ran your analysis between Voyant and Rmd Notebooks, did you get consistent results? Why or why not? How do different visualization methods represent the data differently? Were there limitations in the tools or approaches you used? What risks are there in reading this way (draw on Underwood)?

- **Scope & Scale:** How limiting (or enabling) was the constraint of comparing five or more texts? What would you analyze differently with more or fewer texts?

- **Transferability:** How might you use this workflow in other courses, disciplines, or projects like a capstone?

## Assessment

Your work will be assessed according to the following criteria located [here](https://djwrisley.github.io/RLAC/rubrics/):

## Tips for Success

**Writing:** Use tools like [Markdown Live Preview](https://markdownlivepreview.com/) and [Hemingway App](https://hemingwayapp.com/) to refine your prose for clarity and legibility. Keep the [F-shape principle](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/) for web writing in mind—readers scan top-to-bottom and left-to-right, so structure your argument visibly.

**Visualization:** Make your screenshots speak. Use clear captions that explain what readers are seeing and why it matters to your argument. Your visualizations should support and enhance your analysis, not merely decorate it or fill space. Feel free to annotate on top of the visuals (like putting arrows or circles).

**Collaboration:** If working in pairs, you may submit a single essay that links to both group members' sites. Include a brief statement describing each person's unique contribution to the work.

**Publishing:** Post your assignment to your course site as a post so instructors and classmates can read and engage with your work.

It is fine to publish your assignment iteratively, but when you finish the final version of your assignment, write at the bottom of it "READY FOR GRADING". 


Good luck with your analysis!


