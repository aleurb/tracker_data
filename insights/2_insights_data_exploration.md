# @title: Findings
# @date : 2025-02-11 ALUR

- Original data is not normalized. Therefore, data transformation and data validation is required.
- Data size: Amount of rows is significant: File 3 contains more than 70 mln rows.
- Data contains multiple tables. Therefore, tables must be merged.
- Dataset `Daily`: possible data duplicates (PK_HEALTH_METRICS_HEART_ID=1,2)
