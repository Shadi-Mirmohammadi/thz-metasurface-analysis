# THz Metasurface Modulator Analysis

Automated analysis pipeline for terahertz metasurface modulators based on
Fe:Ga₂O₃, processing HFSS simulation exports into publication-ready figures.

IRMMW-THz 2026 paper: *Optically Tunable Terahertz Metasurface Absorber Based on
Fe-Doped β-Ga₂O₃* (Salt Lake City, October 2026).

## What this does
- Loads HFSS Floquet-port reflection sweeps across 13 conductivity states (σ = 0–30 S/m)
- Automatically locates the resonance and computes reflection modulation depth (MD)
- Generates journal-grade figures (300 DPI PNG + vector PDF)

## Key result
A gold H-shaped split-ring resonator absorber on Fe:Ga₂O₃ (with ground plane) reaches 77.5%
reflection-amplitude modulation at 300.4 GHz between σ = 0 and 25 S/m, which is 95.0% in reflected power and 82.2% in
absorption. Absorption flattens near σ ≈ 15 S/m.

![Modulation depth](MD_vs_sigma.png)

## Stack
Python · pandas · matplotlib · Ansys HFSS

## How to run
1. Open `metasurface_md_analysis.ipynb` in Google Colab or Jupyter
2. Upload your HFSS reflection export (CSV columns: σ in S/m, frequency in GHz, |S11|)
   and set `CSV_FILE` in the first code cell
3. Run all cells; figures save as PNG + PDF

The HFSS export behind the figure above is not included in this repository.

## Context
Reconfigurable THz metasurfaces are candidate building blocks for 6G wireless,
imaging, and sensing. This tool quantifies how device modulation scales with
photo-induced conductivity.
