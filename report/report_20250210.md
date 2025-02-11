
@title : Impact of Stimulation on Heart Rate
@date  : 2025-02-10
@author: Aleksandras Urbonas

1. Primary Question: Does X stimulation affect heart rate metrics?
- Based on the analysis, we found that users (N=2361) who participated in the 'Program' - indicating stimulation - (at least S=10 sessions) - showed an average HR change of -0.03 bpm. 
- The impact varied across sessions, with the maximum observed change being 95.00 bpm.

2. Secondary Insights:
- Additional factors influencing HR change include session duration and time of day (further analysis needed for seasonality patterns).
- A significant amount of time was dedicated to data exploration and schema understanding. A more detailed schema and business process description can be of help.
- Samples data contains ~70 mln records, which slows the analysis and it is recommended to process such data in SQL, for example, performing aggregations by user over different periods of time.
- Data validation was completed: some records were excluded from analysis.
- Data was analysed using Python, allowing the analysis to be repeated.
