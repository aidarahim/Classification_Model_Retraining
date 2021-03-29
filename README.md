# Classification_Model_Retraining

## Executive Summary
“A rose by any other name... is still a rose” (butchered Shakespeare phrase from Romeo and Juliet).

I am interested in exploring how a successful classification model holds up over time. This is relevant to the work that data scientists carry out, as there is always an element of timing to it. When a model is put into production, how long will it be useful and relevant for? Does it ever need to be retrained? If so, then how often?

I start with 2 categories: practical here's how you do stuff (r/LifeProTips), and deeper existential thoughts (r/Showerthoughts). They are among the largest subreddits, with memberships ~20M, ensuring large post volumes over time. 1000 posts are extracted from each subreddit, at midnight on the 20th of each month, starting Sept 2019 all the way to Feb 2021. Only post 'titles' were used for classification.

8 classification models are evaluated, and 2 are down-selected for comparison: a Logistic Regression and a Support Vector Classifier (SVC). Both perform similarly on test data during the model development phase, even though the SVC scored close to perfect on testing data.

Both models perform similarly throughout time, at accuracies close to that obtained during the model development phase (~85%), and with a remarkably linear relationship between their accuracies. This suggests that in this specific instance, these models are sufficiently robust to variations in posts over time.

The limits of the models are pushed by running them on different pairs of posts, on which the models were not trained. Happily, classification accuracy is still close to 80% when tried on 2 different subreddit pairings.

Repo content is in the folder 'Classification_Model_Retraining'.
