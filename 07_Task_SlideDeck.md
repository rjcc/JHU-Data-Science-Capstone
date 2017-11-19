Coursera Data Science Specialization Capstone Project
========================================================
author: Mark Blackmore
date: 2017-11-18
autosize: true

The Project
========================================================

This project involves Natural Language Processing.  The critical task is to 
take a user's input pharse (group of words) and to output a pedicted next word.  

*Project deliverables:*  

- Next Word Prediction Model, as basis for an app
- Next Word Prediction App hosted at shinyapps.io
- This presentation hosted at Rpubs

Next Word Prediction Model
========================================================

The next word prediction model uses the principles of "tidy data" applied to text mining in R. Key model steps: 

1. Input: raw text file for model training
2. Clean training data; separate into 2 word, 3 word, and 4 word ngrams, save as tibbles
3. Sort and save most the frequent ngrams in the tibbles as repos
4. Ngrams function: uses a "backoff" type prediction model
  - user supplies an input phrase
  - model uses last 3, 2, or 1 words to predict the best 4th, 3rd, or 2nd match in the repos
5. Ouput: next word prediction

Benefits: easy to read code; uses "pipes"; fast processing of training data; able to sample up to 25% of original corpus; relatively small output repos

Next Word Prediction App
========================================================

The next word prediction app provides a simple user interface to the next word prediction model.  

*Key Features:*  

1. Text box for user input  
2. Text box prompts user input if left blank   
3. Predicted next word outputs dynamically below user input  
4. Side panel with user instructions  

*Key Benefits:*  

1. Fast response  
2. Method allows for large training sets leading to better predictions

[Shiny App Link](https://mblackmo.shinyapps.io/ngram_match/)  

Documentation and Source Code
========================================================

Tidy Data  
"http://vita.had.co.nz/papers/tidy-data.html"

Text Mining with R: A Tidy Approach  
"http://tidytextmining.com/index.html"

Shiny App    
"https://mblackmo.shinyapps.io/ngram_match/"

Shiny App Source Code repository on Github    
"https://github.com/mark-blackmore/JHU-Data-Science-Capstone/tree/master/ngram_match"

Data Specialization Capstone repository on Github    
"https://github.com/mark-blackmore/JHU-Data-Science-Capstone"
