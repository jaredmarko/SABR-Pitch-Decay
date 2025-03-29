# SABR-Pitch-Decay

## Overview

This repository contains the code and analysis for our pitch decay project, presented at the SABR Analytics Conference. Titled *"Analyzing Longevity with Pitch Decay: A New Way of Evaluating Pitchers,"* our work investigates how a pitch’s effectiveness diminishes as batters see it repeatedly within a game. We introduce a novel metric—**pitch count (by type) against batter**—to quantify this decay, leveraging Statcast data to provide actionable insights for pitcher management, prospect evaluation, and in-game decision-making.

## Project Structure

- **`SABR_Pitch_Decay.ipynb`**: The main Jupyter Notebook containing the full analysis, including data loading, cleaning, metric calculations, and visualizations.
  
## Key Findings

- **Pitch Decay is Evident**: Low-RPM (1500-1950) four-seam fastballs exhibit significant decay, reducing pitcher efficiency.
- **Spin Rate Impacts Decay**: High-RPM fastballs (2400-3000 RPM) show greater resistance to decay, as evidenced by lower wOBA increases.
- **Case Study - Joey Estes**: Estes’ slider remains consistent with repeated exposure, while his fastball shows high variance, suggesting a potential role as a reliever or secondary-pitch specialist.
- **Applications**: Pitch decay data can optimize pitching rotations, inform prospect evaluation (e.g., Mark Appel’s low-spin fastball), and guide in-game decisions (e.g., Blake Snell’s 2020 World Series pull).

## Visualizations

The notebook includes several visualizations to illustrate pitch decay:
- **Heatmaps**: Display batter adjustments (whiff rate, wOBA, launch angle) as pitch counts increase, highlighting decay patterns.
- **Line Graphs**: Show wOBA decay by pitch type (e.g., Joey Estes) and spin rate group (four-seam fastballs), emphasizing spin rate’s role.
- **Box Plots**: Reveal wOBA distribution by pitch type, showcasing consistency and variance (e.g., Estes’ slider vs. fastball).

## Setup and Installation

### Prerequisites
- Python 3.7+
- Google Colab (recommended) or a local Jupyter Notebook environment
- Git (for cloning the repository)

### Dependencies
Install the required Python libraries using `pip`:
```bash
pip install pybaseball pandas numpy matplotlib seaborn plotly
