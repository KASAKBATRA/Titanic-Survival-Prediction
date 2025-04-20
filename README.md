# Titanic-Survival-Prediction
This project uses machine learning to predict whether a passenger survived the Titanic disaster based on features like age, gender, ticket class, and fare. It includes data preprocessing, feature engineering, model training, and performance evaluation.
_______________________________________________________________________________________________________________________________________________________

## Dataset

The dataset is sourced from the famous 
[Titanic dataset on Kaggle](https://www.kaggle.com/c/titanic/data)]
It includes:

- `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- `Sex`: Gender of the passenger
- `Age`: Age in years
- `SibSp`: Number of siblings/spouses aboard
- `Parch`: Number of parents/children aboard
- `Fare`: Passenger fare
- `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

_________________________________________________________________________________________________
## Features

- Preprocessing missing values
- Label and one-hot encoding for categorical variables
- Feature scaling with `StandardScaler`
- Model training using `RandomForestClassifier`
- Evaluation with accuracy, precision, recall, F1-score, and confusion matrix

___________________________________________________________________________________________________

# Code Explanation 

Data manipulation (pandas, numpy)
Preprocessing (StandardScaler)
Model training (RandomForestClassifier)
Model evaluation (accuracy_score, etc.)

# preprocessing 
Missing Age and Fare values are filled with the median.
Missing Embarked values are filled with the most common port.
Cabin is dropped because it has too many missing values.

# feature engineering 
Converts Sex into numerical values (male = 0, female = 1)
One-hot encodes Embarked and removes the first column to avoid dummy trap.
Drops unused columns: Name, Ticket, PassengerId.

# Prepare data 
X: input features
y: target (Survived)
StandardScaler: normalizes Age and Fare for better model performance
Data is split into 80% training and 20% testing

# modeling 
A Random Forest Classifier is used.
It's trained on the training data.

# evaluation

Evaluates the model with:
Accuracy: Overall correctness
Precision: Correct positives out of predicted positives
Recall: Correct positives out of actual positives
F1 Score: Balance between precision and recall
Classification report: Detailed breakdown
Confusion matrix: Matrix showing TP, FP, FN, TN


