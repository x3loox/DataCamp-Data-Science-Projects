# 🎬 Netflix 1990s Movie Analysis

This project is part of my **Data Science learning journey** on [DataCamp](https://www.datacamp.com/).  
It involves performing exploratory data analysis (EDA) on Netflix movie data, focusing specifically on **movies released in the 1990s**.

---

## 📌 Project Objectives

Using the provided `netflix_data.csv` dataset, the main goals of the project are:

- 🎯 **Filter** the dataset to include only movies from the 1990s (1990–1999).
- 🎯 **Determine** the most frequent movie duration during that decade.
- 🎯 **Count** how many **short action movies** (less than 90 minutes) were released in the 1990s.

---

## 🧠 Problem Context

> You work for a production company that specializes in nostalgic movie styles. To study trends in 1990s movies, you’ll analyze Netflix’s movie data to better understand duration and genre trends during that time.

---

## 📂 Dataset Information

**File:** `netflix_data.csv`

| Column         | Description                         |
|----------------|-------------------------------------|
| `show_id`      | Unique ID of the show               |
| `type`         | Movie or TV Show                    |
| `title`        | Title of the show/movie             |
| `director`     | Director name                       |
| `cast`         | Cast members                        |
| `country`      | Country of origin                   |
| `date_added`   | When it was added to Netflix        |
| `release_year` | Year it was released                |
| `duration`     | Duration in minutes                 |
| `description`  | Description of the movie/show       |
| `genre`        | Genre of the movie/show             |

---

## 🧪 Analysis Overview

### ✅ Step 1: Filter Movies Released in the 1990s
```python
movies = netflix_df[netflix_df["type"] == "Movie"]
movies_1990s = movies[(movies["release_year"] >= 1990) & (movies["release_year"] <= 1999)]
```

---

### ✅ Step 2: Most Frequent Movie Duration (1990s)
```python
plt.hist(movies_1990s["duration"])
plt.title("Distribution of Movie Durations in the 1990s")
plt.xlabel("Duration (minutes)")
plt.ylabel("Number of Movies")
plt.show()

duration = 100
```
📌 **Result:** The most common movie duration in the 1990s was approximately **100 minutes**.

---

### ✅ Step 3: Count Short Action Movies (< 90 min)
```python
action_movies_1990s = movies_1990s[movies_1990s["genre"] == "Action"]
short_movie_count = sum(action_movies_1990s["duration"] < 90)
```
📌 **Result:** The number of short action movies released in the 1990s is **X**.

---

## ✅ Skills Used

- Python (`pandas`, `numpy`)
- Data visualization with `matplotlib`
- Conditional filtering & logic
- Exploratory Data Analysis (EDA)
- Jupyter Notebook formatting

---

## 📂 Project Structure  
```
Task-2-Netflix-1990s-Movie-Analysis/
│
├── data/
│   └── netflix_data.csv
├── notebooks/
│   └── netflix_1990s_eda.ipynb
├── requirements.txt
└── README.md
```

---

## 📦 Installation & Usage  

1️⃣ Clone the repository  
```bash
git clone https://github.com/x3loox/DataCamp-Data-Science-Projects/blob/main/Task-2-Netflix-1990s-Movie-Analysis.git
cd Task-2-Netflix-1990s-Movie-Analysis
```

2️⃣ Install dependencies  
```bash
pip install -r requirements.txt
```

3️⃣ Run the notebook  
```bash
jupyter notebook notebooks/netflix_1990s_eda.ipynb
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