# Passive Reflector Measurement 

## 1. Overview

This dataset contains measured angular reflection patterns at 26–30 GHz and corresponding simulated patterns at 28 GHz. **Each measured frequency and each simulated pattern is independently normalized to its own peak (0 dB)** within each case.

## 2. Dataset contents

The dataset contains 12 CSV files:

| File | Surface | Designed incidence | Designed reflection | Measured incidence |
| --- | --- | ---: | ---: | ---: |
| `metal_inc0.csv` | Metal plate | — | Specular | 0° |
| `metal_incm15.csv` | Metal plate | — | Specular | −15° |
| `metal_incm30.csv` | Metal plate | — | Specular | −30° |
| `nominal_inc0_ref45.csv` | IMST | 0° | +45° | 0° |
| `nominal_inc0_ref60.csv` | TMYTEK | 0° | +60° | 0° |
| `nominal_inc0_refm60.csv` | TMYTEK | 0° | −60° | 0° |
| `nominal_incm30_ref15.csv` | TMYTEK | −30° | +15° | −30° |
| `nominal_incm30_ref60.csv` | TMYTEK | −30° | +60° | −30° |
| `non_nominal_inc0_ref45_txm15.csv` | IMST | 0° | +45° | −15° |
| `non_nominal_inc0_ref60_txm15.csv` | TMYTEK | 0° | +60° | −15° |
| `non_nominal_incm30_ref15_tx0.csv` | TMYTEK | −30° | +15° | 0° |
| `non_nominal_incm30_ref60_tx0.csv` | TMYTEK | −30° | +60° | 0° |

In filenames, `m` preceding an angle denotes a negative value (e.g., `incm30` = −30°). Nominal/non-nominal refers to whether the measured illumination matches the surface's designed incidence.

## 3. CSV schema

| Column | Description | Unit |
| --- | --- | --- |
| `angle_deg` | Receiver observation angle | degrees |
| `meas_26_ghz` | Normalized measured magnitude at 26 GHz | dB |
| `meas_27_ghz` | Normalized measured magnitude at 27 GHz | dB |
| `meas_28_ghz` | Normalized measured magnitude at 28 GHz | dB |
| `meas_29_ghz` | Normalized measured magnitude at 29 GHz | dB |
| `meas_30_ghz` | Normalized measured magnitude at 30 GHz | dB |
| `sim_28_ghz` | Normalized simulated magnitude at 28 GHz | dB |

Normalization is performed separately for each frequency/pattern, so values describe relative angular levels, not absolute received power or cross-frequency peak differences.

## 4. Missing values

Blank, `NaN`, or non-finite values (including `-inf`) should be treated as **unavailable data at that angle**, not as zero-valued measurements. Readers should exclude these entries from analysis as appropriate. The original CSV values are left unchanged.

## 5. Measurement setup

Indoor VNA-based measurements were performed over 26–30 GHz with a receiver scanning an angular arc approximately 2.5 m from the reflector. The dataset covers a metal plate and IMST/TMYTEK passive reflective surfaces under nominal and non-nominal transmitter incidence (0°, −15°, or −30°, depending on the case). Absorbers were used to reduce environmental reflections. See the associated publication for the full setup and measurement procedure.

## 6. Related publication and citation

**Paper:** 

**Dataset:** 

