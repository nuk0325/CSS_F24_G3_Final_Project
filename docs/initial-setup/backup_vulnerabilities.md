# Backup Vulnerabilities  
*Created to maintain project timeline continuity.*  

---

## Project Context  
During the project, we encountered a challenge where the VM had to be duplicated for a MAC user. Unfortunately, this team member was delayed in sharing their steps to be duplicated on the original system, which delayed the process for the next member. To address this, backup vulnerabilities were introduced into the original system. This allowed the remaining members to continue their tasks through a completed scan of the system with the added vulnerabilities. Meanwhile, the delayed worked independently on their duplicated VM, introducing equivalent vulnerabilities of the same severity to complete their portion of the project.  

This adjustment ensured that the project timeline stayed on track and that each team member could meet their responsibilities.   

---

## Backup Vulnerabilities Added  

### 1. Weak SSH Configuration  
- **Description:** Enabled password-based authentication in SSH.  
- **Command to Introduce:**  
  ```bash
  sudo nano /etc/ssh/sshd_config
  ```
- Set PasswordAuthentication to yes
- **Impact** Increased risk of unauthorized access through brute-force attacks  
### 2. Unpatched Vulnerable Application (Apache2)
- **Description:** Installed an older version of Apache2 with known CVEs
- **Command to Introduce:**
    ```bash
  sudo apt install apache2=2.4.29-1ubuntu4
  ```
- **Impact:** Allowed exploitation of web server vulnerabilities, such as remote code execution.

### 3. Improper File Permissions
- **Description:** Configured world-readable and writable permissions on sensitive directories
- **Command to Introduce:**
    ```bash
  sudo chmod -R 777 /etc
  ```
- **Impact:** Exposed critical system files to potential tampering or unauthorized access.
### 4. Disabled Firewall Rules
- **Description:** Removed critical firewall rules, leaving the system unprotected.
- **Command to Introduce:**
    ```bash
  sudo ufw reset
  sudo ufw disable
  ```
- **Impact:** Allowed unrestricted traffic to and from the VM
### 5. Outdated SSL Configuration
- **Description:** Configured world-readable and writable permissions on sensitive directories
- **Command to Introduce:**
    ```bash
  sudo chmod -R 777 /etc
  ```
- **Impact:** Exposed critical system files to potential tampering or unauthorized access.
### 6. Disable Apparmor
- **Description:** Configured world-readable and writable permissions on sensitive directories
- **Command to Introduce:**
    ```bash
  sudo systemctl stop apparmor
  sudo systemctl disable apparmor
  ```
- **Impact:** Reduced security on application profiles by disabling security modules.
### 7. Set Permissions Incorrectly
- **Description:** Set incorrect permissions on sensitive files like /etc/passwd and /etc/shadow.
- **Command to Introduce:**
    ```bash
    sudo chmod 644 /etc/shadow
    sudo chmod 777 /etc/passwd
    ```
- **Impact:** Exposes critical user data and system integrity to unauthorized access.
### 8. Enable SSH Root Login
- **Description:** Allowed root access over SSH by enabling root login.
- **Command to Introduce:**
    ```bash
    sudo nano /etc/ssh/sshd_config
    # Find the line PermitRootLogin and set it to yes:
    PermitRootLogin yes
    ```
- **Impact:** Increased risk of unauthorized access through SSH with root privileges.
