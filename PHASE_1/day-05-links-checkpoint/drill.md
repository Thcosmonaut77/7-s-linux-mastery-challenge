# Paths, Links & Tree Structure Drill

CHECKPOINT. Create a symbolic link to a config file, resolve its real path, print a two-level tree 
of /etc, and explain to a peer, in your own words, the difference between a hard link and a symbolic 
link.

- Create a symbolic link to a config file
    - ln -s /etc/sysctl.conf sysctl.conf

- Resolve its real path 
    - readlink sysctl.conf

- Print a two-level tree of /etc
    - tree -L 2 /etc

- Difference between hard link and symbolic link
    - A **Hard link** is like a backup of an original file in the same file system, it duplicates all of the original's content and act as a backup to the file, it persists if the original file gets deleted from the system 
    - A **Symbolic link** is like a pointer to the original file, any modification made reflects on both symbolic link and original file, it could be in a different file system. If the original file gets deleted, the link breaks, making the symbolic link invalid