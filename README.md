# SC1015 Mini-Project
For our mini project in the Introduction to Data Science and Artificial Intelligence module (SC1015), we performed analysis on the IBM HR Analytics Employee Attrition and Performance [dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) from Kaggle. 

### Problem Definition
- What is the profile of employees who quit IBM?
- Top reasons for an employee's resignation
- What can IBM do to better retain its workers?

### Members (DSF3)
1. Hung Kuo-Chen
2. Jodi Tay Seow Xuan
3. Yang Xiaoyue

### Files Included
1. IBMAttrition.csv - dataset
2. SC1015 Project Slides.pdf - presentation slides for our project
3. SC1015 Mini Project.ipynb 
    - Cleaning and preparation
    - Basic visualization
    - Exploratory data analysis
    - Machine learning: Random Forest, Logistic Regression, Neural Network  

### Notebook Details
#### Cleaning and Preparation
   a. Check for missing values within the dataset

   b. Remove insignificant columns: 'EmployeeCount', 'Over18', 'StandardHours', and 'EmployeeNumber'


#### Basic Visualization
   a. Used box plots, histograms, and violin plots in visualizing numeric variables

   b. Used the GroupBy function to create a categorical bar plot of attrition against each categorical variable


#### Exploratory Data Analysis
   a. Plot a correlation matrix to identify multicollinearity and any existing patterns within numeric variables

   b. Explored bi-variate relationships with a scatter plot


#### Machine Learning
*1. Random Forest*

    a. Extract numeric variables that have high correlation with attrition as predictors and build a model using Random Forest Classifier
       - A accuracy of 84.5% is achieved

    b. Do hyperparemeter tuning using Random Search and plot one of the trees from Random Forest
       - The accuracy is improved to 84.7%

*2. Logistic Regression*

    a. Get the 6 categorical variables and convert them into indicator variables using pandas.get_dummies
    
    b. Build a Logistic Regression model based on the predictors and print out the rank of importance of predictors using Recursive Feature Elimination (RFE)
       - The accuracy on test set is 0.84
       - 'OverTime' and 'Gender' contribute more to the predicton of attrition than the rest of the predictors
    
    c. Examine the classification report and analyze the model based on 'precision' and 'recall'
       - Get the conclusion that the model is not effective even with high accuracy
       - The highly imbalanced distribution of employees when categorizing by attrition is the major factor for the high accuracy
    
    d. Get the confusion matrix to back up our conclusion

*3. Neural Network*

    a. Import PyTorch library and select major numeric attributes
        - The attributes include 'MonthlyIncome', 'DistanceFromHome' and 'YearsInCurrentRole'

    b. Build a multilayer perceptron model for multi-label classification
    
    c. Train the model with CrossEntropyLoss as loss function and SGD as optimizer.
        - The loss of the model reduced significantly after training through 3 epochs
        - The accuracy on test cases is 85.7%


### Conclusion

*Machine Learning Comparisons*
- Random Forest suggests that numeric variables with relatively high correlation with attrition are useful in predicting attrition
- Logistic Regression is not recommended as a technique as most categorical variables are irrelevant in determining attrition
- Neural Network is highly useful in effectively predicting attrition

*Data Driven Insights*
- Common profile of employees who quit: low salary, lives far away from office, low chance of career progression/lack of opportunities
- Actions for IBM: increase salary incentives, enhance effective employee assessments, change up roles in senior management

### What we have learnt from this project?
- Using pandas.get_dummies to convert catrgorical variables into indicator variables
- Logistic Regression model 
- Justify the suitability of a model based on readings from classification report
- Neural Network model

### References
1. https://analyticsindiamag.com/guide-to-hyperparameters-tuning-using-gridsearchcv-and-randomizedsearchcv/
2. https://www.analyticsvidhya.com/blog/2021/06/understanding-random-forest/
3. https://stackoverflow.com/questions/55229301/one-hot-encoding-multiple-columns-in-sklearn-and-naming-columns
4. https://www.datacamp.com/community/tutorials/understanding-logistic-regression-python
5. https://towardsdatascience.com/building-a-logistic-regression-in-python-step-by-step-becd4d56c9c8
6. https://github.com/PacktPublishing/Deep-learning-with-PyTorch-video
7. https://androidkt.com/load-pandas-dataframe-using-dataset-and-dataloader-in-pytorch/
