# Scenario 07 — Network Interface and Wi-Fi Diagnostics

## Objective

Inspect the workstation's network interfaces and Wi-Fi configuration to verify that the active network adapter is enabled, properly configured, and being used for the default 
network route.

## Environment

- Platform: macOS
- Active Interface: Wi-Fi (`en0`)
- IPv4 Address: `192.168.0.88`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.0.1`
- Wi-Fi Status: On
- Interface Status: Active
- Tools Used: `networksetup`, `ifconfig`, `ipconfig`, `route`

## Troubleshooting Process

### 1. Identify Available Network Interfaces

The available network hardware interfaces were inspected using:

```bash
networksetup -listallhardwareports
