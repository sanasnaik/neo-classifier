# NEO Classifier
Used R code to predict whether asteroids/NEOs would be classified as hazardous or non-hazardous.

## What I Did
I used Kaggle to find a dataset I was interested in using, which was the “Nearest Earth Objects” dataset sourced from NASA. I plotted the variables from the dataset to gain some insight into it. It had information on different asteroids and other NEOs such as their names, estimated sizes, relative velocity, miss distance, absolute magnitude, and whether or not they were classified as hazardous. I then created a decision tree using rpart for the dataset to predict whether or not an asteroid would be classified as hazardous based on its  characteristics. I also used naive Bayes to create predictions, and then I compared the accuracies of both methods using their confusion matrices.

## What I Learned
For my rpart decision tree, the only two variables that were considered in predicting a hazardous object were its minimum estimated diameter and the miss distance. 
Its minimum estimated diameter is important to know because a larger asteroid would be considered much more hazardous. Furthermore, the consideration of the miss distance suggests that the distance at which an asteroid passes by Earth plays a significant role in determining its classification. A smaller miss distance might lead to the classification of an asteroid as hazardous, while a larger miss distance might suggest a lower risk of impact and therefore a classification of non-hazardous.
Finally, when I evaluated the accuracy of my rpart and naive Bayes models, the rpart accuracy was around 6% higher than my naive bayes accuracy. (91% vs. 85%, respectively). This may indicate that rpart is a better tool to use to classify asteroids as hazardous or not. However… <br />
From the confusion matrices, I gathered that rpart had much more false negatives (predicted that the asteroid was not hazardous when it was) and the naive bayes model yielded more false positives (predicted that the asteroid was hazardous, when it was safe). The rpart model is more likely to falsely assign an asteroid a “non-hazardous” classification while the naive bayes model is more likely to falsely assign an asteroid a “hazardous” classification. In terms of applicability, the naive bayes model is probably safer to use in the real world, because it would be safer to assume an asteroid is dangerous rather than assume a hazardous asteroid is safe.

Dataset: https://www.kaggle.com/datasets/sameepvani/nasa-nearest-earth-objects
