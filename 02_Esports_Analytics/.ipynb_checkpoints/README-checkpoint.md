# Esports & Competitive Match Performance Analytics

## Project Overview
This project engineered a data pipeline to ingest, sanitize, and analyze chaotic match telemetry from competitive multiplayer lobbies. The objective was to isolate the mathematical correlation between raw in-game damage output and overall match placement across various game modes.

## Tech Stack
- **Language:** Python
- **Libraries:** Pandas (Data Sanitization), Seaborn & Matplotlib (Statistical Visualization)

## Key Engineering Challenges Solved
1. **Text Trailing & Casing Normalization:** Eliminated hidden padding and trailing spaces across categorical strings using `.str.strip()` and normalized text casing to prevent index duplication during aggregation.
2. **Regex Substring Extraction:** Parsed mixed text/numeric data structures (e.g., '5 kills') using regular expression digit mapping (`r'(\d+)'`) while safely mapping missing rows to zero.
3. **String Delimiter Stripping:** Cleared localized string formatting (commas within thousands) to prevent numeric parsing exceptions before casting features to floating-point metrics.

## Final Analytical Takeaway
Lobby telemetry confirms a strong correlation between high-impact damage and critical placement thresholds. Solo queues generated the highest baseline damage efficiency (1,200 units per match), yielding a superior average placement tier (6.0) compared to group queues.