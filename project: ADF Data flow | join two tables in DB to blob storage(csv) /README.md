# SQL to Blob Storage Data Join using Azure Data Factory

## Project Overview
This project involves joining data from **two tables** in an **Azure SQL Database** and transferring the result to **Azure Blob Storage** in **CSV** format using **Azure Data Factory**.

The main tools used in this project:
- **Azure SQL Database**: Source database containing the tables to be joined.
- **Azure Data Factory (ADF)**: Handles the data flow, performs the join, and transfers the data.
- **Azure Blob Storage**: Destination for the joined data in CSV format.

## Architecture Overview
1. **Source**: Two tables from an Azure SQL Database.
2. **Data Flow**: Joining the tables in Azure Data Factory's Data Flow.
3. **Sink**: Writing the joined data to Azure Blob Storage in CSV format.

### Data Flow Pipeline Plan:

##Source (Azure SQL - two tables) --> Join (Data Flow) --> Sink (Blob Storage - CSV)

## Prerequisites
Before starting, ensure the following resources are set up in Azure:
- **Azure SQL Database** with the two source tables.
- **Azure Blob Storage** account and container.
- **Azure Data Factory** instance for orchestrating the data flow.
- Proper **network configurations** (firewall rules) to allow communication between these services.

## Steps for Implementation

### 1. Setup Azure SQL Database
- Ensure that the Azure SQL Database contains the two tables you want to join.
- Verify the tables have matching fields or keys to perform the join.

### 2. Create a Blob Storage Account
- Go to the **Azure Portal** and create a **Blob Storage** account.
- Create a **container** within the Blob Storage account where the output will be stored.

### 3. Create Azure Data Factory Pipeline
- Navigate to your **Azure Data Factory** and create a new pipeline.
  
#### a. **Source** (Azure SQL Database):
   - Create two **source datasets** connecting to the two SQL tables in your database.
   - Configure the datasets to retrieve the relevant data.

#### b. **Data Flow**:
   - Inside the pipeline, create a **Data Flow**.
   - Add a **Join** transformation to combine the two tables based on a common key or condition.
  
#### c. **Sink** (Azure Blob Storage):
   - Create a **sink dataset** connected to the **Azure Blob Storage** account, specifying the CSV format.
   - Ensure that the output is directed to the appropriate container and is in CSV format.

#### d. **Trigger**:
   - Set up a trigger to run the pipeline on-demand or at scheduled intervals.

### 4. Monitor the Pipeline
- Once the pipeline is running, monitor its progress in the **ADF Monitoring tab**.
- Verify that the data is successfully joined and transferred to Blob Storage in CSV format.

## Conclusion
This project demonstrates how to join data from two tables in **Azure SQL Database** and transfer the joined data to **Azure Blob Storage** in **CSV** format using **Azure Data Factory**.
