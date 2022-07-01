# Regression Tree Modeling for your Sales Predictions
## Finding Patterns and solutions for increased sales performance with Machine Learning

**Author**: Steven Shiroma

### Business problem:

Finding the best predictions for your current sales needs is important! Using my modeling system can improve business decisions.


### Data:

Link to raw data may be found here:
https://drive.google.com/file/d/1199k_srUmEbPv4THVPwxRgQdDTUxkpWz/view?usp=sharing
and the original source here:
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

Target:
Outlet sales per item in 100-1,000$ range.

Features:

Item Identifier(Not used in model)

Item weight

Item Fat Content
	Low Fat
	Regular

Item Visibility

Item Type: These categories included

	Baking Goods
	Breads
	Breakfast
	Canned
	Dairy
	Frozen Foods
	Fruits and Vegetables
	Hard Drinks
	Health and Hygiene
	Household
	Meat
	Others
	Seafood
	Snack Foods
	Soft Drinks
	Starchy Foods

Item MRP (Market Retail Price)
	ranges from 0 - 300$

Outlet Identifier
	Identifies between ten different outlet brands.

Outlet Establishment Year

Outlet Size
	Small Medium or High

Outlet Location type
	Tier 1, Tier2, Tier 3

Outlet Type
	Supermarket Type 1, Super Market Type 2, Super Market Type 3, Grocery store




## Methods
- Data preparation steps with explanation and justification for choices

- Ordinal encoded incorrect Item Fat Content labels.

 -About 1/8th of the Item Weights were missing and imputed with the Median stategy

 -About 1/4th of the Outlet Sizes were missing and imputed with the Most Frequent strategy

 - Dummy Model instantiated and performed as expected and is a poor condidate.

 - Linear Regression Model applied and performed OK.

 - Regression Tree Model applied and performed marginally better than Linear Regression Model.


## Results
 - Dummy Baseline Model
  -Model Training R2: 0.56
  -Model Testing R2: 0.57
  
  -Model Training MSE: 1297236.374852866
  -Model Testing MSE: 1194586.954134335
  
  -Model Training MRSE: 1138.9628505148296
  -Model Testing MRSE: 1092.971616344329


 - Linear Regression Model applied, and performed OK, 
	-Model Training R2: 0.56
	-Model Testing R2: 0.57

	-Model Training MSE: 1297236.374852866
	-Model Testing MSE: 1194586.954134335

	-Model Training MRSE: 1138.9628505148296
	-Model Testing MRSE: 1092.971616344329


 - Regression Tree model applied and performed marginally better
	Hyerparameters: A Max Depth of 5 was selected.
	
	-Training Model R2 0.62
	-Testing Model R2 0.58

	-Model Training MSE: 1138739.418683952
	-Model Testing MSE: 1146473.1774573105

	-Model Training MRSE: 1067.1173406350174
	-Model Testing MRSE: 1070.7348772956407

### Here are examples of how to embed images from your sub-folder


#### Sales of Each Item Type
![download](https://user-images.githubusercontent.com/95104650/176814142-ea60807a-787e-4220-bd49-8aaece7c9a64.png)


 -Here I am comparing the different item types to their overall sales to determine which items yield better sales. Starchy foods are a clear top contender for best sales.
 

#### Item Sales v.s. their MRP
![download](https://user-images.githubusercontent.com/95104650/176815598-3a6bda06-3cf7-4748-8032-c0ce48c4373c.png)

 -Here you can see the sales of different store types(Color coordinated via the legnd). Grocery stores are generating the least profit per item while Supermarket Type 3's have the highest sales recorded.


## Model

My choice for the final model would be the Regression Tree Model, for it's slightly higher performance.

 - Regression Tree model applied and performed marginally better
	Hyerparameters: A Max Depth of 5 was selected.
	
	-Training Model R2 0.62
	-Testing Model R2 0.58

	-Model Training MSE: 1138739.418683952
	-Model Testing MSE: 1146473.1774573105

	-Model Training MRSE: 1067.1173406350174
	-Model Testing MRSE: 1070.7348772956407

-with an rmse of around 1000$ could relatively predict the sales of items sold at various types and sizes of stores.


## Recommendations:

I recommend using this model to predict sales forecasts for these types of supermarkets. 


## Limitations & Next Steps

For this data set I was limited by the inconsistencies and lack of data, with more correlated data it is possible to further provide better predictive modeling.
This model is limited to only these types and sizes of Market stores, and should only be deployed on such to predict sales.
The next step should be to gather more data and for more accuracy, settle one predicting only the supermarket or grocery market types as they have very different sales.


### For further information


For any additional questions, please contact **Stevenpshiroma@gmail.com**
