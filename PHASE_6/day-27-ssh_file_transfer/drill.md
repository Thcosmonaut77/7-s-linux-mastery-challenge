# Remote Access & File Transfer

Generate an SSH key pair, copy the public key to a remote host, connect without a password, then 
securely copy a file to and from that server.

# Steps/Commands
- Open Terminal
    - launch ubuntu terminal

- Generate SSH key pair
    - ssh-keygen
    - follow prompts

- Create remote host & copy public key 
    - launch an ubuntu ec2 instance
    - set password
    - add local machine public key to the authorized_keys file

- Connect to remote server without password
    - On local machine:
        - ssh ubuntu@3.255.186.86

- Securely copy file from remote to local
    - touch file
    - exit (from remote server)
    - one local:
        - scp ubuntu@3.255.186.86:/home/ubuntu/file .