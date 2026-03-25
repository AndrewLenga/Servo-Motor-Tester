# Servo-Motor-Tester
This repository contains the full design suite—including Schematic, PCB Layout, and 3D CAD models—for a high-stability Servo Motor Tester. Engineered using a modified astable multivibrator topology, this device provides a robust hardware solution for validating RC servo response without the need for a microcontroller.
1. Executive Summary
Standard RC servos operate on a specific Pulse Width Modulation (PWM) protocol, requiring a carrier frequency (period) with a high-state duration.
This design leverages the NE555P precision timer to synthesize this waveform by decoupling the charge and discharge timing constants, ensuring high-fidelity signal reproduction for professional benchtop testing.
3. Circuit Architecture & Signal Integrity
A. Non-Symmetric Astable Topology
In a textbook 555 astable configuration, the duty cycle is constrained to achieve the duty cycle required for servo control, this design incorporates a signal diode in parallel with the discharge path.
Charging Phase: The timing capacitor charges through the series combination of the potentiometer 

Discharging Phase: 
It provides a low-impedance return path to Pin 7 (Discharge), effectively bypassing the primary timing resistors.

Implementation Specifications
Parameter	Specification
Logic Family	Bipolar NE555 / CMOS Equivalent
Input Voltage ( DC (Regulated)
Operating Frequency	
(Targeted for standard RC protocols)
Output Pulse Range  (Min) to  (Max)
Connector Interface	3-Pin Header (Signal-VCC-GND)
4. Documentation & Manufacturing
This project includes a comprehensive set of production files:
Schematic: Hierarchical design focusing on signal flow and net-clearance.
<img width="1262" height="630" alt="image" src="https://github.com/user-attachments/assets/45a69f18-50de-445c-939b-8db06798146e" />

PCB Layout: Optimized for a compact footprint with enhanced ground planes for EMI reduction.
<img width="920" height="806" alt="image" src="https://github.com/user-attachments/assets/c45bb511-af2e-4564-beb9-45675cac1d11" />

3D Model: STEP/STL files for mechanical integration and enclosure design.
<img width="1100" height="728" alt="image" src="https://github.com/user-attachments/assets/f2210f22-a318-4044-8e22-e6decc3d71cd" />

