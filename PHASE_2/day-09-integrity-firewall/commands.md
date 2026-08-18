# Integrity, Encryption & Firewalling

- "md5sum"
    - This command calculates the MD5(Message-Digest Algorith 5) hash of a file or input
    - A *hash* i a fixed-length value generated from data. If the file changes, its hash changes as well
    - e.g **"md5sum script.sh"**. This commands displays the has of the file *script.sh*

- "sha256sum"
    - This command calculates the SHA-256 cryptographic hash
    - SHA-256 is significantly more appropriate that MD5 for modern integrity verification
    - e.g **"sha256sum script.sh"**

- "gpg --gen-key"
    - *gpg* stands for *"GNU Privacy Guard"*, it is an implementation of th OPenPGP standard and can be used for: 
        - Encryption
        - Decryption
        - Digital signatures
        - Key management 
        - Identity verification
    - e.g **"gpg --gen-key"**. This command creates a public and private key for you after prompting you for *Real name, Email address, and Passphrase.
    - You can view the key using **"gpg --list-keys"**
    - You can share the public key but always protect the private key

- "gpg --encrypt"
    - This command encrypts a file using a recipient's public key 
    - e.g **"gpg --encrypt file.txt"**. This command will prompt for a recepient User ID before encrypting the file 
    - You could also pass in the recepient ID in the same command using the --recipient or -r flag
    - e.g **"gpg -e -r 7 file.txt"**. This command encrypts file.txt using the User ID , *7*
    - You can also combine encryption with a digital signature, this prompts for passphrase
    - e.g **"gpg -e -s -r 7 note.txt"**

- "gpg --decrypt"
    - This decrypts an encrypted GPG file 
    - e.g **"gpg -d file.txt.gpg"**. This command will decrypt the file and display the content according to the command being used
    - Another useful option is to output the content of the encripted file to a new file without displaying it on the terminal, using the **"-o"** flag
    - e.g **"gpg -o file.txt -d file.gpg"**. This command will decrypt the contents of *file.gpg* into *file.txt*

- "chattr +i"
    - Translates to change **"file attributes"**, It modifies filesystem attributes that provide additional controls beyond normal Linux permissions
    - The **"+i"** attribute means *"immutable"*. With this attribute, the file cannot be normally modified or removed, even if normal permissions allow that 
    - e.g **"sudo chattr +i important.txt"**. After setting this, even *sudo rm -f important.txt* will not be able to delete the file, nor will the file be able to be modified the normal way 
    - To reverse it, use the **"-i"** attribute

- "lsattr"
    - The **"lsattr"** command displays filesystem attributes assigned to files, it is particularly useful for checking attributes set using **"chattr"**
    - e.g **"lsattr file.txt"**. This command displays the attributes assigned to file.txt
        - i:    immutable
        - a:    append-only
        - A:    don't update access time
        - d:    no dump
        - s:    synchronous updates

- "ufw enable"
    - UFW stands for **"Uncomplicated Firewall"**
    - It is a user-friendly interface for managing Linux's firewall functionality, commonly used on Ubuntu systems 
    - e.g **"sudo ufw enable"**. This command activates and enable firewall

- "ufw allow"
    - This command is used to create a firewall rule allowing a specified network traffic
    - e.g **"sudo ufw allow ssh"**. This activates the ssh port(22) and enables it automatically on startup

- "ufw status"
    - This command is used to check the ports opened in the firewall
    - e.g **"sudo ufw status"**

NOTE:   To delete a firewall, first run **sudo ufw status numbered"** the you delete the port using the number. e.g **"sudo ufw delete 2"**