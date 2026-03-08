# 📡 Design of a 2.45 GHz RF Receiver in CMOS 45nm Technology

<p align="center">
RF Receiver Front-End Design for ISM Band Wireless Communication
</p>

---
<p align="center">
	
## 👨‍💻 Authors
</p>
<p align="center">
	
- **Azad Hossain Saykat** – 021221017  
- **Sazzad Hossen** – 021221026  
- **Suvom Karmakar** – 021221027  
- **Md. Tahman Hossain** – 021221099  
</p>

<p align="center">
<img width="258" height="234" alt="Image" src="https://github.com/user-attachments/assets/ed3bcb05-66a4-4548-b233-5ff860243f1a" />>
</p>
Department of Electrical and Electronic Engineering  
United International University (UIU)  
Dhaka, Bangladesh  

Capstone Project – 2026

---

# 📖 Abstract

The increasing demand for compact and power-efficient wireless communication systems has accelerated the development of integrated **RF receiver architectures**.

This project presents the **design and simulation of a 2.45 GHz RF receiver front-end implemented in CMOS 45 nm technology**. The proposed architecture integrates the following fundamental RF blocks:

- Band Pass Filter (BPF)
- Low Noise Amplifier (LNA)
- Mixer
- Low Pass Filter (LPF)

The entire system was designed and verified using **Cadence Virtuoso**.

### Achieved Performance

| Parameter | Result |
|----------|-------|
| Operating Frequency | **2.45 GHz** |
| Technology | **CMOS 45nm** |
| Total Gain | **≈ 50 dB** |
| THD | **1.319 %** |
| Power Consumption | **6.261 mW** |

The obtained results demonstrate an effective trade-off between **gain, linearity, and power efficiency**, making the design suitable for **ISM band wireless communication applications such as WiFi, Bluetooth, and IoT systems**.

---

# 📡 System Architecture

The proposed RF receiver follows a **direct conversion (homodyne) architecture**, which directly converts the RF signal to baseband.

```
RF Input → Bandpass Filter → Low Noise Amplifier → Mixer → Low Pass Filter → Baseband Output
```

---

# 🧠 RF Receiver Block Diagram

<p align="center">
<img width="636" height="339" alt="Image" src="https://github.com/user-attachments/assets/116225fe-3745-421e-9a20-dde505ecf96b" />
</p>

---

# 🔧 Design Methodology

The RF receiver was designed using a **modular design approach**.

Each block was first designed individually, optimized through simulations, and then integrated into the complete system.

### Design Flow

1. Literature Review
2. Specification Definition
3. Circuit Design
4. Device Characterization (gm/ID methodology)
5. Cadence Virtuoso Simulation
6. System Integration
7. Performance Evaluation

---

# 🔬 RF Receiver Sub-Blocks

---

# 1️⃣ Band Pass Filter (BPF)

The BPF is placed directly after the antenna to select the desired RF channel while suppressing out-of-band interference.

### Key Features

- Center Frequency: **2.45 GHz**
- Active Inductor Implementation
- Differential Structure
- High Selectivity

### BPF Schematic

<p align="center">
<img width="902" height="385" alt="Image" src="https://github.com/user-attachments/assets/8a2d48b9-00cb-4e86-a1c9-56fa9ca7f59b" />
</p>

### BPF DC Analysis

<p align="center">
<img width="904" height="289" alt="Image" src="https://github.com/user-attachments/assets/2175b88c-2601-41b2-ab7f-0091f7d549d2" />
</p>

