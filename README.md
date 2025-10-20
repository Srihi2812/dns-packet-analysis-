# dns-packet-analysis-
DNS packet capture and analysis using tcpdump and wireshark


This repository contains screenshots showing how DNS queries and ICMP errors were captured on macOS using `tcpdump` and analyzed with Wireshark.

## Contents
- `screenshots/` — Wireshark screenshots
- `README.md` — this file

## Summary
Captured DNS queries (A/AAAA), NXDOMAIN responses, and ICMP unreachable messages using `tcpdump -w`. Analyzed packets in Wireshark to understand DNS resolution and network troubleshooting steps.

## How to reproduce (local)
1. `sudo tcpdump -i en0 -n -s 0 -w dns_icmp.pcap '(udp port 53) or icmp'`
2. In another terminal: `dig @8.8.8.8 www.yummyrecipesforme.com`
3. Stop capture with `Ctrl+C`
4. Open `dns_icmp.pcap` in Wireshark

