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

From the average powers, the following inferences can be made:

•	28T full adder consumes the most power among the three designs.

•	28 T F.A. takes up the most power, taking close to 13.25 μW as it has a greater number of transistors compared to design 1 & 2 so the RC delay is much higher.

•	Between Design 1 & 2, Design 2 takes up more power as it uses both NMOS and PMOS transistors and since PMOS is more resistive than NMOS it slows down the charging thus leading to more power and delay while Design 1 uses PTL logic for calculating sum which uses only NMOS so RC delay is lesser

•	But Design 2 and 28 T produces a much cleaner output than Design 1 since it uses TG and static CMOS methods respectively.

From the delays calculated, the following inferences can be
made:

•	The average delays in sum of design 1 and 2 are significantly lesser than the 28T full adder, proving its high-speed characteristics.

•	Thus, depending on the requirement of the project, an appropriate choice can be made between these full adder designs.

