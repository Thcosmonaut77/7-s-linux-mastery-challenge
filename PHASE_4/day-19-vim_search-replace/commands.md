# Vim Navigation & Search/Replace

- "gg / G"
    - These commands move the cursor to different positions in the file 
    - The first one, **"gg"** moves the cursor to the beginning of a file
    - e.g In *Normal Mode*, run **"gg"**. This will take the cursor to the beginning of the file 
    - The second command **"G"**, moves the curso to the end of the file
    - e.g In *Normal Mode*, run **"G"** to go to the last line of the file

- ":10"
    - This will take you directly to line 10 of the file 
    - e.g In *Normal Mode*, run **":70"** to take you to line 70

- "/(search forward)"
    - This command searches forward through a file for a specified pattern
    - e.g In *Normal Mode* run **"/devops"**. This will search forward through the file for the pattern *devops*

- "?(search backward)
    - This command will search backward through a file for a specified pattern
    - e.g In *Normal Mode* run **"?super"**. This will search backwards through the file for the specified pattern

- "n / N"
    - After performing a search using **"/"** & **"?"**, you can use n & N to move betwen matches
    - **"n"** moves to the next occurence of the search
    - **"N"** moves to the previous occurence of the search 

- ":%s/old/new/g"
    - This is one of the most useful Vim commands 
    - It performs a search & replace throughout the entire file
        - **":"**       enters vim's command-line mode
        - **"%"**       apply change to the entire file
        - **"s"**       substitute
        - **"old"**     the text you want to find
        - **"new"**     the replacement text
        - **"g"**       replace all occurences on each line
    - e.g In *Normal Mode* run **":%s/super/ultra/g"**. This will search through the file for all occurences of *super* and replace them with *ultra*

- "dw"
    - This vim command is used to delete from the cursor position through the end of a word
    - e.g In *Normal Mode*, run **"dw"** to delete the word that the cursor is on

-  "x"
    - This vim command is used to delete the character under the cursor
    - e.g In *Normal Mode*, press **"x"** to delete the character that the cursor is under

- "o / O"
    - These commands are used to create a new line and immediately enter *Insert Mode*
    - The first one, **"o"** opens a new line below and puts you into *Insert Mode*
    - The second one, **"O"** opens a new line above and enters *Insert Mode*

- "ZZ"
    - This is a convenient way to save the file and exit 
    - e.g In *Normal Mode*, run **"ZZ"** to save your configurations and exit the text editor 