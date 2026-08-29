# Text Processing Checkpoint 

- "grep"    
    - This command searches for a specified pattern and prints the lines that match 
    - **"grep"** means **"Global Regular Expression Print"**
    - e.g **"grep "server" file.txt"**. This will search the file for lines that match the search word, *server*

- "grep -r"
    - This command searches for a pattern recursively through directories and their files
    - e.g **"grep -r "PermitRootLogin" /etc/ssh/"**. This will search for the pattern recursively through the ssh directory

- "grep -i"
    - This command performs a case-insensitive search, so it will print out the matching result regardless of the case 
    - e.g **"grep -i "super" file.txt"**. This will print out the match, regarless of lowercase or uppercase characters

- "sort"
    - This command arranges lines of text into a particular order
    - By default, it performs alphabetical sorting 
    - e.g **"sort file.txt"**

- "sort -n"
    - This command performs numeric sorting rather than alphabetical sorting 
    - e.g **"sort -n file.txt"**

- "uniq"
    - This command removes or reports repeated adjacent lines
    - **"uniq"** only detects duplicates that are next to each other
    - e.g **"uniq file.txt"**

- "cut -d',' -f"
    - This command extracts specific sections or fields from each line
    - It is particularly useful for CSV files
        - cut:      extracts parts 
        - -d',':    comma is the delimiter
        - -f:       specifies the field

    - e.g **"cut -d',' -f1 file.csv"**

- "awk '{print$1}'"
    - The **"awk"** command is one of the most powerful text processing tools in Linux
    - It prints the specified field of each line
    - e.g **"awk '{print$7}' employees.txt"**. This command will print out the 7th field of each line in the *employees.txt* file 

- "sed 's/old/new/g'"
    - **"sed"** is a stream editor
    - It is commonly used to search and replace text in a file
    - e.g **"sed 's/super/ultimate/g' file.txt"**. This will find and replace all instances of *super* with *ultimate* in the file
    - By default, it doesn't change the original file, it will only print out the modified result to the terminal

- "pipe chains (|)
    - The **"pipe"** is one of the most important concepts in linux
    - Represented by **"|"**, It takes the standard output of one command and sends it as the standard input of another command
    - e.g **"ls | grep ".txt" "**. **"ls"** produces a list of files, **"grep"** receives that output and keeps only lines containing *.txt*
    
