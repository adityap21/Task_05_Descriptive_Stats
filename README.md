# Task_05_Descriptive_Stats

## Overview

This project explores how well ChatGPT can answer data analysis questions compared to Python code, using a real NBA player statistics dataset from the 2022–23 season. The main goal is to evaluate the capabilities and limitations of large language models (LLMs) when interpreting tabular, quantitative data.

## Dataset

- Sampled 50 NBA players from the 2022–23 season.
- Each row includes: Player, Team, GP (games played), PTS, REB, AST, STL, BLK, FG%, 3P%, FT%.
- **Note:** The actual CSV dataset is not included in this repository, per assignment requirements.

## Questions Asked

1. **Who scored the most points per game?**
2. **Who is the best all-around player (PTS + REB + AST)?**
3. **Who is the most complete player?** (open-ended)
4. **Who is the best shooter?** (FG%, 3P%, FT%)
5. **How many players averaged at least 25 points per game?**
7. **How many players averaged at least 8 assists per game?**

## Method

For each question:
- The relevant data was pasted into ChatGPT and the question was asked in natural language.
- The same question was answered using a Python script.
- Answers were compared in a documentation table, and mismatches or reasoning errors were noted.

## Example Documentation Table

| Question                                  | Python Answer          | GPT Answer (summary)                                                        | Match? | Notes                                                |
|--------------------------------------------|------------------------|-----------------------------------------------------------------------------|--------|------------------------------------------------------|
| Who scored the most points per game?       | Joel Embiid (33.1)     | Joel Embiid (33.1)                                                           | Yes    | Direct match                                         |
| Who is the best all-around player?         | Luka Doncic (49.0 sum) | Luka Doncic (32.4+8.6+8.0=49.0)                                             | Yes    | Direct match                                         |
| Who is the most complete player?           | Not applicable         | "Giannis and Jokic—depends how 'complete' is defined"                        | N/A    | Open-ended, LLM gave narrative answer                |
| Who is the best shooter?                   | Curry (3P%), Durant (FG%, FT%) | "Depends: Curry for 3P%, Durant for FG%/FT%. Best depends on stat chosen."   | Partial| LLM gave nuanced, not single answer                  |
| # players averaged ≥25 PPG                 | 15                     | 15                                                                          | Yes    | Direct count                                         |
| # players averaged ≥8 AST                  | 5                      | 4                                                                           | No     | GPT missed one; needed clarification for boundary    |

## Key Findings

- ChatGPT gives accurate answers for simple, well-defined stat questions when data is clean.
- For ambiguous or open-ended questions, ChatGPT hedges or narrates, not computes.
- LLMs can miscount or skip values in large tables or on boundaries (e.g., ≥8.0).
- Prompt engineering and human validation are essential.

## Files in this Repo

- `analysis.py` – All Python code for analysis and visualization.
- `README.md` – This file.

## Instructions

1. Clone/download this repository.
2. Open `analysis.py` to view and run the analysis code.
3. See documentation tables for question-by-question results.

---

