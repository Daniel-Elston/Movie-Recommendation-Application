![GitBanner3](https://user-images.githubusercontent.com/98388088/158277311-535b2e53-190e-4060-a383-42e9f308ca75.png)

<hr>

<h1 align='center'> Movie Recommendation Search Engine </h1>

<hr>

## Table of contents
- [Status and Details](#status-and-details)
- [Technology](#technology)
- [Introduction](#introduction)
    - [Project Description](#project-description)
    - [Objectives](#objectives)
- [Data Science Methodology](#data-science-methodology)
    - [Problem Formulation](#problem-formulation)
    - [Data Engineering Methods](#data-engineering-methods)
    - [Modeling](#modeling)
    - [Deployment](#deployment)
- [Conclusions](#conclusions)
- [Contributing Members and Contacts](#contributing-members-and-contacts)


## Status and Details
- **Project Status**: [Complete]
- **Date Coded**: 14/04/2022
- **Link to raw Data**: https://www.kaggle.com/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows/activity
- **Notes**: 2 files exist, one lablled NB and one App. The NB file has an analysis complete with the movie recommendation architecture. The App file has the application independant of analysis.


## Technology
- Language: Python 3.7
- Libraries: pandas, numpy, sklearn, nlkt
- Set up File: Install nltk, package download x 3


## Introduction
The purpose of this project is to develope an application that can recommend movies based on user input. Often times it is difficult deciding on what film to watch. Many websites recommend films based on movie titles alone. This application aims to give an extra level of help to the film buff by suggesting movies based on their overview/description.

### Project Description
The dataset used in this project is the IMBD dataset of top 1000 movies and TV shows. The dataset consists of 1000 movies and TV shows rated by critics and users as well as other information such as lead actors, gross profit etc. A further feature of this dataset is the Overview feature, where a description of the movie plot is given. This dataset can be switched with a larger dataset when deployed to allow for a broader set of results. However for the purpose of this project, 1000 observations is plenty. A 'shuffle results' feature has further been added to avoid repeat suggestions.

The Overview feature has been indexed to reduce variation in words and improving matching potential. Relevance judgements have been applied to evaluate the model effectively. Precision and recall metrics have also been employed for evaluation. The results are as expected, returning the films deemed most relevant to the user input first.

### Objectives
- Provide movie recommendations based on user input query
- Connect raw textual data with user input queries
- Employ BM25 retrieval framework to provide relevance judgements 
- Evaluate retrieval model


## Data Science Methodology
The below subsections outline the standard methodology of data scientists.

### Problem Formulation
Many people spend a significant amount of time (as much as hours) looking for a movie to watch. It can sometimes even be a reason to avoid watching a movie altogether. If your in the mood for a particular film, simply think of a few key words to describe it and input them to this application. You will be met with many films alligned with your input.

A further problem considered was the fact that many film buffs have the same movies being recommended time and time again. To avoid this, a shuffle feature is added. This shuffles the resultant movie suggestions, bringing more unpopular movies to the surface. The shuffle options further adds a component of variation to the suggested movie plot.

### Data Engineering Methods
- Data Reduction
- Stop word removal
- Lemmatization
- Vectorization

### Modeling 
Using BM25 retrieval framework, each vectorized document was scored to give a metric of relevance. The result was a dataframe consisting of movies most relevant to the user input query.

### Deployment
Having some blind test trials from friends, the application works very well. Users seem satisfied with both the results, their chosen suggsted film, the variation in suggestions and the thought process behind the shuffle option.

## Conclusions
The application works very well providing sound suggestions for movies based on user input. Although difficult to evaluate, the F1-score for most words seems quite high (avg. 80%). The thought surrounding the shuffle button further appears to be much appreciated by the film buff. 

## Contributing Members and Contacts
**Group Members**: This project was completed by a group of 4.
**Team Lead: [Daniel Elston](https://github.com/Daniel-Elston)**

|Name     |  GitHub Handles   |  
|---------|-----------------|
| Daniel Elston | [Git DE](https://github.com/Daniel-Elston)   |

Please feel free to contact me if you have any questions, require any further information or wish to contribute.<br/>
Email 1: delstonds@outlook.com <br/>
Email 2: ec21024@qmul.ac.uk
