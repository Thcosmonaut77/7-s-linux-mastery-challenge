# Controlling Processes with Signals

- "kill"
    - Despite its name, **"kill"** does not necessarily mean "terminate a process", it sends a signal to a process
    - The proces is identified using its PID(process ID)
    - e.g **"kill 123"**. This sends a default signal which is *SIGTERM* to the process *123*
    - *SIGTERM* means *"please terminate yourself gracefully"*

- "kill -9"
    - This command sends the *SIGKILL* signal to the process
    - *SIGKILL* tells the kernel to *"immediately terminate the process*
    - e.g **"kill -9 123"**

- "kill -HUP"
    - This command sends the *SIGHUP* signal to the process
    - *-HUP* stands for *hangup* and it typically reloads the service without completely stopping and restarting
    - Not all services treat *-HUP* as "*reload"*
    - e.g **"kill -HUP 123"**

- "killall"
    - This command sends signals to processes based on their names, rather that PID
    - e.g **"killall firefox"**

- "pkill"
    - This is another command for sending signals to processes based on criteria such as:
        - process name
        - pattern
        - user
        - group
        - terminal
        - PID
    - e.g **"pkill -f "python app.py" "**. The *-f* option matches against the full command line, particularly useful when multiple processes use the same executable

- "fg"
    - **"fg"** means *foreground*
    - It brings a background or suspended job into the foreground
    - e.g **"fg"**

- "bg"
    - **"bg"** means *background*
    - This command resumes a suspended job and allows it to continue running in the background
    - e.g **"bg"**

- "Ctrl + Z"
    - This is a keyboard shortcut, not an actual command you type 
    - It sends the *SIGTSTP* signal to the foreground process
    - This normally suspends the process
    - e.g **"CTRL + Z"**

- "nohup"
    - *no hangup*
    - It allows a command to continue running after you close your terminal or log out 
    - e.g **"nohup ./long_backup.sh &"**. This command will run the backup in the background, and persist even when you lose connection to the server or you close you terminal

- "disown"
    - This is a *shell built-in*
    - It removes a job from the shell's job table
    - This is especially useful when you've already started a command and forgot to use **"nohup"**
    - e.g run **"jobs"** to view running processes in the background, the use the serian number of the process you want to remove; **"disown %4"**. This will remove the process that is 4th in the job table
    