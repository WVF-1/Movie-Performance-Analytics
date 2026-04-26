# Movie-Performance-Analytics
An exploration of how finances and other metadata play into the outcomes of a movie's success.

# 🎬 Movie Performance Analytics
### May Newsletter — Movie Intelligence Series (Part 1 of 3)

A three-notebook exploratory data analysis of ~45,000 films from the TMDB Movies Metadata dataset. The project investigates the financial mechanics of the film industry — which genres pay off, whether bigger budgets guarantee bigger returns, and when studios should time their releases.

This is Part 1 of a three-part May newsletter series on movie intelligence. Parts 2 and 3 will extend the analysis to cast/crew influence and audience rating behaviour respectively.

---

## 📂 Repository Structure

```
├── NB1_Data_Cleaning.ipynb        # Data loading, repair, and feature engineering
├── NB2_Financial_Analysis.ipynb   # Core financial analysis and exploratory charts
├── NB3_Newsletter_Visuals.ipynb   # Publication-ready figures and narrative summary
├── movies_metadata.csv            # Source data (upload to Colab manually — see below)
└── README.md
```

---

## 📊 Dataset

**Source:** [TMDB Movies Metadata](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset) via Kaggle  
**Size:** ~45,000 films | **Analysis-ready subset:** ~4,800 films (budget and revenue both recorded)  
**Key fields used:** `budget`, `revenue`, `genres`, `release_date`, `vote_average`, `vote_count`, `popularity`

> `movies_metadata.csv` is not committed to this repo due to file size. Download it from the Kaggle link above and upload it to your Colab environment before running.

---

## 🚀 Running the Notebooks

The notebooks are designed for **Google Colab** and must be run in order, as each one depends on outputs from the previous.

**Step 1 — Upload the data**  
Upload `movies_metadata.csv` to the Colab session storage.

**Step 2 — Run NB1**  
Cleans the raw data and saves `movies_clean.parquet` to the session. This is the only input NB2 and NB3 require.

**Step 3 — Run NB2**  
Performs the core financial analysis and saves exploratory chart PNGs.

**Step 4 — Run NB3**  
Generates six publication-ready figures for the newsletter.

---

## 🔍 Questions Explored

- Which genres deliver the highest return on investment?
- Does a bigger production budget guarantee a bigger return?
- How does ROI vary across budget tiers (micro → blockbuster)?
- Which months — and which decades — produce the most profitable releases?
- What separates the all-time hits from the all-time flops?

---

## 🎨 Visual Style

All charts use a custom cinema-inspired palette:

| Role | Colour |
|------|--------|
| Primary bars / lines | Midnight Navy `#1a1a2e` |
| Highlights / top performers | Oscar Gold `#e8b94f` |
| Warnings / flops / contrast | Cinema Crimson `#c0392b` |
| Neutral fills | Silver `#bdc3c7` |

---

## 📦 Dependencies

All standard libraries — no special installs required in Colab.

```
pandas
numpy
matplotlib
scipy
pyarrow      # for parquet read/write
```

---

## 🗺️ Series Roadmap

| Part | Focus | Status |
|------|-------|--------|
| **1 — Financial Performance** | Genre ROI, budget tiers, seasonal patterns | ✅ Complete |
| 2 — Cast, Crew & Keywords | Director ROI, actor profitability, keyword analysis | 🔜 Coming |
| 3 — Audience Ratings Behaviour | Commercial success vs audience satisfaction | 🔜 Coming |
| Final — Predictive Intelligence | ML model combining all three layers | 🔜 Coming |

---
