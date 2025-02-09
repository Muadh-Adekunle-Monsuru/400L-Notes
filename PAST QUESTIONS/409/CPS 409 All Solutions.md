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


**SECTION A**

**Question 1**

This question is similar to Question 1 in the previous years

**Question 2**

**(a) Data Communication:**

The exchange of data between two or more devices over a communication medium. It involves encoding, transmitting, and decoding data.

**(b) Bandwidth:**

The range of frequencies a communication channel can carry. It determines the maximum data rate achievable.

**(c) Network Model:**

A framework that defines the layers of communication in a network. Examples include the OSI model and TCP/IP model.

**(d) Network Protocols:**

Sets of rules and standards that govern how devices communicate on a network. They define message formats, addressing schemes, error handling, etc.

**(e) Unguided Media:**

Wireless communication channels that do not use physical conductors. Examples include radio waves, microwaves, and infrared.



**SECTION B**

**Question 1**

**(a) Three Characteristics of Computer Network Performance:**

8. **Throughput:**  The actual amount of data transmitted per unit of time (bps, Mbps, Gbps).
9. **Latency:**  The delay between sending a message and receiving it.
10. **Jitter:**  The variation in latency, which can affect real-time applications.

**(b) Propagation and Transmission Time Calculation:**

* **Propagation time:** Distance / Speed of light = (24000 * 1000 m) / (2.4 * 10^8 m/s) = 0.1 s
* **Transmission time:** Message size / Bandwidth = (1.5 * 1024 * 8 bits) / (1 * 10^9 bps) = 0.012288 s
* **Total time:** Propagation time + Transmission time = 0.1 s + 0.012288 s = 0.112288 s

**Determining and Measuring:**

* **Throughput:** Measured using network monitoring tools (e.g., iperf, PRTG) by sending large files and measuring the transfer rate.
* **Latency:** Measured using ping or traceroute commands, or specialized tools that capture round-trip delay.
* **Jitter:** Measured using similar tools as latency, looking at the variation in round-trip times over multiple packets.

**(c) Radio Waves for Long-Distance Broadcasting:**

* **Omnidirectional propagation:**  Radio waves can travel in all directions, making them suitable for reaching a wide audience.
* **Long-distance coverage:**  Different frequencies can travel long distances, enabling nationwide or global broadcasting.
* **Relatively low cost:** Compared to laying cables, radio broadcasting infrastructure is more cost-effective for reaching large populations.

**Question 2**

**(a) Information Representation using Analog and Digital Signals:**

![[Pasted image 20250208214352.png|500]]
* **Analog:** A continuous waveform, where the amplitude or frequency of the wave represents the information.  Think of a smooth, curvy line. Examples:  Older audio signals, sensor readings.
* **Digital:**  Discrete signals represented by distinct voltage levels (typically 0 and 1). Think of a series of steps or pulses. Examples:  Computer data, digital audio.


**(b) Reasons for Protocols and Standards in Computer Networks:**

1. **Interoperability:**  Enable devices from different vendors to communicate seamlessly.
2. **Standardization:**  Provide a common framework for network design and implementation.
3. **Reliability:**  Ensure reliable data transmission through error detection and correction mechanisms.
4. **Security:**  Implement security measures to protect data.
5. **Manageability:**  Simplify network management and troubleshooting.


---
![[409_2 2.jpeg]]

**Question 5**

**(a) Frequency Domain of Non-Periodic Composite Signal:**

**Understanding the Signal:**

* **Non-periodic:** This means the signal doesn't repeat at regular intervals. Its frequency components will be continuous, not discrete.
* **Bandwidth:** 200 kHz, the range of frequencies present in the signal.
* **Middle frequency:** 140 kHz, the center of the bandwidth.
* **Peak amplitude:** 20V, the highest amplitude of the signal.
* **Zero amplitude at extremes:** The signal's amplitude goes to zero at the edges of the bandwidth.

**Drawing the Frequency Domain:**

Since the signal is non-periodic, we represent it as a continuous spectrum.

