#Getting and Cleaning Data Course Assignment #1
##(Code Book)

###Summary
This document describes the structure and the content of **run_analysis()** output files **clean_data.txt** and **summarised_data.txt**.

<br>
<br>

###clean_data.txt

####Format
+ ASCII-text
+ Space-delimited
+ The text qualifier is " (double quote)
+ The first row contains column headers.
+ Total number of columns 68
+ Total number of rows (including header) 10300

<br>
<br>

####Data
+ The file combines **training** and **test** data sets.
+ Each record represents an individual observation form either **training** or **test** data sets.
+ The column names appear as defined in **features.txt** file.
+ The columns are limited to **mean** and **std** variables as describen in Prog. Assignment.

<br>
<br>

####Dictionary
Column / Variable | Description
-------------------------------|-----------------------------------------------------------------------------------
subjectID | An integer code that identifies and individual subject.
activityName | A string that describes the type of activity. (see list of activities table below)
tBodyAcc-mean()-X | The remaining columns correspond to **mean** and **std** features (measurments) as described in Prog. Assignment. 
tBodyAcc-mean()-Y |
tBodyAcc-mean()-Z |
tGravityAcc-mean()-X |
tGravityAcc-mean()-Y |
tGravityAcc-mean()-Z |
tBodyAccJerk-mean()-X |
tBodyAccJerk-mean()-Y |
tBodyAccJerk-mean()-Z |
tBodyGyro-mean()-X |
tBodyGyro-mean()-Y |
tBodyGyro-mean()-Z |
tBodyGyroJerk-mean()-X |
tBodyGyroJerk-mean()-Y |
tBodyGyroJerk-mean()-Z |
tBodyAccMag-mean() |
tGravityAccMag-mean() |
tBodyAccJerkMag-mean() |
tBodyGyroMag-mean() |
tBodyGyroJerkMag-mean() |
fBodyAcc-mean()-X |
fBodyAcc-mean()-Y |
fBodyAcc-mean()-Z |
fBodyAccJerk-mean()-X |
fBodyAccJerk-mean()-Y |
fBodyAccJerk-mean()-Z |
fBodyGyro-mean()-X |
fBodyGyro-mean()-Y |
fBodyGyro-mean()-Z |
fBodyAccMag-mean() |
fBodyBodyAccJerkMag-mean() |
fBodyBodyGyroMag-mean() |
fBodyBodyGyroJerkMag-mean() |
tBodyAcc-std()-X |
tBodyAcc-std()-Y |
tBodyAcc-std()-Z |
tGravityAcc-std()-X |
tGravityAcc-std()-Y |
tGravityAcc-std()-Z |
tBodyAccJerk-std()-X |
tBodyAccJerk-std()-Y |
tBodyAccJerk-std()-Z |
tBodyGyro-std()-X |
tBodyGyro-std()-Y |
tBodyGyro-std()-Z |
tBodyGyroJerk-std()-X |
tBodyGyroJerk-std()-Y |
tBodyGyroJerk-std()-Z |
tBodyAccMag-std() |
tGravityAccMag-std() |
tBodyAccJerkMag-std() |
tBodyGyroMag-std() |
tBodyGyroJerkMag-std() |
fBodyAcc-std()-X |
fBodyAcc-std()-Y |
fBodyAcc-std()-Z |
fBodyAccJerk-std()-X |
fBodyAccJerk-std()-Y |
fBodyAccJerk-std()-Z |
fBodyGyro-std()-X |
fBodyGyro-std()-Y |
fBodyGyro-std()-Z |
fBodyAccMag-std() |
fBodyBodyAccJerkMag-std() |
fBodyBodyGyroMag-std() |
fBodyBodyGyroJerkMag-std() |

<br>
<br>

###summarised_data.txt

####Format
+ ASCII-text
+ Space-delimited
+ The text qualifier is " (double quote)
+ The first row contains column headers.
+ Total number of columns 68
+ Total number of rows (including header) 181

<br>
<br>

####Data
+ The file contains an aggregated data from **clean_data.txt** file.
+ The column names appear as defined in **features.txt** file with "MEAN of" prefix.
+ The columns are means of feaures (measurments) groupped by **subjectID** and **activityName**.

