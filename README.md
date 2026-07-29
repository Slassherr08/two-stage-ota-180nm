# Two-Stage OTA Design — 180nm CMOS

Design, simulation, and verification of a two-stage operational transconductance
amplifier (OTA) in 180nm CMOS technology, using **Keysight ADS**.

## Overview

- **Technology node:** 180nm CMOS
- **Tool:** Keysight ADS
- **Topology:** Two-stage OTA (first stage: differential pair, second stage: common-source gain stage), Miller compensation 


## Target Specifications

| Parameter | Target | Simulated | Notes |
|---|---|---|---|
| Supply Voltage (V)|1.8|||
| DC Gain (dB) |70| | |
| GBW (MHz) |10| | |
| Phase Margin (°) |60| | |
| Slew Rate (V/µs) |10 | | |
| Power Consumption (mW) |≤1mW| | |
| Input Common Mode Range (V) |1| | |
| Output Swing (V) |1.4| | |
| CMRR (dB) |≥60| | |
| PSRR (dB) |≥50| | |


See [`docs/specifications.md`](docs/specifications.md) for full derivations and [`results/summary_table.csv`](results/summary_table.csv) for the machine-readable version.

## Repository Structure

```
two-stage-ota-180nm/
├── docs/                  Design notes, specs, hand calculations
├── ads_workspace/         ADS workspace (design intent files only, see .gitignore)
├── schematics/exported/   PDF/PNG exports of schematics for quick viewing
├── simulations/           Organized by analysis type (dc, ac, transient, noise, corners_mc)
├── results/               Final plots and summary tables
├── layout/                Layout files (if/when applicable)
└── scripts/               AEL/Python automation and post-processing scripts
```

## Getting Started

1. Set up the 180nm PDK locally — **not included in this repo** (foundry-licensed). See [`docs/pdk_setup.md`](docs/pdk_setup.md).
2. Open `ads_workspace/` in Keysight ADS.
3. Schematics and testbenches are organized under the corresponding `simulations/` subfolder.
4. Exported results land in `results/plots/` and `results/summary_table.csv`.

> **Note:** PDK/technology library files are excluded from version control via `.gitignore` — see [`docs/pdk_setup.md`](docs/pdk_setup.md) for what's excluded and how to relink your PDK after cloning.

## Design Progress

- [ ] Hand calculations / sizing
- [ ] Schematic entry
- [ ] DC operating point verification
- [ ] AC analysis (gain, phase margin, GBW)
- [ ] Transient analysis (slew rate, settling time)
- [ ] Noise analysis
- [ ] PVT corners
- [ ] Monte Carlo
- [ ] Layout
- [ ] Post-layout simulation

## References

- List textbooks, papers, or app notes used (e.g., Razavi, *Design of Analog CMOS Integrated Circuits*)

## License

See [LICENSE](LICENSE).
