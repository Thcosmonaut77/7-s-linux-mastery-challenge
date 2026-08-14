# File Inspection

- "cat"
    - Translates to **"Concatenate"**
    - This command is used to display the contents of files in a linux system 
    - e.g **"cat website.conf"**. This will display the content of the website.conf file 
    - You can also display multiple files sequentially, in the order that you put them, separated by a space
    - e.g **"cat file1 app.py index.html"**. This will will display the contents of the three files sequentiall from file1 to index.html
    - You can also concatenate that contents of a file into another file, new or existing 
    - e.g **"cat file.txt > note.txt"**. This command copies the content of file.txt into a new or existing note.txt, if the file exists, this command overwrites the content.
    - You can concatenate the contents of a file into another file without overwriting that file's previous content
    - e.g **"cat note1 >> note2"**. This command concatenates the content of note1 into note2 without overwriting the content in note2. If the file you're appending to does not exist, it will simply create one for you 
    - You can also add the **"-n"** flag to the command to display files with line numbers
    - e.g **"cat -n script.sh"**. This displays the content of script.sh and also display the line numbers as well

- "less"
    - This command is used to view the contents of large files so it does not fllod the terminal 
    - It displays files with scrollable page viewer, and once you're done, just hit **"q"** on your keyboard to exit back to the terminal 
    - e.g **"less /var/log/syslog"**. This displays the content of **"syslog"** in a scrollback view. Content that would otherwise flood the terminal if used with **"cat"**
    - You can also combine some useful flags with the command such as **"-N"** and **"-S"**, which displays the scrollback with line numbers and horizontal scrolling for long lines respectively 
    - e.g **"less -NS /var/log/syslog"**. This displays the content of syslog with a scrollback view that shows line numbers and scrolls horizontally for long lines 
    - While in the less view, there are useful keys to use for navigation
        - [space]/f:                    next page
        - b:                            previous page
        - ↑/↓(up and down arrow keys):  scrolling line by line
        - /[pattern]:                   search forward for a keyword (n - next match)
        - ?[pattern]:                   search backwards
        - g / G:                        top of page / bottom of page
        - q:                            quit

- "head"
    - This is a command that is used to display the first 10 lines of a file 
    - e.g **"head /var/log/syslog"**. This displays only the first 10 lines of the file *syslog*

- "head -n"
    - With the **"-n"** flag, you can control how many lines are displayed
    - e.g **"head -n 1 /var/log/syslog"**. This commands displays only the first line of the file, you can tweak the number of line you wish to display
    - Alternatively, you can use **"head -1 file.txt"**
    - You can also choose to view all lines of the file except for the last lines
    - e.g **"head -n -30 /var/log/syslog"**. This commands displays all the lines of syslog except the last 30 lines

- "tail"
    - The opposite of the **"head"** command
    - This command displays the last 10 lines of a file
    - e.g **"tail /var/log/auth.log"**. This command will display the last 10 lines of the auth.log file 
    - Like head, you can add the **"-n"** flag to the command to control the amount lines displayed
    - e.g **"tail -n 5 /var/log/auth.log"** or **"tail -5 /var/log/auth.log"** will display the last 5 lines of the auth.log file
    - You could also use **"tail -n +5 /var/log/auth.log"** to display the contents of auth.log file from the 5th line to the last line 

- "tail -f"
    - This command displays the content of a file, following it as it grows
    - e.g **"tail -f /var/log/syslog"**. This command display the last 10 lines of a file and gives a live stream of new logs as they are being added to the file
    - **"CTRL C"** to exit livestream mode
    - You can also control the number of lines displayed first before the livestraem activity by adding the **"-n"** flag
    - e.g **"tail -fn 5 /var/log/syslog"**. This command displays the last 5 lines of the syslog file and follows it as it grows
    - You can also follow multiple files as well using the **"-F"** flag
    - e.g **"tail -F auth.log bootstrap.log"**. This displays the last 10 lines of each file and follow them while they grow simultaneously 
    - You can also combine the **"-F"** flag with the **"-n"** flag 
    - e.g **"tail -Fn 5 syslog auth.log"**. This command displays the last five lines of syslog and auth.log while also following them simultaneously

- "wc"
    - This commands counts the lines, words and character count of a file in that order
    - e.g **"wc auth.log"**. This will display the number of lines, words, and character count of the file auth.log

- "wc -l"
    - This command counts only the number of lines in a file
    - The **"wc"** command can be used with other useful flags to display only what is specified
        - **"-l"**: lines only 
        - **"-w"**: words only 
        - **"-c"**: characaters only 

- "file"
    - This command is used to detect the different types of files in the system
    - e.g **"file auth.log"**. This command will tell us what type of file auth.log is 
    - The **"file"** command can be used with the **"wildcard(*)"** flag to classify every file in your current working directory 

- "stat"
    - This command is used to display detailed metadata of files or directories in linux 
    - e.g **"stat file.txt"**. This command displays the detailed metadata of file.txt