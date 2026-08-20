# Creating & managing Users

- "useradd"
    - This is a command in Linux that is used to create a new user account .
    - It creates the account entry, but depending on the options and distributions, it may not automatically create a home directory or password
    - e.g **"sudo useradd 7even"**. This command will create a user called *7even*. without a home directory you can verify with the command **"id 7even"**

- "useradd -m"
    - The **"useradd"** command with the **"-m"** flag is used to create a user with its own home directory 
    - e.g **"sudo useradd -m 7even"**. This create the user *7even* along with the user's home directory 

- "useradd -m -s"
    - This command combines both the **"-m"** flag to create user's home directory and **"-s"** to specify the user's login shell
    - e.g **"sudo useradd -ms /bin/bash 7even"**. This will create the user *7even* along the a home directory, and also sets the user's login shell to be */bin/bash*

- "adduser"
    - This command is more user-friendly and has a higher level interface for creating users
    - It creates the user, the user's home directory, the password, takes details like full name and work phone, and add users to supplemental groups
    - e.g **"sudo adduser 7even"**

- "passwd"
    - This command is used to set or change a user's password
    - For the current user: **"passwd"**
    - For another user: **sudo passwd 7even"**

- "usermod -aG"
    - This command is used to add an existing user to one or more supplementary groups
    - e.g **"sudo usermod -aG devops 7even"**. This command ads the usr *7even* to the group *devops*
    - You can add a user to multiple groups by separating the groups with commas
    - e.g **"sudo usermod -aG devops,cloud 7even"**. This adds the user *7even* to the groups *devops* and *cloud*

- "usermod -s"
    - This command changes the default login shell of a user
    - e.g **"sudo usermod -s /bin/bash 7even"**

- "usermod -l"
    - This command is used to change a user's login name/username
    - e.g **"sudo usermod -l 7even user1"**. This command changes the login name of *user1* to *7even*

- "userdel"
    - This command is used to remove a user account from the linux system
    - e.g **"sudo userdel 7even"**. This command removes the account entry for the user *7even* but the home dirctory remain

- "userdel -r"
    - This command is used to remove a user account, the user's home directory and mail spool
    - e.g **"sudo userdel -r 7even"**
