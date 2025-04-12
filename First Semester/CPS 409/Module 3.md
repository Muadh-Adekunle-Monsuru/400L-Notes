### **Network Operating Systems (NOS)**

---
A **Network Operating System (NOS)** is specialized software designed to control Local Area Networks (LANs). It plays a pivotal role in enabling communication between computers, facilitating file transfers, and ensuring network security. PCs can either operate with or without a NOS:  

---
##### **PC with Network Operating System (NOS)**  
When a NOS is installed, it introduces a crucial software component known as the **Redirector**, which determines whether a command is intended for the local Operating System (OS) or for the network.  

**Workflow of a Command in a PC with NOS:**  
1. Commands from the application program are intercepted by the **Redirector**.  
2. Network commands are sent to the following layers:  
   - **NetBIOS (Network Basic Input Output System)** software.  
   - **LAN protocol software** (specific to the LAN type, such as Token Ring or Ethernet).  
3. The **LAN protocol software** translates commands for the **Network Interface Card (NIC)**.  
4. The NIC, a hardware component, connects the computer to the LAN. Modern NICs support multiple standards, such as 10BaseT and 100BaseT.  

---

##### **PC without Network Operating System (NOS)**  
In a PC without NOS, the system operates solely on its OS, such as **DOS** or **Windows**. Commands are executed locally through the **Basic Input Output System (BIOS)**, which translates program instructions into hardware commands.  

**Key Components of a PC without NOS:**  
- The OS handles requests to input/output devices like keyboards, printers, and disk drives.  
- The BIOS is stored in Read-Only Memory (ROM) and ensures compatibility between the OS and hardware.  

---

##### **3.3 Peer-to-Peer vs. Client/Server LANs**  

- **Peer-to-Peer LAN**:  
  - No dedicated server.  
  - All workstations are equal and share resources.  

- **Client/Server LAN**:  
  - A **server** manages resources and handles requests from **clients**.  
  - Clients request files or services, while the server processes and delivers them.  

---

##### **3.4 NOS Functions**  

- **File and Print Services**:  
  NOS enables transparent file transfers and print services, ensuring users can access shared resources without disruption.  

- **Network Monitoring**:  
  - Tracks user logins and enforces password policies.  
  - Detects and disables unauthorized access.  
  - Logs user activity and monitors email communications (where legally permissible).  

- **Traffic Analysis**:  
  NOS identifies network bottlenecks, traffic sources, and equipment failures, ensuring optimal performance.  

---

###  **Switching Technology**  

**Introduction:**  
Switching technology addresses the challenge of connecting multiple devices in a network efficiently. Instead of impractical point-to-point or bus topologies, switching uses nodes called switches to create temporary connections. These nodes can connect end systems (e.g., computers or phones) or facilitate routing between nodes.  

**Methods of Switching:**  
1. **Circuit Switching:** Establishes a dedicated path for the duration of a session.  
2. **Packet Switching:** Transfers data in packets. It includes:  
   - **Virtual-Circuit Networks**: Sets up a virtual path for subsequent packets.  
   - **Datagram Networks**: Independently routes each packet.  
3. **Message Switching:** Entire messages are stored and forwarded by each switch.  

**Switching Computers:**  
Switching is performed by specialized computers, such as the Lucent 4ESS and 5ESS, which manage large volumes of calls efficiently.  

**Structure of Switches:**  
1. **Circuit Switches:** Utilize:  
   - **Space-Division Switches**: Use crossbar or multistage switches, which reduce the number of required crosspoints.  
   - **Time-Division Switches**: Use Time-Slot Interchange (TSI) for multiplexing data.  

2. **Packet Switches:** Comprise:  
   - **Input/Output Ports**: Handle physical and data link layers, queue packets, and manage errors.  
   - **Routing Processor:** Determines the next hop and output port via table lookups.  
   - **Switching Fabric:** Transfers packets between input and output queues using mechanisms like crossbar or banyan switches.  

