# Online-Retail-Customer-Segmentation
Project Overview
This project focuses on identifying major customer segments for a UK-based online retailer specializing in unique all-occasion gifts. Utilizing transaction data from 01/12/2010 to 09/12/2011, the goal is to analyze purchasing patterns to segment customers effectively for targeted marketing and strategic business decisions.

Dataset Description
The dataset includes 541,909 rows and 8 columns with the following details:

InvoiceNo: Unique identifier for each invoice
StockCode: Unique code for each product
Description: Text description of the product
Quantity: Number of items purchased
InvoiceDate: Date and time of invoice generation
UnitPrice: Price per unit of the product
CustomerID: Unique identifier for the customer
Country: Country of the customer
Note: The dataset contains 5,268 duplicate values, 1,454 null values in 'Description', and 135,080 missing values in 'CustomerID'.

Data Preparation
Missing Values: Replaced null values in Description with 'No Description' and dropped rows with missing CustomerID.
Data Type Conversion: Converted InvoiceDate to datetime format.
Duplicate Removal: Removed duplicate rows.
Filtering: Excluded rows with negative quantities.
New Columns: Added TotalPrice by multiplying Quantity and UnitPrice.
Text Standardization: Converted text in Description and Country to uppercase.
Insights
Geographical Sales Distribution: The UK has the highest total sales, with notable contributions from the Netherlands, Australia, and Japan.
Product Contribution: Significant sales from 'Paper Craft Little Birdie', 'Medium Ceramic Top Storage Jar', and 'World War 2 Glider Asstd Designs'.
Sales Patterns: Highest sales on Thursday, peak sales in November, and lowest in February.
Customer Behavior: Most customers make a few purchases, while a small number make many. Most products are sold at lower prices.
Machine Learning Models Used
Hierarchical Clustering: Silhouette Score: 0.7827, Davies-Bouldin Index: 0.5503
Hierarchical Clustering with GridSearchCV: Silhouette Score: 0.9384, Davies-Bouldin Index: 0.5193
K-Means Clustering: Silhouette Score: 0.9285
K-Means Clustering with GridSearchCV: Silhouette Score: 0.9949
DBSCAN: Silhouette Score: 0.9210
DBSCAN with RandomizedSearchCV: Silhouette Score: 0.9643
Model Selection: K-Means Clustering with GridSearchCV was chosen for its highest Silhouette Score, indicating well-defined and distinct clusters.

Conclusion
The analysis effectively segmented customers, providing actionable insights for targeted marketing. The K-Means Clustering model with GridSearchCV, achieving a Silhouette Score of 0.9949, offered the most accurate customer segmentation.



