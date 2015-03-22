#Getting and Cleaning Data
This file describing how the script for "Getting and Cleaning Data" course works.
 
##Course Project

1. Unzip the source (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) into a folder on your local work directory. For example (C:/Users/yourname/Desktop/Coursera).

2. Put run_analysis.R into (C:/Users/yourname/Desktop/Coursera/UCI HAR Dataset).

3. Starts RStudio and then
   setwd("C:/Users/yourname/Desktop/Coursera/UCI HAR Dataset"); source("run_analysis.R").

4. The result "data" table has provided by script "run_analysis.R" containes 180 rows (30 subjects and 6 activities for each activity and each subject) and 68 columns.

5. The script "run_analysis.R" creates file "cleaned_data_set_of_averages.txt", that contains result data. 

