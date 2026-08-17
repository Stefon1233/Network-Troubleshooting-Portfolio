# Scenario 13 — HTTP, HTTPS, and TLS Troubleshooting

## Objective

Test HTTP and HTTPS connectivity, identify HTTP redirects, verify successful HTTPS communication, measure connection and TLS negotiation times, and inspect the TLS certificate 
presented by a remote web server.

## Tools Used

- curl
- OpenSSL
- macOS Terminal

## Tests Performed

### 1. HTTP Response Test

Tested the HTTP endpoint for GitHub:

```bash
curl -I --max-time 10 http://github.com
