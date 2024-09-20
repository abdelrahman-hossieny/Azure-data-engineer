# Google Play Store Data Cleaning and Transformation with PySpark

## Overview

This project focuses on cleaning and transforming a dataset from the Google Play Store using **PySpark**. The dataset is in CSV format and contains information about various applications, including reviews, installs, and prices. The goal of the project is to prepare the data for further analysis by cleaning and converting string-based columns into numeric formats.

### Key Features:
- Read a CSV file containing Google Play Store data.
- Clean and transform columns with string data by removing unwanted characters.
- Convert string data to numeric types for accurate analysis.
- Create a temporary SQL view for running SQL queries directly on the DataFrame.

## Technologies Used

- **Apache Spark**: For distributed data processing.
- **PySpark**: Python API for Apache Spark.
- **Python**: Programming language used to interact with PySpark.
- **CSV**: Data format for input.
- **SQL**: Used to query the temporary view of the DataFrame.

## Project Steps

### 1. Reading the CSV File
The project begins by loading a CSV file containing Google Play Store data into a PySpark DataFrame.

### 2. Data Cleaning and Transformation
The key columns are cleaned and transformed as follows:
- **Reviews** column: Cast as an integer.
- **Installs** column: Remove non-numeric characters (e.g., commas and `+`) and cast as an integer.
- **Price** column: Remove the dollar sign (`$`) and cast as an integer.

### 3. Temporary View Creation
A temporary SQL view of the cleaned DataFrame is created, which allows SQL queries to be executed directly on the DataFrame for further analysis.

