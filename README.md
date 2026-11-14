# StreamFlix Content Analytics

End-to-end data analysis of StreamFlix, a streaming platform, using six linked tables (15,000 subscribers, 9,000 titles, 650,000 viewing sessions, 130,000 ratings, 110,000 reviews and 65,000 watchlist entries). The project covers Python data cleaning, exploratory analysis and KPIs, a 5-page Power BI dashboard and a management report for the CEO.

## What was done

- **Data cleaning (Python, pandas):** profiled all six tables, standardised dates, removed 432 repeated entries (200 ratings, 171 reviews, 61 watchlist) and added flags for records that don't fit the subscription timeline, such as 131,199 viewing sessions dated after the subscriber left.
- **Exploratory analysis (matplotlib):** 10 charts covering monthly viewing, watch hours by year, genres, movies vs TV shows, origin countries, subscriber plans, devices, age, completion by genre and review sentiment.
- **KPIs:** 10 KPIs checked against the targets, including watch hours, active and churn rates, completion, monthly revenue, ARPU, watchlist conversion, hit concentration and the Originals share of hours, plus a cohort retention analysis.
- **Dashboard (Power BI + DAX):** 5 pages (Engagement Overview, Content Performance, Subscriber Insights, Experience, Catalogue and Investment) with slicers, a map and key insights.
- **Management report:** a plain-language summary for the CEO with findings, risks, opportunities and recommendations.

## Key findings

- Viewing is growing fast: January to May 2026 gave about 2.2 million of the 3.33 million total watch hours.
- 74.7% of subscribers are active and 25.3% have left, so the four KPIs with targets are all met.
- Newer subscribers are less loyal: 12-month retention fell from about 96% for the 2016 to 2018 signups to 80.4% for 2025, and the Basic with Ads plan loses 34.3% of its subscribers.

## Data notes

- About 20% of watch hours are dated after the subscriber's recorded leaving date. These rows were flagged, not deleted, and key results were checked with and without them.
- Ratings, reviews and the watchlist's "watched" marker mostly cannot be matched to actual viewing, so they were not used to explain viewing behaviour.
- The raw data files are not included in this repository.

## Tools

Python · pandas · matplotlib · seaborn · Jupyter · Power BI · DAX

## Files

- `notebooks/` – Phase 1 (cleaning), Phase 2 (EDA), Phase 3 (KPIs)
- `charts/` – exported charts (PNG)
- `dashboard/` – Power BI file (.pbix)
- `report/` – management report
