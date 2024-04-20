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

<<<<<<< HEAD
### 5. Conclusion
=======
### 5. Conclusion

## Contributors
##### Hakimi - Presentation, Data Analysis, Machine Learning
##### Feng Ren - Presentation, Data Analysis, Machine Learning
##### Younes - Presentation, Data Cleaning, EDA 


## Problem Formulation
##### Predict Manufacturer's Suggested Retail Price

In order to evaluate how we gonna predict the car price, we have to consider the questions chronologically.

1. Look at the car dataset and see the counting for each variables?
2. Are there any missing values in each variable of the dataset?
3. How is city mpg and highway mpg correlated using box plot? Address the outliers as well when comparing and for future machine learning test.
4. Which features are heavily correlated to one another by using heat map?
5. Check for NULL missing values, and make sure the data is filled or drop the variable so the machine learning will not encounter any problems?
6. Create a new column for Present Year (2024) and plot the Years of Manufacture, this variable will be considered as well for the machine learning model?
7. Check the data again for variables that has catergorical values, we have to address them by changing to numerical values for the machine learning to analyse?
8. Plot the different machine learning model and check which prediction model has the best result, in terms of lowest mean squared error (MSE) and lowest mean absolute error (MAE), when also checking for which range of values work best?

## Conclusion

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

1. Regplot of Linear Regression
<img width="610" alt="Regplot of Linear Regression" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/7b5097c1-e69d-4ddf-9009-1f26032d6109">

2. Regplot of K-Neighbors Regressor
<img width="603" alt="Regplot of K-Neighbors Regressor" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/60265a16-bef7-45f4-ace0-c704696c8d51">

3. Regplot of Decision Tree Regressor
<img width="610" alt="Regplot of Decision Tree Regressor" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/0a1838ff-33d2-4aa8-94af-5a5264c46ab5">

4. Regplot of Gradient Boosting Regressor
<img width="618" alt="Regplot of Gradient Boosting Regressor" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/839912c7-d176-4f48-bd08-7b763eaa64ff">

##### 4.5 Observations when comparing all the regplot for the 4 types of machine learning model

The regression line in these plots represents the relationship learned by the model. Ideally, for perfect predictions, all points would lie on the line where the predicted value equals the actual value (the diagonal line, if it were plotted) The closer the points to this hypothetical diagonal line, the better the model's prediction. 

When we compare the tightness of the scatter around the regression line in these graphs, the Gradient Boosting Regressor appears to be performing the best, followed by the K-Neighbors Regressor, Decision Tree Regress, and lastly the Linear Regression.

1. Barplot of Machine Learning Models with MAE
<img width="667" alt="Barplot of Machine Learning Models with MAE" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/7aeea383-a772-4f26-a537-d17fac574ee4">


2. Barplot of Machine Learning Models with MSE
<img width="667" alt="Barplot of Machine Learning Models with MSE" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/cb7eb91e-68e3-4c25-9039-92e42abeee38">

##### 4.8 Observations when using Barplot for comparing all the 4 types of machine learning model using MAE and MSE
1.Mean Absolute Error (MAE)

Importantly, this metric gives an average of the absolute differences between the predicted and actual values. It's straight forward and easy to interpret since it's in the sam eunits as the target variable. The lower the MAE, the better the model's performance.

2.Mean Squared Error (MSE)

Importantly, this metric squares the difference between the predicted and actual values, which penalizes larger errors more severely than smaller ones. Like MAE, a lower MSE indicates better performance, but because of the squaring, MSE is more sensitive to outliers than MAE.

When evaluating models, a model with both a low MAE and MSE is considered good, but these two metrics can sometimes tell a slightly different story. A low MAE with high MSE might indicate that while a model is generally accurate, there are a few predictions with large errors (potential outliers). Conversely, a high MAE with a low MSE might suggest that the model consistently makes moderate errors but doesn't have extreme errors.

3. Barplot Analysis
The bar plots help to visualise these metrics across different models. In the context of car price prediction, we want to look at models that has the lowest bar in both MAE and MSE plots. 

To summarise, Decision Tree Regressor has the lowest for both MAE and MSE so it is predicts better and accurately, and this represents how well the model has learned from the training data and how it generalise to new, unseen data. Followed by Gradient Boosting Regressor, K - Nearest Regressor, and lastly Linear Regression.



## References
https://arxiv.org/pdf/1809.03006.pdf?ref=hackernoon.com 
https://www.analyticsvidhya.com/blog/2020/08/types-of-categorical-data-encoding/

>>>>>>> bff1a4d6bb78da2cfe7d79561d54f495e9ca41b0
