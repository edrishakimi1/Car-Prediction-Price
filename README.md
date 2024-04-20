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

##### Source of Data

Below is the link to the dataset we use for our analysis.

https://www.kaggle.com/CooperUnion/cardataset

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

## Data Visualisation - See variables with total number
1. Countplot of different car brands

<img width="661" alt="Countplot of different car brands" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/b376d689-b637-44d5-8f69-4541af49df83">

We can see that the company 'Chevrolet' has the most cars in our dataset. We also see that there are companies with only afew cars such as 'Bugatti' and 'McLaren' which is reflective of the real-world as we don't find different models of these cars. A countplot could really give us a good understanding of the data that we are working.

2. Countplot of Transmission Type

<img width="623" alt="Countplot of Transmission Type" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/bc6f2e5f-0ce1-43ed-9245-fef1dcf8ccb0">

We see that there are alot of values for automatic and manual, automatic is more than manual so this is a good indicator that in future as we move to a marketplace that will potentially be saturated with electronic vehicles (EV) or manual cars. Some customer prefer manual cars as they want to drive, and some prefer EV and it may be best to have both as well. But for both automate and manual there are very little data but currently is fine now as it is reflective of the present years but in future we should consider cars that have both automatic and manual mode.

3. Countplot of engine fuel type

<img width="665" alt="Countplot of engine fuel type" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/74bd3145-5263-462f-aadd-2bae847aae67">

We can see that majority of cars have 'regular unleaded' feature, also 'premium unleaded; both required and recommended, are also considered. as well as flex-fuel. Similar to before currently and present years there is still top up of fuels, and the car market is not dominant with electric mode of cars, so we do not have to concern ourself with that. But in future, we should work on dataset that are electric and disel related.

4. Count of Vehicle Size

<img width="853" alt="Countplot of Vehicle Size" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/129ed86b-3950-41b6-90c2-55610e62c62c">

We can see that most of the cars are compact and the least cars are of large size, which is a reflection of the real world as large cars are for family use, and compact cars are more common.

5. Missing Null Values

<img width="643" alt="MissingnoValues" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/102fcb8b-45b0-4537-827a-c8f555c54bbb">

We can see that the variable ' Market Category' has the most missing values, and some variable 'Engine HP' Engine Fuel Type' has abit of missing values so we need to address them before we can test the machine learning model. We will use encoding and one hot encoding to do the machine learning later. This gives us a good graphic representation of which variables has missing values so that later on we can either fill up the missing values with median or we can drop the variable feature completely.

## Data Visualisation - Exploratory Data Analysis
1. Groupby Average price of cars in years
<img width="661" alt="Groupby Average price of cars in years" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/4c1962c5-1bbe-4e96-90f6-f17249adb86f">

Prices increases steadily after the years goes on so we can look at the competitive price landscape of cars to adjust the retail price to make it seem reasonable as we predict the car retail price without any loss of profit while gaining the customer demand.

2. Groupby Average price of cars with brands
<img width="671" alt="Groupby Average price of cars with brands" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/880138d0-8d10-4a40-9afb-f3fd0169661a">

We see different average price points for each car brand. we can see that the highest is Bugatti which is the most expensive car brand in the present world, and the most affordable is like Toyota, Nissan, Hyundai, Kia.

3. Groupby Popularity with car brands
<img width="335" alt="Groupby Popularity with car brans" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/fc40196a-7342-49d8-a927-d3c42acc83fe">

We see that most people get Ford and BME, while very little in Lincoln and Genesis that we are also not aware of.

4. Before Scatterplot highway and city mpg
<img width="661" alt="Before Scatterplot highway and city mpg" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/3a576ad0-aa20-44d5-8c94-d16eb0a2ea46">

We want to consider the linear relationship between 'highway MPG' and 'city mpg' as both of the mpg (miles per gallon) are similar and they should be correlated for the dataset we are using, they are not correlated, we have to expect that the computation for prediction may be wrong. Therefore, we cannot have dataset that have a highway mpg that differs from city mpg. Based on the plot below, there is one outlier where the highway mpg is about 350. We have to remove the outlier as there should not be cars that have this high mpg, so we need to remove it as it will affect our results as errors in the data can cost the machine learning operation to fail.
 
5. After Scatter plot highway and city mpg
<img width="672" alt="After Scatterplot highway and city mpg " src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/e6efd961-245a-43ae-b137-7f45331ff261">

6. Before Boxplot of highway MPG
<img width="662" alt="Before Boxplot of highway MPG" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/c1001131-7e82-45ef-9ad7-9403e90fc7de">

We see how the distribution is spread. We see that the average values are 25 for highway MPG and the maximum value being equal to around 40 and the points above 40 are considered outliers. We see that the distribution of data is quite compact as it only spread from 21 to 30 roughly.
   
7. After Boxplot of highway MPG
<img width="664" alt="After Boxplot of highway MPG" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/26e3e506-95c8-4eda-93c9-a16ad90ede8b">

We see that the distribution of data is quite compact as it only spread from 21 to 30 roughly. We also see clearly that the highway MPG is more skewed towards to right and alot of values to the right of the mean. What we can infer is that more than 50 percent of the values are above the mean.

8. Before Boxplot of city mpg
<img width="665" alt="Before Boxplot of city mpg" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/4f1280b8-3143-4aea-9257-36d83ecc5394">

