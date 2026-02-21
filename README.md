# PMOS-Based Low Dropout (LDO) Voltage Regulator – 90nm CMOS

## Overview

This repository presents the transistor-level design and simulation of a PMOS-based Low Dropout (LDO) voltage regulator implemented in 90nm CMOS technology.

The objective is to design a stable, low-noise, high-PSRR regulator capable of delivering up to 100mA load current with low dropout voltage and robust loop stability.

The architecture includes a high-gain error amplifier, PMOS pass device, bandgap reference, feedback network, and frequency compensation.

---

## Design Specifications

| Parameter | Target Value |
|------------|--------------|
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

The LDO consists of:

- PMOS Pass Transistor
- Two-Stage Error Amplifier (OTA-based)
- 1.2V Bandgap Reference
- Resistive Feedback Network
- Miller Compensation Network

The PMOS pass element enables low dropout operation without requiring a charge pump.

---

## PMOS vs NMOS LDO Comparison

| Feature | PMOS LDO | NMOS LDO |
|----------|-----------|-----------|
| Pass Device | PMOS | NMOS |
| Dropout Voltage | Low (VSD(sat)) | Very Low (RDS(on)-based) |
| Gate Drive Requirement | No charge pump required | Often requires charge pump for full enhancement |
| Loop Gain | Generally higher | Moderate |
| Output Resistance | Higher | Lower at high load |
| Area | Larger (lower mobility) | Smaller |
| Speed | Slower (hole mobility) | Faster (electron mobility) |
| Design Complexity | Moderate | Higher (gate boosting required) |

### Reason for Selecting PMOS

Although NMOS devices offer lower on-resistance and faster response due to higher electron mobility, they require a gate voltage higher than the input supply to fully turn on in low-dropout conditions. This typically necessitates a charge pump, increasing design complexity and power consumption.

A PMOS-based topology avoids the need for a charge pump, simplifies implementation, and provides sufficient loop gain for stable operation, making it well-suited for moderate-load, low-power analog applications.

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
- Transient Load Step Response
- Loop Gain & Phase Margin
- PSRR Analysis
- Output Noise Analysis

---

## Results Summary

The regulator maintains a stable 1.2V output across line and load variations with phase margin exceeding 60° under worst-case conditions. The PMOS pass device enables low-dropout performance without additional gate boosting circuitry.

---

## Future Enhancements

- Adaptive Biasing for Reduced Quiescent Current
- Full PVT Corner Analysis
- Monte Carlo Simulations
- Layout and Parasitic Extraction
- Noise Optimization for RF Applications

---

## Author

Meesala Joshita  
Analog / Mixed-Signal IC Design
