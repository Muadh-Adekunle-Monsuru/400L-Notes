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

Analog Signal Processing: Any signal processing conducted on an analog signal
Components that helps in 
Capacitor, resistors, inductors 

Tools used:
Processing:

A system behavior can be mathematically modelled and is represented the time domain as h(t) and in the frequency domain as H(s) where s is a complex number in form of $s = a + ib$ or $s = a+jb$ in electrical engineering terms. Electrical engineers use j because current is represented by the variable $i$. input signals are usually called x(t) or X(s) and output signals are usually called y(t) or Y(S)

Convolution:
This is the backs component processing that state an input signal and it can be combined with the system function to find the output signal. It is the integral of the product of two waveform after one has reversed and shift, the symbol for convolution
![[Pasted image 20241216094208.png|200]]

Fourier Transform
It is a function that forms a signal or system in the time domain into the frequency domain but it only works for certain one. The constraint for which systems or signals can be tranform on the fourier transform
![[Pasted image 20241216094518.png|200]]
most of the time the fourier tranform integral isnt used to determine the transform usually a table of transform pairs is used to find the fourier transform of a signal or a system. The inverse of the fourier transform is used to go from frequency domain to time domain each signal or system that can be transported has a unique fourier transform, there is only one time signal and one frequency signal that goes together.

Time domain: A plot in the time domain shows the magnitude of a signal at a point in time
Frequency domain: This is the domain that engineering are glad exists. . It's unfamiliar to most
people, but makes the math associated with analog signal processing
much easier than if it's analyzed in the time domain. a plot in the frequency domain shows either the phase shift or the magnitude of a signal at each frequency that. This can be found by taking the fourier transform of a time signal and are ploted similarly bode plot.

Impulse: A signal that has an infinite magnute and an infinite simally narrow width with an area under it of 1 and centered at 0.  An impulse can be represented as an infinite sum of sinusoid that include all possible frequencies, it is not in reality possible to generate such a signal but it can be sufficiently approximated with a large amplitude, narrow pulse, to produce the theortical impulse response in a network to a high degree of accuracy, the symbol for an impulse is δ(t) if an impulse is used as an input to a system the output is known as the impulse response because all possible

---
Guided Media: Pg  93
Guided media, which are those that provide a conduit from one device to another, include twisted-pair cable, coaxial cable, and fiber-optic cable. A signal traveling along any of these media is directed and contained by the physical limits of the medium. Twisted-pair and coaxial cable use metallic (copper) conductors that accept and transport signals in the form of electric current. Optical fiber is a cable that accepts and transports signals in the form of light.