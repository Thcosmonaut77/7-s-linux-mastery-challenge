# Deeper Service Management & Log

- "systemctl list-units --type=service"
    - This is a command used to list the currently loaded service units managed by *systemd*
    - e.g **"systemctl list-units --type=service"**

- "systemctl list-units --state=failed"
    - This command is used to display systemd units that have entered a failed state
    - e.g **"systemctl list-units --state=failed"**

- "systemctl daemon-reload"
    - This command tells *systemd* to reload its unit configuration files
    - e.g **"sudo systemctl daemon-reload"**

- "journalctl"
    - This command displays logs collected by the systemd journal
    - e.g **"journalctl"**

- "journalctl -f"
    - This command continuously follows the system journal as new entries arrive
    - e.g **journalctl -f"**

- "journalctl -u"
    - This command displays the journal entries belonging to a specific systemd unit/service
    - e.g **"journalctl -u nginx"**

- "journalctl --since"
    - This command displays journal entries starting from a specified time or date 
    - e.g **"journalctl --since "1 hour ago""**

- "journalctl -p err"
    - This command displays journal messages at the error priority level
    - e.g **"journalctl -p err"**

- "tail -f /var/log/syslog"
    - This command continuously monitors the traditional syslog file 
    - e.g **"tail -f /var/log/syslog"**

- "tail -f /var/log/auth.log"
    - This command continuously monitors the authentication log on systems such as ubuntu, that maintain */var/log/auth.log*
    - e.g **"sudo tail -f /var/log/auth.log"**