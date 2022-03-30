# Kevin PaRK Portfolio                 
Welcome to my data science portfolio. I am passionate about data analytics, data visualization, and behavioral economics.

## Predictive models in Category based Data analysis using Carsales data sets
The market price of a second hand car is determined by many aspects. Buyers and sellers can find an overwhelming amount of such information scattered over the internet. There is no one tool to analyse, compare, predict and visualise the important features and price of different car categories or makes. For buyers, they can know what features can expect for the price they are willing to pay for the car. For sellers, they can know how much they can receive for the car to be sold. 

The aim of this project is to build such predictive models to facilitate decision making for second hand car buyers and sellers. The study implemented predictive models on actual data from Carsales second hand car sale site. Multiple Linear, Random Forest and Neural Network predictive modelling techniques were employed to create predictive models. Using real dataset from Carsales, we observe contributing features in category into different levels of prestige - luxury sports, luxury and economy cars. Moreover, we drill down car categories to discover the price influencing features on different car makes. 

There are findings based upon the methodology in this project: 
1. using real data and modelling categories shows that the same model is not effective for all cars. 
2. predictive modelling technique performance was depends on the car category and make. 
3. the importance of car features change according to each car category and make. 

This research will investigate those factors based on Carsales data, and make models for the above categories. And observe if there is a difference in the contributing features to the final price. If interesting car features are different for different car classifications (economy/luxury/high-end luxury) that says the buyers are different for each classification. 

At first, we have to extract data from Carsales second hand car sale site. Using real data from Carsales, we will discover the most suitable predictive model to see a difference in the contributing features to the final price. There will be three predictive regression models used - Multiple linear, Random Decision Tree and Neural Network regression to build, test the models and identify which model does the best predictions. The algorithms and programs upon methodology for this research, all uses in Python. The reason is that it provides better in terms of productivity, which can implement algorithms for production use where can integrated into web pages or production database. 

The process of building predictive models for this research shown below.
a) Scrape sample Toyota Corolla dataset from Carsales.com.au to build and test the models for predicting sale price and identify which model does the best predictions.

b) Build predictive models and observe importance features for different categories in level of prestige of car brand - luxury sports / luxury / economy cars

c) Drill down the categorized data to see features of individual makes. Build predictive models and observe importance features compared with categorized dataset.

For Part a) will employ predictive models into a real life car sales site from Carsales and exhibit its effectiveness and feasibility. For Part b), we will observe importance features for different categories in level of prestige of car brand - luxury sports / luxury / economy cars. Moreover, we will drill down those categorized data to see features of individual makes.

Following are expected outcomes and significance to identify from part a).

1. scraping data from Carsales.com.au; it will extract data of Toyota Corolla car brand from Carsales.

2. pre-processing part from dataset; it will examine the prices of a specific car and explore the distribution of the prices. For example, evaluate the correlations between the variables, and explore the distribution of selected variables against price variables, etc.

3. build a multiple linear regression model with the selected variables; it will try at least three linear regression models to identify the optimal model and evaluate the performance of the regression model.

4. build a random decision tree model with the selected variables;  it will try at least three random decision trees regression models with different complexity parameters to obtain the optimal tree and evaluate the model performance.

5. build a neural network regression model with the selected variables; it will try at least three neural network regression models to identify the optimal model and evaluate the performance of the regression model.

6. compare the performance of the optimal regression from multiple linear, decision tree and neural network and discuss, justify the most suitable predictive model.

Following are expected outcomes and significance to identify from part b).

1. data extraction from Carsales.com.au; it will extract data at least three Individual car makes will be collected with selected variables in each category. Individual car makes dataset in each category example shown below.

![Capture](https://user-images.githubusercontent.com/32251175/160735385-38721775-6c7b-4205-99cc-0314b4f154bf.PNG)

2. build predictive models using multiple Linear, random forest and neural network regression techniques for each categorized dataset - Luxury Sports / Luxury / Economy

3. compare the performance from multiple linear, decision tree and neural network and discuss, justify the most suitable predictive models from those categorized dataset.

4. drill down those categorized data into individual car makes, for example, build predictive models for only Lamborghini car brands.

5. compare the performance of predictive models from categorized data and individual makes and discuss.

6. compare those categorized data to see importance features compared to  individual makes and  discuss.

