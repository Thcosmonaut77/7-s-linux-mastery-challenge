# File Navigation

- "pwd"
    - Translates to "Print Working Directory"
    - Show the current location a user is in the system

- "ls"
    - Translates to "List"
    - Lists files and directories in the current working directory

- "ls -l"
    - Translates to "List with long flag"
    - Lists files and directories in the current working directory in a detailed format
    - Displays files/directories owners amd permissions

- "ls -a"
    - Translates to "List with all flag"
    - Lists all files and directories in the current working directory, incuding hidden files and directories
    - Hidden files and directories begin with a "." 

- "ls -la"
    - Translates to "List with long and all flags"
    - Lists all files and directories in the current working directory with detailed information like owners and permissions

- "ls -lh"
    - Translates to "List with the long and human-readable flags"
    - Lists files in the current working directory with detailed information and sizes that is easier for humans to read and comprehend 

- "cd"
    - Translates to "Change directory"
    - Using it without a flag would take you to the home directory of the current user logged in. e.g "/home/7"
    - Using it with the absolute path will take you to the directory at the end of the path. e.g "/home/7/linux/linux_challenge"

- "cd .."
    - Translates to "Change directory to the one that comes before"
    - This commands will take to the directory that comes before your currrent working directory
    - If you're in "/home/7/linux/linux_challenge", the command will take you to "/home/7/linux"

- "cd ~"
    - Translates to "Change directory to user home"
    - Like "cd", "cd ~" will also take you to the home directory of the user currently logged in the system

- "cd -"
    - Translates to "Change directory to the previous location
    - If you were inside a directory in your home directory, e.g "/home/7/linux", and you change directory to "/etc/ssh", this command will take you back to your linux directory in your home(or anywhere) from the ssh directory in /etc(or your previous location)