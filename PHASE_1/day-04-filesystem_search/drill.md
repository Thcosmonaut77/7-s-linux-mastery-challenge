# Filesystem Search Drill

Find every .conf file under /etc, find every file larger than 1MB in /var, then report total disk usage 
of /home and remaining free space on the root filesystem.

## Steps/Commands
- Open terminal
    - Launch ubuntu terminal

- Find every .conf file in /etc
   - find /etc -name *.conf

- Find files larger that 1MB in /var 
    - find /var -size +1M

- Total disk usage of /home
    - du -sh /home

- Free space on root filesystem 
    - df -h /