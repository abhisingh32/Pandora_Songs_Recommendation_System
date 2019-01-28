# Pandora_Songs_Recommendation_System

Data Pre-processing:
I have used PANDAS to process the data in suitable form. It includes loading the data from multiple files and then joining/ manipulating as per the requirement at each step of the algorithm. e.g. pandas library is used to combine User and Track column separated by hyphen.

Algorithm:
Note: Please refer the code for reference to below explanation.

1.	I have Pandas dataframes form both the train data and test data.
2.	Import the libraries such as OS and Pandas to process the file path and files respectively. An important library here is Surprise library. It is used here for reading the dataset, perform SVD and also for cross_validation operation.
3.	train and test CSV that are provided, are read below to the df_trainfile and df_testfile dataframes. df_trainfile contains the dataset with tab seperated values instead of commma as in typical csv file.
4.	Fetching the path of the tab-seperated data file for further processing by load_from_file fuction. df_test_rt loads the copy of the test data subsequent iterations.
5.	reader-> reads the data from file, sep-> tells the seperation of the data or acts as delimiter, seprating two consequtive data blocks.
6.	Now we have to build an algorithm and train it as well. We will fist load the deafult SVD algorithm for that and then train it using the train the algorithm using trained_set
7.	Since the model is trained now, we will test the model using Root Mean Sqaure Error(RMSE) as evaluation metric.
8.	Create an empty list to store the predicted values. Now the every record is iterated for the complete set of test data and rating is predicted for each user-track pair.
9.	New data frame is created to load the load the result file in .csv file. The new dataframe is formatted in the required format (joining by hyphen)
10.	Ratings column is added to add the predicted Ratings alongwith combined user-track pair.
11.	Save the dataframe to results.csv - as per the submission format 




Links to sources:

# For understanding the concepts of SVD in recommendation system
https://medium.com/@m_n_malaeb/singular-value-decomposition-svd-in-recommender-systems-for-non-math-statistics-programming-4a622de653e9
# Reference from GITHUB 
https://github.com/rashmishrm/Collaborative-Filtering-Demo
# For exploring surprise library and packages.
https://surprise.readthedocs.io/en/stable/index.html
# surprise package algorithms:
https://surprise.readthedocs.io/en/stable/prediction_algorithms_package.html
