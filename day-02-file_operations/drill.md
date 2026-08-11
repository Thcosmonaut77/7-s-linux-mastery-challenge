# File Operation Drill

Create a nested folder structure practice/2026/august in one command, create three empty files 
inside it, copy the folder to a backup location, rename one file, then safely delete only the empty 
directories left behind

## Steps/Commands
- Open terminal
    launch Ubuntu terminal

- Create nested folder structure
    - mkdir -p practice/2026/august

- Create empty files
    - cd practice/2026/august
    - touch file1.txt file2.txt file3.txt

- Copy folder to backup location
    - cp -r ~/practice/2026/august ~/practice/2026/backup

- rename one file
    - mv ~/practice/2026/august/file1.txt ~/practice/2026/august/note1.txt

- Safely delete empty directories
    - cd ~/practice/2026/
    - mv august/ backup/ ~ 
    - cd ~
    - rm -r practice/