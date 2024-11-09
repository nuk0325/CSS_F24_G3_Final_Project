## OS Setup for Ubuntu 24.10
### 1. Installation and Basic Configuration  
  -  **1.1 Download and Install Ubuntu 24.10 on Virtual Machine**  
    	-  **a. Download the ISO:**
         	-  Download the Ubuntu 24.10 ISO file from Ubuntu releases.  
    	-  **b. Setup the Virtual Machine:**  
       		-  In VirtualBox, created a new VM with the following settings:  
           		-  Type: Linux  
          		-  Version: Ubuntu 24.10 (64-bit)  
        - **c. Run the Installation Wizard:**  
      		-  Select New in the boot menu.  
        	 -  Follow the installation wizard, setting up a hostname (Project) and creating a primary user account.(group3)
          -  Assigned password to user account (project)  
-  **1.2 Configure System Settings**  
    -  **a. Update and Upgrade System:**
      ```bash 
      	sudo apt update && sudo apt upgrade -y
      ``` 
  	-  **b. Set Hostname:**  
     	-  Ensure the hostname is set to ProjectVM:
       ```bash
        	  sudo hostnamectl set-hostname ProjectVM
        ```
  	-  **c. Take Screenshots:**  
     	-  Screenshots were taken throughout the installation process and saved to /docs/initial-setup/screenshots/.  
### 2. System Settings Changes  
-  **2.1 Disable Guest Accounts**  
  	-  **a. Edit GDM Configuration:**  
     	-  Open GDM config file:
        ```bash 
       		  sudo nano /etc/gdm3/custom.conf
        ```  
      	-  Add the following line under [security]:  
          	-  AllowGuest=false  
  	-  **b. Restart GDM:**
      ```bash 
     	  sudo systemctl restart gdm3
      ```
  	-  **c. Documentation:**  
     	-  Configured to restrict guest access for security.
  -  **2.2 Enable and Configure Firewall**  
    	-  **a. Enable UFW Firewall:**
       ``` bash
         sudo ufw enable
       ```
        -  **b. Set Basic Firewall Rules:**  
      		-  Allow SSH, HTTP, and HTTPS traffic:
       ```bash 
          		  sudo ufw allow ssh  
          		  sudo ufw allow http  
          		  sudo ufw allow https
       ```
        -  **c.  Verify status:**
       ```bash
          	  sudo ufw status
       ``` 

### 3. User Permissions  
  -  **a. List All Users:**  
        -  Default users are reviewed with:
     ```bash
          	-  cat /etc/passwd
     ```
  -  **b. Configure Group Memberships:**  
     	-  Ensure no unnecessary users are part of privileged groups. Remove any unneeded users from the sudo group as necessary.
### 4. Export VM and Upload to Shared Folder
