# Initial Configuration Documentation for Ubuntu 24.10

## 1. Firewall Configuration
- **Firewall Tool**: UFW (Uncomplicated Firewall)
- **Commands**:
  - **Enable Firewall**:
    ```bash
    sudo ufw enable
    ```
  - **Allow SSH**:
    ```bash
    sudo ufw allow ssh
    ```
  - **Allow HTTP and HTTPS Traffic**:
    ```bash
    sudo ufw allow http
    sudo ufw allow https
    ```
- **Verification**:
  - To confirm active rules:
    ```bash
    sudo ufw status
    ```

## 2. User Permissions Configuration
- **Guest Account**: Disabled in `/etc/gdm3/custom.conf`.
- **Configuration**:
  ```ini
  [security]
  AllowGuest=false
