# RFM Analysis — Customer Retention Scoring

## Overview
RFM (Recency · Frequency · Monetary) analysis on ~1M real retail 
transactions (UCI Online Retail II dataset) to score customers, 
identify churn risk, and generate a prioritized retention action list.

## Business Context
RFM is a standard retention framework in commercial banking and 
card portfolios. This project produces a P1–P5 priority tier output 
directly usable by Field and Phone Sales teams for targeted outreach.

## Techniques
- Data cleaning (cancellations, null IDs, negative quantities)
- RFM metric computation from raw transaction history
- Quantile-based scoring (1–5 per dimension)
- Weighted composite RFM score (R=30%, F=30%, M=40%)
- Segment profiling (Champions, At-Risk, Loyal, Dormant)
- Revenue-at-risk quantification

## Priority Tiers Output
| Tier | Segment | Action |
|---|---|---|
| P1 | At-Risk High Value | Immediate save action |
| P2 | Champions / Loyal | Proactive retention |
| P3 | Potential Loyalists | Upsell / Activate |
| P4 | Needs Attention | Re-engagement |
| P5 | Lost / Dormant | Win-back or remove |

## Tech Stack
Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## Dataset
UCI Online Retail II — https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci
