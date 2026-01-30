# Poisson Generalized Linear Models for Urban Bird Collisions

This repository contains R code implementing **Poisson Generalized Linear Models (GLMs)** to analyze bird collision probabilities across urban-agricultural landscapes. The workflow focuses on identifying key landscape metrics that influence collision risk and evaluating scale effects across different bird groups.

## 🎯 Objectives
1. Identify the landscape variables that best explain collision probability (odds-ratio).
2. Select the most parsimonious GLM to explain collision rates.
3. Assess the effect of spatial scale (250 m, 500 m, 1000 m) on variable importance.

## 📂 Repository Contents
- **Poisson_all_script_v1.Rmd**: Main script with the full analysis pipeline.
- **Key steps include:**
  - Correlation analysis (Spearman) for variable selection.
  - Poisson GLM fitting with standardized predictors.
  - Collinearity assessment using VIF.
  - Model selection and averaging with AICc (`MuMIn` package).
  - Calculation of *Incidence Rate Ratios* (IRR) with confidence intervals.
  - Visualization of results via forest plots.

## 📦 Required R Packages
- `dplyr`
- `psych`
- `corrplot`
- `readxl`
- `car`
- `MuMIn`
- `ggplot2`

## 📊 Data
The analysis uses landscape metrics derived from urban vegetation, forests, semi-open areas, wetlands, and water bodies.  
Data are stored in **LandscapeMetrics_AllLevels_v9.xlsx**, organized by buffer scales (250 m, 500 m, 1000 m) and bird groups.

## 📈 Expected Outputs
- Correlation matrices for each scale and bird group.
- Poisson GLMs fitted and refined by collinearity checks.
- IRR tables with 95% confidence intervals.
- Forest plots showing relative importance and effect direction of predictors.

## 🚀 Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/GLM-biodiversity.git
