# Network Commands Cheat Sheet

Quick reference for common Windows networking commands used throughout my Network Troubleshooting Portfolio.

---

## IP Configuration

### View Basic IP Configuration

```cmd
ipconfig
```

Displays the computer's IP address, subnet mask, and default gateway.

### View Detailed Network Configuration

```cmd
ipconfig /all
```

Displays detailed information about network adapters, including:

* IPv4 address
* Subnet mask
* Default gateway
* DNS servers
* DHCP status
* MAC address

### Release DHCP Address

```cmd
ipconfig /release
```

Releases the current IP address received from DHCP.

### Renew DHCP Address

```cmd
ipconfig /renew
```

Requests a new IP address from the DHCP server.

### Flush DNS Cache

```cmd
ipconfig /flushdns
```

Clears cached DNS records. Useful when troubleshooting DNS resolution problems.

---

## Ping

### Test Local TCP/IP

```cmd
ping 127.0.0.1
```

Tests whether the local TCP/IP stack is functioning.

### Test Default Gateway

```cmd
ping <gateway-IP>
```

Example:

```cmd
ping 192.168.1.1
```

Tests connectivity between the computer and the local router/default gateway.

### Test Internet Connectivity

```cmd
ping 8.8.8.8
```

Tests external connectivity without depending on DNS name resolution.

### Test DNS and Internet Connectivity

```cmd
ping google.com
```

Tests whether a domain name can be resolved and whether the destination responds.

---

## DNS Lookup

```cmd
nslookup google.com
```

Queries DNS to determine the IP address associated with a domain.

Useful for diagnosing DNS resolution problems.

---

## Traceroute

```cmd
tracert google.com
```

Displays the network path packets take to reach a destination.

Useful for identifying where connectivity problems may occur between the local network and destination.

---

## ARP Table

```cmd
arp -a
```

Displays IP addresses and their associated physical/MAC addresses stored in the ARP cache.

Useful when investigating devices on the local network or possible IP addressing issues.

---

## Network Connections

```cmd
netstat
```

Displays active network connections.

Additional useful command:

```cmd
netstat -ano
```

Displays active connections, listening ports, and process IDs.

---

# Basic Troubleshooting Order

When a computer cannot reach the internet, test connectivity in this order:

```cmd
ping 127.0.0.1
ping <default-gateway>
ping 8.8.8.8
ping google.com
```

### Interpreting Results

**127.0.0.1 fails**

* Investigate the local TCP/IP/network configuration.

**Default gateway fails**

* Investigate the network adapter, Wi-Fi connection, Ethernet cable, or router connection.

**8.8.8.8 fails**

* Local networking may work, but external internet connectivity needs investigation.

**8.8.8.8 works but google.com fails**

* Investigate DNS.

**Everything succeeds**

* Basic network connectivity and DNS resolution are functioning.

---

# Commands Used in This Portfolio

| Command              | Purpose                             |
| -------------------- | ----------------------------------- |
| `ipconfig`           | View IP configuration               |
| `ipconfig /all`      | View detailed network configuration |
| `ipconfig /release`  | Release DHCP address                |
| `ipconfig /renew`    | Renew DHCP address                  |
| `ipconfig /flushdns` | Clear DNS cache                     |
| `ping`               | Test connectivity                   |
| `nslookup`           | Test DNS resolution                 |
| `tracert`            | Trace network path                  |
| `arp -a`             | View ARP cache                      |
| `netstat`            | View network connections            |

---

## Skills Demonstrated

* TCP/IP
* DNS
* DHCP
* IP Addressing
* Network Diagnostics
* Windows Command Line
* Network Troubleshooting
