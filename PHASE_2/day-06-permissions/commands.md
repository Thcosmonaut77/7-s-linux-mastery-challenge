# Reading & Setting Permissions

- "ls -l"
    - The **"ls"** with the **"-l"** flag is a command used to display files and directories in long listing format, including their permissions, ownership, size, and modification time.
    - e.g **"ls -l"**. This command will display the list of files and directories in the current working directory, including the permissions and ownerships attached to each file or directory
    - Using this command, the first character on each line represents the type of file;
        - -:    Regular file
        - d:    Directory
        - l:    Symbolic link
        - c:    Character device
        - b:    Block device
        - s:    Socket
        - p:    Named pipe
    - The second to tenth character represents permision bits for User, Group, and Others, group in threes
    - Each entity(user, group, or others) have three permission bits assigned to them (r: read, w: write, x: execute, -: no permission)
    - These permission bits can be represented with numbers (r: 4, w: 2, x: 1, -: no permission)

- "chmod (relative +/-)
    - The **"chmod"** command is used to add or remove permissions with out replacing existing permissions
    - By specifying if it is the user, group, others, or all of them, then use the relative **"+ or -"** to add *r, w, or x* permissions
    - e.g **"chmod u+x script.sh"**. This command adds the execute permission to the user for *script.sh*
        - u:    user
        - g:    group
        - o:    others
        - a:    all
        - +:    add(operator)
        - -:    remove(operator)
        - r:    read
        - w:    write
        - x:    execute

- "chmod (assignment =)
    - The **"chmod"** command with the **"="** operator sets permissions exactly as specified, rather than adding or removing permissions without affecting other permissions
    - e.g **"chmod g=rw file2.txt"**. This command sets the permission for the user to be read and write for file2.txt
    - You can also specify the permissions of more that just one entity with a single command
    - e.g **"chmod u=rw, g=rw, o=r file.txt"**. This command acts on the persmissions of the user, group, and others for *file.txt*

- "chmod 755 (octal)"
    - The **"chmod"** command can also be used with numbers to represent the permission bits
        - r:    4
        - w:    2
        - x:    1
    - e.g **"chmod 755 file.txt"**. This command will add r, w, and x permissions to the user, r, and x to the group and others.
    - Each number represent the sum of the permission bits you want to apply to user(7), group(5), other(5)
    - This type of permission typically applies to files that everyone should be able to execute nd read but only owner should be able to modify

-   "chmod 644"
    - This permission settings apply to configuration files
    - e.g **"chmod 644 website.conf"**. This command sets the permission setting to read and write for the user, read only for the group and others

- "chmod 600"
    - This permission settings apply to sensitive files
    - e.g **"chmod 600 key.pem"**. This command sets the permission for only the user to read and write

- "chmod -R"
    - The **"chmod"** command with the **"-R"** flag is used to to apply changes to a directory and all its content, including it's subdirectories and files
    - e.g **"chmod -R 755 dir1/"**. This command will change the permission of the dir1 directory to 755, including its subdirectories and files

- "umask"
    - The **"umask"** command is used to set default permissions for new files and directories
    - e.g **"umask"**. This command will display the mask for default permissions, subtract that from 777 and you get the default permission set (umask=022, 777-022 default permission=755)

- "umask -S"
    - The **"umask -S"** command displays the default permission in an easy to understand format
    
- "stat -c '%A %U %G'"
    - The **"stat"** command displays detailed information about a file 
    - The **"-c"** flag specifies the information you want displayed
        - %A:   file permissions is human-readable form 
        - %U:   file owner username
        - %G: file group name
    - e.g **"stat -c '%A %U %G' file.txt"**. This command displays detailed information on the owner of the file, the group, and file permissions in human-readable form