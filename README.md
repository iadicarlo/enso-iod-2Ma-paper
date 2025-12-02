# A 2 million year transient climate simulation reveals an opposing relationship between IOD and ENSO

[![DOI](https://zenodo.org/badge/1107786948.svg)](https://doi.org/10.5281/zenodo.17781292)

This repository contains the analysis notebooks for the paper **"A 2 million year transient climate simulation reveals an opposing relationship between IOD and ENSO"**.

## Repository Structure

```
.
├── notebooks/              # Analysis notebooks
│   ├── 1_IOD_ENSO_PC_analysis.ipynb
│   ├── 2_IOD_ENSO_mean_std.ipynb
│   ├── 3_IOD_ENSO_composites.ipynb
│   └── 4_IOD_ENSO_szn_cycle.ipynb
├── README.md              # This file
└── requirements.txt       # Python dependencies
```

**Note**: Data files and figure outputs are not included in this repository due to size constraints (>140 GB). Please contact the authors for access to the data.

## Notebooks

1. **`1_IOD_ENSO_PC_analysis.ipynb`**  
   Principal component analysis and EOF decomposition for IOD and ENSO variability.

2. **`2_IOD_ENSO_mean_std.ipynb`**  
   Mean and standard deviation analysis of IOD/ENSO indices across orbital configurations.

3. **`3_IOD_ENSO_composites.ipynb`**  
   Composite analyses for different IOD/ENSO phases and orbital configurations.

4. **`4_IOD_ENSO_szn_cycle.ipynb`**  
   Seasonal cycle analysis and diagnostics for IOD/ENSO.

## Installation

```bash
# Clone the repository
git clone https://github.com/iadicarlo/enso-iod-2Ma-paper.git
cd enso-iod-2Ma-paper

# Create a virtual environment (Python 3.11+ required)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```
