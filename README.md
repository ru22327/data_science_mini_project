# Predicting the cost of medical insurance

This code was written in Python for a short project to explore and create a predictive model from the medical insurance dataset (obtained from https://github.com/stedy/Machine-Learning-with-R-datasets/blob/master/insurance.csv) using data visualisation and correlation techniques. 

URL TO GITHUB: https://github.com/ru22327/data_science_mini_project.git 

## Introduction:

This dataset contains 1338 samples of medical insurance charges from the US population, as well as physical characteristics of the patients such as their age, sex, BMI, number of dependents, smoking status and region of residence. My aim with this dataset was to create a model which could be used to predict medical insurance costing based on certain parameters. Hence, this code firstly involves visually exploring correlations between these variables to ultimately hone in on a relationship suitable enough to create and optimise a predictive model.

The annotated code in this notebook can also be applied to other datasets where the user wants to visualise the relationship between variables using bar plots and box plots, and perform a linear regression model with polynomials. 

## How to install: 

To follow the code in this notebook, download the insurance.csv file in this repository to your directory of choice, then load the medical_costs.ipynb to JupyterLab and follow the instructions within. All libraries to be imported are written into code cells, and markdown cells are used to guide the user through the set-up and analysis. Running all code cells consecutively will generate the results expected. The only cell requiring modification is code cell 2 where the user is prompted to edit the file path to the directory containing the downloaded insurance.csv file. 

## Methods:

This project contains code to perform the following techniques:

-	Annotated bar charts and box plots with matplotlib
-	Correlation matrices with seaborn
-	Scatterplots with multiple variables using seaborn 
-	Categorising data using for-loops and binning data into custom categories using pandas
-	Creating a subset of the data frame 
-	Linear regression with polynomial features using scikit-learn

## Expected results:

Running through this notebook will firstly provide an exploration of the dataset to verify whether the variables are equally distributed and not biased towards a particular group of people. A heatmap and multi-variable scatter matrix comparing all continuous variables with data points coloured by smoking status reveals distinct patterns between charges and both age and BMI. Grouping the charge costs into 3 distinct bands, and categorising the BMI values into pre-defined weight classifications [1], depicts higher insurance costing to be more dependent on age in non-smokers, but BMI in smokers.

The strongest relationship seen in this project is between charges and BMI for smokers. Therefore, linear regressions were plotted on this data to create a predictive model, and polynomials were introduced in optimisation attempts. Plotting the models raises a concern of needing to balance a better model score against over-fitting however.

## Summary/ Conclusions:

The medical cost dataset contains multiple unbiased variables to explore. The most noticeable variable to affect insurance charge was smoking status – in non-smokers, age is the driving factor, whereas BMI has a more prominent influence in smokers. Linear regression models were plotted with the latter and the best model score to be obtained was 0.74 by implementing a 10th degree polynomial, however the 2nd degree (score = 0.66) seemed to have a visually better fit. Ideally, a score closer to 1.0 would be the best predictive model, but 0.74 was the best that could be found in this project, and this is only applicable to a subset of the population. 

Next steps: To determine which polynomial regression is best statistically, the R-squared values could be calculated for the training and test subsets for each model – the closer they are in value, the better the predictive power.


References:

[1] Defining adult overweight &amp; obesity (2022) Centers for Disease Control and Prevention. Centers for Disease Control and Prevention. Available at: https://www.cdc.gov/obesity/basics/adult-defining.html (Accessed: December 18, 2022).
