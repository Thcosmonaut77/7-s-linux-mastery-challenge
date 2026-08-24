# Users & Packages Checkpoint Drill

CHECKPOINT. Provision a complete new team member account (user, groups, password) and 
install the three tools they need for their role, in a single documented sequence.

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Create group
    - sudo groupadd devops

- Create user with password
    - sudo adduser user1

- Add user to group
    - sudo gpasswd -a user1 devops

- Verify
    - id user1
    - getent group devops
    - groups user1

- Install tools for role
    - sudo apt update && sudo apt install docker.io git nginx -y

- Add user to docker group
    - sudo usermod -aG docker user1

- Verify
    - groups user1