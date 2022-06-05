# Phase 2 Project Description



## Overview
My assigned task was to analyze the King County Housing dataset using linear regression models in order to make profitable business decisions for a new real estate development company. The idea of the modeling is to find out what features of a house lead to the highest selling prices. The criteria listed in the dataset that I initially want to look at include: Number of Bedrooms, Number of Bathrooms, Number of Floors, Condition of the house and Square Footage, Grade and Year Built. As we progress with the models we will add or remove features as needed. 

## Business Problem
The housing market has always been competitive, but it can be argued that is more true now than ever. The issue that our clients want us to help them address is with identifying features that give a house the best chance to be highly valued.
Once a developer has this information it can be used to increase profit margins through understanding what features to spend money on for the greatest return. If the developer is in the market of single family new builds then knowing what is the optimal number of floors, bedrooms and bathrooms will help reducing chance of overspending. Furthermore if the business wants to renovate and they know what condition a house has to be in to turn the best profit, they will have a leg up on the competitors. 

### Data Understanding and Cleaning

To begin this process we first will import our data and inspect it. We must make sure there are no missing values or other issues that will keep us from being able to run our regression models. The data we are using was supplied in the github repository and includes all data of single-family home sales from 2014-2015 in King County numbered at over 21,000.

### Modeling

After our dataset is properly cleaned and ready to be used in our models, we begin by using a heatmap to show initial correlations. 
From there we check for multicollinearity and remove the variables that overly correlated to each other to help ensure that the model is not 
negatively effected.

After the inital correlations are explored we start with a baseline model with our target variable, the price, against the highest correlated 
Y-variable, which in this case was above square footage. This model is then iterated over and new models built off of it. 

The models become more complex as more features are added in a search for the most accurate model which will give our clients the best data for
their business decision making.

****

### Regression Results 
The final model which included nearly all features other than 'cond_poor', as well as '5 fair' and lower for 'grade', produced our best all around results.

- While the R-squared of .535 is not quite as high as we would like it, it still has value in explaining approximately 54% of the variance of our target variable, price.
- Our Mean of Absolute Errors, which tell us how much of an error we can predict on average is down immensely to 111,818.
- Our prob(F-statistic) of 0.00 should mean that there is a low probability of achieving these results with the null hypothesis being true, and tells us that our regression is meaningful.
- Our P-values were deemed significant on all features of the final model.
- With all these considerations we can reject the null hypothesis that there is no relationship between the features and the target variable, which is price, at an alpha of 0.05 and confidence level of 95%.
***
## Conclusion
In following the logic of as a X-variable(house features) increases by 1, Y(house price) will increase by coefficient, we see that according to our final model when holding all other variables constant:
  
  - Every square foot of living space added above the basement increases the sale price by    over 161 dollars ($131 for each increase in basement square footage)
   
   
   - Increasing the condition of a home from 'fair' to 'good' can increase the price by $88,388.
   
       -  According to the KC glossary 'fair' is badly worn, while 'good' means no obvious maintenance is needed.
       
       
   
   - Increasing the building grade from 'good' to 'better' can net an increase of $105,660.
       -  According to the KC glossary 'good' is a home just above average while 'better' has architectural design with extra interior and exterior design. 
    
   
   - Adding an extra floor increases the price of a house by $63,160.
   
   
   - The addition of an extra full bathroom can increase the sale price by $57,940.
   ****