1. **Frequency Axis:** Draw a horizontal axis representing frequency (f), from (140 kHz - 100 kHz) = 40 kHz to (140 kHz + 100 kHz) = 240 kHz.
2. **Amplitude Axis:** Draw a vertical axis representing amplitude (A), from 0V to 20V.
3. **Spectrum Shape:** Draw a curve that is centered at 140 kHz, reaching a peak of 20V, and tapering down to 0V at 40 kHz and 240 kHz. The shape could be triangular, Gaussian, or another smooth curve, as the exact shape isn't specified.

**Important Note:** The frequency domain representation shows the distribution of amplitudes across the range of frequencies present in the signal.

**(b) Differentiating Between:**

**i. Shielded and Unshielded Twisted Pair Cable:**

* **Shielded Twisted Pair (STP):**  Has a metallic shield around the twisted pairs to protect against electromagnetic interference (EMI). Used in noisy environments.
* **Unshielded Twisted Pair (UTP):**  Does not have a shield. More common and less expensive, suitable for most office environments.

**ii. Guided and Unguided Media:**

* **Guided Media:**  Physical conductors guide the signal (e.g., copper cables, fiber optic cables).
* **Unguided Media:**  Wireless transmission, signals propagate through the air or space (e.g., radio waves, microwaves).

**iii. Analog and Digital Transmission:**

* **Analog Transmission:**  Uses continuous waveforms to represent data.
* **Digital Transmission:**  Uses discrete signals (0s and 1s) to represent data.

**iv. Circuit Switching and Packet Switching:**

* **Circuit Switching:**  Establishes a dedicated path between sender and receiver before transmission (e.g., traditional telephone network).
* **Packet Switching:**  Divides data into packets, each of which is routed independently through the network (e.g., the internet).

**v. OSI Model and TCP/IP Model:**

* **OSI Model (Open Systems Interconnection):**  A seven-layer conceptual model for network communication (Application, Presentation, Session, Transport, Network, Data Link, Physical).
* **TCP/IP Model (Transmission Control Protocol/Internet Protocol):**  A four-layer model that is the basis of the internet (Application, Transport, Network/Internet, Link/Network Interface).

**vi. Bridges and Routers:**

* **Bridges:** Operate at the Data Link Layer (Layer 2) and connect two LAN segments, forwarding traffic based on MAC addresses.
* **Routers:** Operate at the Network Layer (Layer 3) and connect different networks, forwarding traffic based on IP addresses.

**Question 6**

**(a) Functionalities of Networking/Internetworking Devices:**

1. **Hub:**  (Layer 1)  A simple device that broadcasts incoming signals to all connected ports.
2. **Switch:**  (Layer 2)  Learns MAC addresses and forwards traffic only to the intended recipient.
3. **Router:**  (Layer 3)  Connects different networks and routes traffic based on IP addresses.
4. **Firewall:**  A security device that controls network traffic based on predefined rules.

**(b) Why Digital Communication through Circuit Switching is Inefficient:**

* **Wasted Bandwidth:**  In circuit switching, the path is dedicated even when no data is being transmitted, leading to wasted bandwidth.
* **Longer Setup Time:**  Establishing a circuit takes time, making it less suitable for bursty data.
* **Less Flexible:**  Difficult to reroute traffic if a link fails.

**Packet switching** is more efficient for digital communication because it uses bandwidth only when data is being transmitted, and packets can be routed flexibly through the network.

**Question 7**

**(i) Bandwidth of Periodic Signal:**

The bandwidth of a periodic signal is the difference between the highest and lowest frequencies present.

Bandwidth = 1100 Hz - 100 Hz = 1000 Hz = 1 kHz

**(ii) Drawing the Spectrum:**

5. **Frequency Axis:** Draw a horizontal axis representing frequency (f), from 0 Hz to 1100 Hz.
6. **Amplitude Axis:** Draw a vertical axis representing amplitude (A), from 0V to 10V.
7. **Discrete Frequencies:** Mark the frequencies 100 Hz, 300 Hz, 500 Hz, 700 Hz, 900 Hz, and 1100 Hz on the frequency axis.
8. **Amplitudes:** Draw vertical lines (impulses) at each of the marked frequencies, each with an amplitude of 10V.

**Important Note:** The spectrum of a periodic signal consists of discrete frequency components (impulses), unlike the continuous spectrum of a non-periodic signal.


