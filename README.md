# ML-Based Fair Team Matchmaking

A machine learning system that splits players into two balanced teams so that every match is as fair as possible.

## Overview

Unbalanced teams ruin matches. This project groups players by skill and predicts win probability, then picks the 4v4 split that is closest to a 50/50 outcome.

## How It Works

1. **Data**: A synthetic dataset of 100 players with skill-related attributes (`Players.xlsx`).
2. **Skill clustering**: K-Means groups players into 6 skill clusters.
3. **Win-probability model**: Logistic Regression predicts the chance that one team beats the other.
4. **Team selection**: All possible 4v4 splits of a player pool are evaluated exhaustively, and the split with win probability closest to 50% is chosen.

## Repository Contents

| File | Description |
|------|-------------|
| `MATCHMAKING.ipynb` | Main notebook: data prep, clustering, model training, team splitting |
| `Players.xlsx` | Synthetic player dataset (100 players) |
| `ML_Matchmaking_Report.docx` | Formal project report |

## Tech Stack

Python, Pandas, NumPy, scikit-learn (K-Means, Logistic Regression), Jupyter Notebook

## Getting Started

```bash
git clone https://github.com/hanicode2025/ML-based-fair-matchmaking.git
cd ML-based-fair-matchmaking
pip install pandas numpy scikit-learn openpyxl jupyter
jupyter notebook MATCHMAKING.ipynb
```

Run all cells in order. Keep `Players.xlsx` in the same folder as the notebook.

## Author

Tadepalli Haneesh, B.Tech ECE (IoT), SR Gudlavalleru Engineering College
