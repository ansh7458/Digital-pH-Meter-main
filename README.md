# ⚗️ Digital pH Meter — Analog Front-End Prototype

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Arduino-00979D?style=for-the-badge&logo=arduino" />
  <img src="https://img.shields.io/badge/WiFi-ESP8266-E7352C?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Display-OLED-white?style=for-the-badge" />
  <img src="https://img.shields.io/badge/PCB-KiCad-314CB0?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Institute-NSUT-blue?style=for-the-badge" />
</p>

> **Centre for Electronic Design and Technology**  
> Netaji Subhas University of Technology, New Delhi  
> *Date: October 2024*

---

## 📋 Table of Contents
- [Synopsis](#-synopsis)
- [Introduction](#-introduction)
- [Block Diagram](#-block-diagram)
- [Schematic Diagram](#-schematic-diagram)
- [Working Principle](#-working-principle)
- [Conclusion](#-conclusion)
- [Bill of Materials](#-bill-of-materials)

---

## 🎯 Synopsis

This project aims to design and prototype a **digital pH meter** with an OLED display and **wireless data transmission via WiFi** (ESP8266). The current work involves breadboard testing of the analog front-end circuitry powered by a 2.5 V reference and handling input signals in the **−600 mV to 600 mV** range. Circuit operation has been validated with a DC power supply.

## 📖 Introduction

A pH meter measures the acidity or alkalinity of a solution by converting the hydrogen-ion activity into an electrical potential. Glass pH probes generate a voltage in the range of approximately **−0.414 V to 0.414 V**, proportional to the solution pH. The probe output is high impedance and requires a buffer amplifier, followed by level shifting and scaling to match the microcontroller's ADC input range.

## 🔧 Block Diagram

<p align="center">
  <img src="Block Diagram/" alt="System Block Diagram" width="600"/>
</p>

## 📐 Schematic Diagram

The analog front-end uses a **TLC4502 dual op-amp** for buffering and amplification with a precise **2.5 V reference**.

## ⚙️ Working Principle

The analog front-end consists of two main sections:

1. **Bias Network**: Establishes a mid-supply reference at 2.5 V, shifting the pH probe signal into the ADC range
2. **Amplification Stage**: Differential amplifier scales the ±600 mV probe output into a 0–5 V span for the Arduino Nano's ADC

The conditioned voltage is read by the Arduino Nano. An **ESP8266** module handles wireless transmission, and an **OLED display** shows real-time readings.

## ✅ Conclusion

A prototype analog front-end was implemented and tested on breadboard using a 2.5 V reference and TLC4502 op-amps. Testing with an actual pH probe is pending. Future integration with ESP8266 and OLED will enable wireless, real-time pH monitoring.

## 📦 Bill of Materials

| S.No | Component | Value | Qty |
|------|-----------|-------|-----|
| 1 | Arduino Nano | — | 1 |
| 2 | TLC4502 Dual Op-Amp | — | 1 |
| 3 | Resistor | 1 kΩ | 1 |
| 4 | Resistor | 100 Ω | 1 |
| 5 | Potentiometer | 100 kΩ | 1 |
| 6 | Capacitor | 0.1µF, 10µF | 1 ea |
| 7 | OLED Display | — | 1 |
| 8 | BL8530 Boost Converter | — | 1 |

## 🛠️ Technologies Used

`Arduino` · `ESP8266` · `KiCad` · `TLC4502` · `OLED` · `Analog Design`

## 👥 Authors
- **Ansh Gupta** — NSUT, New Delhi
- **Aditya Garg** — NSUT, New Delhi

---
*Centre for Electronic Design and Technology, NSUT, New Delhi*
