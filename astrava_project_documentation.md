# ASTRAVA — Unveiling Lunar and Martian Terrain Signatures on Earth
> **Digital Image Processing Framework for Planetary Analog Identification**

ASTRAVA is a Digital Image Processing project that aims to discover and characterize potential terrestrial analog sites on Earth by identifying surface and terrain characteristics similar to selected regions of the Moon and Mars. These terrestrial analogs support research and mission preparation for future permanent lunar bases and Martian exploration missions.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Target Environments & Data Sources](#target-environments--data-sources)
- [Digital Image Processing Pipeline](#digital-image-processing-pipeline)
- [Feature Matching & Similarity Scoring](#feature-matching--similarity-scoring)
- [Interactive Visualization Dashboard](#interactive-visualization-dashboard)
- [Expected Outcomes & Scope](#expected-outcomes--scope)

---

## Project Overview

Establishing human presence on the Moon and Mars requires extensive ground testing in representative environments on Earth. **ASTRAVA** uses open-source satellite imagery, planetary remote sensing datasets, and advanced spatial image processing techniques to identify, score, and rank potential terrestrial analog sites automatically.

---

## Target Environments & Data Sources

ASTRAVA integrates open-source datasets from agencies such as NASA, ESA, and USGS across specific terrestrial and extraterrestrial regions of interest:

| Category | Target Regions & Environments | Primary Dataset Focus |
| :--- | :--- | :--- |
| **Earth Environments** | Deserts, polar ice/tundra regions, volcanic landscapes, impact craters | High-resolution multispectral imagery & Digital Elevation Models (DEM) |
| **Lunar Regions** | Shackleton Crater, Malapert Massif | Surface roughness, permanent shadow regions, topography |
| **Martian Regions** | Jezero Crater, Gale Crater | Palaeolake sediment structures, deltaic deposits, dust distribution |

---

## Digital Image Processing Pipeline

The core image processing workflow applies multiple spatial, texture, and topographic techniques to isolate surface signatures:

1. **Grayscale Transformation & Histogram Analysis:**  
   Standardizes dynamic range and tonal distributions across varying sun illumination angles and atmospheric conditions.
2. **Contrast Enhancement:**  
   Applies Adaptive Histogram Equalization (AHE) and linear contrast stretching to highlight subtle geological and topographic variations.
3. **Edge Detection & Structural Extraction:**  
   Utilizes spatial filters (e.g., Sobel, Canny, Laplacian) to map crater rims, fault lines, bedrock exposures, and ridge lines.
4. **Texture Analysis via GLCM:**  
   Extracts Gray-Level Co-occurrence Matrix (GLCM) features—including contrast, energy, homogeneity, and correlation—to quantify surface roughness and grain texture.
5. **Topographical Analysis:**  
   Calculates slope, aspect, elevation profiles, and surface roughness metrics from Digital Elevation Models (DEMs).
6. **Multispectral & False-Color Composites:**  
   Generates tailored RGB and false-color band combinations to differentiate mineralogical signatures and surface composition.

---

## Feature Matching & Similarity Scoring

To evaluate candidate terrestrial sites objectively against lunar and Martian reference locations:

- **Vector Feature Extraction:** Quantitative parameters from texture (GLCM), topography (slope/roughness), and spectral signatures are combined into multidimensional feature vectors.
- **Normalized Feature Distance:** Implements normalized Euclidean and Cosine distance algorithms to compute cross-planetary similarity metrics.
- **Sensor & Resolution Calibration:** Adjusts scoring calculations for differences in spatial resolution, radiometric range, and sensor geometry across Earth, Lunar, and Martian datasets.

---

## Interactive Visualization Dashboard

An interactive dashboard allows researchers and mission planning teams to visualize, query, and filter candidate site rankings:

* **Dual-View Image Comparison:** Side-by-side visualization of raw, enhanced, edge-detected, and texture-mapped imagery.
* **Topographic & Texture Panels:** Real-time plots for GLCM metrics, slope histograms, and elevation cross-sections.
* **Analytical Heatmaps:** Geographically projected similarity heatmaps indicating feature correlation across regional target zones.
* **Dynamic Site Ranking:** Filterable leaderboards that rank potential analog sites based on customizable feature weights.

---

## Expected Outcomes & Scope

- **Primary Deliverable:** An open, reproducible Digital Image Processing framework for preliminary site screening.
- **Research Impact:** Streamlines site selection and lowers reconnaissance costs for lunar base site selection and rover testing operations.
- **Scope Disclaimer:** Output similarity scores serve as preliminary screening indicators and must be validated through follow-up field geology, environmental sampling, and engineering assessments.