# Diamond Dollar Case Competition: Relief Pitcher Valuation

## Overview

This repository contains the code and analysis for our Diamond Dollar Case Competition submission, presented at the SABR Analytics Conference. Our project focuses on evaluating MLB relief pitchers by developing two novel metrics: **Save Score** and **Reliever Impact Score (RIS)**. Using Statcast, FanGraphs, and Baseball-Reference data from 2023-2024, we quantify reliever effectiveness beyond traditional saves, incorporating context-adjusted factors like inherited runners, hitter quality, and leverage. Our analysis identifies under- and over-appreciated closers, ranks top relievers, and provides actionable insights for teams to optimize bullpen management.

### Authors
- David Baitt
- Owen Lefkowicz
- William Haray
- Jared Markowitz
- Andrew Fossi

## Project Structure

- **`DiamondDollarCaseCompetition.ipynb`**: The main Jupyter Notebook containing the full analysis, including data collection, cleaning, metric computation, ranking, and visualizations.
- **`data/`** (optional): A folder containing CSV files (`bref_2023.csv`, `bref_2024.csv`) with Baseball-Reference relief pitching data. *Note*: These files are required to run the notebook unless sourced directly.
- **Output Visuals**:
  - `misvaluation_plot.png`: Scatter plot of Saves vs. Save Score, colored by RIS.
  - `radar_chart.png`: Radar chart of the top reliever’s performance profile.
  - `ris_save_score_distributions.png`: Histograms of RIS and Save Score distributions.
  - `saves_vs_save_score.png`: Scatter plot of Saves vs. Save Score with RIS as hue/size.
  - `ris_save_score_boxplot.png`: Box plots of RIS and Save Score by year.
  - `bubble_ris_vs_save_score.png`: Bubble plot of RIS vs. Save Score, with bubble size as Saves.

## Key Findings

- **Save Score and RIS Metrics**:
  - Save Score adjusts traditional saves for context (e.g., inherited runners, hitter quality, leverage), with a mean of 0.26 and standard deviation of 4.21.
  - RIS combines skill metrics (SIERA, K%, BB%, leverage, xwOBA) to measure overall impact, with a mean of 43.72 and standard deviation of 13.67.
- **Top Performers**:
  - 2023: Devin Williams led relievers with an RIS of 79.19; Tanner Scott topped closers with a Save Score of 6.58.
  - 2024: Mason Miller led relievers with an RIS of 91.20; Tanner Scott again led closers with a Save Score of 3.13.
- **Misvaluation**:
  - Under-Appreciated Closers: Tanner Scott (2023, 2024) and Griffin Jax (2024) excelled in Save Score despite fewer save opportunities.
  - Over-Appreciated Closers: Emmanuel Clase (2023) and Clay Holmes (2024) had high saves but lower Save Scores, indicating over-reliance on traditional metrics.
- **Validation**:
  - RIS correlates strongly with WPA (0.569, p<0.0001), outperforming saves (0.516, p<0.0001).
  - Predictive power (2023 to 2024): RIS shows a moderate correlation with future WPA (0.383, p=0.0589), while Save Score and saves have weaker predictive ability.

## Visualizations

The notebook generates several visualizations to illustrate reliever valuation:
- **Scatter Plots**: Compare Saves vs. Save Score, with RIS as hue/size, highlighting misvaluation (e.g., Emmanuel Clase vs. Tanner Scott).
- **Histograms**: Show distributions of RIS and Save Score, with means marked.
- **Box Plots**: Display RIS and Save Score distributions by year (2023-2024).
- **Bubble Plot**: Visualize RIS vs. Save Score, with bubble size representing saves.
- **Radar Chart**: Profiles the top reliever’s performance across key metrics (SIERA, WPA, K%, RIS).

## Setup and Installation

### Prerequisites
- Python 3.7+
- Google Colab (recommended) or a local Jupyter Notebook environment
- Git (for cloning the repository)

### Dependencies
Install the required Python libraries using `pip`:
```bash
pip install pybaseball pandas numpy matplotlib seaborn scikit-learn fuzzywuzzy python-Levenshtein scipy
