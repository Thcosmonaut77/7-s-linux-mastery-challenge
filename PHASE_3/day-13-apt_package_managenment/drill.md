# APT Package Management Drill

Refresh the package index, search for and install a small utility, inspect its package details, then 
purge it completely along with its configuration files.

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Refresh the package index
    - sudo apt update

- Search utility
    - apt search nginx

- Install utility
    - sudo apt install nginx -y

- Inspect package details
    - apt show nginx

- Purge package
    - sudo apt purge nginx -y