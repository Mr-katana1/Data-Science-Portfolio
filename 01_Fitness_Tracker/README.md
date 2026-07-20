# Advanced Health & Caloric Optimization Tracker
Project Description
This project set out to create a robust automated data pipeline for the cleaning, processing and analyzing of messy, human-logged fitness data across a 30 day stretch of consistent tracking. The intention behind this process was to remove some of the water weight variations to allow for a clearer view of behavior between training and rest days.
## Tech Stack
- Language: Python
- Libraries: Pandas (Data Manipulation and Time Series Analysis), Seaborn, Matplotlib (Data Visualization)
## Engineering Challenges Resolved
1. Time-Series reconstruction: Fixed the broken calendar of the date information by coercing the messy strings to datetime objects and reconstructing the calendar with .asfreq('D') which would automatically insert missing tracking dates when necessary.
2. Data type correction & data smoothing: Handled all strings of text and numbers to be consistent numeric values with localized string replacement, corrected the data to accommodate all of the null values in the dataset through mathematical forward filling with .ffill() and created a 7 day rolling average column to remove the daily fluctuations of water weight.
3. Data categorization: Standardized the very open string format of workout logs to consistent categorical data.
## Final Business Insight
The final analysis reveals a clear distinction in the behavior, the scattered plot illustrates this point well by separating the caloric intake into clear brackets. As you can see training days exist at the higher caloric intake of ~3,300 kcal with substantial protein intake versus the resting days with ~3,000kcal. With the weight progress perfectly correlated to the 7 day rolling average the data proves a level of optimization in the framework.