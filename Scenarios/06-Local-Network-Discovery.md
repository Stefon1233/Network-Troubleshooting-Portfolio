# Scenario 06 — Local Network Discovery

## Objective

Identify active devices on the local network and compare information obtained from the workstation's ARP table with an active Nmap host discovery scan.

## Environment

- Platform: macOS
- Network Interface: Wi-Fi (`en0`)
- Local IP Address: `192.168.0.88`
- Subnet Mask: `255.255.255.0`
- Network: `192.168.0.0/24`
- Default Gateway: `192.168.0.1`
- Tools Used: `ipconfig`, `arp`, Nmap

## Troubleshooting Process

### 1. Identify Local Network Configuration

The workstation's IPv4 address, subnet mask, and default gateway were identified.

```bash
IP=$(ipconfig getifaddr en0)
MASK=$(ipconfig getoption en0 subnet_mask)
GATEWAY=$(ipconfig getoption en0 router)

echo "IP Address: $IP"
echo "Subnet Mask: $MASK"
echo "Default Gateway: $GATEWAY"
