# Steam Telemetry: Real-World Data Sanitization and Time-series EDA

## Project Summary

This pipeline creates an end-to-end process for cleaning and performing time-series analysis on real-world monthly player telemetry from Steam. Issues such as string-formatted percentages, separate year and month components, missing first-month deltas and unclean numerical data are all solved to enable analysis on multi-year player-base trends.

## Tech Stack

* **Language**: Python

* **Libraries**: Pandas (for numerical coercion, date synthesizing and aggregation), Seaborn and Matplotlib (for time-series data visualization)

## Engineering Process

1. **String and Percentage Normalization:** Removed % symbols from telemetry metrics (such as avgpeakperc) and converted the string-formatted inputs into real numbers. (e.g. '92%' becomes 0.92, and the input was transformed via pd.to_numeric() into float64).
2. Temporal Features: Synthesized datetime objects from fragmented year and month columns, and merged them back together to create time-series features (i.e. Datetime64).
3. Missing Value Imputation: Corrected unclean monthly percentage deltas (e.g. "gain" field) and set initial months to a baseline value of 0. (e.g. Filled NA gain with 0 via fillna()).
4. Time-Series Analysis: Ranked games by aggregate simultaneous users and displayed historical data for leading esports games such as Dota 2 on plots.