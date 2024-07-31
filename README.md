# Machine Learning for Energy Systems

## Abstract

A Machine Learning project that applies a wide range of ML algorithms to predict greenhouse gas leakage from oil wells in Alberta.

The task is to train models that can predict greenhouse gas emission type (Serious or Non-Serious using Classification) and emission type (in m3/day using Regression). Classification models are evalutated based on highest accuracy and regression models are evaluated based on lowest root mean squared error.

## Objective

* Process the data by: Removing outliers, Imputing missing data points, Handling text data and Standardization
* Train binary classification models using "Classfication" and fine tune hyperparamenters using GridSearchCV or RandomizedSearchCV based on accuracy.
* Train regression models using "Emission Rate (m3/day") and fine tune hyperparamenters using GridSearchCV or RandomizedSearchCV based on mean squared error.
* Test all models on a test set to get the most reliable classifier and regressor

## About the Problem

Exploitation of oil and gas reserves has raised public concern regarding contamination of soil and underground water resources, and increase in greenhouse gas emission. Methane, sequestered CO2 and/or any liquid or combination can migrate and leak from wellbores to water aquifers, ground surface and atmosphere. Leakage pathways may exist along and through boreholes. The presence of such fluid pathways is a significant environmental issue. Regular field monitoring should be applied to detect serious leakage through exiting oil and gas wells. Leakiest wells should be prioritized for amendment. The Alberta Energy Regulator (AER) in Alberta, Canada, operates such field tests for energy wells within the province. The AER applies field tests for identification of fluid migration measuring leakage rate (m3/day) and classifies wells as serious or non-serious in terms of leakage.

The challenge is that there are many wells in producing areas in Alberta. Efficient and cost-effective testing operation for all wells is impossible.

## Dataset

Source: [GHG_Emission.csv](https://github.com/Sidkian/Machine-Learning-for-Energy-Systems/blob/master/GHG_Emission.csv)

The dataset is retrieved from Alberta Energy Regulator (AER). Locations of the wells are changed, and some key properties are generated synthetically or are greatly manipulated for confidentially reason.

The following figure shows location map and pie chart of 1500 hydrocarbon wells with serious and non-serious classification:

![Well-Location](https://github.com/Sidkian/Machine-Learning-for-Energy-Systems/blob/master/well-location.png)

## Classification

Documentation: [Classification](https://github.com/Sidkian/Machine-Learning-for-Energy-Systems/tree/master/Classification/Classification.md)

12 Classifiers were trained to predict the Classification of Serious (1) or Non Serious (0). The accuracy on test set (never seen before data) is:

![Test Set Accuracy](https://github.com/Sidkian/Machine-Learning-for-Energy-Systems/blob/master/Classification/Images/test-set-acc.png)

## Regression

Documentation: [Regression](https://github.com/Sidkian/Machine-Learning-for-Energy-Systems/tree/master/Regression/Regression.md)

5 Regressor were trained to predict Emission Rate. The Root Mean Square Error (RMSE) on test set (never seen before data) is:

![Test Set RMSE](https://github.com/Sidkian/Machine-Learning-for-Energy-Systems/blob/master/Regression/Images/test-set-rmse.png)