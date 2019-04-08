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

In this project, We do the Exploratory Data Analysis first, to investigate the relations among all the features. We visualize the relation between each feature and the target variable using seaborn regplot() method. We use heatmap to show the correlations among the variables.
The categorical feature 'Research' at first seems to be unimportant since it has the lowest correlation with the target variable. But upon diving further deep into it, we compare the number of candidates who do and do not have Research on their profile, we get to know that it is an important factor.
![Research_Relation](https://user-images.githubusercontent.com/48134752/55743011-e0faea00-5a4e-11e9-98a9-a158775e7964.PNG)

The dataset is then split into train and test sets, and is scaled to the same level, so that the results won't be biased towards some particular features.

## Regression models
We then apply various regression algorithms to the training set. First we are plotting the Learning curves of Random Forest, Linear and Support Vector regressors, to visualize the training behaviour of the models.


    

