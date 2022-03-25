# Kevin Portfolio                 
Welcome to my data science portfolio. I am passionate about data analytics, data visualization, and behavioral economics.

## Project 1: Predictive models in Category based Carsales data sets
The aim is to build predictive models to facilitate decision making for second hand car buyers and sellers. This project is implemented predictive models on actual data from Carsales second hand car sale site. 

Multiple Linear, Random Forest and Neural Network predictive modelling techniques were employed to create predictive models. 

Using real dataset from Carsales, we will observe contributing features in category into different levels of prestige - luxury sports, luxury and economy cars. Moreover, we drill down car categories to discover the price influencing features on different car makes. 

1. data extraction from Carsales.com.au; it will extract data at least three Individual car makes will be collected with selected variables in each category

| Categorized dataset       | Included individual car makes                          |
| ------------------------- |:-----------------------------------------------------: |
| Luxury Sports             | Lamborghini, Ferrari and Porsche                       |
| Luxury                    | BMW C-class, Mercedes-Benz E series and Audi A8 series |

2. build predictive models using multiple Linear, random forest and neural network regression techniques for each categorized dataset - Luxury Sports / Luxury / Economy

3. compare the performance from multiple linear, decision tree and neural network and discuss, justify the most suitable predictive models from those categorized dataset.

4. drill down those categorized data into individual car makes, for example, build predictive models for only Lamborghini car brands.

5. compare the performance of predictive models from categorized data and individual makes and discuss.

6. compare those categorized data to see importance features compared to  individual makes and  discuss.

### Part 1. Dataset
```python
dataset['price'].describe()
```
<img width="609" alt="image32" src="https://user-images.githubusercontent.com/32251175/160059949-3aa8d530-c2e9-4687-b273-7abab63c930b.png">
<img width="418" alt="image33" src="https://user-images.githubusercontent.com/32251175/160059965-77b5c48f-323c-4b13-8094-c9a9ff8d848a.png">
<img width="396" alt="image57" src="https://user-images.githubusercontent.com/32251175/160060007-69a70460-2f17-41c0-adf8-8b2dd2d28eb0.png">