<table>
  <tr>
    <td align="center">
     <img width="469" height="349" alt="Image" src="https://github.com/user-attachments/assets/ccc399f0-35ca-484c-8d10-e370ada04038" /><br>
      DC Analysis Schematic Block 1
    </td>
    <td align="center">
      <img width="810" height="420" alt="Image" src="https://github.com/user-attachments/assets/1d08f194-edd4-459a-b83d-c7438a22127b" /><br>
       DC Analysis Schematic Block 2
    </td>
  </tr>
  <tr>
    <td align="center">
     <img width="804" height="739" alt="Image" src="https://github.com/user-attachments/assets/140ff91b-2b30-43a1-b75c-36373e25586f" /><br>
       DC Analysis Schematic Block 3
    </td>
    <td align="center">
      <img width="814" height="609" alt="Image" src="https://github.com/user-attachments/assets/dffc2633-7386-452f-8ed3-40a8a2b38bb8" /><br>
       DC Analysis Schematic Block 4
    </td>
  </tr>
</table>

### BPF AC Analysis

## 3dB Point
<img width="756" height="505" alt="Image" src="https://github.com/user-attachments/assets/ef5648af-bd6d-4004-b1ef-60cb94fb42c4" />
</p>

## Center Frequency at 2.45GHz
<p align="center">
<img width="782" height="487" alt="Image" src="https://github.com/user-attachments/assets/8bdb91ca-39f7-4c71-b7af-10c44621e71a" />
</p>

### Design Method

The filter was designed using **gm/ID methodology**, enabling efficient transistor sizing while optimizing:

- Transconductance efficiency
- Power consumption
- RF performance

---

# 2️⃣ Low Noise Amplifier (LNA)

The **LNA amplifies weak RF signals** received from the antenna while minimizing noise.

### Topology

Cascode Common Source with **Inductive Source Degeneration**

### LNA Specifications

| Parameter | Value |
|---------|------|
| Supply Voltage | 1.2 V |
| Power Consumption | 2 mW |
| Gain | 15 – 20 dB |
| Noise Figure | < 2 dB |
| Operating Frequency | 2.45 GHz |

### LNA Schematic

<p align="center">
<img width="901" height="546" alt="Image" src="https://github.com/user-attachments/assets/b6d22c19-85ab-4512-a38f-1cb94d1919a3" />
</p>
### DC Analysis

<p align="center">
<img width="654" height="410" alt="Image" src="https://github.com/user-attachments/assets/c7aa153c-f076-4d46-a834-bc7428707bf3" />
</p>

### AC Analysis
Maximum Gain at 2.45GHz = 23.47"dB"
<p align="center">
<img width="702" height="260" alt="Image" src="https://github.com/user-attachments/assets/b441667b-fa6b-4fe7-9c65-02350c5cf9e6" />
</p>

### Transient Analysis
Gain Calculation from transient analysis,
A_v=20 log_10⁡〖((49.541+48.414)mV/(477.318-461.314)mV)〗
A_v=16.3 dB 
<p align="center">
<img width="785" height="594" alt="Image" src="https://github.com/user-attachments/assets/94a345b2-31d6-443e-8ed0-f35d52fff2cd" />
</p>

### S-Parameter Analysis
S-parameters are studied to investigate the input and output reflections, return loss, and signal integrity of the system. The S-parameter plots for S11 (Input Reﬂection Coefﬁcient), S22 (Output Reﬂection Coefﬁcient), without losing general but fundamental observation, are below mentioned: S21 (Forward Transmission Gain), and S12 (Reverse Trans- mission Gain).

<p align="center">
<img width="901" height="568" alt="Image" src="https://github.com/user-attachments/assets/452621d1-6080-47bb-9b47-16fb4e4df80a" />
</p>

### Stability & Noise Figure Analysis
The noise figure analysis checks the noise contribution of the LNA and stability check the oscillation occur, or not.
<p align="center">
<img width="796" height="458" alt="Image" src="https://github.com/user-attachments/assets/5c1ae5dc-d1f9-4a92-8d97-f9d81e8b0167" />
</p>

### Performance Analysis
The simulation data will be matched to the LNA specifications provided in the table below
## Table: LNA Specification vs Simulation Results

