Phase 2 Project 
### Overview
We constructed a linear regression model through an iterative process to determine how house characteristics correlated with sale price. The model was trained and tested on a dataset containing 21,597 sales of houses in King County, Washington from May 2014 to May 2015. This model can be used by real estate companies, such as Every Door Real Estate, to determine appropriate housing prices from a house's features. Setting the right price for a house can improve sales and comissions for that company. We used recursive feature elimination with cross-validation to decide which features to include in our model. Our final model had an  𝑅2  of 0.80, explaining of the variance in price. The RMSE, the average error of our model in units of price, was $161,112. Two of our key measures were renovations and home condition. All else held equal, a house that has been renovated has a mean price of $20,000 greater than houses that were not renovated. All else held equal, a house in very good condition has a mean price of $54,000 greater than average.

### Business Problem
In the housing market, home sellers and realtors have different goals. A seller's ultimate goal is to sell the house at the highest price. A real estate agent's goal is to sell a higher volume of properties in order to maximize commissions. There is a fine balance between these two goals: the agent aims to sell the property as quickly as possible, but at a high enough value to satisfy their client. A realistic understanding of home prices is a necessity to optimize this tradeoff.

Our client is Every Door Real Estate, a real estate company in Seattle, Washington. Every Door Real Estate represents individuals selling their moderately price homes. This project aims at developing a linear regression model to help Every Door understand how different home features correlate with home prices. The model is constructed using historical home sales in King County, Washington. Every Door can use this model to determine an appropriate range of values for a home based upon its characteristics. This information can be used to determine how much a home is valued on the market and whether a home seller is over- or under-valuing their property.

### Data Understanding
For this analysis, we will utilize the "King County Housing Price from May 2014- May 2015" created by the Center for Spatial Data Science (https://spatial.uchicago.edu). It contains 21,597 entries with 21 different columns about home sales in the Seattle metropolitan area. We've included some descriptive statistics. This dataset provides us with information suitable for linear regression analysis to predict home prices in the Seattle metroplitan area. This robust dataset contains information about previous home selling prices along with multiple features of the home at time of sale. One limitation of this dataset - is that it represents a single year of data, another limitation is that it isnt current data. Ideally to make relevant and accurate predictions we'd need data that is current. Even if this data is not particularly useful at captuing current market trends, it is still useful at helping us evaluate if linear regression is a good fit to model these relationships.

### Conclusion
Our home price prediction model helps improve agency commissions for Every Door Real Estate’s by solving the problem of competing incentives between home seller and listing agency. While traditional approaches to valuing homes can lead to sellers over-valuing their homes and dragging out the sale process as a result, our home prediction model prices homes to sell which improves the volume of sales the agency is able to process. Our model provides statistical backing to agents as they push back on unrealistic client expectations. Additionally, our model identifies categories of home improvement that boost a home’s value which improves client satisfaction and commission value.

### Data
To build a model suited for the demands of Every Door Real Estate, a Seattle based real estate agency, we analyzed a data set of 22K home sales from the Seattle Metro area between 2014 and 2015.

### Model Approach 
Knowing the model would be deployed by agents in their work with homeowners, we needed to produce a model that agents could use to accurately estimate the value of a client’s home and provide insight into what factors led to their estimate while pointing to potential home improvements to boost the predicted value. We tested 7 iterations of our model looking for the right combination of home attributes to give us a balance these factors

### Prediction accuracy (R2)
Prediction precision (variance between train & test)
Statistical significance (p-values of our coefficients)
Alignment with assumptions of linear regressions
Linearity: linear relationship between the response variable (Y) and predictor (X)
Homoscedasticity: residuals are evenly spread across range of predicted values
Independence: observations are independent of each other
Normality: model residuals should follow a normal distribution
Ability to draw inferential conclusions from the coefficients
Coefficients that were in the purview of homeowners to improve
Our final model included the features; 'sqft_living', 'waterfront','bedrooms', 'was_renovated', 'bed_bath_ratio','ratio_sqft_living_lot','sqft_living_to_bathroom_ratio', 'condition', and 'zipcode'

### Model Results
Our final model has an mean R2 of 0.81 and 0.78 for the train and test respectively giving the Every Door Real Estate the power to predict about 80% of the fluctuation in home value based on criteria they pass into the model. Our root mean squared error is $ 161,112 meaning our home price prediction off by $161,112 on average which is reasonable given the range of home prices we trained our data on ($78 K to $7.7MM). Our model is precise with small differences in the R2 between our train and test split. Each of our model coefficients are statistically significant with P-values significantly less than 0.05 Our model conforms with each of the assumptions for linear regressions except some issues with colinearity

### Limitations & Next Steps
Our model has a 20% error. With further feature engineering we could reduce our error and create a more predictive model. Specifically, we would further explore the interaction between home condition and renovation to eliminate potential collinearity.

As mentioned in our introduction, we analyzed 1 year of sales data from 2014 to 2015, with additional and more recent data we could update the model to be more relevant to today’s market.

With additional input from Open Door, we could further limit the scope of the model to focus on their target market which would produce a more limited but more accurate model.
