# Azure Data Engineering Project

This project focuses on building a robust data engineering pipeline using Azure services. The pipeline involves extracting data from various sources, transforming it using Azure Data Factory, Apache Spark in Azure Databricks, and storing it in Azure Data Lake Gen 2 and Azure Synapse Analytics. The final step includes creating visualizations with Power BI.

# Data Source

This section covers the initial steps of the data pipeline, involving ETL processes. The data is extracted from multiple sources, and various transformation logic, such as handling null values, is applied before loading the data to the target location.

# Data Factory

Azure Data Factory is used to build a robust data pipeline that connects to multiple sources, orchestrates ETL processes, and efficiently loads data to the target destinations. For more information, refer to [Azure Data Factory](https://azure.microsoft.com/en-us/products/data-factory).

# Data Lake Gen 2

Azure Data Lake Gen 2 serves as the object storage solution in this project, providing a scalable and secure environment for storing files. It utilizes storage accounts to create containers and store blob files, as well as tables for structured data.

For more information, refer to [Azure Data Lake Gen 2](https://azure.microsoft.com/en-us/solutions/data-lake/).

# Azure Databricks

Azure Databricks, powered by Apache Spark, is employed for basic data transformations. It leverages the distributed computing capabilities of Spark to process and transform data efficiently.

For more information, refer to [Azure Databricks](https://azure.microsoft.com/en-us/solutions/data-lake/).

# Azure Synapse Analytics

Azure Synapse Analytics is utilized for running SQL queries on the transformed data. It provides a powerful analytical environment for gaining insights from the processed data.

For more information, refer to [Azure Synapse Analytics](https://azure.microsoft.com/en-us/products/synapse-analytics/).

# Dashboard

The final step in the pipeline involves creating visualizations using Power BI. The Power BI dashboard showcases key insights and data visualizations for better understanding and decision-making.

# Dataset

The project uses the [2021 Olympics in Tokyo dataset](https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo/data) for testing and demonstration purposes. This dataset includes [add key features] and is subject to [any data preprocessing steps].

# Azure Account Structure

The project's Azure account structure is visualized below. This structure encompasses [brief description of the key components or purpose].

![Azure Account Structure](/img/Az-Account-Structure.PNG)

# Azure

data-rg
    containers
        data container
            2 dirs
                raw & transformed data

# Copy data from source to lake

Data Factory
    data-rg
        pipeline
            copy data
            source (github repo)
            sink




