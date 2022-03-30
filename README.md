# Kevin Park Portfolio               
Welcome to my data science portfolio. I am passionate about data analytics, data visualization, and behavioral economics.

## Project 1: Price prediction and understanding contributing features (Carsales data sets)

The aim of this project is to build predictive models to facilitate decision making for second hand car buyers and sellers. The project implemented predictive models on actual data from [Carsales](https://www.carsales.com.au/). Multiple Linear, Random Forest and Neural Network predictive modelling techniques were employed to create predictive models. Moreover, we drill down car categories to discover the price influencing features on different car makes. 

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

![8](https://user-images.githubusercontent.com/32251175/160744242-4b10c001-76b0-4f6f-be19-753f16e2b3e4.PNG)
![9](https://user-images.githubusercontent.com/32251175/160744252-f10e0fac-c265-4f32-8034-1b33a7ee61eb.PNG)
![10](https://user-images.githubusercontent.com/32251175/160744258-6b33dfd2-e98f-4fa9-b51d-c6a2165a500f.PNG)



