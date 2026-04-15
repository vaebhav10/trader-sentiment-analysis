# Trader Performance vs Market Sentiment Analysis

## Overview

This project analyzes how market sentiment (Fear/Greed) impacts trader behavior and performance using historical trading data.

## Dataset

* `fear_greed_index.csv` → Contains daily market sentiment (Fear/Greed classification)
* `historical_data.csv` → Contains trade-level data including PnL, trade size, and timestamps

## Workflow

1. Data Cleaning and Preprocessing

   * Handled missing values and duplicates
   * Converted timestamps to daily format

2. Feature Engineering

   * Aggregated trade-level data into daily metrics per trader:

     * daily_pnl
     * num_trades
     * avg_trade_size
     * win_rate

3. Data Integration

   * Merged trading metrics with sentiment data on date

4. Analysis

   * Compared performance (PnL) across sentiment regimes
   * Analyzed behavior (trade frequency and trade size)
   * Segmented traders (high vs low frequency)

5. Visualization

   * Mean vs median comparisons
   * Sentiment vs performance charts
   * Segmentation analysis

## Key Insights

* Trading activity increases during Fear conditions, indicating reactive behavior
* Profitability is concentrated among high-frequency traders
* Extreme Greed provides the most favorable conditions for active trading

## Setup

Install required libraries:

pip install pandas numpy matplotlib seaborn

## How to Run

1. Place both datasets (`fear_greed_index.csv`, `historical_data.csv`) in the project folder
2. Open the notebook `analysis.ipynb`
3. Run all cells sequentially
4. View outputs, charts, and insights