---
![[409_2 3.jpeg]]



**SECTION B**

**Question 1**

**(b) Limitations and Alternatives for Large Networks:**

**i. Why Impractical for Very Large Networks:**

* **Cost:** A full mesh topology becomes very expensive to implement and maintain as the number of nodes (regional offices in this case) increases significantly. The number of links grows exponentially.
* **Complexity:** Managing and troubleshooting a large, fully meshed network becomes extremely complex.

**ii. Better Alternatives:**

1. **Hierarchical Routing:** Implement a hierarchical network architecture with multiple layers of routers. This divides the network into smaller, more manageable routing domains.
2. **Partial Mesh or Hub-and-Spoke:** Instead of a full mesh, use a partial mesh or a hub-and-spoke topology between regional offices. A hub-and-spoke topology designates a central "hub" location that all other locations connect to. This reduces the number of links required compared to a full mesh.
3. **Software-Defined Networking (SDN):**  SDN allows centralized control and management of the network, simplifying complex topologies and improving efficiency.

**Question 2**

**(a) Analog vs. Digital Signals:**

**(Diagram):**

* **Analog:** A continuous waveform, smoothly varying in amplitude or frequency.  (Imagine a smooth sine wave).
* **Digital:** Discrete signal levels, typically representing 0 and 1. (Imagine a series of square waves).

**(Description):**

* **Analog:** Information is encoded as variations in the continuous waveform. Susceptible to noise and attenuation.
* **Digital:** Information is encoded as distinct voltage levels. More robust against noise and easier to process and regenerate.

**(b) Radio Waves for Long-Distance Broadcasting:**

* **Omnidirectional Propagation:** Radio waves can travel in all directions, making them suitable for reaching a wide audience without needing line-of-sight between transmitter and receiver.
* **Long-Distance Coverage:** Different frequencies of radio waves can travel long distances, enabling nationwide or global broadcasting.
* **Relatively Low Cost:** Compared to laying cables, radio broadcasting infrastructure is more cost-effective for reaching large populations over vast areas.

**(c) Non-Interference of Remote Controls:**

Remote controls typically use infrared (IR) light or radio frequencies (RF).

* **IR Remote Controls:** Operate on line-of-sight and are easily blocked by obstacles.  This directionality prevents interference between neighbors as the signal is unlikely to reach beyond your home.
* **RF Remote Controls:** Use radio waves but operate on specific frequencies and often use unique device addresses. This combination of frequency and addressing ensures that signals from one remote control only control its intended device.

**(d) Tethering:**

Tethering is the process of sharing a mobile device's internet connection with other devices.

**Ways to do it over WLAN (Wi-Fi):**

1. **Portable Wi-Fi Hotspot:** The mobile device acts as a Wi-Fi access point, allowing other devices to connect to its internet connection.
2. **Wi-Fi Tethering Apps:** Some apps provide advanced tethering features, like controlling the number of connected devices or setting data limits.

**Question 3**

**(a) Bandwidth of Signal:**

The bandwidth of a signal is the difference between the highest and lowest frequencies present.

Bandwidth = 240 Hz - 10 Hz = 230 Hz

**(Drawing):**

1. **Frequency Axis:** Draw a horizontal axis from 0 Hz to 240 Hz.
2. **Amplitude Axis:** Draw a vertical axis representing amplitude.
3. **Frequencies:** Mark the frequencies 10, 25, 60, 120, and 240 Hz on the frequency axis.
4. **Impulses:** Draw vertical lines (impulses) at each frequency, all with the same amplitude (as specified in the question).

**(b) Functions of Network Implementation Devices:**

1. **Switch:** A Layer 2 device that learns MAC addresses and forwards traffic only to the intended recipient, improving network efficiency.
2. **Router:** A Layer 3 device that connects different networks and routes traffic based on IP addresses, enabling communication between networks.
3. **Firewall:** A security device that controls network traffic based on predefined rules, protecting the network from unauthorized access and cyber threats.

**(c) Inefficiency of Circuit Switching for Digital Communication:**

Circuit switching establishes a dedicated path between sender and receiver before transmission. This path remains dedicated even when no data is being transmitted, leading to:

