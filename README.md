
**A regression challenge** is designed to test your understanding of the topics you learned in class while putting you to the test using actual, messy, and huge data.
For this project, a regression model is used to forecast Bangkok housing prices using data from 2023, enabling the ability for investors and potential homebuyers to make informed, data-science-based decisions which is tested against unseen real housing data for evaluation on Kaggle.
The 


**Lasso regression** is an effective tool for building predictive models, particularly in scenarios with many features or potential overfitting concerns. The combination of regularization and automatic feature selection makes the Lasso Regression a preferred choice in for many applications, especially when model interpretability is important.
In this project, the metric used to evaluate the model is the **root mean squared error (RMSE)**, in which the Lasso model obtained the best score compared to the OLS and RANSAC (Random Sample Consensus).


All calculations aim to answer the following problem statement, 
"Which property characteristics and market conditions have the greatest impact on current residential housing prices in Bangkok, to help homebuyers and property investors make informed investment decisions?"
data dictionary:

| Column Name                   | Data Type   | Description                                | Example                              |
|-------------------------------|-------------|--------------------------------------------|--------------------------------------|
| id                            | int64       | Unique identifier for each property        | 1                                    |
| province                      | object      | Province where the property is located     | Bangkok, Nonthaburi, Samut Prakan   |
| district                      | object      | District where the property is located     | Ratchathewi                          |
| property_type                 | object      | Type of property                           | Condo, Detached House, Townhouse     |
| bedrooms                      | float64     | Number of bedrooms in the property         | 2.0                                  |
| baths                         | float64     | Number of bathrooms in the property        | 1.0                                  |
| floor_area                    | int64       | Floor area of the property in square meters| 50                                   |
| log_floor_area                | float64     | Log-transformed floor area                 | 3.912                                |
| floor_level                   | float64     | Level of the floor (0 if not Condo)       | 5.0                                  |
| land_area                     | float64     | Land area of the property in square meters (0 if Condo)| 100                        |
| log_land_area                 | float64     | Log-transformed land area (0 if Condo)    | 4.605                                |
| nearby_stations               | int64       | Number of nearby stations                  | 2                                    |
| nearest_station_name          | object      | Name of the nearest station (NaN if not any) | BL22 Sukhumvit MRT                |
| nearest_station_distance       | int64       | Distance to the nearest station in meters (0 if not any) | 500                          |
| nearby_supermarkets           | float64     | Number of nearby supermarkets               | 1.0                                  |
| has_many_bedrooms             | int64       | Indicator if it has many bedrooms (1/0)   | 1                                    |
| has_many_baths                | int64       | Indicator if it has many baths (1/0)      | 0                                    |
| has_bus_stops                 | int64       | Indicator if it is near bus stops (1/0)   | 1                                    |
| year_built_bin                | category    | Year built categorized (e.g., before 2000, between 2011 and 2015) | 2011_2015          |
| has_security                  | int64       | Indicator if there is security (1/0)      | 1                                    |
| has_pool                      | int64       | Indicator if there is a pool (1/0)        | 0                                    |
| has_sports                    | int64       | Indicator if there are sports facilities (1/0)| 1                               |
| has_parking                   | int64       | Indicator if there is parking (1/0)       | 1                                    |
| price                         | float64     | Price of the property (NaN if testing data)| 3,500,000                            |
| is_train                      | int64       | Indicator if it is a training data (1/0)  | 1                                    |

