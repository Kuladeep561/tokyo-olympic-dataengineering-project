# Tokyo Olympics 2021 Data Engineering Project

## Overview

This report details the data engineering project focused on Tokyo Olympics 2021 data. The project involved designing and implementing a data warehouse architecture utilizing Azure Data Factory, Azure Databricks, Azure Synapse Analytics, and Power BI.



### Data Source

The dataset used for analysis was obtained from [Kaggle](https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo). The raw CSV files were hosted on GitHub and served as the data source, accessible in the [data](./data) directory of this repository.

## Data Ingestion

The initial step involved ingesting raw data from GitHub into our landing zone, which is Azure Data Lake Gen 2 storage. This process was facilitated by Azure Data Factory, a cloud-based data integration service. For detailed pipeline information, refer to [datafactory](./pipeline).

## Data Transformation

Upon successful ingestion, the data underwent transformation using Azure Databricks, a cloud-based data processing platform. This step included data cleaning, duplicate removal, schema standardization, and the creation of a Hive database. The transformed data, stored in Parquet format in Azure Data Lake Gen 2, can be explored in the [databricks.ipynb](./databricks/Tokyo%20Olympic%20Transformation.ipynb) notebook.

## Data Analytics

The transformed data was integrated into Azure Synapse Analytics, a cloud-based data warehouse service, through Azure Data Lake Gen 2's linked services. This integration enabled the execution of complex analytics on the data. As an illustration, a sample analysis was conducted to rank countries based on the number of athletes participating in the Olympic games. View the analysis results in ![analytics.jpg](./kkd-tokyo-olympic-sa%20-%20Azure%20Synapse%20Analytics.png)

## Data Visualization

For effective visualization, Power BI, a business intelligence platform, was employed to create dashboards and reports. Power BI was connected to Azure Databricks as a data source, utilizing tables prepared during the transformation phase. Several dashboards were created to communicate key insights from the data. Refer to [dashboards.pdf](./tokyo-olympics-dashboards.pdf) for a visual representation of the prepared dashboards. Here is an example dashboard ![dashboard-medals.jpg](/dashboard-medals.jpg)

---
