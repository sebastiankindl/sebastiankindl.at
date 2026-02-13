---
title: "Machine Learning Force Fields for WSe2"
date: 2025-10-12
description: "Developing accurate and efficient interatomic potentials for semiconductors using MACE."
summary: "Bridging the gap between ab-initio accuracy and classical simulation speed for 2D materials."
cover:
    alt: "MACE Model Visualization"
    caption: "MACE Architecture applied to WSe2"
ShowBreadCrumbs: false
ShowReadingTime: false
ShowWordCount: false
ShowToc: false
ShowPostNavLinks: false
weight: 1
---

---

### The Challenge
Predicting the physical properties of materials like **Tungsten Diselenide (WSe2)** usually requires *Density Functional Theory (DFT)*. While highly accurate, DFT is computationally extremely expensive, limiting simulations to small systems and short timescales. Classical force fields, on the other hand, are fast but often fail to capture the complex quantum mechanical interactions of 2D materials.

{{< figure src="/projects/mace/phonon_bands_pdos.png" title="Establishing the Baseline" caption="Ground-truth phonon band structure and Density of States (DOS) for pristine WSe2. These vibrational properties serve as the physical benchmark for our model training." >}}

---

### The Solution
In my bachelor thesis, I implemented and trained a **Machine Learning Force Field (MLFF)** based on the **MACE (Multi-Atomic Cluster Expansion)** architecture. 
- **Data Generation:** Curated a high-quality dataset of atomic configurations using ab-initio methods.
- **Model Training:** Utilized equivariant neural networks to map atomic environments to potential energy surfaces.
- **Validation:** Benchmarked the model against ground-truth DFT data to ensure high fidelity in force and energy predictions.

---

### Key Results
- **Efficiency:** Achieved a speedup of several orders of magnitude compared to traditional DFT.
- **Accuracy:** Maintained "ab-initio" level precision (low MAE in energy/forces), enabling large-scale Molecular Dynamics (MD) simulations.
- **Scalability:** Demonstrated that the model can generalize to larger supercells that were previously unreachable.
- **Scientific Insight:** Successfully modeled defect-induced changes in the material's vibrational spectrum, which is critical for semiconductor applications.


{{< figure src="/projects/mace/compare_12x12_band_pdos.png" title="Model Validation" caption="Comparison of phonon band structures and PDOS. The difference plot highlights the near-ab-initio accuracy of the MACE force field." >}}

{{< figure src="/projects/mace/local_pdos_overview.png" title="Model Validation" caption="Comparison of phonon band structures and PDOS. The difference plot highlights the near-ab-initio accuracy of the MACE force field." >}}

---

### Tech Stack
- **Languages:** Python
- **ML Frameworks:** PyTorch, MACE
- **Simulation Tools:** ASE, Phonopy
- **Science:** DFT, Solid State Physics, Phonon Analysis

---

<div style="text-align: center;">

{{< button href="https://github.com/sebastiankindl/thesis-mace-mlff-wse2" >}}View Code on GitHub{{< /button >}}

</div>

---