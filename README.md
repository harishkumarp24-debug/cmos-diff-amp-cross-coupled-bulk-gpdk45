# Differential Amplifier with Active Load using Cross-Coupled Bulk (GPDK45)

Fully differential CMOS amplifier with a cross-coupled-bulk active load, designed in **Cadence Virtuoso** using the **GPDK45** (45 nm) generic PDK. Based on the paper *"A Fully Differential Amplifier with Active Load using Cross-Coupled Bulk to Enhance the Gain and CMRR"* (K. Nisar, A. Ballo, A. D. Grasso, Univ. of Catania).

**Author:** P. Harish Kumar, UG-3 ECE, Roll No. S20240020317

## Targets vs. Results

| Parameter | Target | Achieved |
|---|---|---|
| Differential gain | > 40 dB | 40.03 dB |
| Bandwidth | > 280 kHz | 290 kHz |
| CMRR | > 40 dB | 46.24 dB |
| Common-mode gain | - | -6.21 dB |
| Power | Minimum | 7.64 uW |
| Supply (VDD) | - | 1 V |

CMRR (dB) = Ad(dB) - Acm(dB) = 40.03 - (-6.21) = 46.24 dB

## Design Parameters

L = 45 nm for all devices except M9 (135 nm). ITRIM = 54 nA, IBIAS = 95 nA.

| Transistor | W | Role |
|---|---|---|
| M1, M2 | 145 nm | Input pair: transconductance and differential gain |
| M3, M4 | 300 nm | Cross-coupled bulk load: CMRR improvement |
| M5 | 4.6 um | Biasing and common-mode operating point |
| M6 | 180 nm | Current mirror |
| M7 | 200 nm | Current mirror |
| M8 | 300 nm | Tail: output resistance, lower CM gain |
| M9 | 180 nm (L = 135 nm) | Bias mirror |
| M10 | 150 nm | Bias branch |

## Analyses Performed
Transient, AC, DC, power, differential gain, common-mode gain, DC sweep (vcm), noise, CMRR, Monte Carlo (200 samples) and PVT corners.

## Physical Design
- DRC: no errors
- LVS: schematic and layout match
- RC extraction performed
- GDSII exported

## Files
- `CADENCE_PROJECT_REPORT_8.pdf`: full project report
- `netlist.scs`: Spectre netlist
- `DIFF_AMP_5.gds`: GDSII layout

## Tools
Cadence Virtuoso, Spectre, GPDK45 PDK.

## Reference
1. Cadence GPDK45 Generic PDK Documentation, Cadence Design Systems.
2. K. Nisar, A. Ballo, A. D. Grasso, "A Fully Differential Amplifier with active load using cross-coupled bulk to enhance the gain and CMRR," DIEEI, University of Catania.
