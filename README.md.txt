Getting and Cleaning Data
This project is the final assignment of Coursera's "Getting and Cleaning Data" course.

Goal
As described in the assignment page:

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.

Data Science Topic
Again, let us quote the assignment page here:

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone.

Material
Data description:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Non-precessed data:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Tasks
Again, according to the course assignment:

You should create one R script called run_analysis.R that does the following:

Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Way the tasks are handled:
The file run_analysis.R, which intends to get the data and clean it, addresses the tasks in pretty much the same order. We first collect the X training and testing sets (X_train.txt and X_test.txt) and merge them together, we then do the same for the Y training and testing sets (Y_train.txt and Y_test.txt), which consists of dataframes with only one column. We then obtain the names of the columns from features.txt. We make sure the sets have compatible dimensions. We add the names to the X and Y dataframes. We also read the activity labels from activity_labels.txt and apply them to the Y dataframe. We finally combine dataframes X and Y together, calling it data. We simplify slightly the names of columns in the data dataframe and group the rows by categories of activity. We then export the dataframe data to a text file.

Features:
Refer to the Code Book.