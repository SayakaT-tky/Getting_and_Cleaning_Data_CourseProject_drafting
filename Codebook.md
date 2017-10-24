# Code book for Getting and Cleaning Data course project
The data file in this repository, tidydata.txt, is the file which this codebook connects to. It consists of 10299 rows and 68 columns, where the first row contains the variable names.

## Data
The data file "tidydata.txt" was created as a tidy data set through the project work cleaning the data source acquired from here: [UCI Machine learning project data](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

The original data source is a set of measurement of 6 activities performed by 30 individuals, which were obtained with smartphones. These data include:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration
- Triaxial Angular velocity from the gyroscope

The original data set is consists of training and test data. These data sets were cleaned as a tidy data set with the average of each variable for each activity and each subject. Transformation details are described in the next section ("Transformations"). 

## Transformations
The transformations made with the source data set through the project script(`run_analysis.R`) are as follows: 
#### Combine the original data set  
Step1: Merges the training and the test sets to create one data set.
#### Extract specific variables  
Step2: Extracts only the measurements on the mean and standard deviation for each measurement.
#### Alter the value labels and variable names  
Step3: Uses descriptive activity names to express each activities in the data set.  
Step4: Appropriately labels the data set with descriptive variable names.
#### Summarize the data  
Step5: From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.  
Step6: Outputs the result to "tidydata.txt".

## Variables
All measurements are normalized and bounded within [-1,1].
### Demensions
The acceleration signal from the smartphone accelerometer are recorded in standard gravity units 'g'.
The angular velocity vector measured by the gyroscope are recorded in radians per second.
### Identifiers
* `Activity`
The activity type performed by the individual, strings of either 6 values (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING).
* `Subject`
The ID of each individual subjects, integers ranging from 1 to 30.
### Measurement variables
All values for the measured variables are numeric, floating-point number. The variables are categorized into two types, time domain signals and frequency domain signals. 
#### 1. Time domain signals  
Time domain signals were captured with the accelerometers and gyroscopes and recorded as 3-axial raw signals. Variables of time domain signals have prefix 'TimeDomain' in its variable names.  
* `Acc`: Signals captured with the accelerometers  
* `Gyro`: Signals captured with the gyroscopes  
* `Body`: The body acceleration signals separated with a low pass Butterworth filter from the original acceleration signals  
* `Gravity`: The gravity acceleration signals separated with a low pass Butterworth filter from the original acceleration signals  
* `Jerk`: the body linear acceleration and angular velocity were derived in time to obtain Jerk signals
* `Magnitude`: the magnitude of these three-dimensional signals were calculated using the Euclidean norm
* `Mean`:  
* `StD`:  

#### 2. Frequency domain signals  
Frequency domain signals were calculated with Fast Fourier Transform (FFT) being applied to some of the time domain signal measurements. These are indicated in its variable name with prefix 'FrequencyDomain'.  

=================

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ
tGravityAcc-XYZ
tBodyAccJerk-XYZ
tBodyGyro-XYZ
tBodyGyroJerk-XYZ
tBodyAccMag
tGravityAccMag
tBodyAccJerkMag
tBodyGyroMag
tBodyGyroJerkMag
fBodyAcc-XYZ
fBodyAccJerk-XYZ
fBodyGyro-XYZ
fBodyAccMag
fBodyAccJerkMag
fBodyGyroMag
fBodyGyroJerkMag



