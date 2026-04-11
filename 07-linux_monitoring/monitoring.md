# Linux System Monitoring

## Introduction to System Monitoring
Monitoring system resources is essential to ensure optimal performance, detect issues, and troubleshoot problems in Linux. Various tools allow us to monitor CPU, memory, disk usage, network activity, and running processes.

## Index of Commands Covered

### CPU and Memory Monitoring
- `top` – Real-time system monitoring
- `htop` – Interactive process viewer (requires installation)
- `vmstat` – Report system performance statistics
- `free -m` – Show memory usage

### Disk Monitoring
- `df -h` – Check disk space usage
- `du -sh /path` – Show disk usage of a specific directory
- `iostat` – Display CPU and disk I/O statistics

### Network Monitoring
- `ifconfig` – Show network interfaces (deprecated, use `ip a`)
- `ip a` – Show network interface details
- `netstat -tulnp` – Show active connections and listening ports
- `ss -tulnp` – Alternative to `netstat` for socket statistics
- `ping hostname` – Test network connectivity
- `traceroute hostname` – Show network path to a host
- `nslookup domain` – Get DNS resolution details

### Log Monitoring
- `tail -f /var/log/syslog` – Live monitoring of system logs
- `journalctl -f` – Live system logs for systemd-based distros
- `dmesg | tail` – View kernel logs

## CPU and Memory Monitoring
### Using `top`
To view real-time CPU and memory usage:
```bash
top
```
Press `q` to quit.

### Using `htop`
A user-friendly alternative:
```bash
htop
```
Use arrow keys to navigate and `F9` to kill processes.

### Using `vmstat`
To check CPU, memory, and I/O stats:
```bash
vmstat 1 5  # Update every 1 sec, show 5 updates
```

### Checking Memory Usage
```bash
free -m
```
Shows free and used memory in megabytes.

## Disk Monitoring
### Using `df`
Check available disk space:
```bash
df -h
```
### Using `du`
Find the size of a directory:
```bash
du -sh /var/log
```
### Using `iostat`
Check disk and CPU usage:
```bash
iostat
```

## Network Monitoring
### Checking Network Interfaces
```bash
ip a  # Show IP addresses and interfaces
```
### Viewing Open Ports and Connections
```bash
netstat -tulnp  # Show listening ports
ss -tulnp  # Alternative to netstat
```
### Testing Connectivity
```bash
ping google.com  # Test internet connection
traceroute google.com  # Trace the path to Google
```
### Checking DNS Resolution
```bash
nslookup example.com
```

## Log Monitoring
### Live Monitoring of System Logs
```bash
tail -f /var/log/syslog  # Follow logs in real-time
journalctl -f  # Systemd logs
```
### Checking Kernel Logs
```bash
dmesg | tail
```

## Process Monitoring
### Using `ps`
```bash
ps aux
```
Shows all running processes

```bash
ps -ef
```
Displays process list in full format

### Using `top` for Process Sorting
Inside `top`:
- Press `P` → Sort by CPU usage
- Press `M` → Sort by memory usage

---

## Load Average
```bash
uptime
```
Shows system load average (1, 5, 15 minutes)

👉 Load indicates how busy the system is

---

## Memory Details
```bash
cat /proc/meminfo
```
Detailed memory information

---

## CPU Information
```bash
lscpu
```
Displays CPU architecture details

---

## Disk and I/O Monitoring Advanced
### Using `iotop`
```bash
iotop
```
Shows real-time disk I/O usage by processes

### Using `lsblk`
```bash
lsblk
```
Lists block devices (disks and partitions)

---

## Network Monitoring Advanced

### Displays real-time network bandwidth usage
### Using `iftop`
```bash
iftop
```

### Using `nload`

### Shows incoming and outgoing traffic
```bash
nload
```

---

## Open Files and Ports

### List open files
```bash
lsof
```

### Check which process is using port 80
```bash
lsof -i :80
```

---

## System Resource Limits

### Shows system limits for user processes
```bash
ulimit -a
```

---

## Background and Foreground Processes

### List background jobs
```bash
jobs
```
### Run job in background
```bash
bg
```
### Bring job to foreground
```bash
fg
```

---

## Process Priority

### Start process with priority
```bash
nice -n 10 command
```
### Change priority of running process
```bash
renice -n 5 -p PID
```
