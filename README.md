# 📊 Website Performance Analysis

A Python-based data analytics project that explores website traffic data (sessions, users, channels, and engagement metrics) to uncover patterns in visitor behavior and channel performance.

## 📌 Project Overview

This project analyzes website performance data to answer key questions such as:
- How do sessions and users trend over time?
- Which acquisition channels bring the most traffic?
- Which channels drive the most engaged/quality visitors?
- When (which hours of the day) does the website get the most traffic?
- Is engagement rate stable or volatile compared to traffic volume?

## 🛠️ Tech Stack / Libraries

- **Python**
- **Pandas** – data cleaning, aggregation, groupby operations
- **NumPy** – numerical computation (mean estimators, etc.)
- **Matplotlib** – line charts, bar charts, titles/labels
- **Seaborn** – bar plots, boxen plots, heatmaps
- **Jupyter Notebook (VS Code)** – `website performance analysis.ipynb`

## 📂 Dataset

The dataset contains hourly/date-level website traffic records with fields such as:

| Column | Description |
|---|---|
| `DateHour` | Timestamp of the traffic record |
| `Sessions` | Number of sessions |
| `Users` | Number of unique users |
| `channel group` | Traffic source (Direct, Organic Social, Organic Search, Referral, Organic Video, Email, Unassigned) |
| `Average engagement time per session` | Avg. time spent per session |
| `Engagement rate` | Ratio of engaged sessions to total sessions |
| `Engaged Session` / `Non-Engaged` | Session-level engagement split |

Data spans roughly **April 5, 2024 – May 5, 2024**.

## 📈 Analysis Performed

1. **Sessions & Users Over Time** — Line chart tracking hourly sessions/users across the full date range.
2. **Total Users by Channel** — Bar chart comparing user volume across acquisition channels.
3. **Average Engagement Time by Channel** — Bar chart of average time-on-site per channel.
4. **Engagement Rate Distribution by Channel** — Boxen plot showing spread/variance of engagement rate per channel.
5. **Engaged vs Non-Engaged Sessions by Channel** — Grouped bar chart comparing engaged vs non-engaged session counts.
6. **Traffic by Hour & Channel** — Heatmap of session volume across hours of day and channel.
7. **Engagement Rate vs Sessions Over Time** — Dual line chart comparing traffic volume trend against engagement rate trend.

## 🔍 Key Insights

- **Strong daily seasonality:** Sessions and Users follow a clear repeating daily wave — traffic rises sharply during the day and drops to near-zero overnight, confirming human browsing patterns rather than random/bot traffic.
- **Organic Social is the #1 traffic driver:** It brings in the highest total users (~48K), well ahead of Direct (~30K), Organic Search (~28K), and Referral (~27K). Email and Organic Video contribute negligible volume.
- **Volume ≠ Engagement:** Despite having the lowest traffic volume, **Organic Video (~185s) and Email (~130s)** users spend far more time engaging per session than high-volume channels like Direct, Organic Social, and Organic Search (~45–55s) — small but highly invested audiences.
- **Referral traffic converts best:** Referral shows the **highest median engagement rate (~0.65)** and the best engaged-vs-non-engaged session ratio (roughly 2:1), suggesting referral visitors are the most "qualified" traffic.
- **Direct traffic is lower quality:** Direct has more non-engaged sessions than engaged ones — high volume but relatively weaker quality compared to Referral or Organic Search.
- **Organic Social has scale AND decent engagement:** It leads in both total sessions and engaged session count (~32K engaged), making it the single most valuable channel overall despite a mid-range engagement rate.
- **Peak traffic hours are midday–evening:** The hourly heatmap shows Organic Search and Direct traffic peaking between roughly 11 AM–8 PM, while overnight hours (2 AM–6 AM) see the lowest activity across all channels.
- **Engagement rate is stable regardless of traffic spikes:** While session volume swings heavily day to day (20 to 100+ sessions), the engagement rate line stays flat/consistent — meaning visitor quality doesn't degrade even when traffic surges.

## 🚀 How to Run

1. Clone/download this repository.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Open `website performance analysis.ipynb` in Jupyter Notebook / VS Code.
4. Run all cells to reproduce the charts and insights.

## 📁 Project Structure

```
WebsitePerformanceAnalysis/
│
├── README.md                             # Project documentation
├── data/                                 # Raw dataset (CSV)
└── website performance analysis.ipynb   # Main analysis notebook
```


## ✅ Conclusion

This analysis highlights that **channel quality matters as much as channel volume**. While Organic Social drives the most traffic, Referral traffic converts best, and low-volume channels like Organic Video and Email produce disproportionately engaged visitors. These insights can help prioritize marketing spend toward channels that balance both reach and engagement.
