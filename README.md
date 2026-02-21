# PMOS-Based Low Dropout (LDO) Voltage Regulator

## Overview

This repository presents the transistor-level design and simulation of a PMOS-based Low Dropout (LDO) voltage regulator implemented in 90nm CMOS technology.

The regulator is designed to provide a stable 1.2V output from a 1.4V–1.8V supply while supporting load currents up to 100mA. The architecture emphasizes low dropout voltage, high PSRR, low output noise, and robust loop stability.

The project is intended for analog IC design learning, research, and professional portfolio development.

---

## Design Specifications

| Parameter | Value |
|------------|--------|
| Technology | 90nm CMOS |
| Input Voltage | 1.4V – 1.8V |
| Output Voltage | 1.2V |
| Maximum Load Current | 100mA |
| Dropout Voltage | ≤ 200mV @ 100mA |
| Line Regulation | ≤ 1mV/V |
| Load Regulation | ≤ 1mV |
| Phase Margin | ≥ 60° |
| PSRR @ 1kHz | ≥ 60dB |
| PSRR @ 1MHz | ≥ 40dB |
| Quiescent Current | < 100µA |

---

## Architecture

The LDO consists of the following main blocks:

- PMOS Pass Transistor
- High-Gain Error Amplifier
- Bandgap Reference (1.2V)
- Feedback Resistor Network
- Frequency Compensation Network

The PMOS pass device enables low dropout operation, while internal compensation ensures loop stability across the full load range.

---

## Simulation Environment

- Cadence Virtuoso
- Spectre Simulator
- 90nm CMOS PDK

---

## Analyses Performed

- DC Operating Point
- Line Regulation
- Load Regulation
- Transient Response
- Loop Gain and Phase Margin
- PSRR Analysis
- Output Noise Analysis

---

## Results Summary

The LDO achieves stable regulation across load and line variations while maintaining high PSRR and low dropout voltage. Loop stability is ensured with a phase margin greater than 60° under worst-case conditions.

---

## Future Work

- Monte Carlo Analysis
- Corner Simulations (TT, FF, SS)
- Layout Design and Parasitic Extraction
- Power Efficiency Optimization
- Adaptive Biasing for Reduced Quiescent Current

---

## Author

[Your Name]  
Analog / Mixed-Signal IC Design
