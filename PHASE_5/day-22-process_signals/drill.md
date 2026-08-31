# Controlling Processs with Signals Drill

Start a long-running command in the background, suspend it, resume it in the background, then 
start a second one that survives you logging out, using nohup

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Start a long-running command in the background
    - sleep 700 &

- Confirm 
    - jobs

- Suspend it
    - jobs (to display its place in the job table)
    - fg %1
    - CTRL + Z

- Resume it in the background
    - bg %1

- Confirm it is running 
    - jobs

- Start command that survives logout 
    - nohup sleep 1200 > nohup-test.log 2>&1 &
    