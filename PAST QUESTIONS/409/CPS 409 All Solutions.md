![[409_1 2024.jpeg]]


### **SECTION A**

#### **Question 1**

A new University, XYZ, Osogbo, is setting up its campus network.

**(a) Key design issues to consider before implementing the network solution:**

- **Scalability:** The network should support future expansion.
- **Security:** Implementing authentication, encryption, and firewall protection.
- **Reliability:** Ensuring minimal downtime with redundancy and failover mechanisms.
- **Bandwidth Management:** Adequate bandwidth allocation for smooth operations.
- **Cost:** Selecting an optimal balance between performance and affordability.
- **Interoperability:** Ensuring compatibility with existing hardware/software.
- **Ease of Maintenance:** Using manageable networking equipment and protocols.

**(b) Criteria necessary for the network to be effective and efficient:**

- **Delivery:** Data must reach the intended recipient, whether a device or user.
- **Accuracy:** Data should be transmitted without errors, as altered data may become unreliable.
- **Timeliness:** Data must arrive promptly; for instance, real-time delivery is essential for audio and video, ensuring they are received in the sequence produced without delay.
- **Jitter:** Minimizing variations in packet arrival time is crucial for maintaining quality in data streams, especially for audio and video.

**(c) Justification of the choice of transmission medium over other transmission media:**
I would recommend fiber optic cables as the primary transmission medium because:
- Supports very high bandwidth
- Minimal signal degradation over long distances
- Immune to electromagnetic interference
- Better security as it's difficult to tap
- Future-proof for increasing bandwidth demands
- Ideal for campus backbone infrastructure

**(d) Most suitable Network Topology with justification:**

- **Star Topology:**
    - Each department connects to a central switch or router.
    - **Justification:**
        - Easy troubleshooting and maintenance.
        - Scalability, as new nodes can be added without affecting others.
        - High performance as failures in one node do not affect others.

#### **Question 2**

Brief explanation of key concepts in Data Communication:

**(a) Communication Media:**  
Physical or wireless pathways that carry data between devices. Examples include twisted pair cables, coaxial cables, fiber optics, and wireless transmission.

**(b) Transmission Impairments:**  
Factors that degrade signal quality, such as attenuation (signal loss over distance), noise (unwanted interference), and distortion (signal alteration due to medium properties).

**(c) Network Model:**  
A structured framework that defines data flow and communication between devices. Examples include the OSI Model (7 layers) and TCP/IP Model (4 layers).

**(d) Channel Capacity:**  
The maximum data transfer rate a communication channel can support, typically measured in bits per second (bps). Influencing factors include bandwidth, signal power, and noise.

**(e) Line of Configuration:**  
The arrangement of communication links between devices, such as point-to-point (direct link) or multipoint (shared medium among multiple devices).

### **SECTION B**

#### **Question 3**

**(a) Protocol Agreement Before Communication:**  
Protocols are standardized rules that devices follow to communicate. They ensure proper data transmission, error handling, and synchronization. Without protocol agreement (e.g., TCP/IP, HTTP, FTP), devices may not interpret data correctly, leading to failed communication.
Before communication begins, devices must agree on:
- Data format and encoding
- Timing and synchronization
- Flow control mechanisms
- Error detection and correction methods
This ensures both sender and receiver can properly interpret and process the transmitted data.
**(b) VoIP vs. PSTN Differences:**

- **VoIP (Voice over Internet Protocol):** Uses internet-based transmission, allowing voice calls over IP networks (e.g., Skype, WhatsApp Calls).
- **PSTN (Public Switched Telephone Network):** Uses traditional circuit-switched telephony, with dedicated lines for voice communication.
- **Key Differences:**
    - **VoIP:** Packet-switched, cost-effective, requires internet.
    - **PSTN:** Circuit-switched, reliable but costly, uses dedicated voice channels.

**(c) Roles of Alice, Bob, and Eve in Cryptography:**

- **Alice:** The sender of the message.
- **Bob:** The intended recipient of the message.
- **Eve (Eavesdropper):** A malicious actor attempting to intercept or decipher the message.
- **Application:** Cryptographic protocols like RSA, AES, and Diffie-Hellman ensure secure communication between Alice and Bob while preventing Eve from intercepting meaningful data.
**Scenarios**:
- Alice encrypts a message meant for Bob using his public key
- Bob decrypts the message using his private key
- Eve attempts to intercept and decode the encrypted communication between them
**(d) Three Characteristics to Measure Network Performance:**

