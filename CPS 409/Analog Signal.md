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