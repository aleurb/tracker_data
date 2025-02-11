# Data exploration: manual

# File 1. SESSIONS:
- Size: 1'930'677 records, 252MB
- Period: from 2024-04-02 to 2025-01-28
PK_ACTIVITY_SESSION_ID  # PK
CREATED_DATE            # End of session. Out of scope
LAST_MODIFIED_DATE      # Flag for modifications. Out of scope.
ROW_IS_VALID            # Flag for valid records.
FK_USER_ID              # FK: user Id. Links to daily
FK_SYSTEM_PROGRAM_ID    # FK: program ID
START_DATE              # Session start datetime
END_DATE                # Session end datetime
FK_REFERENCE_ID         # FK: reference id, out of scope
SESSION_TYPE            # session type, category, text
IS_FINISHED             # flag: is session finished
INTENSITY               # flag: if has value, then stimulator is on
RATING                  # remove: out of scope
RATING_ISSUE            # remove: out of scope
RATING_ISSUE_MESSAGE    # remove: out of scope
- Data frequency: several per day
- Data (header + first three rows + last three rows):
	"PK_ACTIVITY_SESSION_ID","CREATED_DATE","LAST_MODIFIED_DATE","ROW_IS_VALID","FK_USER_ID","FK_SYSTEM_PROGRAM_ID","START_DATE","END_DATE","FK_REFERENCE_ID","SESSION_TYPE","IS_FINISHED","INTENSITY","RATING","RATING_ISSUE","RATING_ISSUE_MESSAGE"
	1,"2024-04-02 11:15:07","2024-04-02 11:15:07",1,3,1,"2024-04-02 11:09:40","2024-04-02 11:15:07",1,"Program",1,NULL,NULL,NULL,NULL
	2,"2024-04-04 07:51:07","2024-04-04 07:51:07",1,215,1,"2024-04-04 07:47:05","2024-04-04 07:51:07",1,"Program",1,NULL,NULL,NULL,NULL
	3,"2024-04-04 08:15:31","2024-04-04 08:15:31",1,120,2,"2024-04-04 08:09:31","2024-04-04 08:15:31",2,"Program",1,NULL,NULL,NULL,NULL
	1928186,"2025-01-28 05:03:48","2025-01-28 05:03:48",1,70701,0,"2025-01-28 05:03:48","2025-01-28 05:15:48",19,"Program",1,9,NULL,NULL,NULL
	1928187,"2025-01-28 05:03:57","2025-01-28 05:03:57",1,40592,0,"2025-01-28 05:03:57","2025-01-28 05:11:57",2,"Program",1,7,0,"Device Malfunction",""
	1928188,"2025-01-28 05:04:01","2025-01-28 05:04:01",1,65874,0,"2025-01-28 05:04:01","2025-01-28 05:12:01",4,"Program",1,3,1,NULL,NULL


# File 2. DAILY: Daily Measurements
- Size: 166'409 rows, 17MB
- Period: from 2024-09-08 to 2025-01-28
- Column `FK_USER_ID`: foreign key, UserID
- Column `PK_HEALTH_METRICS_HEART_ID`: foreign key, identifies User's `HeartID`
- Column `DATE`: day of sessions
- Column `TIMEZONE_OFFSET`: can be ignored, because Heart Sample data already saves data in server time including the time offset
- Data Frequency: daily
- Data (header + first three rows + last three rows):
	"PK_HEALTH_METRICS_HEART_ID","FK_USER_ID","DATE","TIMEZONE_OFFSET","RESTING_HR","MIN_HR","AVG_HR","MAX_HR","SOURCE","HEART_RATE_VARIABILITY_DAY_HRV","HEART_RATE_VARIABILITY_SLEEP_HRV","CREATED_DATE","LAST_MODIFIED_DATE","ROW_IS_VALID"
	1,"14064","2024-09-08",10800,65,60,73,133,"apple",NULL,NULL,"2024-09-11 09:56:50","2024-09-11 09:56:50",1
	2,"14064","2024-09-09",10800,65,60,73,133,"apple",NULL,NULL,"2024-09-11 09:56:52","2024-09-11 09:56:52",1
	3,"28876","2024-09-09",7200,77,75,89,119,"apple",NULL,NULL,"2024-09-11 09:57:01","2024-09-11 09:57:01",1
	166407,"10354","2025-01-28",-10800,NULL,50,53,57,"apple",NULL,NULL,"2025-01-28 10:11:28","2025-01-28 10:11:28",1
	166408,"47537","2025-01-28",-25200,NULL,68,69,70,"apple",NULL,NULL,"2025-01-28 10:14:56","2025-01-28 10:14:56",1
	166409,"37161","2025-01-28",-10800,NULL,73,73,73,"apple",NULL,NULL,"2025-01-28 10:17:09","2025-01-28 10:17:09",1


# File 3. SAMPLES: measurements by `HeartId`
- Size: 77'064'762 records, 6.3GB
- Period: from 2024-09-08 21:04:00 to 2025-01-28 10:32:54
- Variable `PK_HEALTH_METRICS_HEART_HR_SAMPLE_ID`: PK
- Variable `FK_HEALTH_METRICS_HEART_ID`: Foreign Key, joins to `HEART_ID`
- Variable `DATE`: measurements of average heart rate at specific time of session
- Variable `AVG_HEART_RATE`: measurement value. Contains float and integer values, and can be rounded to N digits precision
- Data Frequency: every few minutes, multiple per hour
- Data (header + first three rows + last three rows):
	"PK_HEALTH_METRICS_HEART_HR_SAMPLE_ID","FK_HEALTH_METRICS_HEART_ID","DATE","AVG_HEART_RATE","CREATED_DATE","LAST_MODIFIED_DATE","ROW_IS_VALID"
	240,3,"2024-09-09 11:24:00",97,"2024-09-11 09:57:03","2024-09-11 09:57:03",1
	241,3,"2024-09-09 11:32:00",91.33333333333333,"2024-09-11 09:57:03","2024-09-11 09:57:03",1
	242,3,"2024-09-09 11:35:00",90,"2024-09-11 09:57:03","2024-09-11 09:57:03",1
	77064760,166035,"2025-01-28 08:52:00",75,"2025-01-28 10:32:54","2025-01-28 10:32:54",1
	77064761,166035,"2025-01-28 08:56:00",81.33333333333333,"2025-01-28 10:32:54","2025-01-28 10:32:54",1
	77064762,166035,"2025-01-28 09:01:00",78,"2025-01-28 10:32:54","2025-01-28 10:32:54",1
