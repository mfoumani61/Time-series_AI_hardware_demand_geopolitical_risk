# Time-series_AI_hardware_demand_geopolitical_risk
# Paper Title: A Comparative Time-Series Analysis of AI Hardware Demand Considering Geopolitical Risk in the Asia-Pacific Region: The Case Study of China and South Korea

├── README.md
├── data/
│   ├── raw/
│   │   ├── china_raw.csv
│   │   └── south_korea_raw.csv
│   └── processed/
│       └── normalized_1990_2026.csv
├── R/
│   ├── 00_setup.R
│   ├── 01_data_cleaning.R
│   ├── 02_descriptives_plots.R
│   ├── 03_structural_break.R
│   ├── 04_relative_importance.R
│   ├── 05_regressions_models_7_8.R
│   └── 06_outputs_tables_figures.R
├── output/
│   ├── tables/
│   └── figures/
└── docs/
    └── codebook.md

# What Each Piece Contains:

**1. data/raw/ — the annual 1990–2026 series for both countries, one row per year, with the exact variable names from the paper:**

    Outcome: AI_GPU_Demand

    Internal drivers: Data_Center_Count, AI_Compute_Power, Cloud_AI_Investment, Train_Compute, AI_Model_Count

    Geopolitical risks (0–10 normalized scale): Export_Control_Level, Sanctions_Index, Trade_Tension_Level, Defense_Related_Influence, Semiconductor_Security_Risk

**2. R/ scripts — must implement exactly what the paper promises:**

    Log transforms per Equations 1–6 (including the + c constant — we state what c is in codebook.md)

    Base Model (Eq. 7) and Risk-regulated Model (Eq. 8)

    Structural break tests (structural break analysis" in the paper)

    Relative importance analysis

  **3. Output and data visualizations:**

    All figures (we reproduce figures such as Figure 3 at minimum)

**4. Final documentation (docs/codebook.md):**
  
   docs/codebook.md variable-by-variable: definition, units, source, normalization rule, missing-data handling, and the c constant used in log transforms.
