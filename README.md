# SYNTHETIX_HACKATHONELECTRICAL
# Analog Signal Extraction System

## Overview

This project implements an **analog signal processing system designed to extract a target frequency component from a noisy input signal**. The objective is to isolate a **6 kHz sine wave** from a mixed-frequency input while suppressing unwanted frequency components.

The system uses a **multi-stage analog filtering architecture** followed by signal conditioning blocks to accurately recover the desired signal.

---

## Problem Statement

The input signal contains multiple frequency components and noise. The goal of this project is to:

* Isolate the **6 kHz signal component**
* Suppress unwanted frequencies such as **600 Hz and 18 kHz**
* Deliver a clean **0.4 Vpp sine wave output**
* Implement the circuit both in **simulation** and **hardware schematic design**

---

## System Architecture

The signal processing chain consists of the following stages:

1. **High Pass Filter (HPF)**
2. **Band Pass Filter (BPF) – Stage 1**
3. **Band Pass Filter (BPF) – Stage 2**
4. **Low Pass Filter (LPF) – Stage 1**
5. **Low Pass Filter (LPF) – Stage 2**
6. **RC Smoothing Network**
7. **Voltage Divider**

Each block improves signal quality and progressively removes unwanted frequency components.

---

## Circuit Blocks Description

**High Pass Filter (HPF)**

Removes low-frequency interference before the signal enters the band-selective stages.

**Dual Band Pass Filters**

Two cascaded band-pass filters increase selectivity around 6 kHz, significantly improving rejection of unwanted frequencies.

**Dual Low Pass Filters**

Two LPF stages suppress higher frequency components and noise after the band selection stage.

**RC Smoothing Network**

Reduces residual ripple and stabilizes the waveform before amplitude scaling.

**Voltage Divider**

The voltage divider adjusts the amplitude of the signal to achieve the required **0.4 Vpp output level**.

---

**Noise Suppression Performance**

FFT analysis confirms effective suppression of unwanted components.

Frequency Component	Result
600 Hz	Suppressed to −55 dB
18 kHz	Strongly attenuated
Other noise components	Significantly reduced

This ensures that the 6 kHz component dominates the output spectrum.

## Simulation Results

The system successfully achieved the following:

* Target signal frequency extracted: **6 kHz**
* Output amplitude: **0.4 Vpp**
* Low-frequency suppression: **600 Hz attenuated to approximately -55 dB**
* High-frequency noise significantly reduced

These results confirm effective filtering and signal recovery.

---

## Tools Used

* **LTSpice** – Circuit simulation
* **KiCad** – Schematic design
* Analog filter design techniques
* Operational amplifier based signal conditioning

---

## Bonus Implementation

The complete circuit schematic was also implemented in **KiCad** to demonstrate hardware feasibility and circuit organization.

---

## Applications

This type of analog signal extraction system can be used in:

* Communication receivers
* Biomedical signal processing
* Audio signal filtering
* Sensor signal conditioning
* Embedded analog front-end circuits

---

## Conclusion

The project successfully demonstrates an **analog filtering approach for extracting a specific frequency component from a noisy signal**. Through multi-stage filtering and signal conditioning, the system accurately isolates a **6 kHz sine wave with a 0.4 Vpp output**, meeting the design objectives.

The design was verified through simulation and documented using professional schematic tools.
