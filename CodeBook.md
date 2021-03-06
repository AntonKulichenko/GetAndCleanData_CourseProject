# Code Book for Course project

The code book describes the variables, the data, and any transformations or work performed to clean up the data.

## Data Source
* the data for the project should be taken from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
* the description for the data is here http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Information about data

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

### For each record it is provided:

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

### The dataset includes the following files:

- `README.txt`

- `features_info.txt`: Shows information about the variables used on the feature vector.

- `features.txt`: List of all features.

- `activity_labels.txt`: Links the class labels with their activity name.

- `train/subject_train.txt`: Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

- `train/X_train.txt`: Training set.

- `train/y_train.txt`: Training labels.

- `train/Inertial Signals` folder: not used in this task

- `test/subject_train.txt`: Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

- `test/X_test.txt`: Test set.

- `test/y_test.txt`: Test labels.

- `test/Inertial Signals` folder: not used in this task

## Data processing steps

* The data from data files is read into corresponding data frames.
* Appropriate column headers are added.
* Train and test datasets are merged.
* Necessary columns (containing `mean` or `std`) are left and the rest are deleted.
* The activity column is converted from integer into vector.
* Tidy dataset is created and saved to `tidy.txt`.