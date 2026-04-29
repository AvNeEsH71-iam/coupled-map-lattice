# Coupled Map Lattice Coursework Project

This project implements a complete study of a coupled map lattice (CML) with local dynamics

\[
x_{n+1} = x_n^2 \exp(r-x_n), \quad r\in[1,3], \; x>0.
\]

## Folder Structure

```
coupled-map-lattice/
|-- code/
|   |-- map_model.py
|   |-- cml.py
|   |-- analysis.py
|   |-- plotting.py
|   |-- main.py
|   `-- compile_report.py
|-- data/
|-- plots/
|-- figures/
|-- report/
|   |-- report.tex
|   `-- figures/
|-- requirements.txt
`-- README.md
```

## What Is Included

1. Single map dynamics and parameter exploration for `r in [1,3]`.
2. Bifurcation diagram with raw CSV (`data/bifurcation_data.csv`) and PNG (`plots/bifurcation_diagram.png`).
3. Chaos diagnostics: phase-space and Lyapunov exponent scan.
4. Fixed-point stability analysis based on multipliers.
5. CML simulation on ring topology with diffusive coupling and tunable `epsilon`.
6. Synchronization study with regimes: no sync, partial sync, full sync.
7. Spatiotemporal visualizations and heatmaps.
8. Advanced explorations:
   - Topology comparison (ring/small-world/random)
   - Cluster synchronization profile
   - Finite-size effect with varying `N`

## Setup

From the repo root:

```powershell
pip install -r requirements.txt
```

## Reproduce All Results

```powershell
python code/main.py
```

This generates:

- CSV data in `data/`
- High-resolution plots in `plots/`
- Copied report figures in `report/figures/`
- Additional figure copies in `figures/`

## Compile the Report

Option 1 (Python helper):

```powershell
python code/compile_report.py
```

Option 2 (manual):

```powershell
cd report
pdflatex -interaction=nonstopmode report.tex
pdflatex -interaction=nonstopmode report.tex
```

## Notes

- All scripts are modular and documented.
- `code/main.py` is the main entry point for complete reproducibility.
- Generated outputs are submission-ready.
