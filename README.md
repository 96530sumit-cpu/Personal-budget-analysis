# PEPA – Personal Expense Pattern Analyzer

PEPA (Personal Expense Pattern Analyzer) is a beginner-friendly personal finance dashboard built with **Python, Streamlit, Pandas, and Matplotlib**. It helps users record daily expenses, understand spending patterns, monitor a monthly budget, and export expense reports.

## Features

- **Add expenses:** Record the date, category, description, amount, and payment mode.
- **Expense summary:** View total expenses, transaction count, and average transaction amount.
- **Category analysis:** Explore category-wise spending with bar and pie charts.
- **Monthly analysis:** Review month-wise totals and compare the latest two months.
- **Daily analysis:** View daily spending trends and summary statistics.
- **Budget alert:** Set a monthly budget and see remaining funds, with alerts when 80% or 100% of the budget is reached.
- **Smart insight:** Identify the category with the highest total spending.
- **Filters:** Filter records by category and date range.
- **Export reports:** Download expense data as CSV, Excel, or PDF.

## Technology Stack

- Python
- Streamlit
- Pandas
- Matplotlib
- ReportLab (PDF export)
- OpenPyXL (Excel export)
- Custom CSS

## Project Structure

```text
PEPA-Expense-Tracker/
├── app.py
├── analysis.py
├── requirements.txt
├── style.css
└── data/
    └── expense_template.csv
```

> The application creates `data/expenses.csv` automatically when it is first run, if the file does not already exist.

## Requirements

- Python 3.9 or later
- pip
- A web browser

## Installation and Setup

1. **Download or clone** this project and open its folder in a terminal.

2. **Create a virtual environment** (recommended):

   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment:**

   Windows:
   ```bash
   venv\Scripts\activate
   ```

   macOS/Linux:
   ```bash
   source venv/bin/activate
   ```

4. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

5. **Run the Streamlit application:**

   ```bash
   streamlit run app.py
   ```

6. Streamlit will display a local URL in the terminal (usually `http://localhost:8501`). Open it in your browser.

## How to Use

1. Open the dashboard in your browser.
2. Use **Add New Expense** in the sidebar.
3. Enter the expense date, category, description, amount, and payment mode.
4. Select **Add Expense** to save the record.
5. Review the summary cards, charts, monthly and daily analysis, and smart insights.
6. Set a monthly budget to monitor spending.
7. Use the filters to view selected categories or date ranges.
8. Download CSV, Excel, or PDF reports when required.

## Expense Data Format

The application stores records in `data/expenses.csv` with these columns:

| Column | Description |
|---|---|
| `Date` | Expense date (`YYYY-MM-DD`) |
| `Category` | Expense category |
| `Description` | Short details about the expense |
| `Amount` | Expense amount in INR |
| `Payment_Mode` | UPI, Cash, or Card |

A starter template is included at `data/expense_template.csv`.

## Running the Optional Analysis Script

The repository also includes `analysis.py`, a command-line analysis script that reads `data/expenses.csv` and prints total expenses, category totals, the highest-spending category, and average expense. It also displays category charts.

Run it after the application has created the expense data file:

```bash
python analysis.py
```

## Notes

- Expense records are stored locally in a CSV file; this project does not include cloud synchronization or user authentication.
- Keep a backup of `data/expenses.csv` if you want to preserve your records.
- Run commands from the project root folder so that relative file paths work correctly.
- The dashboard uses Indian Rupees (₹) for displayed amounts.

## Future Improvements

- Add user login and separate profiles.
- Add recurring expense support.
- Add spending forecasts and more advanced analytics.
- Add cloud database storage and data backup.
- Add configurable expense categories.

## Author

**Project:** PEPA – Personal Expense Pattern Analyzer  
**Author:** Sumit Yadav

**Purpose:** Personal expense tracking and spending-pattern analysis
