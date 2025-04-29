# Ransomware Traffic Detector

This project is a basic proof-of-concept Python tool that analyzes `.pcap` files (Wireshark packet captures) for potential ransomware behavior. It uses simple rule-based logic to flag suspicious patterns in network activity.

## Features
- Accepts `.pcap` files as input
- Flags common ransomware indicators:
  - Sudden bursts of outbound connections
  - Communication to uncommon ports
  - High-frequency access to SMB shares or known C2 IPs
- Outputs summary of flagged activity

## Skills Demonstrated
- Python scripting
- PCAP parsing using `scapy`
- Network security concepts
- Basic behavioral detection logic

## Example Usage
```bash
$ python detect_ransomware.py --pcap ransomware_sample.pcap
```

## Sample Output
```text
[!] Suspicious burst: 45 outbound connections in 5 seconds to multiple IPs
[!] Potential C2 communication on port 4444
[+] Analysis complete: 2 high-risk events flagged.
```

## Requirements
- Python 3.7+
- scapy (`pip install scapy`)

## Setup
```bash
git clone https://github.com/your-username/ransomware-traffic-detector.git
cd ransomware-traffic-detector
python detect_ransomware.py --help
```

---

**Author:** Bobby Litmon  
**Contact:** litmonbobby@gmail.com
