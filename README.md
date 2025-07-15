# GDB & CPI Transparency Dashboard

This project explores the relationship between **Political Integrity** and **Corruption Perceptions Index (CPI)** scores, drawing data from the [Global Data Barometer 2024](https://globaldatabarometer.org/) and [Transparency International's CPI 2024](https://www.transparency.org/en/cpi/2024).

Our goal is to visualize how transparent governance frameworks (particularly in political finance and lobbying) correlate with public perceptions of corruption — and to highlight a striking gap in lobbying transparency globally.

---

## Why Compare Political Integrity and CPI?

Political integrity — especially transparent regulation of political finance and lobbying — is critical in reducing corruption. Countries that regulate political money tend to foster trust in institutions and better accountability.

We hypothesized that:
- **Higher integrity scores** (from GDB data) would **correlate with higher CPI scores** (indicating lower corruption).
- **Missing data**, especially around lobbying, may itself indicate **opaque systems**.

This dashboard helps us test and visually communicate these insights.

---

## Data Preparation

We used two datasets:
- `gdb-2024-full-data.csv` (Global Data Barometer – Political Integrity)
- `cpi-2024.csv` (Corruption Perceptions Index)

### Data Cleaning and Processing:
- Cleaned both datasets in Excel, removed incomplete or irrelevant entries.
- Renamed inconsistent columns, matched country names, and aligned formats.
- Used a **pivot table** to aggregate Political Finance and Lobbying scores by country.
- Merged CPI scores using `VLOOKUP`, producing the final dataset: `merged-gdb-cpi.csv`.

---

## Tech Stack

| Tool       | Purpose                          |
|------------|----------------------------------|
| React      | Frontend app framework           |
| Recharts   | Data visualizations (charts)     |
| Tailwind CSS | Responsive styling             |
| PapaParse  | CSV parsing in-browser           |

---

## Key Features

- **Interactive Region Filter** — Toggle between Africa, Latin America & Caribbean, or view all.
- **Bar Chart** — Compare Political Finance and Lobbying scores by country.
- **Scatter Plot** — Visualize correlation between Political Integrity and CPI scores.
- **Top 10 Countries by CPI** — See which countries lead in low perceived corruption.
- **Data Gap Summary** — Emphasizes missing lobbying data as a key insight.

---

## Interesting Insights

- **Only 4 countries** (Brazil, Chile, Colombia, Mexico) have Lobbying transparency scores — 33 of 37 are missing.
- **Uruguay** stands out with the **highest CPI score (76)** and a **strong Political Finance score (67.31)** — yet no Lobbying data. Even high performers may lack complete transparency.
- **Missing data is not failure** — it highlights real gaps in governance and reporting.

---

## What We Learned

- Data sparsity can be a **story in itself** — not a limitation, but a message.
- Simple, well-framed comparisons can uncover **governance blind spots**.
- Merging and cleaning open datasets is crucial to meaningful analysis.


