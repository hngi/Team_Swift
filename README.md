# Team_Swift 
#### Machine Learning Track

## Recommender System for Lucid Blog
This repository contains the files and notebooks used to model the recommender system for lucid.blog.
We prepared the dataset given for wrangling operation by querying the sql file and obtaining a .csv file.
The obtained data was cleaned to remove outliers and unnecesssary features.

### Exploratory Data Analysis
Each database table was explored to determine their statistical properties such as mean, standard deviation, min/max, etc.

### Building the Recommender Systems.
Each keyword in the short bio content was converted into a list of strings where each string is a keyword. And content-based filtering approach was used to model the recommender system. For this task, we looked at the similarities among the user's bio content to recommend followers and articles to read. 

* Why similarity?
We must talk about similarity because we want to find users who have similar contents in their short bio to follow each other and also to suggest related article to read.

* How do you define similarity?

**Similarity is the relation of sharing properties.**

For example, in Twitter, you can get recommendations on who to follow, which is probably found by calculating similarity. One could
say that two people have similar tastes because they both like films with Tom Hanks, science fiction films, or simply all-evening movies. But then, even people who like scifi have different tastes. Maybe one person likes Star Trek and another Star Wars. Are they similar?

Also, similarities can also be found using additional information such as metadata about which other user was follow by another user.

* Similarity Functions
There are different functions such as Jaccard similarity, Pearson Correlation Coefficient, Cosine Similarity, etc.
Since we have quantitative data, we decided to go with *Cosine Similarity.*


### Testing the model
It only makes sense to look at users who’ve similar bio content as the test user (content-based filtering) since they would share similar personalities. To be even pickier, we need users who not only have similar content but also share some followers with the user (neighborhood based filtering). Those are the ones that make better recommendations.
We tested the model by inputting the test user's id in the ```who_to_follow``` and ```article_to_read``` function to show the recommended followers and articles to read respectively.


The download link to the dataset for team_swift_recommender_sys https://drive.google.com/folderview?id=1mnqsQoZ4V8h-W8gPA3AISvUsfpu8vPdQ, then you can  open the code on Google colab and remount the downloaded dataset on colab from your Google drive that is after uploading the dataset to your Google drive.
https://github.com/hngi/Team_Swift/blob/master/Team_Swift_Recommender_sys.ipynb

The download link to the dataset for Article_recommender https://drive.google.com/folderview?id=1aIysvBfKMD8o79D8H5P59ageLIdQuudm , then you can  open the code on Google colab and remount the downloaded dataset on colab from your Google drive that is after uploading the dataset to your Google drive.
https://github.com/hngi/Team_Swift/blob/master/Article_recommender.ipynb
