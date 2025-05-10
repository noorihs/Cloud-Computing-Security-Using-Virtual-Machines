# Cloud-Computing-Security-Using-Virtual-Machines


## Overview

This project aims to simulate a secure private cloud infrastructure using virtual machines (VMs). It explores key security practices in cloud environments by setting up a secure server, configuring a protected network, and testing against common threats using open-source tools.

## Objectives

- Deploy and configure a secure cloud server using Linux-based systems.
- Implement HTTPS, SSH with key-based authentication, and firewall rules.
- Encrypt and securely transfer data across the network.
- Simulate real-world attacks such as Man-in-the-Middle (MITM) using ARP spoofing.
- Perform vulnerability assessment using OpenVAS (GVM).
- Analyze network traffic with Wireshark to observe the impact of security mechanisms.

## Environment Setup

- **Platform:** VMware Workstation
- **Virtual Machines:**
  - `Ubuntu Server`: Cloud service provider
  - `Ubuntu Desktop`: Client/user machine
  - `Kali Linux`: Attacker machine

- **Networking Mode:** Bridged Mode with manual static IP configuration for realistic LAN simulation.

## Key Tools Used

- **OpenSSL**: File encryption, SSL certificate generation.
- **Apache**: Web server setup with HTTPS support.
- **UFW**: Uncomplicated Firewall for service restriction.
- **OpenSSH**: Secure remote shell access with hardened SSH.
- **SCP**: Secure file transfer over SSH.
- **Wireshark**: Network packet inspection.
- **OpenVAS/GVM**: Vulnerability scanning and analysis.

## Main Features & Steps

1. **Secure Server Setup**:
   - Installed Apache, SSH, UFW, and OpenSSL.
   - Configured HTTPS with a self-signed certificate.
   - Restricted ports to HTTP (80), HTTPS (443), and SSH (22).

2. **SSH Hardening**:
   - Created a non-root user.
   - Enabled SSH key authentication.
   - Disabled password logins for increased security.

3. **File Encryption and Transfer**:
   - Encrypted files on the server using AES-256-CBC.
   - Transferred encrypted files using SCP.
   - Decrypted safely on the client side.

4. **MITM Attack Simulation**:
   - Performed ARP spoofing using Kali Linux.
   - Captured and analyzed HTTP vs HTTPS traffic using Wireshark.

5. **Vulnerability Scanning**:
   - Installed and configured OpenVAS.
   - Detected network and server vulnerabilities.

## Important Notes

- **Networking** was configured manually to ensure proper IP addressing across reboots.
- **HTTPS** effectively protected sensitive information against interception.
- **MITM attacks** successfully demonstrated the risks of unencrypted communication.
- **OpenVAS** usage revealed practical challenges in vulnerability scanning and configuration.

## For More Details

For a complete walkthrough, screenshots, detailed configurations, encountered issues, and justifications for every step, **please consult the final report** provided in the `rapport_cloud.pdf` file.

---

**Authors**:  
Yasmine Aibèche, Lyna Racha Bentoumi, Ihsene Noor Khouas, Sara Rahma Sadaoui  
**USTHB - Computer Security Engineering – Cloud Computing Course 2024/2025**
