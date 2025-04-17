# Thesis Code: Mg II Absorption Analysis in Post-Starburst Galaxies

This repository contains the Python code used for analyzing Mg II absorption features in post-starburst galaxies and nearby quasars. The analysis supports the results presented in the bachelor's thesis titled:

**"Searching for Mg II absorption in quasar spectra near E+A post-starburst galaxies with fast outflows"**

## 📂 Files

- `Thesis_code.ipynb`: The main Jupyter notebook containing all code used in the thesis, fully annotated with explanations and section headers.
- Spectral data files (not included here) were sourced from SDSS and saved in local directories under `../data/spectra/`.

## 🧪 What the Code Does

The code follows this logical sequence:

1. **Load and Inspect FITS Spectra**  
   - Reads galaxy or quasar spectra from SDSS FITS files  
   - Extracts and plots raw flux vs wavelength

2. **Continuum Normalization**  
   - Fits a polynomial continuum  
   - Normalizes the spectrum and optionally clips extreme flux spikes

3. **Redshift Query**  
   - Retrieves redshifts using Astroquery's SDSS interface  
   - Used for both galaxies and verification of quasar redshifts

4. **Spectral Line Analysis**  
   - Calculates expected wavelengths of Mg II and O II lines using redshift  
   - Plots these line positions in both galaxy and quasar spectra  
   - Velocity shifts are computed from observed vs expected wavelengths

5. **Quasar Search using NED**  
   - Searches for quasars near selected post-starburst galaxies using NED  
   - Filters based on type, redshift proximity, and angular distance  
   - Downloads spectra for matched quasars via SDSS

6. **Galaxy–Quasar Matching**  
   - Computes angular and projected physical distances between galaxy and each quasar  
   - Visualizes positional relationships in RA/Dec space with optional distance circles

7. **Sky Map and Visualization**  
   - Generates sky map plots (e.g. Aitoff projection) showing galaxies and quasars  
   - Draws customizable angular separation circles with unique color coding

## 🛠️ Requirements

Install the following Python packages to run the notebook:

```bash
pip install numpy matplotlib astropy specutils astroquery
```

## 📘 Usage

Open the notebook:

```bash
jupyter notebook Thesis_code.ipynb
```

Ensure that SDSS FITS files are placed in `../data/spectra/` or update the paths accordingly.

## 📜 License

This code is part of an academic project and is shared for transparency and reproducibility. You may reuse or adapt it with proper citation.

## 🙏 Acknowledgements

Thanks to SDSS and NED for public data access, and to the developers of `astropy`, `specutils`, and `astroquery` for enabling this scientific workflow.