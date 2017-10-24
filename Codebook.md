# Code book for Getting and Cleaning Data course project
This codebook connects to the data file `tidydata.txt` in this repository. It consists of *** rows and 68 columns, where the first row contains the variable names.

## Data
The data file `tidydata.txt` was created as a tidy data set through the project work with `run_analysis.R`, to clean the data source acquired from here: [UCI Machine learning project data](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

The original data source is a set of measurement of 6 activities performed by 30 individuals, which were obtained with smartphones. These data include:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration
- Triaxial angular velocity from the gyroscope

This original data set consists of training and test data sets. These data sets were cleaned as a tidy data set with the average of each variable for each activity and each subject. Transformation details are described in the next section ("Transformations"). 

## Transformations
The transformations made with the source data set through the project script(`run_analysis.R`) are as follows: 
#### Combine the original data set  
Step1: Merges the training and the test data sets to create one data set.
#### Extract specific variables  
Step2: Extracts only the variables on the means and standard deviations for each measurement.
#### Alter the value labels and variable names  
Step3: Applies descriptive activity names to values instead of factor numbers to express each activities in the data set.  
Step4: Appropriately labels the data set with descriptive variable names.
#### Summarize the data  
Step5: From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.  
Step6: Outputs and saves the result to 'tidydata.txt'.

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
Time domain signals were captured with the accelerometers and gyroscopes and recorded as 3-axial raw signals (represented with 'X','Y', and 'Z' at the end of variable names). Variables of time domain signals have prefix 'TimeDomain' in its variable names.  
* `Acc`: Signals captured with the accelerometers  
* `Gyro`: Signals captured with the gyroscopes  
* `Body`: The body acceleration signals separated with a low pass Butterworth filter from the original acceleration signals  
* `Gravity`: The gravity acceleration signals separated with a low pass Butterworth filter from the original acceleration signals  
* `Jerk`: Jerk signals obtained as a time derivative of the body linear acceleration and angular velocity
* `Magnitude`: The magnitude of the three-dimensional signals, which were calculated using the Euclidean norm
* `Mean`: The average of each measurement set
* `Std`: The stantdard deviation of each measurement set

#### 2. Frequency domain signals  
Frequency domain signals were calculated with Fast Fourier Transform (FFT) being applied to some of the time domain signal measurements. These are indicated in its variable name with prefix 'FrequencyDomain'. The abbreviations used in each variables are same as those used for time domain signals.


