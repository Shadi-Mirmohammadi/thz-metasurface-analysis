# THz Metasurface Modulator Analysis

Automated analysis pipeline for terahertz metasurface modulators based on
Fe:Ga₂O₃, processing HFSS simulation exports into publication-ready figures.

## What this does
- Loads HFSS Floquet-port reflection sweeps across 13 conductivity states (σ = 0–30 S/m)
- Automatically locates the resonance and computes reflection modulation depth (MD)
- Generates journal-grade figures (300 DPI PNG + vector PDF)

## Key result
A gold H-shaped split-ring resonator absorber on Fe:Ga₂O₃ (with ground plane) reaches 77.5%
reflection-amplitude modulation at 300.4 GHz, which is 95.0% in reflected power and 82.2% in
absorption. Absorption flattens near σ ≈ 15 S/m.

![Modulation depth](MD_vs_sigma.png)

## Stack
Python · pandas · matplotlib · Ansys HFSS

## How to run
1. Open `metasurface_md_analysis.ipynb` in Google Colab or Jupyter
2. Upload your HFSS reflection export (CSV: σ, frequency, reflection magnitude)
3. Run all cells — figures save automatically as PNG + PDF

## Context
Reconfigurable THz metasurfaces are candidate building blocks for 6G wireless,
imaging, and sensing. This tool quantifies how device modulation scales with
photo-induced conductivity.
