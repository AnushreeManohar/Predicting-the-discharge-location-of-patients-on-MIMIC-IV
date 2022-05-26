# Predicting the discharge location of patients on MIMIC-IV

### Overview

- Predicting the discharge location of patients on MIMIC-IV data using data from admission, patients and inputevents table.
- MIMIC-IV data contains information about real patients during their period of stay in the hospital including laboratory measurements, vitals documented, their demographics details and so on for the period from 2008 – 2019 in a relational database. 

### Pre-processing and Exploratory Data Analysis

- Discarded 126657 rows which had no discharge location specified.
- The target class was clearly imbalanced as most of the patients were discharged to home.
- Used SMOTE oversampling for imbalanced multi-label classification.

### Models and accuracies

- Decision Tree, Random Forest, KNN, Naive Bayes, Multinominal Naive Bayes, Logistic Regression and Gradient Boost models were built.
- The accuracies were only upto 45%. 
- Feature selection was performed using information gain and random forest where top features were identified to reduce size of the columns from over 500 to 40.
- However, there was no much improvisation in the accuracies, it raised only by 1%.
- ROC curve for multi-label classification was plotted which showed the auc for each of the target classes.
- SMOTE oversampling method was applied to get an even distribution of the target classes.
- There was a significant rise in the accuracies of decision tree, random forest and KNN models.
- Accuracies improved from 40's to 70's.
- Random forest was identified to be the best with an accuracy of 78.75%.

