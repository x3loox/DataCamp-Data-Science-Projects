# 🏫 NYC Public School SAT Analysis

This project is part of my **Data Science journey** on [DataCamp](https://www.datacamp.com/).  
It explores the SAT performance of public high schools in New York City across **math, reading, and writing** sections.

---

## 📌 Project Objectives

Using the provided `schools.csv` dataset, this project answers 3 key questions:

- ✅ Which NYC schools have the **best math results** (≥ 80% of 800)?
- ✅ What are the **top 10 performing schools** based on total SAT score?
- ✅ Which **borough** has the **highest standard deviation** in SAT performance?

---

## 🧠 Problem Context

Every year, U.S. high school students take the SAT — a standardized test measuring literacy, numeracy, and writing skills. Each section is scored out of 800.  
This analysis helps policymakers, educators, and parents understand which schools and boroughs perform best in NYC.

---

## 📂 Dataset Information

**File:** `schools.csv`

| Column             | Description                        |
|--------------------|------------------------------------|
| `school_name`      | Name of the school                 |
| `borough`          | NYC borough                        |
| `average_math`     | Average math SAT score             |
| `average_reading`  | Average reading SAT score          |
| `average_writing`  | Average writing SAT score          |

---

## 🧪 Analysis Summary

### ✅ Step 1: Best Math Results (≥ 80%)
```python
best_math_schools = schools[["school_name", "average_math"]]
best_math_schools = best_math_schools[best_math_schools["average_math"] >= 640]
best_math_schools = best_math_schools.sort_values("average_math", ascending=False)
```
📌 **Result:** These schools scored **640+ in Math**, equivalent to 80% or higher.

---

### ✅ Step 2: Top 10 Schools by Total SAT Score
```python
schools["total_SAT"] = schools[["average_math", "average_reading", "average_writing"]].sum(axis=1)
top_10_schools = schools[["school_name", "total_SAT"]].sort_values("total_SAT", ascending=False).head(10)
```
📌 **Result:** Displays the top 10 schools based on combined SAT score.

---

### ✅ Step 3: Borough with Largest Standard Deviation in SAT
```python
sat_stats = schools.groupby("borough")["total_SAT"].agg(["mean", "std"]).round(2)
largest_std_dev = sat_stats.sort_values("std", ascending=False).head(1)
```
📌 **Result:** Identified the borough with the **greatest variation** in SAT performance.

---

## ✅ Skills Used

- Python (`pandas`)
- Grouping and aggregation
- Conditional filtering
- Descriptive statistics
- Data storytelling with Jupyter Notebook

---

## 📂 Project Structure  
```
Task-1-NYC-SAT-Analysis/
│
├── data/
│   └── schools.csv
├── notebooks/
│   └── nyc-schools-sat-analysis.ipynb
├── requirements.txt
└── README.md
```

---

## 📦 Installation & Usage  

1️⃣ Clone the repository  
```bash
git clone https://github.com/x3loox/DataCamp-Data-Science-Projects/Task-1-NYC-SAT-Analysis.git
cd Task-1-NYC-SAT-Analysis
```

2️⃣ Install dependencies  
```bash
pip install -r requirements.txt
```

3️⃣ Run the notebook  
```bash
jupyter notebook notebooks/nyc-schools-sat-analysis.ipynb
```

---

## 🙌 Author

**AlaEldin Ali MohammedToum AbdElaziz**  
🇸🇩 Sudanese, based in 🇪🇬 Egypt  
- [LinkedIn](https://www.linkedin.com/in/x3loox/)  
- GitHub: [x3loox](https://github.com/x3loox)  
- Email: alaali123887@gmail.com

---

## 📜 License

This project is for **educational purposes only**.

---

✨ If you like this project, feel free to ⭐ the repo and connect with me on [LinkedIn](https://www.linkedin.com/in/x3loox/). 