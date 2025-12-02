# A 2 million year transient climate simulation reveals an opposing relationship between IOD and ENSO

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
├── environment.yml        # Conda environment specification
└── requirements.txt       # Pip requirements (frozen versions)
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

### Using conda (recommended)

```bash
# Clone the repository
git clone https://github.com/iadicarlo/enso-iod-2Ma-paper.git
cd enso-iod-2Ma-paper

# Create environment from environment.yml
conda env create -f environment.yml
conda activate enso-iod-2ma
```

### Using pip

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

## Data Requirements

The notebooks require preprocessed data files (not included in this repository):

- **EOF/PC analysis**: Pre-computed EOF patterns and principal components
- **Climate indices**: Niño3.4, DMI, WIO, EIO time series (2 Ma)
- **Orbital parameters**: 2 Ma orbital forcing data
- **Composites**: SST, precipitation, wind stress composites
- **Reference data**: COBE-SST2 and ERSSTv5 for validation

Please contact the authors for access to the data files.

## Running the Notebooks

After installation and obtaining the data, launch Jupyter:

```bash
jupyter notebook
```

Navigate to the `notebooks/` folder and open any notebook. The notebooks are designed to run sequentially but can also be run independently.

## Citation

If you use this code or data, please cite:

> [Author list]. (Year). A 2 million year transient climate simulation reveals an opposing relationship between IOD and ENSO. *Journal*, *Volume*(Issue), pages. DOI

## Contact

**Ibrahim Abdelkader Di Carlo**  
Email: i.r.d.abdelkaderdicarlo@uu.nl  
Utrecht University

## License

[Specify license here]
