![[CPS 406 Test.jpeg]]

## (a) Distributed Computing and Its Common Goals (5 Marks)

**Distributed computing** refers to a system where multiple computers work together over a network to achieve a common goal, appearing as a single coherent system to the end-user.

**Common goals of distributed computing:**
1. **Resource sharing** - Allows sharing of hardware, software, and data across networked computers
2. **Concurrency** - Enables multiple processes to run simultaneously on different machines
3. **Scalability** - Systems can be easily expanded by adding more nodes
4. **Fault tolerance** - The system continues functioning even if some components fail
5. **Transparency** - Hides the distributed nature of the system from users

## (b) Why Distributed Computing Over Client-Server (5 Marks)

Distributed computing is preferred over traditional client-server computing because:

1. **Better scalability** - Can handle growth more efficiently by adding more nodes
2. **Improved reliability** - No single point of failure (unlike client-server where server failure cripples system)
3. **Higher performance** - Workload can be distributed across multiple machines
4. **Geographical flexibility** - Components can be located in different physical locations
5. **Cost-effectiveness** - Can utilize existing hardware resources more efficiently
6. **Load balancing** - Work can be dynamically distributed to avoid overload

## (c) 5 Models of Distributed Computing (5 Marks)

1. **Client-Server Model** - Clients request services from servers which provide them
2. **Peer-to-Peer (P2P) Model** - All nodes are equal and can act as both clients and servers
3. **Three-Tier Model** - Separates presentation (client), application logic, and data storage tiers
4. **N-Tier/Multi-Tier Model** - Further divides application into more specialized layers
5. **Cluster Computing** - Groups of similar computers work together as a single system
6. **Grid Computing** - Shares resources across different administrative domains

## (d) Mobile and Wireless Computing Applications (5 Marks)

**a. Fighting Insurgency:**
- Real-time communication between field operatives and command centers
- GPS tracking of personnel and equipment
- Mobile surveillance and reconnaissance using drones with wireless transmission

**b. Emergency Services:**
- Ambulances with mobile access to patient records en route
- Disaster response coordination using mobile devices
- Location-based emergency alerts to citizens' mobile devices

**c. Government:**
- Mobile platforms for citizen services (license renewals, tax payments)
- Wireless-enabled field inspections and reporting
- Emergency broadcast systems to mobile devices

## (f) Network Security Modeling Approaches (5 Marks)

Three approaches to modeling network security:

1. **Perimeter Security Model (Castle Approach)**
   - Focuses on strong outer defenses (firewalls, gateways)
   - Weakness: Vulnerable if perimeter is breached

2. **Layered Security Model (Defense in Depth)**
   - Multiple layers of security controls
   - If one layer fails, others provide protection
   - Includes physical, technical, and administrative controls

3. **Zero Trust Model**
   - "Never trust, always verify" principle
   - Strict identity verification for every access request
   - Micro-segmentation of network resources

**Best Approach:** The **Zero Trust Model** is currently considered the most effective as it addresses modern threats like insider attacks and compromised credentials, though it's more complex to implement. For most organizations, a combination of layered security moving toward zero trust principles is ideal.


---
![[CPS 406 23_24.jpeg]]


## Question 1

### (a) Distributed Computing: Understanding, Goals, Characteristics, Issues and Challenges (8 Marks)

**Understanding:**
Distributed computing is a paradigm where multiple autonomous computers communicate through a network to achieve a common goal. These systems appear as a single coherent system to end-users despite being geographically dispersed.

**Goals:**
1. Resource sharing (hardware, software, data)
2. Improved performance through parallel processing
3. Increased reliability through redundancy
4. Scalability to accommodate growth
5. Cost-effectiveness through resource pooling

**Characteristics:**
1. Concurrency of components
2. Lack of global clock
3. Independent failure of components
4. Heterogeneity of systems
5. Transparency (access, location, migration, etc.)

**Issues and Challenges:**
1. Network latency and bandwidth limitations
2. Security vulnerabilities across multiple nodes
3. Synchronization difficulties
4. Partial failures (some components failing while others work)
5. Complexity in design and maintenance
6. Consistency maintenance across nodes

### (b) Five Models of Distributed Computing (10 Marks)

1. **Client-Server Model:**
   - Centralized servers provide services to multiple clients
   - Clients initiate requests, servers respond
   - Example: Web browsers (clients) and web servers

