Python Network Sniffer

A lightweight network packet sniffer and live traffic dashboard built with Python and Scapy. This project captures network packets and displays useful information such as source and destination IP addresses, protocols, packet sizes, and real-time traffic statistics.

Developed as a hands-on cybersecurity learning project using Kali Linux.

Features

Basic Packet Sniffer

Capture live network packets.

Display source and destination IP addresses.

Identify TCP, UDP, ICMP, ARP, and other traffic.

Display packet sizes and timestamps.

Show TCP/UDP source and destination ports.

Live Traffic Dashboard

Display total packets captured.

Track total captured bytes.

Calculate approximate packets per second.

Display protocol counts and percentage distribution.

Show the latest 10 captured packets.

Refresh the terminal dashboard automatically.

DNS Analyzer

Identify DNS queries and responses over UDP.

Display queried domain names.

Inspect DNS answer records, including A, AAAA, and CNAME records.

🛠️ Technologies Used

Python 3 — Programming language

Scapy — Packet capture and analysis

Rich — Live terminal dashboard

Kali Linux — Cybersecurity testing environment

UTM — Virtualization environment

Requirements

Python 3

Kali Linux or another compatible Linux environment

Administrator/root privileges for packet capture

A working network connection

Installation


▶️ Usage

1. Basic Packet Sniffer

Run:

sudo python3 sniffer.py

The program displays captured packets with timestamps, protocols, source and destination addresses, and packet sizes.

2. Live Traffic Dashboard

Run:

sudo python3 dashboard.py

The dashboard displays protocol statistics, total captured bytes, packet rates, and recent packet activity.

3. DNS Analyzer

If you have saved the DNS analyzer version separately as dns_sniffer.py, run:

sudo python3 dns_sniffer.py

It displays DNS queries and responses using UDP port 53. This version does not cover every DNS transport, including DNS over HTTPS.

Press Ctrl + C to stop a running capture.

🧪 Testing

Generate test traffic from another terminal:

ping -c 4 1.1.1.1

Generate DNS traffic:

nslookup example.com

Generate HTTP/HTTPS connection traffic:

curl -I https://example.com

Observe the captured packets or updated dashboard in the terminal running the sniffer.

Actual results depend on network connectivity, DNS configuration, virtual network settings, and the interface being monitored.

📂 Project Structure

python-network-sniffer/
├── sniffer.py
├── dashboard.py
├── dns_sniffer.py
├── README.md
└── .gitignore

Note: dns_sniffer.py is optional. Include it only if you have saved the DNS analyzer as a separate file. Adjust the file structure to match the files actually present in your repository.

🔐 Security and Ethical Use

This project is intended for educational purposes and authorized network monitoring.

Capture traffic only on systems and networks you own or have permission to monitor.

Avoid collecting or publishing private packet payloads or sensitive network data.

Do not upload credentials, API keys, private certificates, or sensitive packet captures to GitHub.

🎯 Learning Objectives
