# Structural Damage Detection using a hybrid CNN-SVM
This repository contains a CNN-SVM for structural damage detection using acceleration data. The model is implemented in Python using the pytorch library.
Note: This is an element by element monitoring of the structure.

# Requirements
To use this code, you will need the following libraries:

* torch
* matplotlib
* numpy
* sklearn
* pandas

You will also need access to the appropriate data files for training and evaluating the model.

# Data Loading
The data_reader function is responsible for loading the data that will be used to train and test the model. It has the following parameters:

* CSVpath: a string containing the file path to the excel file containing addresses of the data.
* col: a list of integers specifying the columns of the data to use.
* skiprows: an integer specifying the number of rows to skip at the beginning of the data file.
* max_rows_undamaged: an integer specifying the maximum number of rows to load from the undamaged data files.
* max_rows_damaged: an integer specifying the maximum number of rows to load from the damaged data files.
* resample_factor: an integer specifying the resampling factor for the data. If set to 1, the data will be downsampled by a factor of 2 using odd rows. If set to 2, the data will be upsampled by a factor of 2 using the even rows.
* batch: batch size

# Training and Evaluating the Model
The model is fit to the training data. The model is then used to make predictions on the test and the training data. The performance of the model is evaluated based on accuracy, f1 score, recall, precision and roc_auc_score.

# Additional Resources
If you have any questions or need further assistance, please open an issue in this repository.
