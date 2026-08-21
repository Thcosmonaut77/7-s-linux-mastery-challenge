# Groups & Access Circles

- "groupadd"
    - This command is used to create a nw group in linux
    - A group is a collection of users that can share permissions to files, directories, and other resources
    - e.g **"sudo groupadd devops"**. This command creates the group *devops*
    - You can verify with the command **"getent group devops"**

- "groupdel"
    - This comand is used to delete existing groups in linux
    - e.g **"sudo groupdel devops"**. This command deletes the existing group *devops*

- "gpasswd -a"
    - This command is used to add users to groups
    - e.g **"sudo gpasswd -a 7even devops"**. This command adds the user *7even* to the group *devops*

- "gpasswd -d"
    - This command is used to remove users from groups
    - e.g **"sudo gpasswd -d 7even devops"**. This command removes the user *7even* from the group *devops*

- "getent group"
    - This command is used to retrieve group information from the system's configured database
    - e.g **"getent group"**. This command displays the available group entries
    - You could queryt for a specific group by specifying the name of the group 
    - e.g **"getent group devops"**

- "getent passwd"
    - This command is used to display user account information from the system's configured user databases
    - e.g **"getent passwd"**
    - To query for a specific user, you just add the username to the command
    - e.g **"getent passwd 7even"

- "groups"
    - This command displays the groups in which the current user is a member of 
    - e.g **"groups"**
    - You can check for another user as well
    - e.g **"groups 7even"**

- "id -Gn"
    - This command displays the name of groups associated to a user
    - e.g **"id -Gn"**
    - For another user:
    - e.g **"id -Gn 7even"**

- "newgrp"
    - This command changes the effective primary group of your current shell session
    - This is particularly useful after changing group membership when you want the new group membership to reflect without logging out and back in 
    - **"newgrp devops"**. suppose you add yourself to a new group (devops), the current shell may not immediately reflect. Running the above command will activate the changes 

- "cat /etc/group"
    - This command displays the content of the */etc/group* file.
    - The file contains locat group account information
    - e.g **"cat /etc/group"**