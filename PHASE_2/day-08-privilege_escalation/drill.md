# Privilege Escalation & Identity Drill

Attempt a command that fails for lack of permission, re-run it instantly with sudo !!, then list 
exactly which commands your account is permitted to run as another user.

## Steps/Commands
- Attempt command that requires higher privilege
    - apt update

- Re-run command with sudo 
    - sudo !!

- List commands available as another user
    - sudo -u root sudo -l