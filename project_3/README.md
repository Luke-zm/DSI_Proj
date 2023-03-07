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
This is a very special platform!  
It is a centralised gamming forum that is based on reddit.  
For example, I want to post some random thoughts, all I have to do is simply post, and then this post will appear in the correct subreddit.  
Additionally, if I want to look at posts by other users, then all I have to do is to type some key words, then suggested posts based on my topic will appear.  
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

A class function is written for this task.  
It will be able to automate the collection of data.  
It can also save and extend the current csv file should new data under the same topic appear.  
A simple way to obtain the possible attribute and methods for the PRAW package is also included.

### Data dictionary
|no|feature|description|
|-|-|-|
|1|id|the unique id to each reddit post, used to make only 1 post is scrapped|
|2|title|title of the post scrapped|
|3|post_content|if the post is word post, then post content exit|

---
### Data EDA

Features like user, posting habbits like use of emojis and use of pictures were examined.
The number of occurance of words are counted, length of titles are also examined.
Distribution of number of words used to form title are presented graphically.  
Occurance of each words are for the top words are also examined.  

A word cloud is generated:  
<img src='./img/ntd_ps_1st.png'></img>

Then, a simple basic and most naive model that may not even worth 1 point in GA is built.  
It uses TFIDF and Multinominal Naive Bayes.   
Multinominal Naive Bayes is used becuase the text data is not normally distributed.  
TFIDF is used because the number of occurance of the term is not as important as the term itself.   
Hence I also look at the number of appearance of a term in a single document (1 title).  
The results are good, simply because the give away words are not removed.  

Results for the most basic NB model are:  

- The recall of this inference is: 0.93
- The precision of this inference is: 0.91
- The f1 score for this inference is: 0.92

The condusion matrix is:  
<img src='./img/basic_nb.png'></img>

Removing the key give away words like `nintendo` and `playstation` decreases the model performance slightly, but not too much.  
Removing words like `got` and `day` had no impact on the test set.  
This result is very likely due to the use of TF-IDF in the tokeninsation process.  

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
