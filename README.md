# Orbital Telemetry and Economic Reality 🛰️📈

> **Assessing Satellite Nighttime Lights for High-Frequency Macroeconomic Nowcasting and Crisis Detection**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![R-Project](https://img.shields.io/badge/Language-R%20%7C%20Econometrics-blue)](https://www.r-project.org/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--4999--1861-green)](https://orcid.org/0009-0003-4999-1861)
[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.22095939-blue)](https://doi.org/10.5281/zenodo.22095939)
[![Research Status](https://img.shields.io/badge/Status-Research%20Preprint-orange)](#)

---

## 📌 Executive Summary

Traditional macroeconomic monitoring relies heavily on official national accounts data, such as Gross Domestic Product. However, in developing nations or regions with weak institutional capacity, official statistics are frequently compromised by measurement errors, substantial publication lags, informal economy omissions, and political manipulation.

This research repository implements a spatial econometric framework that evaluates Satellite Nighttime Lights—captured via NASA and NOAA low-Earth orbit sensors—as an objective, politically neutral, and real-time proxy for macroeconomic output tracking, high-frequency nowcasting, and crisis detection.

---

## 🔬 Methodology and Approach

Rather than relying on self-reported state data, this project bridges satellite sensor physics with macroeconomic accounting. We quantify nighttime luminosity by measuring the actual light energy radiating from the Earth's surface into space. This raw physical data is processed to filter out background noise (like clouds and natural terrain) and is then matched against geographic country borders.

We construct a massive longitudinal dataset spanning from 1990 to 2024, pairing these satellite light metrics with official World Bank indicators, including real GDP per capita, national statistical quality scores, and oil dependency metrics. To find the true economic signal, the codebase utilizes advanced Panel Fixed Effects regression models. This approach isolates the actual economic activity by mathematically controlling for permanent country characteristics (like land size and natural geography) as well as global economic shocks.

---

## 📊 Key Findings

Our empirical analysis provides several critical insights into how satellite lights reflect economic reality:

* **The Core Relationship:** We confirm a highly significant, positive connection between nighttime illumination and formal economic output. Satellite-detected energy output serves as a reliable and unmanipulable physical footprint of real aggregate economic activity globally.
* **Development Asymmetries:** The way economic growth translates into light differs based on a country's development stage. Emerging markets tend to grow via horizontal urban sprawl, producing a massive expansion of light pollution. In contrast, advanced post-industrial states grow through capital-intensive, energy-efficient technologies, meaning their economic growth produces a less dramatic increase in raw light output.
* **Real-Time Crisis Detection:** By analyzing historical micro-trajectories, specifically during the 2008 Great Recession, we proved that industrial zones and urban footprints physically darken during economic shocks. Satellite imagery successfully captures these severe structural downturns simultaneously with, or even before, the release of official national statistics.
* **Resource Economy Resilience:** We tested whether economies heavily dependent on oil extraction would break our tracking model, given that oil rigs are usually far from major cities. The results showed that they do not. The wealth generated from isolated oil extraction is ultimately injected into national banking, administrative, and consumer centers, triggering urban illumination that accurately mirrors the country's overall economic health.
* **Nowcasting vs. Long-term Forecasting:** While satellite lights are incredibly powerful for real-time assessment (nowcasting) and verifying current economic conditions, structural data gaps in developing nations make it difficult to use them for long-term (multi-year) predictive forecasting.

---

## 🛠️ Data Pipeline & Technology Stack

* **Data Acquisition:** Automated extraction of macroeconomic indicators directly from the World Bank API.
* **Spatial Processing:** High-resolution spatial rendering, geographic polygon mapping, and noise filtering to clean satellite imagery data.
* **Econometric Modeling:** Implementation of robust panel data models designed to correct for internal data inconsistencies and accurately measure economic shifts over time.

---

## 🎯 Operational Applications

1. **Central Bank Monetary Policy:** Monetary authorities can deploy this automated processing to detect under-reported shadow economy activity and verify official GDP releases before making critical interest rate decisions.
2. **Sovereign Debt Risk Monitoring:** International financial institutions can use monthly light radiance shifts as an early-warning signal for sovereign default risks or economic contractions caused by geopolitical conflicts.
3. **Alternative Investment Data:** Quantitative macro funds can monitor high-resolution pixel luminosity over specific industrial zones, ports, and extraction hubs to estimate quarterly productivity before official trade statistics are published.

---

## ✒️ Citation & Author Info

**Author:** Bekdaulet Abzhamiev  
**Role:** Researcher  
**ORCID:** [0009-0003-4999-1861](https://orcid.org/0009-0003-4999-1861)
