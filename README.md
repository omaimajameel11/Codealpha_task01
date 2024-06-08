# Codealpha_task01
# Titanic Classification

## Overview

The Titanic Survival Prediction System is a machine learning model designed to predict the likelihood of a passenger surviving the sinking of the Titanic. This README file outlines the factors considered, the data preprocessing steps, and the methodology used to train and evaluate the model.

## Key Factors Affecting Survival

The following factors were considered as predictors for the survival of passengers:

1. **Socio-Economic Status (SES)**
   - **Pclass**: Ticket class (1st, 2nd, 3rd)
     - 1st class passengers had a higher chance of survival compared to 2nd and 3rd class passengers.

2. **Gender**
   - **Sex**: Male or Female
     - Females had a higher likelihood of survival compared to males.

3. **Age**
   - **Age**: Age of the passenger
     - Younger passengers had a higher survival rate.

4. **Family Size**
   - **SibSp**: Number of siblings/spouses aboard
   - **Parch**: Number of parents/children aboard
     - Passengers with smaller family sizes had a higher chance of survival.

5. **Fare**
   - **Fare**: Ticket fare
     - Higher fares were associated with higher survival chances.

6. **Embarked**
   - **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)
     - Passengers who embarked from Cherbourg had a higher survival rate.

## Data Preprocessing

1. **Handling Missing Values**
   - Imputed missing values for the `Age` column using the median age.
   - Filled missing values in the `Embarked` column with the most common embarkation point.
   - Replaced missing values in the `Fare` column with the median fare.

2. **Encoding Categorical Variables**
   - Converted categorical variables (`Sex`, `Embarked`) into numerical format using one-hot encoding.

3. **Feature Scaling**
   - Applied scaling to continuous variables (`Age`, `Fare`) to normalize the data.

## Model Training and Evaluation

1. **Model Selection**
   - Several machine learning algorithms were evaluated, including Logistic Regression, Decision Trees, Random Forests, and Support Vector Machines (SVM).

2. **Cross-Validation**
   - Used cross-validation to ensure the model's robustness and to tune hyperparameters.

3. **Performance Metrics**
   - Evaluated the model using accuracy, precision, recall, and the F1-score.

4. **Final Model**
   - Selected the model with the best performance metrics and tested it on a hold-out test set to ensure generalizability.

## Usage

1. **Input Features**
   - The system requires the following input features to make a prediction:
     - Pclass (1, 2, or 3)
     - Sex (Male or Female)
     - Age (numerical value)
     - SibSp (number of siblings/spouses aboard)
     - Parch (number of parents/children aboard)
     - Fare (numerical value)
     - Embarked (C, Q, or S)

2. **Output**
   - The system outputs a binary prediction:
     - 1: The passenger is predicted to survive.
     - 0: The passenger is predicted not to survive.

## Conclusion

The Titanic Survival Prediction System leverages socio-economic status, gender, age, family size, fare, and port of embarkation to predict the survival of passengers. By understanding and analyzing these factors, the model aims to provide accurate survival predictions based on historical data.