* **Wasted Bandwidth:** Bandwidth is reserved but unused during idle periods.
* **Inefficiency for Bursty Data:** Digital communication is often bursty, with periods of high activity followed by inactivity. Circuit switching is not efficient for this type of traffic.

Packet switching is more efficient because it uses bandwidth only when data is being transmitted.

**(d) Comparison and Contrast:**

Here's a comparison of five of the items you listed. Remember to choose any five for your answer.

**i. Analog and Digital Transmission:**

* **Analog:** Continuous waveforms, susceptible to noise, older technology.
* **Digital:** Discrete signals, robust against noise, modern technology.

**ii. OSI Model and TCP/IP Model:**

* **OSI:** 7 layers, conceptual, not widely implemented.
* **TCP/IP:** 4 layers, practical, basis of the internet.

**iii. Guided and Unguided Media:**

* **Guided:** Physical conductors (cables), high bandwidth, secure.
* **Unguided:** Wireless (radio waves), mobility, less secure.

**iv. Bridges and Routers:**

* **Bridges:** Layer 2, connect LAN segments, forward based on MAC addresses.
* **Routers:** Layer 3, connect networks, forward based on IP addresses.

**v. Circuit Switching and Packet Switching:**

* **Circuit:** Dedicated path, inefficient for bursty data, older technology.
* **Packet:** Shared path, efficient for bursty data, modern technology.

**vi. LAN and WLAN:**

* **LAN:** Wired, high bandwidth, secure, limited mobility.
* **WLAN:** Wireless, lower bandwidth, less secure, high mobility.


---
![[409_2 5.jpeg]]


**Question 2**

**(a) Correlation between OSI and TCP/IP Models:**

Both the OSI and TCP/IP models are conceptual frameworks that define the layers of communication in a network. They simplify the communication process by breaking it down into manageable layers, each with specific functions.  The layers define how network devices interact and ensure interoperability.

**(b) Effect of Twists per Unit Length in Twisted Pair Cable:**

The number of twists per unit length significantly impacts the cable's performance:

* **Reduced EMI/RFI:** More twists reduce electromagnetic and radio-frequency interference. The twists help cancel out noise picked up by the cable.
* **Increased Data Rate:** Higher twist density allows for higher data rates as the signal is less susceptible to interference and crosstalk.
* **Improved Signal Quality:**  More twists lead to better signal integrity over longer distances, reducing signal loss and errors.

**(c) Output Signal-to-Noise Ratio (SNR) Calculation:**

1. **Output Signal Power:**
   * Convert dB loss to a ratio: 20 dB = 10^(20/10) = 100
   * Output signal power = Input signal power / Loss ratio = 0.5 W / 100 = 0.005 W = 5 mW

2. **Output SNR:**
   * SNR = Output signal power / Output noise level = 5 mW / 4.5 µW = (5 * 10^-3 W) / (4.5 * 10^-6 W) ≈ 1111.11

3. **SNR in dB:**
   * SNR (dB) = 10 * log10(SNR) = 10 * log10(1111.11) ≈ 30.46 dB

**(d) Non-Interference of Remote Controls:**

Remote controls often use either infrared (IR) light or radio frequency (RF) signals.

* **IR Remote Controls:** Operate with line-of-sight.  IR signals are easily blocked by walls and other objects, limiting their range and preventing interference with neighbors.
* **RF Remote Controls:** While RF signals can travel through walls, remote controls typically operate on specific frequencies and use unique device addresses. This addressing scheme ensures that signals from one remote only control its intended device, even if neighbors' devices operate on similar frequencies.

**Question 3**

**(a) Frequency Division Multiplexing (FDM) in AM and FM Radio Broadcasting:**

FDM divides the available bandwidth into separate frequency channels. Each channel is allocated to a different broadcast station.

* **AM Radio:** Uses Amplitude Modulation. The amplitude of the carrier wave is varied to encode the audio signal, while the frequency remains constant. AM radio has lower bandwidth and is more susceptible to noise.
* **FM Radio:** Uses Frequency Modulation. The frequency of the carrier wave is varied to encode the audio signal, while the amplitude remains constant. FM radio has higher bandwidth, allowing for better audio quality and is less susceptible to noise.

FDM allows many radio stations to broadcast simultaneously without interfering with each other because each station's signal is confined to its assigned frequency band.

