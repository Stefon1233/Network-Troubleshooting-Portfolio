# Scenario 14 — Network Path and Route Failure Analysis

## Objective

Troubleshoot network path and routing problems by comparing a working local gateway, a reachable internet destination, and an unreachable destination.

## Tools Used

- ping
- traceroute
- route
- macOS Terminal

## Troubleshooting Scenario

A user reports that their network connection is working, but a specific remote destination cannot be reached.

The goal is to determine whether the problem exists on the local network, at the default gateway, along the upstream route, or at the destination.

## 1. Default Route Verification

The system's default network route was inspected using:

```bash
route -n get default | grep -E "gateway:|interface:"

