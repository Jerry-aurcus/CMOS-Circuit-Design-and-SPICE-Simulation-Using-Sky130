# CMOS-Circuit-Design-and-SPICE-Simulation-Using-Sky130 

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