**(b) Network Implementation Devices (Two Examples):**

1. **Firewall:** A network security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules. Firewalls can be hardware or software based.
2. **Switch:**  A Layer 2 device that connects network segments and forwards data packets only to the intended recipient based on MAC addresses, improving network efficiency and reducing collisions.

**(c) Protocol Functions:**

* **i. ARP (Address Resolution Protocol):** Resolves IP addresses to MAC addresses, enabling devices to communicate on a local network.
* **ii. HTTPS (Hypertext Transfer Protocol Secure):**  A secure version of HTTP, used for secure communication over the internet. It encrypts data to protect it during transmission.
* **iii. ICMP (Internet Control Message Protocol):** Used for network diagnostics and error reporting. Ping uses ICMP to test network connectivity.
* **iv. SMTP (Simple Mail Transfer Protocol):**  Used for sending email.
* **v. FTP (File Transfer Protocol):** Used for transferring files between computers on a network.

**Question 4**

**(a) Bandwidth of Signal with Five Sine Waves:**

The bandwidth is the difference between the highest and lowest frequencies.

Bandwidth = 240 Hz - 0 Hz = 240 Hz

**(Drawing):**

3. **Frequency Axis:** Draw a horizontal axis from 0 Hz to 240 Hz.
4. **Amplitude Axis:** Draw a vertical axis representing amplitude.
5. **Frequencies:** Mark the frequencies 0, 25, 60, 120, and 240 Hz on the frequency axis.
6. **Impulses:** Draw vertical lines (impulses) at each frequency, all with the same amplitude.

**(b) Comparison and Contrast (Skipping Previously Covered):**

**iv. Frequency Division Multiplexing (FDM) and Time-Division Multiplexing (TDM):**

* **FDM:** Divides the bandwidth into frequency channels, each channel used by a different transmission stream.  Used in radio broadcasting.
* **TDM:** Divides the transmission time into slots, each slot allocated to a different transmission stream. Used in T1/E1 lines.

**v. Frequency Domain and Time Domain:**

* **Frequency Domain:** Represents a signal in terms of its constituent frequencies and their amplitudes. (e.g., spectrum of a signal).
* **Time Domain:** Represents a signal in terms of its amplitude variations over time. (e.g., a graph of voltage vs. time).

**vi. Circuit Switching and Packet Switching:**

* **Circuit Switching:** Dedicated path, inefficient for bursty data. (e.g., traditional phone calls).
* **Packet Switching:** Shared path, efficient for bursty data. (e.g., the internet).

---
![[409_2 6.jpeg]]

**Question 2**

**(a) Importance of Protocol Agreement:**

Devices must agree on protocols before communication because protocols are the sets of rules that govern how data is formatted, transmitted, received, and interpreted. Without a common protocol, devices wouldn't understand each other's signals, leading to communication breakdown. Protocols ensure interoperability and standardized communication.

**(b) Justification for Optical Fiber Investment:**

Telecommunication companies invest in optical fiber due to its numerous advantages:

1. **High Bandwidth:** Fiber offers significantly higher bandwidth than copper cables, enabling faster data transmission and supporting more users/services.
2. **Long Distance:** Fiber can transmit signals over longer distances without significant signal loss, reducing the need for repeaters.
3. **Immunity to EMI/RFI:** Fiber is immune to electromagnetic and radio-frequency interference, ensuring clearer signals and higher data integrity.
4. **Security:** Fiber is harder to tap into than copper, making it more secure for transmitting sensitive data.
5. **Lightweight and Durable:** Fiber cables are lighter and more durable than copper, making them easier to install and maintain.

**(c) Digital vs. Analog Signals:**

* **Analog Signals:** Continuous waveforms that vary in amplitude or frequency to represent data.
* **Digital Signals:** Discrete signals represented by distinct voltage levels (typically 0 and 1).

**Property Making Digital Better:**

Digital signals are more resistant to noise and interference. They can be regenerated perfectly, ensuring data integrity over long distances. Analog signals degrade with noise accumulation, making them less reliable.

**(d) Radio Waves for Long-Distance Broadcasting:**

Radio waves are suitable for long-distance broadcasting due to:

