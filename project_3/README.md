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

Now, imagine that I am working for a gaming news platform.  
My platform is rolling out a new service, pushing interesting contents from a bank of mixed up posts to user, based on ther user's preference.  
Before I push the post to the Nintendo/ PlayStation fans, I will first need to identify where these posts come from.  
Somehow the contents the game news platform generates is very similar to reddit, so I decided to gather some reddit posts and make a classifier which can identify is the post is from r/nintendo or r/playstation.  

For this project, my goal is two-fold:  
1. I will collect posts from two subreddits. `r/nintendo` and `r/playstation`, using API.  
2. I will then use NLP to train a classifier on which subreddit a given post came from. This is a binary classification problem.  

---
## Data Gathering

The data from `r/nintendo` and `r/playstation` will be gathered using `praw`, [The Python Reddit API Wrapper](https://praw.readthedocs.io/en/stable/).  
These data will then be saved into 2 different csv files under the `data` folder.  
They are:  
[nintendo_posts.csv](./data/nintendo_posts.csv)  
[playstation_posts.csv](./data/playstation_posts.csv)

### Data dictionary
|no|feature|description|
|-|-|-|
|1|id|the unique id to each reddit post, used to make only 1 post is scrapped|
|2|title|title of the post scrapped|
|3|post_content|if the post is word post, then post content exit|

---


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
