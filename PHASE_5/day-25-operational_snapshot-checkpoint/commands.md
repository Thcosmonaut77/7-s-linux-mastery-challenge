# Process & Service Checkpoint 

- "ps aux | grep"
    - This combination of commands is used to find a running process by name
    - e.g **"ps aux | grep sshd"**

- "systemctl status <svc>"
    - This command displays the current status of a systemd service
    - e.g **"systemctl status docker"**

- "journalctl -u <svc> --since today"
    - This command displays's today's logs for a particular systemd service
    - e.g **"sudo journalctl -u nginx --since today"**

- "kill -0" (liveness check)
    - This one is particularly useful for scripting 
    - This command doesn't kill the service, rather it tests whether it exists and whether you have permission to signal it 
    - e.g **"kill -0 1234"**

- "uptime"
    - This command:
        - displays the current time
        - How long the system has been running 
        - Number of logged-in users
        - Load averages
    - e.g **"uptime"**

- "free -h"
    - This command displays RAM and swap memory usage in human-readable format 
    - e.g **"free -h"**

- "vmstat"
    - This means **virtual memory statistics**
    - It provides a quick overview of:
        - processes
        - memory
        - swap
        - I/O
        - system activity
        - CPU usage
    - e.g **"vmstat"**

- "iostat"
    - This command displays CPU & disk I/O statistics
    - It is commonly used when investigating why a server is lags
    - e.g **"iostat"**

- "watch"
    - This repeatedly executes a command and displays its output every few seconds
    - e.g **"watch uptime"**

- "crontab -e / crontab -l"
    - These commands are used to manage cron jobs for a user
    - Cron auomatically execute commands at scheduled times
    - **"crontab -e"** opens your user's cron table for editing 
    - e.g **"crontab -e"**
    - **"crontab -l"** lists the current user's cron jobs
    - e.g **"crontab -l"**