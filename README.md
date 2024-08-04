# [GCP Project to Monitor and Manage Personal Stock Portfolio](https://github.com/junjiechoo24/financial-portfolio-monitor)

<img src="https://github.com/junjiechoo24/finance_portfolio/blob/main/d4d61301-6e63-4bf7-8466-1815cdde8d67.jpg" alt="Financial Portfolio Management" width="600"/>

## Project Overview

The primary goals of this project are to:
1. Collect my portfolio data from Moomoo and monitor its performance over time to compare it against the S&P 500 benchmark.
2. Manage and track my sector weightings to rebalance based on market outlook.
3. Prevent individual holdings from being overweighted.
4. Track dividend collections.

This project is a daily batch job that integrates data from multiple sources and is deployed on Google Cloud Platform (GCP) using Google Cloud Functions and Google Cloud Scheduler. 

The process begins with collecting my portfolio from Moomoo via its API. This data is then enriched with historical dividend information and sector details sourced from Yahoo Finance API. Since I have stocks from multiple markets, currency conversion is necessary to maintain consistent financial metrics such as total dividends gained, so the currencies are converted into SGD for consistency using real-time foreign exchange rates fetched from a third-party API. 

### Data Sources

- **Portfolio Data**: Collected and processed from Moomoo API.
- **FX Rates**: Fetched daily from a third-party API.
- **Sector and Dividend Data**: Integrated from Yahoo Finance API.

### Tools Used

- **Google Cloud Scheduler**: Schedules tasks to trigger data collection and processing at specified intervals.
- **Google Cloud Functions**: Executes data integration, processing, and analysis tasks as triggered by Cloud Scheduler.
- **Google BigQuery**: Stores processed portfolio and dividend data for structured analysis and reporting.

*Note: Due to the code containing sensitive information, it will not be included. However, I hope this summary is able to illustrate the idea.*

### Skills: Python, GCP (Google Cloud Function, Cloud Scheduler, BigQuery), API integrations
