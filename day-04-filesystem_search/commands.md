# Filesystem Search

- "find -name"
    - The **"find"** command with the **"-name"** finds all instances of a file or directory from a given location in the linux system 
    - e.g **"find /home/7 -name note4.txt"**. This command will find and display the path to all instances of note4.txt in 7's home directory 
    - In the case there might be some case sensitive values in the search criteria, you could use the **"-iname"** flag, that way, it will find every instance of your search criteria regardless of the case of the characters

- "find -type"
    - The **"find"** command with the **"-type"** finds all instances of files or directories according to the type specified
    - e.g **"find . -type f"**. This command will find and display the path to all instances of files starting from the current working directory 
    - You could us the command to find a lot more that files
        - f:    file
        - d:    directory
        - l:    symbolic link
        - c:    character device
        - b:    block device
        - s:    socket
        - p:    named pipe

- "find -size"
    - The **"find"** command with the **"-size"** flag finds all instances of files based on their sizes
    - e.g **"find . -size 100G"**. This command finds a file or files that is exactly 100GB(just an example) in your current working directory 
    - Size flags include:
        - c:    Bytes
        - k:    kiloBytes
        - M:    MegaBytes
        - G:    GigaBytes
    - If you don't know the exact size of the file, you can use **"+"** and **"-"** to specify greater than and less than, respectively 
    - e.g **"find . -size +10M"**. This command files files greater than 10MB in your current working directory 

- "find -mtime"
    - The **"find"** command with the **"-mtime"** flag 
    finds instances of files based on their "*modification time*", measured in days
    - e.g **"find /var/log -mtime 4"**. This command will display all files that were modified 4 days ago  in the /var/log directory
    - Like with the **"-size"** flag, you can also use the **"+ (greater than)"** or **"- (less than)"** with the number of days
    - e.g **"find /var/log -mtime -1"**. This command will display all the log files that were modified less than 24 hours ago

- "find -perm"
    - The **"find"** command with the **"-perm"** flag finds instances of files based on their permission bits(quickly lookup on permission bits in linux)
    - e.g **"find /home/ubuntu -perm 664"**. This command will find and display files that have **664 - (6:r,w 6:r,w 4:r)** permissions in the ubuntu home directory 

- "locate"
    - The **"locate"** command, like the **"find"** command, also locates all instances of a given pattern. Because it uses a pre-built database of filenames, instantly displaying the output rather than searching each filesystem
    - e.g **"locate note"**. This command will print out the path of all files that have *note* pattern
    - In the case of a case-sensitive search, you can use the **"-i"** flag 
    - e.g **"locate -i note"**. Now even if there are files with uppercase patterns, they would also be displayed

- "updatedb"
    - The **"updatedb"** command compliments the **"locate"** command.
    - Lets say you create new files and you try to use *locate* on them, they might not print out those files. Because the **"locate"** command uses a pre-built database for its searches, the **"updatedb"** updates the database with any new filesystems that have been added
    - e.g **"sudo updatedb"**

- "du"
    - The **"du"** command, translating to *"Disk Usage"*, shows the amount of space files and directories are consuming
    - e.g **"du"**. This command will print out the amount of space that files and directories are consuming in your current working directory 
    - You could specify the file or directory you want to observer
    - e.g **"du /var/log"**. This prints out disk usage information of the *log* directory
    
- "du -sh"
    - The **"du -sh"** command combines two flags, that could be used separately, **"summarize (-s)"** and give a **"human-readable (-h)"** output on the size
    - e.g **"du -sh /home"**. This command will display the disk usage of the home directory and everything in it, is a summarized and human-readable format

- "df -h"
    - Translating to **"Disk Free"** with the **"-h"** flag for *human-readable* output
    - The command is used to show the amount of free and used space on mounted filesystems
    - e.g **"df -h"**. This command displays the amount of free and used spaces on all mounted filesystems
    - You can also check for specific file systems
    - e.g **"df -h /"**. This command will display the amount of free and used space on the filesystem mounted in the **"/"** directory

