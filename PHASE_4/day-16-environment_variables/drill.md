# Environment Variable Drill

Set a temporary environment variable, confirm it exists, unset it, then add a directory to your 
PATH for the current session only and prove the shell can now find a script inside it

## Steps/Commands
- Open terminal
    - Launch ubuntu terminal

- Set a temp variable
    - export VAR="Alhamdulillah"

- Confirm existence
    - printenv VAR

- Unset variable
    - unset VAR

- Confirm existence
    - printenv VAR

- Create a directory containing a script
    - mkdir test-scripts.sh
    - vi test-scripts.sh/hello.sh
    - chmod +x test-scripts.sh/hello.sh
    - mv test-scripts.sh/ test-scripts

- Add directory to PATH for current session
    - export PATH="$PATH:$HOME/test-scripts

- Proof shell can find script
    - which hello.sh
    - hello.sh

- Proof PATH change is only for that session
    - Restart terminal
    - hello.sh
    - which hello.sh
    - echo $PATH
    