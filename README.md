# Linear Integrated Circuits Lab Report
# Experiment 1: ANALYSIS OF CS AMPLIFIER
# Circuit 1
# Introduction
A Common Source (CS) amplifier, optimized for low-power applications, is designed and analysed using a 180nm TSMC MOSFET in LTSpice. To evaluate the amplifier's DC operating point, voltage gain, bandwidth, and power consumption, it employs data from DC, AC and transient analyses while operating at VDD = 1.8V and with a 50uW power budget. Low-power VLSI systems are made more efficient with a combination of high gain and wide bandwidth, which minimizes power consumption.
# Aim
 To analyse the common source amplifier using 180nm tsmc  cmos n-mosfet for a given V_DD = 1.8V & determine bandwidth , gain, DC operating point, power and draw its frequency response.
# Component required 
* 180nm tsmc nmos
* Resistor
* Voltage Supply
# Theory
The MOSFET structure has become the most important device structure in the Electronics industry. It dominates the integrated circuit technology in Very Large Scale Integrated (VLSI) digital circuits based on n-channel MOSFETs and Complementary n- Channel and p-channel MOSFETs (CMOS). The technical importance of the MOSFET results from Its low power consumption, simple geometry, and small size, resulting in very high packing Densities and compatibility with VLSI manufacturing technology. Two of the most popular Configurations of small-signal MOSFET amplifiers are the common source and common drain Configurations. The common source circuit is shown below. The common sources, like all MOSFET amplifiers, have the characteristic of high input impedance. High input impedance is Desirable to keep the amplifier from loading the signal source. This high input impedance is Controlled by the bias resistor). Normally the value of the bias resistors is chosen as High as possible. However, too big a value can cause a significant voltage drop due to the gate Leakage current. A large voltage drop is undesirable because it can disturb the bias point. For Amplifier operation the MOSFET should be biased in the active region of the characteristics. 
# Circuit Design:
![circuitddd](https://github.com/user-attachments/assets/63ecf804-7d7b-4316-ad6c-c4fc1b3521bd)


# Given values
Given that V_DD = 1.8 V, Power budget = 50µW and 180nm tsmc nmos.

Let's assume the values of RD, such that the FET should be in **SATURATION REGION**

i.e, V_GS > V_TH  and V_DS > V_OV.

**Assumed Value**

**Resister Value**

RD = 2k ohm

**To Find Current ID**

P = V_DD × ID

ID = 50µW / 1.8V

ID = 27.77 µA

**To get this current W and L should be 1.72 µm and 1.82 µm respectively**

# Transient Analysis

**Input Characteristics:**
![T1](https://github.com/user-attachments/assets/2ee00ab2-c1b3-4111-84fc-bdb275e00332)

**Output Chracteristics:**
![T2](https://github.com/user-attachments/assets/42ffc16c-0ede-4822-b4c0-347abbe771eb)

**Input and Output Chracteristics:**
![correct_ana](https://github.com/user-attachments/assets/7ba6db6a-0a9a-4a87-a511-6b620717483e)


# DC Analysis

![DCDC](https://github.com/user-attachments/assets/fb714344-a805-449c-bdd8-118016f9eedf)

# AC Analysis

**Vout/Vin in dB**

![AC(Vout_Vin)](https://github.com/user-attachments/assets/742e24ac-0f0e-403a-a5f5-4650cfa96e91)

# Result

# Extracting Parameters Using LTspice

**DC OPERATING POINTS**

![dcop](https://github.com/user-attachments/assets/fe3e8d2e-98c4-4cb3-9ecb-5d5f265a0a2a)

**POWER DISSIPIATION**

Vin = 0 W

VDD = 50.2 µW

RD = 5.02 µW


**GAIN in dB**

Av = Vout / Vin

Av ~ 42dB

**DC ANALYSIS**

Conditions for nmos to be in Saturation Region  V_GS > V_TH , V_DS > V_OV

VTH = 0.36 v (given in nmos model), VDD = 1.8 v, VG= 0.675 v, VS = 0.026 v, VD = 1.72 v.

V_GS = VG – VS

V_GS = 0.675 – 0

V_GS = 0.675 v

Hence VGS > VTH 

V_OV = VGS – VTH

V_OV = 0.675 – 0.36

V_OV = 0.315 v

V_DS = VD – VS 

V_DS = 1.72 – 0

V_DS = 1.72 v

Hence V_DS > V_OV 

Therefore fet is in Saturation Region.

# Inference

DC Operating Point Analysis:
The transistor operates within the saturation region if , it ensuring right amplification.

**DC Sweep Analysis:**
By simulation I saw the transfer characteristics of  V_GS in DC Analysis. 

**AC Analysis (Gain in dB):**
By Simulation I saw the frequency response of Cs amplifier and learnt how to find Gain 

**Transient Analysis:**
By Simulation I saw the output waveform and input waveform and output waveform have minimum distortion. 

# Circuit 2

# Introduction

A Common Source (CS) amplifier, optimized for low-power applications, is designed and analysed using a 180nm TSMC MOSFET in LTSpice. To evaluate the amplifier's DC operating point, voltage gain, bandwidth, and power consumption, it employs data from DC, AC and transient analyses while operating at VDD = 1.8V and with a 50uW power budget. Low-power VLSI systems are made more efficient with a combination of high gain and wide bandwidth, which minimizes power consumption.

# Aim

 To analyse the common source amplifier using 180nm tsmc  cmos n-mosfet for a given V_DD = 1.8V & determine bandwidth , gain, DC operating point, power and draw its frequency response.

 # Component required 
 
* 180nm tsmc nmos
* 180nm tsmc pmos
* Voltage Supply

# Theory

This circuit depicts a CMOS inverter, a fundamental building block in digital logic. It consists of a PMOS (M2) and NMOS (CMOSN) transistor connected in series. When the input (V3) is low, the PMOS is ON, pulling the output (V1) high. Conversely, when the input is high, the NMOS is ON, pulling the output low. This creates an inversion function. The sine wave inputs (SINE) with AC analysis commands (AC 1) suggest examining the circuit's frequency response and behavior with varying input signals. The 1.8V source represents the supply voltage for the CMOS logic.

# Circuit Design:
![Circuit_2](https://github.com/user-attachments/assets/22e5862c-7297-4b1a-b3cd-79a3782dde43)



# Given values
Given that V_DD = 1.8 V, Power budget = 50µW and 180nm tsmc nmos and pmos.

Let's assume the values of W and L, such that the FET should be in **SATURATION REGION**

i.e, V_GS > V_TH  and V_DS > V_OV.

**To Find Current ID**

P = V_DD × ID

ID = 50µW / 1.8V

ID = 27.77 µA

**W and L values for PMOS(M1)**

![WandL of pmos cir2](https://github.com/user-attachments/assets/28a9703d-f9e4-4378-9bc5-5b1e591527a6)


**W and L values for NMOS(M2)**

![WandL of nmos cir2](https://github.com/user-attachments/assets/2e0884e0-2996-49af-8a8b-114525bb633e)


# Transient Analysis

**Input Characteristics:**

![input_trs cir2](https://github.com/user-attachments/assets/0ba37800-af72-47ba-b082-d8eb837a4535)


**Output Chracteristics:**

![output_trs cir2](https://github.com/user-attachments/assets/4ab1f59d-d1ac-4da7-afd5-5f4671b5a4d2)


**Input and Output Chracteristics:**

![transient_analysis cir2](https://github.com/user-attachments/assets/50057fbb-7a1c-4b2a-9432-f204897366e8)


# DC Analysis

![DC operation for cir2](https://github.com/user-attachments/assets/3ff56640-fbc4-4b8e-b72a-0fa1928391e2)

**V_gs > Vth and V_ds > V_dsat**

**i.e, 0.9V > 0.6V and 0.399V > 0.293V**

**By this analysis we can say that Fet is in Saturation Region**

# DC Sweep Analysis

![DC_analysis cir2](https://github.com/user-attachments/assets/fd4668f5-cf0e-45c0-a147-4f37c6be3de4)


# AC Analysis

**Vout/Vin in dB**

![AnalysisOfac cir2](https://github.com/user-attachments/assets/7e259156-f971-41a1-8889-d3a5a19abe7e)


# Result

# Extracting Parameters Using LTspice

**DC OPERATING POINTS**

![DC_operating_region cir2](https://github.com/user-attachments/assets/e1071f01-2737-4d5c-bf5f-854c2266eaf7)


**POWER DISSIPIATION**

Vin = 0 W

VDD = 49.84 µW

M1 = 38.50 µW

M2 = 10.98 µW


**GAIN in dB**

Av = Vout / Vin

Av ~ 29dB

# Inference

DC Operating Point Analysis:
The transistor operates within the saturation region if , it ensuring right amplification.

**DC Sweep Analysis:**
By simulation I saw the transfer characteristics of  V_GS in DC Analysis. 

**AC Analysis (Gain in dB):**
By Simulation I saw the frequency response of Cs amplifier and learnt how to find Gain 

**Transient Analysis:**
By Simulation I saw the output waveform and input waveform and output waveform have minimum distortion. 
