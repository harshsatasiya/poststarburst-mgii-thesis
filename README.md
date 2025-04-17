# Thesis Code: Mg II Absorption Analysis in Post-Starburst Galaxies

This repository contains the Python code used for analyzing Mg II absorption features in post-starburst galaxies and nearby quasars. The analysis supports the results presented in the bachelor's thesis titled:

**"Searching for Mg II absorption in quasar spectra near E+A post-starburst galaxies with fast outflows"**

## 📂 Files

- `Thesis_code.ipynb`: The main Jupyter notebook containing all code used in the thesis, with added explanations and section headers.
- Spectral data files (not included here) were sourced from SDSS and saved in local directories under `../data/spectra/`.

## 🧪 What the Code Does

The code performs the following key steps:

1. **Load and Inspect FITS Spectra**  
   - Reads galaxy/quasar spectra from SDSS FITS files  
   - Extracts and plots raw flux and wavelength

2. **Continuum Normalization**  
   - Fits a polynomial continuum  
   - Normalizes and optionally clips extreme flux values

3. **Redshift Query**  
   - Retrieves redshifts of galaxies or quasars using Astroquery and SDSS

4. **Line Analysis**  
   - Calculates expected positions of Mg II and O II lines based on redshift  
   - Compares observed vs expected to calculate velocity shifts  
   - Plots absorption features and marks expected wavelengths

5. **Visualization**  
   - RA/Dec sky maps of galaxies and quasars  
   - Angular separation visualization with customizable color-coded circles

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

Make sure the spectrum files are accessible in the relative paths used inside the code (`../data/spectra/`).

## 📜 License

This code is part of an academic research project and is shared for transparency and reproducibility. Feel free to use or adapt it with appropriate credit.

## 🙏 Acknowledgements

Thanks to SDSS and NED for open access to data, and to the developers of `astropy`, `specutils`, and `astroquery` for enabling this workflow.
