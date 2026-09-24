# 🌊 River Water Quality Analysis

A Python and Django-based **River Water Quality Analysis** project for analyzing pH levels across different rivers and cities. The project allows users to search for rivers, analyze water quality, classify pH levels, generate statistics, and visualize results through charts.

## 📌 Overview

The project analyzes river water-quality data stored in CSV files and provides:

* 🔎 River-name search using fuzzy matching
* 🧪 pH-based water-quality classification
* 📊 River and city-wise statistics
* 🏙️ City-wise pH analysis
* 📈 Data visualization using charts
* 📄 CSV report generation
* 🌐 Django-based web interface
* 🗃️ SQLite database support

## ✨ Features

### 🔍 Fuzzy River Search

Users can search for a river using an approximate name. The project uses **RapidFuzz** to find the closest matching river name.

### 🧪 pH Classification

The project classifies water based on pH values:

| pH Value  | Classification       |
| --------- | -------------------- |
| Below 6.5 | 🔴 Acidic / Unsafe   |
| 6.5 – 8.5 | 🟢 Normal / Safe     |
| Above 8.5 | 🟠 Alkaline / Unsafe |

### 📊 Water Quality Analysis

For a selected river, the project can provide:

* Average pH
* Minimum pH
* Maximum pH
* Number of observations
* City-wise pH statistics
* pH category distribution
* Best and worst cities based on pH

### 📈 Data Visualization

The project generates charts such as:

* City-wise average pH
* pH category distribution
* River water-quality statistics
* Safe pH range visualization

### 📄 CSV Reports

Analysis results can be exported into CSV files for further processing and documentation.

---

## 🛠️ Tech Stack

| Technology | Purpose                   |
| ---------- | ------------------------- |
| Python     | Core programming          |
| Django     | Web application           |
| Pandas     | Data processing           |
| RapidFuzz  | Fuzzy river-name matching |
| Matplotlib | Data visualization        |
| Tabulate   | Formatted terminal output |
| SQLite     | Database                  |

---

## 📁 Project Structure

```text
River-/
│
├── dg.py
├── manage.py
├── river.csv
├── river_with_year_2010_2020.csv
├── db.sqlite3
│
├── .github/
│   └── workflows/
│
└── Django application files
```

### Important Files

**`dg.py`**
Main Python river-analysis script.

**`manage.py`**
Django project management entry point.

**`river.csv`**
Main river water-quality dataset.

**`river_with_year_2010_2020.csv`**
Extended dataset containing yearly river data.

**`db.sqlite3`**
SQLite database used by the Django application.

**`.github/`**
Contains GitHub workflow configuration.

---

# 🚀 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/Srijan0770/River-.git
```

Move into the project directory:

```bash
cd River-
```

## 2. Create a Virtual Environment

### Windows

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### Linux/macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

## 3. Install Dependencies

```bash
pip install django pandas rapidfuzz matplotlib tabulate
```

---

# 🌐 Run the Django Project

Apply the database migrations:

```bash
python manage.py migrate
```

Start the development server:

```bash
python manage.py runserver
```

Open your browser and visit:

```text
http://127.0.0.1:8000/
```

---

# 🧪 Run the River Analysis Script

The `dg.py` script can be used independently for river analysis.

Before running the script, check the CSV file path inside `dg.py`.

Example:

```python
file_path = r"C:\Users\SRIJAN JANA\OneDrive\Desktop\river.csv"
```

Change this path according to where your dataset is stored.

You can also place `river.csv` inside the project directory and update the code accordingly.

Run:

```bash
python dg.py
```

Enter a river name when prompted:

```text
Enter river name: Ganga
```

The program can generate:

* Detailed pH statistics
* City-wise analysis
* Best and worst city results
* CSV reports
* pH visualization charts
* pH category distribution

---

# 📊 Example Analysis

For a selected river, the system can analyze cities associated with that river and calculate their average pH.

The results can then be visualized using charts to make comparison and interpretation easier.

---

# 🎯 Project Objectives

The main objectives of this project are:

1. Analyze river water-quality data using Python.
2. Identify pH conditions across different rivers and cities.
3. Classify water into acidic, normal, and alkaline categories.
4. Provide an easy-to-use river search system.
5. Generate statistical reports automatically.
6. Visualize water-quality information using graphs.
7. Provide a Django-based interface for accessing the analysis.

---

# 🌱 Educational Purpose

This project is intended for **educational and analytical purposes**. It demonstrates how Python, data analysis, machine-learning-related techniques, visualization, and Django can be combined to build an environmental monitoring application.

The pH classification used in this project should not be treated as a complete assessment of drinking-water or ecological safety. A comprehensive water-quality assessment requires additional parameters and applicable regulatory standards.

---

# 📌 Future Improvements

Possible future improvements include:

* 🤖 Machine-learning-based water-quality prediction
* 📍 Interactive geographical river maps
* 📅 Year-wise water-quality trends
* 📊 Additional water-quality parameters
* 👤 User authentication
* ☁️ Cloud deployment
* 📱 Mobile-friendly interface
* 🔔 Water-quality alerts
* 📈 Interactive dashboards

---

# 📜 License

This project currently does not include a license file.

If you plan to make the project open source, you can add an appropriate license such as the **MIT License**.

---

## 👨‍💻 Author

**Srijan Kumar Jana**

GitHub:
https://github.com/Srijan0770

---

⭐ If you find this project useful, consider giving the repository a star!
