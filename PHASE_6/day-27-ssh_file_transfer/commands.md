# Remote Access & File Transfer

- "ssh"
    - **"ssh"** stands for *Secure Shell*. It allows you to securely connect to and administer a remote Linux/Unix machine over an encrypted connection 
    - Instead of physicaly logging into a server, you can connect from your terminal
    - e.g **"ssh ubuntu@192.168.1.50"**. Where *ubuntu* is the user name, while the IP address is the server public IP.
    - You may be prompted for the user's password. After successful authentication, you will get a shell on the remote machine

- "ssh -p"
    - The **"-p"** flag specifies the SSH server port
    - By default, SSH port is 22, but sometimes, administrators might configure SSH to listen on another port
    - e.g **"ssh -p 77 ubuntu@192.168.1.50"**

- "ssh -i"
    - The **"-i"** flag specifies the private SSH key to use for authentication
    - e.g **"ssh -i ~/keys/server.pem ubuntu@192.168.1.50"**
    - The private key stays in your computer while the public key is placed on the server
    - Private keys should always have restrictive permissions:
        - 400

- "ssh-keygen"
    - This command is used to create and manage SSH keys
    - It is one of the most important commands for passwordless & secure SSH authentication
    - e.g **"ssh-keygen"**

- "ssh-copy-id"
    - This command copies your public SSH key to a remote user's *~/.ssh/authorized_keys*
    - This allows you to authenticate using your private key instead of entering the account password every time
    - e.g **"ssh-copy-id ubuntu@192.168.1.50"**

- "scp"
    - This means *Secure Copy*
    - It allows you to securely copy files between machines using SSH
    - e.g **"scp website.html ubuntu@192.168.1.50:/var/www/html/"**. This copies the *website.html* file from your machine to the remote machine
    - e.g **"scp ubuntu@192.168.1.50:/home/ubuntu/log.txt ."**. This copies the *log.txt* file from the remote machine to your local machine

- "sftp"
    - This means *SSH File Transfer Protocol*
    - It provides an interactive file-transfer session over SSH
    - e.g **"sftp ubuntu@192.168.1.50"**. This will get you an interactive shell for file transfer
        - ls:       list remote files
        - cd:       change remote working directory 
        - lpwd:     show local directory
        - lcd:      change local directory 
        - get:      download a file
        - put:      upload a file
        - get -r:   download directory
        - put -r:   upload directory 
        - exit:     exit
        - bye:      exit 

- "rsync"
    - This is a powerful tool for synchronizing files & directories
    - It is particularly useful because it can transfer only the data that has changed
    - e.g **"rsync -av website/ ubuntu@192.168.1.50:/var/www/website/"**. This will synchronize the local to the remote
    - e.g **"rsync -av ubuntu@192.168.1.50:/var/www/website/ ./website/"**. This will synchronize the remote to the local

- "~/.ssh/config"
    - This is your persona SSH client configuration file
    - It allows you to define connection settings once instead of repeatedly typing long commands
    - The file's permission must be 600

- "sshd_config hardening"
    - This file, located at */etc/ssh/sshd_config* controls the behaviour of the SSH server
    - After modifying your *sshd_config*, always run: **"sudo sshd -t"**. If there is no output then the configuration is valid.
    - If there is an error, fix it before restarting the sshd service