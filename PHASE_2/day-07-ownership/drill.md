# Ownership & Special Bits Drill

Create a shared project folder, apply the SGID bit so new files inherit its group, then audit the 
whole system for unexpected SUID binaries.

## Steps/Commands
- Create a shared project folder
    - mkdir -p ./projects/shared_projects
    - ll projects/shared_projects

- Apply SGID
    - sudo chmod g+s projects/shared_projects
    - ll projects/shared_projects

- Create new file
    - touch projects/shared_projects/newfile
    - ll projects/shared_projects

- System-wide audit for SUID
    - find / -perm /4000
    