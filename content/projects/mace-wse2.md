---
title: "AI-Based Framework for Scalable Defect Analysis in 2D Semiconductors"
date: 2025-10-12
description: "Developing accurate and efficient interatomic potentials for semiconductors using MACE."
summary: "Transforming computationally intensive problems into scalable solutions using AI"
cover:
    alt: "MACE Model Visualization"
    caption: "MACE Architecture applied to WSe2"
ShowBreadCrumbs: false
ShowReadingTime: false
ShowWordCount: false
ShowToc: false
ShowPostNavLinks: false
disableAnchoredHeadings: true
weight: 1
---

---

### The Challenge
Predicting the physical properties of materials like **Tungsten Diselenide (WSe2)** usually requires *Density Functional Theory (DFT)*. While highly accurate, DFT is computationally extremely expensive, limiting simulations to small systems and short timescales. Classical force fields, on the other hand, are fast but often fail to capture the complex quantum mechanical interactions of 2D materials.

{{< figure src="/projects/mace/phonon_bands_pdos.png" title="Establishing the Reference System" caption="Ground-truth phonon band structure and Density of States (DOS) for pristine WSe2. These vibrational properties serve as the physical reference used to validate the machine learning model" >}}

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


{{< figure src="/projects/mace/compare_12x12_band_pdos.png" title="Pristine vs Defective" caption="Comparison of phonon band structures and PDOS, demonstrating the emergence of localized vibrational modes and confirming the model's consistency with first-principles theory." >}}

{{< figure src="/projects/mace/local_pdos_overview.png" title="Radial Phonon DOS" caption="Radial Comparison between pristine and defective system, revealing how vibrational properties evolve with distance from the defect. This demonstrates the model's ability to capture localized physical interactions." >}}

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
