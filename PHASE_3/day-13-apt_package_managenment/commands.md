# APT Package Management

- "apt update"
    - This command refreshes the local package index from the configured software repositories
    - It does not install or updates packages 
    - e.g **"sudo apt update"**

- "apt upgrade"
    - This command installs newer versions of currently installed packages
    - It normally avoids removing installed packages or installing additional packages 
    - e.g **"sudo apt update"**

- "apt full-upgrade"
    - This command upgrades packages while being willing to remove or install packages if necessary to resolve dependenciy changes
    - This makes it more aggressive tha **"apt upgrade"**
    - e.g **"sudo apt full-upgrade"**

- "apt install"
    - This command installs software packages
    - e.g **"sudo apt install nginx"**

- "apt remove"
    - This command uninstalls a package while generally leaving its system-wide configuration files behind
    - e.g **"sudo apt remove nginx"**

- "apt purge"
    - This command removes a package and its package-managed configuration files
    - e.g **"sudo apt purge nginx"**

- "apt autoremove"
    - This command removes packages that were automatically installed as dependencies and are no longer required 
    - e.g **"sudo apt autoremove"** after removing software

- "apt search"
    - This command searches the package repository for packages matching a search term 
    - e.g **"apt search nginx"**

- "apt show"
    - This command displays detailed information about a package
    - e.g **"apt show nginx"**

- "dpkg -l / dpkg -L"
    - The first command, **"dpkg -l"**, lists packages known to the local Debian Package database
    - e.g **"dpkg -l nginx"**
    - The second command, **"dpkg -L"**, lists all files installed by a particular package.
    - e.g **"dpkg -L nginx"**