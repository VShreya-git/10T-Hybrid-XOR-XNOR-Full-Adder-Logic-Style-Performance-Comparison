# 10T-Hybrid-XOR-XNOR-Full-Adder-Logic-Style-Performance-Comparison

### I) Project Overview

This work investigates transistor-level optimization of full adder architectures using 10-transistor (10T) hybrid XOR–XNOR logic in 180nm CMOS technology.

Two reduced-transistor implementations were developed and benchmarked against a conventional 28T static CMOS full adder. The designs explore the performance implications of Pass Transistor Logic (PTL) and Transmission Gate (TG) logic under identical stimulus conditions in Cadence Virtuoso.

The focus is on delay, power, and logic integrity trade-offs at the device level.

### II) Design Philosophy

Rather than optimizing at the gate level, this project targets logic-style selection as a performance variable.

#### 1. Static CMOS (28T Baseline)

Complementary pull-up/pull-down networks

•	Full voltage swing

•	High noise margin

•	Increased parasitic capacitance

•	Larger area and higher intrinsic RC delay

![Schematic-representation-of-Standard-FA](https://github.com/user-attachments/assets/31fc8919-0736-4b09-a373-b73c5ed17e87)

#### 2. PTL-Based 10T Hybrid (Design 1)

This design leverages Pass Transistor Logic to minimize transistor count and internal node capacitance.

•	Reduced diffusion capacitance

•	Fewer switching nodes

•	Lower effective RC delay

•	Threshold voltage degradation risk

•	Potential reduced noise margin

PTL prioritizes speed and area efficiency at the expense of output robustness.

<img width="471" height="438" alt="Screenshot 2026-02-17 220121" src="https://github.com/user-attachments/assets/6a95141b-8e45-4717-9c56-9d950d7ed04f" />

#### 3. TG-Based 10T Hybrid (Design 2)

This implementation incorporates Transmission Gates to mitigate PTL voltage loss while retaining reduced complexity.

•	Parallel NMOS–PMOS conduction

•	Full voltage swing restoration

•	Improved signal integrity

•	Slightly increased transistor activity vs PTL

TG logic offers a compromise between performance and reliability.

<img width="424" height="389" alt="Screenshot 2026-02-17 220132" src="https://github.com/user-attachments/assets/d22f5a09-499d-4f25-a7aa-377fddc51a98" />

### III) Performance Insights

Simulation results under identical input stimulus reveal:

•	The PTL-based hybrid exhibits the lowest propagation delay due to minimized capacitive loading.

•	The TG-based hybrid demonstrates improved output waveform quality and logic stability.

•	The 28T CMOS design shows higher delay but stronger signal robustness.

The results highlight the intrinsic trade-off:

Reduced transistor count improves speed but introduces signal integrity constraints that must be mitigated through logic-style selection.
