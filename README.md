# Attrition-analysis
 

INTRODUCTION

We are aiming to create a system of prediction of employee attrition and retention by visualization using business analytics principles on big data and using sentiment analysis to prevent the same. Job hopping is an increasing trend in India and globally and this costs the companies. This issue is developing definitely, anyway most of the organizations did not have a relentless and general point of view of representative wearing down along these wines Human resource prediction analysis is critical to make logical capacities which can be capable to convey more Return on Investment. It is the eventual fate of the association which discovers the business bits of knowledge in the field of information investigation by passing judgment on the past variables and making AI models to foresee the steady loss,non appearances and different dangers to improve the representative maintenance. We will use machine learning to predict employee turnover. Our objective is to find out How Attrition affects companies and how HR Analytics helps in predicting attrition. After analysis we aim at finding factors affecting employee satisfaction and creating environments that promote retention using sentiment analysis of employee E-mail and Feedback dataset. This analysis Is done on a public Human resources dataset with morethan 10000 entries and multiple fields. Multiple statistical analysis is conducted against a detailed of hypothesis which factors affect attrition and which cause retention.

Data will be visualized and a model will be created. The examination was for the most part attempted to distinguish the dimension of worker's disposition, the disappointment factors they face in the association and for what reason they like to change their activity. When the dimensions of Employee's mentality are recognized; the administration would be able tomake fundamental move to lessen whittling down dimension. Since they are considered asspine of the association, their movement will prompt the accomplishment of the association for the long run. 

AIM:

 In this project, we perform a complete machine learning work flow from data exploratory and feature engineering to build different machine learning models and evaluate model performances to predict if an employee will leave his/her current employer and analyze what features will mainly affect employee’s attrition activity.

SCOPE:

1.	To determine effect of attrition on the business.
2.	Determination of solutions to avoid or to control attrition.
3.	To understand the extent of job satisfaction among the employees.
4.	To suggest proper measures.
5.	Helping them to reduce the employee Attrition.
6.	The study educates the causes of attrition for employees in an organization.
7.	The study also helps to find the drawbacks of the current retention strategies.

Data Exploratory and analysis:

Data exploratory is the most important part of the work flow for machine learning project as it is the first approach to understand the whole dataset and all the features including numerical and non-numerical, missing data, duplicate data, meaningful and meaningless. Since we will try the best to understand and apply all the useful features to the models later on, we would have to make ourself understand all the features that we have.

 
Fig 4.1 Distribution of Target Variable


As we could see the distribution of our target variable is imbalanced for the binary variable yes and no.


 
Fig 4.2 Distribution of Numerical Features

This is the distribution of our numerical features. We have preprocessed all the numerical features so there are no missing data or duplicate data. From the exploratory, it looks like exit employee's age and working time with his current position give out some signals of attrition as well as daily rate which refers to paystub.

 
Fig 4.3 Distribution of Non-Numerical Features
This is the distribution of non-numerical features. Even though all the distribution is imbalanced, we could still tell that too much over time work definitely will drive away a loyal employee. Traveling and marital status will also be considered as factors of the effect.

4.2 Feature Engineering:

 
Fig 4.4 Correlation Matrix


From this matrix we could be able to see correlations between each feature and between features and target variable. For correlation score > 0.5, we would consider the two features are correlated. For non-numerical features, we applied one hot encoding and transform them into numerical.





4.3 Model Training:

 
Fig 4.5 Naive Approach

Naive approach is to apply features to the models without hyperparameter tuning. We could roughly get the result of performance of each model. Here we use the linear model, tree-based model, ensemble learning model and deep learning model.

Hyperparameter Tuning:

Here are the graphs with different hyperparameter affect the performance of logistic regression and k nearest neighbors.
  
Fig 4.6 Grid Search Cross Validation Result

K fold cross validation is the method we use to check the performance of the model on different dataset, so basically we split our dataset into trainig set and testing set, and we split training set into same different portions, and we apply each portion to our model and get the mean score of the model performance. Then we will apply use our testing set to verify the accuracy of our predictions.

Model Evaluation:

There are different metrics to evaluate a model's performance. For classification problem, which is what we tried to solve in this project, accuracy is one of the metrics that we will look at. Beside accuracy, precision and recall is another metric that we need to pay more attention especially for imbalanced variable. Assuming we only have 1 employee exit in our dataset and we predict everyone is staying, then we will have a model with accuracy 99% which still cannot be able to help us to find out the employee who would like to exit. So, precision recall and f1 score will the metric for our evaluation. And to better evaluate and visualize the result of precision and recall, we use confusion matrix graph with labels of actual and prediction.

      
Fig 4.7 Metrics score


ROC analysis is another metric to evaluation how well the model could separate the true label and false label accurately. 

 
Fig 4.8 ROC Curve Analysis

AUC a.k.a area under curve, the higher the value is the less randomness the model will generate for the correct true or false label here is yes or no. The ideal AUC will be 1 which will fill up the whole square and worst is the triangle that goes diagonal across the square.

4.4 Feature Importance:

This is the most important analysis that gained from random forest and LASSO aka linear model with regularization. The feature importance reveals how important each feature is and how it will affect the performance of the model.







 
Fig 4.9 Random Forest Feature Importance

 

Fig 4.10 LASSO Feature Importance 

CONCLUSION:

It is quite obvious that everyone will accept, which is paying more and working less may be the eliminate dream for all employees. Overtime, monthly rate, age, years of works they all are very important feature that will affect the attrition activity and performance of an employee. So, it will be quite efficient to approach to those higher risk employees and better communicate with them, so that their intention of attrition could be resolved. It will be beneficial for both employer and employee. Otherwise, plan ahead of time to hire new candidate will be an alternative option.

FURTURE PLAN:

This is a complete flow for machine learning and there is still much of work to do. We will need to spend more time on tuning the model so that we will have a more robust model that could be deployed in the future. If possible, we could collect more data and more features so that the model could learn more from data and make more accurate predictions.
