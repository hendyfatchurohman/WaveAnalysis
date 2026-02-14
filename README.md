# ERA5 Wave Analysis

This repository provides a comprehensive Python workflow for analyzing wave dynamics using ECMWF ERA5 Reanalysis data. It is specifically designed for coastal geomorphological studies and coastal engineering.

## 🌊 Why this analysis is important
Understanding wave climate (Height, Period, and Direction) is critical for:
* **Morphodynamics:** Studying how swells shape the coastline over decades.
* **Coastal Protection:** Identifying extreme events that cause erosion.
* **Renewable Energy:** Assessing potential for wave energy converters.


## 🚀 Features
* **Multi-file GRIB Processing:** Seamlessly combine limited-range ECMWF downloads using `xarray` and `dask`.
* **Publication-Quality Wave Roses:** Specialized plotting of Significant Wave Height (SWH) and Mean Wave Period (MWP) with 36-sector precision.
* **Advanced Time Series:** Dual-axis visualization with extreme event markers ($H_s > 3.0m$) and directional background overlays.
* **Journal-Ready Aesthetics:** High-DPI (300+) exports with bold formatting optimized for thesis and publication.

## 🛠️ Step-by-Step Workflow

### 1. Data Acquisition
1. Create an account at the [Copernicus Climate Data Store (CDS)](https://cds.climate.copernicus.eu/).
2. Request **"ERA5 hourly data on single levels from 1940 to present"**.
3. Select parameters: 
    * `Significant height of combined wind waves and swell`
    * `Mean wave period`
    * `Mean wave direction`
4. Download data in **GRIB** format.

### 2. Environment Setup
Install the necessary dependencies via terminal or command prompt:
```bash
pip install xarray cfgrib dask matplotlib windrose pandas
