# 🎬 Analysis of Netflix Movies & TV Shows

An exploratory data analysis project on the [Netflix Movies and TV Shows dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows) from Kaggle — uncovering trends in content releases, genres, cast/directors, durations, and ratings to understand how Netflix's catalog has evolved over time.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas" alt="Pandas">
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen" alt="Status">
</p>

---

## 📌 Overview

Netflix is one of the largest streaming platforms in the world, and understanding what content performs well — and how the catalog has grown — offers valuable insight into audience preferences and platform strategy.

This project explores the Netflix dataset to answer questions such as:

- How long does it take for content to be added to Netflix after release?
- How many Movies vs. TV Shows are on the platform, and how has that mix changed over time?
- Which countries produce the most content for Netflix?
- Who are the most frequently appearing directors and actors/actresses?
- What are the most common genres, and how do movie durations vary by country?
- What does the distribution of content ratings look like?

## 📂 Repository Structure

| File | Description |
|---|---|
| `netflix.csv` | Raw Netflix dataset (8,807 titles, 12 columns) |
| `IMDb-sample.csv` | Supplementary IMDb sample data |
| `Project_Netflix_Data_Analysis.ipynb` | Jupyter notebook with the full data analysis and visualizations |
| `project_netflix_data_analysis.py` | Python script version of the analysis |
| `Analysis of Netflix Movies & TV Shows.pdf` | Full written report of findings and methodology |
| `README.md` | Project overview (this file) |

## 🗂️ Dataset

The dataset contains **8,807 rows** and **12 columns**:

| Column | Description |
|---|---|
| `show_id` | Unique ID of each show |
| `type` | Movie or TV Show |
| `title` | Name of the show |
| `director` | Director(s) of the show |
| `cast` | Actors/actresses in the show |
| `country` | Countries where the show is available |
| `date_added` | Date the show was added to Netflix |
| `rating` | Content rating |
| `release_year` | Year the show was released |
| `duration` | Length of the show (minutes or seasons) |
| `listed_in` | Genre(s) of the show |
| `description` | Brief summary of the show |

**Source:** Data collected and shared publicly by Shivam Bansal on Kaggle, originally sourced from [Flixable](https://flixable.com/).

## 🧹 Data Cleaning

The raw dataset had missing values in several fields, which were identified and addressed before analysis:

| Column | Missing Values |
|---|---|
| `director` | 2,634 |
| `country` | 831 |
| `cast` | 825 |
| `date_added` | 10–17 |
| `rating` | 4 |
| `duration` | 3 |

Missingness patterns were visualized using a heatmap, and duplicate records were identified for consolidation.

## 📊 Key Findings

- **Content mix:** ~68.4% of Netflix's catalog is Movies, with the remainder being TV Shows.
- **Top content-producing countries:** The United States leads by a wide margin, followed by India.
  - Top countries for **TV Shows**: United States, United Kingdom, Japan
  - Top countries for **Movies**: United States, India, United Kingdom
- **Movie duration:** Movies produced in India tend to run the longest on average (~127 minutes). Overall, most movies fall between **90–99 minutes**.
- **Growth trend:** Content additions grew steadily from the mid-2000s, spiking sharply between 2016–2019, before slowing down in 2020 due to the COVID-19 pandemic's impact on production.
- **Top 5 Directors** (by number of titles): Rajiv Chilaka, Jan Suter, Raul Campos, Marcus Raboy, Suhas Kadav
- **Top 5 Actors/Actresses** (by number of appearances): Anupam Kher, Shah Rukh Khan, Julie Tejwani, Naseeruddin Shah, Takahiro Sakurai
- **Content ratings:** The majority of titles are rated **TV-MA**, indicating a large share of content aimed at mature audiences.
- **Genres:** International Movies, Dramas, and Comedies dominate the catalog, visualized through genre, title, and cast word clouds.

## 🛠️ Methodology

1. **Data loading & inspection** — reviewed structure, types, and summary statistics of the dataset.
2. **Data cleaning** — identified and handled missing values and duplicates; visualized missingness with a heatmap.
3. **Exploratory analysis** — used bar charts, histograms, pie charts, and word clouds to explore:
   - Content distribution by country
   - Trends in Movies vs. TV Shows over release years
   - Duration distributions
   - Content rating breakdown
   - Top directors and actors/actresses
   - Genre frequency via word clouds (title, cast, and genre fields)
4. **Sentiment analysis** — explored sentiment trends across content descriptions over time.

## 🚀 Getting Started

**Clone the repository:**
```bash
git clone <your-repo-url>
cd <repo-folder>
```

**Install dependencies:**
```bash
pip install pandas numpy matplotlib seaborn wordcloud
```

**Run the analysis:**
- Open `Project_Netflix_Data_Analysis.ipynb` in Jupyter Notebook / JupyterLab, **or**
- Run the script directly:
```bash
python project_netflix_data_analysis.py
```

## 🔮 Future Work

- Expand the dataset and feature set with more recent Netflix catalog data.
- Apply machine learning (e.g., logistic regression) to predict genre or content success.
- Build a content recommendation system based on description text similarity.
- Deeper text-based sentiment and thematic analysis of show descriptions.

## 🔗 Quick Links

<p align="center">
  <a href="https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/Project_Netflix_Data_Analysis.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
  </a>
  &nbsp;&nbsp;
  <a href="https://github.com/YOUR_USERNAME/YOUR_REPO/blob/main/Analysis%20of%20Netflix%20Movies%20%26%20TV%20Shows.pdf">
    <img src="https://img.shields.io/badge/Read-Full%20Report%20(PDF)-red?logo=adobeacrobatreader" alt="Read the Report">
  </a>
</p>

## 📚 References

- [Netflix Movies and TV Shows Dataset — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- [Netflix EDA & Recommendation System — Kaggle](https://www.kaggle.com/shivanirana63/netflix-eda-movie-recommendation-system/data)
- [Netflix — Wikipedia](https://en.wikipedia.org/wiki/Netflix)

## 📄 License

This project is intended for educational and research purposes. Dataset usage follows Kaggle's public domain terms.

---

<p align="center">⭐ If you found this project useful, consider giving it a star!</p>
