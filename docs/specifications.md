# Design Specifications — Two-Stage OTA (180nm)

## 1. Target Specifications

| Parameter | Symbol | Target Value |
|---|---|---|
| DC Gain | A_v |70dB| 
| Gain-Bandwidth Product | GBW |1MHz|
| Phase Margin | PM |60°|
| Slew Rate | SR |10V/µs|
| Power Consumption | P | ≤1mW |
| Supply Voltage | V_DD |1.8V|
| Load Capacitance | C_L | 5pF |
| Input Common Mode Range | ICMR |1 V|
| Output Swing | | 1.4 V |
| CMRR | |≥60|
| PSRR | |≥50|
## 2. Topology Choice

Describe the chosen topology and justification:
- First stage: Differential amplifier with active load
- Second stage: Common source gain stage
- Compensation scheme: Miller
- Biasing scheme: Current Mirror

## 3. Technology Parameters (180nm)

| Parameter | NMOS | PMOS |
|---|---|---|
| V_TH | | |
| µ_n C_ox / µ_p C_ox | | |
| L_min | | |
| Typical V_DD | | |