2. **Peer-to-Peer (P2P) Model:**
   - All nodes have equal capabilities and responsibilities
   - No centralized control
   - Example: File sharing networks like BitTorrent

3. **Three-Tier Architecture:**
   - Presentation tier (user interface)
   - Application/logic tier (business rules)
   - Data tier (database storage)
   - Example: Modern web applications

4. **N-Tier/Multi-Tier Architecture:**
   - Extension of three-tier with more specialized layers
   - Each tier serves specific function and communicates with adjacent tiers
   - Example: Enterprise applications with separate web, application, and database servers

5. **Cluster Computing:**
   - Group of similar computers working together as single system
   - High performance through parallel processing
   - Example: Supercomputers, cloud computing platforms

### (c) Four Impact Areas of Distributed Computing in Society (6 Marks)

1. **Healthcare:**
   - Electronic health records accessible across institutions
   - Telemedicine enabling remote consultations
   - Distributed medical research collaborations

2. **Banking and Finance:**
   - Online banking systems
   - Distributed ledger technology (blockchain)
   - Fraud detection across multiple branches

3. **Education:**
   - E-learning platforms accessible globally
   - Distributed research collaborations
   - Shared educational resources

4. **E-Commerce:**
   - Global online marketplaces
   - Distributed inventory management
   - Personalized recommendations using distributed data

## Question 2

### (a) Network Administrator (1 Mark)

A Network Administrator is an IT professional responsible for maintaining computer networks, ensuring their smooth operation, security, and efficiency within an organization.

### (b) Primary Functions of a Network Administrator (3 Marks)

1. Installing and configuring network hardware and software
2. Monitoring network performance and troubleshooting issues
3. Implementing security measures and managing user access
4. Performing regular backups and disaster recovery planning
5. Maintaining network documentation and policies

### (c) Multinational Company Network Scenario (8 Marks)

**i. Reasons for Network Security:**
- Protection of sensitive company data
- Prevention of financial losses from cyber attacks
- Maintaining business continuity
- Compliance with data protection regulations
- Protecting customer and employee information
- Preserving company reputation

**ii. Company's Hottest Goals:**
- Ensuring secure communication between branches
- Maintaining data consistency across locations
- Implementing uniform security policies
- Achieving regulatory compliance in all countries
- Minimizing downtime across the network

**iii. Potential Network Damages:**
- Data breaches exposing sensitive information
- Ransomware attacks encrypting critical data
- DDoS attacks disrupting operations
- Insider threats from disgruntled employees
- Man-in-the-middle attacks intercepting communications

**iv. Combating Measures:**
- Implement end-to-end encryption for all communications
- Regular security audits and penetration testing
- Employee cybersecurity training programs
- Multi-factor authentication for all systems
- Comprehensive backup and disaster recovery plan
- Network segmentation to limit breach impact

## Question 3

### (a) Five Mobile and Wireless Computing Technologies (6 Marks)

1. **Wi-Fi (IEEE 802.11):**
   - Wireless local area networking technology
   - Enables high-speed internet access within limited range
   - Commonly used in homes, offices, and public hotspots

2. **Bluetooth:**
   - Short-range wireless technology for device connectivity
   - Used for peripherals (headsets, keyboards), file transfers
   - Low energy consumption variants for IoT devices

3. **4G/5G Cellular Networks:**
   - High-speed mobile broadband connectivity
   - Enables mobile internet access anywhere with coverage
   - 5G offers ultra-low latency and higher bandwidth

4. **RFID (Radio Frequency Identification):**
   - Uses electromagnetic fields for automatic identification
   - Applications in inventory management, access control
   - Enables contactless payments and tracking

5. **NFC (Near Field Communication):**
   - Very short-range wireless communication (≤4cm)
   - Used for mobile payments, smart cards
   - Enables quick pairing of devices

### (b) Mobile Computing Security Challenges and Solutions (6 Marks)

1. **Data Leakage:**
   - Challenge: Unsecured apps accessing sensitive data
   - Solution: Implement app sandboxing and permission controls

2. **Unsecured Wi-Fi Networks:**
   - Challenge: Man-in-the-middle attacks on public hotspots
   - Solution: Mandate VPN use on all mobile devices

3. **Device Loss/Theft:**
   - Challenge: Physical access to sensitive data
   - Solution: Full disk encryption and remote wipe capabilities

