# Networking Basics Drill

Identify your machine's IP address and default gateway, test connectivity to a public host, fetch a 
URL's headers only, and list every port currently listening

## Steps/Commands
- Open terminal
    - launch ubuntu terminal

- Identify machine IP
    - hostname -I

- Identify default gateway
    - ip route

- Test connectivity to public host 
    - ping -c 4 google.com

- Fetch a URL's headers only 
    - curl -I https://google.com

- List every port currentlt listening 
    - netstat -tulnp