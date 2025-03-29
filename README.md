# SABR Pitch Decay Research (2024)

## Overview
As part of a research initiative for the Society for American Baseball Research (SABR), I developed an analytical pipeline to explore the phenomenon of **pitch decay**—the measurable changes in pitch quality (velocity, movement, spin) as a function of pitcher fatigue, pitch count, or game progression.

## Data Pipeline
- Utilized the `pybaseball` library to pull **Statcast** data from the 2024 MLB season.
- Queried pitch-level data spanning from **April 1 to October 1, 2024**.
- Processed and cleaned data using `pandas`, accounting for time-based inconsistencies and format warnings.

## Methodology
- Parsed `statcast` pitch data and grouped pitches by:
  - **Pitcher**
  - **Pitch type**
  - **Game date**
  - **Inning and pitch count**
- Tracked key pitch metrics over time:
  - `release_speed`
  - `release_spin_rate`
  - `pfx_x`, `pfx_z` (horizontal and vertical movement)
- Calculated **per-game pitch decay curves** and **cumulative season-long decay trends**.
- Developed **fatigue indicators** by modeling decline in pitch metrics as functions of pitch count, innings pitched, and days rest.

## Key Tools & Libraries
- `pybaseball` – For seamless Statcast data access.
- `pandas`, `numpy` – For cleaning, transformation, and statistical computation.
- `matplotlib`, `seaborn` – For exploratory visualizations and decay curve plotting.

## Preliminary Insights
- Pitchers showed **consistent declines in velocity and spin rate** after ~40 pitches.
- Off-speed pitches decayed at a slower rate than fastballs, suggesting different fatigue thresholds.
- Some pitchers demonstrated **resilience to decay**, potentially tied to pitch mix or conditioning.

## Next Steps
- Integrate player-level biomechanical data (where available).
- Correlate decay patterns with in-game performance (e.g., wOBA allowed, strike rate).
- Package insights into a public-facing dashboard or SABR abstract submission.

## Challenges
- Long query time for full-season Statcast data (~2.5 hours for April–October).
- Future warnings due to deprecated datetime conversion methods in `pybaseball`.

## Impact
This work contributes toward a deeper understanding of **pitcher fatigue modeling**, with applications in:
- In-game decision-making (e.g., pitching changes)
- Workload management
- Injury prevention strategies
