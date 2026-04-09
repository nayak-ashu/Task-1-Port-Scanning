# Task-1-Port-Scanning
Performed network port scanning using Nmap to identify open ports, analyze services, and assess potential security risks in a local network.


# Task 1: Network Port Scanning & Security Analysis

##  Objective

To perform network reconnaissance on a local network using Nmap, identify open ports and services, and analyze potential security risks associated with exposed services.

---

##  Tools Used

* Nmap (Network Scanner)
* Wireshark (Optional - Packet Analysis)

---

##  Network Information

* Local IP Address: 192.168.29.55
* Network Range: 192.168.29.0/24
* Scan Type: TCP SYN Scan (Stealth Scan)

---

##  Methodology

1. Identified local IP and subnet using `ifconfig`
2. Derived network range (192.168.29.0/24)
3. Performed TCP SYN scan using:

   ```
   sudo nmap -sS -vv -T4 192.168.29.0/24 -oN result.txt
   ```
4. Discovered active hosts and open ports
5. Mapped ports to corresponding services
6. Analyzed potential security risks

---

##  Scan Results

| IP Address   | Open Port | Service | State |
| ------------ | --------- | ------- | ----- |
| 192.168.29.1 | 80        | HTTP    | Open  |
| 192.168.29.1 | 443       | HTTPS   | Open  |
| 192.168.29.1 | 22        | SSH     | Open  |

*(Replace with your actual results)*

---

##  Analysis of Findings

### 1. HTTP (Port 80)

* Used for web communication
* Transmits data in plaintext

 Risk:

* Susceptible to Man-in-the-Middle (MITM) attacks
* Sensitive data exposure

---

### 2. HTTPS (Port 443)

* Secure web communication using encryption

 Risk:

* Misconfigured SSL/TLS can lead to vulnerabilities

---

### 3. SSH (Port 22)

* Used for remote login

 Risk:

* Brute-force attacks
* Unauthorized remote access if weak credentials are used

---

##  Overall Security Risks

* Open ports increase attack surface
* Unnecessary services may be exploited
* Weak authentication can lead to compromise

---

##  Mitigation Strategies

* Close unused ports
* Use firewall to restrict access
* Implement strong passwords and authentication
* Enable intrusion detection systems (IDS)
* Regularly update and patch services

---

##  Evidence

<img width="1920" height="891" alt="image" src="https://github.com/user-attachments/assets/97b2df4e-30ba-48f8-b97e-5d553d40af25" />


---

##  Conclusion

This task provided hands-on experience in network reconnaissance and port scanning. It helped in identifying exposed services and understanding their associated risks, which is essential for both attackers and defenders in cybersecurity.


---

## Key Learning

* Practical use of Nmap for scanning
* Understanding TCP SYN scan
* Identifying and analyzing open ports
* Basic network security assessment
