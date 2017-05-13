# **Getting and Cleaning Data** course project
The purpose of this project is to collect, work with, and clean a data set. 

One of the most exciting areas in all of data science right now is wearable computing. Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. 
Through this project work, the open data set collected from the accelerometers from the Samsung Galaxy S smartphone was cleaned to finally obtain a new tidy data which can be used for later analysis. Details for the original data set is as written in the 'Data source' section below. 

This repository contains all files related to this project as follows:

* README.md: (This file) Describes what each files are for.
* Codebook.md: Describes the variables, the data, and any transformations made to clean up the data
* run_analysis.R: The R script used to clean up the data to achieve the objectives below:
1. Merge the training and the test sets to create one data set.
2. Extract only the measurements on the mean and standard deviation for each measurement.
3. Use descriptive activity names to name the activities in the data set
4. Appropriately label the data set with descriptive variable names.
5. Create a second, independent tidy data set with the average of each variable for each activity and each subject.
6. Finally output the result to a new file (tidy_data.txt).

# Data source 
A full description of the dataset is available at the original project website:
[UCI](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

===
The experiments have been carried out with a group of 30 volunteers. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

===
# Environments
This project was done with:
* Windows 7 SP1 64-bit
* R version 3.3.3
* Rstudio 1.0.136
* R packages: dplyr 0.5.0; reshape2 1.4.2
