# Tournament Telemetry: Messy Data Sanitization & EDA Pipeline

## Project Overview

This project constructed an end-to-end data sanitization and exploratory analysis pipeline for real-world, messy data exports. Issues with duplicate data, untidy text/dates, imputation, and calculation of new regional performance metrics were addressed.

## Tech Stack

* **Language**: Python

* **Libraries**: Pandas (String Normalization, Coercion, Imputation), Seaborn & Matplotlib (Exploratory Data Analysis)

## Engineering Challenges that were overcome:

1. **Unstructured string normalisation**: Whitespace removal, standardized casing and mapped inconsistent strings within `Player_Tag` and `Region columns`, removed unwanted non-numeric text and converted into usable values.
2. **Numeric coercing & outlier auditing**: Utilised `pd.to_numeric(errors='coerce')` to strip thousands separators, nullify non-numeric characters like `N/A` into `NaN` and enable subsequent filtering of any negative, anomalous values by applying boolean masks.
3. **Mixed datetime parsing: Leveraged**: `pd.to_datetime(format='mixed')` to handle and standardise various date string formats.
4. **Focused imputation & new metrics**: Audited for null values through boolean row indexing (`df.isna().any(axis=1)`)and then imputed missing values on numeric columns by taking the column median and then engineering a new performance metric(`Damage_Per_Elim`).

## Core Business Insights

* Regional data demonstrated a variation of player average damage output, likely due to geographical baseline differences in each tournament segment.