---
title: "Assignment 2 Working with a Corpus S23"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Assignments
  - Corpora
  - chatGPT
  - S23
---

Note that this is a previous semester's assignment.

## Guidelines for the Assignment:  

The Corpus Assignment, otherwise known as Assignment 2, will be completed in one step. It builds on work we did in the textual portion of the class, particularly with Voyant Tools and R Markdown files in Posit Cloud. This assignment can be done alone or in pairs.

This exercise has three main elements: (1) choosing a corpus of three texts or three sets of texts you would like to work with and (2) using some digital textual analysis tools to see what kind of exploratory data analysis (EDA) you can do using that corpus, (3) assembling the evidence in a piece of web-facing written work along with visuals. 

**Step 1**: You will need to pick your corpus. Here are some suggestions for the corpus. 

- A. Three different books by the same author taken from Project Gutenberg. 
- B. Three sets of books by three different authors (but somehow related, belonging to the same political orientation or the same literary movement)
- C. Three sets of books by the same prolific author from different moments of their career, or in different genres. 
- D. Three different sets of articles from a single class or multiple classes in your major. 

The texts can be short stories or articles, but not less than 2000 words. Do not use the Little Cousin Series. The more you know about the texts, the more meaningful the "distant reading" will be. 

If you are using the R Markdown notebook in posit.cloud, you can also build your own corpus from files in Project Gutenberg by creating a list of ID numbers like this: 

> gutenbergbook <- gutenberg_download(c(textID1, textID2, textID3, etc), mirror = "http://mirrors.xmission.com/gutenberg/")

Alternatively, you can source your text files from anywhere else, but if you make a custom corpus, please consult with the instructor before beginning.

**Step 2**: You should do some general research about the authors, the text, the contents. You will want to justify the selection of texts in your assignment. You might even browse them briefly to know what they include. You should do this so that you are not studying the corpus without a general idea of its contents. 

**Step 3**: To do your analysis, you must use the R notebooks and you can combine them with Voyant Tools, Antconc or the wordclous notebook in R to explore the texts. Remember that each method works with its own constraints. You are free to use whatever combination of forms of analysis you like. 

**Step 4**: Build a set of screenshots from your exploratory analysis. Please be sure to include at least three (3). 

**Step 5**: Find two (2) of the readings/resources from this term and include references to them in your essay. Feel free to refer to external resources (including the GPT response below).

Guiding Questions (you do not need to answer all these questions):

- What did you know about the subject before you began your analysis? 
- What does computer-assisted analysis allow you to see that you wouldn't have seen in a linear read? Would a linear read have been possible in the time frame allotted? 
- Was the format in which the corpus reached you sufficient for your purposes? What are some of the shortcomings of the texts? 
- What is a trend you can identify in the materials? What are you able to learn by looking at the text the way you did? 
- Were there any surprises in your exploration? 
- How well would this assignment work for a language other than English?


You assignment can be 1250-1500 words, or about a 6-8 minute read. Please publish it to your course site with a visible tab. 

**Due date: 28 Oct**.


-----

chatGPT4 Prompt with Mar 14 version: 

> What kinds of computation can be used to explore textual corpora? What is exploratory data analysis (EDA) and how can it help us understand texts better?

Response from chatGPT:

There are several computational techniques that can be used to explore textual corpora, including:

Text Preprocessing: This involves cleaning and transforming raw text data into a more usable format. Text preprocessing techniques include tokenization, stopword removal, stemming, and lemmatization.

Text Mining: This refers to the process of extracting useful information and patterns from textual data. Techniques used in text mining include topic modeling, sentiment analysis, and named entity recognition.

Natural Language Processing (NLP): This involves using algorithms and statistical models to analyze and understand human language. NLP techniques include part-of-speech tagging, dependency parsing, and machine translation.

Exploratory data analysis (EDA) is a statistical approach used to analyze and summarize datasets. In the context of textual corpora, EDA can help us understand the characteristics of the data, identify patterns and trends, and generate hypotheses for further analysis. Some common techniques used in EDA of textual data include:

Word frequency analysis: This involves identifying the most frequently occurring words in a corpus, which can provide insight into the main topics and themes.

Word clouds: A visual representation of word frequency in which the size of each word corresponds to its frequency.

Topic modeling: This technique involves identifying the underlying topics and themes in a corpus using statistical methods.

Sentiment analysis: This involves analyzing the sentiment or emotion expressed in a text, which can provide insight into the attitudes and opinions of the author.

Overall, exploratory data analysis can help us better understand textual data by providing a comprehensive overview of its characteristics and identifying patterns and trends that may be of interest for further analysis.


chatGPT 4 Prompt with Mar 14 version:

> What is Handwritten Text Recognition (HTR)? Why would you use it? How do they make it easy for a researcher to explore a collection? Is HTR available for all  world languages? What might the challenges for non-Western handwritten archives? 

Handwritten Text Recognition (HTR) is a technology that allows machines to recognize and convert handwritten text into machine-readable digital text. It involves the use of algorithms and machine learning techniques to analyze handwritten documents and convert them into searchable digital text.

HTR is used in various fields, including digitization of historical documents, automated transcription of handwritten notes, and automated data entry from forms. It is also useful for researchers who work with handwritten archives, as it enables them to easily search and analyze handwritten documents.

To make it easy for researchers to explore a collection, HTR can be integrated with digital archives, providing users with the ability to search and browse through digitized collections. This integration enables users to easily locate specific handwritten documents and extract relevant information from them.

HTR technology is available for many languages, including English, French, Spanish, German, and Chinese. However, some languages, especially those with complex scripts or cursive handwriting, may present challenges for HTR systems. In some cases, it may be necessary to develop specialized HTR models for specific languages or handwriting styles.

One of the main challenges for non-Western handwritten archives is the lack of training data. HTR models require large amounts of data to accurately recognize handwriting, and this data may not be readily available for non-Western languages or scripts. Additionally, non-Western scripts may have unique characteristics that make them more difficult to recognize using HTR technology. This can make it challenging to develop accurate HTR models for non-Western archives.