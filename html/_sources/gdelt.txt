GDELT Data Collection
=====================

Each day, a cronjob runs a script that finds the previous date, and then runs gdelt.py to download the gdelt file for each candidate. Then, parseGDELT.py gets the article count for each candidate, and then the data is stored into each candidate's GDELT table in Cassandra.

