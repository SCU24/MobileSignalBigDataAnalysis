# Mobile Signal Big Data Analysis and Prediction

This project utilizes big data from mobile networks to analyze and predict signal and speed metrics based on user activity and network type. Using Google BigQuery and PySpark, the analysis focuses on exploring and modeling network performance trends for 2015.

## Project Overview

The notebook achieves the following:

- Retrieves mobile signal data from Google BigQuery.
- Preprocesses data using PySpark to handle large datasets efficiently.
- Aggregates and visualizes average signal and speed metrics by network type and activity.
- Replaces missing values and prepares data for further analysis.
- Builds and evaluates predictive models for signal and speed.

## Prerequisites

### Libraries

The following libraries are required to run the notebook:

- **Google Cloud SDK**: For accessing BigQuery data.
  - Install: `pip install google-cloud-bigquery`
- **PySpark**: For big data processing and machine learning.
  - Install: `pip install pyspark`
- **Additional Libraries**: For data manipulation and visualization.
  - `pandas`, `matplotlib`, `seaborn`

### Google Cloud Setup

1. Create a Google Cloud project and enable the BigQuery API.
2. Download your service account key file (`.json`) and reference it in the notebook.

## Dataset Description

- **Source**: `bigquery-public-data.catalonian_mobile_coverage_eu.mobile_data_2015_2017`
- **Fields**:
  - `date`, `hour`: Temporal data for tracking trends.
  - `lat`, `long`: Geospatial coordinates.
  - `signal`: Signal strength.
  - `net`: Network type (e.g., 3G, 4G).
  - `speed`: Network speed.
  - `status`, `activity`: Contextual information about network usage.
- **Data Scope**:
  - Includes data from January 1, 2015, to December 31, 2015.
  - Filtered to remove rows with null `speed` values.

## Results and Insights

- **Aggregated Metrics**:
  - Average signal and speed computed for each combination of network type and activity.
  - Null values in key fields replaced to ensure data consistency.
- **Maximum Values**:
  - Peak `speed` and `signal` levels identified for 2015.
- **Predictive Modeling**:

  - **Linear Regression**:
    - Evaluated based on R2 and RMSE
  - **Random Forest**:
    - Evaluated based on R2 and RMSE

- **Visualizations**:
  - Average signal for different network types
  - Average speed for different network types

## How to Run

1. Install all dependencies listed in the prerequisites section.
2. Authenticate your Google Cloud account using the service account key.
3. Execute the notebook cells sequentially to perform data retrieval, processing, and analysis.

## Future Work

- Expand analysis to additional years or broader datasets.
- Improve model accuracy with feature engineering.
- Integrate results into a dashboard for real-time monitoring.

## Contact

For questions or collaboration, please contact the project maintainer.
