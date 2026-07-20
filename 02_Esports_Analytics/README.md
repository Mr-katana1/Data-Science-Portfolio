
project overview
this project built out a data pipeline that took in unclean, raw match telemetry from competitive multiplayer lobbies and clean, transform, analyze and derive insights from. The goal was to find the mathematical correlation of in game raw damage dealt to rank in game in a match.
## tech stack
* language: python
* libraries: pandas(for data cleaning), seaborn & matplotlib(for statistical visualization)
## key engineering challenges solved
1. Text trailing and casing normalization : removed hidden whitespace and trailing characters in all categorical strings using pandas .str.strip() method and lowercased all text inputs to prevent duplicated keys during aggregation and counting.
2. Regex substring extraction : parsed string formatting with non numeric and numeric values mixed together like '5 kills' by finding all integer patterns using regex digit capture r'(\d+)'. This safely allowed for any nulls to map to 0.
3. String delimiter stripping : cleared localized string formatting such as commas within the thousands using string methods. This allowed features with string formatting to be safely cast into floats.
## final analytical takeaway
lobby telemetry has validated that there exists a strong relationship between high value damage outputs and crucial placement cutoffs. Lobby solo queues achieved the best raw damage to placement efficiency with an average baseline of 1,200 damage per game at a placement rank average of 6.0. Group lobbies' raw damage per placement was 1,077 damage at rank average 7.3.