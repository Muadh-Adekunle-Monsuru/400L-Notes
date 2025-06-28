![[22_23.jpeg]]


## **Question One**  

### **(a) Confidentiality, Integrity, and Availability (CIA) in ATM Systems**  
- **Confidentiality:**  
  - **Requirement:** Ensuring that only authorized users (via PIN and card) can access account details.  
  - **Importance:** **High** – Prevents identity theft and financial fraud.  

- **Integrity:**  
  - **Requirement:** Ensuring that transaction records are accurate and unaltered (e.g., no unauthorized modifications to account balances).  
  - **Importance:** **High** – Prevents fraud and ensures trust in financial systems.  

- **Availability:**  
  - **Requirement:** Ensuring the ATM is operational when needed (e.g., no downtime due to DDoS attacks).  
  - **Importance:** **Medium-High** – Users rely on 24/7 access for cash withdrawals.  

### **(b) Computer Network Security**  
Computer network security refers to the policies, technologies, and practices designed to protect networks, devices, and data from unauthorized access, misuse, or cyberattacks. It ensures **confidentiality, integrity, and availability (CIA triad)** of information.  

### **(c) Computer Forensics vs. Computer Security**  
- **Computer Forensics:** The process of **identifying, preserving, analyzing, and presenting digital evidence** from computers/networks in a legally admissible manner.  
- **Comparison:**  
  - **Computer Security:** Focuses on **preventing** attacks (e.g., firewalls, encryption).  
  - **Computer Forensics:** Focuses on **investigating** attacks after they occur (e.g., recovering deleted files, tracing hackers).  



## **Question Two**  

### **(a) Ten Challenges of Computer Security**  
1. **Evolving Cyber Threats** (e.g., zero-day exploits).  
2. **Insider Threats** (malicious or negligent employees).  
3. **Weak Passwords & Authentication.**  
4. **Software Vulnerabilities** (unpatched systems).  
5. **Phishing & Social Engineering.**  
6. **Data Leakage & Unauthorized Access.**  
7. **Denial-of-Service (DoS) Attacks.**  
8. **Cloud Security Risks.**  
9. **IoT Device Vulnerabilities.**  
10. **Regulatory Compliance (e.g., GDPR, PCI-DSS).**  

### **(b) Security Concepts & Relationships (Diagram Explanation)**  
**Security Concepts:**  
- **Threats** (e.g., malware) → **Vulnerabilities** (e.g., unpatched software) → **Risks** (potential harm).  
- **Countermeasures** (e.g., firewalls, encryption) mitigate risks.  

**Diagram:**  
```
Threats → Exploit Vulnerabilities → Risks → Countermeasures → Reduced Risk  
```  


## **Question Three**  

### **(a) Security Requirements**  
1. **Configuration Management:**  
   - Ensures systems are securely configured (e.g., disabling unused ports).  
2. **Contingency Planning:**  
   - Disaster recovery plans (e.g., backups, failover systems).  
3. **Incident Response:**  
   - Steps to detect, contain, and recover from breaches.  
4. **Risk Assessment:**  
   - Identifying threats, vulnerabilities, and potential impacts.  

### **(b) Fundamental Security Design Principles**  
1. **Isolation:**  
   - Separating systems to limit breach impact (e.g., network segmentation).  
2. **Encapsulation:**  
   - Restricting access to internal data (e.g., APIs, object-oriented security).  


## **Question Four**  

### **(a) Countermeasure**  
A **countermeasure** is a security control (e.g., firewall, encryption) used to **prevent, detect, or respond** to cyber threats.  

### **(b) Threat Actions Leading to Consequences**  
1. **Unauthorized Disclosure:**  
   - **Attack:** Eavesdropping, phishing.  
2. **Deception:**  
   - **Attack:** Spoofing, man-in-the-middle (MITM).  
3. **Disruption:**  
   - **Attack:** DoS, ransomware.  
4. **Usurpation:**  
   - **Attack:** Malware, privilege escalation.  

## **Question Five**  

### **(a) Vulnerabilities vs. CIA Objectives**  
| **Vulnerability**       | **CIA Impact**          |  
|-------------------------|-------------------------|  
| Weak Encryption         | **Confidentiality**     |  
| Unpatched Software      | **Integrity**           |  
| Single Point of Failure | **Availability**        |  

