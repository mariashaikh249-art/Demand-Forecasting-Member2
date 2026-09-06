# Demand Forecasting Tool for a Nonprofit Organization — Member 2 (Matplotlib/Seaborn)

**SDC Internship — Group 17**
**Role:** Member 2 — Individual Contributor
**Tool used:** Python (pandas, Matplotlib, Seaborn) in Jupyter Notebook
**Group Lead:** Areeba Rasool (dataset shared from her repo)

## Project
This is my individual piece of the group's "Demand Forecasting Tool for a Nonprofit Organization" project. The group is analyzing the **Blood Transfusion Service Center dataset** (UCI ML Repository) to help a nonprofit predict which past blood donors are likely to donate again.

## Mini-Plan
My piece focuses on visually exploring donor behavior patterns using Matplotlib/Seaborn — specifically how recency, frequency, and monetary value of past donations relate to whether a donor returns to donate again. I documented the dataset, built 3 labeled charts, and turned the patterns into one clear, actionable recommendation for the nonprofit's next donation drive.

**Data consistency note:** This notebook uses the full `transfusion.csv` exactly as shared by the Group Lead (no rows removed), so the numbers below match the rest of Group 17's analysis.

## Files
| File | Description |
|---|---|
| `Demand_Forecasting_Member2_Maria.ipynb` | Full reproducible notebook: EDA, 3 charts, recommendation |
| `transfusion.csv` | Dataset (shared by Group Lead, used unmodified) |
| `chart1_correlation_heatmap.png` | Correlation between Recency, Frequency, Monetary, Time, and Class |
| `chart2_recency_boxplot.png` | Recency distribution: donors vs non-donors |
| `chart3_return_rate_by_recency.png` | Return rate: recent (0-6mo) vs lapsed (7+mo) donors |

## Key Insight
Recency (how recently someone last donated) is the strongest signal for whether they'll donate again — stronger than their total donation history. Recent donors (0-6 months) return at 37.3%, versus 10.8% for lapsed donors. 87% of one-time donors never return.

## Observations
- Recency has a noticeably stronger relationship with repeat donation than Frequency or Monetary — knowing *when* someone last gave matters more than *how many times* they've given.
- Frequency and Monetary are perfectly correlated (1.00) since Monetary is just Frequency × a fixed donation volume — so for modeling purposes, one of these two columns is redundant.
- The overall repeat-donation rate is low (~24%), meaning most donors in this dataset only give once or twice — donor retention is a bigger opportunity than donor acquisition here.
- The recent-vs-lapsed gap (37.3% vs 10.8%) is over 3x, which is a strong enough signal that a nonprofit could realistically use "months since last donation" alone as a simple targeting rule, without needing a complex model.

<!-- Add your observations below -->


## Recommendation
Target outreach at donors active in the last 0-6 months with active reminders (call/SMS/email), since they convert at ~37% vs ~11% for lapsed donors. Build a dedicated "second-donation" follow-up aimed at first-time donors shortly after their first visit, since 87% of one-time donors never come back.

## How to Reproduce
1. Open `Demand_Forecasting_Member2_Maria.ipynb` in Jupyter.
2. Run all cells top to bottom.
3. This regenerates all three PNG charts directly from `transfusion.csv`.

## AI Assistance Disclosure
Used Claude to help structure the analysis and cleanup code as permitted by the internship's AI-assistance policy; I reviewed the logic and results before submitting.
