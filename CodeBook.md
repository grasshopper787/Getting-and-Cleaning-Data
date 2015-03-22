###Code Book

The R script "run_analysis.R" performs the following to clean up the data:

1. Merges the training and the test sets to create one data set. Merges ./train/X_train.txt with ./test/X_test.txt - the result of which is a 10299x561 data frame, as in the original description ("Number of Instances: 10299" and "Number of Attributes: 561"), train/subject_train.txt with test/subject_test.txt - the result of which is a 10299x1 data frame with subject IDs and train/y_train.txt with test/y_test.txt the result of which is also a 10299x1 data frame with activity IDs.

2. Reads features.txt and extracts only the measurements on the mean and standard deviation for each measurement. The result is a 10299x66 data frame, because only 66 out of 561 attributes are measurements on the mean and standard deviation.

3. Reads activity_labels.txt and applies descriptive activity names to name the activities in the data set:

walking

walkingupstairs

walkingdownstairs

sitting

standing

laying

All feature names (attributes) and activity names are converted to lower case, underscores and brackets () are removed. 

4. Appropriately labels the data set with descriptive activity names. Then it merges the 10299x66 data frame containing features with 10299x1 data frames containing activity labels and subject IDs. The result is saved as merged_clean_data.txt, a 10299x68 data frame such that the first column contains subject IDs, the second column activity names, and the last 66 columns are measurements. Subject IDs are integers between 1 and 30 inclusive.

5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject. The result is saved as cleaned_data_set_of_averages.txt, a 180x68 data frame, where as before, the first column contains subject IDs, the second column contains activity names, and then the averages for each of the 66 attributes are in columns 3:68. There are 30 subjects and 6 activities (180 rows) in this data set with averages.