### **(b) Five Ingredients of Symmetric Encryption**  
1. **Plaintext** (original data).  
2. **Encryption Algorithm** (e.g., AES).  
3. **Secret Key** (shared between sender/receiver).  
4. **Ciphertext** (encrypted data).  
5. **Decryption Algorithm** (reverses encryption).  

### **(c) Three Steps of Computer Security Strategy**  
1. **Prevention** (firewalls, access control).  
2. **Detection** (IDS, SIEM).  
3. **Response** (incident handling, recovery).  

## **Question Six**  

### **(a) Attack Surfaces**  
The **total exposure points** where an attacker can exploit vulnerabilities (e.g., open ports, weak passwords, unsecured APIs).  

### **(b) Attack Tree**  
A **hierarchical model** representing potential attack paths (e.g., root node = attack goal, branches = methods).  

### **(c) Requirements for Secure Symmetric Encryption**  
1. **Strong Key Management** (secure generation, storage, distribution).  
2. **Secure Algorithm** (e.g., AES-256, resistant to brute force).  

---
![[23_24.jpeg]]


### **(d) New Additions for 2023/2024 Session**  
**i. Systems and Services Acquisition**  
- Ensures secure procurement of IT systems (e.g., vendor risk assessment, secure coding standards).  

**ii. System and Communications Protection**  
- Safeguards data in transit (e.g., TLS, VPNs) and at rest (e.g., firewalls, IDS).  

**iii. System and Information Integrity**  
- Ensures accuracy of data (e.g., checksums, anti-malware).  


## **Question Two** **  
**(a) Countermeasure**  
Security controls like firewalls/encryption to mitigate threats.  

**(b) Threat Actions & Consequences**  
- **Unauthorized Disclosure:** Phishing → Data leaks.  
- **Deception:** Spoofing → Fake transactions.  
- **Disruption:** DoS → Service downtime.  
- **Usurpation:** Malware → Unauthorized control.  

---

## **Question Three**  

### **(a) Eight Challenges of Computer Security**  
1. **Zero-Day Exploits** (unpatched vulnerabilities).  
2. **Insider Threats** (employees leaking data).  
3. **Cloud Security Risks** (misconfigured buckets).  
4. **IoT Weaknesses** (default passwords).  
5. **Ransomware Attacks** (data encryption for extortion).  
6. **Regulatory Compliance** (GDPR, CCPA penalties).  
7. **AI-Powered Attacks** (deepfake social engineering).  
8. **Supply Chain Attacks** (compromised vendor software).  

### **(b) Security Concepts & Relationships (Diagram)**  
**Flow:**  
```
Threats (e.g., hackers) → Exploit Vulnerabilities (e.g., weak passwords) → Risks → Countermeasures (e.g., MFA) → Residual Risk  
```  


## **Question Four**  

### **(a) Attack Surfaces**  
- **Definition:** All entry points for attacks (e.g., APIs, USB ports, user inputs).  
- **Examples:**  
  - **Network:** Open ports (e.g., port 22 for SSH).  
  - **Software:** Buffer overflow vulnerabilities.  
  - **Human:** Phishing emails.  

### **(b) Attack Tree**  
- **Hierarchical model** showing attack paths:  
  - **Root Node:** Attack goal (e.g., "Steal ATM credentials").  
  - **Branches:** Methods (e.g., "Skimming device" or "Phishing PIN").  
- **Use Case:** Helps prioritize defenses (e.g., mitigating high-probability branches).  
example
![[Pasted image 20250627121826.png]]
### **(c) Secure Symmetric Encryption Requirements**  
1. **Strong Key Management:**  
   - Use AES-256, rotate keys periodically.  
2. **Secure Algorithm Implementation:**  
   - Avoid deprecated algorithms (e.g., DES).  


## **Question Five**   

### **(a) Security Requirements**  
1. **Configuration Management:**  
   - Documenting system settings (e.g., disabling Telnet).  
2. **Contingency Planning:**  
   - Backup strategies (e.g., 3-2-1 rule: 3 copies, 2 media types, 1 offsite).  
3. **Incident Response:**  
   - **Steps:** Detection → Containment → Eradication → Recovery.  
4. **Risk Assessment:**  
   - **Formula:** **Risk = Threat × Vulnerability × Impact.**  

### **(b) Security Design Principles**  
1. **Isolation:**  
   - **Example:** Virtual LANs (VLANs) to segment networks.  
