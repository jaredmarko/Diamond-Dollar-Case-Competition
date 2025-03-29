# Relief Pitcher Valuation: Diamond Dollars 2025

## 🧠 Summary

This project was created for the 2025 SABR Diamond Dollars Case Competition and introduces two custom metrics to evaluate MLB relievers:

- **Save Score**: A context-adjusted performance metric for closers based on leverage, opponent quality, and Win Probability Added (WPA).
- **RIS (Reliever Impact Score)**: A skill-based rating system optimized via regression on underlying indicators like SIERA, strikeout rate, and xwOBA.

---

## 📊 Project Goals

- Identify under- and over-valued closers beyond the traditional "save" stat.
- Integrate advanced metrics from Statcast, FanGraphs, and Baseball-Reference.
- Validate new metrics against actual WPA and test predictive power year-over-year.

---

## 🛠️ Requirements

Install the following packages before running:

- `fuzzywuzzy`
- `python-Levenshtein`
- `pybaseball`
- `scikit-learn`
- `LinearRegression` (custom pip package)
- `pandas`, `numpy`

> Install using `pip install <package-name>`

---

## 📦 Data Sources

- Statcast (via `pybaseball`)
- FanGraphs (relief pitcher stats, 2023–2024)
- Baseball-Reference (custom CSV imports for reliever usage)

---

## 🧹 Workflow Summary

### Step 1: Data Collection

Collected 2023–2024 data using `pybaseball`, custom CSVs, and FanGraphs.

### Step 2: Cleaning & Merging

- Player name harmonization via `fuzzywuzzy`
- Filtered for late-inning relievers (7th inning or later)
- Merged all datasets on `Player` and `Year`

### Step 3: Save Score

A custom stat incorporating:
- WPA per opportunity
- Leverage index
- Opponent quality (wOBA)
- Inherited runners

### Step 4: RIS (Reliever Impact Score)

Optimized with `LinearRegression` using:
- `SIERA` (inverted)
- Inherited Runner Success Rate
- `K%`, `BB%`
- `xwOBA`
- Leverage Index

RIS scaled 0–100.

### Step 5: Pitcher Rankings

Ranked relievers by:
- RIS (overall skill)
- Save Score (context-based performance)
- Misvaluation (Save Score vs. Save Opportunities)

### Step 6: Validation

- **RIS vs. WPA** correlation: 0.57
- **Save Score vs. WPA**: 0.52
- **2023 RIS → 2024 WPA**: 0.38

---

## 🔎 Key Insights

- **Under-Appreciated**: Griffin Jax, Trevor Megill, Tanner Scott (elite Save Scores)
- **Over-Appreciated**: Emmanuel Clase (low Save Score despite high SV total)
- **RIS is more predictive of WPA** than SV or Save Score alone

---

## 👨‍💻 Author

**Jared Markowitz**  
Tulane University  
Presenter at 2025 SABR Analytics Conference  
Connect: [LinkedIn](https://www.linkedin.com/in/jared-markowitz-2563a8b8/)

---

## 🧠 Final Thoughts

By integrating modern metrics and context, this project offers a framework to more accurately value relievers. RIS and Save Score can help front offices and fans alike better understand bullpen impact.