| Parameter | Specification | Simulation Result |
|-----------|---------------|-----------------|
| Supply Voltage | 1.2 V | 1.2 V |
| Frequency | 2.45 GHz | 2.45 GHz |
| Noise Figure (NF) | < 2 dB | 2.3 dB |
| Gain | 15–20 dB | 23 dB |
| S11 (Input Return Loss) | ≤ -10 dB | -11 dB |
| S22 (Output Return Loss) | ≤ -10 dB | -12 dB |
| S21 (Forward Gain) | 15–20 dB | 20 dB |
| S12 (Reverse Isolation) | ≤ -25 dB | -42 dB |

### Key Advantages

- Improved gain
- Reduced Miller capacitance
- Better isolation
- Lower noise figure

---

# 3️⃣ Mixer

The mixer performs **frequency down-conversion**, translating the RF signal to baseband.

### Mixer Type

Gilbert Cell Active Mixer

### Function

```
IF = RF − LO
```

Where:

- RF = Input signal
- LO = Local oscillator signal
- IF = Intermediate Frequency

### Mixer Schematic

<p align="center">
<img width="806" height="666" alt="Image" src="https://github.com/user-attachments/assets/14f0beed-931e-4152-9c34-2bfcf5584254" />
</p>

### DC Analysis

<p align="center">
<img width="881" height="461" alt="Image" src="https://github.com/user-attachments/assets/d8615118-caff-407a-b58b-984dcc86f912" />
</p>
### Mixer Simulation Test Bench

<p align="center">
<img width="887" height="392" alt="Image" src="https://github.com/user-attachments/assets/2a8db215-aa2f-4e5d-b148-56d2098ce04e" />
</p>


### Transient Analysis
A transient analysis for the mixer design is necessary to assess the time-domain behavior of the system. The proposed approach assists the validation of the frequency conversion performance, signal distortion and overall behavior under different input conditions.
<p align="center">
<img width="928" height="359" alt="Image" src="https://github.com/user-attachments/assets/c77fa19b-360d-4ee1-a0ff-154e7f16ca9d" />
</p>
<p align="center">
<img width="922" height="515" alt="Image" src="https://github.com/user-attachments/assets/46809088-20a2-479e-8e11-dce6767b35e6" />
</p>
RF frequency fRF = 2.45 GHz LO frequency fLO = 2.43 GHz
The sum frequency is: fSUM = fRF + fLO = 4.88 GHz (This is the carrier) 
The difference frequency is: fIF = |fRF − fLO| = 20 MHz (This is the envelope)
### Voltage Conversion Gain vs LO Signal Power
The voltage conversion gain is a figure of merit which demonstrates how efficient the mixer converts the input RF signal at desired IF. The voltage conversion gain is plotted against the LO signal power in the figure below.
<p align="center">
<img width="824" height="402" alt="Image" src="https://github.com/user-attachments/assets/1eab7328-96d3-4830-909f-88c8479c9cab" />
</p>

The conversion gain individually obtained with the mixer is small than its expected one, but it would be improved by design modification. However, both the isolation and harmonic suppression were valid and therefore the overall performance was presented as acceptable
---

# 4️⃣ Low Pass Filter (LPF)

The LPF removes high-frequency mixing products and preserves only the baseband signal.

### LPF Implementations

- Passive LPF
- Active LPF
- 2nd Order Gm-C Filter

### 2nd Order Low Pass Filter Schematic Diagram

<p align="center">
<img width="975" height="356" alt="Image" src="https://github.com/user-attachments/assets/4867238a-c1f7-42a9-b1bb-7c54184cd9a5" />
</p>

### 2nd Order Low Pass Filter DC analysis

<p align="center">
<img width="899" height="292" alt="Image" src="https://github.com/user-attachments/assets/abfffcdd-bb99-4478-ae29-db66d8d4339d" />
</p>

### 2nd Order Low Pass Filter AC analysis

