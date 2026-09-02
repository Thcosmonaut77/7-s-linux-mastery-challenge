# Deeper Service Management & Logs Drill

List every failed service on the box, then pull today's logs for one specific service, filtered to errors 
only, and follow it live for one minute.

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- List failed services
    - systemctl list-units --state=failed

- Pull today's log for a service
    - journalctl -u nginx --since today

- Livestream today's error logs for one minute
    - 