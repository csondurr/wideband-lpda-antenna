# Radiova ET-LPDA Wideband Antenna

A **2.4-5.8 GHz air-dielectric twin-boom Log-Periodic Dipole Array (LPDA)** designed in CST Studio Suite for directional RF transmission and experimental antenna engineering work.

> **Validation status:** electromagnetic simulation completed. Physical fabrication, VNA validation and anechoic-chamber measurements have not yet been completed.

## Highlights

- Frequency range: **2.4-5.8 GHz**
- Architecture: **air-dielectric twin-boom LPDA**
- Elements: **20 log-periodic dipoles / 40 half-elements**
- Nominal impedance: **50 ohm**
- Active RF boom length: approximately **150 mm**
- Boom spacing: approximately **10.9 mm**
- Main-beam direction: **+x boresight** in the CST model
- Solver: **CST HF Frequency Domain**, tetrahedral adaptive mesh

## Simulated Performance

| Frequency | S11 | VSWR | Directivity | Realized Gain | Total Efficiency |
|---|---:|---:|---:|---:|---:|
| 2.4 GHz | approximately -22 dB | approximately 1.16 | 8.695 dBi | 8.661 dBi | approximately -0.0345 dB |
| 5.8 GHz | approximately -15.5 to -16 dB | approximately 1.35-1.40 | 9.542 dBi | 9.398 dBi | approximately -0.1433 dB |

Across the intended 2.4-5.8 GHz band, the simulated VSWR remains approximately **1.10-1.45** and the S11 response is generally around or below **-15 dB**. These figures are simulation results and must not be interpreted as measured hardware performance.

## Design Summary

The antenna uses a metallic, substrate-free construction to reduce dielectric loss and improve power-handling potential compared with a thin printed implementation. The CST model includes finite-conductivity metal, a 50-ohm discrete port and a simplified coaxial/choke physical-shadow representation.

Key manufacturing and integration items still requiring prototype validation include:

- element-length, rod-diameter and boom-spacing tolerances;
- RF connector and coaxial-feed implementation;
- common-mode suppression using a ferrite choke;
- cable and connector insertion loss;
- reflected-power monitoring and PA VSWR protection;
- VNA and radiation-pattern measurements.

## Repository Structure

```text
wideband-lpda-antenna/
├── README.md
├── .gitignore
├── cst/
│   └── Radiova_ET_LPDA_2p4-5p8GHz.cst
└── docs/
    ├── TECHNICAL_SUMMARY.md
    └── Radiova_ET_LPDA_Technical_Report_TR.pdf
```

## Project Files

- CST simulation model: `cst/Radiova_ET_LPDA_2p4-5p8GHz.cst`
- Turkish technical report: `docs/Radiova_ET_LPDA_Technical_Report_TR.pdf`
- Repository-readable engineering summary: [`docs/TECHNICAL_SUMMARY.md`](docs/TECHNICAL_SUMMARY.md)

## Simulation Configuration

| Parameter | Configuration |
|---|---|
| Software | CST Studio Suite |
| Solver | HF Frequency Domain |
| Mesh | Tetrahedral / adaptive |
| Reference impedance | 50 ohm |
| Simulated range | 2.0-6.5 GHz |
| Far-field monitors | 2.4, 2.45, 5.2, 5.8 and 6.0 GHz |
| Material model | Finite-conductivity aluminum / lossy metal |
| Feed model | 50-ohm discrete port with coax/choke physical-shadow model |

## Author

**Cem Sondur**  
Electrical and Electronics Engineering  
RF, microwave and antenna design



## Repository maintenance

**Evidence boundary:** CST simulation only; fabrication and calibrated antenna measurements remain outstanding.

- [Validation status](docs/VALIDATION.md)
- [Contribution guide](CONTRIBUTING.md)
- [Safety and security](SECURITY.md)
- [Citation metadata](CITATION.cff)

## License

Copyright (c) 2026 Cem Sondur. Distributed under the [MIT License](LICENSE). Component models and other third-party material remain subject to their original licenses.
