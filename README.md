# CSS_F24_G3_Final_Project

# Linux System Vulnerability Management and Hardening Project

## Project Overview
This project demonstrates a vulnerability management process on a Linux virtual machine by:
1. Introducing intentional vulnerabilities.
2. Running an initial vulnerability scan with Nessus.
3. Applying various system hardening techniques to mitigate vulnerabilities.
4. Performing a post-hardening scan to assess the effectiveness of our security measures.

This is a school project for educational purposes only and is intended to showcase an understanding of endpoint security, system hardening, and vulnerability assessment tools.

## Table of Contents
- [Project Objectives](#project-objectives)
- [System Requirements](#system-requirements)
- [Setup and Installation](#setup-and-installation)
- [Vulnerability Introduction](#vulnerability-introduction)
- [Initial Vulnerability Scan](#initial-vulnerability-scan)
- [Hardening Techniques](#hardening-techniques)
- [Post-Hardening Scan](#post-hardening-scan)
- [Results](#results)
- [Contributions](#contributions)

## Project Objectives
The main objectives of this project are to:
- Understand and implement a basic vulnerability management lifecycle.
- Learn how to intentionally configure insecure settings and identify the resulting vulnerabilities.
- Apply hardening measures on Linux and evaluate their effectiveness with a vulnerability scanner.

## System Requirements
- **Operating System**: Ubuntu Linux 24.10
- **Vulnerability Scanner**: Nessus Essentials
- **Virtualization Software**: VirtualBox or VMware

## Setup and Installation

### Step 1: Setting Up the VM
1. Install Ubuntu Linux 24.10 on a virtual machine.
2. Configure basic OS settings:
   - Set hostname, create a user account with secure credentials, and configure password policies.
   - Enable the firewall using `ufw`.
3. Install standard software (e.g., OpenSSH, curl) as part of the baseline setup.

### Step 2: Installing Nessus
1. Download Nessus for Ubuntu from [Tenable’s website](https://www.tenable.com/products/nessus).
2. Install Nessus using `dpkg`:
   ```bash
   sudo dpkg -i Nessus-10.8.3-ubuntu1604_amd64.deb
3. Start and enable the Nessus service:
   ```bash
    sudo systemctl start nessusd
    sudo systemctl enable nessusd
4. Complete Nessus registration via the web interface (https://localhost:8834).
## Vulnerability Introduction
To simulate a vulnerable system, we’ll intentionally configure certain security weaknesses, such as:
  -  Open Ports: Enable unnecessary services (e.g., FTP, Telnet).
  -  Weak User Permissions: Create accounts with default permissions.
  -  Insecure Configurations: Disable firewall rules or enforce weak password policies.

## Initial Vulnerability Scan
1. Run an initial Nessus scan to identify baseline vulnerabilities:
    -  Save scan results as .txt or .pdf in /scans/baseline-scan/.
2. Document vulnerabilities in docs/initial-scan/scan-summary.md, including:
    -  A summary of high, medium, and low-severity vulnerabilities.
    -  Relevant CVE numbers and descriptions.
## Hardening Techniques
To mitigate identified vulnerabilities, the following hardening techniques will be applied:

1. User Account Management: Disable guest accounts and remove unnecessary user permissions.
2. Service Management: Disable or remove unused services (e.g., Telnet).
3. Configuration Changes: Apply strict firewall rules and enable secure SSH configurations.
4. System Updates: Install security updates and patch known vulnerabilities.
5. The steps taken and configurations applied are recorded in docs/hardening/os-hardening.md.

## Post-Hardening Scan
After implementing hardening measures:  
1. Run a post-hardening scan with Nessus to assess the effectiveness of the security improvements.
2. Save results to /scans/post-hardening/.
3. Document findings and compare them with the initial scan in docs/post-hardening-analysis.md.
## Results
The post-hardening analysis will include:  
  -  A summary of resolved and remaining vulnerabilities.
  -  Screenshots and data visualizations highlighting improvements.
  -  Conclusions on the impact of the hardening techniques.
## Contributions
Juliana Garza: Project setup and initial VM configuration.  
Sunwook Kang: Vulnerability introduction and initial scan.  
Joshua Orozco: System hardening and configuration.  
Joseph Montez: Post-hardening scan and results analysis.  
## License
This project is for academic purposes only and should not be used for any production environment or unauthorized testing.

## Additional Documentation
1. Initial Setup Steps: docs/initial-setup/initial-os-setup.md
2. Installed Software List: docs/initial-setup/software-list.md
3. Configuration Changes: docs/initial-setup/configuration.md
4. Vulnerability Summary: docs/initial-scan/scan-summary.md
5. Hardening Documentation: docs/hardening/os-hardening.md
6. Post-Hardening Analysis: docs/post-hardening-analysis.md
