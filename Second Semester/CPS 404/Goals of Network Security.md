
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
## **Database Security**

Database security encompasses a variety of measures aimed at safeguarding a Database Management System (DBMS) from cyber threats, data breaches, and unauthorized access. It ensures the **integrity**, **availability**, and **confidentiality** of data.

---

## **Network Security Overview**

### **Basic Principles (as covered in lectures):**

* **Authentication and Authorization**: Verifies user identity and assigns appropriate access levels.
* **Encryption**: Secures data both in transit and at rest using techniques such as **MD5** and **SHA1**.
* **Access Control**: Implements controls like **Role-Based Access Control (RBAC)** and **Mandatory Access Control (MAC)** to restrict user actions based on permissions.
* **Backup and Recovery**: Ensures data availability and continuity in case of failure or loss.
* **SQL Injection Prevention**: Utilizes **parameterized queries** to protect against injection attacks.

---

## **Security Control and Auditing**

Security controls are protective measures put in place to **prevent**, **detect**, or **respond** to security risks.

### **Types of Security Controls:**

* **Administrative Controls**: Includes policies, procedures, and end-user training (e.g., **Security Awareness Training**).
* **Technical Controls**: Involves software and hardware mechanisms such as **firewalls**, **antivirus**, and **IDS**.
* **Physical Controls**: Includes tangible barriers like **biometric locks**, **security cameras**, and **access cards**.

### **Categories of Security Controls:**

* **Preventive**: Block attacks before they occur (e.g., firewalls).
* **Detective**: Identify and alert administrators of incidents (e.g., Intrusion Detection Systems).
* **Corrective**: Restore systems after a breach (e.g., backup recovery tools).
* **Deterrent**: Discourage attacks through visible security (e.g., CCTV).
* **Compensatory**: Alternative controls used when primary ones aren’t feasible.

---

### **Security Auditing**

Security auditing involves the systematic evaluation of security practices and controls to ensure compliance and identify vulnerabilities.

#### **Key Activities:**

* **Log Review**: Regular inspection of system and access logs.
* **Vulnerability Assessment**: Scanning systems for known security weaknesses.
* **Penetration Testing**: Simulating cyberattacks to evaluate defense mechanisms.
* **Compliance Checks**: Verifying adherence to regulatory standards and policies.

---

## **Digital Forensics**

Digital forensics is the process of identifying, preserving, analyzing, and presenting digital evidence in a way that is **legally admissible**. It is vital in the investigation of cybercrime, fraud, insider threats, and data breaches.

### **Steps in a Forensic Investigation:**

1. **Identify** – Locate potential evidence.
2. **Preserve** – Secure and protect data from tampering.
3. **Analyze** – Examine evidence to understand the incident.
4. **Document** – Record findings and processes for legal and technical review.

### **Types of Digital Forensics:**

* **Computer Forensics**: Analysis of desktops, laptops, and storage devices.
* **Network Forensics**: Monitoring and analysis of network traffic, logs, and router data.
* **Mobile Device Forensics**: Recovery and analysis of data from phones, tablets, and SIM cards.
* **Cloud Forensics**: Investigation of data stored or processed in cloud environments, including server logs and VM snapshots.

> ✅ *Note: Explore tools used in digital forensics and study real-life case examples for deeper understanding.*

---

