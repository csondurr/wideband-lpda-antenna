# Radiova ET-LPDA Technical Summary

## 1. Scope

Radiova ET-LPDA is a directional, air-dielectric, metallic twin-boom Log-Periodic Dipole Array covering the 2.4-5.8 GHz design band. The model was developed as a compact wideband antenna intended for experimental directional RF transmission and system-integration studies.

All numerical results in this document were obtained from electromagnetic simulation. The design has not yet been validated by physical measurements.

## 2. Antenna Architecture

| Parameter | Value / approach |
|---|---|
| Antenna type | Twin-boom Log-Periodic Dipole Array |
| Design band | 2.4-5.8 GHz |
| Number of elements | 20 dipoles / 40 half-elements |
| Dielectric | Air; no PCB substrate |
| Element material | Aluminum / metallic rods with stepped diameters |
| Maximum element span | Approximately 90-100 mm |
| Active RF boom length | Approximately 150 mm |
| Estimated field-installation package | Approximately 250-320 mm including mounting and feed hardware |
| Boom spacing | Approximately 10.9 mm |
| Nominal impedance | 50 ohm |
| Feed in simulation | 50-ohm discrete port |

The substrate-free metallic construction was selected to reduce dielectric loss and provide a mechanically realistic basis for later power-handling studies. The simulation also contains a simplified physical representation of the coaxial-feed and choke region so that first-order pattern disturbances can be observed.

## 3. Simulation Method

| Parameter | Configuration |
|---|---|
| Electromagnetic software | CST Studio Suite |
| Solver | HF Frequency Domain |
| Mesh | Tetrahedral adaptive mesh |
| S-parameter sweep | 2.0-6.5 GHz |
| Far-field monitors | 2.4, 2.45, 5.2, 5.8 and 6.0 GHz |
| Material representation | Finite-conductivity aluminum / lossy metal |
| Reference impedance | 50 ohm |

## 4. Impedance Matching

The simulated S11 response remains generally around or below -15 dB throughout the intended operating band. Two pronounced matching regions occur near 3.1 GHz and 4.05 GHz, consistent with the frequency-dependent movement of the active region along an LPDA structure.

Approximate operating-point values:

| Frequency | Simulated S11 | Simulated VSWR |
|---|---:|---:|
| 2.4 GHz | Approximately -22 dB | Approximately 1.16 |
| 5.8 GHz | Approximately -15.5 to -16 dB | Approximately 1.35-1.40 |

The approximate VSWR range across 2.4-5.8 GHz is 1.10-1.45, remaining below the commonly used 2:1 engineering threshold in the model.

## 5. Efficiency

The simulated radiation-efficiency values at the sampled far-field frequencies remain close to 0 dB. This is consistent with the low-loss, air-dielectric metallic architecture.

| Frequency | Simulated total efficiency |
|---|---:|
| 2.4 GHz | Approximately -0.0345 dB |
| 5.8 GHz | Approximately -0.1433 dB |

In a fabricated system, feed cable, connector, choke and assembly losses are expected to be more significant than the modeled conductor loss of the antenna body.

## 6. Far-Field Performance

The simulated main beam remains directed along the model's +x boresight direction at both critical band edges.

| Frequency | Directivity | Realized gain |
|---|---:|---:|
| 2.4 GHz | 8.695 dBi | 8.661 dBi |
| 5.8 GHz | 9.542 dBi | 9.398 dBi |

The higher-frequency pattern exhibits more visible side-lobe structure than the 2.4 GHz pattern, while retaining the intended forward main beam.

## 7. Prototype Validation Plan

Before presenting this antenna as experimentally verified, the following work should be completed:

1. Manufacture the twin-boom and dipole elements with controlled tolerances.
2. Finalize the coaxial transition, RF connector and ferrite-choke arrangement.
3. Measure S11 and VSWR using a calibrated vector network analyzer.
4. Compare measured and simulated impedance behavior.
5. Measure radiation patterns, gain and front-to-back ratio in a suitable test range.
6. Begin transmitter tests at low power and increase power gradually.
7. Use reflected-power monitoring and VSWR shutdown protection for PA testing.

## 8. Status

- [x] Parametric electromagnetic model
- [x] S-parameter simulation
- [x] VSWR analysis
- [x] Efficiency analysis
- [x] Far-field simulation at critical frequencies
- [ ] Mechanical prototype
- [ ] VNA validation
- [ ] Measured gain and radiation patterns
- [ ] High-power validation

## 9. File Integrity

Expected SHA-256 checksums for the source files supplied for the initial repository release:

```text
7646c68c59473ab3ef5d3ee90af778fc00ede4240b99ba4c0775f083ecac2ee1  Radiova_ET_LPDA_2p4-5p8GHz.cst
efa1885ef4f5985c90454fa8287db018a2e4a7891513660951f5a3f8472c2599  Radiova_ET_LPDA_Technical_Report_TR.pdf
```

## 10. Attribution

Design and documentation: **Cem Sondur**  
Copyright (c) 2026 Cem Sondur.
