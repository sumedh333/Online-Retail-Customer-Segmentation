# Online-Retail-Customer-Segmentation
Project Overview
This project aims to identify major customer segments within a transnational dataset containing all transactions from 01/12/2010 to 09/12/2011 for a UK-based non-store online retailer specializing in unique all-occasion gifts. The dataset includes 541,909 rows and 8 columns, representing various transaction details, such as product descriptions, quantities, unit prices, and customer IDs. The primary goal is to analyze purchasing patterns to distinguish different customer groups, including wholesalers, for targeted marketing and strategic business decisions.

Dataset Description
InvoiceNo: Unique identifier for each invoice.
StockCode: Unique code for each product.
Description: Text description of the product.
Quantity: Number of items of the product.
InvoiceDate: Date and time of invoice generation.
UnitPrice: Price per unit of the product.
CustomerID: Unique identifier for the customer.
Country: Country of the customer.
The dataset contains 5,268 duplicate values and 1,454 null values in the 'Description' column. Additionally, there are 135,080 missing values in the 'CustomerID' column.

Insights from Data Analysis
Geographical Sales Distribution: The United Kingdom has the highest total sales, significantly more than other countries. The Netherlands, Australia, and Japan have higher average order values, indicating more spending per transaction.
Product Contribution: Products like 'Paper Craft Little Birdie', 'Medium Ceramic Top Storage Jar', and 'World War 2 Glider Asstd Designs' contribute significantly to overall sales volume.
Sales by Day: Thursday has the highest sales, while Saturday has the lowest.
Monthly Sales Variation: Sales peak in November and are lowest in February.
Customer Purchasing Behavior: Most customers make few purchases, whereas a small number of customers make many purchases.
Product Pricing: Most products are sold at lower prices, with a few high-priced items.
Machine Learning Models Used
Linear Regression

Performance:
MSE: 1408.44
R² Score: 0.00015
Linear Regression with GridSearchCV

Performance:
MSE: 1408.44
R² Score: 0.00015
RandomForestRegressor

Performance:
MSE: 1658.94
R² Score: 0.0374
RandomForestRegressor with RandomizedSearchCV

Performance:
MSE: 1380.75
R² Score: 0.0234
Gradient Boosting Regressor

Performance:
MSE: 1400.37
R² Score: 0.0096
Gradient Boosting Regressor with GridSearchCV

Performance:
MSE: 1406.61
R² Score: 0.0051
Model Selection
RandomForestRegressor with RandomizedSearchCV was chosen as the final prediction model. Here’s why:

Lowest Mean Squared Error (MSE): 1380.75, indicating fewer prediction errors.
Reasonable R-squared (R²): 0.0234, which, although not the highest, is still acceptable.
Reason for Selection:
Lower MSE: Indicates fewer prediction errors, leading to more accurate forecasts.
Balanced Performance: Despite R² not being the highest, the significant reduction in MSE outweighs the slight drop in R².
Model Explainability
To ensure transparency and understand the importance of different features in the RandomForestRegressor model, we used SHAP (SHapley Additive exPlanations) values. SHAP provides detailed insights into the contribution of each feature to the model’s predictions, which helps in making informed business decisions.
