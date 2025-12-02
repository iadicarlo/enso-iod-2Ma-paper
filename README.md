# A 2 million year transient climate simulation reveals an opposing relationship between IOD and ENSO

This repository contains the analysis notebooks and data for the paper **"A 2 million year transient climate simulation reveals an opposing relationship between IOD and ENSO"**.

## Repository Structure

```
.
├── notebooks/              # Analysis notebooks
├── variables/             # Data files organized by type
│   ├── eof_analysis/      # EOF/PC analysis results
│   ├── climate_indices/   # Climate index time series
│   ├── composites/        # Composite analysis data
│   ├── orbital_params/    # Orbital parameter files
│   ├── reference_data/    # Reference datasets (COBE, ERSSTv5)
│   ├── derived_data/      # Derived fields and statistics
│   └── scripts/           # Helper scripts
├── archive/               # Archived/old versions
├── Figures_*/             # Figure output directories
├── config/                # Configuration plots
├── orbit/                 # Orbital diagram figures
└── *.png                  # Individual figure outputs
```

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

### Using uv (recommended)

[uv](https://github.com/astral-sh/uv) is a fast Python package installer and resolver.

```bash
# Install uv if you haven't already
curl -LsSf https://astral.sh/uv/install.sh | sh

# Clone the repository
git clone https://github.com/iadicarlo/enso-iod-2Ma-paper.git
cd enso-iod-2Ma-paper

# Create environment and install dependencies
uv venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
uv pip install -e .
```

### Using pip

```bash
# Clone the repository
git clone https://github.com/iadicarlo/enso-iod-2Ma-paper.git
cd enso-iod-2Ma-paper

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -e .
```

### Alternative: Using requirements.txt

```bash
pip install -r requirements_3.11.11.txt
```

## Data

The `variables/` folder contains all preprocessed data needed to run the notebooks:

- **EOF/PC analysis**: Pre-computed EOF patterns and principal components
- **Climate indices**: Niño3.4, DMI, WIO, EIO time series
- **Orbital parameters**: 2 Ma orbital forcing data
- **Composites**: SST, precipitation, wind stress composites
- **Reference data**: COBE-SST2 and ERSSTv5 for validation

## Running the Notebooks

After installation, launch Jupyter:

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
