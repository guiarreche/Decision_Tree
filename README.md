# Chatbot based on Decision_Tree project

OVERVIEW

Project that simulates a decision tree to help the customer check house prices in a certain region, the customer must respond some questions with yes or no, and then the chatbot will return wether the price is cheap, average, or expensive. The answer given to the customer is based on a decision tree based on a database from house prices, in which the classification method consists in finding the GINI Index that measures the impurity of picking a random sample, the coefficient varies between 0 and 1, in which 0 represents purity and 1 impurity.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

HOW WE CREATED THE DECISION TREE

1 - FILTER THE TABLE
We used the house price database found in the USEFUL LINKS, using all the columns besides DATE, YEAR RENOVATED, ZIP CODE, LATITUDE, LONGITUDE, SQFT LIVING 15, SQFT LOT 15. 
TOOL USED: Pandas. (See in Tratamento.ipynb) 

2 - USING THE FUNCTION SCALE TO NORMALIZE VALUES BETWEEN 0 and 1 to all table values.
TOOL USED: We used the sklearn to achieve that. (See in Tratamento.ipynb)

3 - FINDING THE WEIGHTS OF WHICH COLUMN.
We used a method of portfolio analysis called CAPM, which is used very often for pricification models and investments, and then we used the solver tool from excel to find the coefficients. (See in formacao_preco.xlsx)

Note: We found that the column BEDROOMS had 0 weight at the end.

4 - CATEGORIZATION OF CHEAP, AVERAGE, AND EXPENSIVE.
We used the coefficients that we found on excel , and multiplied those them to each respective column, after that we put them in a equation which consists in the column PRICE divided by each of the columns. (See in Tratamento.ipynb)

5 - USING THE DECISION TREE TO CREATE A CHATBOT
At the end we wrote a csv file (See in arvore.csv and arvore.jfif) with the tree information to feed our chatbot (See in Bot.ipynb).

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

USEFUL LINKS

Links:
The database used was found in this open directory using the zipcode: 98070 from the website https://www.kaggle.com/c/house-prices-advanced-regression-techniques. 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

CONTRIBUTORS

@guiarreche
@Custodiovjoao
@leonardoferretti
