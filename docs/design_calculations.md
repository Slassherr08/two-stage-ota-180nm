# Hand Calculations — Two-Stage OTA Sizing

## 1. Compensation Capacitor Sizing

Given phase margin target, derive C_c (Miller cap) relative to C_L.

## 2. Stage 1 (Differential Pair) Sizing

- Tail current (I_SS):
- g_m1 required for target GBW:
- W/L for M1, M2 (input pair):
- W/L for M3, M4 (current mirror load):

## 3. Stage 2 (Common-Source) Sizing

- Bias current I_D2:
- g_m2 (for non-dominant pole placement, typically g_m2 ≥ 2.2·GBW·C_L/C_c or similar):
- W/L for M6 (gain device), M7 (current source load):

## 4. Nulling Resistor (if used)

- R_z target to cancel RHP zero: R_z ≈ 1/g_m6 (or per chosen strategy)

## 5. Bias Circuit Sizing

- Reference current:
- Mirror ratios:

## 6. Power Budget Check

P = V_DD × (I_stage1 + I_stage2 + I_bias)

## 7. Summary Table (Hand Calc vs. Simulated)

| Device | W (µm) | L (µm) | I_D (µA) | g_m (µA/V) | V_ov (V) |
|---|---|---|---|---|---|
| M1/M2 | | | | | |
| M3/M4 | | | | | |
| M5 (tail) | | | | | |
| M6 | | | | | |
| M7 | | | | | |

## Notes / Iterations

Log design iterations here — what changed and why (e.g., "increased tail current from X to Y to meet slew rate target").
