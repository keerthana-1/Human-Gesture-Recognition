# Human Gesture Recognition using timeseries data

# Phase 1:

- Read and Process Training Data:
1. Initializes an empty DataFrame final_df.
2. Loops through 24 dimensions (assumed from the naming convention of the files).
3. Reads each .arff file for training data, converts it to a DataFrame, and extends the data into a list.
4. Combines data from all dimensions into a single DataFrame final_df.
5. Adds class attribute and a column to indicate training data.
   
- Read and Process Test Data: Similar process as for the training data, but reads test data files and stores the result in final_df1.
   
- Combine Train and Test Data:
1. Concatenates the training and test DataFrames.
2. Adds an id column for indexing.
3. Reorders columns to have id at the beginning.
   
- Save to CSV: Saves the combined DataFrame to a CSV file.
