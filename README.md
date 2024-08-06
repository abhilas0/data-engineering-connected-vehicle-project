## **IOT Data Pipeline for Vehicle Telematics Data Engineering Project**

### Project Description

A leading vehicle company has implemented IoT devices in their cars to collect telematics data, including speed, location, fuel consumption, and engine health. This data goes into the Amazon S3.This project aims to build a data pipeline that transfers this data from Amazon S3 to Azure Data Lake Storage (ADLS) and ultimately to Azure SQL Database for advanced analytics and reporting.

### Objectives

* Establish a secure and efficient data pipeline from Amazon S3 to ADLS.
* Transform and load data from ADLS to Azure SQL Database.
* Ensure data integrity, scalability, and real-time processing capabilities.

### Architecture 

**1. Data Ingestion:**
   
  * **Source**: Amazon S3 bucket.
  * **Frequency**: Real-time or batch uploads of telematics data.

**2. Data Transfer to ADLS:**

  * **Tool**: Azure Data Factory (ADF)
  * **Process**: ADF pipelines will be configured to periodically extract data from Amazon S3 and load it into ADLS.
  * **Security**: Use AWS IAM roles and Azure Managed Identity for secure data transfer.

**3. Data Loading to Azure SQL Database:**

* **Tool**: ADF
  * **Process:**
    * Load processed data from ADLS into Azure SQL Database.
    * Implement incremental data loading to handle continuous data streams.

![Smart Vehicle Project](https://github.com/user-attachments/assets/17343768-2fc7-43f3-86c4-af60ae146c43)

### Expected Outcomes:

Real-time insights into vehicle performance and driver behavior.
Improved decision-making based on data-driven analytics.
Enhanced operational efficiency and reduced maintenance costs.

### Technologies Used:

* **AWS:** S3, IAM
* **Azure:** Data Lake Storage, Data Factory,SQL Database
* **Languages:** Python, SQL
* **Security:** Managed Identities, IAM Roles, SQL Authentication


### Conclusion:
This project will enable the vehicle company to leverage IoT data effectively. The seamless data pipeline from Amazon S3 to Azure SQL Database ensures data integrity, scalability, and real-time processing capabilities.


