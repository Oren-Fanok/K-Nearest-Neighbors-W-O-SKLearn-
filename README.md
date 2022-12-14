# K-Nearest-Neighbors-Without-SKLearn

# Overview

This program will outline the process to create K Nearest Neighbors Analysis without the use of SKLearn (for the most part).

# Process

I start by reading in my training dataset, this is the data I will be using to train my model. I removed categorical columns and added a distance column which will be used to gauge the "distance" between our target user and other users. Next I created my target user, which is the data from the first row of my training dataframe. Then I built my distance function, using Euclidean distance to calculate the formula. Finally I sorted the values of my training dataframe in regards to distance from my target user and displayed the results.

Now I am ready to begin building my KNN model. Here I set my K value (number of neighbors) to 10, and sort my training_df by distance again. Finally I assign my KNN to list the 10 nearest neighbor semgents to my target user.

Next I read in my testing data, to begin testing my KNN model's accuracy. Again I remove the categorical variables, and assign a new empty column to my testing dataframe called prediction. This column will hold the segment my KNN model predicts the user will fall into. Again I choose a target user (this time from the testing dataset) to calculate distance from and input my Euclidean distance function again. I then sort my training_df by distance and retrieve the results, here I can see that the distances are fairly close to the target customer from my testing data.

Now again, I built my KNN model and return the most likely segments of the 10 nearest neighbors to my target customer from the testing data.

Finally, I can begin predicting the segment each user should fall into using my KNN model. I create my prediction variable which is the most likely segment a user will fall into based on the sorted training df I created above. Now this prediction is only relevant for the target customer from the testing dataframe I defined above, so I assign the prediction to the empty prediction column for the first user in the testing dataframe.

To get a prediction for each user in the testing dataframe, I perform the above steps but iterate over each row within the testing dataframe assigning a prediciton for each user. To test the accuracy of my model I read in the master data with the true segments and run a confusion matrix and a classification report. Here you can see the accuracy of my KNN model is 99% 



