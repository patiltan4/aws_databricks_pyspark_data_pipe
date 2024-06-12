# PySpark Olympic Insights on Databricks

## Overview

**PySpark Olympic Insights on Databricks** is a comprehensive project that leverages PySpark, Databricks, and AWS to analyze and gain insights from Olympic data. This project involves various data frames related to coaches, athletes, entries by gender, medals, and teams. It showcases advanced data processing and analytics capabilities using PySpark on the Databricks platform and Data from Amazon S3.

## Project Structure

- **Coaches Data**: Information about Olympic coaches.
- **Athletes Data**: Information about Olympic athletes.
- **Entries by Gender Data**: Participation numbers categorized by gender and discipline.
- **Medals Data**: Medal counts for each country.
- **Teams Data**: Information about Olympic teams and their events.

## Technologies Used

- **PySpark**: For large-scale data processing and analysis.
- **Databricks**: As the collaborative data platform.
- **AWS**: For hosting the data.

## Getting Started

### Prerequisites

- An AWS account
- Access to Databricks
- Basic knowledge of PySpark and data analysis

### Setup Instructions

1. **Clone the Repository**
    ```sh
    git clone https://github.com/yourusername/pyspark-olympic-insights.git
    cd pyspark-olympic-insights
    ```

2. **Upload Data Files to AWS S3**
    - Upload your data files (`coaches_file`, `athletes_file`, `entriesgender_file`, `medals_file`, `teams_file`) to an S3 bucket.

3. **Create a Databricks Cluster**
    - Log in to your Databricks account and create a new cluster.
    - Ensure the cluster has access to the necessary libraries for PySpark.

4. **Import the Notebooks**
    - Import the provided Jupyter notebooks from the repository into your Databricks workspace.

5. **Configure S3 Access**
    - Set up your Databricks cluster to have access to your S3 bucket. This may involve configuring IAM roles or keys.

6. **Run the Analysis**
    - Open the notebooks in Databricks and follow the instructions to load the data from S3 and run the analysis.

## Data Schema

### Coaches DataFrame Schema
```plaintext

 |-- Name: string (nullable = true)
 |-- Country: string (nullable = true)
 |-- Discipline: string (nullable = true)
 |-- Event: string (nullable = true)
```
### Athletes DataFrame Schema
```plaintext

 |-- PersonName: string (nullable = true)
 |-- Country: string (nullable = true)
 |-- Discipline: string (nullable = true)
```
### EntriesByGender DataFrame Schema
```plaintext
 |-- Discipline: string (nullable = true)
 |-- Female: integer (nullable = true)
 |-- Male: integer (nullable = true)
 |-- Total: integer (nullable = true)
```
### Teams DataFrame Schema
```plaintext
 |-- TeamName: string (nullable = true)
 |-- Discipline: string (nullable = true)
 |-- Country: string (nullable = true)
 |-- Event: string (nullable = true)
```
### Medals DataFrame Schema
```plaintext
 |-- Rank: integer (nullable = true)
 |-- Team_Country: string (nullable = true)
 |-- Gold: integer (nullable = true)
 |-- Silver: integer (nullable = true)
 |-- Bronze: integer (nullable = true)
 |-- Total: integer (nullable = true)
 |-- Rank by Total: integer (nullable = true)
```
