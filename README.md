# 📊 Python Ranking Table

A simple Python project that demonstrates how to **sort data, assign rankings, and create a visually styled ranking table using Pandas**.

The project uses a sample dataset containing student names and scores. The scores are sorted from highest to lowest, rankings are automatically assigned, and Pandas styling is used to highlight the score values.

## 🚀 Project Overview

This project demonstrates three useful Pandas techniques:

* Sorting a DataFrame by a column
* Creating a ranking column dynamically
* Styling DataFrame values for better visualization

### Example Dataset

| Name | Score |
| ---- | ----: |
| A    |    78 |
| B    |    95 |
| C    |    84 |
| D    |    91 |
| E    |    88 |

After sorting and ranking:

| Rank | Name | Score |
| ---: | ---- | ----: |
|    1 | B    |    95 |
|    2 | D    |    91 |
|    3 | E    |    88 |
|    4 | C    |    84 |
|    5 | A    |    78 |

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Jupyter Notebook** / Python environment

## 📌 Code

```python
import pandas as pd

df = pd.DataFrame({
    "Name": ["A", "B", "C", "D", "E"],
    "Score": [78, 95, 84, 91, 88]
})

# Sort scores from highest to lowest
df = df.sort_values(by="Score", ascending=False)

# Assign rankings
df["Rank"] = range(1, len(df) + 1)

# Style the ranking table
df.style \
    .background_gradient(subset=["Score"]) \
    .highlight_min(subset=["Score"])
```

## 🔍 How It Works

### 1. Create the DataFrame

A Pandas DataFrame is created containing names and their corresponding scores.

```python
df = pd.DataFrame({
    "Name": ["A", "B", "C", "D", "E"],
    "Score": [78, 95, 84, 91, 88]
})
```

### 2. Sort the Scores

The `sort_values()` function sorts the students according to their scores.

```python
df = df.sort_values(by="Score", ascending=False)
```

`ascending=False` means the highest score appears first.

### 3. Assign Rankings

A `Rank` column is created using Python's `range()` function.

```python
df["Rank"] = range(1, len(df) + 1)
```

This produces rankings from **1 to 5** based on the sorted order.

### 4. Style the Table

Pandas' `.style` functionality is used to make the table easier to read.

```python
df.style \
    .background_gradient(subset=["Score"]) \
    .highlight_min(subset=["Score"])
```

* `background_gradient()` applies a color gradient to the scores.
* `highlight_min()` highlights the lowest score.

## 🎯 Learning Objectives

By completing this project, you can learn how to:

* Create DataFrames with Pandas
* Sort DataFrame records
* Generate rankings programmatically
* Use `range()` with DataFrame length
* Apply conditional styling to DataFrames
* Present data in a more readable format

## 💡 Possible Improvements

This project can be extended by:

* Using a larger dataset
* Handling tied scores
* Adding grades such as A, B, C, and D
* Highlighting the highest score
* Calculating the average score
* Adding percentage scores
* Creating charts to visualize rankings
* Loading the data from a CSV or Excel file
* Building an interactive ranking dashboard

## 📁 Project Structure

```text
python-ranking-table/
│
├── ranking_table.py
└── README.md
```

## 👨‍💻 Author

**Charles Akinnurun**

Machine Learning Engineer | AWS AI/ML Scholar '26 | Computer Science Student

---

⭐ If you found this project useful, consider giving the repository a star!
