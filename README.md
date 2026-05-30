# 🎬 Netflix Movies — Data Analysis Project

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)

> An Exploratory Data Analysis (EDA) project performed on a Netflix movies dataset — exploring genres, popularity scores, vote averages, and release year trends.

---

## 📌 Project Overview

This project analyzes **9,827 Netflix movies** to answer key questions about content trends on the platform:
- Which genres appear most frequently?
- What are the voting patterns across movies?
- Which movies have the highest and lowest popularity?
- Which year had the most movie releases?

---

## 📂 Dataset

**File:** `mymoviedb.csv`

| Column | Description |
|---|---|
| `Title` | Name of the movie |
| `Genre` | Movie genre(s) — comma-separated |
| `Release_Date` | Date of release |
| `Popularity` | Popularity score |
| `Vote_Average` | Average user rating |
| `Vote_Count` | Total number of votes |
| `Overview` | Movie description *(dropped during cleaning)* |
| `Original_Language` | Language of origin *(dropped during cleaning)* |
| `Poster_Url` | URL of movie poster *(dropped during cleaning)* |

---

## 🛠️ Libraries Used

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## 🔍 Data Cleaning & Preprocessing

The following steps were applied to prepare the data for analysis:

- **Date Conversion:** `Release_Date` was converted to datetime format and only the year was extracted
- **Dropped Irrelevant Columns:** `Overview`, `Original_Language`, and `Poster_Url` were removed
- **Vote_Average Categorization:** Ratings were binned into 4 categories using a custom `categorize_col()` function:
  - `not_popular`
  - `below_avg`
  - `average`
  - `popular`
- **Genre Handling:** Comma-separated genre values were split and the dataframe was exploded so each row represents one genre per movie
- **Null Values:** Any rows with NaN values were dropped after categorization

---

## 📊 Exploratory Data Analysis (EDA)

### Q1. What is the most frequent genre on Netflix?
**Drama** is the most frequent genre, appearing in over **14%** of all entries across 19 unique genres.

### Q2. Which genre receives the highest votes?
About **25.5%** of movies fall in the `popular` vote category. **Drama** leads here as well, accounting for over **18.5%** of popular movies.

### Q3. Which movie has the highest popularity?
🕷️ **Spider-Man: No Way Home** — Genres: *Action, Adventure, Science Fiction*

### Q4. Which movie has the lowest popularity?
📽️ **The United States Thread** — Genres: *Music, Drama, War, Sci-Fi, History*

### Q5. Which year had the most movie releases?
📅 **2020** had the highest number of movie releases in this dataset.

---

## 📈 Visualizations

All visualizations were built using **Seaborn** and **Matplotlib**:

- Genre Distribution — Horizontal Count Plot
- Vote Average Category Distribution — Count Plot
- Release Year Distribution — Histogram

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/netflix-data-analysis.git
   cd netflix-data-analysis
   ```

2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. Place the `mymoviedb.csv` dataset in the project folder.

4. Launch the notebook:
   ```bash
   jupyter notebook NetflixDSprojDA.ipynb
   ```

---

## 📁 Project Structure

```
netflix-data-analysis/
│
├── NetflixDSprojDA.ipynb   # Main analysis notebook
├── mymoviedb.csv           # Dataset (add manually)
└── README.md               # Project documentation
```

---

## 🙋‍♀️ Author

**[ VIJAY LAXMI ]**  
📧 [vijaylaxmi1130@gmail.com]  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/vijaylaxmi-mani-40a381229/)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
