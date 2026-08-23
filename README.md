# 2008 Formula 1 Championship Analysis

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lilyrgb/formula-1-2008-championship-analysis/blob/main/formula-1-2008-championship-analysis.ipynb)

## Overview

This Google Colab project analyzes driver and constructor performance in the 2008 Formula 1 World Championship. It reads race results from a CSV file, applies the historical scoring system, calculates individual driver statistics, and generates ordered championship standings.

## Project Features

- Upload and parse race-result data directly in Google Colab.
- Apply the 2008 Formula 1 points system.
- Calculate a selected driver's total points, wins, and podium finishes.
- Generate complete driver standings and display the top five.
- Aggregate driver points into constructor standings.
- Export the driver standings to a text file.

## Repository Contents

| File | Description |
| --- | --- |
| `formula-1-2008-championship-analysis.ipynb` | English Google Colab notebook containing the complete analysis workflow. |

## Scoring System

The notebook awards points to the top eight finishers using the 2008 system:

| Position | Points |
| --- | ---: |
| 1st | 10 |
| 2nd | 8 |
| 3rd | 6 |
| 4th | 5 |
| 5th | 4 |
| 6th | 3 |
| 7th | 2 |
| 8th | 1 |

All other finishing positions receive zero points.

## Dataset Requirements

The notebook expects a file named `formula1_data.csv` with one row per driver result in each Grand Prix and these columns:

- `Driver` — driver name
- `Position` — integer finishing position
- `Team` — constructor or team name

The dataset is not included in this repository.

## How to Run

1. Click the **Open in Colab** badge above.
2. Run the notebook cell.
3. Upload `formula1_data.csv` when prompted.
4. Review the selected driver's statistics.
5. Inspect the driver and constructor standings printed by the notebook.
6. Download `drivers_standings_2008.txt` from the Colab file panel if needed.

## Main Functions

- `load_data()` uploads and parses the CSV dataset.
- `calculate_points(position)` applies the 2008 scoring rules.
- `analyze_driver_performance(...)` calculates points, wins, and podiums.
- `generate_driver_standings(...)` ranks drivers and creates a text export.
- `generate_constructor_standings(...)` aggregates points by team.

## Technologies

- Python 3
- Google Colab
- Python standard-library modules: `csv` and `io`
- `google.colab.files` for interactive file upload

## Notes

- The notebook assumes valid integer values in the `Position` column.
- Standings are ordered by total points only; official championship tie-break rules are not implemented.
- The notebook has been cleaned for publication, with code, comments, messages, and documentation written in English.
