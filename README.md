# Human Gesture Recognition using timeseries data

## Phase 1:

1. Read and Process Training Data:
- Initializes an empty DataFrame final_df.
- Loops through 24 dimensions (assumed from the naming convention of the files).
- Reads each .arff file for training data, converts it to a DataFrame, and extends the data into a list.
- Combines data from all dimensions into a single DataFrame final_df.
- Adds class attribute and a column to indicate training data.
   
2. Read and Process Test Data: Similar process as for the training data, but reads test data files and stores the result in final_df1.
   
3. Combine Train and Test Data:
- Concatenates the training and test DataFrames.
- Adds an id column for indexing.
- Reorders columns to have id at the beginning.
   
4. Save to CSV: Saves the combined DataFrame to a CSV file.

## Phase 2:

- Read the NATOPS_sid_TRAIN.csv file saved from phase1.
- Perform KMeans clustering on the features for each unique sid.
- Calculate the cluster ratios for each sample.
- Merge these ratios back with the original dataset.
- Save the final DataFrame to a CSV file.

## Phase 3:

Training and evaluating multple classification models

1. K-Nearest Neighbors (KNN)

Test Accuracy: 0.66
Cross-Validation Accuracy: ~0.98

2. Logistic Regression

Test Accuracy: 0.68
Cross-Validation Accuracy: ~0.75

3. Random Forest

Test Accuracy: 0.66
Cross-Validation Accuracy: ~0.98

4. Support Vector Machine (SVM)

Test Accuracy: 0.62
Cross-Validation Accuracy: ~0.87

5. Multi-Layer Perceptron (MLP)

Test Accuracy: 0.63
Cross-Validation Accuracy: ~0.97

6. Ensemble Classifier

Test Accuracy: 0.68
Cross-Validation Accuracy: ~0.97
