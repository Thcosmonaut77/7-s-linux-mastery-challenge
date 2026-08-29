# Text Processing Checkpointy Drill

CHECKPOINT. From a raw log file, build one pipeline that filters for 'error' entries, extracts the 
timestamp column, sorts the results, and removes duplicates, all in a single chained command.

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Navigate to logfile location
    - cd /var/log

- Run chained command
    - grep -i "error" syslog | awk '{print$1}' | sort | uniq

