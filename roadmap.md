# Tanzania Data Science Roadmap — DATA workspace

Progression from pandas fundamentals to a basic ML model, all built around real or realistic Tanzanian datasets (population, agriculture, economy, insurance). Each level builds a new skill on top of the last.

## Level 1 — Pandas Fundamentals
**File:** `level1_pandas_basics.ipynb`
**Dataset:** Regional population (2022 census, National Bureau of Statistics) — real
**Skills:** DataFrame creation, indexing, sorting, filtering, groupby, handling missing values, basic summary stats
**Status:** ✅ complete

## Level 2 — Visualization
**File:** `level2_visualization.ipynb`
**Dataset:** Population (real) + maize production by region (illustrative)
**Skills:** matplotlib/seaborn — bar charts, histograms, scatter plots, subplots, merging DataFrames
**Status:** ✅ complete

## Level 3 — Statistics
**File:** `level3_statistics.ipynb`
**Dataset:** Rainfall vs. maize yield (synthetic, modeled on real regional patterns)
**Skills:** correlation, distributions, hypothesis testing (t-test), confidence intervals, sample size/statistical power, Simpson's paradox
**Status:** ✅ complete

## Level 4 — Data Cleaning & Feature Engineering
**File:** `level4_cleaning.ipynb`
**Dataset:** Messy insurance claims data (synthetic, MIA-style — missing values, inconsistent formatting, outliers, duplicates)
**Skills:** diagnosing before cleaning, per-column missing-value judgment, standardizing text, mixed date parsing, duplicate handling, IQR outlier detection, feature engineering
**Status:** ✅ complete

## Level 5 — Basic Machine Learning
**File:** `level5_ml_intro.ipynb`
**Dataset:** Insurance claim review flag (synthetic, classification task)
**Skills:** one-hot encoding, train/test split, logistic regression, accuracy/precision/recall/confusion matrix, feature importance via coefficients, spotting data leakage
**Status:** ✅ complete

## Level 6 — Capstone
**File:** `level6_capstone.ipynb`
**Dataset:** Population (real) + maize production (illustrative) + insurance penetration (illustrative), merged
**Skills:** multi-dataset merging, dashboard-style multi-panel figures, regression on small samples (and knowing when NOT to train/test split), writing an analytical narrative with explicit limitations
**Status:** ✅ complete

---

### Roadmap complete
All six levels are built. The natural next step is real data — pulling live regional datasets (as the earlier IRS project did with Open-Meteo/FAOSTAT/World Bank/TMA) and applying this same skill sequence to real MIA claims data or a real InsurePro analytics feature.

### Notes
- Real datasets are sourced from Tanzania NBS (nbs.go.tz), with figures cited in each notebook's markdown cells.
- Where real granular data isn't publicly available (e.g. district-level rainfall or region-level insurance stats), datasets are clearly labeled as **synthetic/illustrative**, built to reflect realistic patterns for practice purposes — never presented as authoritative.
- Each notebook is self-contained: rerun top to bottom with `Kernel > Restart & Run All`.
