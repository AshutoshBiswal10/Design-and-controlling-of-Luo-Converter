# Comparative Analysis of Control Strategies for Enhancing the Performance of a DC-DC Luo Converter

This repository presents the mathematical modeling, small-signal analysis, controller design, and simulation of a **Positive Output Luo Converter (POLC)** under closed-loop voltage regulation using MATLAB/Simulink.

The project investigates the performance of three different control strategies:

- Proportional-Integral-Derivative (PID)
- Two-Degree-of-Freedom PID (2-DOF PID)
- Three-Degree-of-Freedom PID (3-DOF PID)

The controllers are evaluated based on transient response, overshoot, gain margin, phase margin, and overall voltage regulation performance.

---

## Project Overview

Positive Output Luo Converters (POLCs) are widely employed in renewable energy systems, electric vehicles, and high-gain DC-DC conversion applications due to their high voltage conversion ratio, low output ripple, and positive output polarity.

However, the nonlinear switching dynamics of the converter make accurate voltage regulation challenging under varying input and load conditions.

This project addresses these challenges by:

- Developing a mathematical model of the converter using **state-space averaging**
- Deriving the small-signal control-to-output transfer function
- Designing and comparing PID, 2-DOF PID, and 3-DOF PID controllers
- Evaluating controller performance through time-domain and frequency-domain analyses using MATLAB Sisotool

---

## Methodology

The complete workflow followed in this project is:

1. Develop the Positive Output Luo Converter operating in Continuous Conduction Mode (CCM).
2. Derive the averaged state-space equations.
3. Linearize the nonlinear converter using the state-space averaging technique.
4. Obtain the control-to-output transfer function.
5. Design classical PID, 2-DOF PID, and 3-DOF PID controllers.
6. Tune controller parameters using MATLAB Sisotool.
7. Analyze controller performance using:
   - Step Response
   - Root Locus
   - Bode Plot
8. Compare transient and steady-state characteristics under identical operating conditions.

---

## Technical Specifications

| Parameter | Value |
|-----------|--------|
| Input Voltage | 150 V |
| Output Voltage | 225 V |
| Inductor (L₁, L₂) | 36.04 mH |
| Lift Capacitor (C₁) | 21.40 μF |
| Output Capacitor (C₂) | 30.40 μF |
| Load Resistance | 135.2 Ω |
| Rated Output Power | 440 W |
| Switching Period | 20 μs |

---

## Controllers Implemented

### PID Controller
Conventional feedback controller designed to regulate converter output voltage using proportional, integral, and derivative actions.

### 2-DOF PID Controller
Introduces proportional and derivative set-point weighting to improve reference tracking while reducing overshoot.

### 3-DOF PID Controller
Extends the 2-DOF structure by introducing an additional integral set-point weighting parameter, enabling independent tuning of tracking performance and disturbance rejection.

---

## Performance Comparison

| Controller | Rise Time (s) | Overshoot (%) | Gain Margin (dB) | Phase Margin (°) |
|------------|--------------:|--------------:|-----------------:|-----------------:|
| PID | 0.0186 | 60.2 | 0.0288 | 7.03 |
| 2-DOF PID | 0.0210 | 14.2 | 0.0068 | 70.2 |
| 3-DOF PID | **0.0029** | **30.0** | **0.0231** | **48.9** |

The comparative analysis demonstrates that the **3-DOF PID controller** provides the fastest transient response while maintaining satisfactory stability and improved voltage regulation compared to conventional PID control.

---

## Simulation Results

The repository includes simulation results for:

- Converter output voltage
- Output current
- Input voltage
- Input current
- Inductor current
- Step responses
- Bode plots
- Root locus plots
- Controller performance comparison

---

## Repository Structure

```text
.
├── Hardware/                              # Hardware implementation files and related resources
├── MATLAB Simulation/                     # MATLAB/Simulink models, controller design, and simulations
├── PCB Designing using KiCad/             # PCB schematics and board layout files
├── References/                            # Research papers, datasheets, and supporting literature
├── Results/                               # Simulation plots, controller comparisons, and output waveforms
├── Hardware_Luo_Converter_with_IGBT.slx   # Complete Simulink model of the Luo Converter with closed-loop control
└── README.md
```

### Repository Contents

- **Hardware/** – Hardware implementation resources, component details, and supporting files for the Luo Converter prototype.

- **MATLAB Simulation/** – MATLAB scripts and Simulink models used for small-signal modeling, controller design, transfer function analysis, and simulation.

- **PCB Designing using KiCad/** – KiCad project files including schematic diagrams, PCB layouts, and fabrication-ready design files.

- **References/** – Research papers, datasheets, and reference materials used during the design and analysis of the converter.

- **Results/** – Simulation outputs including step responses, Bode plots, root locus diagrams, output voltage/current waveforms, and controller performance comparisons.

- **Hardware_Luo_Converter_with_IGBT.slx** – Complete MATLAB/Simulink model integrating the Positive Output Luo Converter, IGBT-based switching circuit, and the implemented PID, 2-DOF PID, and 3-DOF PID control strategies.

- **README.md** – Project overview, methodology, simulation details, repository structure, and usage instructions.

---

## Software & Tools

- MATLAB
- Simulink
- MATLAB Sisotool
- Control System Toolbox

---

## Key Features

- State-space averaged modeling of a Positive Output Luo Converter
- Small-signal linearization
- Transfer function derivation
- PID, 2-DOF PID, and 3-DOF PID controller design
- Frequency-domain stability analysis
- Comparative controller evaluation
- MATLAB/Simulink implementation

---

## Future Work

- Fractional-Order PID (FOPID) controller implementation
- Adaptive and intelligent control techniques
- Hardware implementation using DSP or FPGA
- Real-time validation under varying operating conditions
- Efficiency optimization for renewable energy applications

---

## Citation

If you use this work in your research, please cite:

> **Comparative Analysis of Control Strategies for Enhancing the Performance of DC-DC Luo Converters**, IEEE India Council International Subsections Conference (INDISCON), 2025.

---

## Author

**Ashutosh Biswal**

B.Tech, Electrical Engineering

National Institute of Technology Rourkela

MATLAB | Simulink | Control Systems | Power Electronics
