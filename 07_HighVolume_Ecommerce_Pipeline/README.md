# High-volume e-commerce analytics (~540k entries)

## Project highlights
There has been developed data sanitation and customer-analytic pipeline for high-volume e-commerce data set with more than 540,000 database entries.
The project tackled various issues, such as encoding, cancellations, unit price issues, number of items purchased, missing customer identifiers and revenue trends across time-scales years to months
## Tech Stack

* **Language:** Python
* **Libraries:** Pandas (vectorized operations, period time-series, aggregates), seaborn, matplotlib (plots)
## Engineering Steps:

1- **Encoding and robust ingestion:** ~540k rows processed within pandas with proper latin1 byte-stream encoding;
2- **Audited transaction cancellations:** ~140k entries have been removed, including string-prefixed invoice entries ( Cxxxxx), negative returns, zero price entries;
3- **Customers filtering** Customers with missing ID's are isolated in separate processing batch to compute lifetime value;
- **Vectorized transformation and aggregation:** quantity x unit-price is calculated, transformed into month period ('M') and summarized with nunique of customers and invoices.