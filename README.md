# Graduate_Admission_Chances_Prediction
This Project is about building the predictive model for predicting the Chances of Graduate Admissions in the American Universities. The dataset contains several parameters which are considered important during the application for Masters Programs. This dataset is taken from kaggle datasets which can be found here: https://www.kaggle.com/mohansacharya/graduate-admissions

The parameters included are:

    GRE Scores ( out of 340 )    
    TOEFL Scores ( out of 120 )    
    University Rating ( out of 5 )    
    Statement of Purpose and Letter of Recommendation Strength ( out of 5 )    
    Undergraduate GPA ( out of 10 )    
    Research Experience ( either 0 or 1 )    
    Chance of Admit ( ranging from 0 to 1 )    

## Exploratory Data Analysis:

In this project, We do the Exploratory Data Analysis first, to investigate the relations among all the features. We visualize the relation between each feature and the target variable using seaborn regplot() method.
![Feature_Target_Relation_Plots](https://user-images.githubusercontent.com/48134752/55744143-d4c45c00-5a51-11e9-9881-e6a0ec40a162.PNG)


We use heatmap to show the correlations among the variables.



The categorical feature 'Research' at first seems to be unimportant since it has the lowest correlation with the target variable. But upon diving further deep into it, we compare the number of candidates who do and do not have Research on their profile, we get to know that it is an important factor.
![Research_Relation](https://user-images.githubusercontent.com/48134752/55743011-e0faea00-5a4e-11e9-98a9-a158775e7964.PNG)

The dataset is then split into train and test sets, and is scaled to the same level, so that the results won't be biased towards some particular features.

## Regression models: Visualizing the behaviour and fit the models

We then apply various regression algorithms to the training set. First we are plotting the Learning curves of Random Forest, Linear and Support Vector regressors, to visualize the training behaviour of the models.

![Learning_Curves_Regr](https://user-images.githubusercontent.com/48134752/55743461-fde3ed00-5a4f-11e9-807e-c8c04ab146ec.PNG)

From above plots, we decide to use Linear Regression first. Since Random Forest regressor shows high variance, adding more data won't do any good. In that case, we need to have more complex model, which we will see later by tuning the hyperparameters.

We then move on to apply Linear Regressor by finding the best parameters using Grid Search. Same is followed for Decision trees, Support Vector and Random Forest regressors. We use r2 score to measure the accuracy of the Regression Models predictions.

## Classification models: fit the models with best parameters and get the best accuracy

For trying the classification models, we need to convert the Target Variable to categorical type from continuous type. So we decided that if the Chance of Admit is greater than 80% (0.80), we'll convert it to 1 and if it's less than 80%, we convert it ot 0.

We then apply the classifiers Logistic Regression, Support Vector classifier, Naive Bayes, Decision Tree and Random Forest Classifiers and K Nearest Neighbours. We use f1 score to measure the accuracy of the classification models predictions.

## Comparing all the estimators performance:

Finally, we visualize the comparison of all the Regression models' scores in one plot and all the classification models' scores in another plot.
![Performance_Comparison](https://user-images.githubusercontent.com/48134752/55743889-1accf000-5a51-11e9-9606-02b6427190f4.PNG)


The graph of regressors shows that the Random forest and Linear regressors perform comparably well than others.
For classifiers, the graph shows that the Logistic Regressor and Support Vector Classifier worked well.


## Conclusion:

Getting into the desired university for Post Graduate programs is a 'dream come true' for almost all the aspirants. This model can be a potential saviour for a huge number of aspirants, which will enable them to spend less money on the applications, as they will be able to apply only to the appropriate universities according to their credentials, because the application forms of the universities often cost a significant amount for a grad student.
