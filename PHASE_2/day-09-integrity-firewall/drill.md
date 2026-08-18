# Integrity, Encryption & Firewalling Drill

Generate a SHA-256 checksum for a downloaded file to verify its integrity, make a file immutable 
with chattr, then open only port 22 and port 443 on the firewall.

## Steps/Command
- Open terminal
    - Launch Ubuntu terminal

- Generate SHA-256 of a file
    - sha256sum note.gpg

- Make a file immutable
    - sudo chattr +i note.gpg

- Open port 22 and 443
    - sudo ufw enable
    - sudo ufw allow ssh
    - sudo ufw allow https
    - sudo ufw status