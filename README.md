# Getting-and-Cleaning-Data-Week-4-Assignment


## Purpose
Used for the week 4 of Getting and Cleaning Data Coursera course.

## Instructions
* Download from (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) 
and unzip the data file into your R working directory.
* Second, download the R source code into the same directory.
* Finally, execute R source code to generate tidy data file.

## Data description
The variables in the data X are sensor signals measured with waist-mounted smartphone from 30 subjects. The variable in the data Y 
indicates activity type the subjects performed during recording. 
See http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones for further details.

## Code explanation
The code combines training dataset and test dataset, and produces a dataset with the averages of each variable for each activity.

## Generated dataset
Generated dataset contains variables calculated based on the mean and standard deviation based on each row from all 30 subjects.

## Exercise instructions
1. Merges the training and the test sets to create one data set.
Use command rbind to combine training and test set
2. Extracts only the measurements on the mean and standard deviation for each measurement.
Use grep command to get column indexes for variable name contains "mean()" or "std()"
3. Uses descriptive activity names to name the activities in the data set
Convert activity labels to characters and add a new column as factor
4. Appropriately labels the data set with descriptive variable names.
Give the selected descriptive names to variable columns
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Use pipeline command to create a new tidy dataset with command group_by and summarize_each in dplyr package
