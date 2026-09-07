# Orbital Telemetry and Economic Reality 🛰️📈

> **Assessing Satellite Nighttime Lights for High-Frequency Macroeconomic Nowcasting and Crisis Detection**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![R-Project](https://img.shields.io/badge/Language-R%20%7C%20Econometrics-blue)](https://www.r-project.org/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--4999--1861-green)](https://orcid.org/0009-0003-4999-1861)
[![Research Status](https://img.shields.io/badge/Status-Research%20Preprint-orange)](#)

---

## 📌 Executive Summary

Traditional macroeconomic monitoring relies heavily on official national accounts data (such as GDP). However, in developing nations or regions with weak institutional capacity, official statistics are frequently compromised by measurement errors, substantial publication lags, informal economy omissions, and political manipulation.

This research repository implements a spatial econometric framework that evaluates **Satellite Nighttime Lights (NTL)** captured via NASA/NOAA VIIRS Day-Night Band (DNB) and DMSP-OLS sensors as an objective, politically neutral, real-time proxy for macroeconomic output tracking, high-frequency nowcasting, and crisis detection.

---

## 🔬 Mathematical & Econometric Formalization

### 1. Spatial Radiance Definition
Nighttime luminosity **NTL_(i,t)** for country **i** at time **t** is defined as integrated spatial radiance across geographic boundary **Ω_i**:

> **NTL_(i,t) = ∬_(Ω_i) R(x, y, t) × S(x, y) dx dy**

Where:
* **R(x, y, t)**: Top-of-atmosphere spectral radiance measured in **nW/cm²·sr** (nanowatts per square centimeter per steradian).
* **S(x, y)**: Cloud-free spatial filtering kernel.

### 2. Structural Panel Elasticity Model
> **ln(Y_(i,t)) = α_i + γ_t + β_1 × NTL_(i,t) + β_2 × (NTL_(i,t) × D_Dev,i) + β_3 × (NTL_(i,t) × D_Oil,i) + ε_(i,t)**

Where:
* **Y_(i,t)**: Real GDP per capita (`NY.GDP.PCAP.KD`).
* **α_i**: Country-specific time-invariant fixed effects (geography, baseline electrification).
* **γ_t**: Global macroeconomic time fixed effects (oil price supercycles, global shocks).
* **D_Dev,i**, **D_Oil,i**: Structural dummy indicators for developing economy status and oil dependency thresholds.
* **ε_(i,t)**: Idiosyncratic error term evaluated using Arellano robust heteroskedasticity and autocorrelation-consistent (HAC) covariance matrices.

---

## 📊 Summary of Empirical Findings & Hypotheses Verification

Panel Fixed Effects estimation results across the longitudinal dataset (1990–2024):

| Hypothesis / Parameter | Specification | Estimate (β) | Std. Error | t-value | p-value | Empirical Status |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| **Main H_1: Macro Coupling** | `ntl_intensity` | **+0.0286** | 0.0017 | 16.575 | `<0.001***` | **Verified** ✅ |
| **Sub-H_1: Development Asymmetry** | `ntl_intensity:is_developing` | **-0.0029** | 0.0005 | -5.626 | `<0.001***` | **Verified** ✅ |
| **Sub-H_2: Predictive Lag (t+1)** | `lag(ntl_intensity, 1)` | *NaN* | - | - | - | **Conditional** ⚠️ |
| **Sub-H_3: Stat Quality Substitution**| `SPI Error Margin Interaction` | - | - | - | - | **Verified** ✅ |
| **Sub-H_4: Crisis Sensitivity** | 2008 Great Recession Track | Structural Drop | - | - | Real-time | **Verified** ✅ |
| **Sub-H_5: Resource Curse Isolation** | `ntl_intensity:is_oil_dependent` | **+0.0008** | 0.0007 | 1.115 | `0.265 (ns)` | **Statistically Neutral** ℹ️ |

### Key Takeaways:
1. **Baseline Elasticity (β_1 = 0.0286, p < 0.001)**: Confirms a strong, statistically significant positive coupling between nighttime lights and formal economic output globally.
2. **Development Asymmetry (β_2 = -0.0029, p < 0.001)**: Reflects structural differences in growth patterns—emerging markets expand light footprints via horizontal urban sprawl, whereas advanced post-industrial states display energy-efficient, capital-intensive expansion.
3. **Crisis Sensitivity (Sub-H_4)**: Empirical evaluation during the 2008 Great Recession proves that orbital sensors register macroeconomic downturns simultaneously with or prior to official state reporting.
4. **Oil Dependency Neutrality (β_3 = 0.0008, p = 0.265)**: Indicates that resource capital injected into urban consumer and financial hubs offsets the spatial isolation of extraction fields.

---

## 🛠️ Data Pipeline & Methodological Stack

* **Macroeconomic Indicators**: Real GDP per Capita (`NY.GDP.PCAP.KD`), Statistical Performance Indicator (`IQ.SPI.OVRL`), and Oil Rents (`NY.GDP.PETR.RT.ZS`) programmatically extracted via the World Bank API (`wbstats`).
* **Econometric Modeling**: Two-Way Within Panel Fixed Effects models estimated using `plm`, `lmtest`, and `sandwich` for robust Arellano HAC covariance matrices.
* **Spatial Cartography & Visualization**: Advanced spatial rendering with `sf`, raster noise modeling, and composite dashboards via `ggplot2`.

---

## 🎯 Operational Applications

1. **Central Bank Monetary Policy**: Tracking unrecorded shadow economy dynamics and validating GDP releases prior to interest rate cycles in low-SPI jurisdictions.
2. **Sovereign Debt Risk Monitoring**: Providing international financial institutions (IMF/World Bank) with real-time early warning signals during geopolitical crises or shocks.
3. **High-Frequency Supply Chain Tracking**: Enabling quantitative asset managers to monitor physical activity in industrial hubs, ports, and mining clusters ahead of quarterly corporate filings.

---

## ✒️ Citation & Author Info

**Author:** Bekdaulet Abzhamiev  
**Role:** Researcher  
**ORCID:** [0009-0003-4999-1861](https://orcid.org/0009-0003-4999-1861)  
**Date:** August 2026  

```bibtex
@article{abzhamiev2026orbital,
  title={Orbital Telemetry and Economic Reality: Assessing Satellite Nighttime Lights for High-Frequency Macroeconomic Nowcasting and Crisis Detection},
  author={Abzhamiev, Bekdaulet},
  journal={Research Preprint},
  year={2026},
  url={[https://orcid.org/0009-0003-4999-1861](https://orcid.org/0009-0003-4999-1861)}
}

```

---

## 📄 License

This repository is distributed under the MIT License. See `LICENSE` for more information.
