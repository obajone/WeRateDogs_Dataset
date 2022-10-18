# WeRateDogs Data Exploration
## by Eddington Obaro Jonathan

## Wrangling Process

> This analysis was based on the WeRateDogs twitter archive. The data wrangling process involved three 
stages which are: data gathering, assessment and cleaning. 
The first stage was the data gathering. There were three datasets which were required to be wrangled 
and they are twitter-archive-enhanced.csv, image_predictions.tsv and tweet-json.txt. The twitter-archive-enhanced.csv was downloaded manually from Udacity Classroom. The image_predictions.tsv
was downloaded programmatically from Udacity Classroom. The tweet-json.txt was expected to be an 
additional dataset gathered from Twitter’s API. However, because of my inability to setup a Twitter 
developer account, I chose the shortcut approach which required that I download the tweet-json.txt file 
manually from Udacity Classroom. I was also required to copy and paste the content of twitter_api.py (a 
file downloaded from Udacity Classroom) into my Jupyter notebook.

>During the data assessment, I discovered that some ratings were retweeted. There were missing values 
in some columns. There were values in rows that were supposed to be empty. There were inaccurate 
values. Some rating_denominator rows were inconsistent. There were extremely high rating score 
which could have been a result of typo error. Some columns in one table were duplicated in other 
tables. There were inconsistent column names. All these issues made the data dirty. However, there 
were some tidiness issues. Some columns required splitting. Some columns needed to be complete 
tables.

>During the data cleaning, I removed the retweets and columns with high number of missing values. For 
the rows with inaccurate rating scores, I replaced them with the accurate rating scores which I got from 
the ‘text’ column where the rating scores were extracted from. However, I dropped the rows with 
supposed null values which had inaccurate values in them. Also, for the rows with rating_denominator 
greater than 10, I reduced the rating_denominator to 10 by dividing both rating_numerator and 
rating_denominator by an appropriate number. I replaced ratings above 100 with the mean. I dropped 
duplicated columns. I renamed column with inconsistent names. I split columns that required splitting 
and I converted columns that needed to be complete tables into tables.
In the last part of the data cleaning, I merged the three datasets to produce a master dataset which I 
stored as twitter_archive_master.csv


## Summary of Findings

- People are most likely to retweet a rating that they like.
- It appears that people tend to like tweets with high rating score.
- It appears that people tend to retweet tweets with high rating score.
- The highest mean rating was done between 06:00 and 07:00 daily. This means that WeRateDogs  give high ratings within this hour of the day.
- There is no significant difference in the rating scores in different days of the week.
- WeRateDogs tend to give high ratings in the month of October and low ratings in the month of November.
- In the three years under study, 2017 got the highest rating scores while 2015 got the lowest rating scores.
- People tend to like a rating between the hours of 6:00 and 7:00.
- People are more likely to like a rating on a Wednesday and are less likely to like a rating on a Thursday.
- People are more likely to like a rating in May, June and July and are less likely to like a rating in November and December.
- People are more likely to retweet a rating in June and are less likely to retweet a rating in November.
- People retweeted more ratings in 2017, about five times more than in 2015.
- People liked more ratings in 2017, almost ten times more than in 2015.