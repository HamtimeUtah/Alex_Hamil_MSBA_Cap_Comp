## Capstone Project: Swire Coca-Cola
Repository containing Alex Hamil’s portfolio of work for the data science project Swire Coca-Cola machine maintenance and downtime

# Table of Contents
- [Business Problem Statement](#Business-Problem-Statement)
- [Our Solution to the Problem](#Our-Solution-to-the-Problem)
- [My Contribution to the Project](#My-Contribution-to-the-Project)
- [Solution's Value to the Business](#Solutions-Value-to-the-Business)
- [Challenges Our Group Faced](#Challenges-Our-Group-Faced)
- [What I learned from the Project](#What-I-earned-from-the-Project)


## [Business Problem Statement](#Business-Problem-Statement)
Swire Coca-Cola has 6 production plants to meet the demand of 192 million cases of various beverages from 13 different states. These plants are currently only able to meet 94.4% of the demand. One of the reasons these plants fall short of meeting the total product demand is because they are plagued with unplanned down time. This downtime is caused by various failure modes like maintenance, mechanical failure, general wear and tear, etc.

Extensive repairs result in lengthy downtimes that generate work orders in the IWC system.  The long lead times caused by these work orders cost Swire Coca-Cola $60 million annually in production losses. 

The purpose of this project is to create a model that allows Swire Coca-Cola to better understand plant machine maintenance and make predictions of costly failures before they occur.


## [Our Solution to the Problem](#Our-Solution-to-the-Problem)
* Our solution to the problem started by cleaning and understanding the data and its gaps prior to model selection.
* Next we had to decide which variables in the data we wanted to focus on and what our target variable would be. We chose ACTUAL_WORK_IN_MINUTES for our taget variable and to exclude the functional area nodes since this data is captured in the FUNCTIONAL_LOC variable.
* Finally we decided to try both supervised and unsupervised models. We used supervised models to try to create a predictive model that could indicate factors leading to downtime and unsupervised models to look for unseen relationships between maintenance and failure patterns of machinery.

## [My Contribution to the Project](#My-Contribution-to-the-Project)
My contributions to the Exploratory Data Analysis were the exploratory visualizations and summary graphics surrounding the FUNCTIONAL_AREA_NODE locations and the results sections of the EDA analysis. For the modeling notebook I focused on the linear, lasso, and dummy regression models and summarized the supervised modeling results. I wrote a large portion of the work that we used for the business problem statement and created the slides with the business recommendations for the final presentation.

![](/images/Regression%20ROC%20Curve.png)

## [Solution's Value to the Business](#Solutions-Value-to-the-Business)

The Model's classification will be able to help the business understand the costs associated with   
Sensitivity - false positives (identifying customers as credit worthy that are actually risky)  
Specificity - False negatives (identifying customers as risky that would be good candidates for financial products) 

![Specificity](images/Business%20Impact%20Specificty.png)

![Sensitivity](images/Business%20Impact%20Sensitivity.png)

Understanding these rates can help the business consider risk based pricing- where interest rates and credit amounts are adjusted for clients prone to default.

## [Challenges Our Group Faced](#Challenges-Our-Group-Faced)
* With the overwhelming amount of data in the majority class. We found it helpful to downsample the data for this class. This helped reduce overfitting our model to the majority characteristics of customers that are capable of repayment. 
* The limited data available about the minority class meant that we had to resample some of the same data from this class while using various data samples from the majority class. This allowed us to use a larger sample of data and potentially capture more patterns and interactions in the data.
* Capturing the nuances of the data by averaging multiple prediction models helped us to reduce variance and account for different aspects of the data. As you can see we were able to account for 85% of the variance in the data with our ensemble model. 

## [What I learned from the Project](#What-I-earned-from-the-Project)
I learned the importance of developing adequate domain knowledge, importance of understanding your data and its limitations, and the importance of resilient modeling methods.  

Having enough domain knowledge is crucial because it allows you to understand the real-world importance of the features and variables you are studying. This is critical for selecting important variables and effective feature engineering.  

Knowing your data and its limitations is important because it allows you to adjust for important missing variables, and guard against overfit or poor ROC-AUC results. Imbalanced data can minize important details of the target variable or contributing variables.  

Knowing when and how to use multiple modeling methods and the best methods for sampling the most amount of data is important. This will allow the model to account for as much variance as possible while trying to avoid overfit. 
