# NorthStar Urban Mobility and Logistics
## Databases and Analytics Assignment — University of West London

This repository contains the full analytical solution for the NorthStar Urban Mobility 
and Logistics case study, completed as part of the Databases and Analytics module.

---

## Project Overview

NorthStar is a large regional organisation operating across several major UK cities,
managing public shuttle services, last-mile delivery, warehouse dispatch operations,
and electric vehicle charging hubs. This project analyses the organisation's fragmented
data environment and proposes an integrated database and analytics solution.

---

## Repository Structure

| Notebook | Description |
|---|---|
| `Section1_SQL_in_R.ipynb` | SQL queries written and executed within R using sqldf |
| `Section2_R_Analytics.ipynb` | Statistical analysis and data visualisation using R and ggplot2 |
| `Section3_Python_Processing.ipynb` | Data cleaning, feature engineering and visualisation using Python |
| `Section4_MongoDB.ipynb` | NoSQL database design and CRUD operations using MongoDB Atlas |
| `Section5_Query_Optimisation.ipynb` | Indexing strategies and query performance tuning in MongoDB |

---

## Dataset

The `north_dataset` folder contains 9 CSV files used across all sections:

| File | Records | Description |
|---|---|---|
| `orders.csv` | 1250 | Service orders across mobility and logistics operations |
| `deliveries.csv` | 950 | Operational dispatch and completion outcomes |
| `customers.csv` | 650 | Customer master data with engagement and loyalty metrics |
| `drivers.csv` | 170 | Driver workforce data with training and rating information |
| `vehicles.csv` | 120 | Fleet asset data including battery and maintenance indicators |
| `incidents.csv` | 280 | Delivery and asset incident records |
| `complaints.csv` | 320 | Customer complaints and compensation handling |
| `app_events.csv` | 640 | Digital platform events modelled into MongoDB |
| `hubs.csv` | 8 | Operational hubs and control points |

---

## Technologies Used

- **R** — sqldf, ggplot2, dplyr
- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **MongoDB Atlas** — PyMongo, CRUD operations, Aggregation Pipelines
- **Google Colab** — Development and execution environment
- **GitHub** — Version control and submission

---

## Key Findings

- Certain city zones consistently show higher delivery failure rates than others
- Driver training score has a positive correlation with customer ratings
- App sessions with high API latency are directly linked to failed events and complaints
- MongoDB document design allows integrated customer, order and complaint records
  to be retrieved in a single query rather than across multiple joined tables
- Indexing key fields reduced query execution time significantly across all collections

---

## MongoDB Collections

Three collections were designed and implemented in MongoDB Atlas:

| Collection | Documents | Description |
|---|---|---|
| `customer_profiles` | 650 | Customer records with nested orders and complaints |
| `app_sessions` | 637 | App events grouped by session with latency metrics |
| `delivery_cases` | 950 | Delivery records with nested driver info and incidents |

---

## How to Run

1. Open any notebook in Google Colab
2. Upload the `north_dataset` CSV files to `/content/northstar-analytics/north_dataset/`
3. For Sections 4 and 5 replace the MongoDB connection string with your own Atlas URI
4. Run each cell in order from top to bottom
