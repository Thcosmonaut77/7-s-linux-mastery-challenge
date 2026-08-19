# Security Checkpoint & Audit Drill

CHECKPOINT. Produce a one-page mini security audit of a server: who has logged in recently, 
who is logged in right now, which accounts have never logged in, and every sudo command run in 
this session

## Steps/Commands
- Open Terminal
    - Launch an ubuntu terminal

- Who has logged in recently
    - last -10

- Who is currently logged in 
    - w

- Accounts that have never logged in 
    - lastlog | grep -i "never logged in"

- Every sudo command run in this session
    - history | grep -i sudo
    