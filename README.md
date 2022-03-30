# Kevin Park          
Welcome to my data science portfolio. I am passionate about data analytics, data visualization, and behavioral economics.

## Project 1 - Data analysis with predictive models in category based on [Carsales](https://www.carsales.com.au) datasets

* This project is to build a tool to analyse, compare, predict and visualize the important features and price of different car categories or makes.
* The aim of this project is to build such predictive models to facilitate decision making for second hand car buyers and sellers.
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

