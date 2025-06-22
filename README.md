# 📦 Amazon Prime Dataset ETL & Dashboard Project - AZURE

This project demonstrates an **end-to-end data pipeline** for analyzing Amazon Prime video data using **Azure cloud services**. It showcases the ingestion, transformation, and visualization of streaming content data through a modern cloud data stack.

---

## 🚀 Tech Stack

- **🔄 Azure Data Factory** – For building and orchestrating ETL pipelines
- **🧠 Azure Databricks (PySpark)** – For data transformation and cleansing
- **📊 Power BI** – For interactive data visualization and reporting
- **💾 Azure Blob Storage** – For raw and processed data storage
- **🧱 Azure SQL Database** – For storing transformed data

---

## 📁 Project Structure
amazonPrimeDataset/
│
├── data/ # Sample raw dataset (CSV format)
│ └── amazon_prime_titles.csv
│
├── notebooks/ # Databricks transformation notebooks
│ └── clean_amazon_data.py
│
├── pipeline/ # ADF pipeline screenshots or JSON exports
│ └── amazon_adf_pipeline.json
│
├── dashboard/ # Power BI .pbix file or screenshots
│ ├── amazon_prime_dashboard.pbix
│ └── dashboard_preview.png
│
├── README.md # Project documentation (this file)

---

## 📚 Dataset Source

- **Source**: [Kaggle – Amazon Prime Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/amazon-prime-movies-and-tv-shows)
- Contains information on:
  - Titles, release year, genre
  - Cast, director, country
  - Date added to platform, duration, rating

---

## 🛠️ Workflow Overview

1. **Data Ingestion**  
   Raw `.csv` file uploaded to Azure Blob Storage

2. **ETL in Azure Data Factory**  
   - Pipeline pulls raw data from blob
   - Loads into staging in Azure SQL or Databricks

3. **Data Cleansing in Databricks (PySpark)**  
   - Handles nulls, formats dates, filters duplicates
   - Saves clean data to curated layer

4. **Data Load to Azure SQL DB**  
   - Structured data for querying and reporting

5. **Visualization in Power BI**  
   - Interactive dashboard showing:
     - Content trends over time
     - Genre distribution
     - Country-wise content analysis
     - Ratings breakdown

---

## 📊 Dashboard Preview

![Amazon Prime Power BI Dashboard](dashboard/dashboard_preview.png)

---

## 🔍 Key Insights

- Most Amazon Prime content was added between 2017–2020
- Dominant content type: Movies (~80%)
- Top countries: United States, India, United Kingdom
- Genre trends show Comedy and Drama lead globally
- Most content rated TV-14 and TV-MA

---

## 📥 How to Run This Project

1. Clone this repository  
   ```bash
   git clone https://github.com/matrukan/amazonPrimeDataset.git
2. Upload the amazon_prime_titles.csv file to Azure Blob Storage

3. Import the amazon_adf_pipeline.json in Azure Data Factory

4. Open Databricks and run notebooks/clean_amazon_data.py to transform data

5. Load transformed data to Azure SQL or export for Power BI

6. Open dashboard/amazon_prime_dashboard.pbix in Power BI Desktop

