1) Download the dataset
2) Assign each data in each file to variables
	features <- features.txt : List of activities performed when the corresponding measurements were taken and its codes (labels)
	subject_test <- test/subject_test.txt : contains test data of 9/30 volunteer test subjects being observed
	x_test <- test/X_test.txt : contains recorded features test data
    y_test <- test/y_test.txt : contains test data of activities’code labels
    subject_train <- test/subject_train.txt : contains train data of 21/30 volunteer subjects being observed
	x_train <- test/X_train.txt : contains recorded features train data
	y_train <- test/y_train.txt : contains train data of activities’code labels
3) Merge training and test sets to create one dataset: rbind x_test and x_train also rbind y_test and y_train
   aslo rbind subject_test and subject_train then cbind the last 3
4) Extract only measurements of mean & std
5) Use descriptive activity names: replace the code numbers with its corresponding activity taken from activities variables
6) Label the dataset with descriptive names
	Code column in TidyData renamed into activities
	All Acc in column’s name replaced by Accelerometer
	All Gyro in column’s name replaced by Gyroscope
	All BodyBody in column’s name replaced by Body
	All Mag in column’s name replaced by Magnitude
	All start with character f in column’s name replaced by Frequency
	All start with character t in column’s name replaced by Time
7) Create a second, independent tidy data set with the average of each variable for each activity and each subject
	output is created by sumarizing tidy taking the means of each variable for each activity and each subject, after groupped by subject and activity.
	Export output into output.txt file.