# Multi-Cloud AGN Simulation with pyCloudy

A Python framework for simulating multi-layer active galactic nucleus (AGN) cloud structures using Cloudy photoionization code and pyCloudy wrapper. This project generates 3D emission maps and continuum spectra for complex AGN geometries.

## Overview

This code simulates AGN cloud structures with multiple concentric shells, each representing different physical regions (BLR, torus/BALR, NLR). It computes:

- **3D emission maps** for Lyα (1215.67 Å) and Hα (6562.81 Å)
- **Transmitted continuum** through each cloud layer
- **Reflection and scattering** between clouds
- **Multi-angle observations** (spherical geometry)

The framework is designed to model systems like **Mrk 231** (Veilleux et al. 2013) and similar AGN with complex multi-phase outflows.

---

## Features

- **Multi-cloud cascading**: Output from inner clouds feeds as input to outer clouds
- **Ellipsoidal geometry**: Models clouds with variable aspect ratios
- **Angular dependence**: Simulates clouds at different viewing angles (theta)
- **Density laws**: Supports radial and angular density variations (power-law profiles)
- **3D visualization**: Generates projected emission maps from Cloudy output
- **Continuum plotting**: Visualizes UV-optical spectra with absorption/emission features
- **Automatic scaling**: Handles physical size ratios between nested clouds

---

## Requirements

### Software
- [Cloudy](https://gitlab.nublado.org/cloudy/cloudy/-/wikis/home) (v17.03 or later recommended)
- Python 3.7+
- [pyCloudy](https://github.com/Morisset/pyCloudy) 0.10.0+

### Python Packages
```bash
pip install numpy matplotlib scipy pyCloudy
```

---

## Installation

1. **Clone the repository:**
```bash
git clone https://github.com/Nietzschedgie/pyCloudy-multi-cloud-agn.git
cd multi-cloud-agn
```

2. **Set Cloudy path:**
Edit the script to point to your Cloudy installation:
```python
# In your script
cloudy_path = '/path/to/cloudy/source/cloudy.exe'
pc.config.cloudy_exe = cloudy_path
```

3. **Create output directory:**
```bash
mkdir models
```

---
