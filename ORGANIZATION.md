# Repository Organization Summary

## What Was Done

### 1. Notebooks Organization
- **Main notebooks** (1, 3, 4) are kept at **root level** AND copied to `notebooks/` folder
- **Archived notebooks**: All copies, old versions, and experimental notebooks moved to `archive/`
  - IOD_ENSO-Copy*.ipynb (23 copies)
  - multiple_regression*.ipynb
  - nino_iod_relationship.ipynb
  - vera.ipynb
  - PC_analysis.ipynb

### 2. Figures Organization
- **All figures kept at root level** for easy access (used in paper)
- Figure directories preserved:
  - `config/`, `config_mean/`, `config_mean_var/`
  - `orbit/`
  - `Figures_*/` (multiple directories)
  - `szn_cycle_*/`
- Individual PNG files kept at root

### 3. Variables Folder Cleanup
Organized into subdirectories:
- **`eof_analysis/`**: EOF patterns, PCs, variance explained (*.pkl files)
- **`climate_indices/`**: Niño3.4, DMI, WIO, EIO time series (*.nc, *.csv)
- **`composites/`**: All composite analysis files (*_sel_*.nc)
- **`orbital_params/`**: pCESM orbital parameter files
- **`reference_data/`**: COBE-SST2, ERSSTv5, target grids
- **`derived_data/`**: Slopes, correlations, means, STD files
- **`scripts/`**: Python helper scripts

### 4. Archive Folder
Contains:
- Old notebook versions
- Large correlation figure directories (10,000+ PNG files)
  - dmi_cor_figs/, dmi_cor_psl_figs/, dmi_cor_taux_figs/, etc.
- Virtual environment folder (`energy/`)
- Miscellaneous files: PDFs, PSDs, pickles, posters
- Old subdirectories: cal/, script_2Ma/, original_iod_model/, etc.

### 5. New Files Created
- **`pyproject.toml`**: Modern Python project configuration with uv support
- **`README.md`**: Updated with installation instructions and repo structure
- **`.gitignore`**: Proper gitignore for Python/Jupyter projects
- **`FONT_SIZE_GUIDE.md`**: Documentation for fixing font size issues (already existed)

## File Locations

### At Root Level (Easy Access)
```
1_IOD_ENSO_PC_analysis.ipynb
3_IOD_ENSO_composites.ipynb
4_IOD_ENSO_szn_cycle.ipynb
README.md
pyproject.toml
requirements_3.11.11.txt
FONT_SIZE_GUIDE.md
*.png (all figure files)
config/, orbit/, Figures_*/, szn_cycle_*/ (figure directories)
```

### In notebooks/ Folder
```
1_IOD_ENSO_PC_analysis.ipynb (copy)
3_IOD_ENSO_composites.ipynb (copy)
4_IOD_ENSO_szn_cycle.ipynb (copy)
```

### In variables/ Folder
```
eof_analysis/       - EOF/PC results
climate_indices/    - Time series data
composites/         - Composite analyses
orbital_params/     - Orbital forcing
reference_data/     - Validation datasets
derived_data/       - Processed fields
scripts/            - Helper scripts
```

### In archive/ Folder
```
All old notebooks, copies, and experimental files
Large correlation figure directories
Virtual environment
Miscellaneous old files
```

## Next Steps for GitHub

1. **Review the structure** - Make sure all needed figures are accessible
2. **Test notebooks** - Verify they run with the new pyproject.toml
3. **Add to git**:
   ```bash
   git add notebooks/ variables/ *.png config/ orbit/ Figures_*/ szn_cycle_*/
   git add pyproject.toml README.md .gitignore FONT_SIZE_GUIDE.md
   git add 1_IOD_ENSO_PC_analysis.ipynb 3_IOD_ENSO_composites.ipynb 4_IOD_ENSO_szn_cycle.ipynb
   ```
4. **Commit and push**:
   ```bash
   git commit -m "Organize repository structure with notebooks, data, and figures"
   git push -u origin main
   ```

## Notes

- **Figures remain at root** for easy access and paper preparation
- **Notebooks at root** for immediate use, copies in `notebooks/` for organization
- **Variables organized** but not removed - all data preserved
- **Archive folder** contains everything not immediately needed but kept for reference
- **No files deleted** - everything moved to appropriate locations