**Challenges and Improvements:**  
- **Blocking:** Occurs in multistage switches during heavy traffic but can be minimized using the Clos criteria.  
- **Optimization:** Time-space-time (TST) switches combine time and space switching to balance efficiency and delay.  
---
# Key Concepts in Cryptography

## Basic Terminology
- **Plaintext**: Original message before encryption
- **Ciphertext**: Transformed (encrypted) message
- **Cipher**: Encryption/decryption algorithms
- **Key**: Number(s) used by the cipher for encryption/decryption

## Two Main Categories of Cryptography

### 1. Symmetric-Key (Secret-Key) Cryptography
- Same key used for encryption and decryption
- Both sender and receiver share the key
- Examples: DES, AES, Triple DES

### 2. Asymmetric-Key (Public-Key) Cryptography
- Uses two different keys: public and private
- Public key is available to everyone
- Private key kept secret by owner
- Sender encrypts with receiver's public key
- Receiver decrypts with their private key

## Traditional Ciphers

### Substitution Ciphers
- **Monoalphabetic**: One-to-one character replacement
- **Polyalphabetic**: One-to-many character replacement
- Example: Caesar Cipher (shift cipher)

### Transposition Ciphers
- Reorders symbols rather than replacing them
- Changes position of characters without substitution
![[Pasted image 20250120182038.png]]
## Modern Ciphers

### Simple Components
- XOR Cipher
- Rotation Cipher
- S-box (Substitution box)
- P-box (Permutation box)

### Major Modern Algorithms

**DES (Data Encryption Standard)**
- 64-bit block size
- 56-bit key
- Uses 16 rounds of encryption

**AES (Advanced Encryption Standard)**
- Replaced DES as standard
- Key sizes: 128, 192, or 256 bits
- 10-14 rounds depending on key size

### Modes of Operation
1. **ECB (Electronic Code Book)**
   - Basic block-by-block encryption
   - Same plaintext blocks produce same ciphertext

2. **CBC (Cipher Block Chaining)**
   - Each block depends on previous block
   - More secure than ECB

3. **CFB (Cipher Feedback)**
   - Allows encryption of bits smaller than block size
   - Error propagation occurs

4. **OFB (Output Feedback)**
   - Similar to CFB but prevents error propagation
   - Each bit encrypted independently

## Asymmetric-Key Cryptography Algorithms

### RSA (Rivest, Shamir, Adleman)
- Most common public key algorithm
- Uses two keys: public (e) and private (d)
- Key Generation Process:
  1. Choose two large prime numbers (p and q)
  2. Calculate n = p × q (modulus)
  3. Calculate public key e and private key d
  4. Announce e and n publicly, keep d private

**Implementation**:
- Encryption: C = P^e mod n
- Decryption: P = C^d mod n
- Restriction: Plaintext value must be less than n
- Best suited for:
  - Short messages
  - Digital signatures
  - Encrypting symmetric keys
  - Authentication

### Diffie-Hellman
- Designed specifically for key exchange
- Allows two parties to create a shared secret key over public channels
- Process:
  1. Both parties agree on public numbers p (prime) and g
  2. Each party chooses private number (x and y)
  3. Exchange calculated values (R1 = g^x mod p, R2 = g^y mod p)
  4. Both parties can derive same secret key K

**Security Considerations**:
- Vulnerable to man-in-the-middle attacks
- Requires authentication to prevent intercepted communications
- Best used in combination with authentication schemes

## Key Comparison of Symmetric vs Asymmetric

### Symmetric-Key
- Same key for encryption and decryption
- Faster processing
- Better for large data volumes
- Requires secure key distribution

### Asymmetric-Key
- Different keys for encryption/decryption
- Slower processing
- Better for small data volumes
- Public key can be freely distributed
- Commonly used for:
  - Key exchange
  - Digital signatures
  - Authentication

## Security Best Practices
- Combine symmetric and asymmetric methods for optimal security
- Use authentication with key exchange protocols
- Choose appropriate key sizes for security level needed
- Consider computational resources when selecting algorithms
- Implement proper key management procedures
