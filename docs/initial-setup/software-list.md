# Installed Software List for Ubuntu 24.10

## 1. Browsers
- **Firefox**
  - **Version**: Default installed version with Ubuntu 24.10
  - **Purpose**: Web browsing for documentation, research, and tool downloads.
  - **Installation**:
    ```bash
    sudo apt install firefox -y
    ```

## 2. Productivity Software
- **LibreOffice**
  - **Version**: Latest version from Ubuntu repository
  - **Purpose**: General-purpose productivity software for documentation.
  - **Installation**:
    ```bash
    sudo apt install libreoffice -y
    ```

## 3. Security Tools
- **curl**
  - **Version**: Installed from Ubuntu repository
  - **Purpose**: Data transfer and API testing.
  - **Installation**:
    ```bash
    sudo apt install curl -y
    ```
- **git**
  - **Version**: Latest stable version in Ubuntu repository
  - **Purpose**: Version control for project management.
  - **Installation**:
    ```bash
    sudo apt install git -y
    ```

## 4. Virtualization and Networking Tools
- **net-tools**
  - **Version**: Latest available in repository
  - **Purpose**: Provides commands like `ifconfig` for network interface configurations.
  - **Installation**:
    ```bash
    sudo apt install net-tools -y
    ```

## 5. Nessus Vulnerability Scanner
- **Purpose**: Nessus is used to scan for vulnerabilities on the system.
- **Installation**: Download from Tenable’s website, then install:
  ```bash
  sudo dpkg -i Nessus-10.8.3-ubuntu1404_amd64.deb
  ```
-  **Access**: Nessus can be accessed at https://localhost:8834 after setup.
