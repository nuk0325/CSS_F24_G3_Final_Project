# Initial Scan

### 1. Scan process (suppose after compiling plugin)

#### 1. Start Nessus
```
sudo systemctl start nessusd
```
<img width="1392" alt="start_nessus" src="https://github.com/user-attachments/assets/d6290460-889f-40aa-ba73-07683b23ac00">

#### 2. Go to the “https://localhost:8834” website

<img width="1392" alt="create_new_scan" src="https://github.com/user-attachments/assets/864d15da-b48f-47da-b00b-c520d41cbb3b">

#### 3. Check IP address
```
ip address
```
<img width="1392" alt="check_ip_address" src="https://github.com/user-attachments/assets/1f5c3552-c617-4e2a-84e7-ae5e4e9a6646">

#### 4. Create new scan
* Select scan type

<img width="1392" alt="select_scan_type" src="https://github.com/user-attachments/assets/4aa486b3-32db-4e5b-86a5-157ed776ec64">

* set target

<img width="1392" alt="target_setting" src="https://github.com/user-attachments/assets/978ed27e-429b-4d93-a28e-b46389b1675e">

* set port

<img width="1392" alt="port_setting" src="https://github.com/user-attachments/assets/9f73c4a2-44ec-4e6c-9995-fc1609a655fa">

* check TCP & UDP (to scan deeply)

<img width="1392" alt="TCP UDP" src="https://github.com/user-attachments/assets/8b324ae0-c29c-40d0-a99e-4241bb729634">

#### 5. Launch the scan

<img width="1392" alt="scan_launching" src="https://github.com/user-attachments/assets/569626e1-dffb-42c6-bd24-582db9ea0aa0">

---

### 2. Analyzation of the initial scan
#### 1. Scan Result

<img width="1004" alt="initial_scan_report" src="https://github.com/user-attachments/assets/fa5dfe9d-4960-4b58-9563-33bbe23085ad">

#### 2. Vulnerabilities

* Node.js
  * A vulnerability was detected in the Node.js version included by default in Kali Linux. It may be an outdated version or a specific version maintained for OS stability, which can result in vulnerabilities being present.

* SSL
  * A vulnerability was detected in the SSL certificate present in Kali Linux, indicating it is not trusted. If the certificate is issued by the server itself, Nessus may classify it as untrusted.

* Intel Media SDK
  * A vulnerability was detected in the video processing library included by default in Kali Linux. It may be an outdated version that has not been updated to the latest release.

* OpenJDK 8
  * A vulnerability was detected in the OpenJDK included in the default Java runtime environment of Kali Linux. This can occur if it has not been updated to the latest version.


