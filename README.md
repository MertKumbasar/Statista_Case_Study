# Data Quality Checks for Company Financial Data

## Overview
This project implements automated data quality checks for company financial data extracted from multiple sources.  
The goal is to detect inconsistencies, missing values, implausible financial figures, and potential extraction errors before storing data in a database.

The project was developed as part of a data quality case study.

---

## Pipeline Architecture

The validation pipeline follows these steps:

1. **Load Data**
2. **Completeness Check** – detect missing values
3. **Correctness Check** – validate logical constraints
4. **Consistency Check** – ensure stable attributes per company
5. **Statistical Plausibility** – detect abnormal year-over-year revenue changes
6. **LLM Semantic Validation** – GPT evaluates suspicious anomalies
7. **Export Flagged Dataset**

Output: an Excel file with additional columns flagging detected issues.

---

## Setup

### 1. Install dependencies
```bash
pip install -r requirements.txt

openai api key is requierd inside the .env file for LLM analysis
