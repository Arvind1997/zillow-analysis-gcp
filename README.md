# zillow-analysis-gcp
This repository serves as the information for Zillow Property Sales analysis that starts from cleaning the dataset and storing it in Google Cloud Storage and the ETL process is performed using Mage and the Google Compute Engine while the analysis is done using Big Query and finally, the Visualzation is done using Looker Studio.

## Overview:

This project focuses on Zillow Sales Analysis using data obtained from the ATTOM API provided by Zillow. The data is cleaned using Python, resulting in a CSV file with 57 columns. The project involves loading this CSV file into Google Cloud Storage, setting up a Google Compute instance, and deploying a pipeline using Mage for further analysis in BigQuery and visualization in Looker.

## Data Columns
The dataset contains 57 columns, including property information, location details, and sales-related data. Notable columns include Id, fips, address, latitude, longitude, yearBuilt, rooms, baths, beds, saleTransDate, saleamt, and various others.

## Prerequisites
Obtain Zillow data from ATTOM API.
Clean the data using Python and generate a CSV file.
Create a Google Cloud account.
Load the CSV file into Google Cloud Storage.
Create a Google Compute instance and install necessary extensions (pip3, python3, etc.).
Deploy a pipeline using Mage.

## Pipeline Steps

1. Start Mage:
mage start <pipeline name>

3. Data Loading:
Create a data loader to connect with the data in Google Storage.

4. Transformation:
Use the transform stage to create necessary dimension and fact tables. Send the transformed data to the exporter as a dictionary.

5. Data Export:
The data exporter exports the transformed data to BigQuery.

6. BigQuery Validation:
Perform table validations in BigQuery.

7. Analytics Table:
Create the analytics table named 'zillow-analytics' for further analysis.

8. Looker Visualization:
Utilize Looker for visualization and analysis.

## Looker Visualization
Looker is used for visualizing the data and creating insightful analytics. The zillow-analytics table is a key component for further analysis and reporting in Looker. Visualizations are attached for a comprehensive understanding of the Zillow Sales Analysis.

## Additional Notes
Ensure proper Google Cloud account setup.
Verify pipeline deployment using Mage.
Validate data in BigQuery before creating analytics tables.
Explore and customize Looker for in-depth visualization and analysis.


