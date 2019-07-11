# Subreddit Post Classifier

### Overview
Aim of the project is to create a model that can accuratly classify reddit posts based on which subreddit they came from by employing NLP principles

### Data
Data was gathered usign the reddit api: https://www.reddit.com/dev/api/ and is stored in csv files:

from r/Warhammer40k - warhammer40k.csv
from r/smashbros - smashbros.csv
from r/paintball - paintball.csv

code for data collection can be found in Reddit Web Scrapping.ipynb and can be rerun easily or applied to different subreddits by changing urls in 'subs' list and rerunning the data collection cell.

### 2 Subreddit Models
Models for 2 of the 3 subreddits are each in seperate notebooks names appropriately.
Each note book compares Logistic regression, kNN, and Multinomial Naive Bayes and uses grid search to tune hyper paramters

### 3 Subreddit Models
The 3 subreddit model is also in a seperate notebook. Liek the 2 subreddit models it includes 3 seperate NLP models and also includes a further interpretation of the best performing model to identify which words were the most discerning, as well the posts the model predicted incorrectlt

### Methods
All models were tested with both Count and TF-IDF Vectorizer and in gerenal TF-IDF performed better. 

Tuning:
Bisection search was used in tandum with grid search to tune hyperparameters, but this does not necessarily prodoce the best result for a given model. The best performing model with 3 subreddits was further tuned using Bayes Optimization, but no improvement was made

Error:
Many of the the posts from the chosen subreddits included no text, so post titles were included too, the lack of information is likely a large source of error as well as terms that are used in both subreddits, but one to a much larger extent

