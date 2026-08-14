# Paths, Links, & tree structures

- "tree"
    - The **"tree"** command displays directories and files of a specified path or the current working directory in a tree-like visual format
    - The **"tree"** command is installed by default on ubuntu, you will need to install it to use it
    - **"sudo apt install tree"**
    - e.g **"tree"**. This command displays a visual tree-like display of the current working directory 
    - The **"tree"** command can be used with other useful flags for a more specific display
        - -a:       Include hidden files
        - -d:       Directories only
        - -f:       Displays full path
        - --du:     Show file sizes per directory

- "tree -L"
    - The **"tree"** command with the **"-L (Limit Depth)"** flag is a command that is used to display directories and files of a specified path or the current working directory in a tree-like visual format, limited to the number of levels specified
    - e.g **"tree -L 1 /etc/apt"**. This command display only one level of the tree-like visual formant display of /etc/apt

- "ln(hard link)"
    - The **"ln"** command is used to create a second name for the same data, it will not use an extra space and all data remain the same 
    - e.g **"ln /home/trippy/notes.txt /home/trippy/backup_notes.txt"**. This command creates a hard link of notes.txt named backup_notes.txt
    - This command is good for backing up files in the same filesystem

- "ln -s(symbolic link)"
    - The **"ln"** command with the **"-s"** flag is a command used to create symbolic links of files accross filesystems. It creates a pointer file containing the path to the target file 
    - e.g **"ln -s /var/www/site-live site"**. This command creates a symbolic link named *site*, pointing to the actual file which is *site-live*

- "readlink" 
    - The **"readlink"** command shows where a symbolic link is pointing to 
    - e.g **"readlink site"**. This command will display the full path of where the symbolic link is pointing to 

- "realpath"
    - The **"realpath"** command displays the full path of anyfile in your current working directory 
    - e.g **"realpath note1.txt"**. This command will display the absolute path to the file *note1.txt*

- "basename"
    - The **"basename"** command strips the directory part of an absolute path
    - e.g **"basename /var/log/syslog"**. This command will strip away all the directory part of the path and display just the *syslog* file 

- "dirname"
    - Inverse of the **"basename"** command, this command strips away the file part of an absolute path
    - e.g **"dirname /var/log/syslog"**. This command will strip away the file part of the path which is *syslog* and display the directory part of that path which is **"/var/log"**

- "pushd / popd"
    - These commands are used to save and stack directories navigated, and return back up the stack respectively
    - e.g **"pushd /var/log/"**, this saves the home directory and navigate to */var/log*, then **"pushd /etc/apt"**, this then saves */var/log* and navigates to */etc/apt*.
    - To return back up the stack, run **"popd"**. This command will navigate you back up the saved stack one at a time, so if we are at */etc/apt*, running **"popd"** will us back up to our previously stacked navigation, which is */var/log*
    - To view the saved stack, run **"dirs"**

- "ls -lt"
    - The **"ls"** command with the **"-lt"** flag is used to list the content on a specific path or the current directory, sorting its content by the newest at the top with the oldest at the bottom
    - e.g **"ls -lt"**. This command will display the content of the current working directory in the order of newest at the top with the oldest at the bottom.
    - You can also reverse that, having the oldest at the top and the newest at the bottom using **"ls -ltr"**