1. **Omnidirectional Propagation:** They can travel in all directions, reaching a wide audience without requiring line-of-sight.
2. **Long-Distance Coverage:** Different frequencies can travel vast distances, enabling regional and national broadcasts.
3. **Relatively Low Infrastructure Cost:** Compared to wired solutions, radio broadcasting infrastructure is less expensive for covering large areas.

**Question 3**

**(a) VoIP Adoption Justification:**

Organizations adopt VoIP due to:

1. **Cost Savings:** VoIP calls over the internet are often cheaper than traditional PSTN calls, especially for long-distance and international calls.
2. **Flexibility and Scalability:** VoIP systems are easily scalable and offer features like call forwarding, voicemail, and conferencing, which are more complex to implement in PSTN.
3. **Integration:** VoIP can be integrated with other communication tools and business applications, streamlining workflows.
4. **Enhanced Features:** VoIP offers features like video conferencing, instant messaging, and presence information, enhancing communication capabilities.

**(b) Technical Barriers in VoIP:**

1. **Latency and Jitter:** Delay and variation in delay can affect call quality, making conversations difficult.
2. **Packet Loss:** Packets may get lost during transmission, leading to gaps in audio.
3. **Quality of Service (QoS):** Ensuring consistent call quality can be challenging, especially on congested networks.
4. **Security:** VoIP systems are vulnerable to security threats like eavesdropping and denial-of-service attacks.
5. **Dependence on Internet Connection:** VoIP relies on a stable internet connection; outages can disrupt communication.

**(c) Computer with NOS vs. Without NOS + NIC:**

* **Computer with NOS:** A NOS provides centralized management of network resources, security, and user access. It simplifies tasks like file sharing, printer management, and network monitoring.
* **Computer without NOS + NIC:** Requires individual configuration for network access and resource sharing. Each computer manages its own security and access control, making administration more complex. A NIC only provides the physical connection to the network.

**In essence:** A NOS provides a software layer for managing and simplifying network operations, while a computer without a NOS relies on individual machine configurations.

**(d) Peer-to-Peer vs. Client/Server Networks:**

* **Peer-to-Peer:** All computers have equal roles and can act as both clients and servers. Resources are shared directly between computers. Suitable for small networks.
* **Client/Server:** Centralized servers provide resources and services to client computers. Servers manage security and access control. Suitable for larger networks requiring centralized administration.

**Question 4**

**(a) Network Security through Cryptography:**

Cryptography is fundamental to network security as it provides:

1. **Confidentiality:** Encryption ensures that only authorized parties can read the data.
2. **Integrity:** Hashing ensures that data is not altered in transit.
3. **Authentication:** Digital signatures verify the sender's identity.
4. **Non-Repudiation:** Prevents senders from denying that they sent a message.

**(b) Cryptography Concepts:**

* **i. Cipher:** An algorithm used to encrypt and decrypt data.
* **ii. Symmetric Key:** Uses the same key for encryption and decryption. Fast but less secure for key exchange.
* **iii. Asymmetric Key:** Uses a pair of keys – a public key for encryption and a private key for decryption. Secure for key exchange but slower.

**(c) Monoalphabetic Cipher Identification:**

* **i. Ciphertext: MHMAE; Plaintext: OSOGBO:** Not monoalphabetic. 'O' is encrypted as 'M' in the first instance and 'H' in the second.
* **ii. Ciphertext: AZYKI; Plaintext: YAHOO:** Monoalphabetic. Each letter consistently maps to another letter.

**(d) Shift Cipher Encryption/Decryption:**

* **i. Encryption of "FOUNTAIN" with key = 12:**
   * F(6) + 12 mod 26 = R(18)
   * O(15) + 12 mod 26 = A(1)
   * U(20) + 12 mod 26 = G(6)
   * N(13) + 12 mod 26 = Z(25)
   * T(19) + 12 mod 26 = f(5)
   * A(0) + 12 mod 26 = M(12)
   * I(8) + 12 mod 26 = u(20)
   * N(13) + 12 mod 26 = Z(25)

   Ciphertext: RAGZFMUZ