1. **Throughput:** The actual data transfer rate, measured in Mbps or Gbps.
2. **Latency:** The time delay between sending and receiving data, measured in milliseconds (ms).
3. **Packet Loss:** The percentage of data packets lost in transit, affecting communication quality.

---

![[409_1 2023.jpeg]]

### **SECTION A**

#### **Question 1**  

**(d) Which property of the transmission medium can cause the signal to be degraded, reduced in amplitude, distorted, or contaminated?**  
- **Attenuation:** The gradual weakening of a signal as it travels through a transmission medium.  
- **Noise:** Unwanted disturbances (e.g., electromagnetic interference) that alter the signal.  
- **Distortion:** Changes in the signal waveform due to varying speeds of frequency components.  



### **Question 2**  

The topology shown in Figure is **Mesh Topology**.

**(a) Advantages and disadvantages of the topology in Figure 1**  

**Advantages:**  
- **Redundancy and Fault Tolerance:** If one link fails, communication can still occur via alternative paths.  
- **Improved Reliability:** Since multiple paths exist, network downtime is minimized.  
- **Better Security:** Direct links reduce unauthorized access risks.  

**Disadvantages:**  
- **High Cost:** Requires more cabling and network interfaces.  
- **Complex Configuration:** Difficult to set up and maintain.  
- **Scalability Issues:** Adding new nodes increases complexity.  

**(b) Possibility of having redundant communication paths between some or all devices in this topology?**  
- **Yes,** mesh topology inherently supports redundancy.  
- **Full Mesh:** Every node connects to every other node.  
- **Partial Mesh:** Only some nodes have multiple connections.  
- **Effect:** Ensures alternative communication routes in case of failures.  

**(c) Practical example of the topology with justification**  
- **Example:** Internet backbone networks and financial transaction networks.  
- **Justification:**  
  - High availability is critical in banking and telecom industries.  
  - Fault tolerance ensures uninterrupted operations.  
  - Security concerns demand dedicated point-to-point connections.  

---

### **SECTION B**  

**(e) Multiplexing**  
- **Definition:** A technique that combines multiple signals into one medium for transmission.  
**Types:**  
  - **Time-Division Multiplexing (TDM):** Each signal gets a fixed time slot.  
  - **Frequency-Division Multiplexing (FDM):** Different signals use different frequency bands.  
  - **Wavelength-Division Multiplexing (WDM):** Used in fiber optics, assigns different wavelengths to signals.  
- **Application:** Used in telecommunication networks, cable TV, and radio broadcasting.  

---
![[409_1 2022.jpeg]]

**SECTION A**

**Question 1**

**(a) Recommended Network Topology:**

 a **hybrid topology** combining elements of a **star topology** for regional offices and a **mesh topology** for interconnecting these offices. 

* **Star within regions:** Each regional office would utilize a star topology, with all devices connecting to a central switch or router. This is practical for local management and scalability within each office.
* **Mesh between regions:**  The central connection points (likely core routers) of each regional office would be interconnected in a mesh topology.  A full or partial mesh would be chosen based on budget and redundancy needs.  This provides multiple paths for data to travel, ensuring high availability and fault tolerance in case of link failures.

**(b) Diagram:**

```
          Regional Office 1                 Regional Office 2
      (Star Topology)                  (Star Topology)
        -------*-------                -------*-------
        |       |       |                |       |       |
      *---*---*---*---*              *---*---*---*---*
        |       |       |                |       |       |
        -------*-------                -------*-------
            \       /                    \       /
             \     /                      \     /
              -----                      -----
                 |                          |
          Regional Office 3                 Regional Office 4
      (Star Topology)                  (Star Topology)
        -------*-------                -------*-------
        |       |       |                |       |       |
      *---*---*---*---*              *---*---*---*---*
        |       |       |                |       |       |
        -------*-------                -------*------- 
```

**(c) Advantages of Hybrid (Star/Mesh):**

1. **Scalability:**  Star topology within regions allows easy expansion by connecting new devices to the central switch. Mesh topology between regions ensures that adding new regional offices doesn't disrupt the entire network.
2. **Fault Tolerance:** Mesh connectivity provides redundant paths, so if one link fails, data can still travel through alternative routes. This is crucial for business continuity.
3. **Performance:**  Star topology minimizes collisions within a region. Mesh topology reduces latency between regions by providing direct or efficient paths.
4. **Centralized Management:** Star topology simplifies management within each region as all devices connect to a central point.  While the mesh part requires more planning, it offers network-wide control through the core routers.

