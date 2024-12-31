### Overview of Signal and Data Transmission Concepts
https://www.slideshare.net/slideshow/wmcn-ch2/8427022

#### Signal Types:
1. **Analog Signal**: 
   - A continuously varying electromagnetic wave.
   - Propagates over various media.
   - Signal intensity changes smoothly without interruption.

2. **Digital Signal**: 
   - A sequence of voltage pulses transmitted over wired media.
   - Uses constant levels to represent binary data:
     - Binary 0: Constant positive voltage level.
     - Binary 1: Constant negative voltage level.

---

#### Components of a Communication System:
- **Transmitter**: Converts data into a transmittable signal.
- **Receiver**: Converts received signals back into data.
- **Communication**: Involves electromagnetic waves.
- **Medium**: Carries data; categorized as:
  - **Guided Media**: Twisted pair, optical fiber, coaxial cable.
  - **Unguided Media**: Air, water, vacuum.
  
**Communication Links**:
- **Direct Link**: Point-to-point or multi-point connection.

---

### Time Domain Concept
- Signals are analyzed as functions of time.
- **Analog Signals**: 
  - Continuous variation of intensity over time.
  - No breaks or interruptions.
- **Digital Signals**: 
  - Maintain constant intensity levels that shift discretely.
  - Transition periods are brief.

**Periodic Signals**:
- Repeat the same pattern over time.

**Wavelength**: The distance a signal wave travels to complete one cycle.

---

### Frequency Domain Concept
- Signals consist of multiple frequencies.
- **Spectrum**: The range of frequencies in a signal.
- **Bandwidth**: 
  - The difference between the highest and lowest frequencies in a channel.
  - Larger bandwidth allows higher transmission speeds.
  - Types:
    - **Absolute Bandwidth**: Full width of the spectrum.
    - **Effective Bandwidth**: Narrow frequency range containing most signal energy.

---

### Data and Signal Transmission:
1. **Data**: Entities conveying meaning or information.
2. **Signals**: Electrical or electromagnetic representations of data.
3. **Transmission**: Communication by propagating and processing signals.

#### Types of Data:
- **Analog Data**: Continuous values (e.g., sound, video).
- **Digital Data**: Discrete values (e.g., text, integers).

#### Analog vs. Digital Transmission:
- **Analog Transmission**:
  - Does not consider content integrity.
  - Signals weaken over distance; amplifiers boost signals (and noise).
- **Digital Transmission**:
  - Focuses on data integrity.
  - Uses repeaters to eliminate noise and maintain signal quality.

#### Advantages of Digital Transmission:
1. Digital technology.
2. Data integrity.
3. Capacity utilization.
4. Security and privacy.
5. Integration of diverse systems.

---

### Transmission Impairments:
1. **Attenuation Distortion**:
   - Signal strength decreases with distance.
   - Guided media: Exponential decay.
   - Unguided media: Affected by atmospheric conditions.
2. **Delay Distortion**:
   - Propagation velocity varies with frequency.
   - Causes intersymbol interference, limiting maximum bit rates.
3. **Noise Distortion**:
   - Unwanted signals introduced during transmission.
   - Types:
     - Thermal noise.
     - Intermodulation noise.
     - Cross-talk.
     - Impulse noise.

---

### Data Transmission Modes:
- **Parallel Mode**:
  - Multiple bits transmitted per clock cycle.
- **Serial Mode**:
  - Single bit transmitted per clock cycle.
  - Types:
    - **Asynchronous**: No synchronization between sender and receiver.
    - **Synchronous**: Synchronized transmission.
    - **Isochronous**: continuous and consistent timing.

![[Pasted image 20241209121604.png]]


---
==Page 63 CIT 303==
### **Analog Signal Processing**
- **Definition**: The manipulation or analysis of signals that are continuous in time and value (analog signals).
- **Components Involved**: 
  - **Capacitors**, **resistors**, and **inductors** are key components in analog signal processing circuits.

---

### **Mathematical Representation**
- **System Behavior**: 
  - In the **time domain**, it is represented as $h(t)$.
  - In the **frequency domain**, it is represented as $H(s)$, where $s = a + jb$ (complex number).  
    - Engineers use $j$ instead of $i$ because $i$ commonly represents current in electrical engineering.

- **Input Signals**:
  - Represented as $x(t)$ in the time domain or $X(s)$ in the frequency domain.
- **Output Signals**:
  - Represented as $y(t)$ in the time domain or $Y(s)$ in the frequency domain.

---

### **Key Concepts**

1. **Convolution**:
   - A mathematical operation that combines an input signal with the system’s function to produce an output signal.
   - Formula: It is the integral of the product of two functions, one reversed and shifted.

2. **Fourier Transform**:
   - Converts a signal from the **time domain** to the **frequency domain**.
   - **Constraints**: Only certain types of signals/systems can be transformed using the Fourier Transform.
   - **Practical Use**:
     - Instead of solving the integral every time, engineers use tables of Fourier Transform pairs.
     - The **Inverse Fourier Transform** is used to switch back from frequency domain to time domain.

---

### **Domains in Signal Processing**
1. **Time Domain**:
   - Shows how the signal changes over time (e.g., a waveform).
2. **Frequency Domain**:
   - Represents the signal in terms of its frequency components.
   - Visualized with tools like **Bode plots**, which show magnitude and phase shift across frequencies.

---

### **Impulse**
- **Definition**: A theoretical signal with:
  - Infinite magnitude,
  - Infinitely narrow width,
  - Total area under the curve = 1.
- **Properties**:
  - Represents all possible frequencies combined.
  - Symbol: $\delta(t)$.
  - **Impulse Response**: If an impulse is the input to a system, the resulting output is called the system's impulse response.
- **Practical Approximation**: Approximated using high-amplitude, narrow pulses in real-world applications.

---
### **Guided Media** (Pg. 93)

**Definition**: Guided media are physical pathways that direct and contain signals from one device to another.  

---

### **Types of Guided Media**  
1. **Twisted-Pair Cable**:  
   - Made of metallic (copper) conductors.  
   - Transports signals as **electric current**.  

2. **Coaxial Cable**:  
   - Also uses metallic (copper) conductors.  
   - Transmits signals in the form of **electric current**.  

3. **Fiber-Optic Cable**:  
   - Uses optical fibers to transport signals.  
   - Signals are carried in the form of **light**.  

---

#### **Characteristics**:  
- Signals are **directed** and **contained** by the physical boundaries of the medium.