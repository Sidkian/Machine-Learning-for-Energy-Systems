# Classification

## Data Processing

Documentation: [Classification - Data Processing]()

The data is processed in the following steps:
* Removed outliers based on Emission rate (m3/day) for instances out of the range $\mu$ &pm; 2.5 $\sigma$ (where $\mu$ = mean and $\sigma$ = standard deviation )
* Dropped "Emission Rate (m3/day)" column
* Split the data into training set (80%) and test set (20%)
* Imputed median into numerical columns with missing data on training set and used it to transform the the test set
* Encoded text columns on training set and used it to transform the test set
* Scaled all numerical columns and used it to transform the test set

## Data Visualization 

Documentation: [Classification - Data Visualization]()

The processed data is used to generate the following plots for data visualization:

* Location map showing well placement in Alberta:
    ![Location Map]()
* Correlation plot showing the correlation between each column and the Classification Column. :
    ![Correlation Plot]()
* Cross Plot between Measured Dept and X Coordinate (left) & Deviation and Measure Depth (right)
    ![Cross Plot]()
* Histogram of Month Well Spudded (left) and Deviation (right)
    ![Hist Plot]()

## Models

Documentation: [Classification - Models]()

The following models are trained and fine tuned to predict Classification of Serious (1) or Non Serious (0):
* Dummy Classifier
* Stocastic Gradient Descent
* Logistic Regression
* Support Vector Machines: Linear
* Support Vector Machines: Polynomial
* Decision Tree
* Random Forest
* Adaptive Boosting on SVM (linear)
* Adaptive Boosting on Decision Tree
* Hard Voting
* Soft Voting
* K Nearest Neighbours

Accuracy on Training Set: 
![Training Set Accuracy]()

Accuracy on Test Set:
![Test Set Accuracy]()