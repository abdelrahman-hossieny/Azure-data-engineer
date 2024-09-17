
## Prerequisites
Before proceeding, ensure the following resources are set up in your Azure account:
- **Azure SQL Database** with the necessary tables and data.
- **Azure Blob Storage** account and container.
- **Azure Data Factory (ADF)** instance for orchestrating the data flow.
- Proper **network configurations** (like firewall rules) to allow communication between these services.

## Steps for Implementation

### 1. Setup Azure SQL Database
- Ensure that the Azure SQL Database contains the data you wish to transfer.
- Verify that the data meets the filtering and sorting requirements you plan to implement.

### 2. Create a Blob Storage Account
- Go to the **Azure Portal** and create a **Blob Storage** account.
- Within the Blob Storage account, create a **container** where the final data will be stored.

### 3. Create Azure Data Factory Pipeline
- Navigate to your **Azure Data Factory** and create a new pipeline.
  
#### a. **Source** (Azure SQL Database):
   - Add a **source dataset** that connects to the **Azure SQL Database**.
   - Set up the source query or table selection to identify the dataset you want to move.

#### b. **Data Flow**:
   - Inside the pipeline, create a **Data Flow**.
   - Add a **Filter** transformation to apply the required filter condition to the data.
   - Add a **Sort** transformation to sort the data as required (by date, ID, or any other column).
  
#### c. **Sink** (Azure Blob Storage):
   - Create a **sink dataset** that connects to the **Azure Blob Storage** account and points to the container where the data should be saved.
   - Specify the format in which the data will be saved (e.g., CSV, Parquet).

#### d. **Trigger**:
   - Set up a trigger to run the pipeline at specific intervals or manually trigger the pipeline.

### 4. Monitor the Pipeline
- Once the pipeline is running, you can monitor its progress using **ADF's Monitoring tab**.
- Check for any errors or failed executions and verify that the data in Blob Storage is properly filtered and sorted.

## Conclusion
This project demonstrates how to move data from **Azure SQL** to **Azure Blob Storage** using **Azure Data Factory** with both filtering and sorting applied. This approach helps in efficiently transferring only the relevant data in the desired format and order.
