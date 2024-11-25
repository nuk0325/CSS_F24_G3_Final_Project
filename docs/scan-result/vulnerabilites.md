# Vulnerabilities



## 1. Apache



* description

  * A package running alongside Apache2 has vulnerabilities.




* used command

```
sudo apt update
sudo apt install apache2
```



## 2. Node.js



* description

  * The Node.js version included by default in Kali Linux has vulnerabilities.
  
  * An outdated version of Node.js installed with npm has vulnerabilities.




* used command

```
used command
sudo apt install npm -y
```



## 3. IP forwarding enable



* description

  * Resetting all firewall rules also removes traffic filtering rules related to IP forwarding, creating an environment where network traffic can flow freely.




* used command

```
used command
sudo iptables -F
```



## 4. DNS server



* description

  * Disabling the firewall, which filters and limits network traffic, makes it easier for malicious requests to target the DNS server.




* used command

```
used command
sudo ufw disable
```

#### (if you haven’t installed ufw)

```
sudo apt update
sudo apt install ufw -y
sudo ufw disable
```



## 5. DHCP server



* description

  * Disabling the firewall, which filters and limits network traffic, makes it easier for malicious requests to target the DHCP server.




* used command

```
used command
sudo ufw disable
```
#### (if you haven’t installed ufw)
```
sudo apt update
sudo apt install ufw -y
sudo ufw disable
```
