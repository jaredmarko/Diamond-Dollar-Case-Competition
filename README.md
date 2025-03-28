# Pitch Decay Analysis: Diamond Dollar Case Competition

## Overview

This repository contains the code and analysis for our pitch decay project, presented at the SABR Analytics Conference as part of the Diamond Dollar Case Competition. Titled *"Analyzing Longevity with Pitch Decay: A New Way of Evaluating Pitchers,"* our work explores how a pitch’s effectiveness declines as batters see it repeatedly within a game. We introduce a novel metric—**pitch count (by type) against batter**—to quantify this decay, using Statcast data to uncover actionable insights for pitcher management, prospect evaluation, and in-game decisions.

## Project Structure

- **`DiamondDollarCaseCompetition.ipynb`**: The main Jupyter Notebook containing the full analysis, including data loading, cleaning, metric calculations, and visualizations.
- **`data/`** *(optional)*: A folder containing CSV files with Statcast data used in the analysis (e.g., pitch-level metrics). *Note*: If CSV files are not included due to size constraints, they can be sourced from the `pybaseball` library as shown in the notebook.

## Key Findings

- **Pitch Decay is Evident**: Low-RPM (1500-1950) four-seam fastballs decay fastest, impacting pitcher efficiency.
- **Spin Rate Matters**: High-RPM fastballs (2400-3000 RPM) resist decay better, as shown in our wOBA decay analysis.
- **Case Study - Joey Estes**: Estes’ slider remains consistent with repeated exposure, while his fastball shows high variance, highlighting his potential as a reliever or secondary-pitch specialist.
- **Applications**: Teams can use decay data to optimize pitching rotations, evaluate prospects (e.g., Mark Appel’s low-spin fastball), and make data-driven in-game decisions (e.g., Blake Snell’s 2020 World Series pull).

## Visualizations

The notebook includes several visualizations to illustrate pitch decay:

- **Heatmaps**: Show batter adjustments (whiff rate, wOBA, launch angle) as pitch counts increase.
- **Line Graphs**: Display wOBA decay by pitch type (e.g., Joey Estes) and spin rate group (four-seam fastballs).
- **Box Plots**: Highlight wOBA distribution by pitch type, revealing consistency and variance.

## Setup and Installation

### Prerequisites

- Python 3.7+
- Google Colab (recommended) or a local Jupyter Notebook environment
- Git (for cloning the repository)

### Dependencies

Install the required Python libraries using `pip`:

```bash
pip install pybaseball pandas numpy matplotlib seaborn plotly