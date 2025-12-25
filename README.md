Tender Trends ETL Pipeline

## 📝 Project Overview

This project automates the extraction, transformation, and analysis of European Union tender data (TED – Tenders Electronic Daily). It collects daily tender XML files, parses them into structured CSVs, cleans the data, stores it in a MySQL database, and generates business insights through a Power BI dashboard.

**Key Highlights:**

* End-to-end ETL pipeline (XML → CSV → MySQL)
* Data cleaning and CPV code normalization
* Automation using Python scripts and batch file
* Power BI dashboard for visualizing tender trends

---

## 📂 Project Structure

```
tender_project/
│
├── Scripts/
│   ├── download_ted_file.py      # Download daily tender XML files
│   ├── parse_xml_to_csv.py       # Parse XML → CSV
│   ├── clean_csv.py              # Clean and normalize CSV data
│   ├── csv_to_mysql.py           # Load cleaned CSV into MySQL
│   ├── demo.py                   # Sample data checks and exploration
│   ├── main.py                   # Orchestrates full ETL pipeline
│   └── csv/
│       ├── tenders.csv           # Raw tender data (CSV)
│       └── tenders_clean.csv     # Cleaned tender data (CSV)
│
├── run_pipeline.bat               # Batch file to automate pipeline
├── tender_trends.pbix             # Power BI dashboard
├── README.md                      # Project documentation
└── .gitignore                     # Ignored files (e.g., .idea/)
```

---

## ⚙️ Technologies Used

* **Python**: Data scraping, parsing, cleaning, and ETL
* **Pandas**: Data manipulation and cleaning
* **Requests**: Download XML files
* **MySQL**: Data storage
* **Power BI**: Visualizing tender trends

---

## 🚀 How It Works

### 1. Download Tenders

`download_ted_file.py` downloads XML files daily from TED (European Tenders).

### 2. Parse XML to CSV

`parse_xml_to_csv.py` extracts tender details and saves them as a CSV file.

### 3. Clean CSV

`clean_csv.py` performs data cleaning, handles missing values, and normalizes CPV codes.

### 4. Load into MySQL

`csv_to_mysql.py` inserts cleaned data into a MySQL database for easy querying.

### 5. Data Analysis

`tender_trends.pbix` provides visual insights, such as:

* Top CPV codes
* Tender counts by country
* Trends over time

### 6. Automation

`run_pipeline.bat` runs the full pipeline with one click.

---

## 💡 How to Run

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/tender-trends-etl-pipeline.git
cd tender-trends-etl-pipeline
```

2. **Create a Python virtual environment**

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Configure MySQL**

* Update credentials in `csv_to_mysql.py` (use environment variables for security)

5. **Run the pipeline**

```bash
python main.py
```

Or run `run_pipeline.bat` on Windows.

6. **View Insights**

* Open `tender_trends.pbix` in Power BI Desktop.

---

## 🛠 Features to Improve

* Add exception handling for network errors
* Use environment variables for sensitive info (DB credentials)
* Add unit tests for CSV cleaning and parsing scripts
* Optimize large XML file handling

---

## 📈 Project Impact

* Automates tender data collection and analysis
* Provides actionable insights for procurement and market research
* Demonstrates Python ETL skills, database management, and business intelligence

---

## 📄 License

This project is open-source for learning and demonstration purposes.
