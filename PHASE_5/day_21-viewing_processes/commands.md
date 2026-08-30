# Viewing Processes

- "ps aux"
    - This command displays a snapshot of all running processes on the system 
    - e.g **"ps aux"**. This command gives you a broad view of processes currently running on your linux machine

- "ps -ef"
    - This command displays all running processes in a full-format listing 
    - e.g **"ps -ef"**

- "ps -u"
    - This command displays processes associated with a specific user
    - e.g **"ps -u 7even"**. This command displays the currently running processes associated with the user *7even*

- "top"
    - This command provides a real-time, continuously updating view of running processes
    - Unlike the **"ps"** command which normally gives you a snapshot, **"top"** continuously refreshes the information
    - e.g **"top"**. press *q* to exit

- "htop"
    - This is an interactive and more user-friendly version of **"top"**
    - e.g **"htop"**

- "pgrep" 
    - This command searches for processes based on their name or other attributes and returns their PIDs(process IDs)
    - e.g **"pgrep nginx"**. 

- "pstree"
    - This command displays processes in tree structure, showing parent-child relationships
    - e.g **"pstree"**

- "lsof -i"
    - This command list open files
    - In linux, many resources are represented as files including network connections
    - e.g **"lsof -i"**. This will show processes that have network sockets open

- "jobs"
    - This command displays jobs that are running or stopped in your current shell session
    - This is different from **"ps"** which shows system processes
    - e.g **"jobs"**

- "nice/renice"
    - These commands control the CPU scheduling priority of processes.
    - They are especially useful when you want a CPU-intensive task to have less impact on other workloads
    - **"nice"** starts a new process with a specified niceness value
    - e.g **"nice -n 10 backup.sh"**. This command will start *backup.sh* with a niceness value of *10*
    - **"renice"** changes the nice value of a process that is already running
    - e.g **"renice 10 -p 823"**. This will change the PID 823 to a nice value of 10