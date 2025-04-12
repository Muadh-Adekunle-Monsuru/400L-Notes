### **OSI Model**  

The **OSI Model** (Open Systems Interconnection) was introduced in the 1980s by the **ISO (International Organization for Standardization)**. It defines **what** needs to be done for data communication between computers, without specifying **how** it should be done.  

#### **Purpose of the OSI Model**  
- Provides a **blueprint** for how data is transmitted between systems.  
- Standardizes technology across hardware and software.  
- Outlines rules and protocols for computer communication.  
- Each layer serves a specific function.

---

### **The Seven Layers of the OSI Model**

| **Layer** | **Name**     | **Function**                                                                             | **Protocols/Standards**    | **Data Unit** | **Examples/Devices**                       |
| --------- | ------------ | ---------------------------------------------------------------------------------------- | -------------------------- | ------------- | ------------------------------------------ |
| **7**     | Application  | Provides network services to end-users.                                                  | HTTP, FTP, SMTP, DNS, DHCP | Data          | Web browsers, email clients, apps          |
| **6**     | Presentation | Translates, encrypts, and compresses data.                                               | SSL/TLS, JPEG, GIF, MPEG   | Data          | Format converters, encryptors              |
| **5**     | Session      | Manages sessions between systems, including establishing and maintaining connections.    | NetBIOS, RPC, PAP, SSH     | Data          | Session management systems                 |
| **4**     | Transport    | Ensures reliable delivery of data and controls flow.                                     | TCP, UDP                   | Segments      | Load balancers, firewalls                  |
| **3**     | Network      | Handles routing and logical addressing (e.g., IP addresses).                             | IP, ICMP, RIP              | Packets       | Routers, Layer 3 switches                  |
| **2**     | Data Link    | Manages physical addressing (MAC) and error detection.                                   | Ethernet, PPP              | Frames        | Switches, bridges, network interface cards |
| **1**     | Physical     | Transmits raw data over physical media, defining electrical and physical specifications. | RS-232, Ethernet, USB      | Bits          | Cables, hubs, repeaters                    |

---

### **Key Characteristics of Each Layer**  

1. **Physical Layer**  
   - Manages physical data transmission (e.g., cables, voltages).  
   - Defines interconnection standards like Ethernet or USB.  

2. **Data Link Layer**  
   - Provides error-free transmission over the physical layer.  
   - Handles MAC addressing and manages collisions.  

3. **Network Layer**  
   - Routes data using logical addresses (IP).  
   - Manages traffic and congestion control.  

4. **Transport Layer**  
   - Ensures reliable end-to-end communication.  
   - Controls data flow and performs error checking.  

5. **Session Layer**  
   - Maintains sessions and synchronizes communication.  
   - Implements checkpoints for long transfers.  

6. **Presentation Layer**  
   - Converts data formats for network compatibility.  
   - Handles encryption and compression.  

7. **Application Layer**  
   - Interfaces directly with the end-user and their applications.  
   - Supports file transfers, emails, and more.  

---

### **OSI vs. TCP/IP Model**  

| **Feature**         | **OSI Model**                     | **TCP/IP Model**                |
|----------------------|-----------------------------------|----------------------------------|
| **Layers**           | 7                                | 4                               |
| **Development**      | Developed as a theoretical model | Based on real-world protocols   |
| **Standards**        | Abstract, not tied to protocols  | Built around TCP and IP         |
| **Layer Combination**| Separate Presentation & Session  | Combined with Application layer |
| **Usage**            | Mainly for reference            | Widely used in practice         |

**Layer Mapping (Mermaid Diagram)**  

OSI Model:                     TCP/IP Model:
+-------------------------+    +-------------------+
| 7. Application          |    | 4. Application   |
+-------------------------+    +-------------------+
| 6. Presentation         |          ^
+-------------------------+          |
| 5. Session              |          |
+-------------------------+          |
| 4. Transport            |    | 3. Transport     |
+-------------------------+    +-------------------+
| 3. Network              |    | 2. Internet      |
+-------------------------+    +-------------------+
| 2. Data Link            |          ^
+-------------------------+          |
| 1. Physical             |    | 1. Network Access|
+-------------------------+    +-------------------+


---

### **Data Encapsulation in TCP/IP**  

1. **Encapsulation Steps**  
   - Data moves through the TCP/IP layers, gaining headers (and trailers at the Data Link layer) for each layer's purpose.  
2. **Key Components**  
   - **Header:** Adds protocol-specific information like sender and recipient details.  
   - **Trailer:** Used for error detection at the Data Link layer.  

---

### **Transport Layer Protocols**  

| **Protocol** | **Type**            | **Description**                                                                 |
|--------------|---------------------|---------------------------------------------------------------------------------|
| **TCP**      | Connection-oriented | Ensures reliable, ordered delivery of data.                                     |
| **UDP**      | Connectionless      | Transmits data quickly without establishing a connection (less reliable).       |

---

### **Sockets**  
A **socket** is an endpoint for communication between two machines.  
- **Port Numbers:** Identify specific processes or services at the receiving end.  
- **Usage:** Sockets enable data transmission in a network through protocols like TCP/IP.  