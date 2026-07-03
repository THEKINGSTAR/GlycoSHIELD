# GlycoSHIELD

<p align="center">

# 🧬 Modeling Protein Glycosylation Using Molecular Dynamics-Derived Glycan Libraries

**Eastern European Bioinformatics and Computational Genomics Workshop (EEBG 2026)**

[![Workshop](https://img.shields.io/badge/Workshop-EEBG_2026-blue.svg)](#)
[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](#)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](#)
[![Bioinformatics](https://img.shields.io/badge/Topic-Glycoproteomics-green.svg)](#)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](#)

</p>

---

## 📖 Overview

**GlycoSHIELD** is a computational framework for rapidly modeling **protein glycosylation** by grafting molecular dynamics-derived glycan conformers onto experimentally determined or computationally predicted protein structures.

This repository contains the customized hands-on tutorial prepared for the **Eastern European Bioinformatics and Computational Genomics Workshop (EEBG 2026)** running on the **Athena / Cyfronet HPC Infrastructure**.

The tutorial demonstrates an end-to-end workflow that starts from an AlphaFold protein structure, automatically retrieves glycosylation sites from UniProt, builds GlycoSHIELD input files, grafts realistic glycan conformers, and analyzes glycan shielding across the protein surface.

---

# Why GlycoSHIELD?

Modern structure prediction methods such as **AlphaFold** have dramatically improved our ability to predict protein structures.

However, predicted protein structures generally **do not include post-translational modifications**, particularly glycans.

Protein glycosylation plays a critical role in:

- Protein folding
- Molecular recognition
- Cell signaling
- Immune evasion
- Antibody accessibility
- Protein stability
- Receptor interactions

Traditionally, modeling glycosylated proteins requires extensive Molecular Dynamics (MD) simulations that may consume thousands of CPU or GPU hours.

**GlycoSHIELD** dramatically reduces this computational cost by reusing previously simulated glycan conformer libraries and automatically selecting conformations compatible with the target protein.

---

# ✨ Features

- 🧬 Automatic AlphaFold structure retrieval
- 🔍 Automatic UniProt glycosylation annotation retrieval
- ⚙ Automatic GlycoSHIELD input generation
- 🌳 Molecular dynamics glycan conformer grafting
- 🚫 Steric clash detection and filtering
- 🧱 Optional membrane-aware conformer filtering
- 📊 Glycan occupancy analysis
- 📈 Glycan shielding analysis
- 🖥 Interactive 3D visualization using py3Dmol
- 📄 Publication-quality figures
- 📚 Complete notebook converted to Markdown documentation

---

# 🔄 Workflow

```text
              UniProt
                 │
                 ▼
 Retrieve Glycosylation Sites
                 │
                 ▼
     AlphaFold Protein Model
                 │
                 ▼
 Generate GlycoSHIELD Input
                 │
                 ▼
 Load Glycan MD Libraries
                 │
                 ▼
 Structural Superposition
                 │
                 ▼
 Steric Clash Detection
                 │
      Accepted Conformers
                 │
        ┌────────┴────────┐
        ▼                 ▼
 Shielding Analysis   Membrane Analysis
        │
        ▼
 Publication Figures
```

---

# 📂 Repository Structure

```text
.
├── README.md
├── Exercise.ipynb
├── requirements.txt
│
├── GlycoSHIELD_tut_fixed3/
│   └── GlycoSHIELD_tut_fixed3.md
│
├── figs/
│
├── output/
│
└── tmp_files/
```

---

# 📚 Documentation

The repository contains multiple forms of the workshop material.

| Document | Description |
|-----------|-------------|
| **README.md** | Project overview and quick start guide |
| **Exercise.ipynb** | Interactive Jupyter notebook |
| **GlycoSHIELD_tut_fixed3/GlycoSHIELD_tut_fixed3.md** | Complete notebook exported to Markdown with explanations, code, outputs, and figures |

---

# 📖 Complete Tutorial

The complete workshop tutorial is available as Markdown:

## ➜ **[GlycoSHIELD_tut_fixed3/GlycoSHIELD_tut_fixed3.md](./GlycoSHIELD_tut_fixed3/GlycoSHIELD_tut_fixed3.md)**

It contains:

- Complete notebook walkthrough
- Biological background
- AlphaFold integration
- UniProt integration
- GlycoSHIELD execution
- Glycan conformer grafting
- Interactive visualization
- Shielding analysis
- Occupancy calculations
- Figures
- Outputs
- Workshop-specific modifications

---

# 🚀 Quick Start

Clone the repository

```bash
git clone https://github.com/THEKINGSTAR/GlycoSHIELD.git
cd GlycoSHIELD
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch the notebook

```bash
jupyter notebook Exercise.ipynb
```

---

# 🧪 Tutorial Workflow

The notebook demonstrates a complete glycoprotein modeling pipeline.

## 1. Retrieve AlphaFold Structure

Automatically downloads an AlphaFold protein structure from the AlphaFold Protein Structure Database.

---

## 2. Retrieve UniProt Glycosylation Sites

Automatically retrieves experimentally annotated glycosylation sites.

---

## 3. Generate GlycoSHIELD Input

Creates all required GlycoSHIELD input files.

---

## 4. Graft Glycan Conformers

Aligns MD-derived glycan conformers to each glycosylation site.

---

## 5. Detect Steric Clashes

Automatically rejects impossible conformations.

---

## 6. Analyze Shielding

Calculates residue-specific shielding generated by glycan ensembles.

---

## 7. Compare Membrane and Non-membrane Models

Evaluate how membrane constraints affect glycan flexibility.

---

# 📊 Example Results

The notebook generates figures similar to the following.

## AlphaFold Structure Lookup

```
figs/alphafold_structure_lookup.png
```

---

## Glycan Conformer Acceptance

```
figs/glycan_conformer_acceptance.png
```

---

## Glycan Brush Visualization

```
figs/glycan_brush_visualization.png
```

---

## Glycan Shielding Profile

```
figs/glycan_shielding_profile.png
```

---

# 🧬 Scientific Background

GlycoSHIELD enables researchers to investigate glycoprotein structure without performing expensive molecular dynamics simulations for every new protein.

Instead of simulating glycans from scratch, GlycoSHIELD reuses previously sampled molecular dynamics conformers and grafts them onto static protein structures.

Accepted conformers are determined through structural alignment and steric clash detection, producing realistic glycan ensembles suitable for structural analysis.

This strategy provides an efficient approximation of glycan flexibility while dramatically reducing computational requirements.

Applications include:

- Structural Bioinformatics
- Computational Glycobiology
- Antibody Accessibility Analysis
- Vaccine Design
- Epitope Mapping
- Molecular Docking
- Surface Shielding Analysis
- Glycoproteomics

---

# 💻 Technologies

- Python
- Jupyter Notebook
- NumPy
- Matplotlib
- MDAnalysis
- py3Dmol
- ipywidgets
- AlphaFold Protein Structure Database
- UniProt
- GlycoSHIELD

---

# 🔧 Workshop Modifications

The original GlycoSHIELD tutorial was adapted for the Athena / Cyfronet environment.

Changes include:

- Updated library paths
- py3Dmol integration
- Removal of unsupported notebook widgets
- Improved compatibility with shared JupyterHub environments
- Updated plotting routines
- Additional explanatory notes
- Simplified execution workflow

---

# 📖 References

- Sikora M. *GlycoSHIELD: A computational framework for modeling glycan shields.*
- Jumper J. et al. *Highly Accurate Protein Structure Prediction with AlphaFold.* Nature (2021).
- Varadi M. et al. *AlphaFold Protein Structure Database.* Nucleic Acids Research (2022).
- The UniProt Consortium. *UniProt: the Universal Protein Knowledgebase.*

---

# 🙏 Acknowledgements

Prepared for the

**Eastern European Bioinformatics and Computational Genomics Workshop (EEBG 2026)**

using the

**Athena / Cyfronet High Performance Computing Infrastructure**.

Special thanks to the GlycoSHIELD developers and the workshop organizers for providing the tutorial materials and computational resources.

---

# 📜 License

This repository is intended for educational and research purposes.

Please refer to the repository's license for reuse and redistribution terms.

---

# ⭐ Citation

If you use this repository in your work, please cite the original **GlycoSHIELD**, **AlphaFold**, and **UniProt** publications.

---

## 📬 Questions

For questions regarding the workshop materials, please open an issue in this repository.

For implementation details and the complete hands-on tutorial, see:

➡️ **[`GlycoSHIELD_tut_fixed3/GlycoSHIELD_tut_fixed3.md`](./GlycoSHIELD_tut_fixed3/GlycoSHIELD_tut_fixed3.md)**

---

<p align="center">

**Happy Modeling! 🧬**

</p>