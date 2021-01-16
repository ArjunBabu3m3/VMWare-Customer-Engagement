# VM Ware - Customer-Engagement Improvement

### TABLE OF CONTENTS
* [Objective](#objective)
* [Technologies](#technologies)
* [Algorithms](#algorithms)
* [Data](#data)
* [Analysis](#analysis)
* [Results](#results)

## OBJECTIVE 
## Improving customer engagement at VMWare through Analytics
1. To find a model with parameters to show the estimates of performance that could be shared with business.
2. Prove that the model could be implemented in the real world so that the business could be convinced of the benifits.
3. Suggest future extensions to this model that the business can incorporate to improve its performance.

## TECHNOLOGIES
Project is created with:

* R Programming - **SMOTE, LiblineaR, ggplot2, randomForest, RRF, gbm, xgboost**

## ALGORITHMS
* SMOTE
* Random forest
* LASSO
* Ridge Regression
* XGBoost

## DATA
The data consists of 700+ variables from 500+ potential customers from VMWare's web analytics team. As the dataset is confidential, I cannot share the data I received here on GitHub as opensource. However, you can always buy the project from ISB's publication content sharing website.

## ANALYSIS
Dealt with null values and variable data types in order to process the input data in R. Selected significant variables through thorough exploratory analysis. Then cleaned the data in R and the code file can be accessed [here](https://github.com/VipanchiKatthula/VMWare-Customer-Engagement/blob/master/code/Project%20Code.R)

## Random Forest Model - Variable selection using Importance
Used the Random Forest model's capability to show the variable importance to identify the significant variables from the variables selected after the exploratory analysis.
![GitHub Logo](/images/RF_model.PNG)

The importance is calculated through the mean decrease in gini index value and below are the top variables that came out significant.

![GitHub Logo](/images/significant_variables.PNG)

## LASSO Regression Model
We built a Lasso regression model using the top 200 variables that came out significant from the Random Forest model. We performed Cross-validation to get the best cost paramater for the LASSO regression.
![GitHub Logo](images/LASSO_Model.PNG) 

## XGBoost Model
We also built XGBoost model using the top 200 variables from the Random Forest model. The XGBoost model outperformed the LASSO regression in terms of accuracy and recall by 6% and 4% but understanding the model parameters is difficult. So, we went ahead with the Random forest model to better understand the model variables.
![GitHub Logo](images/Xgboostresult.PNG) 

## RESULTS
1. The top most variables that control the user conversion from visitor to a customer are **product page views, first data of download, top resources and pdf downloads**. 
2. By mainly focusing on the visitors that view a product page more than the mean page views, the conversion rate of the comapny can be highly increased. 
3. If a user is downloading more pdfs from the website, then it means that he is interested in the coresponding product as these pdfs are mostly product manuals and inromation brochures. 
4. The performance of the model can be imprved by understanding the user-behavior of more and more users. The limitation currently on the project is that the data was only for ~500 users. This can be overcome by training the model on more users.
