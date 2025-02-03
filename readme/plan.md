# plan.md

Objective: To analyze the effects of X stimulation on heart rate (HR) metrics using the provided data.
Limitations: This task is feasible within the 8-hour limit if the approach is efficient, focusing on key analysis and limiting time spent on minor details. The complexity primarily lies in handling the large dataset and ensuring the analysis captures all significant patterns in HR data.

Steps to Implement:

# Data Preprocessing & Cleaning (2-3 hours):
Merge Datasets:
		Step 1: Load the files (Activity Sessions, Daily Health Metrics, and Health Metrics Samples) into Pandas DataFrames.
		Step 2: Merge the Activity Sessions (File 1) with the Health Metrics Samples (File 3) using FK_USER_ID.
		Step 3: Merge the resultant DataFrame with the Health Metrics Daily (File 2) based on FK_USER_ID and CREATED_DATE.
Clean Data:
		Handle any missing or invalid values (e.g., HR values or timestamps).
		Normalize data where needed (especially timestamp formats, duplicate removal in File 2).

Feature Engineering (1-1.5 hours):
        Create Relevant Columns:
            Stimulation Indicator: Add a column to mark sessions that correspond to periods of X stimulation.
            Heart Rate Change: Calculate the difference in average HR pre- and post-stimulation.
            Duration of Impact: Calculate the duration of the HR impact from the stimulation sessions.
	Time-based Features: Extract time-based features (e.g., time of day, day of week, etc.) to analyze trends over time.

# Exploratory Data Analysis (EDA) (1.5-2 hours):
Overall Trends: Plot average HR values for each user over time.
Distribution of HR: Visualize the distribution of HR metrics before and after stimulation events.
Comparison of Stimulated vs. Non-Stimulated HR: Compare the HR metrics between sessions where stimulation occurred vs. those that did not.
Statistical Analysis: Use t-tests or other statistical tests to assess whether there is a significant difference in HR before and after stimulation.

# Primary Analysis: Does X Stimulation Affect HR? (1.5 hours):
Define Impact of Stimulation: Analyze how HR changes over the course of sessions involving X stimulation, considering average HR changes, duration, and intensity.
Visualize Results: Plot the average HR changes over time and the duration of HR impact. You can use line plots and bar plots to show variations.
Time-series Analysis: Use moving averages to capture the trends in HR before and after stimulation.

# Secondary Insights: Additional Patterns or Trends (1 hour):
Behavioral Trends: Look for trends in HR variability across different days, types of sessions, or users.
Correlations: Investigate correlations between HR and other available metrics (e.g., session intensity, rating, and session type).
Outlier Detection: Identify any unusual patterns, such as users with extreme HR changes during sessions.

# Reporting (1 hour):
Findings Documentation: Prepare a detailed report summarizing the key findings, including:
	Does X stimulation affect HR?
	Duration and magnitude of impact.
	Additional patterns or trends discovered in the data.
Visualizations: Include plots and tables to help illustrate the findings.

---------------------------------------------------------------------------

# Tools & Techniques:
Libraries: Pandas, NumPy, Matplotlib, Seaborn, SciPy (for statistical analysis), and Jupyter Notebook for interactive analysis.
Time-series Methods: Rolling windows for smoothing and trend analysis.
Statistical Tests: t-tests for comparing HR before and after stimulation.

---------------------------------------------------------------------------

# Complexity and Time Estimate:
- Data Preprocessing: Merging and cleaning the data for analysis, handling large data volume (~2GB raw data to be processed). This step is time-intensive due to the size and potential issues with missing or incorrect data.
- Analysis: The primary analysis of the HR effect from X stimulation is straightforward but requires care in identifying the stimulation periods and ensuring correct alignment of data.
- Visualizations and Insights: The time-series analysis and visualization steps require iterative analysis to ensure the interpretation is clear and accurate.
- Final Report: Time will be allocated to summarizing the findings in a clear, concise report.

Total time to implement from scratch: 7.5-8 hours.
