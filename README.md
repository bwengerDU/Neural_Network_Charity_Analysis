# Neural_Network_Charity_Analysis


## Overview

In this project I am working with Alphabet Soup Charity to examine and predict whether applicants for their funding can be successful. By examining over 34,000 organizations that they have worked with in the past they hope to analyze the key features of these organizations that have lead to success in the past in order to help identify which of the current applicants are suited to become successful if they were to receive Alphabet Soup's funding. 

## Results

-In Deliverable #1 I was tasked with processing the data by removing 'EIN' and 'NAME' columns, grouping columns with 10 or more unique values, one-hot encoding of categorical variables, splitting features and target arrays, splitting into training and testing sets, and standardizing the data. The target for the model is 'IS_SUCCESSFUL' while 'STATUS', 'ASK_AMT', 'IS_SUCCESSFUL', 'APPLICATION_TYPE', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT' are the features of my model. I removed 'AFFILIATION_Other' and 'USE_CASE_Other' columns. 

![alt text](https://github.com/bwengerDU/Neural_Network_Charity_Analysis/blob/main/Images/Deliverable2.png)
-In Deliverable #2 compiled, trained, and evaluated the model. I built my model with 2 layers containing 80 neurons in the first layer and 30 in the second while utilizing Relu and Sigmoid functions as this set up would be a suitable for non linear data sets and to address binary data. The initial results of this model produced 72.06% accuracy with 56.88% loss. This fell short of the 75% accuracy target rate. In the following steps I attempted to increase the accuracy score of my model. 

![alt text](https://github.com/bwengerDU/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1.png)
-Optimization Attempt #1 - Dropping noisy features 'AFFILIATION_Other' and 'USE_CASE_Other'. This model was able to produce an accuracy score of 72.86%, which was an improvement of .8%.  

![alt text](https://github.com/bwengerDU/Neural_Network_Charity_Analysis/blob/main/Images/Attempt2.png)
-Optimization Attempt #2 - Adding a hidden layer of 15 neurons with a Relu function produced a model that produced an accuracy score of 72.78% which took us a step backwards. 

![alt text](https://github.com/bwengerDU/Neural_Network_Charity_Analysis/blob/main/Images/Attempt3.png)
-Optimization Attempt #3 - Change activation functions from Relu to Sigmoid for the second and third layer produced an accuracy score of 72.78% so it had minimal effect. 

![alt text](https://github.com/bwengerDU/Neural_Network_Charity_Analysis/blob/main/Images/Attempt4.png)
-Optimization Attempt #4 - Redistribute neurons to have 80 in the first layer, 40 in the second layer, and 10 in the third layer. This model produced an accuracy score of 73.05%. 

## Summary
My models did improve with some of the changes, but I was only barely able to surpass 73% accuracy score on my final attempt. I think that my model would have been able to surpass the 75% threshold if I were to remove further noisy features. There may a very limited amount of features that can still be dropped, but it should move me closer to the target. It would also be helpful if we could further analyze what is classified what is considered to be successful and to perhaps delve into that data to determine which ones were marginally successful compared to those that would be considered to be a high level of success. Shifting the focus towards those with higher levels of success would help to make the model more accurate in predicting success in future applicants. 
