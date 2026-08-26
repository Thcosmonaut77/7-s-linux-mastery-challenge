# Persisting Configuration Drill

Add a permanent environment variable and a custom alias to your .bashrc, reload it without 
opening a new terminal, and confirm both persist in a fresh session.

## Steps/Commands
- Open terminal
    - Launch ubuntu terminal

- Add permanent variable and set alias to .bashrc
    - sudo vi ~/.bashrc 
        - add: export VAR="AllahuAkbar"
        - add: alias al='echo "alhamdulillah"'

- Reload without opening new terminal
    - source ~/.bashrc

- Confirm if changes persists
    - echo $VAR
    - al