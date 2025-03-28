# Diamond-Dollar-Case-Competition
Pitch Decay Analysis: Diamond Dollar Case Competition
Overview
This repository contains the code and analysis for our pitch decay project, presented at the SABR Analytics Conference as part of the Diamond Dollar Case Competition. Titled "Analyzing Longevity with Pitch Decay: A New Way of Evaluating Pitchers," our work explores how a pitch’s effectiveness declines as batters see it repeatedly within a game. We introduce a novel metric—pitch count (by type) against batter—to quantify this decay, using Statcast data to uncover actionable insights for pitcher management, prospect evaluation, and in-game decisions.
Authors
David Baitt

Owen Lefkowicz

William Haray

Jared Markowitz

Andrew Fossi

Project Structure
DiamondDollarCaseCompetition.ipynb: The main Jupyter Notebook containing the full analysis, including data loading, cleaning, metric calculations, and visualizations.

data/ (optional): A folder containing CSV files with Statcast data used in the analysis (e.g., pitch-level metrics). Note: If CSV files are not included due to size constraints, they can be sourced from the pybaseball library as shown in the notebook.

Key Findings
Pitch Decay is Evident: Low-RPM (1500-1950) four-seam fastballs decay fastest, impacting pitcher efficiency.

Spin Rate Matters: High-RPM fastballs (2400-3000 RPM) resist decay better, as shown in our wOBA decay analysis.

Case Study - Joey Estes: Estes’ slider remains consistent with repeated exposure, while his fastball shows high variance, highlighting his potential as a reliever or secondary-pitch specialist.

Applications: Teams can use decay data to optimize pitching rotations, evaluate prospects (e.g., Mark Appel’s low-spin fastball), and make data-driven in-game decisions (e.g., Blake Snell’s 2020 World Series pull).

Visualizations
The notebook includes several visualizations to illustrate pitch decay:
Heatmaps: Show batter adjustments (whiff rate, wOBA, launch angle) as pitch counts increase.

Line Graphs: Display wOBA decay by pitch type (e.g., Joey Estes) and spin rate group (four-seam fastballs).

Box Plots: Highlight wOBA distribution by pitch type, revealing consistency and variance.

Setup and Installation
Prerequisites
Python 3.7+

Google Colab (recommended) or a local Jupyter Notebook environment

Git (for cloning the repository)

Dependencies
Install the required Python libraries using pip:
bash

pip install pybaseball pandas numpy matplotlib seaborn plotly

Running the Notebook
Clone the Repository:
bash

git clone https://github.com/your-username/pitch-decay-project.git
cd pitch-decay-project

Replace your-username with your GitHub username.

Open in Google Colab:
Upload DiamondDollarCaseCompetition.ipynb to Google Colab:
Go to colab.research.google.com, click File > Upload notebook, and select the .ipynb file.

Alternatively, if the notebook is already on GitHub, open it directly in Colab by clicking the “Open in Colab” badge (if added) or using the GitHub URL.

Install Dependencies in Colab:
Run the following cell at the top of the notebook to install dependencies:
python

!pip install pybaseball pandas numpy matplotlib seaborn plotly

Run the Notebook:
Execute the cells in order to load data, perform analysis, and generate visualizations. The notebook uses pybaseball to fetch Statcast data, so an internet connection is required.

Usage
Data Source: The notebook fetches Statcast data using the pybaseball library for the 2023 MLB season. You can modify the date range in the statcast() function to analyze different seasons.

Custom Data: If you have your own CSV files, place them in the data/ folder and update the notebook to load them instead of fetching from pybaseball.

Visualizations: The notebook generates heatmaps, line graphs, and box plots. Outputs are saved as PNGs (e.g., whiff_rate_heatmap.png) and HTML files (e.g., woba_heatmap.html) for interactive viewing.

Contributing
We welcome contributions! To contribute:
Fork the repository.

Create a new branch (git checkout -b feature/your-feature).

Make your changes and commit (git commit -m "Add your feature").

Push to your fork (git push origin feature/your-feature).

Open a pull request with a description of your changes.

Future Directions
Explore pitch decay for other pitch types (e.g., changeup spin rates, curveball vertical depth).

Investigate pitch sequencing effects on decay.

Analyze batter-specific trends (e.g., power vs. contact hitters).

Integrate biomechanical and psychological factors (e.g., fatigue, high-pressure scenarios).

Acknowledgments
Inspired by Lance Brozdowski’s analysis of the 2024 Skenes-Ohtani matchup.

Builds on prior work by Jim Albert (Times Through The Order Effects) and Jon Roegele (The Effect of Seeing Pitches).

Thanks to the SABR Analytics Conference and the Diamond Dollar Case Competition for the opportunity to present this work.


