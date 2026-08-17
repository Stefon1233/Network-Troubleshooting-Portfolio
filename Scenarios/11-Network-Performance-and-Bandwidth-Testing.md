# Scenario 11 - Network Performance and Bandwidth Testing

## Objective

Evaluate network performance by measuring internet upload/download capacity, network responsiveness, latency, and packet loss.

## Tools Used

- networkQuality
- ping
- Terminal
- macOS

## Tests Performed

### 1. Network Quality Test

Used the macOS `networkQuality` utility to measure internet connection performance.

Results:

- Upload Capacity: 158.102 Mbps
- Download Capacity: 294.086 Mbps
- Responsiveness: Medium (436 RPM)
- Upload Flows: 20
- Download Flows: 20

The test confirmed substantial available upload and download bandwidth.

### 2. Default Gateway Latency Test

Tested connectivity to the local default gateway:

`192.168.0.1`

Results:

- Packets transmitted: 10
- Packets received: 10
- Packet loss: 0.0%
- Average latency: 2.202 ms

This indicates reliable communication between the computer and local router.

### 3. Cloudflare Latency Test

Tested external connectivity using Cloudflare DNS:

`1.1.1.1`

Results:

- Packets transmitted: 10
- Packets received: 10
- Packet loss: 0.0%
- Average latency: 16.444 ms

### 4. Google DNS Latency Test

Tested external connectivity using Google DNS:

`8.8.8.8`

Results:

- Packets transmitted: 10
- Packets received: 10
- Packet loss: 0.0%
- Average latency: 23.931 ms

## Troubleshooting Analysis

The local gateway responded with very low latency and no packet loss, indicating that the local network connection was functioning normally.

Both external DNS targets also returned all packets successfully with no packet loss. Cloudflare had lower average latency than Google DNS during this test.

The bandwidth test showed strong upload and download capacity. No significant connectivity or packet-loss problem was detected.

## Conclusion

The network connection was operating normally during testing. Local network connectivity, internet connectivity, bandwidth, and packet delivery were successfully verified.

## Evidence

- `Screenshots/11-Network-Performance-and-Bandwidth-Testing/01-Network-Quality.png`
- `Screenshots/11-Network-Performance-and-Bandwidth-Testing/02-Latency-Comparison.png`
- `Results/11-Network-Performance-and-Bandwidth-Testing/network-quality.txt`
