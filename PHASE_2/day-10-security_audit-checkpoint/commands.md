# Security Checkpoint & Audit

- "find / -perm /4000 (SUID audit)"
    - This command searches the entire filesystem for files that have SUID(Set User ID) permission bit set 
    - SUID is represented by the numeric permission bit 4000
    - When an executable has SUID set, it runs with the permissions of the file's owner, rather than the permissions of the user executing it.
    - The command **"find / -perm /4000"** searches the entire file system based on permission, filtered to files or directory that have the SUID permission bit 
    - A better audit version is **"sudo find / -perm /4000 -type f 2>/dev/null"**. This command uses the sudo privilege, giving access to protected directories, *-type f* limits the results to regular files and *2>/dev/null* hides permission-denied errors

- "last"
    - **"last"** is a command that displays login history. It displays information about previous user logins and logouts
    - e.g **"last"**. This displays information about previous user logins and logouts
    - You could check details on a specific user by adding their username to the **"last"** command
    - e.g **"last 7even"**. This will display previous login and logout details of the user *7even*
    - You can decide to specify the number of records you want to display. 
    - e.g **"last -10"**. This command will display the last 10 login records

- "lastlog"
    - **"lastlog"** displays the most recent login for users on the system
    - Unlike **"last"** which shows login history, **"lastlog"** focuses on the last login for each account 
    - e.g **"lastlog"**
    - You can check for a specific user by using the **"-u"** flag followed by the username
    - e.g **"lastlog -u 7even"**

- "w"
    - This command shows the users that are currently logged into the system and what they are doing 
    - It also displays system uptime ad load information
    - e.g **"w"**
    - You can check for a specific user by indicating the username
    - e.g **"w 7even"**

- "who"
    - This command shows the users that are currently loggen in the system, it is similar to **"w"**, but it provides less information
    - e.g **"who"**
    - You can view boot time and all login information using the **"-b"** and **"-a"** flag respectively 

- "groups"
    - This  command displays the groups that a user belongs to 
    - e.g **"groups"**. This display the  groups that the current user belongs to 
    - You can check for another user
    - e.g **"groups 7even"**

- "passwd"
    - This command is used to change or setup a user's password
    - For your account, you run: **"passwd"**.This command will change or setup the password of the current user
    - For another account, you run **"sudo passwd 7even"**. This will change or setup the password or the user *7even*
    - You can use the **"passwd"** command with some useful flags:
        - -l:   locks account password
        - -u:   unlocks account password
        - -d:   deletes account password
        - -S:   checks password status

- "chage -l"    
    - This command displays the password-aging information of a user
    - e.g **"sudo chage -l 7even"**. This command will display the password age information of the user *7even*

- "lastb"
    - This command displays failed login attempts
    - e.g **"sudo lastb"**
    - You can check for specific users
    - e.g **"sudo lastb 7even"**

- "history | grep sudo"
    - This command searches your shell history for commands containing the word *sudo*
    - e.g **"history | grep sudo"**. This will search your shell history and print out all commands containing the word *sudo*. You can try other commands as well
    - For a better search, you can make the search case-insensitive by using the **"-i"** flag
    - e.g **"history | grep -i apt"**. This will run a case insenstitive search that prints out commands containing *apt*
    