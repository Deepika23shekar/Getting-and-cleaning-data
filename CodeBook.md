#Code Book
This code book describes the variables of the data set, and any transformations performed to clean up the data in unique_act_sub.txt

1.The dataset is downloaded and extracted

2.Each data is assigned to variables 
  *features <- features.txt
  *subject_test <- test/subject_test.txt
  *x_test <- test/X_test.txt
  *y_test <- test/y_test.txt 
  *subject_train <- test/subject_train.txt
  *x_train <- test/X_train.txt
  *y_train <- test/y_train.txt
  
3.Training and testing data are merged to create one file called as Merged_Data

4.TidyData (10299 rows, 88 columns) is created by subsetting Merged_Data, selecting only columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement.

5.Entire numbers in code column of the TidyData replaced with corresponding activity taken from second column of the activities variable

6.code column in TidyData renamed into activities
All Acc in column’s name replaced by Accelerometer
All Gyro in column’s name replaced by Gyroscope
All BodyBody in column’s name replaced by Body
All Mag in column’s name replaced by Magnitude
All start with character f in column’s name replaced by Frequency
All start with character t in column’s name replaced by Time

7.FinalData is created by sumarizing TidyData taking the means of each variable for each activity and each subject, after groupped by subject and activity.
Export FinalData into FinalData.txt file.