* **ii. Decryption of "XAHQ" with key = 12:**
   * X(23) - 12 mod 26 = L(11)
   * A(0) - 12 mod 26 = O(14)
   * H(7) - 12 mod 26 = V(21)
   * Q(16) - 12 mod 26 = e(4)

   Plaintext: LOVD

---
![[409_2 8.jpeg]]


**Question 2**


**(c) Cable Links Required for Topologies:**

For "n" devices:

* **Mesh:** n(n-1)/2  (Every device connects to every other device)
* **Ring:** n (Devices connected in a closed loop)
* **Bus:** 1 (All devices share a single cable)
* **Star:** n (All devices connect to a central hub/switch)

**Question 3**

**(b) Comparison:** (Focusing on the new comparisons)

**iv. UDP and TCP:**

* **UDP (User Datagram Protocol):** Connectionless, unreliable, fast, suitable for streaming and gaming where some data loss is acceptable.
* **TCP (Transmission Control Protocol):** Connection-oriented, reliable, slower, suitable for applications where data integrity is crucial (e.g., file transfer, web browsing).

**Question 4**

**(a) Network Implementation Devices:** (Focusing on different examples)

1. **Modem:** Modulates and demodulates signals for transmission over communication channels (e.g., cable modem, DSL modem).
2. **Firewall:** A security device that controls network traffic based on predefined rules, protecting against unauthorized access.
3. **Load Balancer:** Distributes network traffic across multiple servers to improve performance and availability.

**(b) Protocols:**

* **i. ICMP (Internet Control Message Protocol):** Used for network diagnostics and error reporting (e.g., ping).
* **ii. MIME (Multipurpose Internet Mail Extensions):** Used for email to support various content types (e.g., attachments, images).
* **iii. HTTPS (Hypertext Transfer Protocol Secure):** Secure version of HTTP, encrypts communication between browser and website.
* **iv. DHCP (Dynamic Host Configuration Protocol):** Assigns IP addresses dynamically to devices on a network.
* **v. SNMP (Simple Network Management Protocol):** Used for network monitoring and management.
* **vi. SMTP (Simple Mail Transfer Protocol):** Used for sending email.
* **vii. LDAP (Lightweight Directory Access Protocol):** Used for accessing and managing directory information (e.g., user accounts).


---
![[409_2 2021.jpeg]]

**Question 2**

**(c) Twists per Unit Length in Twisted Pair Cable:**

More twists per unit length in a twisted pair cable improve its quality by:

1. **Reducing EMI/RFI:**  The twists help cancel out electromagnetic and radio-frequency interference picked up by the cable, leading to a cleaner signal.
2. **Increasing Data Rate:**  Higher twist density allows for higher data rates as the signal is less susceptible to interference and crosstalk.
3. **Improving Signal Quality:**  More twists improve signal integrity over distance, reducing signal loss and errors.

**Question 3**

**(a) Fourier Analysis:**

Fourier analysis is a mathematical technique that decomposes a periodic signal into a sum of sine and cosine waves of different frequencies. It reveals the frequency components present in the signal.

**(c) OSI and TCP/IP Model Correlation:**

**(i) How they correlate:**

* Both are layered models for network communication.
* Corresponding layers perform similar functions (though not exact one-to-one mapping).
* Both provide a framework for understanding and standardizing network communication.

**(ii) Significance and Drawbacks of Layer Combination:**

**Significance:**

* **Simplicity:**  A single Application layer simplifies the model and makes it easier to understand and implement.
* **Efficiency:** Fewer layers can potentially reduce overhead and improve performance.

**Drawbacks:**

* **Loss of Specificity:** Combining layers loses the distinct functions of Presentation (data formatting) and Session (session management), which can be important in some applications.
* **Reduced Flexibility:**  Changes in one aspect of the Application layer might affect other aspects, making it less modular and harder to modify.

**Question 4**

**(a) Protocol Functions:**

* **i. TCP (Transmission Control Protocol):** Connection-oriented, reliable, ensures ordered delivery, flow control, congestion control.
* **ii. UDP (User Datagram Protocol):** Connectionless, unreliable, fast, suitable for streaming where some data loss is acceptable.
* **iii. ICMP (Internet Control Message Protocol):** Used for network diagnostics and error reporting (e.g., ping).
* **iv. ARP (Address Resolution Protocol):** Resolves IP addresses to MAC addresses.
* **v. RARP (Reverse Address Resolution Protocol):** Resolves MAC addresses to IP addresses (obsolete).

