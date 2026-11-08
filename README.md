# azure-sales-data-pipeline
•	Project Overview: End-to-End Data Pipeline using Azure SQL, Storage, and Data Factory
•	This project demonstrates an end-to-end data engineering pipeline using cloud services from Microsoft Azure. The objective was to extract sales data from a database, store raw data, apply transformations, and save the processed data for analytics.
•	________________________________________
•	Azure SQL Database Creation
•	First, we created an Azure SQL Database to store structured sales data.
•	Table Created: sales_data
•	The table included the following columns:
•	product_id (INT)
•	product_name (VARCHAR)
•	category (VARCHAR)
•	price (INT)
•	quantity (INT)
•	sales_date (DATE)
•	Data Inserted:
•	(1,'Laptop','Electronics',50000,2,'2024-01-01'),
(2,'Mobile','Electronics',20000,5,'2024-01-02'),
(3,'Shoes','Fashion',3000,10,'2024-01-03'),
(4,'Watch','Fashion',5000,7,'2024-01-04'),
(5,'Tablet','Electronics',15000,3,'2024-01-05');
•	This served as the source data for the pipeline.
•	________________________________________
•	Azure Storage Account Setup
•	Next, we created an Azure Storage Account to store raw and processed data.
•	Inside it, we created:
•	Directory for data storage
•	Two containers:
o	input → to store raw data
o	output → to store processed data
•	Data was stored in Azure Blob Storage format.
•	________________________________________
•	Data Factory Pipeline – Raw Data Ingestion
•	We created an Azure Data Factory to automate data movement.
•	Pipeline 1: Copy Raw Data
•	Process:
•	Source → Azure SQL Database (sales_data table)
•	Destination → Blob Storage (input container)
•	Result:
•	Raw data successfully copied
•	Stored as input/raw data
•	This data was not modified
•	________________________________________
•	Data Factory Pipeline – Data Transformation
•	We created another pipeline with a Data Flow to transform the data.
•	Transformations Applied:
•	Filter Condition:
•	price > 10000
•	Sorting Applied:
•	Sort by sales_date DESC
•	________________________________________
•	Store Processed Data
•	The transformed data was stored in:
•	Storage Account
•	output container
•	As processed data
•	This data is now ready for:
•	Reporting
•	Analytics
•	Dashboard creation
•	________________________________________
•	Architecture Flow Summary
•	Azure SQL Database
        │
        │
        ▼
Data Factory Pipeline 1
(Copy Activity)
        │
        ▼
Blob Storage (Input Container)
(Raw Data)
        │
        │
        ▼
Data Factory Pipeline 2
(Data Flow – Filter & Sort)
        │
        ▼
Blob Storage (Output Container)
(Processed Data)
________________________________________
7. Project Outcome
This project successfully demonstrated:
•	Cloud database creation
•	Data ingestion
•	Data transformation
•	Data storage
•	Pipeline automation
________________________________________
8. Key Skills Learned
•	Azure SQL Database
•	Azure Storage Account
•	Azure Blob Storage
•	Azure Data Factory
•	ETL Pipeline Development
•	Data Transformation
•	Cloud Data Engineering

