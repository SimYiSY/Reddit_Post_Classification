<img src="https://logodownload.org/wp-content/uploads/2018/02/reddit-logo.png" width="600"/>

# Reddit Webscraping


# Introduction
Fairy tales teach children about romantic love. The princess is in danger, the prince comes to the rescue, and they live happily ever after.

But as you grow up, you realise that love is not as simple as saving the person dear to you from her stepmother, an apple, or a curse. Love involves a lot of trial and error, meeting halfway, and swallowing one’s pride. Everything is complicated.


How do you know when it’s really all over?  Is it when one of you calls it quits?  Or, is there still hope even when someone has walked out?  This project will look into it, break up or make up

There are numerous reasons that relationships break up.  Some of them are even good reasons.  For instance, if you are just leading your partner on, it is right to cut him or her loose.  If he or she isn’t trustworthy, that is a good reason for a break up.  Of course, sometimes people’s lives change and the partner no longer fits into the total picture, in which case, it is good to end the relationship.

We will use data from the below mentioned subreddit for this project:

- Subreddit used:
  - Relationship advice: looking for opinions on how to improve or resolve relationship issue
  - Breakups: mentioning why the breakup happen, and why it is not resolved


<img src="http://3.bp.blogspot.com/-qppebMLzuGU/USy6vN-xmmI/AAAAAAAAAdM/HONipAqwV3k/s1600/break-up-mix-art-copy-300x289.jpg" />

## Problem Statement

Create a classification model to determine the text being relationship advice or breakup.

## Executive Summary

The data is webscrapped from 2 reddit subreddit post relationship_advice and BreakUp. A series of transformation, including StopWords removal, Stemming and Vectorization, is done to the raw data to create bag-of-words. A few model is used, mainly LogisticRegression, Naive Bayes and a few DecisionTrees models to see which model gives us the best accuracy to differentiate the 2 different type of subreddit post. MultinomialNB was selected as the best model, which gives us the best accuracy. LogisticRegression was used to analyze the keywords as the model will let us know the importance of the keywords

### Content summary
- Webscrapped from relationship_advice & BreakUp reddit
- Data cleaning
  - Stopwords removal
  - Stemming
  - lowercase
  - punctuation removal
  
- Modeling

  - Vectorizor
    - CountVectorizor
    - TFIDVectorizor
    - Hashing Vectorizor
  - Models
    - LogisticRegression 
    - MultinomialNB 
    - KNN 
    - SVC 
    - DecisionTree  
    - Bagging 
    - ADABoost

### Accuracy of models
- MultinomialNB 
  - 86% for relationship_advice 
  - 83% for BreakUp
- LogisticRegression
  - 86.5% for relationship_advice 
  - 78% for BreakUp
  
### Key findings

- The findings shown that relationship_advice tend to mention more about the other person(Boyfriend,spouse,wife,gf,bf) as opposed to Breakup when it is more self focused(dream, memory,sad, better, move on).
- There is a small misclassification of the model, and after taking a manual check on the post, it can be interpreted that the post would have been better classified under the opposite thread instead. 
- Its interesting to note that around the 6am - 12pm time period, not much relationship advices are posted. This interpretation would be better look into by a psychology specialist to see if there is a relationship in time of post with the content.

### Content
1. Webscrapping
2. Data Cleaning
3. Preprocessing of text data
4. EDA
5. Model
6. Analysis and Recommendation