4. **Malware:**
   - Challenge: Mobile-specific viruses and spyware
   - Solution: Install reputable mobile antivirus software

## Question 4

### (a) Characteristics and Features of Client-Server Computing (6 Marks)

1. **Centralized Management:**
   - Resources and data are managed centrally on servers
   - Simplifies administration and maintenance

2. **Asymmetrical Roles:**
   - Clear distinction between client (requester) and server (provider)
   - Clients initiate sessions, servers await requests

3. **Scalability:**
   - Can handle increasing clients by adding servers
   - Vertical (more powerful servers) and horizontal (more servers) scaling

4. **Transparency:**
   - Clients unaware of server location or implementation details
   - Presents single system image

5. **Message-Based Communication:**
   - Uses well-defined protocols (HTTP, FTP, SMTP)
   - Standardized request-response pattern

6. **Stateless or Stateful:**
   - Stateless servers don't retain client information between requests
   - Stateful servers maintain client context

### (b) Student Portal Development Using 3-Tier Architecture (6 Marks)

**Presentation Tier (Client Tier):**
- Contains: User interface components (web pages, mobile app)
- Technologies: HTML5, CSS, JavaScript, React/Angular/Vue.js
- Responsible for: Displaying information, collecting user input

**Application Tier (Logic Tier):**
- Contains: Business logic, application rules
- Technologies: Node.js, Python (Django/Flask), Java (Spring)
- Responsible for: Processing requests, enforcing business rules

**Data Tier:**
- Contains: Database management system
- Technologies: MySQL, PostgreSQL, MongoDB
- Responsible for: Data storage, retrieval, and integrity

## Question 5

### (a) Computing Concepts (2.5 Marks each)

**i. Mobile Computing:**
Technology that enables transmission of data, voice, and video via wireless devices without needing fixed physical connection, allowing users to compute while mobile.

**ii. Wireless Computing:**
Computer networking that uses wireless data connections between network nodes, eliminating need for wired connections, using technologies like Wi-Fi, Bluetooth, or cellular networks.

**iii. Browser:**
Software application used to access, retrieve, and display content on the World Wide Web, interpreting HTML and other web languages to present web pages to users.

**iv. Firewall:**
Network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules, acting as a barrier between trusted and untrusted networks.

**v. Vulnerability:**
Weakness in a system's design, implementation, or operation that could be exploited to violate the system's security policy, potentially leading to unauthorized access or damage.

## Question 6

### (a) Computer and Network Security (4 Marks)

