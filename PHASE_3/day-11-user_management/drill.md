# Creating & Managing Users Drill 

Create a new user with a home directory and Bash shell, set their password, add them to a 
secondary group, rename the account, then remove it along with its home directory

## Steps/Commands
- Open terminal
    - Launch an ubuntu terminal

- Create new user with home directory and bash shell
    - sudo useradd -ms /bin/bash 7even
    - getent passwd 7even

- Set password
    - sudo passwd 7even
    - "*no display, type in password correctly*"

- Add to secondary group
    - sudo usermod -aG sudo 7even
    - id 7even

- Rename account 
    - sudo usermod -l purple 7even 
    - id purple

- Remove account recursively 
    - sudo userdel -r purple