# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* In this project I created a ML model that analyzes the risk factor of potential loanees based on previous loan data
* The dataset included datapoints like the size of loan, interest rate, income, number of accounts and demerits help by the loanee in comparison to whether they defaulted on the oan or not
* The prediction was based on 'loan_status' which means the model predicts whether an account would be 'healthy' or 'high-risk'
* The ML Model works by splitting the original data into training and testing data. The training allows us to coach an accurate ML model to recognize patterns in the dataset and the testing lets us know how accurate the model is. With our training set defined, I run a Logistic Regression Model to train the training data based on the probability of a certain result when datapoints fall into certain patterns. Once that training is done I test the Model using the testing dataset and see how accurately the model is based on the accuracy score, classification report and confusion matrix. Then I used an OverSampler to make sure there are an equal amount of 'healthy' values as 'default' values which balances out the dataset. Then I run the test and print the results again to compare

## Results

* Machine Learning Model 1:
~The precision of the model is pretty good. 100% accurate at determining healthy loanees and 85% accurate at predicting defaulters.

~The recall of the model is also encouraging. 91% identification of default instances and 99% when it comes to healthy

~Specificity from my understanding is how well the model identified when a "default" loanee was not "healthy" and when a "healthy" loaneed was. "healthy" being the negative class in this instance

~the f1 score is a combination of the precision and recall scores by mean. The healthy loanees have a really good f1 score while in comparison default is not as good but is still relatively high for an initial credit analysis

~A high geometric mean means that the model performed very well on both positive and negative identification.

~The iba takes a look at the accuracy scores for the predictions. Since the scores are close to 1 that means the prediction is relatively reliable

~The support column shows a high disparity in data between default and healthy loanees. Meaning if we were to normalize the value set and get more data (about 18,000 more values) on "defaulted accounts" our predictions might be more accurate and the scores could go up



* Machine Learning Model 2:
  ~The precision score in this model actually went down for the 'default' category which is a little concerning but could be within the margin of error depending on the preferences of the data analyst
  ~The recall saw a massive improvement with both datasets sitting at an even 99%
  ~The specificity score also saw really good improvement with both datasets rising to 99%

## Summary
* Based on all scores, the second model is actually more accurate even though it scored 'lower' on the test based on precision
* It's more important that potential defaulters aren't marked 'healthy' than making sure potentially healthy accounts aren't marked 'default'

I would recommend waiting for an improved OverSampled Model with precision score seeing the same improvement that the other scores saw. This would be a better determinant that the dataset isn't overfitted and the ML model is actually accurately calculating the account potential.