# Weather Telemetry REST API & Time-Series Pipeline

## Project Overview
This project is an automated data pipeline that connects to a public API, show hourly weather telemetry, parses nested JSON , and convert time-series metric into daily analytical summaries and trends.

## Tech Stack
* **Language:** Python
* **Libraries:** Requests (HTTP/API integration). Pandas (JSON & time-series aggregation), Seaborn & Matplotlib (Data Visualization)

## Key Engineering Challenges Solved
1. **JSON Payload Unpacking:** Extracted nested dictionary structures from whether API responses to flatten multi-variable hourly arrays into a structured Pandas DataFrame.
2. **Datetime Transformation:** Converted raw object string timestamps into native datetime and enabling time-series featurs ('.dt.date' and '.dt.hour')
3. **Multi-Metric Dictionary Aggregations:** Using Pandas `.groupby().agg()` with dictionary mapping to Calculate distinct statistical metrics (mean temperatures vs MAX wind speeds) in a single pass

## Final Analytical Takeaway
The time series line plot highlights distinct diurnal temperature cycles across the 7-day period, while daily aggregation successfully isolated MAX wind speed events against baseline average temperatures.