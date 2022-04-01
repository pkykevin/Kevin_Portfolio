# Kevin Park          
Welcome to my data science portfolio. I am passionate about data analytics, data visualization, and building machine learnig models.

## Project 1 - Predictive models in category based on [Carsales](https://www.carsales.com.au) datasets

* This project is to build a tool to analyse, compare, predict and visualize the important features and price of different car categories or makes.
* The aim is to build such predictive models to facilitate decision making for second hand car buyers and sellers.
* Multiple Linear, Random Forest and Neural Network predictive modelling techniques were employed to create predictive models.
* The study implemented predictive models on actual data from [Carsales](https://www.carsales.com.au) website.
* We will observe contributing features in category into different levels of prestige - luxury sports, luxury and economy cars.
* We also drill down car categories to discover the price influencing features on different car makes.

### Part 1. Dataset

#### A. Data extraction

The sample dataset of Toyota Corolla extracted from [Carsales](https://www.carsales.com.au).  Python’s Beautiful Soup v4 library used to extract data into a form that can be imported. 

![1](https://user-images.githubusercontent.com/32251175/160815871-c6367950-716f-4555-ada2-23d1bc7b30dd.PNG)

Following is an example of Toyota Corolla dataset in csv file extracted from Carsales website.

![2](https://user-images.githubusercontent.com/32251175/160816821-fb5064f4-2b00-4665-a286-28ab249f6806.PNG)

#### B. Data exploration

The dataset comprises of 21 attributes related to 2030 sold Toyota Corolla cars. The table has 2030 rows and 21 columns. Based on this dataset, the research needs to develop a reliable predictive model to predict the selling price of the cars. Therefore, the target variables applicable for model is ‘Price’.

As we have identified price as the target variable, the research has examined the prices of the Toyota Corolla vehicles by calculating the summary statistic and prepared the histogram, density and box plot of the price variable in the Toyota Corolla dataset. The price is a continuous numerical variable. The following are results of summary statistics and plots created in Python.

![3](https://user-images.githubusercontent.com/32251175/160816828-5deb7f84-9c75-4bb6-9d09-b03a93622880.PNG)

The summary statistic shows that, the selling price for Toyota Corolla has an average value of $16,990, standard deviation of $4,974 and mean of $17,355 (minimum from $1,900 to maximum $35,980) There is also indication of extreme values, which is shown in the histogram, density and boxplot. 

#### C. Check for missing values

We need to check for any missing values in the Toyota Corolla dataset provided using *isnull()* function. Consequently, the plot below shows that, the dataset is free from any missing values.

![4](https://user-images.githubusercontent.com/32251175/160821302-3f4d2a70-e81e-45d8-a5c9-9c3b4d6bcd66.PNG)

Having missing values in a dataset can cause errors with predictive modelling algorithms. The simplest strategy for handling missing data is to remove records that contain a missing value. We can use dropna() to remove all rows with missing data. The table has been cut from 2030 in the original dataset to 1894 with all rows containing a NaN removed.

![5](https://user-images.githubusercontent.com/32251175/160821359-3811f2c6-7c33-46dd-b696-b2079a18553a.PNG)

#### D. Transformation of categorical values into numerical values

As regression models only take on numerical variable, it is important that we need to transform categorical variables into numeric variables to feed into the regression model. In this case, Fuel_Type variable identified as a categorical variable with two possible values which are Petrol and Diesel. 

For transformation purpose, we assigned binary value in which 1 and 0 implies the car has the particular fuel type. The following Python script for transformation process shown below.

![6](https://user-images.githubusercontent.com/32251175/160821472-9fccb2e2-d45a-4103-9619-e88c80d20984.PNG)

#### E. Correlations evaluation and dimensionality reduction

Following section shown the correlations between variables and carried out dimensionality reductions by removing several variables. Prior to evaluating the correlation, five variables were removed from the dataset. The table belows lists 5 variables removed and reasons for it.

![7](https://user-images.githubusercontent.com/32251175/160821616-8b69e981-fdf2-4f54-b76c-ba8752a483b8.PNG)

The correlation plot below is prepared using the heatmap function after the first phase of removal.

![8](https://user-images.githubusercontent.com/32251175/160821690-52620e27-89cd-41f6-8bce-5ee1a608d354.PNG)

Following the correlation between variables shown above, dimensionality reduction is performed by removing high cross-correlation variables. Followed with a merge of target variable ‘Price’. It is also noted year, km, fuel_cost variables have high-correlation, which shows that they are important variables which later will be used in predictive modelling. Variable year, km have negative relationship with the sale price, which implies that older cars and long km are cheaper. Variable weight, emission_standards, engine_size and airbags implying increase the weight of the car has a positive effect on the sale price. Moreover, another features like fuel_capacity and fuel_cost have positive linear relationship implying includes these features have positive effect on the sale price.

### Part 2. Regression Technique using Multiple linear regression

#### a. Regression models 

In this section, multiple linear regression as a technique is applied for predictive modelling of the case study on Toyota Corolla dataset. As the main task for the predictive modelling is to predict the selling price of used Toyota Corolla using the variables selected in Part 1, therefore, price variable will be used as target variable. 

Prior to building the linear regression models, the dataset was partitioned with ⅔ as the training data sample and ⅓ as the testing data. The trained dataset comprises of 1262 training data and 632 testing data. 

![9](https://user-images.githubusercontent.com/32251175/160988349-5ac285ed-475b-4df2-9f0e-586b7274498c.PNG)

This is the process of building a model used backward elimination. 

![10](https://user-images.githubusercontent.com/32251175/160988358-2e4a5ce5-08ef-4bb1-92db-23ba51ecc3f9.PNG)

From step 1, select a significance level to stay in the model, for example, SL = 0.05 applied in this method. Step 2, fit the full model with all possible predictors. After you fit the model, you will see the one with the highest p-value, so if the p-value is greater than the significance level then you go to step 4. Step 4 is to remove that predictor. It is to remove basically the variable that has the highest p-value. And step 5, you fit the model without this variable. The model will be rebuilt with the fewer number of variables. In step 5, continue to fit the model again with one less variable. This process will keep doing that until it comes to a point where the variable of that p-value is still less than the significance level, then go to FIN (means model is ready). 

##### 1) Regression Model 1.

The first regression model technique predictive model has included all of the attributes in the selected variables identified previously section. This model resulted in an adjusted R-squared of 0.817 and Root Mean Square Error (RMSE) of 1856.29. The regression and model evaluation result is shown below.

![11](https://user-images.githubusercontent.com/32251175/160989844-b96bd704-4c00-4d0f-8d3e-0bea6ca5e2ff.PNG)


This is a comparison of predicted values with actual values and the scatter plot for regression model 1.

![12](https://user-images.githubusercontent.com/32251175/160989880-9a5e5d5f-d4e8-413f-acaa-a101ca5799b5.PNG)

##### 2) Regression Model 2.

The attributes applied for regression model 2. comprises age, km, airbags, engine_size, gears, emission_standards, weight and fuel_cost. This model resulted in an adjusted R-squared of 0.817 and Root Mean Square Error (RMSE) of 1841.17. The regression and model evaluation result is shown below.

![13](https://user-images.githubusercontent.com/32251175/160990029-dbcf061c-2cf8-47f9-b6c7-79baf2962b8e.PNG)

This is a comparison of predicted values with actual values and the scatter plot for regression model 2.

![14](https://user-images.githubusercontent.com/32251175/160990039-e3961b8d-a212-4c8e-bb79-3c2a90a653e1.PNG)

##### 3) Regression Model 3.

The attributes applied for regression model 3 comprises age, km and weight. This model resulted in an adjusted R-squared of 0.988 and Root Mean Square Error (RMSE) of 1957.55. The regression and model evaluation result is shown below.

![15](https://user-images.githubusercontent.com/32251175/161185287-2d917a05-42d3-496c-8ca9-44d98d6f49e0.PNG)

This is a comparison of predicted values with actual values and the scatter plot for regression model 3.

![16](https://user-images.githubusercontent.com/32251175/161185340-7166cccb-db90-4920-8b8d-204cfaa999e7.PNG)

#### b. Evaluation

![17](https://user-images.githubusercontent.com/32251175/161185422-fd0a9aa1-9b78-4b71-9def-6903f2955718.PNG)

The table above summarises the results of three linear regression technique predictive models based on the Toyota Corolla dataset. RMSE is used to measure the difference between predicted variable and the actual variable. Therefore, the lower RMSE would be preferred, which implies that the model 2 is the most optimal linear regression predictive model. 

### Part 3. Regression Technique using Random Decision Tree

#### a. Regression models

In this section, random decision tree technique is applied for predictive modelling of Toyota Corolla dataset. This section summarises and evaluates four random decision tree predictive models to predict price.

Prior to building the random decision tree regression models, the dataset was partitioned with ⅔ as the training data sample and ⅓ as the testing data. The trained dataset comprises of 1262 training data and 632 testing data. Then, the number of trees in the forest of 1,000 is selected to fit a number of decision tree classifiers.

Decision trees makes split that maximize the decrease in impurity. By calculating the decrease in impurity for each feature across all trees we can know that feature importance. The Python script and figure of feature importance shown below.

![18](https://user-images.githubusercontent.com/32251175/161185563-aa204a09-ad89-41fd-afc1-5db1044e0c9e.PNG)

![19](https://user-images.githubusercontent.com/32251175/161185601-d80f513b-5cb4-42a3-a6c5-f16e0d9b6b5c.PNG)

As can be seen from the graph, feature importance from Toyota Corolla shows that Age and KM are the highest features contributing to the final price followed by weight, engine size and fuel cost.

##### 1) Regression Model 1.
##### 2) Regression Model 2.
##### 3) Regression Model 3.