2. **Encapsulation:**  
   - **Example:** REST APIs hiding database structures.  
---

![[CPS 404 20-21.jpeg]]

### **Question 1**  

#### **(a) Data Encryption**  
**Definition:**  
Data encryption converts plaintext (readable data) into ciphertext (unreadable) using algorithms and keys, ensuring only authorized parties can decode it.  

**Purpose:**  
- Protects sensitive data (e.g., financial records, personal messages).  
- Secures data in transit (e.g., HTTPS) and at rest (e.g., encrypted hard drives).  

**Example:** AES-256 encrypting WhatsApp messages.  

#### **(b) Reasons to Adopt Data Encryption**  
1. **Prevent Data Breaches** (e.g., stolen laptops with encrypted files are useless).  
2. **Regulatory Compliance** (e.g., GDPR, HIPAA require encryption).  
3. **Secure Communications** (e.g., encrypted emails protect business secrets).  
4. **Mitigate Insider Threats** (employees can’t access unauthorized data).  
5. **Protect Financial Transactions** (e.g., encrypted credit card payments).  

#### **(c) Symmetric vs. Asymmetric Encryption**  

| **Feature**          | **Symmetric Encryption**               | **Asymmetric Encryption**             |  
|----------------------|---------------------------------------|---------------------------------------|  
| **Key Type**         | Single shared key                     | Public/private key pair               |  
| **Speed**           | Faster (e.g., AES)                    | Slower (e.g., RSA)                    |  
| **Use Case**        | Bulk data encryption                  | Key exchange, digital signatures      |  
| **Example**         | AES, DES                              | RSA, ECC                              |  


#### **(d) Caesar Cipher Encoding/Decoding**  
**Key:** $C_i = P_i + 5$ (shift each letter 5 positions forward).  

**Plaintext:**  
*"My Director, I am a whistle blower. Chief Alayelola has 5 billion dollars in his Sterling Bank Account"*  

**Encoded Steps:**  
- M → R (M + 5)  
- Y → D (Y wraps around to D)  
- (Space/punctuation unchanged)  

**Encoded Message (Partial):**  
*"RD INJHYJTW, N FR F BNXYQQJ GQTBSJ. HMNJK FQFDJQTQF MFX 5 GNQQNTS ITQFWX NS MNX XYJWQLSL GFSD FHHTSZY"*  

**Decoding:** Reverse the shift ($P_i = C_i - 5$).  

---

#### **(e) Weaknesses of Caesar Cipher**  
1. **Brute-Force Vulnerable:** Only 25 possible shifts (easy to crack).  
2. **No Key Complexity:** Single static key.  
3. **Frequency Analysis:** Letter patterns reveal shifts (e.g., "E" is common).  
4. **No Authentication:** No integrity checks (tampering undetectable).  
5. **Limited to Alphabets:** Fails with numbers/symbols.  

### **Question 3**  

#### **(a) Ethical Hacking & Attack Steps**  
**Ethical Hacking:** Authorized penetration testing to identify vulnerabilities.  

**Unethical Hacker’s Steps:**  
1. **Reconnaissance:** Gather target info (e.g., phishing, OSINT).  
2. **Scanning:** Probe for weaknesses (e.g., Nmap, Nessus).  
3. **Exploitation:** Attack vulnerabilities (e.g., Metasploit).  
4. **Covering Tracks:** Delete logs (e.g., timestomping).  

#### **(b) Hacking Tools**  
1. **Metasploit:** Exploit framework for penetration testing.  
2. **Wireshark:** Network traffic analyzer (for MITM attacks).  
3. **John the Ripper:** Password-cracking tool.  


#### **(c) Algebra of Information Security**  
$$ \text{Info Security} = \text{Confidentiality} + \text{Integrity} + \text{Availability} + \text{Authentication} $$ 
- **Confidentiality:** Encryption (AES).  
- **Integrity:** Checksums/Hashing (SHA-256).  
- **Availability:** DDoS protection (Cloudflare).  
- **Authentication:** MFA (Google Authenticator).  

**Justification:** Combined, these ensure data is *private*, *unaltered*, *accessible*, and *verified*.  


---
![[CPS 404 f.jpeg]]

### **Question Six**
The three core objectives of computer security are:

* **Confidentiality:** Ensuring that sensitive information is accessed only by authorized individuals.
* **Integrity:** Ensuring that data is accurate and has not been tampered with.
* **Availability:** Ensuring that systems and data are accessible when needed.

