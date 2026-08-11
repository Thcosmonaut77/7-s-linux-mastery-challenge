# File Operation

- "mkdir"
    - Translates to **"Make Directory"**
    - It is used to create folders in linux
    - Folders are called directories in linux
    - e.g **"mkdir projects"**, this creates a directory named projects
    - You can create multiple files by spearating them with a space. e.g **"mkdir projects budgets equipments"**, this creates three different directories in the same working diretory

- "mkdir -p"
    - Translates to **"Make Directory with the parent flag"**
    - It is used to create folder structures in linux 
    - e.g **"mkdir -p projects/budgets/buildings"**, this command creates directories, each nested in the one before it. So buildings would be a directory inside budgets, and budgets would be inside projects
    - You can create an entire path from your home directory as well. e.g **"mkdir -p ~/projects/budgets/buildings/terraces/smart_terraces"**. 

- "touch"
    - It is a command used to create an empty file in linux
    - it can also be used to update the timestamp of an existing file
    - It the file exists, using the touch command will not delete the contents of the file(if any), it will just update its timestamp
    - e.g **"touch index.html"**. This creates a file in your current working directory
    - You could also create multiple files with the same command. e.g **"touch index.html styles.css app.js"**. This creates three different files in your current working directory 

- "cp"
    - Translates to **"Copy"** 
    - This command copies files or empty directories from one location to another in the linux system 
    - e.g **"cp file.txt /home/ubuntu/devops"**. This copies file.txt from its current location to the devops directory.
    - You could also reference the full path. e.g **"/home/ubuntu/notes/file.txt /home/ubuntu/devops"**. This works especially if your current working directory is not notes
    - You can also copy the contents of a file into a new file, creating the file in the process
    - e.g let's say in your current working directory, you have only file.txt. **"cp file.txt backup.txt"**. This copies the contents of file.txt, create the file backup.txt and put the contents of file.txt in it
    - You can also copy multiple files to a single location. e.g **"cp file1.txt file2.txt file3.txt /home/ubuntu/cloud/notes"**

- "cp -r"
    - Translates to **"Copy with the Recursive flag"**
    - This command is used to copy a directory that has content inside it 
    - Let's say you have a directory named *"website"*, and inside it is everything required for the website deployment. You want to copy this directory and all its structures to another location. e.g **"cp -r website /var/www"**. This copies all the content of the website directory(and the directory itself) to /var/www

- "mv"
    - Translates to **"Move"**
    - This command is used to move files or directories to other locations in the system 
    - e.g You have one file in your current working director, and you want it moved to another location **"mv file.txt ~/home/ubuntu/notes"**. This moves file.txt to the note directory in your user home 
    - This commands is also used to rename files or directories in the same directory. e.g **"mv file.txt note.txt"**. This renames file.txt into note.txt

- "rm"
    - Translates to **"remove"**
    - This command is used to delete files. e.g **"rm file1.txt"**. This deletes file1.txt from the current working directory 
    - You can also delete multiple files by separating them with a space.
    - e.g **"rm file1.txt file2.txt file3.txt"**. This deletes all three files
    - When you delete a file in linux, there is no recycle bin, files are permanently deleted. Use responsible

- "rm -r"
    - Translates to **"Remove with the Recursive flag"**
    - This command is used to delete a directory that has content in it
    - e.g **"rm -r projects/"**. This deletes the project directory with all other files or directories that are in it

- "rm -rf"
    - Translates to **"Remove with the Recursive and Force flags"**
    - This is a command that needs to be carefully studied and understood so you know why you should not use it unless absolutely necesary
    - This commands forces the recursive deletion of a directory with everything inside it. It will not prompt for confirmation and even attempts to delete even when normal protective measures would have stopped it 
    - e.g **"rm -rf projects/"**. This deletes the project directory, and everything in it 
    - Be very careful with this command

- "rmdir"
    - Translates to **"Remove Directory"**
    - This command is used to delete empty directories in a linux system 
    - The command would typically fail if the directory has any content in it 
    - e.g **"rmdir empty_directory"**. This deletes the directory, but only if it is empty 