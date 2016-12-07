#Getting and Cleaning Data Course Assignment #1
##(README)

###Summary
This document describes design and use of **run_analysis()** function which was developed as part of course's programing assignment.

###Steps to run **run_analysis()**
1. Download R script and data from GitHub [mproekt1/data_science_getting_and_cleaning_data_PrAss1](https://github.com/mproekt1/data_science_getting_and_cleaning_data_PrAss1.git) repo.
2. It is preffered to use **RStudio** to run the code.
3. Install and load **dplyr** package.
4. Make sure that data directory **/UCI HAR Dataset** exists in the same directory as the script **run_analysis.R**.
5. Load **run_analysis.R** script using **source()** function.
6. Call function **run_analysis()** (omit input parameters)

###Design notes

####Directory sctructure
The script **run_analysis.R** expects to find data in the same directory. There is a code in the script that determines location of the script file and checks to see if the data directory **/UCI HAR Dataset** is present in the same location. If one or more data files are missing, the script will throw an error. The data directory has the following structure and files:

Directory / File | File description
---------------------------------------------------------------|-----------------------------------------------------------
_[current script directory]_/**UCI HAR Dataset/activity_labels.txt**| contains translations of activities' numeric codes
_[current script directory]_/**UCI HAR Dataset/features.txt**| contains names of the features (variables) in test and train data files.
_[current script directory]_/**UCI HAR Dataset/train/X_train.txt**| contains observations from **training** set. Each record represents a single observation. Each column represents a single feature (variable) which corresponds to an item in **features.txt**.
_[current script directory]_/**UCI HAR Dataset/train/y_train.txt**| contains a list of activity codes from **training** set. Each record represents an activity code that corresponds to an observation in **X_train.txt** with the same row number.
_[current script directory]_/**UCI HAR Dataset/train/subject_train.txt**| contains a list of subject codes from **training** set. Each record represents a subject code that corresponds to an observation in **X_train.txt** with the same row number.
_[current script directory]_/**UCI HAR Dataset/test/X_test.txt**| contains observations from **test** set. Each record represents a single observation. Each column represents a single feature (variable) which corresponds to an item in **features.txt file**.
_[current script directory]_/**UCI HAR Dataset/test/y_test.txt**| contains a list of activity codes from **test** set. Each record represents an activity code that corresponds to an observation in **X_test.txt** with the same row number.
_[current script directory]_/**UCI HAR Dataset/test/subject_test.txt**| contains a list of subject codes from **test** set. Each record represents a subject code that corresponds to an observation in **X_test.txt** with the same row number.



####run_analysis() function

**run_analysis()** has following declaration:  
```
run_analysis <- function(max_rows = -1)
```
where input paramter **max_rows** sets the maximum number of records from the data files to be returned. It's useful to limit the number of returned records during testing. 

max_rows value | return value
-------------------------|------------------------------------------------------------------------
**positive integer** | Sets the maximum number of records to be read from **training** and **test** data files. Does not effect number of records read from **activity_labels.txt** and **features.txt**. These two files will be read in its entirety. 
**0** or **negative** | The function reads all records from all data files.

Upon completion, the function will generate two files in the same directory as the script:  

File Name | Description
------------------------|-----------------------------------------------------------------
**clean_data.txt** | Contains **_clean_** data, that is data which was put through the filteres descibed in the assignment. Each record contains a single observation (no summarisation).
**summarised_data.txt** | Contains summarised data from **clean_data.txt** groupped by **subjectID** and **activityName** variables.
