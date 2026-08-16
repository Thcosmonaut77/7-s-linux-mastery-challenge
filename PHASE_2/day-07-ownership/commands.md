# Ownership & Special Bits

- "chown"
    - The **"chown"** command is used to change the ownership of files and directories in a linux system 
    - e.g **"sudo chown 7even note1.txt"**. This command changes the user owner ship of the file *note1.txt* to the user *7even*
    
- "chown user:group"
    - With the **"chown"** command, you cansimultaneously change user and group ownership
    - e.g **"chown 7even:devops script.sh"**. This command changes the user ownership of the script file to the user *7even* and the group ownership to the group *devops*

- "chown -R"
    - The **"chown"** command with the **"-R"** flag is used to recursively change user/group ownership of directories and everything underneath it, including subdirectories and files
    - e.g **"chown -R ubuntu:ubuntu /home/ubuntu/devops"**. This command changes the user and group ownership of the devops direcetory and every other content within it to ubuntu

- "chgrp"
    - The **"chgrp"** command is used to change the group ownership of files and directories without changing the user ownership
    - e.g **"sudo chgrp ubuntu file1.txt"**. This command changes the group ownership of the file *file1.txt* to the group *ubuntu*

- "chmod u+s (SUID)"
    - **"SUID"** stands for **"set user ID"**
    - It is a special permission that causes an executable program to run with the effective privileges of the file owner, rather than the privileges of the user who executed it 
    - e.g **"sudo chmod u+s myfile"**. This commands will change the *execute - x* permission of the user to *SUID - s*, allowing other users to execute that file using the permission of the file owner 

- "chmod g+s (SGID)"
    - **"SGID"** stands for **"set group ID"**
    - It has two distinct behaviors when applied to either a file or a directory
    - For an executable file, the program executes with the effective group permission associated with the file 
    - e.g **"sudo chmod g+s script.sh"**. This command will change the *execute - x* permission of the group to *SGID -s*, allowing the file to execute with the effective permissions of the group associated with the file 
    - When *SGID* is set on a directory, newly created files and subdirectories generally inherit the directory's group
    - e.g **"sudo chmod g+s projects/"**. This command changes the *execute -x* permission of the group associated with the directory to *SGID - s*.
    - New sub directories and files greated will inherit the group

- "chmod -t (sticky bit)"
    - The sticky bit is used on a directory to prevent users from deleting or renaming files belonging to other users, even if they have write permission on the directory 
    - e.g **"chmod -t shared_project/"**. This command changes the *execute - x* permission of others to *sticky-bit - t* on the directory, turning it into a sticky-bit directory

- "find -perm /4000"
    - This commands searches a specified path for for files or directories with *SUID*
    - e.g **"find /home/projects -perm /4000"**. This command searches the projects directory for any files or directories with the *SUID* permission 
        - /4000:    SUID
        - /2000:    SGID
        - /1000:    sticky-bit
    - You can also specify to search for either files for directories, using the **"-type"** flag
    - e.g **"find /home/projects -perm /2000 -type d"**. This command will search the project directory for for directories with *SGID*

- "getfacl"
    - The **"getfacl"** is a command used to display the Access Control List (ACL) associated with a file or directory 
    - e.g **"getfacl project.txt"**. This command display s detailed file ownership and permission information on the file *project.txt*

- "setfacl -"
    - This command means to set access control list, with the **"-m"** flag to modify the ACL
    - e.g **"setfacl -m u:7even:rw- file.txt"**. This command modifies the ACL of *file.txt* to give the user *7even* read and write permission 