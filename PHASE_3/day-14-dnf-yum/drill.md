# DNf?YUM & Alternative Installs Drill

On an Amazon Linux or RHEL box, install a package with dnf, confirm it with rpm -qa, then 
compare the workflow against the equivalent apt steps from Day 13.

## Steps/Commands
- Open Terminal
    - Launch Amazon Linux instance

- Install a package with dnf
    - sudo dnf install nginx

- Confirm package
    - rpm -qa

- Compare workflow
    - DNF and APT are the higher-level package managers responsible for repositories, dependency resolution, installation, updates, and removal.

    RPM and DPKG are the lower-level package systems that work with the actual installed package database and package files.

    For a DevOps/SysAdmin workflow, the practical pattern to remember is:

    Install with the high-level manager → verify with the low-level package database → verify the actual application.