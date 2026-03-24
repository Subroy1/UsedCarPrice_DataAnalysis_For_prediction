# UsedCarPrice_DataAnalysis_For_prediction
Application of various regression algorithms to understand key drivers of used car data price predictions. 

# Data-Driven Insights into Used Car Sales 
**Jupyter Notebook with code, experimentation, further insights, and deployment strategies: https://github.com/Subroy1/UsedCarPrice_DataAnalysis_For_prediction/blob/main/PracticalAssignement2_used_cars_II.ipynb**

## Business Goal

Worldwide, used car sales is a major business occupution due to its ability to provide affordable transportation to millions of citizens.
Though there is no one-size-fits-all solution as location , region , country , availability of public mode of transportation , purpose of owning a car etc and affordability based on demographics also play a part, this exercise makes an effort to understand the fundamental principles of Machine learning algorithm in order to price cars based on available features and derived features with additional application of domain knowledge in this field.
Finally a summary report would be provided to the intended audience namely used car dealers or franchises who would restructure their inventory accordingly to boost sales.

## Data

We dropped five features which have little role to play in model building and are redundant [size, type , region, VIN, id]. In addition , I decided to transform some features into new ones for normalizing the data . The target variable price is also log transformed to cater for large values causing massive imbalance across different car makes and models . 

<img width="868" height="547" alt="image" src="https://github.com/user-attachments/assets/912b4c91-6b06-4d12-910a-e4a2967ee2aa" />


## Modeling and performance
Models Utilized: Baseline Linear Regression, Ridge , Lasso  and Elastic Net were employed to predict used car prices.
Data Preparation: Features underwent preprocessing including imputation, one-hot encoding for categorical variables, and frequency encoding for high-cardinality features like model.
Hyperparameter Tuning: GridSearchCV was applied to Ridge, Lasso, and Elastic Net models to optimize their regularization parameters, although default Ridge performed best .
Best Model: Ridge Regression (with alpha=1 or alpha=0.1) demonstrated the best performance among the tested models with negligible differences
Performance Metrics: The best model achieved an R2 score of approximately 0.65, indicating it explains about 65% of the variance in car prices, with a Root Mean Squared Error (RMSE) of around $8,300 on actual predicted prices.

## Conclusions
The model revealed that there’s a significant relationship between certain features and the target variable 

#### Interesting Findings
Certain manufacturers like 'datsun' and 'ferrari' show exceptional premium, possibly due to rarity or luxury status.
The car's model is second most important feature .
Car condition plays a crucial role; condition_new and cylinders_12
Depreciating Factors: Age (numeric_transformer__age) and odometer readings are consistent depreciators
Fuel Type Influence: Different fuel types exhibit varying negative impacts relative to the reference diesel, indicating a preference for diesel or other unlisted fuel types in the market represented by the dataset.

### Actionable insights
Condition is Key: Dealers should prioritize acquiring and maintaining cars in good to excellent condition, as poor conditions severely degrade value.
Inventory Strategy: Focus on stockpiling inventory for specific manufacturers and models that align with market demand
Age and Mileage Management: Factor in depreciation due to age and high odometer readings when considering trade-ins or sourcing vehicles
Local Market Awareness: Recognize that state-specific pricing trends are significant
Minor Feature Impacts:  fuel type, number of cylinders, transmission, drive type, and paint color 


