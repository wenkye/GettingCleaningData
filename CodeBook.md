# CodeBook

Description: a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md.

## The data source

* Original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
* Original description of the dataset: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Assumptions
It is assumed that the Samsung data is unzipped into the working directory. The data therefore resides in the same folder as `run_analysis.R`

In other words, it should be like this:
```
 ---
  |
  |---run_analysis.R
  |
  |---UCI HAR Dataset/
```

## Transformations I have performed to clean up the data

```activity_labels``` contains all the data from activity_labels.txt
```features```  contains all the data from features.txt
```extract_features```  extract only the measuresments for mean and standard deviation 
```X_test_data``` contains all the test data from x_test.txt
```y_test_data```  contains all the data from y_test.txt

The run_analysis.R that does the following. 

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

## How ```run_analysis.R``` implements the above steps:

* Require ```reshapre2``` and ```data.table``` librareis.
* Load both test and train data
* Load the features and activity labels.
* Extract the mean and standard deviation column names and data.
* Process the data. There are two parts processing test and train data respectively.
* Merge data set.