We will repeat the same operation for 'city mpg' and we see below some outliers that might interfere in our predictions. Therefore, we will delete those values by limiting the range shown.

9. After Boxplot of city mpg
<img width="661" alt="After Boxplot of city mpg" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/0bd6794e-5600-426c-bd8d-d9ab1b4ccb41">

We remove the outliers. We also see clearly that the city MPG is more skewed towards to right and alot of values to the right of the mean. What we can infer is that more than 50 percent of the values are above the mean.

10. Boxplot of both city mpg and highway MPG
<img width="865" alt="Boxplot of both city mpg and highway MPG" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/0db4a128-ea8b-4b0d-aeb7-468f8fbe2493">

We want to compare the 2 variables 'city mpg' and 'highway MPG' side by side. We see that in terms of 'city mpg' most of the values that are present are in the range between 15 to 22 respectively. While in terms of 'highway MPG', we find that most of the values that are present are in the range 22 to 30 respectively. Therefore, we can see how the values are spread in the boxplot.

11. Boxplot of Engine HP
<img width="864" alt="Boxplot of Engine HP" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/16613e71-620a-4882-920a-38c501c7e5ad">

We see that most of the values of 'Engine HP' lie between 150 to 300 respectively. The maximum value of the engine horsepower will be something like 500 while the remaining values that are higher can consider them to be outliers. The boxplot also looks as though it is right skewed where there are more number of values of 'Engine HP' that are higher than the mean value of about 250 (mean).

12. Heatmap of all variables
<img width="818" alt="Heatmap of all variables" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/7b66edb1-a62d-4a1e-a359-3e850f4a0911">

We use heatmap in python, we can consider all the important features of the car and how they relate to each other. We see that 'highway MPG' and 'city mpg' are highly related, with the value of 0.94. While also 'Engine HP' and 'Engine Cyliners' are also correlated 0.78. This correlation are important as it validates whether the data is true in our dataset. In the car industry, and above when we plot the scatterplot of 'highway MPG' and 'ciy mpg' we know that both must be related and they cannot differ, additionally for 'Engine HP' and 'Engine Cylinders' they are correlated as having higher number of cylinders will relate to higher number of horsepower in the car industry.

13. Barplot of Years after Manufacture and car count
<img width="652" alt="Barplot of Years after manufacture and car count" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/dff12dfb-3bb6-4174-8e6a-5c76095bd76c">

We see the bar plot for the years that is out for the cars, we can see that most of the values are about 9 years old. Therefore, we are working with young cars as there are some other cars in our data that are about 34 years old. These cars are very few in number. This is a good indication as the current data set is not old and we can use it as reference for future prediction of car retail price.

## Data Preprocessing and Cleaning before Machine Learning - Manipulating the data
1. Missingno NULL Data Visualisation
<img width="660" alt="Missingno NULL Data visualisation" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/4c70d8aa-69a2-4714-af14-57dbd9cca726">

2. Before Number of missing variable count
<img width="180" alt="Before Number of missing variable count" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/7c6d43ee-55b4-4cf5-990d-9110931b0fbf">

3. After Number of missing variable count
<img width="172" alt="After Number of missing variable count" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/c3157a09-be0f-442a-81c4-ad6907465ac4">

4. Before encoding Make, Model, Year data
<img width="654" alt="Before encoding Make, Model, Year data" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/189af4af-56ef-43b8-941f-b43cb74733e2">

5. After encoding Make, Model Year data
<img width="665" alt="After encoding Make, Model, Year data" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/a9f5d90f-c956-443a-a1c6-26b30e37b9a8">

6. Before one hot encoding variable and data type
<img width="298" alt="Before one hot encoding variable and data type" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/d7532389-8d16-42a0-8db5-076d3a04355a">

7. After one hot encoding variable and data type
<img width="298" alt="After one hot encoding variable and data type" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/d2707ea3-2765-48c8-b555-baec9b81038c">

##### 3. Manipulating the Data 
We fill up all the missing null usin gmedian as it is better representation than mean for the dataset. We drop 'Market Category' as it has many unique name type. To ensure 0 missing data in the data set.
We encode the variables so that we will convert data to numerical form so that machine learning model can work. We do one hot encoding to convert each variable data into set of 0 and 1 whether the value is present in the data


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

1. Dataframe of Machine Learning Models with MAE, MSE Values
<img width="317" alt="Dataframe of Machine Learning Models and MAE, MSE values" src="https://github.com/edrishakimi1/Sc1015-Retail-Car-Prediction-Price/assets/106168087/60c5d474-3b25-4e26-9906-905948dcd115">


3. Barplot Analysis

The bar plots help to visualise these metrics across different models. In the context of car price prediction, we want to look at models that has the lowest bar in both MAE and MSE plots. 

To summarise, Decision Tree Regressor has the lowest for both MAE and MSE so it is predicts better and accurately, and this represents how well the model has learned from the training data and how it generalise to new, unseen data. Followed by Gradient Boosting Regressor, K - Nearest Regressor, and lastly Linear Regression.



## References
https://arxiv.org/pdf/1809.03006.pdf?ref=hackernoon.com 
https://www.analyticsvidhya.com/blog/2020/08/types-of-categorical-data-encoding/

>>>>>>> bff1a4d6bb78da2cfe7d79561d54f495e9ca41b0
