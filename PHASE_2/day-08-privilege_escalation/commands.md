# Integrity, Encryption & Firewalling 

- "sudo"
    - **"sudo"** stands for **"SuperUser DO"**
    - It allows a permitted user to execute a command with the privilege of another user, typically the **"root"** user
    - e.g **"sudo apt update"**. This command runs apt update with root privileges

- "sudo -i"
    - The **"sudo"** command with the **"-i"** flag opens an interactive shell environment with root login
    - e.g **"sudo -i"**. This command starts and interactive shell session as root

- "sudo -u"
    - The **sudo"** command with the **"-u"** flag allows you to execute a command as another user
    - e.g **"sudo -u 7even mkdir projects"**. This command enables another user other that *7even* to create the directory, projects as the user *7even*
    - Run **"exit"** to return to the previous user

- "sudo !!"
    - The **sudo"** command with the **"!!"** flag executes the previous command again with the *SuperUser* privilege
    - e.g **"apt update"**, the you run **"sudo !!"**. The **"sudo !!"** will run the previous command which would require *SuperUser* privilege again, this time with the appropriate privilege 
    - **"!!"** is a feature of shells such as *Bash*. it is not itself a *sudo* option

- "sudo -l"
    - The **sudo"** command with the **"-l"** flag lists the privileges available to the current user
    - e.g **"sudo -l"**. This would display commands a user is permitted to execute

- "visudo"
    - This command is used to safely edit the sudo configuration file
    - **"visudo"** performs syntax checking before accepting change which is extremely important for such a critical file 
    - e.g **"sudo visudo"**. This commands opens the sudo configuration file for safe editing 

- "su"
    - Translates to **"switch user"**
    - This command allows you to switch from the current user to another user
    - e.g **"su 7even"**. This commands switches from the current user to *7even*

- "su -"
    - This command switches to another user and creates a login shell
    - e.g **"su - 7even"**. This command switches to the user 7even and creates an interactive shell

- "whoami"
    - This command is used to display the usernam of the current user
    - e.g **"whoami"**. This will print out the username of the current user

- "id"
    - This command displays information such as User ID, Primary group ID, Supplementary groups, and Group names of the current user or another specified user
    - e.g **"id 7even"**. This will print out all those information about the user *7even*