<p align="center">
<img width="755" height="376" alt="Image" src="https://github.com/user-attachments/assets/04b996ea-6680-4965-b9ab-7472f981b738" />
</p>
---

# 🔗 Integrated RF Receiver

After individual block optimization, the full RF receiver was integrated.

<p align="center">
<img width="904" height="201" alt="Image" src="https://github.com/user-attachments/assets/dc8d12b2-ddb1-4ab6-9cad-9d613d38cb1a" />
</p>

---

# 📊 Simulation Results
### Transient Analysis

<p align="center">
<img width="923" height="250" alt="Image" src="https://github.com/user-attachments/assets/da3c3bd0-b756-407f-b053-e11ab0f616ae" />
</p>
<p align="center">
<img width="924" height="312" alt="Image" src="https://github.com/user-attachments/assets/bbab0bab-1af0-467d-9ed4-b138529990f9" />
</p>
<p align="center">
<img width="901" height="536" alt="Image" src="https://github.com/user-attachments/assets/bf039dc8-d2f8-4a93-9662-fa670d2a7bc7" />
  
### Gain Response
Total Conversion Gain:
Using the peak-to-peak voltages of the input and final recovered output, we calculated the overall voltage conversion gain (Av) for the cascaded receiver. The peak-to-peak input voltage is 100μV and the recovered output from the transient results is 31.5mV.

A_v=V_out(peak_ to_peak) /V_in(peak_ to_peak)  =(31.5×10^(-3))/(100×10^(-6) )≈315
And when this linear voltage gain is converted to decibels, the result is quite impressive: an overall system gain of 50 dB.


---

### Frequency-Domain (DFT) Analysis

To ensure that the incoming signal was correctly translated and any unwanted frequencies rejected, a Discrete Fourier Transform (DFT) of each major node was taken.
<p align="center">
<img width="923" height="513" alt="Image" src="https://github.com/user-attachments/assets/abce2571-afb6-41b1-a9ad-302c74ce9031" />
</p>
•	The spectrum of the original message shows a very sharp peak at 10 MHz.
•	Observe at the BPF and LNA outputs, how well centered around the 2.45 GHz carrier frequency, is our spectrum thereby demonstrating frontend selectivity.
•	 The dft_mixer_output shows the baseband IF component near 10 MHz and high-frequency mixing products (e.g., in the vicinity of 4.9 GHz)
•	In the end, lpf_output spectrum shows that all the HF harmonics and LO leakage is perfectly suppressed, only 10 MHz baseband tone present. This verifies the success of our 3rd-order LPF design.

---


### System Linearity and SNR 

It was then cracked open to study the noise floor, and linear operating range of this receiver in this maximum performance assessment.
<p align="center">
<img width="891" height="512" alt="Image" src="https://github.com/user-attachments/assets/c6fb6b3f-a0d5-4f6b-bbc8-378d5935f69e" />
</p>
Signal-to-Noise Ratio (SNR): Measurement of noise performance was done with Power Spectral Density (PSD) investigation. The signal power was measured at -107.85dB and the noise floor was at -156.5db
SNR_dB = P_signal-P_noise = -107.85"dB"-(-156.5"dB" ) ≈ 49"dB" 

<p align="center">
<img width="874" height="455" alt="Image" src="https://github.com/user-attachments/assets/9e7fb361-0d82-46c8-a97f-47f0cb73a6a4" />
</p>
Linearity Range: Linearize to Extract the 1-dB Compression Point From 1μV to 1.3mV, and the receiver gives a nice linear response. After a certain point, approximately 1.3mV of input the active devices go into saturation (cut-off) and compress gain. Output Amplitude vs. Input Amplitude - Linearizing to Find the 1-dB Compression Point From 1μV to 1.3mV the receiver maintains a nice linear response. Beyond about 1.3mV of input, the active devices start to saturate (cut-off) and gain is compressed
---

