# Network Port Scanning Task

## Objective
Learn to discover open ports on devices in your local network to understand network exposure and basic network reconnaissance skills.

## Tools Used
- **Nmap**: For network port scanning
- **Wireshark** (optional): For packet analysis

## My Local Network
- **IP Address:** 192.168.157.113
- **Subnet Mask:** 255.255.255.0
- **Network Range:** 192.168.157.0/24

## Steps Performed
1. **Installed Nmap** from the official website.
2. **Identified local IP range**: 192.168.157.0/24
3. **Ran TCP SYN scan** using:
   ```sh
   nmap -sS 192.168.157.0/24
   ```
4. **Noted down IP addresses and open ports** found in the scan.
5. **Analyzed services and security risks** for each open port.
6. (Optional) Used Wireshark for deeper packet analysis.

## Nmap Scan Results

### Device: 192.168.1.1
| Port    | Service | Description                  | Security Risk                       |
|---------|---------|------------------------------|-------------------------------------|
| 21/tcp  | FTP     | File Transfer Protocol       | Unencrypted, vulnerable to sniffing |
| 554/tcp | RTSP    | Real Time Streaming Protocol | May expose video streams            |
| 1723/tcp| PPTP    | VPN Protocol                 | Outdated, known vulnerabilities     |

### Device: 192.168.1.24
| Port    | Service | Description                  | Security Risk                       |
|---------|---------|------------------------------|-------------------------------------|
| 21/tcp  | FTP     | File Transfer Protocol       | Unencrypted, vulnerable to sniffing |
| 554/tcp | RTSP    | Real Time Streaming Protocol | May expose video streams            |
| 1723/tcp| PPTP    | VPN Protocol                 | Outdated, known vulnerabilities     |

## Analysis
- **FTP (21/tcp):** Unencrypted protocol, vulnerable to sniffing and credential theft.
- **RTSP (554/tcp):** May expose video streams, potentially leaking sensitive information.
- **PPTP (1723/tcp):** Outdated VPN protocol with known vulnerabilities, not recommended for secure communications.

## Key Concepts
- **Port scanning**: Identifying open ports and services on a network.
- **TCP SYN scan**: A stealthy scan type that sends SYN packets to detect open ports.
- **Network reconnaissance**: Gathering information about devices and services on a network.
- **Security risks**: Open ports can expose services to attacks if not properly secured.

##
## How to Run This Task Yourself
1. Install Nmap from [nmap.org](https://nmap.org/).
2. Find your local IP range (e.g., `ipconfig` on Windows).
3. Run: `nmap -sS <your-network-range>`
4. Review the results and analyze open ports and services.

## References
- [Nmap Documentation](https://nmap.org/book/man.html)
- [Wireshark Documentation](https://www.wireshark.org/docs/)

---

**This repository contains my scan results, analysis for the Cyber Security Internship Task 1.** # cyber-task-1
