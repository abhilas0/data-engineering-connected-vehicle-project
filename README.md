## **IOT Data Pipeline for Vehicle Data Processing - Data Engineering Project**

### Project Description

A leading vehicle company has equipped its fleet with IoT devices to gather real-time data on vehicle performance, location, temperature and speed. 
This data is crucial for predictive maintenance, performance optimization, and enhancing customer experience. 
The IoT devices send JSON-formatted data to an Amazon S3 bucket, which needs to be processed and stored in a structured format for further analysis.

### Objectives

The goal of this project is to create an end-to-end data pipeline that efficiently transfers, processes, and stores the IoT data from the S3 bucket to Azure Data Lake Storage (ADLS) and finally into an Azure SQL Database. 
The project also involves implementing an Azure Function App to validate the JSON files, routing them to appropriate containers (staging/rejected) based on their validity.

### Architecture 

**1. Data Ingestion from S3 to ADLS:**
   
   * The IoT data is initially stored in an Amazon S3 bucket in JSON format.
   * A scheduled or event-driven process (e.g., ADLS Trigger ) triggers the transfer of these JSON files from the S3 bucket to Azure Data Lake Storage (ADLS) Gen2.
     

**2. Data Validation using Azure Function App:**

   * Once the JSON files land in the staging container of ADLS, an Azure Function App is triggered.
   * The Azure Function App validates the structure and content of each JSON file:
     
        * **Valid JSON files:** Moved to the Staging container in ADLS for further processing.
        * **Invalid JSON files::** Moved to the Staging container in ADLS.
          
    
   **3. Loading Data from ADLS to Azure SQL Database:**

   * After validation, the data in the Staging container is transformed using Azure Data Factory (ADF) to align with the schema of the Azure SQL Database.
   * The transformed data is then loaded into the Azure SQL Database, where it can be queried and analyzed using various Azure tools like Power BI, SQL Server Reporting Services (SSRS), or third-party applications.


![Smart Vehicle Project (1)](https://github.com/user-attachments/assets/b1ab03de-774d-4620-bf64-41a6ab562caa)



### Key Technologies
   * **Amazon S3:** Storage of raw IoT data.
   * **Azure Data Lake Storage (ADLS):** Storage and processing of raw and processed data.
   * **Azure Function App:** Validation and routing of JSON files based on their structure.
   * **Azure SQL Database:** Structured storage of the processed data.


### Outcome

This pipeline ensures a robust, scalable, and automated process for ingesting, validating, and storing IoT data. 
It provides the vehicle company with a reliable data infrastructure that can support advanced analytics and decision-making processes, ultimately leading to improved vehicle performance and customer satisfaction.


