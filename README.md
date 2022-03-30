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

