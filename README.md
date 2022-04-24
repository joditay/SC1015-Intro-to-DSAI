# SC1015 Mini-Project
For our mini project in this module, we performed analysis on the IBM HR Analytics Employee Attrition and Performance [dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) from Kaggle. 

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
1. Random Forest

a.

2. Logistic Regression

a.

3. Neural Network

a.

### Conclusion
- 

### What we have learnt from this project?
- Using pandas.get_dummies to convert catrgorical variables into indicator variables
- Logistic Regression model 
- Justify the suitability of a model based on readings from classification report
- Neural Network model

### References
https://analyticsindiamag.com/guide-to-hyperparameters-tuning-using-gridsearchcv-and-randomizedsearchcv/
https://www.analyticsvidhya.com/blog/2021/06/understanding-random-forest/
https://stackoverflow.com/questions/55229301/one-hot-encoding-multiple-columns-in-sklearn-and-naming-columns
https://www.datacamp.com/community/tutorials/understanding-logistic-regression-python
https://towardsdatascience.com/building-a-logistic-regression-in-python-step-by-step-becd4d56c9c8