**(d) Limitations:**

1. **Cost:** Implementing a mesh topology, especially a full mesh, can be expensive due to the number of links required.
2. **Complexity:**  Designing and managing a hybrid network, particularly the mesh portion, can be more complex than simpler topologies.  Requires skilled network engineers.
3. **Maintenance:** Troubleshooting and maintaining a complex hybrid network can be challenging and time-consuming.

**Question 2**

**(a) Transmission Impairments:**

* **Attenuation:** Signal loss over distance. Measured in decibels (dB).  Compensated using amplifiers or repeaters.
* **Distortion:** Alteration of the signal's waveform. Different frequency components travel at different speeds.  Equalization techniques can help.
* **Noise:** Unwanted signals that interfere with the desired signal. Types include thermal noise, impulse noise, crosstalk. Shielding and filtering are used to mitigate noise.

**(b) Network Model:**

* **OSI Model (Open Systems Interconnection):**  A seven-layer conceptual framework for network communication: Application, Presentation, Session, Transport, Network, Data Link, Physical. Each layer performs specific functions.
* **TCP/IP Model (Transmission Control Protocol/Internet Protocol):**  A four-layer model: Application, Transport, Network (Internet), Link (Network Interface).  It's the foundation of the internet.

**(c) Line Configuration:**

* **Point-to-point:**  Direct connection between two devices (e.g., a dedicated leased line).
* **Multipoint (or multidrop):**  Multiple devices share a single communication line (e.g., older bus topologies).

**(d) Multiplexing:**

Combining multiple signals into one for transmission over a shared medium. 
* **Frequency Division Multiplexing (FDM):** Signals are assigned different frequency bands.
* **Time Division Multiplexing (TDM):** Signals are assigned different time slots.
* **Wavelength Division Multiplexing (WDM):**  Used in fiber optics, signals are assigned different wavelengths of light.

**(e) Switched Network:**

A network that uses switching devices (switches) to forward data packets between devices.  
* **Circuit Switching:**  Dedicated path established between devices before transmission (e.g., traditional telephone networks).
* **Packet Switching:** Data is divided into packets, each of which is routed independently through the network (e.g., the internet).

**SECTION B**

**Question 1**

**(a) Criteria for FUO Network Efficiency and Effectiveness:**

- **Delivery:** Data must reach the intended recipient, whether a device or user.
- **Accuracy:** Data should be transmitted without errors, as altered data may become unreliable.
- **Timeliness:** Data must arrive promptly; for instance, real-time delivery is essential for audio and video, ensuring they are received in the sequence produced without delay.
- **Jitter:** Minimizing variations in packet arrival time is crucial for maintaining quality in data streams, especially for audio and video.
* **Performance:**  High throughput (data transfer rate), low latency (delay), minimal jitter (variation in delay).
* **Security:**  Protection against unauthorized access, data breaches, and cyberattacks.

**(b) Important Parameters for Evaluating Communication Channel Capacity:**

* **Bandwidth:** The range of frequencies a channel can carry. Higher bandwidth = higher data rate.
* **Data Rate (Throughput):**  The actual amount of data transmitted per unit of time (bps, Mbps, Gbps).
* **Signal-to-Noise Ratio (SNR):** The ratio of signal power to noise power. Higher SNR = better signal quality.
* **Channel Capacity (Shannon Limit):** The theoretical maximum data rate achievable over a channel with a given bandwidth and SNR.

**(c) Two Primary Key Concerns in Designing a New Transmission System:**

1. **Performance:** Achieving the desired data rate, latency, and error rate to meet user needs.
2. **Cost:**  Balancing performance requirements with the cost of equipment, installation, and maintenance.

**(d) Design Factors Affecting the Two Concerns:**

* **Transmission Medium:**  Choice of cable (copper, fiber), wireless technology, etc., affects bandwidth, distance, and cost.
* **Signal Encoding:**  Modulation techniques used impact data rate and susceptibility to noise.
* **Multiplexing Techniques:**  Efficiency of channel utilization and cost.
* **Network Protocols:**  Overhead introduced by protocols affects throughput and latency.

---
![[409_1 2021.jpeg]]