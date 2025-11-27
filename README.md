📘 PySpark Books & Ratings Analysis

This project is a hands-on practice using PySpark RDDs and DataFrames on two CSV datasets: books.csv and ratings.csv.
The goal is to understand Spark’s basic workflow for loading, exploring, filtering, and transforming data.

📂 Datasets Used
1. books.csv
2. ratings.csv



⚙️ Environment

This project was executed on:
Spark 2.4.5
Python 3.6
Big Data VM (Linux)
PySpark running through Jupyter Notebook

🚀 What I Did in This Project
✔ RDD Operations
Loaded CSV files from local path using sc.textFile()
Viewed RDD content using:
first()
take(n)
Extracted header and split it into columns
Cleaned and processed raw text lines
Demonstrated basic transformations
DataFrame Operations
Loaded the same CSVs into DataFrames using spark.read.csv()


🧠 Key Learnings

Difference between RDD and DataFrame APIs
How Spark reads files from local filesystem vs HDFS
Schema inference and column selection
How filtering and ordering work internally in Spark
Why file:/// is required in Spark to load local paths

Basic understanding of SparkSession and SparkContext

📊 Example Code Snippets
Load Data into RDD
data = sc.textFile("file:///home/talentum/test-jupyter/Ranjan/ranjan/books.csv")
data.take(5)

Load Data into DataFrame
books_df = spark.read.csv(
    "file:///home/talentum/test-jupyter/Ranjan/ranjan/books.csv",
    header=True,
    inferSchema=True
)

Filter Data
ratings_df.filter("rating <= 1").show(4)

Order Data
ratings_df.orderBy("rating", "book_id").show(50)

📁 Folder Structure (Example)
project/
│
├── books.csv
├── ratings.csv
├── notebook.ipynb
└── README.md

🎯 Purpose

This project is part of my PySpark learning journey.
The aim is to practice real data processing steps using:

RDD API

DataFrame API

CSV ingestion

Data filtering, sorting, and schema inspection

I plan to expand this project later with joins, aggregations, and visualizations.

📝 Author

Pravin
Learning Big Data, Spark, MySQL, Linux, and building strong fundamentals every day.
