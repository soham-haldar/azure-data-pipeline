# End-to-End Data Pipeline Using Microsoft Azure and SQL

Complete data pipeline from data ingestion to dashboard display, utilising Azure services and SQL.

Data used is a sample database from Microsoft that can be [found here](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms)

The data has been loaded into an on-premise SQL database, ingested into the cloud, transformed and updated, and then finally used to generate an interactive dashboard using Power BI.

As the majority of the process has been implemented in Azure, this repository contains specific files from parts of the project that allowed exports.

## Process and Tech Stack:

1. Data Ingestion :
     - On-premise SQL Database, handled with SQL Server Management Studio
     - Data loaded into Azure Data Lake Storage with Azure Data Factory
     - Azure Key Vault used to store SQL logins and API keys.
2. Data Manipulation : 
     - Azure DataBricks used to normalise column names and format dates.
     - Data formatted into Bronze, Silver and Gold buckets to separate raw data and stages of transformation.
3. Data Reporting :
     - Azure Synapse Analytics used to load transformed data
     - PowerBI Dashboard used to visualise data and add filters and statistics

Pipeline scheduled to run daily at a set time.
