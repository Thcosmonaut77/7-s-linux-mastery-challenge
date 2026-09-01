# Viewing Processes Drill

Find the PID of a running process by name, view it in top, show it as part of the process tree, and 
identify which process is using port 80.

# Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Find PID of a running process by name 
    - pgrep -a nginx

- View process in top
    - top
        - L, nginx

- Show as part of process tree
    - pstree -p

- Identify what process is using port 80
    - sudo lsof -i :80