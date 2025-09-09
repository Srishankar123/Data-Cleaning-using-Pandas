# Data Cleaning using Pandas

This repository contains a Jupyter Notebook that demonstrates step-by-step **data cleaning techniques in Python using Pandas**.  
The dataset used is a **Customer Call List (Excel file)** that required extensive preprocessing before it could be used for reliable analysis.

---

## 📌 Purpose of Data Cleaning

The raw dataset contained multiple quality issues such as:
- Duplicate entries  
- Irrelevant columns  
- Messy string formatting (extra symbols, spaces, slashes, numbers in text)  
- Missing or invalid values in fields like phone numbers and names  

Cleaning this data was essential to:
- Ensure accuracy and consistency in the customer records  
- Make the dataset ready for further analysis, reporting, or integration into downstream systems  
- Improve data integrity for decision-making and insights  

---

## 🛠️ Cleaning Workflow

The notebook covers the following steps:

1. **Importing the dataset**
   ```python
   import pandas as pd
   df = pd.read_excel("Customer Call List.xlsx")
   ```

2. **Removing Duplicates**
   ```python
   df = df.drop_duplicates()
   ```

3. **Dropping Irrelevant Columns**
   ```python
   df = df.drop(columns="Not_Useful_Column")
   ```

4. **Cleaning String Data**
   - Strip unwanted characters (`/`, `_`, `.`, numbers) from names  
   - Standardize formatting using `.str.strip()`, `.str.replace()`

5. **Handling Phone Numbers**
   - Remove non-numeric characters with regex  
   - Ensure consistent digit length

6. **Fixing Null or Empty Values**
   - Detect missing values with `df.isnull()`  
   - Replace with appropriate defaults or drop when necessary

7. **Standardizing Data**
   - Consistent casing for categorical fields  
   - Correct data types (e.g., converting strings to numeric)

---

## 📊 Why This Matters

Dirty data leads to **inaccurate insights and poor business decisions**.  
By cleaning the customer call list, we ensure:
- Reliable analysis of customer behavior  
- Accurate contact information for follow-ups  
- Better reporting without duplicates or corrupted records  

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/Srishankar123/Data-Cleaning-using-Pandas.git
   ```

2. Install dependencies:
   ```bash
   pip install pandas openpyxl
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open `Data Cleaning using Pandas.ipynb` and run the cells step by step.

---

## 🧰 Requirements

- Python 3.x  
- pandas  
- openpyxl (for Excel file reading)  
- Jupyter Notebook  

---

## 📂 Files

- `Data Cleaning using Pandas.ipynb` → Main notebook with all cleaning steps  
- `Customer Call List.xlsx` → Input dataset (not included here due to privacy)  
- `cleaned_data.xlsx` → Example of cleaned dataset output (if saved)  

---

## ✅ Outcome

After cleaning, the dataset is:
- Free of duplicates and irrelevant fields  
- Properly formatted with clean names and valid phone numbers  
- Standardized and ready for analysis or business use  
