# Customer-Segmentation-in-Excel
This project uses RFM to segment customers into different categories using Microsoft Excel.

# Introduction

Every business aims to maximise profit. Profit maximisation is easier when the right product is targeted at the right customer. This project aims to categorise customers based on their Recency, Frequency and Monetary (RFM) score. The Recency score is determined by the last transaction of the customer relative to the last transaction date of the data set. The Frequency score is determined by the number of transactions done by the customer and the Monetary score is determined by the total amount the customer has spent and by inference the profit made based on the customer's transactions. Categorising the customers will then inform the product marketing that would be targeted at the customers. 

# Workflow Diagram

![Workflow Diagram](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/70f0e220-b2bc-47cb-8c65-92259fe5f324)


# Data Source
The data set used for this project was obtained from the KPMG Data Analytics virtual internship from The Forage website at https://www.theforage.com/. The file is of the format .xlsx containing four tables on different sheets. The data was provided by an Australian hypothetical Bike and Cycling accessories company known as Sprocket Central Pty Ltd.

# Data Ingestion and Storage
The file was downloaded as an xlsx file and was stored on a local machine.

# Data Cleaning
The downloaded file contained three dimension tables and one fact table as listed below. 

## Transaction Table
This table is a fact table. It consists of 20000 rows of information on transaction of Sprocket Central Pty Ltd.

## New Customers Table
This table is a dimension table. It consists of the details of 100o new customers of Sprocket Central Pty Ltd.

## Customer Demographic Table
This table is a dimensio table. It consists of the information of 4000 old customers of Sprocket Central Pty Ltd.

## Customers' Address
This table is a dimension table. It consits of information on the addresses of 3999 of the customers of Sprocket Central Pty Ltd.

# Data cleaning
The data sets were checked for the dimensions of quality data. This check include Accuracy, Completeness, Consistency, Currency, Relevance, Validity, adn Uniqueness. These are explained further below. Data cleaning is an important aspect of data anaysis and analytics as it determines the quality of outcome of analsysis. A clean data yields better outcomes. Decisions taken on these outcomes enhance productivity and profit.

## Accuracy
The profit column was not included in the transaction table. This would have been better completed with an extra column indicating the profit. Also, the CustomerDemographic table had no age column, and a particular customer had an inaccurate DOB.
Mitigation: The inaccurate DOB that was filtered out, extra columns were created for profit and age.

![image](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/97513a73-cb9e-4fc6-bb58-1b14afe23ff9)


## Completeness
Missing records were identified in some columns of the transaction table, NewCustomerList and the CustomerDemographic table.
Mitigation: The columns with blanks were filtered out.

![image](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/10093625-9c75-4adb-a752-967d015ffcb9)

## Consistency
Data labels such as those of gender from the customerDemographic table and states from the customerAddress tables were inconsistent.  
Mitigation: The gender column was made consistent by replacing all the data points representing male and female with ‘Male’ and ‘Female’ respectively. In the same vein, NSW, VIC and QLD were used for the states in the customerAddress table.

![image](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/12dbdb70-9205-4535-ab5c-91ed07b1f229)


## Currency
The deceased information column on the customerDemographic table was not needed.
Mitigation: The row with deceased client was filtered out.

![image](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/c282f3a8-23f1-4a26-baed-038c3ecd0dae)

## Relevance
The default column in the customerDemographic table holds no valuable information and thus is irrelevant for analysis. Also, cancelled orders was not required for analysis.
Mitigation: The default column was removed, and the cancelled orders were filtered out.

![image](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/2fd187f3-218d-46ce-8d80-f74daf83986d)


## Validity
The data types of some columns such as list_price and standard_cost in the Transactions table and DOB in the customerDemographic table are not appropriate.
Mitigation: The data types for these columns were changed to appropriate data types.


# Data Modelling
The cleaned data tables were set for modelling using Power Pivot. Three of the tables were used for the modelling. This is shown below.

![image](https://github.com/MosunmolaRaji/Customer-Segmentation-in-Excel/assets/138968251/dca27b6c-1994-4e8e-8b38-ead8c8a52d0d)

# Data Analysis
In addition to the age and profit columns, recency column was also created as the period between the actual transaction and the last transaction in the data set. A pivot table was generated and was used to obtain the frequency and monetary columns. the three columns - recency, frequency and mometary columns were then ranked based on quartiles to obtain the R, F, and M scores. These were then concatenated to obtain the RFM score that was used to rank the customers into platinum, gold, silver and bronze.

