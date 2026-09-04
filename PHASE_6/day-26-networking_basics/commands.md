# Networking Basics

- "ip a"
    - This command displays information about the network interfaces and IP addresses configured on your linux machine
    - It is the modern Linux networking utility and has largely replaced other tools such as *ifconfig*
    - e.g **"ip a"**

- "ip route"
    - This command displays the Linux system's routing table
    - The routing table tells Linux where network traffic should be sent 
    - e.g **"ip route"**

- "ping -c"
    - This command tests whether another machine is reachable over a network
    - The **"-c"** flag specifies how many ICMP echo requests should be sent
    - e.g **"ping -c 4 google.com"**. This command will send 4 ICMP echo requests to google.com

- "curl"
    - This is a powerful command-line tool for transferring data to and from servers
    - it is particularly useful for:
        - HTTP/HTTPS
        - APIs
        - web servers
        - downloading data
        - testing endpoints
        - sending HTTP requests
    - e.g **"curl http://localhost"**

- "curl -I"
    - This command retrieves HTTP response headers only
    - e.g **"curl -I https://example.com"**

- "wget"
    - This command is primarily used for downloading files from the internet 
    - It supports protocols such as:
        - HTTP
        - HTTPS
        - FTP
    - e.g **"wget https://example.com/file.tar.gz"**

- "netstat -tulnp"
    - This command displaysnetwork connections & listening ports, including the processes using these ports
    - e.g **"netstat -tulnp"**

- "ss -tulnp"
    - This command displays information about network sockets
    - It is the modern replacement for many netstat use cases
    - e.g **"ss -tulnp"**

- "hostname"
    - This command displays or changes the system's hostname.
    - The hostname is the name assigned to the computer/server on the network.
    - e.g **"hostname"**

- "hostnamectl"
    - This command is the modern tool for manageing the system hostname on systems using systemd
    - It can display information about:
        - hostname
        - OS
        - kernel
        - architecture
        - machine ID
        - boot ID
    - e.g **"hostnamectl"**