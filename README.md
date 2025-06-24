# DSA2040A ETL Midterm – Mark

## Name: Mark
**Student ID (Last 3 Digits):** 677  
**Course:** Data Warehousing and Mining  
**Instructor:** Austin Odera  
**Semester:** US 2025

---

## 1. Project Overview
**Project Title:** ETL Lab – Customer Sales Data Pipeline

### Project Description:
This project is an ETL lab designed to simulate a real-world data pipeline scenario. It involves extracting customer sales data from CSV files, transforming it through various data cleaning and enrichment processes, and loading the final dataset into a database system. The project emphasizes best practices in ETL processes, including file management, documentation, and version control.

The lab is structured into three main phases: Extract, Transform, and Load, each represented by a Jupyter Notebook. The project also includes visual elements to enhance understanding of the data transformations and distributions.

### Project Goals:
- To practice ETL processes using Python and Jupyter Notebooks
- To handle customer sales data effectively
- To demonstrate data cleaning, transformation, and loading into a database
- To apply best practices in data management and documentation

### Project Context:
This project is part of the Data Warehousing and Mining course, focusing on practical applications of ETL techniques. It simulates a scenario where customer sales data needs to be processed for analysis, highlighting the importance of data quality and structure in data engineering tasks.

### Project Scope:
- Extract data from provided CSV files
- Transform the data through cleaning and enrichment
- Load the transformed data into a SQL Server database or alternative format
- Document the process and results in Jupyter Notebooks

### Project Structure:
```
etl-lab/      
├── data/                  # Folder for raw data files
├── transformed/           # Folder for transformed data files
├── etl_extract.ipynb      # Notebook for data extraction
├── etl_transform.ipynb    # Notebook for data transformation
├── etl_load.ipynb         # Notebook for data loading  
├── README.md              # Project documentation
└── requirements.txt       # Python dependencies
```

### Data Files:
- **raw_data.csv**: Contains initial customer sales data
- **incremental_data.csv**: Contains new sales data to be added

Located in the `data/` folder. The data includes columns such as order_id, customer_id, order_date, quantity, and unit_price. The structure allows transformations like calculating total prices and handling missing values.

---

## 2. ETL Phases
The project is divided into three main Jupyter Notebooks:

### a. Extract – `etl_extract.ipynb`
- Loads raw and incremental data
- Displays `.head()` and `.info()`
- Identifies missing values, duplicates, unusual types
- Saves data to `data/` for transformation

### b. Transform – `etl_transform.ipynb`
Applies transformations:
- Remove duplicates
- Drop rows with missing key values
- Add `total_price = quantity * unit_price`
- Convert `order_date` to datetime
- (Optional) Categorize spending levels

Saves as:
- `transformed_full.csv`
- `transformed_incremental.csv`

### c. Load – `etl_load.ipynb`
- Loads transformed files into SQLite or SQL Server using `pyodbc`
- Verifies insertions using preview queries
- Alternative format: `.parquet`

---

## 3. Tools Used
- Python, Jupyter Notebook, Pandas
- SQLite / SQL Server
- Git & GitHub
- pyodbc (optional)
- Matplotlib / Seaborn (optional)

---

## 4. How to Run the Project
1. Clone repo
2. Install requirements
3. Open and run:
   - `etl_extract.ipynb`
   - `etl_transform.ipynb`
   - `etl_load.ipynb`
4. Check outputs in `transformed/` and `loaded/`

---

## 5. Visuals and Screenshots
- Transformed Data Preview
- Histogram of `total_price` distribution

---

## 6. Bonus Features
- Data Profiling: Histogram of `total_price`
- Validation: Missing values + duplicates handled
- Clear documentation and Git commits
- Error handling in Load phase

---

## 7. Conclusion
This lab demonstrates real-world ETL skills. It ensures that sales data is clean, enriched, and stored correctly, ready for analysis or reporting.
