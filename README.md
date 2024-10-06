
# SSIS Data Integration Project: Prospect Data Processing

This project demonstrates a complete ETL (Extract, Transform, Load) process using SQL Server Integration Services (SSIS) to process prospect data from an Excel source. The data is validated, transformed, and updated in a staging table with proper error handling.

## Problem Statement
The objective is to efficiently process prospect data from external Excel sources, validate it, handle errors, and update records. This project ensures data quality by separating good data from bad data and applying the necessary transformations and checks.

## Key Components
- **Excel Source**: Initial loading of 1,410 rows from an Excel source file.
- **Conditional Split**: Separates good data (1,353 rows) from bad data (57 rows) for further processing.
- **Derived Column Transformation**: Splits name, title, and location columns to prepare the data for conversion.
- **Data Conversion**: Ensures that all data is in the correct format for loading into the destination.
- **Lookup Transformation**: Checks for existing records and updates matching records while inserting new records.
- **Error Handling**: Captures bad data and redirects it for further investigation using the Union All component.

## Data Flow Overview
![Data Flow Overview](split.png)

## Outcome
- **Successful Data Processing**: 1,353 rows of good data were transformed and either inserted as new records or updated in the staging table.
- **Error Management**: 57 rows of bad data were isolated and logged for review, allowing for targeted data quality improvements.

## How to Run the Project
1. Open the `.dtsx` SSIS package in SQL Server Data Tools (SSDT).
2. Adjust the Excel connection manager to point to your local data source.
3. Execute the SSIS package and monitor the output for data processing and error logging.

