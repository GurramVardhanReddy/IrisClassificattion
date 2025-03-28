# IrisClassification

## Preprocessing Details
### Loading the Data:
The dataset is loaded using pd.read_csv() from a local path. The dataset appears to be the Iris dataset, which is a common dataset for classification tasks.
The dataset is stored in a Pandas DataFrame named df.
### Inspecting the Data:
df.head() is used to display the first few rows of the dataset to get an idea of its structure.
df.info() provides information about the dataset, including the number of rows, columns, data types, and missing values.
### Feature and Target Separation:
The features (independent variables) are stored in x by dropping the "Species" column from the DataFrame.
The target variable (dependent variable) is stored in y, which is the "Species" column.
### Train-Test Split:
The dataset is split into training and testing sets using train_test_split with a test size of 20% and a random state of 20.
This ensures that the data is divided into training and testing sets in a reproducible manner.

## Model Selection
Three different models are selected for training and evaluation:
### Decision Tree Classifier:
DecisionTreeClassifier(criterion="gini", max_depth=10, min_samples_split=2)
This model uses the Gini impurity criterion for splitting nodes, has a maximum depth of 10, and requires at least 2 samples to split an internal node.
### Bagging Classifier:
BaggingClassifier(n_estimators=20)
This model uses bagging to combine the predictions of 20 base estimators (decision trees by default).
### Random Forest Classifier:
RandomForestClassifier(n_estimators=20)
This model is an ensemble learning method that builds multiple decision trees and merges them to get a more accurate and stable prediction.

## Results
The code evaluates the performance of each model on both the training and testing sets. Here's a summary of the results:
DecisionTreeClassifier(max_depth=10)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00        42
Iris-versicolor       1.00      1.00      1.00        39
 Iris-virginica       1.00      1.00      1.00        39

       accuracy                           1.00       120
      macro avg       1.00      1.00      1.00       120
   weighted avg       1.00      1.00      1.00       120

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
BaggingClassifier(n_estimators=20)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00        42
Iris-versicolor       1.00      1.00      1.00        39
 Iris-virginica       1.00      1.00      1.00        39

       accuracy                           1.00       120
      macro avg       1.00      1.00      1.00       120
   weighted avg       1.00      1.00      1.00       120

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
RandomForestClassifier(n_estimators=20)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00        42
Iris-versicolor       1.00      1.00      1.00        39
 Iris-virginica       1.00      1.00      1.00        39

       accuracy                           1.00       120
      macro avg       1.00      1.00      1.00       120
   weighted avg       1.00      1.00      1.00       120

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

DecisionTreeClassifier(max_depth=10)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00        42
Iris-versicolor       1.00      1.00      1.00        39
 Iris-virginica       1.00      1.00      1.00        39

       accuracy                           1.00       120
      macro avg       1.00      1.00      1.00       120
   weighted avg       1.00      1.00      1.00       120

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
BaggingClassifier(n_estimators=20)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00        42
Iris-versicolor       1.00      1.00      1.00        39
 Iris-virginica       1.00      1.00      1.00        39

       accuracy                           1.00       120
      macro avg       1.00      1.00      1.00       120
   weighted avg       1.00      1.00      1.00       120

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
RandomForestClassifier(n_estimators=20)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00        42
Iris-versicolor       1.00      1.00      1.00        39
 Iris-virginica       1.00      1.00      1.00        39

       accuracy                           1.00       120
      macro avg       1.00      1.00      1.00       120
   weighted avg       1.00      1.00      1.00       120

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
DecisionTreeClassifier(max_depth=10)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00         8
Iris-versicolor       1.00      1.00      1.00        11
 Iris-virginica       1.00      1.00      1.00        11

       accuracy                           1.00        30
      macro avg       1.00      1.00      1.00        30
   weighted avg       1.00      1.00      1.00        30

1.0
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
BaggingClassifier(n_estimators=20)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00         8
Iris-versicolor       1.00      1.00      1.00        11
 Iris-virginica       1.00      1.00      1.00        11

       accuracy                           1.00        30
      macro avg       1.00      1.00      1.00        30
   weighted avg       1.00      1.00      1.00        30

1.0
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
RandomForestClassifier(n_estimators=20)
                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00         8
Iris-versicolor       1.00      1.00      1.00        11
 Iris-virginica       1.00      1.00      1.00        11

       accuracy                           1.00        30
      macro avg       1.00      1.00      1.00        30
   weighted avg       1.00      1.00      1.00        30

1.0
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
