# Real-Time Daily and End-of-Month Effective Exchange Rates (EERs)

[![DOI](https://zenodo.org/badge/DOI/placeholder.svg)](https://doi.org/10.5281/zenodo.placeholder)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview
Forecasting period-average exchange rates efficiently requires using high-frequency data. This repository provides the first real-time dataset of daily and end-of-month effective exchange rates (EERs) for all available countries, both nominal and real. 

By accounting for the typical delay in the publication of trade weights and inflation, these real-time vintages allow researchers to properly test the predictability of period-average exchange rates against the traditional random walk hypothesis. As demonstrated in McCarthy and Snudden (2025), utilizing this daily data can significantly improve forecasting accuracy by up to 40 percent compared to using monthly averages.

**Current Status (Preprint Archive):** This repository currently serves as a static data archive (vintages through August 2022) accompanying Reserve Bank of Australia Research Discussion Paper 2025-09. It will transition to a regularly updated, living dataset upon the formal publication of the paper.

---

## Data Access & Setup

Due to GitHub's file size constraints, this dataset is distributed across two locations. 

### 1. Monthly EER Aggregates (Included in this Repository)
Real-time monthly vintages for the end-of-month (LD) and monthly average (AVE) effective exchange rates for 79 countries are hosted directly in this repository.
* **Access:** Download and extract `monthly_vintages.zip`.
* **Documentation:** See `Readme_Monthly.pdf` for a detailed description of the data construction and methodology.

### 2. Daily EER Vintages (Hosted by the RBA)
Due to the massive size of the daily data vintages (>10 GB unzipped), the daily EER series for 160 countries are hosted externally.
* **Access:** Download the complete daily dataset archive (`.zip`) from the [RBA RDP 2025-09 Supplementary Information Page](https://www.rba.gov.au/publications/rdp/2025/2025-09/supplementary-information.html). 
* **Documentation:** See `Readme_Daily.pdf` for a detailed description of data construction and methodology.

---

## Dataset Structure & Dictionary

For both datasets, data is provided in CSV format with one file per country, identified by its ISO-3 country code (e.g., `ALB.csv`).

### Monthly Aggregates (`monthly_vintages.zip`)
* **`LD/NEER/` and `LD/REER/`:** End-of-month nominal and real EER monthly vintages.
* **`AVE/NEER/` and `AVE/REER/`:** Monthly-average nominal and real EER monthly vintages.
* **`LD_Target/` and `AVE_Target/`:** Realizations ("actuals") constructed using the June 2023 vintage of bilateral nominal exchange rates (NER) and CPI, utilizing the trade weights available in the forecast year.

### Daily Vintages (RBA Download)
* **`Daily_NEER/` and `Daily_REER/`:** Monthly vintages of daily nominal and real EERs. Each CSV has one column per monthly vintage.
* **`Daily_NEER_actuals/` and `Daily_REER_actuals/`:** Realizations ("actuals") of the nominal and real EERs targeted by the forecasts. Each CSV has one column per historical set of trade weights.

*(Note: Real and nominal bilateral exchange rates are not included in these archives and must be obtained from their original sources).*

---

## Replication Materials & Code

A complete replication package is available alongside the daily dataset on the [RBA RDP 2025-09 Supplementary Information Page](https://www.rba.gov.au/publications/rdp/2025/2025-09/supplementary-information.html). 

This package includes the necessary **R** and **Stata** code required to reproduce the out-of-sample forecast evaluation of EERs presented in the paper.

---

## How to Cite
When using this dataset, please cite the paper:

> McCarthy, M., and S. Snudden. (2025). *Forecasts of Period-average Exchange Rates: Insights from Real-time Daily Data*. Reserve Bank of Australia Research Discussion Papers, rdp2025-09.

<details>
<summary><b>Click to copy BibTeX entry</b></summary>

```bibtex
@techreport{mccarthy2025forecasts,
  title={Forecasts of Period-average Exchange Rates: Insights from Real-time Daily Data},
  author={McCarthy, Martin and Snudden, Stephen},
  year={2025},
  institution={Reserve Bank of Australia},
  type={Research Discussion Papers},
  number={rdp2025-09},
  doi={10.47688/rdp2025-09}
}

```

</details>