### System Selectivity and Interference Rejection (FDM Analysis) 

In a more realistic wireless environment, the desired RF signal is always present along with many out-of-band jammers. An FDM scenario was obtained to evaluate how often frequency selectivity appeared at the receiver end and how resistant it was with respect to this interference.
## FDM Test Setup
A composite was used to input signal injected into the receiver instead of one carrier This signal had a wanted carrier at 2.45 GHz (a message signal at 15 MHz), with strong out-of-band interfering carriers centered at 5 GHz and 10 GHz, overlaid. The input was at a default amplitude of 100μV.
<p align="center">
<img width="901" height="417" alt="Image" src="https://github.com/user-attachments/assets/98b867c3-0389-4fdf-9ace-c6d3a213ff8f" />
</p>

## Frequency-Domain (DFT) Proof of Selectivity
The DFT analysis provides a tangible example of the filtering characteristics that are imparted by the receiver at each stage in the cascade:

•	Composite Input Spectrum: The input dft_massege spectrum is a clear representation of the three separate peaks, respectively containing the wanted signal at 2.46 GHz and two large interferers at about 5 GHz and 10 GHz.

•	Rejection to BPF Out-of-band: All the blockers at 5 GHz and 10 GHz are suppressed entirely on the dft_bpf_output node by Band-Pass Filter. Only pass through signal on 2.46 GHz It is very high Q-factor and chosen to develop LC matching and filtering topology.

•	SDF Isolation: As observed at spectrum lpf_output, a single isolated peak from the down converted mixer indicates that high-frequency LO leakages and interferers are completely brought out due to the 3rd-order LPF.

<p align="center">
<img width="901" height="419" alt="Image" src="https://github.com/user-attachments/assets/17c0bbc5-e713-4af7-b444-a9dec5285330" />
</p>

---
### Time-Domain (Transient) Signal Recovery 

The transient analysis also confirms system stability in the presence of FDM:

Frontend Filtering: The first bpf_input waveform is quite dense and distorted because it contains interleaving 2.45 GHz, 5 GHz and 10 GHz frequencies. But just after BPF (bpf_output), the waveform has returned to the recognizable "clean" envelope of a single frequency, modulated carrier.

Message Reconstruction: Even with the aggressive interference present at input only through the recovered output. We are able to construct a whisk clean 15 MHz sine wave.

Voltage Amplification: The recovered timing 15 MHz baseband signal on oscilloscope - peak to peak approx 100mV (somewhere between -50mv and +50mV). In addition, we see that the receiver not only provides very large rejection of blockers but it also delivers significant gain to the signal channel provided with a 100μV input.
## Transient Analysis
<p align="center">
<img width="890" height="336" alt="Image" src="https://github.com/user-attachments/assets/4c77d7f5-cee7-46af-b60d-6d7c437f2d7f" />
</p>

### I/Q (In-phase & Quadrature) Demodulation Architecture
The receiver uses an integral quadrature demodulation topology to accommodate the later modern complex modulation schemes (such as 16-QAM), by which data is radiated through phase and amplitude changes.

## I/Q Architecture Implementation
The amplified RF signal produced by the LNA progresses through two identical parallel paths as illustrated in the system schematic. A standalone active mixer is then followed by a low-pass filter on each branch.

## Schematic Design of the I/Q Structure
<p align="center">
<img width="902" height="227" alt="Image" src="https://github.com/user-attachments/assets/e7234fbf-e88d-4bac-a8d6-8bf6c13cfe18" />
</p>
In-phase (I) Channel: The desired phase reference is then provided to the upper mixer via a LO.
Quadrature (Q) Channel: The lower mixer is driven by an LO signal phase shifted with respect to the I-channel LO.

Orthogonal down-conversion thus enables the real and imaginary parts of any incoming complex RF wave to be separately mapped into quadrants.

### Single Tone I/Q Transient Response

