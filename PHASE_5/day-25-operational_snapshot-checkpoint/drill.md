# Process & Service Checkpoint Drill

CHECKPOINT. Build a one-screen operational snapshot of a server covering uptime, memory, 
the status of three key services, and any scheduled cron jobs.

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Check uptime
    - uptime

- Check memory 
    - free -h
    - vmstat

- Status of 3 services
    - systemctl status docker
    - systemctl status nginx
    - systemctl status cron