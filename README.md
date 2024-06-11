# Customer-Segmentation-in-Excel
This project uses RFM to segment customers into different categories using excel.

# Introduction

Every business aims to maximise profit. Profit maximisation is easier when the right product is targeted at the right customer. This project aims to categorise customers based on their Recency, Frequency and Monetary (RFM) score. The Recency score is determined by the last transaction of the customer relative to the last transaction date of the data set. The Frequency score is determined by the number of transactions done by the customer and the Monetary score is determined by the total amount the customer has spent and by inference the profit made based on the customer's transactions. Categorising the customers will then inform the product marketing that would be targeted at the customers. 

# Workflow Diagram
![WorkFlow Diagram](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/971626c1-5b15-45c6-914d-e0c8aa58cd89)

# Data Source
The data set used for this project was obtained from the KPMG Data Analytics virtual internship from The Forage website at https://www.theforage.com/. The file is of the format .xlsx containing four tables on different sheets. The data was provided by an Australian hypothetical Bike and Cycling accessories company known as Sprocket Central Pty Ltd.

# Data Storage
The file was downloaded as .xlsx file and was saved on a local machine.

# Data Cleaning and Processing
The downloaded file contained three dimension tables and one fact table as listed below. 

## Transaction Table
This table consists of 20000 rows of information on transaction of Sprocket Central Pty Ltd.

## New Customers Table
This table consists of the details of 100o new customers of Sprocket Central Pty Ltd.

## Customer Demographic Table
This table consists of the information of 4000 old customers of Sprocket Central Pty Ltd.

## Customers' Address
This table consits of information on the addresses of 3999 of the customers of Sprocket Central Pty Ltd.

# Data cleaning
## Data quality
The data sets were checked for the dimensions of quality data. This check include Accuracy, Completeness, Consistency, Currency, Relevance, Validity, adn Uniqueness. These are explained further below.

### Accuracy
The profit column has not been included in the transaction table. This would have been better completed with an extra column indicating the profit. Also, the CustomerDemographic table had no age column, and a particular customer had an inaccurate DOB.
Mitigation: The inaccurate DOB that was filtered out, extra columns were created for profit and age.

### Completeness
Missing records were identified in some columns of the transaction table, NewCustomerList and the CustomerDemographic table.
Mitigation: The columns with blanks were filtered out.

### Consistency
Data labels such as those of gender from the customerDemographic table and states from the customerAddress tables were inconsistent.  
Mitigation: The gender column was made consistent by replacing all the data points representing male and female with ‘Male’ and ‘Female’ respectively. In the same vein, NSW, VIC and QLD were used for the states in the customerAddress table.

*	Currency
The deceased information column on the customerDemographic table was not needed.
Mitigation: The row with deceased client was filtered out.
Recommendation: Deceased client should not be included in tables needed for data analysis as this is not needed for analysis for business purposes.

*	Relevance
The default column in the customerDemographic table holds no valuable information and thus is irrelevant for analysis. Also, cancelled orders was not required for analysis.
Mitigation: The default column was removed, and the cancelled orders were filtered out.
Recommendation: The cancelled orders should be stored in a separate data base and not the ones needed for future analysis, so it doesn’t accidentally influence the outcome of analysis used to take future business decisions.

*	Validity
The data types of some columns such as list_price and standard_cost in the Transactions table and DOB in the customerDemographic table are not appropriate.
Mitigation: The data types for these columns were changed to appropriate data types.
Recommendation: Data can be stored using the right data types for analysis purposes.