<p align="center">
<img width="884" height="261" alt="Image" src="https://github.com/user-attachments/assets/6a1bec99-68c0-45db-81eb-05fabd2631e2" />
</p>
A single-tone test was performed to observe Time-Domain response of the I/Q channels as well as measure phase alignment.

•	The outputs received directly from the dual mixers (mixer_out_inphase and mixer_out_qphase) contain numerous high frequency components, which appear quite complex.

•	Both I (green) and Q (purple) channels are recovering nice clean baseband sinewaves after the respective Low-Pass Filters.

•	At a closer look with respect to time-domain plot it is Clearly visible that there is a distinct time lag where the two waves appear to reach their highest amplitude. The time lag was customized and tuned to a quarter of the cycle, which is an accurate phase difference needed for correct quadrature reconstruction.
 

---

### Gain and Phase Error Verification 

## Lissajous Pattern
<p align="center">
<img width="836" height="601" alt="Image" src="https://github.com/user-attachments/assets/223adf69-7199-4590-8901-d1da34fc0e8a" /> </p>

For data to be decoded properly by a quadrature receiver both the channels need to have the same gain and the phase difference between them needs to be strictly 90^∘. This was demonstrated mathematically by plotting a transient amplitude of I-channel and Q-channel in XY plot to form Lissajous curve.
	The plot you get is a continuous, perfectly symmetric circle.

This geometric circle is also the definitive validation for two of the most important figures of merit (FoM’s) that have been implemented in a receiver 0 dB gain mismatch (confirming that both matching LPF and Mixer provide exactly same value addition to the flow), and a 0deg. phase error assuring complete orthogonality. Gains would result in an ellipse and phase error would tilt the axis of that shape.



## Dynamic Phase Trajectory
While one variation (single-tone test with static phase transition) would produce a stationary circle, the QPSK Lissajous plot encodes time-varying changes in phase of the modulated digital signal.

## Lissajous Pattern for QPSK
<p align="center">
<img width="887" height="520" alt="Image" src="https://github.com/user-attachments/assets/3200e394-bf24-456c-848c-004aef3a79e8" /> </p>

•	This pattern creation represents the I-channel amplitude vs time and Q-channel amplitude vs time.
•	The optical paths arising evidently step from the signal quadrants 4- phase to another. Such symmetry is the key to ensure that the differential mixer correctly maps these sharp digital phase shifts without amplitude clipping and phase distortion.

## Signal Integrity and Eye Diagram

Eye Diagram: Eye diagrams are the most important measurement of a quality recovered digital signal, an eye diagram plots several symbol periods on top of each other to show how both channel noise and filter bandwidth impacts the digital pulses.

<p align="center">
<img width="866" height="341" alt="Image" src="https://github.com/user-attachments/assets/c71362d9-0faf-4764-a067-bef69105b214" /> </p>
•	The simulated eye diagrams for both the I and Q channels exhibit wide-open eyes.

•	A wide-open eye signifies that there is minimal Inter-Symbol Interference (ISI) and extremely low timing jitter in the recovered signal.

•	The good signal integrity indicates that the previously determined 20 MHz LPF cut-off is exactly optimized; it successfully attenuates the 2.44 GHz LO leakage and still provides enough bandwidth for the steep QPSK symbol transitions, allowing them to not smear out their edges. As a response, it assures a very accurate digital quantization procedure with nominal BER.
 

---
# 📈 System Performance

| Metric | Result |
|------|------|
| Operating Frequency | 2.45 GHz |
| Total Gain | 50 dB |
| Noise Figure | 2.3 dB |
| THD | 1.319 % |
| Power Consumption | 6.261 mW |

---

# 📊 Comparison With Previous Work

## RF Receiver Performance Comparison

