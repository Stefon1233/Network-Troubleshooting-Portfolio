# Scenario 09 — Network Latency and Packet Loss Analysis

## Objective

Test network connectivity, latency, and packet loss between the workstation, local gateway, public DNS servers, and an Internet domain.

## Environment

- Platform: macOS
- Local Gateway: `192.168.0.1`
- Google DNS: `8.8.8.8`
- Cloudflare DNS: `1.1.1.1`
- External Domain: `github.com`
- Tool Used: `ping`

## Troubleshooting Process

### 1. Test Local Gateway

```bash
ping -c 10 192.168.0.1

