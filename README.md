# Kevin Park          
Welcome to my data science portfolio. I am passionate about data analytics, data visualization, and behavioral economics.

## Project 1 - Predictive models in Category based Data analysis based on [Carsales](https://www.carsales.com.au) datasets

* This project is to build a tool to analyse, compare, predict and visualise the important features and price of different car categories or makes 
* The aim of this project is to build such predictive models to facilitate decision making for second hand car buyers and sellers.
* Multiple Linear, Random Forest and Neural Network predictive modelling techniques were employed to create predictive models.
* The study implemented predictive models on actual data from [Carsales](https://www.carsales.com.au) website.
* We try to observe contributing features in category into different levels of prestige - luxury sports, luxury and economy cars.
* We also drill down car categories to discover the price influencing features on different car makes.

### Part 1. Dataset

#### A. Data exploration

We use sample dataset of Toyota Corolla car sales. The dataset provided comprises of 37 attributes related to 1436 sold Toyota Corolla cars. Based on this dataset, the research need to develop a reliable predictive model to predict the selling price of the cars. Therefore, the target variables applicable for model is ‘Price’.

![2](https://user-images.githubusercontent.com/32251175/160736373-b626234a-2f39-4eb6-9f79-b73ba29b82e4.PNG)

The summary statistic shows that, the selling price for Toyota Corolla has an average value of $9,900, standard deviation of $3,627 and mean of $10,730 (minimum from $4,350 to maximum $32,500) There is also indication of extreme values, which is shown in the histogram, density and boxplot. 

#### B. Check for missing values

We need to check for any missing values in the Toyota Corolla dataset provided using isnull() function. Consequently, the plot below shows that, the dataset is free from any missing values.

![3](https://user-images.githubusercontent.com/32251175/160737020-9fbbd381-42f7-4753-b03b-7c5996b14d75.PNG)

#### C. Transformation of categorical values into numerical values

As regression models only take on numerical variable, it is important that we need to transform categorical variables into numeric variables to feed into the regression model. In this case, Fuel_Type variable identified as categorical variable with three possible values which are CNG, diesel and petrol.

For transformation purpose, we assigned binary value in which 1 and 0 implies the car has the particular fuel type. The following Python script for transformation process shown below.

![4](https://user-images.githubusercontent.com/32251175/160737093-5871e614-8453-4363-a2be-57752cf37361.PNG)

#### D. Correlations evaluation and dimensionality reduction

Following section shown the correlations between variables and carried out dimensionality reductions by removing several variables. Prior to evaluating the correlation, five variables were removed from the dataset. The table belows lists 5 variables removed and reasons for it.

![5](https://user-images.githubusercontent.com/32251175/160737167-2ae47291-7b42-4345-8259-fe4cbad57f0e.PNG)

The correlation plot below is prepared using the heatmap function after the first phase of removal.

![6](https://user-images.githubusercontent.com/32251175/160737243-58b636c9-5cc4-4009-9b98-aa7bcc0a8e7e.PNG)

Following the correlation between variables shown above, dimensionality reduction is performed by removing high cross-correlation variables. Followed with a merge of target variable ‘Price’. It is also noted Age_08_04, KM, Weight, Automatic_airco and Boardcomputer variables have high-correlation, which shows that they are important variables which later will be used in predictive modelling. Age_08_04 and KM have negative relationship with the sale price, which implies that older cars and long KM are more cheaper. Weight implying increase the weight of the car has positive effect on the sale price. Moreover, another features like Automatic_aico, Boardcomputer and Central_Lock have positive linear relationship implying includes these features have positive effect on the sale price.

#### E. Exploration of selected variables against target variables

In this part, each of the selected variables are explored against the target variable ‘Price’. Also, evaluation of the scatter plots of each selected variables against price and the summary statistics of each variables. Please see the following table for explanation on each selected variables against price.

![7](https://user-images.githubusercontent.com/32251175/160738436-55375ab2-9968-4ade-9e97-8e37238d6e0b.PNG)

The figures below shows scatter plot distribution of the selected variables against price prepared in Python. 

![8](https://user-images.githubusercontent.com/32251175/160744621-21e95cf7-cbe2-42e1-bccf-e5aa95449bbc.PNG)
![9](https://user-images.githubusercontent.com/32251175/160744623-25a97ba2-d88e-4850-9fdb-2f66e0b35883.PNG)
![10](https://user-images.githubusercontent.com/32251175/160744629-1ce1f4a6-aa21-47c7-8361-89ba363703d9.PNG)

### Part 2. Regression Technique using Multiple linear regression

#### A. Regression models

In this section, multiple linear regression as a technique is applied for predictive modelling of the case study on Toyota Corolla dataset. As the main task for the predictive modelling is to predict the selling price of used Toyota Corolla using the variables selected in part 1 of this report, therefore, price variable will be used as target variable. 

Prior to building the linear regression models, the dataset was partitioned with ⅔ as the training data sample and ⅓ as the testing data. The trained dataset comprises of 957 training data and 479 testing data. 

![11](https://user-images.githubusercontent.com/32251175/160744920-32d11ce0-c265-4fa9-8eae-8d47c558c9c1.PNG)

This is the process of building a model used backward elimination.

![12](https://user-images.githubusercontent.com/32251175/160744984-d3fa466e-8322-4ff6-bf02-019a59a07f5d.PNG)

From step 1, select a significance level to stay in the model, for example, SL = 0.05 applied in this method. Step 2, fit the full model with all possible predictors. After you fit the model, you will see the one with the highest p-value, so if p-value is greater than significance level then you go to step 4. Step 4 is to remove that predictor. It is to remove basically the variable that has the highest p-value. And step 5, you fit the model without this variable. The model will be rebuild with the fewer number of variables. In step 5, continue to fit the model again with one less variable. This process will keep doing that until it come to a point where the variable of that p-value is still less than significance level, then go to FIN (means model is ready).

##### Regression Model 1

The first regression model technique predictive model has included all of the attributes in the selected variables identified previously section. This model resulted an adjusted R-squared of 0.899 and Root Mean Square Error (RMSE) of 2956.31. The regression and model evaluation result is shown below.

![13](https://user-images.githubusercontent.com/32251175/160751645-fdd661fe-92a0-40f7-9c8f-3ad3e4070c1a.PNG)
![14](https://user-images.githubusercontent.com/32251175/160751649-b2d6c695-884b-4f73-8bd0-8a858d144810.PNG)

##### Regression Model 2

The attributes applied for regression model 2 comprises Age_08_04, KM, HP, Met_Color, Weight, Mfr_Guarantee, BOVAG_Guarantee, Guarantee_Period, ABS, Boardcomputer, Central_Lock, Metallic_Rim. This model resulted an adjusted R-squared of 0.870 and Root Mean Square Error (RMSE) of 1445.83. The regression and model evaluation result is shown below.

![15](https://user-images.githubusercontent.com/32251175/160751824-210cb1d4-f8f0-48d6-8ce3-fff7291973be.PNG)
![16](https://user-images.githubusercontent.com/32251175/160751829-25aa1b1f-a286-45ca-892d-a19b98df95bd.PNG)

