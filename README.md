# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) 222-Flex Ames Competition - Predicting the Housing Sale Price

# Problem Statement
Profit of iBuyer companies rely on selling real estate properties at higher prices than the prices that the properties were bought. In such cases, accurate predictions of housing property market prices are key in securing profit from the real estate transactions. This project seeks to explore the various features of housing properties and find out which features can most accurately predict the housing sales prices, specifically for Ames, IA.


# Background
Buying a house has long been a popular investment option and it is generally believed that buying a home is a great investment. iBuyers are investors that use automated valuation models (AVMs) and other technology to make quick offers on homes, and then resell them ([*source*](https://blog.offerpad.com/what-is-an-ibuyer/?utm_source=google&utm_medium=cpc&utm_campaign=pmax-stlouis&gclid=Cj0KCQjwpImTBhCmARIsAKr58cwChC4Im8uIEXN0Qs36ar3oNoiXC1SO4MU0p6bhAJTNXVI9Wr2bCDUaAlksEALw_wcB)). Such companies profit from buying the property at a lower price than at sale; therefore, in order to secure profit, it is important to be able to accurately predict the market price of the property, so that they can make an offer that is reasonably balance for both the company and the seller. 
An example of failed case of this is Zillow Offers program; the program announced to "wind down" due to their failure in accurately predicting the home prices and purchasing the properties at a higher than the market sales price([*source*](https://wraltechwire.com/2021/11/02/zillow-unable-to-predict-housing-prices-to-wind-down-offers-program-everywhere/)). 

Home prices are indeed volatile, hugely affected by both intrinsic(quality of the home itself), and extrinsic(economic) factors([*source*](https://www.opendoor.com/w/blog/factors-that-influence-home-value)). Intrinsically, it is generally affected by age, condition, neighborhood, usage space, and etc. This particular project will focus on such intrinsic features as indicators of the housing sale price, and see which features we can look at to accurately predict the housing prices. 

# Data 

#### Datasets Used:
- Ames Housing Data: individual residential properties sold in Ames, IA from 2006 to 2010.

    * [train.csv](../data/train.csv) - all of the training data for the model. 
    * [test.csv](../data/test.csv) - the test data for your model used to feed into the regression model to make predictions.
    
#### Data Dictionary 
[*Ames Housing Data Dictionary*](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)


# Analysis
Using filtering method for feature selection, the model incorporates total of 21 features to predict the housing sale price. The features selected goes along with the general idea that the housing price depends on neighborhood, environment, quality of materials, age of the house, and surface area indicative of the usage space. 

The type of the final regression model was chosen to be the elastic net regression, which gave the smallest error output by a small number. Polynomial interaction feature of degree=3 was added, as it was found to have the best fit using the grid search. In the end, the final model had about 0.92 training R-squared score and 0.9 testing R-squared score. This indicates that there is more variability than bias. 

# Conclusions
----
#### Profit of iBuyer companies rely on selling real estate properties at higher prices than the prices that the properties were bought. In such cases, accurate predictions of housing property market prices are key in securing profit from the real estate transactions. This project seeks to explore the various features of housing properties and find out which features can most accurately predict the housing sales prices, specifically for Ames, IA.
----
This project aims to build a reliable model for predicting the housing price that can be used to profit from real estate investment for iBuyer companies. Making use of 21 housing features total, I was able to build a prediction model with R-Squared value of about 0.9, which means that about 90% of the instances fit the model, given the 21 features that were used. The model had higher variance than bias, which indicates that it was more overfit to the training data. As this is a predictive model, I may have to work towards less variance, possibly by reducing the features by even more. 

Also going forward, it might be helpful to examine external features that affect housing prices. Housing sales price depends not only on the internal qualities of houses, but more so on the external factors of the economy. Extra steps to connsider economic factors such as supply, demand, and the inflation will most certainly be needed in order to more accurately predict the sales price of houses. 