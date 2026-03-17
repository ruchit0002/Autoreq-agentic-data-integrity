# AutoReg: Agentic AI for Data Integrity

## Overview

AutoReg is an **Agentic AI-based system** designed to automatically detect and explain anomalies in datasets.
Unlike traditional data cleaning methods that rely on fixed rules, AutoReg **analyzes data patterns, identifies inconsistencies, and provides explanations for anomalies**.

This project demonstrates how AI systems can move from **passive data processing to active data reasoning**.

---

## Problem Statement

Traditional data cleaning approaches:

* Apply static rules (e.g., fill missing values)
* Cannot detect semantic errors (e.g., age = 200)
* Lack contextual understanding

AutoReg addresses this by introducing an **intelligent agent** that:

* Detects anomalies
* Understands why they occur
* Explains abnormal data behavior

---

## Key Features

* Automatic dataset analysis (no manual configuration required)
* Detects anomalies using machine learning
* Works with **any dataset**
* Provides explanation of abnormal values
* Displays results in clean tabular format

---

## How It Works

### Step 1: Dataset Input

The system takes any CSV dataset as input.

### Step 2: Schema Understanding

AutoReg automatically identifies numerical columns.

### Step 3: Model Training

Uses **Isolation Forest** to learn normal data patterns.

### Step 4: Anomaly Detection

Each row is classified as:

* `1` → Normal
* `-1` → Anomaly

### Step 5: Explanation Engine

For each anomaly:

* Compares values with dataset mean and standard deviation
* Identifies abnormal columns

---

## Workflow

```
Dataset
   ↓
Schema Detection
   ↓
Model Training (Isolation Forest)
   ↓
Anomaly Detection
   ↓
Explanation Generation
   ↓
Clean Insights
```

---

## Technologies Used

* **Python**
* **Pandas** (data processing)
* **Scikit-learn** (Isolation Forest)
* **Google Colab / Jupyter Notebook**

---

## Example Output

### Detected Anomalies

| ApplicantIncome | LoanAmount | anomaly |
| --------------- | ---------- | ------- |
| 10000000        | 999999     | -1      |

### Explanation Table

| Row | Column          | Value    | Mean | StdDev |
| --- | --------------- | -------- | ---- | ------ |
| 15  | ApplicantIncome | 10000000 | 5400 | 3200   |

---

## Installation

```bash
pip install pandas scikit-learn
```

---

## Usage

Run the script:

```bash
python autoreq.py
```

Enter dataset name:

```
Enter dataset file name: Loan_approval_data.csv
```

---

---

## Why This Project Matters

Poor data quality leads to:

* Incorrect analytics
* Faulty machine learning models
* Business losses

AutoReg introduces **Agentic AI**, where systems can:

* Detect problems
* Reason about data
* Provide intelligent insights

---

## Future Improvements

* Integration with LLMs (e.g., Gemini) for better reasoning
* Automatic data correction
* Real-time data monitoring
* Web dashboard interface

---

## Author

Ruchit Bhalekar
