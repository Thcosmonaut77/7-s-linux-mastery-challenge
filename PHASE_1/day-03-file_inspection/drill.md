# File Inspection Drill

Pick any log file on the system. View it fully with cat, page through it with less, show the first and 
last 15 lines, count its lines, identify its file type, and inspect its full metadata with stat.

## Steps/Commands
- Open terminal
    launch Ubuntu terminal

- Navigate to log file
    - cd /var/log

- View log file with cat
    - cat auth.log

- Scroll through with less
    - less auth.log

- First 15 lines
    - head -15 auth.log

- Last 15 lines
    - tail -15 auth.log

- Count lines
    - wc -l auth.log

- Identify file type
    - file auth.log

- Inspect metadata
    - stat auth.log