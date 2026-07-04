# 🎮 Dota 2 Pro Match Analysis — PGL Wallachia Season 8

> An Excel-based data analysis project built on professional Dota 2 match data from **PGL Wallachia Season 8** (April 2026), analyzing hero performance, team win rates, and player impact across **2,378 competitive matches** on **Patch 7.41b**.

---

## 📋 Project Overview

This project demonstrates end-to-end data analysis using Microsoft Excel — from raw data cleaning and transformation to an interactive dark-themed dashboard. The dataset covers professional matches from PGL Wallachia Season 8, held April 16–26, 2026 in Bucharest, Romania, with a $1,000,000 prize pool.

---

## 🎯 Objectives

- **Hero Analysis** — Identify pick rates, ban rates, win rates, and assign weighted tier rankings (S to D) per hero
- **Hero Performance by Lane** — Analyze how heroes perform in each role (Carry, Mid, Off Lane, Soft Support, Hard Support, Roam)
- **Best Heroes per Role** — Surface the top 6 performing heroes in each lane based on win rate
- **Team Analysis** — Rank the top 10 best performing teams by win rate among qualified teams (10+ matches)
- **Player Analysis** — Break down player performance by main hero, primary lane, win rate, average GPM and XPM
- **Best Players per Role** — Identify the top performing players in each lane

---

## 📁 File Structure

> ⚠️ Raw data files are too large for GitHub. All files are available on Google Drive below.

[![Google Drive](https://img.shields.io/badge/Google%20Drive-All%20Files-4285F4?style=flat&logo=google-drive&logoColor=white)](https://drive.google.com/drive/folders/1wBkc07BtBRZqAgqDJnm6KoxH-4na91RA?usp=sharing)

**Uploaded to GitHub (analysis files):**

| File | Description |
|---|---|
| `dota2_dashboard.xlsx` | Main interactive dashboard with dark theme and pivot charts |
| `hero_summary.xlsx` | Hero tier list with pick rate, ban rate, win rate, and weighted score |
| `team_analysis.xlsx` | Team win rates and player performance summary |
| `hero_reference.xlsx` | Hero ID to hero name lookup table (sourced from OpenDota API) |

**Available on Google Drive (raw data files):**

| File | Description |
|---|---|
| `players.xlsx` | Player data (24,930 rows) — cleaned and transformed |
| `picks_bans.xlsx` | Draft data — 59,530 pick and ban actions across all matches |
| `main_metadata.xlsx` | Match-level data — 2,378 cleaned matches |
| `teams.xlsx` | Team information linked to match results |

---

## 📊 Dashboard Sections

### 1. Hero Performance
- **Most Picked Heroes** — Top 10 heroes by pick count with lane slicer filter
- **Most Banned Heroes** — Top 10 heroes by ban count
- **Best Performing Heroes by Role** — Top 6 heroes per lane ranked by win rate with tier badges (S/A/B/C/D)
- **Hero Tier List** — Weighted scoring system combining win rate (50%), pick rate (25%), and ban rate (25%)

### 2. Team Performance
- **Best Performing Teams** — Top 10 qualified teams by win rate (minimum 10 matches)

### 3. Player Performance
- **Best Performing Players by Role** — Top 6 players per lane showing main hero, win rate, average GPM, and average XPM

---

## 🛠️ Excel Functions Used

| Function | Purpose |
|---|---|
| `XLOOKUP` | Cross-file hero name and stat lookups |
| `COUNTIFS` | Pick counts, ban counts, win counts per hero/team/player |
| `AVERAGEIFS` | Average GPM and XPM per player per hero |
| `FILTER` | Dynamic filtering of heroes and players by lane and qualification |
| `UNIQUE` | Extracting unique hero, team, and player lists |
| `SORT / SORTBY` | Sorting results by win rate descending |
| `LARGE + SEQUENCE` | Top N value extraction |
| `IF / IFS` | Tier assignment and role classification |
| `VSTACK / CHOOSE` | Combining multi-column arrays |
| `INDEX / MATCH` | Positional lookups |
| `PivotTables + Slicers` | Interactive dashboard filtering |

---

## 🧹 Data Cleaning Steps

- Removed matches with `<UNKNOWN>` teams (both sides)
- Removed matches with one unknown team side
- Synchronized row counts across linked files (teams, metadata, players)
- Fetched hero name reference from OpenDota API via Power Query
- Rebuilt lane/role classification using GPM rank within match + lane_role field
- Applied minimum games filter (10+ matches) for qualified heroes, teams, and players

---

## 📈 Key Findings

- **2,378** clean pro matches analyzed after data cleaning
- **128** unique heroes tracked across all matches
- **97** qualified teams (10+ matches played)
- **220** professional players identified
- **InterActive Philippines** topped the team win rate rankings at **65%**
- Hero tier list built using weighted scoring: Win Rate (50%) + Pick Rate (25%) + Ban Rate (25%)

---

## 🔗 Connect

**Andreij Lacson**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Andreij%20Lacson-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/andreij-lacson-464654307)
[![GitHub](https://img.shields.io/badge/GitHub-Dreygggg-181717?style=flat&logo=github&logoColor=white)](https://github.com/Dreygggg)

---

*Data sourced from OpenDota. Tournament: PGL Wallachia Season 8 — April 2026. Patch 7.41b.*