Computer and network security involves protecting computer systems, networks, and data from theft, damage, or unauthorized access. It encompasses measures to ensure confidentiality (only authorized access), integrity (data isn't altered improperly), and availability (systems are accessible when needed). This field addresses threats like malware, hacking, and data breaches through technologies like firewalls, encryption, and intrusion detection systems.

Effective security requires a layered approach combining technical solutions (antivirus software, encryption), physical protections (secure facilities), and administrative controls (security policies, training). As threats evolve, security measures must continuously adapt to address new vulnerabilities and attack vectors in our increasingly connected digital world.

### (b) Three Approaches to Modeling Network Security (8 Marks)

1. **Perimeter Security Model (Castle Model):**
   - Focuses on strong outer defenses (firewalls, gateways)
   - Assumes internal network is trusted
   - Weakness: Vulnerable if perimeter is breached
   - Example: Traditional corporate networks with firewall at entry point

2. **Layered Security Model (Defense in Depth):**
   - Multiple layers of security controls
   - If one layer fails, others provide protection
   - Includes physical, technical, and administrative controls
   - Example: Network with firewalls, intrusion detection, encryption, and access controls

3. **Zero Trust Model:**
   - "Never trust, always verify" principle
   - No default trust for any entity inside or outside network
   - Strict identity verification for every access request
   - Micro-segmentation of network resources
   - Example: Modern enterprise networks with continuous authentication

The Zero Trust model is increasingly favored as it addresses modern threats like insider attacks and compromised credentials, though it requires more sophisticated implementation than traditional models.


---

1. In not more than two paragraphs, discuss your understanding of mobile and wireless computing
2. identify and discuss four areas where the impact of wireless and mobile computing can be felt
3. Distinguish between a website and web application
4. with the aid of an appropriate diagram, explain how a web application works
5. discuss the steps involved in building web applications
6. explain why web applications is widely-accepts in all works of life today, highlighting its benefits and disadvantages
## **1. Understanding of Mobile and Wireless Computing (2 Paragraphs)**  

Mobile computing refers to the ability to use computing devices such as smartphones, tablets, and laptops while on the move, without requiring a fixed physical connection. It enables users to access data, applications, and services remotely through wireless communication technologies like Wi-Fi, cellular networks (4G/5G), and Bluetooth. Mobile computing emphasizes portability, real-time communication, and location independence, making it essential for modern digital lifestyles.  

Wireless computing, on the other hand, involves data transmission without physical cables, relying on radio waves, infrared, or satellite signals. While mobile computing is a subset of wireless computing, not all wireless systems are mobile (e.g., fixed Wi-Fi networks). Both technologies have revolutionized industries by enabling seamless connectivity, cloud-based services, and the Internet of Things (IoT), transforming how businesses, governments, and individuals interact with digital systems.  

## **2. Four Areas Where Wireless and Mobile Computing Have Impact**  

1. **Healthcare:**  
   - Enables telemedicine, remote patient monitoring, and mobile health apps.  
   - Doctors access patient records wirelessly, improving diagnosis and treatment.  

2. **Business & E-Commerce:**  
   - Mobile payments (e.g., Apple Pay, Google Wallet) facilitate cashless transactions.  
   - Employees access work systems remotely via smartphones and cloud services.  

3. **Education:**  
   - E-learning platforms allow students to attend classes and submit assignments via mobile devices.  
   - Digital libraries and online courses are accessible anywhere.  

4. **Emergency Services:**  
   - GPS and mobile networks help track emergencies and dispatch responders faster.  
   - Wireless sensors in disaster zones provide real-time data for rescue operations.  

---  

## **3. Difference Between a Website and a Web Application**  

| **Feature**          | **Website**                          | **Web Application**                     |  
|----------------------|--------------------------------------|-----------------------------------------|  
| **Purpose**          | Provides static information          | Performs dynamic tasks (e.g., transactions, calculations) |  
| **Interactivity**    | Limited (mostly viewing content)     | High (user inputs, real-time updates)   |  
| **Examples**         | Wikipedia, news blogs                | Gmail, Facebook, online banking        |  
| **Backend Processing** | Minimal (mostly frontend display)  | Heavy (database interactions, APIs)     |  

## **4. How a Web Application Works (with Diagram)**  

### **Diagram Flow:**  
1. **User** sends a request via browser (e.g., login to Facebook).  
2. **Client-Side (Frontend)** processes input (HTML, CSS, JavaScript).  
3. **Request** sent to **Server** via HTTP/HTTPS.  
4. **Server-Side (Backend)** handles logic (PHP, Python, Node.js).  
5. **Database** (MySQL, MongoDB) retrieves/stores data.  
6. **Response** sent back to the user’s browser.  

```
[User] → [Browser] → [Frontend] → [Backend] → [Database]  
           ↑_________________________________________↓  
```  

## **5. Steps in Building Web Applications**  

1. **Planning & Requirement Analysis** – Define purpose, features, and target users.  
2. **UI/UX Design** – Create wireframes and prototypes (Figma, Adobe XD).  
3. **Frontend Development** – Build interface (HTML, CSS, JavaScript, React/Angular).  
4. **Backend Development** – Set up server, APIs, and databases (Node.js, Django, SQL).  
5. **Testing** – Check for bugs, security flaws, and performance issues.  
6. **Deployment** – Host on servers (AWS, Heroku) and launch.  
7. **Maintenance** – Regular updates, security patches, and feature enhancements.  

## **6. Why Web Applications Are Widely Accepted (Benefits & Disadvantages)**  

### **Benefits:**  
- **Accessibility** – Works on any device with a browser.  
- **Cost-Effective** – No need for separate software installations.  
- **Real-Time Updates** – Changes reflect immediately for all users.  
- **Cross-Platform** – Compatible with Windows, macOS, Android, iOS.  
- **Scalability** – Cloud hosting allows easy expansion.  

### **Disadvantages:**  
- **Internet Dependency** – Requires stable connection.  
- **Security Risks** – Vulnerable to hacking (SQL injection, XSS).  
- **Performance Issues** – Slower than native apps in some cases.  
- **Browser Limitations** – Some features may not work across all browsers.  
