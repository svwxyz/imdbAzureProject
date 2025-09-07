# 🎬 IMDb Data Engineering Project – Azure Pipeline + Databricks

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![Databricks](https://img.shields.io/badge/Azure-Databricks-orange)](https://azure.microsoft.com/en-us/services/databricks/)
[![ADF](https://img.shields.io/badge/Azure-DataFactory-blue)](https://azure.microsoft.com/en-us/services/data-factory/)

---

## 📖 Overview  
This project demonstrates how to build a **data engineering pipeline** using **Azure Data Factory**, **Azure Data Lake**, and **Azure Databricks** on IMDb data.

---

## 🛠 Architecture  

1. **Data Ingestion**:  
   - Created an **Azure Data Factory pipeline** to fetch IMDb dataset from **GitHub**.  
   - Copied the raw data into **Azure Data Lake Storage**.  

2. **Data Processing (Transformations)**:  
   - Used **Azure Databricks (PySpark)** notebook to perform all transformations on the raw IMDb data.  
   - Created new derived columns, cleaned text, exploded arrays, calculated ROI & star power, handled missing values, and used window functions to rank movies/directors.  

3. **Data Output**:  
   - Wrote the transformed data back into **Azure Data Lake** in **Delta / Parquet** format with a new file name for downstream analytics.  

---

## 📂 Repository Structure  

---

## 🔥 Key Transformations in Databricks  

- Extract IMDb ID from `movie_imdb_link` 
- Clean & standardize `movie_title`  
- Split & explode `genres` and `plot_keywords`  
- Combine actors into a single `Fullcast` array  
- Compute ROI, total actor Facebook likes, star power  
- Create a `decade` column and group metrics  
- Rank movies per genre & top ROI per director using **Window Functions**  

---

## 🚀 How to Use  
1. Clone or download this repository:
   ```bash
   git clone https://github.com/svwxyz/imdbAzureProject.git
Upload thesilver.ipynb to your Databricks workspace.

Attach your Azure Data Lake credentials.

Run the notebook to ingest, transform and save the IMDb dataset.

👤 Author

Sumit Vishwakarma
📅 Completed: September 2025

---

⭐️ If you found this project useful, give it a star on GitHub!


