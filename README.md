# WeRateDogs

WeRateDogs is a Twitter account that rates people's dogs with a humorous comments about the dog. WeRateDogs has over 4 million followers and has received international media coverage. This Twitter account started in 2015 till now. In this project, I gathered tweet data from the start date of this account in 2015 till the end of 2017 and I Wrangled this data to get some insight.
I worked on more than 5000 tweets.

### Usage
In this project, I used python's libraries pandas, NumPy, matplotlib, requests, tweepy & JSON, I wrote my code in Jupyter Notebook file named "wrangle_act2.ipynb" 


This project was divided into several steps.

### Project Steps
- Step 1: Gathering data

- Step 2: Assessing data

- Step 3: Cleaning data

- Step 4: Storing data

- Step 5: Analyzing & visualizing data

- Step 6: Reporting


### Gathering Data

In this step collecting data takes place. For this project, there were three sources to take
data from it in three different ways:-
1. The First file is “​twitter-archive-enhanced-2.csv”. This file was delivered by email and downloaded manually then imported to our working environment using Pandas Library functions.

2. The Second file is “​image-predictions.tsv”. This file has been hosted on a webpage and downloaded from its reverent URL using Requests Library and opened by Pandas Library functions. This file has image prediction breeds from dog images on the tweet using neural networks.

3. The Third file "​tweet-json". This file was created and gathered from Twitter REST API via Tweepy Library to extract more information pertinent to the tweets’ ids in the first file like retweet counts and favourite counts.



### Data Assessment
In this step, we investigate our imported datasets programmatically and visually for quality and tidiness issues.

#### Visual Assessment:
● The Visual assessment done on a spreadsheet application like Excel named LibreOffice Calc.

#### Programmatic Assessment:

● The programmatic assessment is conducted in Jupyter NoteBook using pandas Library functions.
We managed to find some missing values and messy structures in our datasets and that helped and guided us on what to do in the cleaning step. 

We found some quality issues and some tidiness issues.
#### Quality Issues
twitter-archive-enhanced-2.csv
- Data type of 'timestamp' column is object type.
- Data type of 'tweer_id' column is integers type.
- There are retweets and replies in the datasets.
- Null values are represented as "None" strings in some columns
('name','doggo','pupper','puppo','floofer').
- Some values in the 'name' column are errores like 'a' or 'an'.
- Some values in the 'expanded_url' column are missing.
- Some values in 'rating_numerator' and 'rating_denominator' are incorrect and
weird.

image-predictions.tsv
- Non descriptive columns name.
- Inconsistent capitalization for predicted breeds ('p1','p2','p3')
#### Tidiness Issues

Twitter-archive-enhanced-2.csv
- Values are columns ('doggo','puppo','pupper','floofer') instead of 'dogs_stage'
tweet_json
- This isn't considered an observational unit to have its own table needs to be merged to arc_twitter 

### Data Cleaning
In this step, we tried to fix the issues in our datasets one by one. 

First, we made a copy of our original dataframe to have the ability to return if we made a mistake and retry to fix it.

