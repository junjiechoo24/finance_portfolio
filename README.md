# [GCP Project to Monitor and Manage Financial Portfolio](https://github.com/junjiechoo24/financial-portfolio-monitor)

![Financial Portfolio Management](https://github.com/junjiechoo24/finance_portfolio/blob/main/d4d61301-6e63-4bf7-8466-1815cdde8d67.jpg)

## Project Overview

The primary goals of this project are to:
1. Monitor portfolio performance over time and compare it against the S&P 500 benchmark.
2. Manage sector weightings based on market outlook.
3. Prevent individual holdings from being overweighted.
4. Track dividend collections.

This project integrates data from multiple sources and is deployed on Google Cloud Platform (GCP) using Google Cloud Functions and Google Cloud Scheduler. The process begins with collecting portfolio data from Moomoo. This data is then enriched with historical dividend information sourced from Yahoo Finance and converted into SGD for consistency using real-time foreign exchange rates fetched from a third-party API. Stock and sector information is retrieved from Google Sheets to calculate sector weightings and other relevant metrics.

### Data Processing

- **Conversion**: All financial metrics are converted to SGD using real-time FX rates for HKD, SGD, USD, and MYR.
- **Integration**: Moomoo portfolio data is integrated with catalogue data from Google Sheets.
- **Dividend Calculations**: Dividend yields and related metrics are calculated using data from Yahoo Finance.

### Data Storage and Analysis

Processed portfolio and dividend data is inserted into BigQuery tables after clearing old data based on timestamps. Key metrics are aggregated for overall portfolio analysis. This automated process ensures that the data is up-to-date, facilitating informed portfolio management and decision-making.

### Trigger Mechanism

- **Google Cloud Scheduler**: Schedules tasks to trigger data collection and processing at specified intervals.
- **Google Cloud Functions**: Executes data integration, processing, and analysis tasks as triggered by Cloud Scheduler.

### Daily Data Integration

- **Portfolio Data**: Collected and processed from Moomoo.
- **FX Rates**: Fetched daily from a third-party API.
- **Catalogue Data**: Integrated from Google Sheets.
- **Dividend Data**: Updated from Yahoo Finance.

This project ensures real-time updates and accurate portfolio monitoring, enabling informed decision-making and efficient portfolio management.
