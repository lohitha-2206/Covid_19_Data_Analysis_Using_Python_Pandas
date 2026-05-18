# 🦠 Covid-19 Data Analysis using Python & Pandas

## 📌 Project Introduction

This project is based on performing data analysis and preprocessing operations on a Covid-19 Dataset using Python and the Pandas library inside Jupyter Notebook. The dataset contains information related to Confirmed Cases, Deaths, Recovered Cases, and different Regions affected during the Covid-19 pandemic.

The main objective of this project is to understand how Python and Pandas are used in real-world Covid-19 data analysis for cleaning, exploring, filtering, sorting, and analyzing structured datasets efficiently.

In this project, different data analysis techniques were implemented such as:

- Data Cleaning
- Handling Missing Values
- Data Filtering
- Statistical Analysis
- GroupBy Operations
- Sorting Data
- Covid-19 Case Analysis
- Exploratory Data Analysis (EDA)
- Data Visualization

This project provides practical exposure to working with Covid-19 datasets and understanding how data analysts use Python for extracting meaningful insights from real-world pandemic data.

---

# 📂 Dataset Information

The dataset contains Covid-19 case records from different regions and countries.

### Dataset Features:

- Region/Country
- Confirmed Cases
- Death Cases
- Recovered Cases
- Observation Date

Each record in the dataset represents Covid-19 statistics reported from a specific region.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python
Python was used as the programming language for performing data analysis and dataframe operations.

## 📊 Pandas
Pandas library was used for:
- Data Cleaning
- Data Manipulation
- Handling Missing Values
- Filtering Data
- Statistical Analysis
- GroupBy Operations
- Sorting Data

## 🎨 Seaborn
Seaborn library was used for visualizing missing values using heatmaps.

## 📈 Matplotlib
Matplotlib library was used for displaying plots and visualizations.

## 📓 Jupyter Notebook
Jupyter Notebook was used to execute Python code interactively and visualize outputs step-by-step.

---

# 🔍 Pandas Functions Implemented

## 🔹 import pandas as pd
Used to import the Pandas library.

### Syntax:
```python
import pandas as pd
```

---

## 🔹 pd.read_csv()
Used to import the CSV dataset into Jupyter Notebook.

### Syntax:
```python
data = pd.read_csv("Covid_19_Data.csv")
```

---

## 🔹 count()
Counts the total number of non-null values in each column.

### Syntax:
```python
data.count()
```

---

## 🔹 isnull().sum()
Detects missing/null values from each column.

### Syntax:
```python
data.isnull().sum()
```

---

## 🔹 sns.heatmap()
Displays missing values in heatmap form.

### Syntax:
```python
sns.heatmap(data.isnull())
```

---

## 🔹 plt.show()
Displays the generated plot.

### Syntax:
```python
plt.show()
```

---

## 🔹 groupby()
Groups data according to a specific column.

### Syntax:
```python
data.groupby('Region').sum()
```

---

## 🔹 sort_values()
Sorts the dataframe according to column values.

### Syntax:
```python
data.sort_values(by=['Confirmed'])
```

---

## 🔹 Filtering Records
Used to access records based on specific conditions.

### Syntax:
```python
data[data.Region == 'India']
```

---

# 📊 Tasks Performed in the Project

## ✅ Q1) GroupBy Analysis

### Task:
Show the number of Confirmed, Deaths, and Recovered cases in each Region.

### Code Used:
```python
data.groupby('Region')[['Confirmed', 'Deaths', 'Recovered']].sum()
```

### Explanation:
- Groups records based on Region
- Calculates total confirmed, death, and recovered cases
- Helps compare Covid-19 statistics region-wise

---

# 📊 Q2) Data Filtering

### Task:
Remove all the records where Confirmed Cases are less than 10.

### Code Used:
```python
data = data[~(data.Confirmed < 10)]
```

### Explanation:
- Removes records with very low confirmed cases
- Helps focus on significant Covid-19 data

---

# 📊 Q3) Maximum Confirmed Cases

### Task:
Find the Region with the maximum number of Confirmed cases.

### Code Used:
```python
data.groupby('Region').Confirmed.sum().sort_values(ascending=False)
```

### Explanation:
- Groups records by Region
- Sorts confirmed cases in descending order
- Identifies the most affected region

---

# 📊 Q4) Minimum Death Cases

### Task:
Find the Region with the minimum number of Death cases.

### Code Used:
```python
data.groupby('Region').Deaths.sum().sort_values()
```

### Explanation:
- Groups records by Region
- Sorts death cases in ascending order
- Identifies regions with the least deaths

---

# 📊 Q5) Covid-19 Cases in India

### Task:
Find the number of Confirmed, Deaths, and Recovered cases reported from India till 29 April 2020.

### Code Used:
```python
data[data.Region == 'India']
```

### Explanation:
- Filters records related to India
- Displays Covid-19 statistics for India

---

# 📊 Q6) Sorting Data

### Task:
Sort the entire dataset based on Confirmed and Recovered cases.

### Code Used:
```python
data.sort_values(by=['Confirmed'], ascending=True)

data.sort_values(by=['Recovered'], ascending=False)
```

### Explanation:
- Sorts confirmed cases in ascending order
- Sorts recovered cases in descending order
- Helps analyze trends efficiently

---

# 📌 Important Insights

✔️ Pandas makes Covid-19 data analysis simple and efficient.

✔️ GroupBy operations help compare region-wise Covid-19 statistics.

✔️ Heatmaps help visualize missing values clearly.

✔️ Filtering and sorting records allow targeted analysis.

✔️ Statistical analysis helps identify pandemic trends.

✔️ Real-world Covid-19 datasets can be analyzed efficiently using Python.

---

# 📁 Project Structure

```text
├── Covid19_Data_Analysis.ipynb
├── Covid_19_Data.csv
├── README.md
```

---

# 🎯 Final Conclusion

This project demonstrates how Python and Pandas can be used for real-world Covid-19 data analysis and preprocessing tasks. Different operations such as handling missing values, filtering records, sorting data, statistical analysis, grouping data, and extracting meaningful insights were successfully implemented.

Through this project, practical understanding was gained in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Manipulation using Pandas
- Statistical Analysis
- GroupBy Operations
- Data Visualization
- Python-based Data Analytics

Overall, this project serves as a strong beginner-friendly foundation for learning Data Analysis and Data Science using Python.
