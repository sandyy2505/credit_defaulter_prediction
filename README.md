# Credit_defaulter_prediction
Credit Defaulter prediction model - Logistic Regression, Confusion Matrix.

### Context
The original dataset contains 1000 entries with 20 categorical/symbolic attributes prepared by Prof. Hofmann. In this dataset, each entry represents a person who takes a credit by a bank. Each person is classified as good or bad credit risks according to the set of attributes. It is almost impossible to understand the original dataset due to its complicated system of categories and symbols. Thus, the attributes in this dataset is a subset of the original dataset. Several columns are simply ignored, and some of the important attributes like age, account balance etc. are retained.

### Objective 
To identify if a person is at risk of making default or not.

### Dataset:
- Age (Numeric : Age in years)
- Sex (Categories : male, female)
- Job (Categories : 0 - unskilled and non-resident, 1 - unskilled and resident, 2 - skilled, 3 - highly skilled)
- Housing (Categories : own, rent, or free)
- Saving accounts (Categories : little, moderate, quite rich, rich)
- Checking account (Categories : little, moderate, rich)
- Credit amount (Numeric : Amount of credit in DM - Deutsche Mark)
- Duration (Numeric : Duration for which the credit is given in months)
- Purpose (Categories: car, furniture/equipment, radio/TV, domestic appliances, repairs, education, business, vacation/others)
- Risk (0 - Person is not at risk, 1 - Pesron is at risk(defaulter))

## Model Building - Approach
1. Data preparation
2. Partition the data into train and test set.
3. Built a Logistic regression on the train data.
4. Remove multicollinearity and insignificant variables, if any
5. Choose optimal threshold, if required.
6. Test the data on test set.

### Model evaluation criterion

### We will be using Precision as a metric for our model performance, because here company could face 2 types of losses
1. Could Give loan to defaulters - Loss of money
2. Not give Loan to non-defaulters - Loss of opportunity

### Which Loss is greater ? 
* Giving loan to defaulters i.e. False negative i.e Predicting a person not at risk, while in actual person is at risk of making a default 

### How to reduce this loss i.e need to reduce False Negatives ?
* Company wants Recall to be maximized, greater the recall lesser the chances of false negatives

### Business insights
* We could see that people owning their own house are less probable to default
* As the duration for which credit is taken increases, chances of default increases
* people in quite rich category of savings account has least chances of default, while people in little category of savings account are most probable to default

**So we could conclude that**
* Credit should be given for lesser durations(12 months or less), to people of age inbetween 34 and 57, owning a house, and belonging to rich/quite rich category of savings account  
