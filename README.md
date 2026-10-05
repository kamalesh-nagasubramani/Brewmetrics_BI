# Brewmetrics_BI

A version-controlled Power BI solution for analysing coffee sales across cities, store formats and time.
# BrewMetrics Coffee Co. — Business Intelligence Solution

A version-controlled Power BI solution for analysing BrewMetrics coffee sales across cities, store formats, products and time.

## Project Overview

This project transforms BrewMetrics Coffee Co.'s transactional coffee sales data into an interactive Power BI dashboard. The solution focuses on sales performance, monthly trends, city-level differences, store-format performance and the seasonal behaviour of Cold Brew.

## Data Model

The Power BI solution uses a star-schema structure consisting of:

- **FactCoffeeSales** — contains transactional sales information including date, city, store format, category, item, quantity, unit price and sales amount.
- **DimDate** — supports analysis by date, month, quarter and year.
- **DimStore** — contains city and store-format information.
- **DimProduct** — contains product and category information.

Relationships connect the three dimension tables to the central sales fact table.

## DAX Measures

The model includes measures for:

- Total Sales
- Previous Month Sales
- Month-over-Month Sales Growth %
- Cumulative Sales
- City Rank using RANKX
- Average Sale

## Dashboard

The dashboard provides:

- Total Sales, Average Sale and Month-over-Month Growth KPIs
- Monthly sales trend
- City-level sales comparison
- Store-format performance by city
- Cold Brew monthly sales trend
- City slicer for interactive filtering
- City and Store Format drill-down analysis

## Key Insights

The dashboard can be used to identify differences in sales performance between cities and store formats.

The monthly trend helps highlight changes in sales over time, while the dedicated Cold Brew view makes it easier to examine its seasonal sales pattern.

The city-level comparison also helps identify which locations contribute most strongly to overall sales and where performance gaps exist.

## Version Control and Copilot

The project was developed as a Power BI Project and maintained in GitHub with separate commits for the schema, DAX measures and completed dashboard.

GitHub Copilot was used to assist with the initial DAX development and modelling decisions. Copilot suggestions were reviewed against the actual Power BI semantic model before implementation.