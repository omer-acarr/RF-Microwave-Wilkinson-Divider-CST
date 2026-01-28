# Wilkinson Power Divider Design & Simulation (X-Band)

This project covers the design, electromagnetic (EM) modeling, and simulation of a **Wilkinson Power Divider** using **CST Studio Suite 2025**. The design is optimized for X-band applications, specifically targeting a resonance frequency around **10.2 GHz**.

## 🚀 Project Overview
The Wilkinson Power Divider is a fundamental RF component used to split an input signal into two equal-phase output signals with high isolation between the output ports. This project demonstrates the end-to-end workflow from 3D modeling to S-parameter analysis.

## 🛠 Technical Specifications
- **Center Frequency:** 10.2 GHz
- **Return Loss ($S_{1,1}$):** ~ -15 dB (at 10.2 GHz)
- **Substrate Thickness ($h_{sub}$):** 1.524 mm
- **Copper Thickness ($h_{copper}$):** 35 µm
- **Simulation Type:** Transient Solver

## 📊 Design & Simulation Process

### 1. 3D Modeling
The model consists of a microstrip structure with quarter-wave ($\lambda/4$) transformers. 
- **Substrate:** Dielectric material with defined permittivity.
- **Conductive Layers:** Copper traces and a solid ground plane.
- **Ports:** Three waveguide ports defined for signal entry and exit.



### 2. Simulation Setup & Troubleshooting
During the development phase, several critical technical issues were addressed:
- **Boundary Conditions:** Resolved the *"Farfield monitors not supported with PEC background"* error by switching the Background Material to **"Normal"** (Air) to allow proper wave propagation.
- **Visibility:** Enabled **Bounding Box** ($Ctrl+B$) to visualize the calculation domain boundaries.
- **Solver Optimization:** Configured the **Transient Solver** settings to achieve a steady-state energy criterion of -40 dB.

### 3. Results Analysis
The S-parameter results indicate a successful impedance match at the target frequency.
- **Resonance:** The deepest null in the $S_{1,1}$ curve is located at 10.2 GHz, confirming the accuracy of the geometric dimensions.
- **Bandwidth:** The design maintains an $S_{1,1} < -10$ dB bandwidth from approximately 9.8 GHz to 10.5 GHz.

## 📝 Conclusion
This project demonstrates proficiency in:
- RF/Microwave simulation using **CST Studio Suite**.
- Troubleshooting EM simulation boundary and license errors.
- Analyzing S-parameters for impedance matching and resonance.

