# India Crime Intelligence Dashboard (Tableau)

An interactive Tableau dashboard analysing crime trends across India from 2015 to 2024: state-wise hotspots, crime categories, and the growth of cyber crime and online fraud.

**Live dashboard:** [Tableau Public link here]

<img width="1901" height="1038" alt="Screenshot 2026-10-09 202851" src="https://github.com/user-attachments/assets/c55aa1ff-a57d-4b14-844e-f57d9140e43b" />
<img width="1908" height="1042" alt="Screenshot 2026-10-09 202859" src="https://github.com/user-attachments/assets/82ca016c-b943-4478-b5fb-b4bed77b5fb5" />



## Objective
- Identify which states carry the highest crime volumes and rank them dynamically
- Track the national crime trend over 10 years
- Break cyber crime and fraud into categories and show financial impact (average loss per complaint)
- Let viewers explore by year, state and Top-N ranking without leaving the dashboard

## Data
Four CSV files, combined in Tableau as three linked data sources:

| File | Contents |
|---|---|
| `1_crime_state_year_summary_2015_2024.csv` | State, year, domain, crime head, category, cases |
| `3_cyber_scam_detail_2019_2024.csv` | Cyber scam detail, 2019 to 2024 |
| `6_scam_national_complaints_I4C.csv` | Complaints, amount lost (Rs crore), average loss per complaint |
| `7_fraud_subtypes_2024.csv` | Fraud subtype breakdown (2024 only) |


## What's inside
- **Parameters:** `Select Year` (default 2022) and `Top N` (default 11), driving the dashboard
- **Calculated fields:** `Year Match`, `Total Crime`, `Total Crime Prev`, `YoY %`, `Murder Cases`, `Crime Against Women`, `Cyber Crime`
- **Views:** filled map by state, Top-N state bar chart, crime trend line, crime-head donut, Pareto chart of cyber crime by category, lollipop chart of average loss per complaint, stacked chart, KPI cards
- **Interactivity:** dashboard-wide year and state filters, highlight actions and filter actions

## Key insights
- Cyber crime cases grew from 44,546 (2019) to 101,928 (2024), an increase of about 129%.
- In 2022, Uttar Pradesh reported 793,020 cases, about 33% more than Maharashtra (596,103).

## Known limitations
- The filled map shows blanks for some years because `ipc_sll_total` is not populated for every year in the source file.
- The fraud subtype data covers 2024 only, so it has no year filter.

## Tools
Tableau Desktop, CSV data sources, calculated fields, parameters, dashboard actions

## Repository contents
- `Dashboard.twb`: Tableau workbook
- `data/`: source CSV files
- `images/`: dashboard screenshots
- `India_Crime_Intelligence_Dashboard.pptx`: project walkthrough

## Author
**Sumit Suryavanshi**: [GitHub](https://github.com/sumit1965)
