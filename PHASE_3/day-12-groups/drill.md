# Groups & Access Circles Drill

Create a group named devs, add two users to it, confirm membership with getent, remove one 
member, then delete the group entirely

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Create group *devs*
    - sudo groupadd devs
    - getent group devs

- Add two users to the *devs* group
    - sudo useradd user1
    - sudo useradd user2
    - sudo gpasswd -a user1 devs
    - sudo gpasswd -a user2 devs

- Confirm memebership 
    - getent group devs

- Remove one memeber
    - sudo gpasswd -d user1 devs
    - getent group devs

- Delete the group
    - sudo groupdel devs
    - getent group devs