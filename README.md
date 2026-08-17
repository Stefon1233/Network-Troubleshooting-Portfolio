# Network Troubleshooting Portfolio

## Overview

This portfolio demonstrates practical network troubleshooting skills using macOS command-line tools, packet analysis, DNS diagnostics, routing analysis, TCP connectivity 
testing, HTTPS/TLS verification, and structured troubleshooting scenarios.

The project includes 15 documented troubleshooting scenarios with screenshots, packet captures, command output, and supporting results.

## Skills Demonstrated

- TCP/IP troubleshooting
- IPv4 configuration analysis
- Default gateway testing
- DNS troubleshooting
- DHCP analysis
- Routing and traceroute analysis
- Local network discovery
- Wi-Fi and interface diagnostics
- Packet capture and PCAP analysis
- Latency and packet loss testing
- TCP port testing
- Bandwidth and network performance analysis
- DNS record analysis
- HTTP/HTTPS troubleshooting
- TLS certificate inspection
- End-to-end network troubleshooting methodology

## Tools Used

- `ping`
- `traceroute`
- `route`
- `ifconfig`
- `ipconfig`
- `networksetup`
- `scutil`
- `arp`
- `nmap`
- `nslookup`
- `dig`
- `nc`
- `curl`
- `tcpdump`
- `openssl`
- `networkQuality`

## Troubleshooting Scenarios

### 01 — IP Configuration and Connectivity

Verified local IPv4 configuration, subnet mask, default gateway, internet connectivity, DNS resolution, and route availability.

[View Scenario 01](Scenarios/01-IP-Configuration-and-Connectivity.md)

### 02 — DNS Troubleshooting

Tested local and public DNS resolvers, compared DNS responses, validated expected NXDOMAIN behavior, and confirmed internet connectivity independent of DNS.

[View Scenario 02](Scenarios/02-DNS-Troubleshooting.md)

### 03 — Network Port and Service Testing

Used Nmap and HTTP/HTTPS testing to identify open network services and validate application-layer connectivity.

[View Scenario 03](Scenarios/03-Network-Port-and-Service-Testing.md)

### 04 — DHCP Troubleshooting

Inspected DHCP configuration, lease information, assigned IP addressing, gateway, subnet mask, and DNS server information.

[View Scenario 04](Scenarios/04-DHCP-Troubleshooting.md)

### 05 — Routing and Traceroute

Analyzed the routing table, verified the default gateway, and traced network paths through upstream routers.

[View Scenario 05](Scenarios/05-Routing-and-Traceroute.md)

### 06 — Local Network Discovery

Used ARP and Nmap host discovery to identify active systems on the local subnet.

[View Scenario 06](Scenarios/06-Local-Network-Discovery.md)

### 07 — Network Interface and Wi-Fi Diagnostics

Inspected network adapters, Wi-Fi configuration, interface status, IPv4 addressing, and default route selection.

[View Scenario 07](Scenarios/07-Network-Interface-and-WiFi-Diagnostics.md)

### 08 — Packet Capture and Traffic Analysis

Captured live network traffic with tcpdump, created a PCAP file, and analyzed TCP, HTTPS, DNS, and other traffic.

[View Scenario 08](Scenarios/08-Packet-Capture-and-Traffic-Analysis.md)

### 09 — Network Latency and Packet Loss

Compared latency and packet loss between the local gateway, Google DNS, Cloudflare DNS, and GitHub.

[View Scenario 09](Scenarios/09-Network-Latency-and-Packet-Loss.md)

### 10 — TCP Connectivity Troubleshooting

Tested HTTP, HTTPS, and DNS TCP ports and compared successful connections with an intentionally unsuccessful port test.

[View Scenario 10](Scenarios/10-TCP-Connectivity-Troubleshooting.md)

### 11 — Network Performance and Bandwidth Testing

Measured upload/download capacity, network responsiveness, gateway latency, external latency, and packet loss.

[View Scenario 11](Scenarios/11-Network-Performance-and-Bandwidth-Testing.md)

### 12 — DNS Record Analysis

Analyzed A, AAAA, MX, NS, TXT, and CNAME records using `dig`.

[View Scenario 12](Scenarios/12-DNS-Record-Analysis.md)

### 13 — HTTP, HTTPS, and TLS Troubleshooting

Validated HTTP redirects, HTTPS responses, connection timing, TLS negotiation, and certificate information.

[View Scenario 13](Scenarios/13-HTTP-HTTPS-and-TLS-Troubleshooting.md)

### 14 — Network Path and Route Failure Analysis

Compared a healthy routing path with an unreachable destination to isolate where a connectivity failure may occur.

[View Scenario 14](Scenarios/14-Network-Path-and-Route-Failure-Analysis.md)

### 15 — Complete Network Troubleshooting Capstone

Performed an end-to-end diagnostic covering the interface, IP configuration, gateway, local connectivity, internet connectivity, DNS, routing, TCP ports, HTTPS, and TLS.

[View Scenario 15](Scenarios/15-Complete-Network-Troubleshooting-Capstone.md)

## Supporting Evidence

### Screenshots

Each scenario includes supporting screenshots stored under:

```text
Screenshots/
```

### Packet Capture

Scenario 08 includes a PCAP file:

```text
Packet-Captures/08-Packet-Capture-and-Traffic-Analysis/network-capture.pcap
```

### Performance Results

Scenario 11 includes saved network-quality output:

```text
Results/11-Network-Performance-and-Bandwidth-Testing/network-quality.txt
```

## Repository Structure

```text
Network-Troubleshooting-Portfolio/
├── Scenarios/
│   ├── 01-IP-Configuration-and-Connectivity.md
│   ├── 02-DNS-Troubleshooting.md
│   ├── 03-Network-Port-and-Service-Testing.md
│   ├── 04-DHCP-Troubleshooting.md
│   ├── 05-Routing-and-Traceroute.md
│   ├── 06-Local-Network-Discovery.md
│   ├── 07-Network-Interface-and-WiFi-Diagnostics.md
│   ├── 08-Packet-Capture-and-Traffic-Analysis.md
│   ├── 09-Network-Latency-and-Packet-Loss.md
│   ├── 10-TCP-Connectivity-Troubleshooting.md
│   ├── 11-Network-Performance-and-Bandwidth-Testing.md
│   ├── 12-DNS-Record-Analysis.md
│   ├── 13-HTTP-HTTPS-and-TLS-Troubleshooting.md
│   ├── 14-Network-Path-and-Route-Failure-Analysis.md
│   └── 15-Complete-Network-Troubleshooting-Capstone.md
├── Screenshots/
├── Packet-Captures/
├── Results/
├── Commands/
├── LICENSE
└── README.md
```

## Portfolio Value

This project demonstrates the ability to troubleshoot network problems systematically rather than relying on a single diagnostic tool.

The scenarios progress from basic IP configuration and connectivity testing to packet analysis, TCP service testing, TLS inspection, performance analysis, and a complete 
end-to-end troubleshooting capstone.

The troubleshooting process follows a repeatable workflow that can be applied in help desk, technical support, and junior IT networking environments.
# 
Network-Troubleshooting-Portfolio
