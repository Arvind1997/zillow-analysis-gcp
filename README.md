# Zillow Sales Analysis
This repository serves as the information for Zillow Property Sales analysis that starts from cleaning the dataset and storing it in Google Cloud Storage and the ETL process is performed using Mage and the Google Compute Engine while the analysis is done using Big Query and finally, the Visualzation is done using Looker Studio.

![zillow-logo](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/0d5539ab-1291-4a2c-b72d-85d4744dc252)


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

![zillow-storage-bucket-screenshot](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/d29737e6-18ab-4f8d-b465-5e9a3bb005bd)


![zillow-compute-instance-screenshot](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/c7dabe9e-dec9-4bcb-893a-21d7ac596ec4)


## Pipeline Steps

1. Start Mage:
mage start <pipeline name>

![ssh-magestart-screenshot](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/7b2716a3-68f2-4569-9f05-40e1dd5c60f6)

![mage-ETL-screenshot](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/01d3ea37-6bd4-45b7-99a9-62539dd0f82b)

3. Data Loading:
Create a data loader to connect with the data in Google Storage.

4. Transformation:
Use the transform stage to create necessary dimension and fact tables. Send the transformed data to the exporter as a dictionary.

6. Data Export:
The data exporter exports the transformed data to BigQuery.

![zillow-mage-pipeline-screenshot](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/545a244f-6c55-447e-a7a7-0dc740b1f7c3)

![mage-bigquery-connect-screenshot](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/39875a71-a4ad-44e0-b672-c92de5360ec7)

7. BigQuery Validation:
Perform table validations in BigQuery.

![zillow-bigquery-tables-screenshot](https://github.com/Arvind1997/zillow-analysis-gcp/assets/13155343/2ad343f3-0c11-4a85-a4ad-7c942d55d5aa)


8. Analytics Table:
Create the analytics table named 'zillow-analytics' for further analysis.

9. Looker Visualization:
Utilize Looker for visualization and analysis.

## Looker Visualization
Looker is used for visualizing the data and creating insightful analytics. The zillow-analytics table is a key component for further analysis and reporting in Looker. Visualizations are attached for a comprehensive understanding of the Zillow Sales Analysis.

## Additional Notes
Ensure proper Google Cloud account setup.
Verify pipeline deployment using Mage.
Validate data in BigQuery before creating analytics tables.
Explore and customize Looker for in-depth visualization and analysis.


