# Tanzania Data Science Learning Path

A self-contained, six-level progression through core data science skills — pandas, visualization, statistics, data cleaning, and machine learning — built entirely around Tanzanian data: population, agriculture, and insurance.

## What this is

This isn't a single project — it's a structured set of Jupyter notebooks, each one teaching a specific skill on top of the last, using data grounded in Tanzania rather than generic textbook datasets (Titanic, Iris, etc.). The goal was to learn data science fundamentals while working with numbers that actually mean something in a local context — regional population, maize production, insurance access.

## Real data vs. illustrative data — read this first

This is the most important thing to understand before using anything here.

**Real data:**
- **Regional population figures** (`Population_2022` columns across notebooks) come from Tanzania's 2022 Population and Housing Census, published by the National Bureau of Statistics (NBS — [nbs.go.tz](https://www.nbs.go.tz)). Only regions with confirmed, publicly verifiable figures are included — this is a subset of Tanzania's 31 regions, not all of them.

**Illustrative / synthetic data:**
- **Maize production by region** is modeled on real, documented patterns (Southern Highlands and the Lake Zone are Tanzania's known top maize belts; Arusha and Ruvuma have shown recent production gains; Dar es Salaam and Zanzibar have minimal agricultural land) — but the specific tonnage numbers are constructed for this project, not pulled from an official regional-level source, because that granularity isn't publicly available in verified form.
- **Insurance claims data, rainfall data, and insurance penetration figures** are entirely synthetic, generated with `numpy.random` to reflect realistic relationships (e.g. rainfall correlating with yield, urban regions having higher insurance penetration) — built specifically to have clean, learnable patterns for practicing statistics and ML techniques.

Every notebook states clearly, in its opening markdown cell, which category each dataset it uses falls into. **None of the illustrative data should be treated as real statistics, cited, or used for actual business/policy decisions.**

## Structure

| File | Topic | Dataset |
|---|---|---|
| `roadmap.md` | Full roadmap and skill breakdown | — |
| `level1_pandas_basics.ipynb` | pandas fundamentals — indexing, filtering, groupby, missing values | Real population data |
| `level2_visualization.ipynb` | matplotlib/seaborn — bar charts, scatter plots, subplots, merging | Real population + illustrative maize |
| `level3_statistics.ipynb` | Correlation, hypothesis testing, confidence intervals | Synthetic rainfall/yield |
| `level4_cleaning.ipynb` | Diagnosing and cleaning messy real-world-style data | Synthetic insurance claims |
| `level5_ml_intro.ipynb` | Classification with scikit-learn, evaluation metrics, data leakage | Synthetic insurance claims |
| `level6_capstone.ipynb` | Combining all three datasets into one analysis with a written summary | Real + illustrative, merged |

Each notebook is self-contained — data is generated or defined inline, so any notebook can be run independently with `Kernel > Restart & Run All` without needing to run the others first.

## Requirements

```
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

## Why this approach

Most beginner data science material uses the same handful of generic datasets, which makes it easy to follow tutorials without ever building the judgment to work with messy, real, locally-relevant data. This project deliberately:
- Uses **real Tanzanian government data** wherever it's actually available and verifiable
- Is **explicit and upfront** about which data is synthetic, and why (either because real granular data isn't public, or because a technique like statistical hypothesis testing needs more data points than 31 regions can provide)
- Builds toward datasets and problems (insurance claims, regional agriculture) that connect directly to real projects — MIA (Mwaluseke Insurance Agency), InsurePro, and future work with real NBS/FAOSTAT/World Bank data

## What's next

The natural extension of this roadmap is swapping the illustrative datasets for real ones:
- Pulling live regional data via APIs (Open-Meteo, FAOSTAT, World Bank) the way the earlier IRS (Information Rendering System) project did
- Applying the Level 4/5 cleaning-and-modeling workflow to real, anonymized MIA claims data
- Feeding a real version of the Level 6 dashboard into InsurePro as an analytics feature

## Author

Ambilikisye Mwaluseke (Amby) — DCS student, Mbeya University of Science and Technology.
