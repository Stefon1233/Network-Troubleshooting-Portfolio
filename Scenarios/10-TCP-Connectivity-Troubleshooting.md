# Scenario 10 — TCP Connectivity Troubleshooting

## Objective

Test TCP connectivity to common network services, identify the difference between successful and unsuccessful port connections, and verify HTTPS connectivity using Netcat and 
cURL.

## Environment

- Platform: macOS
- Network Interface: Wi-Fi (`en0`)
- Local Network: `192.168.0.0/24`
- Tools Used: `nc`, `curl`

## Troubleshooting Process

### 1. Test HTTPS Connectivity to GitHub

Netcat was used to test TCP connectivity to GitHub over HTTPS port 443.

```bash
nc -vz github.com 443
