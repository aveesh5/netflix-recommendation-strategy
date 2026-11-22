# Netflix Recommendation Strategy (Challenge 4)

**Author:** Aveesh Ashok Shetty (solo project)
**GitHub repository:** `https://github.com/<your-username>/netflix-recommendation-strategy`  ← replace with your real link

## Business question
*How could Netflix recommend content based on viewer preferences?*

## What this project does
Analyses three small Netflix datasets (10 users, 10 movies, 10 watch-history sessions), cleans and validates them, explores viewing behaviour with 11 visualisations, and designs/evaluates an explainable **hybrid content-based recommender** (content similarity + IMDb quality + engagement popularity + exploration bonus + maturity filter, with a cold-start path for new members).

## Repository structure
```
data/        users.csv · movies.csv · watch_history.csv
notebooks/   netflix_recommendation_analysis.ipynb (+ .html and .pdf exports)
docs/        Netflix_Project_Plan_Agile.docx  (project plan, Kanban, sprint goal, risks, retrospective)
images/      screenshots of the executed notebook
requirements.txt
```

## How to run
```bash
pip install -r requirements.txt
jupyter notebook notebooks/netflix_recommendation_analysis.ipynb   # Kernel -> Restart & Run All
```
All 37 code cells run top to bottom without errors or warnings; the last cell prints 10/10 checks passed.

## Key results
- 12/12 data-validation rules pass; 20 % missing ratings handled with an implicit rating from completion.
- 60 % of sessions completed; mobile sessions have the lowest completion (80 %).
- Hybrid recommender: hit@3 70 % vs 42 % random and 40 % popularity; catalogue coverage 90 % vs 60 %; 0 maturity violations.
- 7 business insights and a KPI table are in notebook section 9.

## Note on the data
The users are fictional and the data is a small illustrative sample created for this assignment (real Netflix Original titles with approximate public metadata). Results demonstrate a method, not real Netflix performance.

## Version control
```bash
git init && git add . && git commit -m "Add datasets, notebook and project plan"
git branch -M main
git remote add origin https://github.com/<your-username>/netflix-recommendation-strategy.git
git push -u origin main
```
