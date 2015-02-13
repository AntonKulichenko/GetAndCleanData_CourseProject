# Course project for Getting and Cleaning Data course 
## Task: 
Create one R script called run_analysis.R that does the following:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

## Data Source
* the data for the project should be taken from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
* the description for the data is here http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Using the project
* Download the data from the source above.
* Unzip the data.
* Put the obtained `UCI HAR Dataset` folder into the working directory.
* Run the run_analysis.R script by executing `source("run_analysis.R")`.
* The resulting file `tidy.txt` will appear in `UCI HAR Dataset` folder.
