📦 Yelp Review Data Engineering Project (ETL Pipeline)

This mini project demonstrates a complete **ETL (Extract, Transform, Load)** process using the publicly available Yelp Dataset. The goal is to build a structured pipeline to extract data from raw files, transform it into a clean and meaningful format, and load it into a SQLite database for analysis and querying.

------------------------------------------------------------

📁 Dataset

- Source: Yelp Open Dataset from Kaggle/Yelp Academic Dataset
- Files used:
  - business.json
  - user.json
  - review.json
  - checkin.json
  - tip.json

Each file contains different information:
- `business.json`: Business details (name, category, location, stars, etc.)
- `user.json`: Information about users (review count, friends, etc.)
- `review.json`: Reviews written by users
- `checkin.json`: Check-in details
- `tip.json`: Short tips or suggestions by users

------------------------------------------------------------

🧠 Project Workflow (ETL)

1. 🔍 Extract
- Read all JSON files using Python’s built-in `json` module and `pandas`
- Parsed each file into a structured DataFrame format
- Handled nested and complex JSON objects carefully

2. 🧹 Transform
- Cleaned null/missing data
- Renamed columns for better readability
- Filtered unnecessary data and retained only required fields
- Performed data type conversions
- Normalized nested columns (like hours, categories, friends list, etc.)

3. 💾 Load
- Created a local SQLite database (`yelp.db`) using `sqlite3`
- Created separate tables: `business`, `user`, `review`, `checkin`, `tip`
- Inserted transformed DataFrames into respective tables
- Ensured proper schema design and indexing for query optimization

------------------------------------------------------------

📊 Technologies Used

- Python
- Pandas
- SQLite (sqlite3)
- JSON Parsing
- Google Colab / Jupyter Notebook
- SQL Queries for testing loaded data

------------------------------------------------------------

🧪 Sample Analysis Performed

- Top 10 businesses with the most reviews
- Average rating per business category
- User with the highest number of friends
- Most common check-in hours
- Sentiment analysis prep from review texts (optional idea)

------------------------------------------------------------

✅ Learning Outcomes

- Understood how to handle real-world JSON datasets
- Built a clean ETL pipeline from scratch
- Improved knowledge of database schema design and optimization
- Practiced SQL queries on normalized tables

------------------------------------------------------------

📂 Folder Structure (Example)

Yelp_ETL_Project/
├── datasets/                - Raw Yelp dataset JSON files
├── cleaned_data/            - Transformed CSVs (optional)
├── yelp.db                  - SQLite database file
├── etl_pipeline.ipynb       - Jupyter notebook with complete ETL code
├── requirements.txt         - Python dependencies
└── README.txt               - Project documentation (this file)

------------------------------------------------------------

🚀 How to Run

1. Place all dataset `.json` files inside the `datasets/` folder.
2. Run `etl_pipeline.ipynb` step-by-step in Jupyter or Google Colab.
3. SQLite database `yelp.db` will be created with populated tables.
4. You can use any SQL browser (DB Browser for SQLite) to view or query the data.

------------------------------------------------------------

🙋‍♀️ Author

Bhavana M  
BSc (Hons) Computer Science  
RV University, Bengaluru  
GitHub: https://github.com/bhavanagowda04

------------------------------------------------------------
