# Table description and usage

`FK_USER_ID` points to a user on our database, so this would be the source of truth for both SESSIONS and HEART METRICS.


# Activity sessions:
FK_REFERENCE_ID refers to an entry in our database depending on SESSION_TYPE, so for SESSION_TYPE=Program, FK_REFERENCE_ID=1 means it's a Program of ID 1


# Heart daily:
All fields should be self explanatory by reading the name


# Heart samples:

FK_HEALTH_METRICS_HEART_ID points to an entry from the daily data, so if this is set to 1, then it refers to a daily data entry with PK_HEALTH_METRICS_HEART_ID=1

the rest of the fields should be self explanatory.


If needed, we can provide these same exports in SQL format, if that works better for you.
