# NLP_Project
Metis Project 04

## Overview

This project is a continuation of the [**Classifying Climate Change Tweets**](https://github.com/gravesa333/Classifying_Climate_Change_Tweets) project, which classified 4 million climate change tweets (written between 2017 and 2019) as "believer" or "denier" tweets. The classified dataset was simplified to focus only on tweets written by US users, and was then used to answer the following questions for this project:  
	
1. Exploratory Data Analysis Questions
	- How many believer and denier tweets were written within each US region? 
	- What is the total number of users within each US region?
	- What is the total number of believer and denier users? Believer and denier users within each US region?
	- Investigate how "consistent" users are, i.e. do users only tweet believer or denier tweets, or is there a mix?
2. What is the sentiment of each tweet? (positive, neutral or negative)
3. What are the top 30 topics among the US tweets?
4. What are the sentiment trends regarding the top 30 topics?
	- How do believers and deniers feel about these topics?
	- How does sentiment vary across US regions?

The primary machine learning technique used for this project were natural language processing (topic modeling), dimensionality reduction, and clustering.

## Notebooks
- The project was completed through a series of jupyter notebooks. See below for a list, along with a brief description of what was accomplished in each notebook:

1. Project_04_EDA
	- The exploratory data analysis questions listed above were investigated in this notebook. Below is a brief summary of the findings:
		- The majority of denier tweets were written in the South.
		- Most users are in the Northeast, South, and West Coast.
		- There is a higher ratio of deniers to believers in the South and Southwest.
2. Project_04_US_NMF
	- Before performing any NLP or clustering, a US region and tweet sentiment were assigned to each tweet.
	- Each tweet was then lemmatized, tokenized, and tagged with a part of speech. It was determined that nouns were the most important words in each tweet to identify topics.
	- Topic modeling was then performed with TFIDF vectorization and NMF.
	- To prepare for clustering, PCA was used to dimensionally reduce the topic-document matrix.
		- A scree plot was used to determine the ideal number of principal components.
	- Finally, k-means clustering was performed.
		- Inertia and silhouette scores were used to determine the optimum number of clusters.