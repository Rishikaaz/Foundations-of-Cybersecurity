# Networking Basics

## 1. OSI Model (Open Systems Interconnection)
A conceptual framework used to understand network interactions in seven layers.
1. Physical Layer (Layer 1)
   Function: Transmission of raw bit stream over a physical medium. Deals with voltages, pinouts, and cabling specifications.
   PDU: Bits.
   Devices/Tech: Cables (Cat6, Fiber), Hubs, Repeaters, Wi-Fi Radio.
2. Data Link Layer (Layer 2)
   Function: Node-to-node data transfer. Handles physical addressing (MAC), framing, and error detection/correction.
   PDU: Frames.
   Devices/Tech: Switches, Bridges, Ethernet, MAC Addresses.
3. Network Layer (Layer 3)
   Function: Logical addressing and routing. Determines the best path for data to travel across different networks.
   PDU: Packets.
   Devices/Tech: Routers, Layer 3 Switches, IP (IPv4/IPv6), ICMP.
4. Transport Layer (Layer 4)
   Function: End-to-end communication, reliability, flow control, and segmentation. Ensures complete data transfer.
   PDU: Segments (TCP) or Datagrams (UDP).
   Protocols: TCP (Connection-oriented), UDP (Connectionless).
5. Session Layer (Layer 5)
   Function: Establishing, managing, and terminating sessions between applications. Handles authentication and reconnection.
   Examples: NetBIOS, RPC, Sockets.
6. Presentation Layer (Layer 6)
   Function: Data translation, encryption, and compression. Ensures data is in a readable format for the application.
   Examples: SSL/TLS, JPEG, ASCII, GIF.
7. Application Layer (Layer 7)
   Function: Network services for end-user applications. The layer the user interacts with directly.
   Protocols: HTTP, FTP, SMTP, DNS, SSH.

## 2. TCP/IP Protocol Suite
A practical, real-world model that condenses the OSI layers into four. It is the foundation of the Internet.
1. Network Interface Layer (Matches OSI Physical + Data Link)
   Handles hardware interfacing and physical transmission.
   Protocols: Ethernet, Wi-Fi (802.11), ARP (Address Resolution Protocol - maps IP to MAC).
2. Internet Layer (Matches OSI Network)
   Handles logical addressing, routing, and packet fragmentation.
   Protocols: IP (Internet Protocol), ICMP (Ping/Traceroute), IGMP.
3. Transport Layer (Matches OSI Transport)
   TCP (Transmission Control Protocol): Reliable, ordered delivery. Uses a "Three-Way Handshake" (SYN, SYN-ACK, ACK) to establish connection. Slower but guarantees delivery.
   UDP (User Datagram Protocol): Unreliable, connectionless. "Fire and forget". Faster, used for streaming and VoIP.
4. Application Layer (Matches OSI Session + Presentation + Application)
   Contains all higher-level protocols.
   Protocols: HTTP, DNS, DHCP, FTP, SMTP, Telnet.

## 3. DNS & HTTP/HTTPS Deep Dive
*   DNS (Domain Name System)
    Function: Translates human-readable domain names (google.com) into machine-readable IP addresses (142.250.190.46).
    Resolution Process:
     1. Client checks local cache/hosts file.
     2. Queries Recursive Resolver (ISP).
     3. Resolver queries Root Server (.).
     4. Root refers to TLD Server (.com).
     5. TLD refers to Authoritative Name Server (google.com).
     6. IP is returned to client.
    Record Types: A (IPv4), AAAA (IPv6), CNAME (Alias), MX (Mail Exchange), TXT (Verification/SPF).

*   HTTP (HyperText Transfer Protocol)
    Stateless: Each request is independent; the server doesn't "remember" previous requests without cookies.
    Structure: Request (Method, Headers, Body) -> Response (Status Code, Headers, Body).
    Methods: GET (Retrieve resource), POST (Submit data), PUT (Update resource), DELETE (Remove resource).
    Status Codes: 200 (OK), 301 (Moved Permanently), 403 (Forbidden), 404 (Not Found), 500 (Internal Server Error).

*   HTTPS (HTTP Secure)
    Mechanism: HTTP layered over SSL/TLS (Secure Sockets Layer / Transport Layer Security).
    Security: Provides Encryption (confidentiality), Integrity (no tampering), and Authentication (server identity verification via Certificates).
    Handshake: Asymmetric encryption is used to exchange a symmetric key, which is then used for the session.

## 4. IP Addressing, Subnetting, and NAT
*   IP Addressing
    IPv4: 32-bit address, dotted-decimal (e.g., 192.168.1.1). ~4.3 billion addresses.
      Classes: Class A (Huge networks), Class B (Medium), Class C (Small/Home).
      Private Ranges: Non-routable on internet. 10.x.x.x, 172.16.x.x-172.31.x.x, 192.168.x.x.
    IPv6: 128-bit address, hexadecimal (e.g., 2001:0db8::). Created due to IPv4 exhaustion.

*   Subnetting
    Definition: Logically dividing a network into smaller sub-networks.
    Benefits: Reduces broadcast traffic, improves security, organizes hosts.
    CIDR Notation: Classless Inter-Domain Routing. e.g., `/24` means the first 24 bits are the network, leaving 8 bits for hosts (254 usable IPs).
    Calculation: A `/24` mask is `255.255.255.0`. A `/25` splits that in half (128 IPs).

*   NAT (Network Address Translation)
    Function: Modifies network address information in packet headers while in transit.
    SNAT (Static NAT): 1-to-1 mapping (Private IP <-> Public IP).
    PAT (Port Address Translation): Many-to-1 mapping. Most common in homes. Multiple devices (phones, laptops) share one Public IP by using different source ports.
