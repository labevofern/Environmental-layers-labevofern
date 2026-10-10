## Citation

If you use environmental layers from this repository, please cite:

Mendonça, N. A., Gutiérrez-Duque, D., & Almeida, T. E. (2026). *Environmental layers: Environmental raster datasets for ecological and biogeographical analyses* [Data repository]. GitHub. https://github.com/labevofern/Environmental-layers

# Environmental Layers

## Overview

This repository contains environmental raster datasets compiled for ecological, biogeographical, and spatial analyses.

The datasets include elevation, bioclimatic variables, net primary productivity, cloud forest predictions, and soil properties. These environmental predictors can be used to investigate species distributions, environmental gradients, habitat suitability, and ecological patterns.

## Environmental Variables

### 1. Elevation

Elevation data were obtained from the Shuttle Radar Topography Mission (SRTM), distributed through WorldClim version 2.1.

Elevation represents the height of the terrain above sea level and is an important predictor of environmental conditions, including temperature, precipitation, and habitat distribution.

- **Source:** SRTM / WorldClim v2.1
- **Spatial resolution:** 30 arc-seconds (~1 km)
- **Accessed:** July 25, 2026

### 2. Bioclimatic Variables

Bioclimatic variables were obtained from WorldClim version 2.1.

The dataset includes 19 bioclimatic variables (BIO1–BIO19), derived from temperature and precipitation data. These variables describe annual climatic trends, seasonality, and extreme environmental conditions.

The variables include:

1. **BIO1:** Annual Mean Temperature
2. **BIO2:** Mean Diurnal Range
3. **BIO3:** Isothermality
4. **BIO4:** Temperature Seasonality
5. **BIO5:** Maximum Temperature of Warmest Month
6. **BIO6:** Minimum Temperature of Coldest Month
7. **BIO7:** Temperature Annual Range
8. **BIO8:** Mean Temperature of Wettest Quarter
9. **BIO9:** Mean Temperature of Driest Quarter
10. **BIO10:** Mean Temperature of Warmest Quarter
11. **BIO11:** Mean Temperature of Coldest Quarter
12. **BIO12:** Annual Precipitation
13. **BIO13:** Precipitation of Wettest Month
14. **BIO14:** Precipitation of Driest Month
15. **BIO15:** Precipitation Seasonality
16. **BIO16:** Precipitation of Wettest Quarter
17. **BIO17:** Precipitation of Driest Quarter
18. **BIO18:** Precipitation of Warmest Quarter
19. **BIO19:** Precipitation of Coldest Quarter

Two spatial resolutions are available:

- **10 arc-minutes:** Approximately 18 km at the equator.
- **30 arc-seconds:** Approximately 1 km at the equator.

**Source:** WorldClim v2.1

**Accessed:** July 25–26, 2026

### 3. Net Primary Productivity (NPP)

Net Primary Productivity (NPP) represents the rate at which vegetation accumulates organic carbon through photosynthesis after accounting for plant respiration.

NPP provides an estimate of ecosystem productivity and carbon availability and is widely used in ecological and biogeographical studies.

The dataset was derived from the MODIS MOD17 product and includes annual estimates for the period 2000–2015.

- **Source:** MODIS MOD17
- **Temporal coverage:** 2000–2015
- **Spatial resolution:** 30 arc-seconds (~1 km)
- **Format:** GeoTIFF

### 4. Cloud Variables

#### Cloud Forest Prediction

Cloud forest prediction data were obtained from EarthEnv.

These data describe the predicted spatial distribution of cloud forest environments, which are associated with atmospheric moisture, cloud formation, and particular climatic and topographic conditions.

Cloud-related environmental information can be useful for investigating species distributions, habitat suitability, and ecological processes in montane ecosystems.

- **Source:** EarthEnv
- **Spatial resolution:** 30 arc-seconds (~1 km)
- **Accessed:** August 3, 2026

### 5. Soil Variables

Soil properties were obtained from SoilGrids, developed by the International Soil Reference and Information Centre (ISRIC).

The dataset includes six soil variables representing the 5–15 cm soil depth interval.

These properties describe soil physical and chemical characteristics that can influence vegetation distribution, nutrient availability, and ecological processes.

The following variables are included:

1. **Cation Exchange Capacity (CEC):**
   Represents the capacity of soil to retain and exchange positively charged ions, an important indicator of soil fertility and nutrient availability.

2. **Clay Content:**
   Represents the proportion of clay particles in the soil, influencing water retention, nutrient storage, and soil structure.

3. **Soil pH (H₂O):**
   Measures soil acidity or alkalinity, influencing nutrient availability, microbial activity, and plant growth.

4. **Sand Content:**
   Represents the proportion of sand particles in the soil, affecting drainage, aeration, and water-holding capacity.

5. **Silt Content:**
   Represents the proportion of silt particles in the soil, influencing soil texture, moisture retention, and physical properties.

6. **Soil Organic Carbon (SOC):**
   Represents the organic carbon stored in the soil, an important indicator of soil organic matter, fertility, and carbon cycling.

- **Source:** SoilGrids (ISRIC)
- **Soil depth:** 5–15 cm
- **Data format:** GeoTIFF

---

## Repository Access and Git LFS

The repository contains large raster files managed using Git Large File Storage (Git LFS).

### Clone the repository

```bash
git clone https://github.com/labevofern/Environmental-layers.git
cd Environmental-layers
```

### Install Git LFS

On macOS, Git LFS can be installed using Homebrew:

```bash
brew install git-lfs
```

Initialize Git LFS and download the datasets:

```bash
git lfs install
git lfs pull
```

### Upload Large Raster Files

To track and upload GeoTIFF files using Git LFS:

```bash
git lfs install
git lfs track "*.tif"
git add .gitattributes
git add .
git commit -m "Add environmental raster layers"
git push origin main
```

Git LFS facilitates the management and version control of large geospatial datasets.

---

## Data Sources and Acknowledgments

The environmental layers were compiled from publicly available environmental databases:

- **WorldClim v2.1:** Elevation and bioclimatic variables.
- **MODIS MOD17:** Net Primary Productivity.
- **EarthEnv:** Cloud forest prediction.
- **SoilGrids (ISRIC):** Soil physical and chemical properties.

Users of these datasets should also acknowledge and cite the original data providers in scientific publications.
