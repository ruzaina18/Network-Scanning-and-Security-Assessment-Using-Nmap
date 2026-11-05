# Network Scanning and Security Assessment Using Nmap

## Project Overview

This project focuses on performing network scanning and security assessment using **Nmap (Network Mapper)**. The objective is to understand network reconnaissance, identify active hosts, discover open ports, detect running services, and assess potential security risks within an authorized network environment.

The project demonstrates practical network security techniques used to evaluate network exposure and identify areas that may require security improvements.

## Objectives

- Identify active devices within a network.
- Discover open, closed, and filtered ports.
- Detect running services and their versions.
- Perform operating system detection.
- Use Nmap scripting capabilities for additional information gathering.
- Analyze scan results and identify potential security risks.
- Document findings and recommend security improvements.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Nmap | Network scanning and security assessment |
| Windows Command Prompt | Execute Nmap commands |
| Wireshark (Optional) | Network traffic analysis |
| GitHub | Project documentation and evidence |

## Practical Implementation

### 1. Nmap Installation Verification

Verified the Nmap installation and checked its version.

**Command:**
```bash
nmap --version
```

### 2. IP Address Identification

Used the `ipconfig` command to identify the local IPv4 address, subnet mask, and default gateway.

**Command:**
```bash
ipconfig
```

### 3. Host Discovery

Performed host discovery to identify active devices within the authorized local network.

**Command:**
```bash
nmap -sn 192.168.1.0/24
```

**Purpose:**
- Identify active network devices.
- Understand network discovery techniques.
- Determine which hosts respond to discovery probes.

### 4. Basic Port Scanning

Scanned the local machine to identify commonly used TCP ports and determine their states.

**Command:**
```bash
nmap 127.0.0.1
```

**Purpose:**
- Identify open ports.
- Understand exposed network services.
- Examine potential entry points.

### 5. Full TCP Port Scanning

Performed a scan across all 65,535 TCP ports on the local machine.

**Command:**
```bash
nmap -p- 127.0.0.1
```

**Purpose:**
- Identify additional open ports.
- Examine the exposure of network services.
- Obtain a broader view of the TCP port configuration.

### 6. Service Version Detection

Used Nmap to identify services and their version information.

**Command:**
```bash
nmap -sV 127.0.0.1
```

**Purpose:**
- Identify running services.
- Detect service version information.
- Identify potentially outdated services for further investigation.

### 7. Operating System Detection

Attempted to identify the operating system of the target machine using Nmap fingerprinting.

**Command:**
```bash
nmap -O 127.0.0.1
```

**Purpose:**
- Understand operating system fingerprinting.
- Gather additional information about the target system.

### 8. Nmap Default Script Scanning

Used Nmap's scripting engine to execute default NSE scripts against discovered services.

**Command:**
```bash
nmap -sC 127.0.0.1
```

**Purpose:**
- Gather additional service information.
- Perform basic security-related checks.
- Understand automated network assessment techniques.

### 9. Saving Scan Results

Exported scan results into a text file for documentation and analysis.

**Command:**
```bash
nmap -sV -sC 127.0.0.1 -oN nmap_report.txt
```

**Purpose:**
- Maintain scan records.
- Review discovered services.
- Support security assessment documentation.

## Security Assessment

The scan results can be analyzed to identify potential network security concerns.

| Assessment Area | What to Investigate |
|---|---|
| Open Ports | Identify unnecessarily exposed ports |
| Running Services | Determine whether services are required |
| Service Versions | Check for outdated or unsupported versions |
| Remote Access | Review SSH and RDP access restrictions |
| Unencrypted Services | Investigate protocols such as FTP and HTTP |
| Network Exposure | Identify devices and services accessible within the network |

**Note:** Open ports do not automatically indicate vulnerabilities. Further investigation is required to determine actual security risks.

## Key Skills Demonstrated

- Network Reconnaissance
- Host Discovery
- TCP Port Scanning
- Service and Version Detection
- OS Fingerprinting
- Nmap Scripting Engine (NSE)
- Network Security Assessment
- Security Risk Identification
- Technical Documentation
- Basic Security Analysis

## Project Evidence

refer screenshots, nmap report and security finding files.

## Expected Outcomes

- Gained practical experience with Nmap network scanning.
- Understood how to discover active hosts and identify exposed ports.
- Learned to detect running services and their versions.
- Developed an understanding of operating system fingerprinting.
- Practiced interpreting scan results and identifying potential security concerns.
- Improved technical documentation and security reporting skills.

## Conclusion

This project provided hands-on experience with network reconnaissance and basic security assessment using Nmap. It demonstrated how network scanning techniques can help identify active hosts, exposed ports, and running services. The findings can be used to support further investigation and recommend appropriate network security improvements.

## Ethical Considerations

All scanning activities should be conducted only on personally owned systems, authorized lab environments, or networks for which explicit permission has been granted. Unauthorized scanning is not permitted.

---

**Project Category:** Cybersecurity | Network Security | Network Reconnaissance

**Tool Used:** Nmap (Network Mapper)
