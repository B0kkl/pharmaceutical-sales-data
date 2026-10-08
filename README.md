# Analysing Pharmaceutical Sales Data

**Project URL:** https://github.com/B0kkl/pharmaceutical-sales-data

**Project Data Source:** https://roadmap.sh/projects/pharmaceutical-sales-data

Exploratory analysis of daily pharmacy sales (Jan 2014 – Oct 2019) using **Python, Pandas and Matplotlib**.

Dataset: [Pharma Sales Data on Kaggle](https://www.kaggle.com/milanzdravkovic/pharma-sales-data) (`salesdaily.csv`).

## Drug categories (ATC codes)

| Code | Drug group |
|---|---|
| M01AB | Acetic acid derivatives |
| M01AE | Propionic acid derivatives |
| N02BA | Salicylic acid and derivatives |
| N02BE | Anilides (paracetamol) |
| N05B | Anxiolytics |
| N05C | Hypnotics and sedatives |
| R03 | Drugs for obstructive airway diseases |
| R06 | Antihistamines |

## Questions answered

1. What are the total sales quantities for each drug category (ATC code)?
2. Which individual drugs have the highest total sales?
3. Which three drugs have the highest sales in January 2015, July 2016 and September 2017?
4. Which drug sold most often in 2017?
5. Which drug category has the highest average daily sales?
6. Are respiratory drugs (R03) sold more during specific months?

## Key findings

- **N02BE (paracetamol-type) dominates**: about 49% of all units sold and about 30 units per day, roughly 3.4x the next category (N05B).
- N02BE is the top seller in all three sampled months; N05B is second each time.
- In 2017 N02BE, M01AB and M01AE each sold on 360+ of 365 days (a near tie). N05C sold on only 99 days.
- **R03 is seasonal**: average daily sales peak in December (about 7.9) and are lowest in July (about 3.0), roughly 2.7x lower.

## Notes and limitations

- The dataset has no brand names; sales are grouped by ATC code, so each code is treated as one "drug".
- "Sold most often" is interpreted as the number of days with at least one sale.
- Data comes from a single pharmacy and measures units, not revenue. 2019 ends on 8 October, so monthly comparisons use average daily sales.

## How to run

```bash
git clone https://github.com/B0kkl/pharmaceutical-sales-data.git
cd pharmaceutical-sales-data
pip install pandas matplotlib jupyter
jupyter notebook
```

Open the notebook and run the cells from top to bottom. The data must be at `data/salesdaily.csv`.

## Project structure

```
pharmaceutical-sales-data/
├── data/
│   └── salesdaily.csv
├── Analysing-pharmaceutical-sales-data.ipynb
└── README.md
```
