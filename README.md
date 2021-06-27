# wafer_fault_detection
## Problem statement
To build a classification methodology to predict the quality of wafer sensors based on the given training data.<br>
## Archietecture
## Data Description
The client will send data in multiple sets of files in batches at a given location.<br>
Data will contain Wafer names and 590 columns of different sensor values for each wafer.<br>
The last column will have the "Good/Bad" value for each wafer.<br>
"Good/Bad" column will have two unique values +1 and -1. <br> 
"+1" represents Bad wafer.<br>
"-1" represents Good Wafer.<br>
## Steps
1.<b>"Data validation"</b>:
The name of the dataset, number of columns,datatype,and whether the whole column in a dataset is empty or not are validated.<br>
The datasets which gets passed in the above validations are moved to <b>"Good Data"</b> folder and the rest of the datasets are moved to <b>"Bad Data"</b> folder.<br>
The datasets in the <b>"Good Data"</b> folder are transformed and stored in a database and then all the datasets exported as a <b>"Input.csv"</b>file.<br>
2.<b>"Data Preprocessing"</b>:
The missing values are handled by using KNN imputer.<br>
The Columns which are having zero standard deviation are removed.<br>
3.<b>"Clustering"</b>:
The dataset is grouped in the form of clusters and it is done by using <b>"Kmeans++"</b> algorithm and for each cluster a seperate model is created.<br>
4.<b>"Model creation"</b>:
The model creation is done by using <b>"Random Forest"</b> algorithm and hyperparameter tuning is also done to avoid the overfitting problem<br>.
5.<b>"Model Prediction"</b>:
Once the test data is given then  <b>"Data validation"</b> and <b>"Data Preprocessing"</b> are done depending upon the cluster the model is chosen and prediction is done using that model and the results are stored in "Prediction.csv" file.








