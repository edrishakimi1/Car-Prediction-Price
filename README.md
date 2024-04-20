## Table of Contents 
### 1. Predicting Car Prices
1.1 Introduction

1.2 Source of Data

1.3 Metrics considered

1.4 Questions to consider when predicting the car price

1.5 Importing libraries

1.6 Reading the data

### 2. Exploratory data analysis 

##### 2.1 Countplot 

&ensp;&ensp;&ensp;2.1.1 Countplot of different car make

&ensp;&ensp;&ensp;2.1.2 Countplot of total cars in different years

&ensp;&ensp;&ensp;2.1.3 Countplot the cars with different transmission type

&ensp;&ensp;&ensp;2.1.4 Countplot of engine fuel type

&ensp;&ensp;&ensp;2.1.5 Countplot of vehicle size

##### 2.2 Missingno

##### 2.3 Groupby 

&ensp;&ensp;&ensp;2.3.1 Group with car make with other variable

&ensp;&ensp;&ensp;2.3.2 Group with average price of cars in different years

&ensp;&ensp;&ensp;2.3.3 Group with make and 'MSRP'

&ensp;&ensp;&ensp;2.3.4 Group with make and 'Popularity' values

##### 2.4 Scatterplot between 'highway MPG' and 'city mpg'

##### 2.5 Boxplot

&ensp;&ensp;&ensp;2.5.1 Boxplot of 'highway MPG'

&ensp;&ensp;&ensp;2.5.2 Boxplot of 'city mpg'

&ensp;&ensp;&ensp;2.5.3 Boxplot of comparing 'city mpg' and 'highway MPG'

&ensp;&ensp;&ensp;2.5.4 Boxplot of 'Engine HP'

##### 2.6 Heatmap of all the variables

##### 2.7 Checking the NULL values

&ensp;&ensp;&ensp;2.7.1 Make Number of Doors have 0 missing values

##### 2.8 Creating a new column for Present Year

##### 2.9 Plotting the barplot of 'Years of Manufacture'

##### 2.7 Checking the NULL values

&ensp;&ensp;&ensp;2.7.2 Make Engine Fuel Type have 0 missing values

&ensp;&ensp;&ensp;2.7.3 Make Engine HP have 0 missing values

&ensp;&ensp;&ensp;2.7.4 Make Engine Cylinders have 0 missing values

&ensp;&ensp;&ensp;2.7.5 Dropping Market Category as there is too many missing values

##### 2.10 Checking data variables for non integer values



### 3. Manipulating the Data 

##### 3.1 Shuffling the data 

##### 3.2 Dividing data into train and test set

##### 3.3 Encoding the data

&ensp;&ensp;&ensp;3.3.1 Encoding the Year Column

&ensp;&ensp;&ensp;3.3.2 Encoding the Model Column

&ensp;&ensp;&ensp;3.3.3 Encoding the Make Column

##### 3.4 One Hot Encoding 

&ensp;&ensp;&ensp;3.4.1 One Hot Encoding the rest Engine Fuel Type, Transmission Type, Driven_Wheels, Vehicle Size, Vehicle Style Column

##### 3.5 Standardization and Normalization of data 

### 4. Machine Learning Analysis 

##### 4.1 Linear Regression 

&ensp;&ensp;&ensp;4.1.1 Regplot of Linear Regression Output  

##### 4.2 K - Neighbors Regressor 

&ensp;&ensp;&ensp;4.2.1 Regplot of K - Neighbors Regressor 

##### 4.3 Decision Tree Regressor 

&ensp;&ensp;&ensp;4.3.1 Regplot of Decision Tree Regressor 

##### 4.4 Gradient Boosting Regressor 

&ensp;&ensp;&ensp;4.4.1 Regplot of Gradient Boosting Regressor
 
##### 4.5 Observations when comparing all the regplot for the 4 types of machine learning model 

##### 4.6 Dataframe of Machine Learning Models 

##### 4.7 (a). Barplot of machine learning models with mean absolute error 

##### 4.7 (b). Barplot of machine learning models with mean squared error 