**(b) Differentiations:**

**(ii) Bandwidth in Hertz vs. Bits per Second:**

* **Hertz (Hz):**  Measures the range of frequencies a channel can carry.
* **Bits per Second (bps):** Measures the rate of data transmission.

They are related but different.  Bandwidth in Hz is a physical property of the channel, while bps depends on the modulation technique used to encode data.

**(v) Point-to-Point vs. Multipoint Connection:**

* **Point-to-Point:** Direct link between two devices.
* **Multipoint:** Multiple devices share a single communication channel.

---
![[409_2 2024.jpeg]]

**Question 4**

**(c) Cipher Analysis:**

**i. BROKENHEARTED → YUWLTIFTVUMTX:**

- **Monoalphabetic.** The letter 'E' is encrypted as 'T' in the first instance and 'T' in the second. A monoalphabetic cipher would always encrypt the same plaintext letter to the same ciphertext letter.

**ii. ADAMANT → OCONOAC:**

- **Monoalphabetic.** Each letter consistently maps to another letter. 'A' becomes 'O'.

**(d) Shift Cipher:**

**i. "CYBERSECURITY" with key 12:**

- C(2) + 12 mod 26 = O(14)
- Y(24) + 12 mod 26 = K(10)
- B(1) + 12 mod 26 = N(13)
- E(4) + 12 mod 26 = Q(16)
- R(17) + 12 mod 26 = D(3)
- S(18) + 12 mod 26 = E(4)
- E(4) + 12 mod 26 = Q(16)
- C(2) + 12 mod 26 = O(14)
- U(20) + 12 mod 26 = G(6)
- R(17) + 12 mod 26 = D(3)
- I(8) + 12 mod 26 = U(20)
- T(19) + 12 mod 26 = F(5)
- Y(24) + 12 mod 26 = K(10)

Ciphertext: oknqdeqogdufk

**ii. "GTJCYPTX" with key 15:**

- G(6) - 15 mod 26 = R(17)
- T(19) - 15 mod 26 = E(4)
- J(9) - 15 mod 26 = u(20)
- C(2) - 15 mod 26 = N(13)
- Y(24) - 15 mod 26 = J(9)
- P(15) - 15 mod 26 = A(0)
- T(19) - 15 mod 26 = E(4)
- X(23) - 15 mod 26 = I(8)

Plaintext: REUNJAEI

**Question 5**

**(b) OSI and TCP/IP:**

**ii. Layer Services and Protocols:**

| Services Provided                           | Name of Layer | Examples of protocols                    |
| ------------------------------------------- | ------------- | ---------------------------------------- |
| Connection and connectionless communication | Transport     | TCP, UDP                                 |
| Error Detection and Correction              | Data Link     | Ethernet, PPP                            |
| Session check-pointing and recovery         | Session       | PPTP (Point-to-Point Tunneling Protocol) |
| Encryption                                  | Presentation  | SSL/TLS                                  |
| Signal Multiplexing                         | Physical      | (Not a layer function)                   |
| Process to process delivery                 | Transport     | TCP, UDP                                 |

**Question 6**

**(a) Protocol Functions:** (Focusing on the new ones)

- **i. TCP (Transmission Control Protocol):** Connection-oriented, reliable, ordered delivery, flow control, congestion control.
- **ii. SNMP (Simple Network Management Protocol):** Used for network monitoring and management.
- **iii. ICMP (Internet Control Message Protocol):** Used for network diagnostics and error reporting (e.g., ping).
- **iv. RPC (Remote Procedure Call):** Allows a program on one computer to execute a procedure or function on a different computer.
- **v. RARP (Reverse Address Resolution Protocol):** Resolves MAC addresses to IP addresses (obsolete).

**(b) Differentiations:** (Focusing on the new ones)

**(iii) Mesh vs. Star Topology:**

- **Mesh:** Every device connected to every other device (or most devices). Redundant paths, high fault tolerance, expensive.
- **Star:** All devices connect to a central hub/switch. Easy to manage, single point of failure.

