# 🌍 Week-1: Environmental Management & Pollution Control  

## 📌 Project Theme  
This project is part of the **Edunet AI Internship** under the theme *Environmental Management & Pollution Control*.  
For Week-1, the focus is on **data collection, cleaning, preprocessing, and basic exploratory data analysis (EDA)**.  

---

## 📊 Dataset  
- **Source**: CPCB (Central Pollution Control Board) – River Water Quality Data 2022  
- **Format**: Originally in PDF, compiled into a structured Excel file  
- **Structure**:  
  - First three columns → `Station Code`, `Name Of Monitoring Location`, `State Name`  
  - Remaining columns → Water quality parameters with **MIN** and **MAX** values:  
    - Temperature (°C)  
    - Dissolved Oxygen (mg/L)  
    - pH  
    - Conductivity (µmhos/cm)  
    - Bio-Chemical Oxygen Demand (BOD, mg/L)  
    - Nitrate (mg/L)  
    - Fecal Coliform (MPN/100mL)  
    - Total Coliform (MPN/100mL)  
    - Fecal Streptococci (MPN/100mL)  

> 🔹 Note: The cell **A2** in the Excel originally contained the text  
> `"Primary Water Quality Criteria (PWQC) notified by MoEF & CC under E (P) Rules, 1986"`.  
> Since it was not actual data, we erased it to avoid messy column names.  

---

## ✅ Work Done in Week-1  

In the provided code (`preprocessing.ipynb`), we have:  

1. **Data Import**  
   - Loaded the Excel file with multi-row headers (parameters + MIN/MAX).  
   - Flattened headers into clean names like `BOD MIN`, `BOD MAX`, etc.  
   - Renamed first three ID columns → `Station Code`, `Name Of Monitoring Location`, `State Name`.  

2. **Data Cleaning**  
   - Dropped metadata rows (criteria, headers).  
   - Converted non-numeric values (`BDL`) to `NaN`.  
   - Casted all parameter columns to numeric (float).  
   - Filled missing numeric values with column mean.  

3. **Feature Engineering**  
   - Preserved **MIN** and **MAX** values.  
   - Created new **AVG** columns = `(MIN + MAX) / 2` for easier analysis.  

4. **Exploratory Data Analysis (EDA)**  
   - Visualized missing values with a heatmap.  
   - Checked correlations between water quality parameters.  
   - Plotted distributions of parameters (pH, DO, BOD, etc. using `AVG`).  
   - State-wise average BOD comparison (bar chart).  

5. **Output**  
   - Saved cleaned dataset as `cleaned_data.csv`.  
   - Organized repo for future weeks.  

---