##### 4.8 Observations when using Barplot for comparing all the 4 types of machine learning model using MAE and MSE

### 5. Conclusion

## Contributors
##### Hakimi - Presentation, Data Analysis, Machine Learning
##### Feng Ren - Presentation, Data Analysis, Machine Learning
##### Younes - Presentation, Data Cleaning, EDA 


## Problem Formulation and Conclusion:

In order to evaluate how we gonna predict the car price, we have to consider the questions chronologically.

1. Look at the car dataset and see the counting for each variables?
2. Are there any missing values in each variable of the dataset?
3. How is city mpg and highway mpg correlated using box plot? Address the outliers as well when comparing and for future machine learning test.
4. Which features are heavily correlated to one another by using heat map?
5. Check for NULL missing values, and make sure the data is filled or drop the variable so the machine learning will not encounter any problems?
6. Create a new column for Present Year (2024) and plot the Years of Manufacture, this variable will be considered as well for the machine learning model?
7. Check the data again for variables that has catergorical values, we have to address them by changing to numerical values for the machine learning to analyse?
8. Plot the different machine learning model and check which prediction model has the best result, in terms of lowest mean squared error (MSE) and lowest mean absolute error (MAE), when also checking for which range of values work best?

Answer:

1. We have observe all the variables and their count, e.g. 'Cheverolet has the highest number of cars followed by ford', 'in 2015 to 2017 which recent years has higher cars', 'Automatic or manual is higher and more relevant then cars with both automatend and manual mode', 'cars are using more unleaded engine fuel compared to electric','alot of compact cars and lesser large cars'.
2. We observe that 'Market Category' has alot of missing values followed by, 'Engine HP', 'Engine Cyclinders', 'Engine Fuel Type', 'Number of Doors'.
3. We have remove the outliers after using box plot for 'city mpg' and 'highway MPG'. We see that in terms of 'city mpg' most of the values that are present are in the range between 15 to 22 respectively. While in terms of 'highway MPG', we find that most of the values that are present are in the range 22 to 30 respectively. Therefore, we can see how the values are spread in the boxplot.
4. In the heatmap, we see that 'highway MPG' and 'city mpg' are highly related, with the value of 0.94. While also 'Engine HP' and 'Engine Cyliners' are also correlated 0.78. This correlation are important as it validates whether the data is true in our dataset. In the car industry, and above when we plot the scatterplot of 'highway MPG' and 'ciy mpg' we know that both must be related and they cannot differ, additionally for 'Engine HP' and 'Engine Cylinders' they are correlated as having higher number of cylinders will relate to higher number of horsepower in the car industry.
5. We drop 'Market Category' as there is too many unique text data and we also make sure the variables with missing values in 2. has been change to 0 missing values.
6. We have changed the Year of dataset so it represents how long the car has been manufactured since so the prediciton model will take note of this. We want to make sure the dataset we use is recent years of cars.
7. We use target encoding for the 'Year', 'Model' and 'Make' and the one hot encoding for the rest of the missing values 'Engine Fuel Type, 'Transmission Type', 'Driven_Wheels', 'Vehicle Size', and 'Vehicle Style.
8. Based on the observation of regplot and barplot to compare the 4 different machine learning models, as a tighter clustering of points around y=x line indicates better preddictions, and a narrower confidence band around the line of best fit also suggests higher accuracy, Gradient Boosting Regressor fits the best, followed by the K-Neighbors Regressor, Decision Tree Regressor, and lastly the Linear Regression. Whereas for barplot when comparing with metrics of MAE and MSE, Decision Tree Regressor has the lowest for both MAE and MSE so it is predicts better and accurately, and this represents how well the model has learned from the training data and how it generalise to new, unseen data. Followed by Gradient Boosting Regressor, K - Nearest Regressor, and lastly Linear Regression.

## Machine Learning 
##### Linear Regression, K-Neigbors Regressor, Decision Tree Regressor, Gradient Boosting Regressor



## References
https://arxiv.org/pdf/1809.03006.pdf?ref=hackernoon.com 
https://www.analyticsvidhya.com/blog/2020/08/types-of-categorical-data-encoding/

