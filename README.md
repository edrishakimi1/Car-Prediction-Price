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
