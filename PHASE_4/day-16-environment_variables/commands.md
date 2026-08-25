# Environment Variables

    An environment variable is a named value stored by the shell and made available to programs running from that shell

- "printenv"
    - This is the command used to display environment variables
    - e.g **"printenv"**. This displays most or all environment variable available to the current process
    - You could also display a specific variable
    - e.g **"printenv LANG"**. This prints out the environment variable for language

- "printenv HOME"
    - This command displays the value of the **"HOME"** environment variable
    - e.g **"printenv HOME"**. This prints out the varaiable of the user's home directory

- "echo $VAR"
    - This command displays the value stored in a shell/environment variable
    - The **"$"** typically replaces the variable specified with its value
    - e.g **"echo $VAR"** or **"echo $HOME"**. This command will print out the values stored in the environment variable specified

- "export"
    - This command makes a shell variable available to child processes
    - e.g **"export VAR"**
    - You could also create and export a varable with a single command
    - e.g **"export VAR="Hello-World""**. This command creates and exports the variable *VAR* having the value *Hello-World*, now programs launched from that shell can access it 

- "unset"
    - This command is used to remove shell variables
    - e.g **"unset VAR"** . This removes the environment variable named *VAR*. So running **"echo"** or **"export"** on it will normally produce a blank result

- "env"
    - This command displays the current environment or runs a command with a modified environment 
    - e.g **"env"**. Like **"printenv"**, this command also displays environment variables 
    - However, this command has an additional capability to run a command with a modified environment 
    - e.g run **"env VAR=Hello bash"** to start a new bash process where **"VAR=Hello"**. Then you run **"env VAR=Hello bash -c 'echo $VAR'"** to test 
    - You can also run a command with a temporary variable
    - e.g **"env APP_ENV=development ./app"**. This makes the **"APP_ENV variable available to *./app*, but does not permanently add it to your shell configuration
    - You can also start a command with an almost empty environment 
    - e.g **"env -i bash"**. This is useful for troubleshooting environment-dependent behaviour

- "source"
    - This command reads and executes commands from a file in the current shell
    - e.g You have **"export CAR="BMW"** in a file named *vars.sh*. Run **"source vars.sh"** or **". vars.sh"**. After that you can run **"echo $CAR"**

- "echo $PATH"
    - This command displays the current *PATH* environment variable
    - The **"PATH"** tells the shell where to look for executable commands
    - e.g **"echo $PATH"**

- "export PATH=$PATH:"
    - This command is related to modifying the *PATH* environment variable
    - However the command is not yet complete, it requires a valid path 
    - e.g **"export PATH=$PATH:/opt/myapp/bin"** or more safely, run **"export PATH="$PATH:/opt/myapp/bin""**.This will keep the existing PATH and add */opt/myapp/bin* to the end. You can now run programs in */opt/myapp/bin* 

- "cat /etc/environment"
    - This command dsiplays the content of the system-wide environment configuration file
    - e.g **"cat /etc/environment"**

