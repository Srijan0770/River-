# River-

River- is a Python-based river water quality analysis project focused on checking pH levels across different rivers and cities. It helps users search a river name, inspect water quality statistics, and generate reports and charts for analysis.

## Overview

The project reads river water quality data from CSV files and performs:

- river name matching using fuzzy search
- pH classification into acidic, normal, and alkaline ranges
- summary statistics for each river
- city-wise water quality analysis
- CSV export for detailed and summarized results
- visualization of pH trends and category distribution

## Features

- Search river data by approximate name using RapidFuzz
- Classify pH values based on safe and unsafe water ranges
- Identify best and worst quality cities for a selected river
- Export analysis results to CSV files
- Generate charts for average pH and category distribution
- Works with a Django project setup via `manage.py`

## Project Structure

- `dg.py` – main river analysis script
- `manage.py` – Django management entry point
- `river.csv` – river water quality dataset
- `river_with_year_2010_2020.csv` – extended river dataset
- `db.sqlite3` – SQLite database used by Django
- `.github/` – GitHub workflow configuration

## Tech Stack

- Python
- Django
- Pandas
- RapidFuzz
- Matplotlib
- Tabulate
- SQLite

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Srijan0770/River-.git
   cd River-
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/macOS
   venv\Scripts\activate      # Windows
   ```

3. Install dependencies:

   ```bash
   pip install django pandas rapidfuzz matplotlib tabulate
   ```

## Run the Django Project

```bash
python manage.py migrate
python manage.py runserver
```

Then open the local server in your browser, typically:

```text
http://127.0.0.1:8000/
```

## Run the River Analysis Script

The script in `dg.py` is designed to query a river name and print a detailed summary. Before running it, check the file path in the script:

```python
file_path = r"C:\Users\SRIJAN JANA\OneDrive\Desktop\river.csv"
```

Update it to match the actual location of your CSV file or place the CSV inside the project folder and change the path accordingly.

Then run:

```bash
python dg.py
```

When prompted, enter a river name such as:

```text
Ganga
```

The tool will generate:

- a detailed pH summary
- best and worst cities based on pH
- CSV reports
- charts for city-wise pH analysis and category distribution

## pH Safety Standard

The project classifies pH using the standard safe range:

- Acidic: below 6.5
- Normal/Safe: 6.5 to 8.5
- Alkaline: above 8.5

## Notes

This project is useful for educational and analytical purposes, especially for environmental data analysis and river health monitoring.

## License

This project does not currently include a license file. If you plan to publish or share it publicly, consider adding an open-source license such as MIT.
