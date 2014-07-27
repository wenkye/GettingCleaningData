# Getting and Cleaning Data

## Course Project

The requirements are:
 - Merges the training and the test sets to create one data set.
 - Extracts only the measurements on the mean and standard deviation for each measurement
 - Uses descriptive activity names to name the activities in the data set
 - Appropriately labels the data set with descriptive activity names. 
 - Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
 
## Steps to run the code
datafile link https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
1. Download the data source and extract the zip file. The folder name should be UCI HAR Dataset.
2. Put the code run_analysis.R in the parent folder of UCI HAR Dataset, then set it as your working directory using ```setwd()``` function in RStudio. The folder structure should be something like this
```
 ---
  |
  |---run_analysis.R
  |
  |---UCI HAR Dataset/
```
3. Run ```source("run_analysis.R")```, then it will generate a new file ```tidysetdata.txt``` in your working directory.

## Dependencies

```run_analysis.R``` file will help you to install the dependencies automatically. It depends on ```reshape2``` and ```data.table```. 