# Flight Data Analysis & Anomaly Detection

Pipeline for analyzing helicopter flight recorder data (Mi-17V5 and Mi-35P) 
exported from SCAT software.

## Overview
- **Aircraft**: Mi-17V5 (BUR recorder) and Mi-35P (Koder-35M recorder)
- **Data**: 8 flights, CSV format, 1Hz resampled
- **Methods**: Manufacturer threshold detection + Isolation Forest

## Pipeline
1. Data loading and resampling to 1Hz
2. In-flight filtering (Weight-on-Wheels sensor)
3. Interactive multi-parameter visualization (Plotly)
4. Anomaly detection: Level 1: manufacturer limits (auto-loaded from docx)
5. Anomaly detection: Level 2: Isolation Forest (scikit-learn)
6. Critical evaluation of results

## Structure
flight_analysis/
    notebooks/ # Jupyter notebooks
    data_local/ # Real flight data (not shared)
    data_public/ # Anonymized samples
    README.md
    Requierment.txt

## Requirements
pip install -r requirements.txt
