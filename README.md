# CMOS-Circuit-Design-and-SPICE-Simulation-Using-Sky130 


# DAY1: Basics Of NMOS drain current (Id) vs drain to source voltage(Vds)


## Why do we need SPICE simulations?
## Circuit Design

Logic gates are made up of PMOS and NMOS transistors arranged in a particular fashion, and they perform specific tasks. For example, a CMOS inverter uses this arrangement to provide the functionality of an inverter.

---

## SPICE Simulation

In SPICE simulation, this circuit is fed with a waveform to identify its output characteristics. These characteristics depend on the behavior of NMOS and PMOS transistors. The output waveform obtained from the SPICE simulator determines the delay of the inverter.

---

## Role of W/L Ratio

Based on the value of this delay, we can tune the W and L values of the PMOS and NMOS transistors. The W/L ratio decides the current, which in turn determines the characteristics and the delay of the inverter. Therefore, to tune the delay, we adjust the W/L ratio using SPICE simulation.

---

## Importance of SPICE Simulation

SPICE simulation is important because, in VLSI, processes like physical design flow, clock tree synthesis, and crosstalk analysis are all built on the concept of delay. Without SPICE, there would be no way to define or analyze delay.

---

## Example

Logic gates are made up of PMOS and NMOS transistors arranged in a particular fashion to perform a specific task. A CMOS inverter is one such example, where the arrangement gives the functionality of an inverter. Using SPICE simulation, when the circuit is fed with a waveform, we can analyze the output characteristics and determine the delay. The W/L ratio of PMOS and NMOS transistors decides the current and, therefore, the delay. By tuning this ratio in SPICE, we can optimize the inverter’s delay.

---

<img width="3360" height="2100" alt="Screenshot 2025-09-23 at 1 53 28 PM" src="https://github.com/user-attachments/assets/ba73c968-9970-4910-81c8-76551ec71cd1" />

<img width="3360" height="2100" alt="Screenshot 2025-09-23 at 2 03 58 PM" src="https://github.com/user-attachments/assets/dd5ebf9c-299f-4588-adeb-9d758a67f945" />

---

## Delay in Buffers

The intersection of input slew and output load determines the delay of a given buffer.

---

## Relation to Circuit Design

The way we differentiate these delays is basically through circuit design, which depends on the W/L ratio of the transistors.

---

## Source of Delay Tables

These delay tables are generated from the SPICE simulation point of view.

---

<img width="3360" height="2100" alt="Screenshot 2025-09-24 at 11 18 51 AM" src="https://github.com/user-attachments/assets/3729be59-5a2a-4417-9144-89a08adcbcc3" />

<img width="3360" height="2100" alt="Screenshot 2025-09-24 at 11 19 14 AM" src="https://github.com/user-attachments/assets/c92ba6e9-cf18-43b8-92e0-50dcab104c87" />

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 22 08 AM" src="https://github.com/user-attachments/assets/c6c5c431-6098-46e9-8f0b-d5cd72fe7ac6" />

## Introduction to basic element in Circuit design – NMOS

## Basic CMOS Device: NMOS

### Structure

An NMOS transistor is built on a p-type substrate. It has an isolation region to differentiate it from the next transistor. Within the substrate, there are n+ diffusion regions that act as the source and drain. Above these regions lies the gate oxide, on which the gate terminal is formed using polysilicon or metal. In addition, the device also has a body terminal (B).

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 36 46 AM" src="https://github.com/user-attachments/assets/66c8a75a-d936-4511-a086-ec303a73d982" />

### Threshold Voltage

The threshold voltage of the NMOS transistor is very important for SPICE simulation, as it determines when the transistor turns on.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 43 14 AM" src="https://github.com/user-attachments/assets/a6e3becc-70a4-461f-8d3d-3116c620e517" />

### Terminal Conditions

When every terminal is grounded, no PN junction is conducting. In this situation, the resistance that exists between the source and drain is called the source–drain resistance.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 48 12 AM" src="https://github.com/user-attachments/assets/436586cf-0f11-406f-9e2b-ce8ca8248e51" />

### Gate Behavior

When the gate is positively charged, it forms a capacitance between the substrate and the gate. This positive charge repels the holes in the substrate, leading to the accumulation of negatively charged carriers around the gate junction.

---

## Strong inversion and threshold voltage



## Depletion and Inversion in NMOS

### Depletion Formation

When the gate voltage starts to increase, depletion of charge carriers begins. The area under the gate is gradually depleted of its majority carriers (holes in the p-type substrate).

---

### Strong Inversion and Threshold Voltage

As the gate voltage increases further, the depletion region grows until the surface region is inverted into n-type. This condition is called **strong inversion**, and the corresponding gate voltage is defined as the **threshold voltage (Vth)**.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 48 12 AM" src="https://github.com/user-attachments/assets/d1c68e8c-bfda-41dc-8fd3-e60c1b9f94cb" />

### Beyond Threshold

When the gate voltage exceeds the threshold:

* The depletion region no longer increases.
* Instead, negative charge carriers (electrons) accumulate near the surface, as there are no holes left to repel.
* A further increase in gate voltage attracts electrons from the n+ source and drain regions, thereby widening the channel.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 55 10 AM" src="https://github.com/user-attachments/assets/d685896b-1401-422a-ab73-43986ab7c221" />

