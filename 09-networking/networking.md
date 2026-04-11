# Networking Commands

1. **`ping google.com`** – Checks connectivity to a remote server.
2. **`ifconfig`** – Displays network interfaces (deprecated, use `ip`).
3. **`ip a`** – Shows IP addresses of network interfaces.
4. **`netstat -tulnp`** – Displays open network connections.
5. **`curl https://example.com`** – Fetches a webpage's content.
6. **`wget https://example.com/file.zip`** – Downloads a file from the internet.
7. **`ss -tulnp`** – Displays socket statistics (modern alternative to netstat)
8. **`traceroute google.com`** – Shows the path packets take to a destination
9. **`nslookup example.com`** – Queries DNS to get domain IP
10. **`dig example.com`** – Advanced DNS lookup tool
11. **`host example.com`** – Resolves domain name to IP address
12. **`ip route`** – Displays routing table
13. **`route -n`** – Shows routing table (older command)
14. **`arp -a`** – Displays ARP table (IP to MAC mapping)
15. **`hostname`** – Displays system hostname
16. **`hostname -I`** – Shows system IP address
17. **`nc -zv hostname 80`** – Checks if a port is open (netcat)
18. **`telnet hostname 80`** – Tests connectivity to a specific port
19. **`nmap localhost`** – Scans open ports on a system
20. **`scp file.txt user@host:/path`** – Securely copy files over network
21. **`rsync -av source/ destination/`** – Sync files between systems
22. **`iftop`** – Displays real-time network bandwidth usage
23. **`tcpdump -i eth0`** – Captures network packets
24. **`curl -I https://example.com`** – Fetch HTTP headers only
25. **`wget -c https://example.com/file.zip`** – Resume interrupted download

## Additional Networking Concepts

### IP Address
- Unique identifier for a device on a network
- Example: 192.168.1.1

### MAC Address
- Hardware address of a network interface
- Used for communication within local network

### DNS (Domain Name System)
- Converts domain names into IP addresses
- Example: google.com → 142.250.x.x

### Port
- Logical endpoint for communication
- Example:
  - 80 → HTTP
  - 443 → HTTPS
  - 22 → SSH

### Protocols
- HTTP/HTTPS → Web communication
- TCP → Reliable communication
- UDP → Fast but less reliable

### Loopback Address
- `127.0.0.1` or `localhost`
- Refers to the local machine

### Public vs Private IP
- Private IP → Used inside local network
- Public IP → Used on internet
