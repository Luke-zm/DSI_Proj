# Nintendo vs PlayStation
---

Content
1. [Introduction](#Introduction)
2. [Problem Statement](#Problem-Statement)
3. [Data Gathering](#Data-Gathering)
4. [Data EDA](#Data-EDA)
5. [Modelling](#Modelling)

---
## Introduction

From the title of this project, it should be obvious that I side with Nintendo.  
Jokes aside, this is a toy project but it may still serve some purpose.  
There may be a need to identify if a comment is posted on Twitter by Nintendo or PlayStation in several scenarios.  

1. Research on gaming industry: If someone wants to analyze how different companies are perceived by consumers, identifying which comments come from Nintendo or PlayStation can be useful.    
2. Marketing campaigns: Nintendo or PlayStation may want to monitor Twitter to gauge how successful their marketing campaigns are, and whether they are resonating with their target audience.
3. Product development: Companies may want to analyze the feedback on Twitter to identify what features and products their customers are asking for, and adjust their product development accordingly.

---
## Problem Statement

For project 3, your goal is two-fold:
1. You'll collect posts from two subreddits of your choosing. You can use [Pushshift's](https://github.com/pushshift/api) API or any other low-code platform for the same. 
Alternatively, you can web-scrape or use any low-code platform, eg., parse-hub, collect data from twitter, wiki, facebook, insta etc.
1. You'll then use NLP to train a classifier on which subreddit (or other sub-sections based on the site you choose to scrape your data from) a given post came from. This is a binary classification problem.


### Requirements

- Gather and prepare your data using the `requests` library.
- **Create and compare two models**. One of these must be a Naive Bayes classifier, however the other can be a classifier of your choosing: logistic regression, KNN, SVM, etc.
- A Jupyter Notebook with your analysis for a peer audience of data scientists.
- An executive summary of your results.
- A short presentation outlining your process and findings for a semi-technical audience.

**Pro Tip:** You can find a good example executive summary [here](https://www.proposify.biz/blog/executive-summary).

---

### Necessary Deliverables / Submission

- Code must be in at least one clearly commented Jupyter Notebook.
- A readme/executive summary in markdown.
- You must submit your slide deck as a PDF.
- Materials must be submitted by the specified date given by the Instructional Team through your GitHub account repo shared with the Instructional Team.

---
