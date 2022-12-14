# K-Nearest-Neighbors-Without-SKLearn

# Overview

This program will outline the process to create K Nearest Neighbors Analysis without the use of SKLearn (for the most part).

# Process

I start by reading in my training dataset, this is the data I will be using to train my model. I removed categorical columns and added a distance column which will be used to gauge the "distance" between our target user and other users. Next I created my target user, which is the data from the first row of my training dataframe. Then I built my distance function, using Euclidean distance to calculate the formula. Finally I sorted the values of my training dataframe in regards to distance from my target user and displayed the results.

Now I am ready to begin building my KNN model. Here I set my K value (number of neighbors) to 10, and sort my training_df by distance again. Finally I assign my KNN to list the 10 nearest neighbor semgents to my target user.

Next I read in my testing data, to begin testing my KNN model's accuracy. Again I remove the categorical variables, and assign a new empty column to my testing dataframe called prediction. This column will hold the segment my KNN model predicts the user will fall into. Again I choose a target user to calculate distance from and input my Euclidean distance function again. 

