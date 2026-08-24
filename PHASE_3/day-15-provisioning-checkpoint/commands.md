# Users & Packages Checkpoint 

- "Id <user>"
    - This command displays identity and group information of a specified user
    - e.g **"id 7even"**

- "getent passwd <user>"
    - This command retrieves user-account information from the system's configure user databases
    - e.g **"getent passwd 7even"**

- "useradd -m -G"
    - This command creates a new Linux usr account 
    - The **"-m"** flag creates the user's home directory, The **"-G"** flag specifies supplementary/secondary groups
    - e.g **"sudo useradd -m -G developers,docker 7even"**. THis command will create the user names *7even& and add the new user to the groups *developers and docker*

- "passwd <user>"
    - This command sets or changes a user's password
    - e.g **"sudo passwd 7even"**

- "apt list --installed"
    - This command lists packages that are currently installed on an Ubuntu/Debian system
    - e.g **"apt list --installed"**

- "apt list --upgradable"
    - This command shows packages that have newer versions available in the configured repositories
    - e.g **"apt list --upgradable"**

- "apt update && apt install -y"
    - This single command is actually two separate commands connected with **"&&"**
    - **"apt update"** refreshes the local package indexes. It contacts configured repositories and retrieves information about available packages and versions
    - **"apt install"** installs a specified package
    - The **"-y"** automatically answers *yes* to prompts
    - e.g **"sudo apt update && sudo apt install nginx -y"**

- "dpkg -l | grep"
    - This command uses the **"pipe (|)"** to combine two commands
    - **"dpkg -l"** lists packages known to the Debian package manager
    - The **"pipe (|)"** sends the output of the first command into the second command
    - **"grep"** searches for a specified text pattern
    - e.g **"dpkg -l | grep nginx"**. This command searches the package list for *nginx*

- "apt autoremove"
    - This command removes packages that were automatically installed as dependencies but are no longer required
    - e.g **"sudo apt autoremove"**

- "history"
    - This command displays commands that have previously been entered in the shell
    - e.g **"history"**