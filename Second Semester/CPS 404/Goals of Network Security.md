
## **Definition of Network Security**

Network security is the process of protecting a computer network from internal and external threats. It ensures the confidentiality, integrity, and availability of network resources by identifying potential risks and implementing measures to mitigate them.

---

## **Steps to Implement Network Security**

1. **Identify Assets**

   * Determine what needs protection: company files, data, routers, switches, etc.

2. **Identify Threats**

   * Understand what the assets are being protected from, such as unauthorized access or cyberattacks.

3. **Assess Risk Likelihood**

   * Evaluate how likely each threat is to occur.

4. **Implement Security Measures**

   * Apply cost-effective methods to protect assets.

5. **Continuous Review**

   * Regularly assess the process and improve security when issues arise.

---

## **Detailed Explanation of Each Step**

### 1. **Asset Identification**

Assets may include:

* Network equipment (routers, switches, firewalls)
* Network operational data (routing tables, cabling)
* Intangible resources (bandwidth, network speed)
* User privacy
* Information transmitted over the network

### 2. **Threat Assessment**

Categories of network attacks:

* **Unauthorized Access:** Gaining access to data or systems without permission.
* **Unauthorized Data Manipulation:** Altering or tampering with data maliciously.
* **Denial of Service (DoS):** Preventing legitimate users from accessing network resources.
* **Intrusion Detection Systems (IDS):** Tools to monitor and detect unauthorized access attempts.

### 3. **Risk Assessment**

* Analyze the likelihood and potential impact of each threat.
* Risk categories:
  * Confidentiality
  * Integrity
  * Availability

**Example:** If a network resource is critical and the likelihood of attack is high, its risk level is **Fairly High**.

### 4. **Constructing a Network Security Policy**

A good policy should:

* Clearly state **what is protected** and **why**
* Identify **who is responsible**
* Provide guidelines for resolving **data conflicts**

It must also be **practical** and **enforceable** with current technologies.

---

## **Types of Network Security Policies**

* **Permissive Policy:** Anything not explicitly prohibited is allowed.
* **Restricted Policy:** Only explicitly allowed actions are permitted.

---

## **Key Policy Elements**

1. **Authentication Policy**

   * Enforces trust using password guidelines and remote login rules.

2. **IT and Maintenance Policy**

   * Outlines procedures for internal and external maintenance.

3. **Privacy and Monitoring Policy**

   * Sets expectations for privacy (e.g., email monitoring, keystroke logging).

4. **Availability Statement**

   * Defines expectations for resource uptime and recovery.

---

## 🔐 **CIA Triad in Network Security**

The **CIA Triad** is a foundational model in information security, representing the three key principles necessary to secure data and systems:

---

### 1. **Confidentiality**

* Ensures that information is accessible only to those authorized to have access.
* Involves protecting personal privacy and proprietary data.
* **Loss of confidentiality** occurs when there is **unauthorized disclosure** of information.

---

### 2. **Integrity**

* Protects information from being modified or destroyed in an unauthorized manner.
* Includes guarantees of **authenticity** and **non-repudiation**.
* **Loss of integrity** happens when there is **unauthorized alteration** of data.

---

### 3. **Availability**

* Ensures that authorized users have **reliable and timely access** to information and resources when needed.
* Threats to availability include **system failures**, **Denial-of-Service (DoS) attacks**, and **natural disasters**.
* Loss of availability is the distruption of access to or use of information 
* 
---

## 🔏 **Non-Repudiation**

* A **security measure** that ensures individuals cannot deny their actions or participation in a transaction.
* Prevents parties from denying:
  * Sending a message
  * Signing a contract
  * Performing a specific action

---
In some security field some additional concepts are needed to present a complete picture, two of the most commonly mentioned are: 
- **Authenticity**: property of being genuine and being able to verify and trusted
- **Accountability**: true secure systems are not yet an achievable goal we must be able to trace a security breach to a responsible party. System must keep record of their activities to permit later forensic analysis.  

Implementing A Network Security Policy:
After a security policy has been defined the next step is to implement it. 
1. All stakeholders in the company, including management and endusers, must agree on the security policy. 
2. It is critical to educate users, the affected parities, including management on why security is important.
3. Security does not come for free, implementing security is expensive and often an ongoing expense
4. It is important to management and financial people about the cost and risk analysis, done in coming up with the security policy.
5. Clearly define responsibilities of the various people for the various path of the network and their reporting relationship.

Elements of network design:
1. Firewall
2. Remote access VPN 
3. Intrusion detection
4. security AAA server
5. SSH: Secure Shell
6. Access Control & Access Limiting


---
## Database Security
Database security involves a range of measures to protect DBMS from cyber threats, data breachers and unauthorized access while ensuring data integrity, availability and confidentiality.

network security overview
In lecture note: basic principle of network security

- Authentication and authorization: ensuring only verified users can access the databases and assigning the proper access level

- encryption: protecting data in transit and at rest using encryption techniques like: MD5, SHA1
- Access control: role-based access control RBAC and mandatory-access control MAC to limit user's action based on  permission, 
- Backup and recovery: to maintain availability
- SQL Injection prevention: using parameterize queries to prevent such.

---
security control and auditing
These are safeguards or counter measuers to avoid, detect or minimize security risk.

Types of security controls 
- Administrative: policies, trainings (security awareness training) of end-users
- Technical: Software or hardware mechanism, firewalls
- Physical control: Locking mechanisms such as biometric

Categories of security controls
- Preventive: Prevent an attack before it happens. (e.g Firewall)
- Detective: identify threats and gives admin a notice when detected, IDS (intrusion detection system)
- Corrective: measures to restore a system back after a breach (e.g data recovery tools)
- Deterrent: Discourage attack by using security camera
- Compensatory: Alternative measures when primary controls are not possible

Auditing:
Security Auditing involves evaluating security practices and controls  to ensure compliance and identify vulnerabilities. Regular checking of sytem and access log.
Key activities:
- Log review: regular checking of system and access logs
- Vulnerability assessment: scanning system for known security weakness
- Penetration testing: involves simulating attacks to evaluate security posture
- Compliance checks: ensure adherence to regulatory standards

---

Digital Forensics
It is the process of identifying, presernving, analyzing and preseting digital evidence in a manner that is legally admissible. It plays a crucial role in investigating cyber crime, fraud, insider threat and data breaches.

Steps in foresic investivgation
1. Identify
2. Preserve
3. Analyze
4. Document


Types of digital forensics:
- Computer: Computers, laptops, and storage
- Network 
- Mobile Device
- Cloud