### Channel Formation

At this point, a conductive channel is formed between the source and drain, allowing current to flow.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 55 17 AM" src="https://github.com/user-attachments/assets/6358d18f-389c-4bfb-a395-78e329f74811" />

### Cutoff Region

When the gate voltage is below threshold, there is no conductive channel, and the transistor is in the **cutoff region**.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 11 59 50 AM" src="https://github.com/user-attachments/assets/910e2bc0-cd97-4c96-8eb2-e73bf447a6a5" />

### Effect of Source-to-Body Voltage (Vsb)

Consider two cases:

* **Vsb = 0**: The depletion region is determined only by the gate voltage.
* **Vsb > 0**: The depletion region becomes larger due to the additional reverse bias across the source–body PN junction. As a result, inversion near the source occurs at a slightly higher gate voltage, causing a delay in channel formation.

## Threshold voltage with positive substrate potential

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 04 46 PM" src="https://github.com/user-attachments/assets/2d4f023b-4f52-4359-b6f9-615afdfa2e00" />


## Threshold Voltage with Body Effect

The threshold voltage of an NMOS transistor is not constant. It depends on the source-to-body voltage (**VSB**) due to the **body effect**. The general equation is:

$$
V_{th} = V_{th0} + \gamma \Big( \sqrt{2\phi_F + V_{SB}} - \sqrt{2\phi_F} \Big)
$$

Where:

* **$V_{th0}$** = Threshold voltage when $V_{SB} = 0$ (zero body bias).
* **$\gamma$** = Body effect coefficient, given by

  $$
  \gamma = \frac{\sqrt{2 q \varepsilon_{si} N_A}}{C_{ox}}
  $$
* **$\phi_F$** = Fermi potential of the substrate.
* **$V_{SB}$** = Source-to-body voltage.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 05 27 PM" src="https://github.com/user-attachments/assets/3710f0b3-3708-40c9-a737-a0d10034bae1" />


<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 07 00 PM" src="https://github.com/user-attachments/assets/bc6cba2e-60fc-460c-ab31-e83d30560718" />


<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 08 51 PM" src="https://github.com/user-attachments/assets/f8a0e82d-55d6-40ab-9a60-e54ca8e673d1" />

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 10 00 PM" src="https://github.com/user-attachments/assets/d5a87d89-01f0-47bc-9947-1ddb114d7a8b" />

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 10 14 PM" src="https://github.com/user-attachments/assets/cc07d7b8-3eba-4934-abed-1529a246cdbe" />

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 12 22 PM" src="https://github.com/user-attachments/assets/0a7adfbe-06fb-4ae9-b687-7359780fdf24" />


## Effect of Parameters

* If **$V_{SB} = 0$**, the threshold voltage equals its intrinsic value $V_{th0}$.
* If **$V_{SB} > 0$**, the depletion region widens, and the channel inversion is delayed. This increases the threshold voltage by the amount given in the equation.
* The constants $\gamma$, $\phi_F$, and $V_{th0}$ are **technology-dependent parameters** provided by the foundry.

---

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 17 56 PM" src="https://github.com/user-attachments/assets/d2d7fb21-5af9-4cae-abd2-eafc0d03e706" />



## Role in SPICE Simulation

The foundry supplies these constants as part of the **device model files** (e.g., BSIM models). When these parameters are fed into the SPICE simulator:

* SPICE calculates the threshold voltage under different biasing conditions.
* The simulator then uses this threshold voltage to generate the correct **I–V characteristics** of the NMOS device.
* This ensures that the simulated transistor matches the behavior of the real fabricated device.

---

## Resistive region of operation with small drain-source voltage
---

## Resistive (Linear) Region of Operation

### Channel Formation

In the resistive region of operation, the **channel width increases with gate-to-source voltage (VGS)**. The effective voltage required to turn the device on is given by **VGS – Vt**, where Vt is the threshold voltage.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 54 56 PM" src="https://github.com/user-attachments/assets/476fba2a-fd52-4f67-9ad9-bf380a02473c" />

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 12 54 59 PM" src="https://github.com/user-attachments/assets/8cf41218-6dec-4237-9a52-887b45225a7b" />

<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 1 00 51 PM" src="https://github.com/user-attachments/assets/7f5e746c-62c3-41f9-a83c-e4888124bc1f" />

### Voltage Gradient Along the Channel

When the source is grounded and a voltage is applied at the drain, a **voltage gradient** is established throughout the channel. This means that the potential is not uniform along the channel length.

---

### Effective Channel Length

Due to fabrication technology effects, the **effective channel length** is smaller than the actual physical channel length. This effect influences the accuracy of current flow modeling.

---

### Gate-to-Channel Voltage Difference

If we plot the channel length against the voltage distribution along the channel, we observe that at every point along the channel there is a **different effective gate-to-channel voltage**. This varying voltage difference determines the local conductivity of the channel.

---
<img width="1680" height="1050" alt="Screenshot 2025-09-24 at 1 08 02 PM" src="https://github.com/user-attachments/assets/539d5d18-555e-4ea8-aba7-08608fe7e17c" />

##  Drift current theory

