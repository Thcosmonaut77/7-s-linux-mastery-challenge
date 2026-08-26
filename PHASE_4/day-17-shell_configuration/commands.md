# Persisting Configuration

- "nano ~/.bashrc"
    - This command opens the user's **".bashrc"** configuration file in the **"nano"** text editor
    - e.g **"nano ~/.bashrc"**. This command opens the current user's *.bashrc* configurattion file using the *nano* text editor

- "source ~/.bashrc"
    - This command reads and executes the contents of *.bashrc* in the current shell.
    - The **"Source"** command is important because changes made to *.bashrc* normally don't affect an already running shell until the file is loaded again
    - e.g **"source ~/.bashrc"**

- "cat ~/.bash_profile"
    - This command displays the contents of the user's *.bash_profile*
    - The *.bash_profile is a bash login shell configuration file 
    - e.g **"cat ~/.bash_profile"**

- "sudo nano /etc/environment"
    - This command opens the *environment* file as the root user for editing 
    - e.g **"sudo nano /etc/environment"**

- "sudo nano /etc/bash.bashrc"
    - This command opens the system wide bash configuration file on Debian/Ubuntu systems
    - e.g **"sudo nano /etc/bash.bashrc"**

- "alias"
    - This command displays currently configured ahell aliases
    - e.g **"alias"**
    - You can also create aliases
    - e.g **" alias sa='echo "AllahuAkbar"' "**. This command creates an alias named **"sa"**. If you run it as the command, the result is the command on the right 

- "unalias"
    - This command is used to remove aliases
    - e.g **"unalias sa"**

- "type"
    - This command tells you what kind of command bash think something is
    - This is useful for troubleshooting command resolution
    - e.g **"type ll"**

- "which"
    - This command show the executable that would normally be found through your *PATH*
    - e.g **"which docker"**

- "whereis"
    - This comman locates the binary, source file, and manual pages associated with a command
    - e.g **"whereis ls"**

    