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

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/0b4f3307-628d-4c80-9c97-7a550bad4c86)

As we could see the distribution of our target variable is imbalanced for the binary variable yes and no.

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/465b0053-2b23-4894-a145-60cf004c20ed)

This is the distribution of our numerical features. We have preprocessed all the numerical features so there are no missing data or duplicate data. From the exploratory, it looks like exit employee's age and working time with his current position give out some signals of attrition as well as daily rate which refers to paystub.

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/775f085b-f229-47d4-b3ec-1377df132c15)
 
This is the distribution of non-numerical features. Even though all the distribution is imbalanced, we could still tell that too much over time work definitely will drive away a loyal employee. Traveling and marital status will also be considered as factors of the effect.

Feature Engineering:

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/60b9dbb2-2935-4a17-9756-5b4606469cb4)

From this matrix we could be able to see correlations between each feature and between features and target variable. For correlation score > 0.5, we would consider the two features are correlated. For non-numerical features, we applied one hot encoding and transform them into numerical.

Model Training:

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/ff10afde-7030-44e6-be98-83ae4c5bf3b4)

Naive approach is to apply features to the models without hyperparameter tuning. We could roughly get the result of performance of each model. Here we use the linear model, tree-based model, ensemble learning model and deep learning model.

Hyperparameter Tuning:

Here are the graphs with different hyperparameter affect the performance of logistic regression and k nearest neighbors.

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/2024fa88-bcb9-4cf5-b98f-b69bcabc0d73)
![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/ef87a501-5b98-4d03-ae86-c3fdf40c0242)
Grid Search Cross Validation Result

K fold cross validation is the method we use to check the performance of the model on different dataset, so basically we split our dataset into trainig set and testing set, and we split training set into same different portions, and we apply each portion to our model and get the mean score of the model performance. Then we will apply use our testing set to verify the accuracy of our predictions.

Model Evaluation:

There are different metrics to evaluate a model's performance. For classification problem, which is what we tried to solve in this project, accuracy is one of the metrics that we will look at. Beside accuracy, precision and recall is another metric that we need to pay more attention especially for imbalanced variable. Assuming we only have 1 employee exit in our dataset and we predict everyone is staying, then we will have a model with accuracy 99% which still cannot be able to help us to find out the employee who would like to exit. So, precision recall and f1 score will the metric for our evaluation. And to better evaluate and visualize the result of precision and recall, we use confusion matrix graph with labels of actual and prediction.

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/8a8f505b-be9b-4780-a9e8-cb9223a37665)
![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/88645682-60d2-43d9-843c-b5fd839ee637)
![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/84c814ca-d2ff-4f6e-a66b-29f56c622fc5)
![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/c0b2c9d9-48f8-44f9-8274-edbff174203f)
![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/79112efd-ed80-4058-b788-6a223977da76)
![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/768d2101-049b-4854-8090-9e40f3ce8788)
Metrics score

ROC analysis is another metric to evaluation how well the model could separate the true label and false label accurately. 

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/209614fb-eb54-4fa3-8a46-21372c15f5a4)
ROC Curve Analysis

AUC a.k.a area under curve, the higher the value is the less randomness the model will generate for the correct true or false label here is yes or no. The ideal AUC will be 1 which will fill up the whole square and worst is the triangle that goes diagonal across the square.

Feature Importance:

This is the most important analysis that gained from random forest and LASSO aka linear model with regularization. The feature importance reveals how important each feature is and how it will affect the performance of the model.

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/81095163-b9c5-4238-a13d-c0d4d824cd74) 
Random Forest Feature Importance

![image](https://github.com/monkey-d-luffy1/Attrition-analysis/assets/88392078/11c1de43-25ed-49ef-9c18-5991ec0f4562)
LASSO Feature Importance 

CONCLUSION:

It is quite obvious that everyone will accept, which is paying more and working less may be the eliminate dream for all employees. Overtime, monthly rate, age, years of works they all are very important feature that will affect the attrition activity and performance of an employee. So, it will be quite efficient to approach to those higher risk employees and better communicate with them, so that their intention of attrition could be resolved. It will be beneficial for both employer and employee. Otherwise, plan ahead of time to hire new candidate will be an alternative option.

FURTURE PLAN:

This is a complete flow for machine learning and there is still much of work to do. We will need to spend more time on tuning the model so that we will have a more robust model that could be deployed in the future. If possible, we could collect more data and more features so that the model could learn more from data and make more accurate predictions.
