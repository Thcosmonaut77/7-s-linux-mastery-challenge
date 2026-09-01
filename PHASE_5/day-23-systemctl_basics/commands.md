# Init Systems & Systemctl Basics

- "systemctl start"
    - This command is used to start a *systemd* service immediately
    - e.g **"sudo systemctl start nginx"**. This tells *systemd* to *"Start the nginx service now"*

- "systemctl stop"
    - This command is used to stop a running service immediately
    - e.g **"sudo systemctl stop nginx"**

- "systemctl restart"
    - This command is used to stop a service and then start it again
    - e.g **"sudo systemctl restart nginx"**

- "systemctl reload"
    - This command is used to reload a service's configuration without completely stopping the service
    - e.g **"sudo systemctl reload nginx"**

- "systemctl enable"
    - This command is used to configure a service to start automatically during boot 
    - e.g **"sudo systemctl enable nginx"**

- "systemctl disable"
    - This command is used to prevent a service from being automatically started during boot 
    - e.g **"sudo systemctl disable nginx"**

- "systemctl enable --now"
    - This is a very useful shortcut for:
        - enabling the service automatically at startup
        - starting the service immediately
    - e.g **"sudo systemctl enable --now nginx"**

- "systemctl status"
    - This command displays detailed information about a service
    - e.g **"sudo systemctl status nginx"**

- "systemctl is-active"
    - This command checks whether a service is currently active
    - e.g **"systemctl is-active nginx"**

- "systemctl is-enabled"
    - This command checks whether a service is configured to automatically start at boot
    - e.g **"systemctl is-enabled nginx"**