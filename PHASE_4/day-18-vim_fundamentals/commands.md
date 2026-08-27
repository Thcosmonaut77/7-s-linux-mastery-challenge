# Vim Fundamentals

- "vim <file>"
    - **"vim"** is a text editor in linux
    - The above command opens a file in the *vim text editor*
    - e.g **"vim file.sh"**. This command creates, or open the file in the *vim text editor*

- "i (insert mode)"
    - In the *vim text editor*, the **"i"** key is what switches from *Normal Mode* to *Insert Mode*
    - *Insert Mode* is where you type and edit text
    - e.g Inside the *vim text editor*, press **"i"** to enter insert mode

- "Esc (command mode)"
    - What this does is to return to *Normal Mode*
    - *Normal Mode is used to execute *vim* commands
    - e.g After typing or editing the text, hit the **"Esc"** key to return to *Normal Mode*

- ":w"
    - This is a command in the *vim text editor* that saves the current file
    - e.g After you're done editing and you return to *Normal Mode*, run **":w"** to save changes

- ":q"
    - This command is used to exit the *vim text editor* if no changes were made to the file
    - e.g After viewing the file with the *vim text editor*, if no changes were made, run **":q"** to exit from the text editor

- ":wq / :x"
    - These two *vim* commands both do the same thing, the both save the file, and exit from the text editor
    - e.g After done editing, in *Normal Mode*, run **":wq"**, to *write* and *quit* or you could use **":x"** to save and quit
    - Both perform the same action

- ":q!"
    - This command is used to exit the *vim text editor* without saving any changes made
    - e.g If you make an edit and wish to exit without saving those changes, run **":q!"** to exit without saving 

- "dd"
    - This command is used to delete a line of text in the *vim text editor* *Normal Mode*
    - e.g Place your cursor on the line you wish to delete, using your arrow keys, and the hit the key **"dd"** to delete the line the cursor is on

- "yy / p"
    - These commands are used in the *vim text editor* to *copy* and *paste* respectively
    - e.g Place the cursor on the line you wish to copy and hit **"yy"** to copy that line, the you move the cursor to where you want to paste and press **"p"** to paste

-  "u / Ctrl+r"
    - These *vim* commands are used to *undo* and *redo* changes
    - e.g Supposing you accidentally delete a line using **"dd"**, you could undo that action by pressung **"u"**
    - e.g If you undo something and decide you want the changes back, you could just run **"Ctrl+r"** to redo the previous action before the current state