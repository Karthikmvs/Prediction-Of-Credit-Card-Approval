# Credit Card Approval Prediction

## Overview

The primary objective of this project is to predict the approval or rejection of credit card applications using machine learning. The challenge lies in understanding the key factors influencing credit card approval decisions and building a predictive model to assist in the decision-making process.

## Steps Involved

1. **Exploratory Data Analysis (EDA)**
2. **Feature Engineering**
3. **Data Preprocessing**
4. **Model Development**
5. **Model Evaluation**
6. **Recommendations**

## Dataset Overview

The dataset contains the following columns:
- `ID`: Unique identifier for each record.
- `Gender`: Gender of the applicant.
- `Has a car`: Indicates whether the applicant owns a car (binary: 0 or 1).
- `Has a property`: Indicates whether the applicant owns a property (binary: 0 or 1).
- `Children count`: Number of children the applicant has.
- `Income`: Income of the applicant.
- `Employment status`: Employment status of the applicant.
- `Education level`: Highest education level attained by the applicant.
- `Marital status`: Marital status of the applicant.
- `Dwelling`: Type of dwelling the applicant resides in.
- `Age`: Age of the applicant.
- `Employment length`: Duration of the applicant's current employment.
- `Has a mobile phone`: Indicates whether the applicant has a mobile phone (binary: 0 or 1).
- `Has a work phone`: Indicates whether the applicant has a work phone (binary: 0 or 1).
- `Has a phone`: Indicates whether the applicant has any phone (binary: 0 or 1).
- `Has an email`: Indicates whether the applicant has an email (binary: 0 or 1).
- `Job title`: Title or position of the applicant's job.
- `Family member count`: Number of family members.
- `Account age`: Age of the applicant's account.
- `Is high risk`: Whether the applicant is considered high risk (0 for no, 1 for yes).

## Exploratory Data Analysis (EDA)

### Univariate Analysis
- Distribution of numerical features using histograms.

### Bivariate Analysis
- Boxplots of numerical features against the target variable.
- Countplots of categorical features against the target variable.

## Feature Engineering

### New Features Created
- `Income per Family Member`: Income / (Family member count + 1)
- `Has a Phone`: Combined mobile, work, and any phone.

### Dropped Original Phone Features
- `Has a mobile phone`, `Has a work phone`, `Has a phone`

## Data Preprocessing

### Handling Missing Values
- Numerical columns filled with median values.
- Categorical columns filled with mode values.

### Encoding Categorical Variables
- One-hot encoding applied.
- Ensured both train and test data have the same columns.

### Scaling Numerical Features
- StandardScaler used for numerical features.

## Model Development

### Models Trained
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting

### Metrics Used
- Accuracy
- Precision
- Recall
- F1-score
- ROC AUC
- Confusion Matrix

## Model Evaluation

### Model Comparison

**Logistic Regression:**
- Accuracy: 0.984
- Precision: 1.0
- Recall: 0.017
- F1-score: 0.034
- ROC AUC: 0.509


**Random Forest:**
- Accuracy: 0.982
- Precision: 0.340
- Recall: 0.137
- F1-score: 0.195
- ROC AUC: 0.566


**Gradient Boosting:**
- Accuracy: 0.984
- Precision: 0.462
- Recall: 0.051
- F1-score: 0.092
- ROC AUC: 0.525


## Best Model Selection

**Chosen Model: Random Forest**
- **Reason:** Reasonable balance between precision (0.340) and recall (0.137).


## Feature Importance

### Top 10 Important Features
- Income
- Employment status
- Age
- Account age
- Family member count
- Marital status
- Education level
- Dwelling
- Job title
- Income per Family Member

## Recommendations

1. Focus on applicants' income and employment status when evaluating credit card applications.
2. Consider the applicant's age and account age as significant factors in the decision-making process.
3. Prioritize applicants with stable employment and higher income per family member.
4. Pay attention to applicants' marital status and number of family members.
5. Enhance data collection for job titles and dwelling types to improve model performance.

## Conclusion

This project demonstrates the use of machine learning to predict credit card approval. By carefully analyzing the data, engineering new features, preprocessing the data, and training various models, we can make informed decisions that enhance the credit card approval process.

## Files in Repository

- `train_data.csv`: Training dataset.
- `test_data.csv`: Test dataset.
- `credit_card_approval.ipynb`: Jupyter notebook containing the complete code for the project.
- `Credit_Card_Approval_Prediction_Presentation.pptx`: PowerPoint presentation summarizing the project.
- `README.md`: This file.
