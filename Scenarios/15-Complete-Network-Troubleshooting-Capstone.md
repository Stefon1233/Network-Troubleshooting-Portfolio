# Scenario 15 — Complete Network Troubleshooting Capstone

## Objective

Perform an end-to-end network diagnostic using a structured troubleshooting workflow covering the network interface, IP configuration, default gateway, local connectivity, 
internet connectivity, DNS, routing, TCP services, HTTPS, and TLS.

## Tools Used

- ifconfig
- route
- ping
- dig
- scutil
- traceroute
- netcat (nc)
- curl
- macOS Terminal

## Troubleshooting Scenario

A user reports a general network connectivity problem.

Rather than immediately assuming a DNS, router, or internet problem, the network is tested systematically from the local interface outward to the application layer.

## 1. Network Interface

The active network interface was inspected.

### Result

- Interface: `en0`
- IPv4 Address: `192.168.0.88`
- Interface Status: Active

The computer had an active network interface and valid private IPv4 address.

## 2. Default Gateway

The default route was inspected.

### Result

- Default Gateway: `192.168.0.1`
- Interface: `en0`

A valid route existed for traffic leaving the local network.

## 3. Gateway Connectivity

The local gateway was tested with ICMP.

### Result

- 4 packets transmitted
- 4 packets received
- 0.0% packet loss

The local computer could successfully communicate with the router.

## 4. Internet Connectivity

Cloudflare DNS (`1.1.1.1`) was tested.

### Result

- 4 packets transmitted
- 4 packets received
- 0.0% packet loss
- Average latency approximately 16.5 ms

This confirmed working internet connectivity independent of DNS name resolution.

## 5. DNS Resolution

GitHub was resolved using:

```bash
dig github.com +short
