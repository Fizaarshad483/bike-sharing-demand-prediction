# bike-sharing-demand-prediction
**IBM Applied Data Science with R — Capstone Project**
## Overview
End-to-end predictive analytics project forecasting hourly bike-sharing demand across 5 global cities (Seoul, New York, Paris, London, Suzhou) using weather and time data.

## Key Results
- Best model: Lasso regression with polynomial terms
- R² = 0.778 | RMSE = 300 (target: R² > 0.72, RMSE < 330) 
- Improved from baseline R² = 0.69 — 13% reduction in error

## Tools & Methods
- **Languages:** R (tidyverse, ggplot2, tidymodels, glmnet, R Shiny)
- **Database:** SQLite via RODBC — 11 analytical queries
- **APIs:** OpenWeather API (live 5-day forecasts via httr)
- **Web scraping:** Wikipedia bike systems data via rvest
- **Dashboard:** Interactive R Shiny app with Leaflet map

## Project Structure
- Data collection via OpenWeather API and Wikipedia scraping
- Data wrangling: regex cleaning, min-max normalisation, dummy variables
- EDA: 11 SQL queries + 6 ggplot2 visualisations
- Predictive modelling: compared 5 regularised regression models
- Deployment: R Shiny dashboard with live weather-to-demand forecasting

## Key Findings
- Temperature and hour of day are strongest demand predictors
- Rainfall is the strongest suppressor (coefficient ~2,050)
- Summer peak: up to 3,556 bikes/hour; winter low: ~300 bikes/hour
- Lasso outperformed Ridge and ElasticNet by automatically removing redundant features

## Files
- `capstone_presentation.pdf` - full project report with visualisations and code snippets
- `SQLite.ipynb` - including R SQL queries 
- `Evalution.ipynb` - including analysis and plots