<br>
<br>

####Dictionary
Column / Variable | Description
--------------------------------------|-----------------------------------------------------------------------------------
subjectID | An integer code that identifies and individual subject.
activityName | A string that describes the type of activity. (see list of activities table below)
MEAN of tBodyAcc-mean()-X | The remaining columns contain means of features (measurments) as described in Prog. Assignment.
MEAN of tBodyAcc-mean()-Y |
MEAN of tBodyAcc-mean()-Z |
MEAN of tGravityAcc-mean()-X |
MEAN of tGravityAcc-mean()-Y |
MEAN of tGravityAcc-mean()-Z |
MEAN of tBodyAccJerk-mean()-X |
MEAN of tBodyAccJerk-mean()-Y |
MEAN of tBodyAccJerk-mean()-Z |
MEAN of tBodyGyro-mean()-X |
MEAN of tBodyGyro-mean()-Y |
MEAN of tBodyGyro-mean()-Z |
MEAN of tBodyGyroJerk-mean()-X |
MEAN of tBodyGyroJerk-mean()-Y |
MEAN of tBodyGyroJerk-mean()-Z |
MEAN of tBodyAccMag-mean() |
MEAN of tGravityAccMag-mean() |
MEAN of tBodyAccJerkMag-mean() |
MEAN of tBodyGyroMag-mean() |
MEAN of tBodyGyroJerkMag-mean() |
MEAN of fBodyAcc-mean()-X |
MEAN of fBodyAcc-mean()-Y |
MEAN of fBodyAcc-mean()-Z |
MEAN of fBodyAccJerk-mean()-X |
MEAN of fBodyAccJerk-mean()-Y |
MEAN of fBodyAccJerk-mean()-Z |
MEAN of fBodyGyro-mean()-X |
MEAN of fBodyGyro-mean()-Y |
MEAN of fBodyGyro-mean()-Z |
MEAN of fBodyAccMag-mean() |
MEAN of fBodyBodyAccJerkMag-mean() |
MEAN of fBodyBodyGyroMag-mean() |
MEAN of fBodyBodyGyroJerkMag-mean() |
MEAN of tBodyAcc-std()-X |
MEAN of tBodyAcc-std()-Y |
MEAN of tBodyAcc-std()-Z |
MEAN of tGravityAcc-std()-X |
MEAN of tGravityAcc-std()-Y |
MEAN of tGravityAcc-std()-Z |
MEAN of tBodyAccJerk-std()-X |
MEAN of tBodyAccJerk-std()-Y |
MEAN of tBodyAccJerk-std()-Z |
MEAN of tBodyGyro-std()-X |
MEAN of tBodyGyro-std()-Y |
MEAN of tBodyGyro-std()-Z |
MEAN of tBodyGyroJerk-std()-X |
MEAN of tBodyGyroJerk-std()-Y |
MEAN of tBodyGyroJerk-std()-Z |
MEAN of tBodyAccMag-std() |
MEAN of tGravityAccMag-std() |
MEAN of tBodyAccJerkMag-std() |
MEAN of tBodyGyroMag-std() |
MEAN of tBodyGyroJerkMag-std() |
MEAN of fBodyAcc-std()-X |
MEAN of fBodyAcc-std()-Y |
MEAN of fBodyAcc-std()-Z |
MEAN of fBodyAccJerk-std()-X |
MEAN of fBodyAccJerk-std()-Y |
MEAN of fBodyAccJerk-std()-Z |
MEAN of fBodyGyro-std()-X |
MEAN of fBodyGyro-std()-Y |
MEAN of fBodyGyro-std()-Z |
MEAN of fBodyAccMag-std() |
MEAN of fBodyBodyAccJerkMag-std() |
MEAN of fBodyBodyGyroMag-std() |
MEAN of fBodyBodyGyroJerkMag-std() |

<br>
<br>

###Activities
Activities are stored in **y_<train|test>.txt** files as integer codes. The codes translation is provided by **activity_labels.txt**.

Activity Code | Activity Name
--------------|--------------------
1 | WALKING
2 | WALKING_UPSTAIRS
3 | WALKING_DOWNSTAIRS
4 | SITTING
5 | STANDING
6 | LAYING