**Vulnerability Correspondence:**

1. **Confidentiality Vulnerabilities:**

   * Weak access controls (e.g., default passwords).
   * Poor encryption practices.
   * Insecure network protocols (e.g., using HTTP instead of HTTPS).
   * Vulnerabilities here may lead to data leaks, eavesdropping, or unauthorized disclosure.

2. **Integrity Vulnerabilities:**

   * Lack of validation or checksums.
   * Malware that alters or corrupts data.
   * Unauthorized modification due to poor authentication or access control.
   * These vulnerabilities result in altered, forged, or deleted information.

3. **Availability Vulnerabilities:**

   * Denial-of-Service (DoS) attacks.
   * Hardware failures or power outages without backup.
   * Insufficient redundancy or failover mechanisms.
   * These lead to systems being inaccessible to users, disrupting operations.

#### (b) Describe each of the five (5) ingredients of symmetric encryption.


1. **Plaintext:**
   The original readable message or data that needs to be protected.

2. **Encryption Algorithm:**
   A set of procedures that transforms plaintext into ciphertext using a key.

3. **Secret Key:**
   A shared key known only to the sender and receiver used for both encryption and decryption.

4. **Ciphertext:**
   The scrambled and unreadable output from the encryption algorithm applied to the plaintext.

5. **Decryption Algorithm:**
   The reverse process that uses the same key to transform ciphertext back into the original plaintext.

#### (c) Discuss each of the three (3) steps of computer security strategy.


1. **Prevention:**

   * Aim: Stop security breaches before they happen.
   * Methods: Firewalls, access control, encryption, anti-malware tools, and security policies.
   * Example: Only authorized users can access a server through password protection.

2. **Detection:**

   * Aim: Identify security incidents as they occur.
   * Methods: Intrusion Detection Systems (IDS), system and audit logs, monitoring tools.
   * Example: An IDS alerts the admin about suspicious login attempts.

3. **Response/Recovery:**

   * Aim: Mitigate damage and restore normal operations.
   * Methods: Incident response plans, backups, disaster recovery procedures.
   * Example: If ransomware encrypts data, a recent backup can be used to restore files.


---
![[CPS 404 q.jpeg]]

### **Question 4**

#### a)

**i.** *What do you understand by risk assessment in network security?*
Risk assessment is the process of identifying, evaluating, and prioritizing potential threats to a network and determining the impact on assets.

**ii.** *Steps in assessing security implications of an enterprise:*

1. Identify assets
2. Identify threats and vulnerabilities
3. Assess likelihood and impact
4. Evaluate existing controls
5. Determine risk levels
6. Recommend mitigation strategies


#### b) *Physical and technical measures to avoid breakdown of network security infrastructure and systems:*

* **Physical:** Lock server rooms, use surveillance cameras, secure hardware.
* **Technical:** Install firewalls, use encryption, perform regular updates, implement intrusion detection systems (IDS).


#### c) *Explain these security attacks:*

* **Interruption:** Disrupting access or availability (e.g., DoS attack).
* **Interception:** Unauthorized access to data (e.g., packet sniffing).
* **Modification:** Altering data in transit (e.g., tampering with messages).
* **Fabrication:** Inserting false data or impersonation (e.g., spoofing).

### **Question 5**

**i. Social Engineering:** Manipulating people into revealing confidential info.
**ii. Vulnerabilities:** Weaknesses in a system that can be exploited.
**iii. Direct Access Attacks:** Physical access to steal or damage systems.
**iv. Cryptanalysis:** Techniques to break encryption and gain unauthorized access.
**v. Man-in-the-Middle Attack:** Intercepting and possibly altering communication between two parties.


### **Question 6**

**a.** *Digital Forensics:*
The process of identifying, preserving, analyzing, and presenting digital evidence legally.

**b.** *Classification:*

1. Computer forensics
2. Network forensics
3. Mobile device forensics
4. Cloud forensics
5. Database forensics

**c.** *Process of Forensic Investigation:*

1. Identification
2. Preservation
3. Collection
4. Examination
5. Analysis
6. Documentation
7. Presentation

**d.** *Three tools of digital forensics:*

* **FTK:** Comprehensive analysis of digital evidence
* **EnCase:** Disk imaging and investigation
* **Autopsy:** Open-source GUI for analyzing digital artifacts (files, emails, logs)