| Category | Parameter | [1] | [2] | [3] | [4] | [5] | [6] | This Work |
|----------|-----------|------|------|-----|------|------|------|-----------|
| **Process** | Technology (nm) | - | 180 | 600 | 180 | 180 | 40 | 45 |
|  | Supply Voltage (V) | - | 1.5 | 3 | 1.8 | 1.5 | 1.1 | 1.2 |
| **System** | Frequency (GHz) | 2.4 | 24 | 2.4 | 24 | 2.42 | - | 2.45 |
|  | Total Gain (dB) | 35 | 14.5 | 20-Dec | 25 | - | - | 400 |
|  | Total Power (mW) | 40 | 45 | 100 | 25.2 | - | - | 6.261 |
| **LNA** | Gain (dB) | - | 15 | 14 | 14.7 | - | - | 23.03 |
|  | NF (dB) | - | 6 | 3.5 | 4.3 | - | - | 2.4 |
|  | Topology | - | Common Gate | Common Source Cascode | Transformer-Coupled | - | - | Common Source Inductive Degeneration |
| **Mixer** | Conv. Gain (dB) | - | 12.5 | 10 | 8.7 | - | - | - |
|  | Type | - | Active Gilbert Cell | Active Gilbert Cell | Current-Bleeding Mixer | - | - | Active Gilbert Cell |
| **BPF** | Bandwidth (MHz) | - | - | - | - | 38 | - | 20–100 (Tunable) |
|  | Power Consumption (mW) | - | - | - | - | 1.3 (Single Stage) | - | 1.63 (Differential) |
| **LPF** | Bandwidth (MHz) | - | - | - | - | - | 20 | 20 |
|  | Power Consumption (mW) | - | - | - | - | - | 2 | 0.2 |

The proposed design demonstrates improved **gain, noise performance, and reduced power consumption**.

---

# 🛠 Tools Used

- **Cadence Virtuoso**
- Spectre RF Simulator
- CMOS 45nm PDK
- MATLAB (for modulated signal generation and analysis)

---

# 📚 Applications

The designed RF receiver can be used in:

- WiFi Systems
- Bluetooth Devices
- IoT Communication
- Wireless Sensor Networks
- ISM Band Communication

---

# Conclusion

A **2.45 GHz RF receiver front-end** was successfully designed and simulated using **CMOS 45nm technology**.

The proposed architecture demonstrates:

- High gain
- Low noise figure
- Low power consumption
- Efficient RF signal processing

These characteristics make the receiver suitable for **modern wireless communication systems and IoT applications**.

---

# Reference
[1] M. Al-Rawi, “Design of 2.4 GHz Transceiver for Wireless Communication,” L. Forces Acad. Rev., vol. 24, no. 3, pp. 232–241, 2019
[2] X. Guan and A. Hajimiri, “A 24-GHz CMOS Front-End,” IEEE J. Solid-State Circuits, vol. 39, no. 2, pp. 368–373, 2004.
[3] B. Razavi, “CMOS RF receiver design for wireless LAN applications,” 1999 IEEE Radio Wirel. Conf. (RAWCON 99), 1999.
[4] C.-Y. Chu and others, “A 24GHz low-power CMOS receiver design,” in IEEE International Symposium on Circuits and Systems (ISCAS), 2025.
[5] A. Bhuiyan, “Design of a Band-Pass Filter in 0,18 $μ$m CMOS for 2,4 GHz Reader-Less RFID Transponder,” Teh. Vjesn. - Tech. Gaz., 2017.
[6] T. B. Kumar and others, “Design Automation of 5-T OTA using gm/ID methodology,” in 2019 IEEE Conference on Information and Communication Technology, 2019.
---
# Acknowledgement

Special thanks to our respected supervisors:

**Dr. Raqibul Mostafa**  
Professor, Department of EEE  
United International University  

**Md. Hasanuzzaman**  
Associate Professor, Department of EEE  
United International University  

---

# Contact

**Suvom Karmakar**  
EEE Graduate, United International University  

Email: **skarmakaruiu@gmail.com**
