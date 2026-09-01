# Init Systems & Systemctl Basics Drill

Pick a service, stop it, confirm it is inactive, restart it, enable it to auto-start at boot in a single 
combined command, and confirm both its active and enabled state

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Pick a service
    - apt list | nginx

- Stop the service
    - sudo systemctl stop nginx

- Confirm
    - sudo systemctl status nginx

- Restart the service
    - sudo systemctl start nginx

- Confirm
    - sudo systemctl status nginx

- Enable to auto start at boot
    - sudo systemctl enable --now nginx

