# Reading & Setting Permissions Drill

Create a script file and set it to rwxr-xr-x using all three chmod methods (relative, assignment, 
octal) in turn, confirming the result with ls -l after each change.

- Create a script file 
    - touch script.sh

- View file permission
    - ls -l

- Set user permission(relative)
    - chmod u+x script.sh

- View file permission
    - ls -l

- Set group permission(assignment)
    - chmod g=rx script.sh

- View file permission
    - ls -l

- Set others permission(octal)
    - chmod 755 script.sh

- View file permission
    - ls -l