# Spotify Listening Analytics — ELT Pipeline

## Overview
An end-to-end ELT pipeline that extracts Spotify listening data via OAuth API,
transforms it through dbt models, and surfaces genre analytics in a Streamlit dashboard.

## Architecture
Spotify API → Airflow (Orchestration) → Raw Data → dbt (Transformation) → PostgreSQL → Streamlit Dashboard

## Tech Stack
- **Orchestration:** Apache Airflow
- **Transformation:** dbt (8 models with automated quality tests)
- **Database:** PostgreSQL
- **Visualization:** Streamlit
- **Language:** Python
- **Auth:** OAuth 2.0 (Spotify API)

## Features
- Automated data extraction from Spotify API using OAuth 2.0
- 8 dbt transformation models with built-in data quality tests
- Genre analytics dashboard built with Streamlit
- Airflow DAGs for scheduling and monitoring pipeline runs

## Setup
1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Configure Spotify API credentials in `.env`
4. Run Airflow: `airflow standalone`
5. Run dashboard: `streamlit run dashboard.py`

## Project Structure
├── dags/          # Airflow DAGs
├── models/        # dbt transformation models
├── dashboard.py   # Streamlit dashboard
├── requirements.txt
└── README.md
