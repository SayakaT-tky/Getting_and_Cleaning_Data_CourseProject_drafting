# Code book for Getting and Cleaning Data course project
The data file in this repository, tidydata.txt, is the file which this codebook connects to. It consists of 10299 rows and 81 columns, where the first row contains the variable names.

## Data
The data file "tidydata.txt" was created as a tidy data set through the project work cleaning the data source acquired from the URL below:
<https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip>

The original data source is a set of measurement of 6 activities performed by 30 individuals, which were obtained with smartphones. These data include:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration
- Triaxial Angular velocity from the gyroscope

The original data set is consists of training and test data. These data sets were cleaned as a tidy data set with the average of each variable for each activity and each subject. Transformation details are described in the next section ("Transformations"). 

## Transformations
The transformations made with the source data set through this course project are as follows: 
* Combining the original data set

Step1: Merges the training and the test sets to create one data set.
* Variable selection

Step2: Extracts only the measurements on the mean and standard deviation for each measurement.
* Alteration of the variable names

Step3: Uses descriptive activity names to name the activities in the data set.
Step4: Appropriately labels the data set with descriptive variable names.
* Summarize the data

Step5: From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Step6: Output the result to "tidydata.txt".

## Variables
All measurements are normalized and bounded within [-1,1].
### Demensions
The acceleration signal from the smartphone accelerometer are recorded in standard gravity units 'g'.
The angular velocity vector measured by the gyroscope are recorded in radians per second.
### Identifiers
* 'Activity'
The activity type performed by the individual  
* Subject
The ID of each individual subjects, integers ranging from 1 to 30.
### Variables

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

The set of variables that were estimated from these signals are: 

mean(): Mean value
std(): Standard deviation
mad(): Median absolute deviation 
max(): Largest value in array
min(): Smallest value in array
sma(): Signal magnitude area
energy(): Energy measure. Sum of the squares divided by the number of values. 
iqr(): Interquartile range 
entropy(): Signal entropy
arCoeff(): Autorregresion coefficients with Burg order equal to 4
correlation(): correlation coefficient between two signals
maxInds(): index of the frequency component with largest magnitude
meanFreq(): Weighted average of the frequency components to obtain a mean frequency
skewness(): skewness of the frequency domain signal 
kurtosis(): kurtosis of the frequency domain signal 
bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
angle(): Angle between to vectors.

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:

gravityMean
tBodyAccMean
tBodyAccJerkMean
tBodyGyroMean
tBodyGyroJerkMean

The complete list of variables of each feature vector is available in 'features.txt'


