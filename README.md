# Project - Phase01_Case_Study
Case Study: Google Play Store  

## Introduction
In this case study we took a cursory dive into Google Play story data and share inital findings. 

## Objectives
You will be able to see how we answered the following quesions :
1. Which app category, in your opinion, has the best ratings? How are you measuring best ratings?  
2. Is there a relationship between ratings and size? How did you measure the relationship? Why did you choose this measurement? 
3. For your category, how many genres are represented? What are their counts?  
4. An open analysis of user review sentiment.

## The dataset
For this case study, we worked with the "data/googleplaystore.csv" & "data/googleplaystore_user_reviews.csv"

## Step 1: Data Importing 
We started by importing the following libraries as well as reading the data files & turing them into dataframes  
    
## Step 2: Data Cleaning
After some exploration we noticed an inconsitency on row 10472 we fixed this shift error. Based on our internet reserach we replaced the NAN values in the "Type" and "Genres" categories with the most up to date information available. Information was not available on the "Current Ver" category NAN values. We decided to set them at 1.0 to indicate that while a version does exist they have never been updated. In order to decide how the NAN values in the Ratings Column. After preforming agg functions on the values as is, dropped, mean inserted and median inserted we decided to leave the NAN values as is. For the purposes of anaylsis we also split genres into sub genres, turned the price column into a float, and unified all size united into M. 

## Step 3: Answering Question 1 
Question One: Which app category, in your opinion, has the best ratings? How are you measuring best ratings?  

In order to answer this question we grouped the dataframe by Category and Rating and then looked at the mean values for each Category. The majority of these means fell between 3.5 and 4.2 Stars. We then ordered our data in decending order and graphed the information. 

## Step 4: Answering Question 2 
Question Two: Is there a relationship between ratings and size? How did you measure the relationship? Why did you choose this measurement? Please create a scatterplot of size vs ratings to demonstrate the relationship or lack thereof. 

In order to answer this question we created subplots of both size and rating and then joined them do examine correlation. We also caluculated mathamatical correlation based on these two elements. 

## Step 5: Answering Question 3  
Question 3: For your category, how many genres are represented? What are their counts? Please show this with a bar chart. 

In order to answer this question we indexed the datafram by both catergory and genre and then took a value count of each sub genre with in the category. We then graphed this information using a bar chart. 

## Step 6: Answering Question 4  
Question 4: You choose what you want to investigate 
. In
We chose to investigate how sentiment affect the rating, and how do other factors affect the sentiment. In order to do this we took the unique values from the reviews and merged their values with our original dataframe to create visualizations of this effect.

## Summary  
Based on our analysis we provided several key take aways for external buisness parters and concluded the following next steps: 
    1. You could continue breaking down the size category into feature lists to dig deeper into the size, rating correlation if any, when zoomed in. 
    2. Data modeling could be done of price and rating correlation which would provide insight on for pricing models. 
    3. Additional data munging could be done on sentimentality ratings and subjectivity scale to determine if an app was recieving real reviews or not.
    4. Data modeling of category type on download rate could be 
