---
title: "Machine Learning Force Fields for Defective WSe2"
draft: false
cover:
  alt: "WSe2 defect & MLFF"
  caption: "Machine Learning Force Fields for Defective WSe2"
showBreadCrumbs: false
ShowReadingTime: false
hideMeta: true
disableAnchoredHeadings: true
---

### Equivariant Graph Neural Networks applied to Defective WSe2

---

Designed and validated a scalable AI framework to accelerate first-principles simulations of defective quantum materials.
I demonstrates how equivariant graph neural networks can replace expensive DFT simulations while preserving physical fidelity.

---

<div style="text-align: center;">

Download the thesis as PDF [here](/files/thesis.pdf)

</div>

---

## Summary

- Designed a reproducible workflow from raw simulation data to physics-based insights
- Trained an **equivariant graph neural network** to replace computationally expensive DFT simulations for defective 2D semiconductors
- Achieved **near-DFT accuracy** for energies, forces, and phonon properties
- Identified and quantified **localized defect signatures** around vacancies
- Demonstrated model robustness and transferability across larger supercells

---

## Abstract

Single-photon emitters in two-dimensional semiconductors, such as tungsten diselenide, have emerged as promising candidates for quantum photonic applications. The microscopic origin of this effect is connected to the interplay between local strain modulations and point defects, which result in defect states within the band gap localized at the defect site, resulting in strongly localized so-called Frenkel excitons . In this thesis, the formation and characteristics of such single-photon emitters are studied using state-of-the-art machine learning force fields. In particular, the equivariant graph neural network MACE is trained on a defective structure produced by DFT calculations. This model is capable of learning interatomic interactions while preserving key symmetries, such as rotational equivariance. The MACE model is applied on strained defect configurations with the aim to capture the formation of intervalley defect excitons proposed as the microscopic origin of single emitted photons. The presented methods provide a fast and scalable way to investigate quantum phenomena caused by defects in two-dimensional materials.

---

## PDF

<div style="position:relative; padding-top:130%;">
  <iframe
    src="/files/thesis.pdf#zoom=90&navpanes=0&toolbar=0&scrollbar=0"
    style="position:absolute; top:0; left:0; width:100%; height:100%; border:none;">
  </iframe>
</div>

---

## Research Context

Defects in two-dimensional semiconductors have emerged as a key ingredient for realizing quantum emitters at the nanoscale. In particular, monolayer tungsten diselenide (WSe₂) has attracted significant attention due to its direct band gap, strong spin–orbit coupling, and valley-selective optical transitions. Experimental and theoretical studies suggest that single-photon emission in WSe₂ originates from the interplay between atomic-scale defects and local strain fields, which give rise to strongly localized excitonic states.

From a theoretical perspective, modeling such defect-induced phenomena poses a major challenge. While density functional theory (DFT) provides accurate insight into structural and vibrational properties, its computational cost severely limits system size and the systematic exploration of defective configurations. This becomes particularly restrictive when studying phonon-related effects in large supercells, which are essential to disentangle genuine defect signatures from finite-size artifacts.

Machine learning force fields (MLFFs) offer a promising route to overcome these limitations by approximating interatomic interactions with near-DFT accuracy at a fraction of the computational cost. Among these approaches, equivariant graph neural networks such as MACE have recently demonstrated exceptional performance by explicitly respecting fundamental physical symmetries. This thesis explores the applicability of such equivariant MLFFs to defective WSe₂ and investigates whether they can reliably capture defect-induced vibrational phenomena relevant for single-photon emission.

---

## Main Contributions

This thesis presents a systematic study of defect-induced phonon properties in monolayer WSe₂ using an equivariant machine learning force field. The main contributions can be summarized as follows:

- Training and validation of an equivariant MACE-based force field on DFT reference data for defective WSe₂ structures

- Application of the trained model to compute phonon dispersion relations, phonon density of states (DOS), and projected DOS (PDOS)

- Identification and analysis of defect-induced localized vibrational modes associated with a single selenium vacancy

- Comparative investigation across multiple supercell sizes to assess localization behavior and exclude finite-size effects

- Demonstration of a physically consistent and transferable MLFF-based workflow for vibrational analysis in two-dimensional materials

---

## Results Overview

The trained MACE model accurately reproduces key vibrational properties of pristine monolayer WSe₂, including the phonon dispersion relation and the characteristic separation of tungsten- and selenium-dominated modes. This agreement with expected physical behavior provides confidence in the model’s ability to generalize beyond the training data.

For defective configurations containing a single selenium vacancy, the phonon spectra reveal additional features not present in the pristine system. In particular, flat bands at optical frequencies and pronounced peaks in the projected phonon density of states indicate the emergence of localized vibrational modes. A local projection analysis confirms that these modes are spatially confined to atoms in the immediate vicinity of the defect.

By systematically increasing the supercell size, it is shown that these localized modes persist while their influence on the global phonon spectrum diminishes. This behavior confirms that the observed features are intrinsic to the defect itself rather than artifacts of finite system size. Overall, the results demonstrate that equivariant MLFFs are capable of capturing subtle, defect-induced vibrational effects in low-dimensional materials.

---

## Limitations & Outlook

Despite the encouraging results, several limitations must be acknowledged. As a machine learning force field, the MACE model provides access to structural and vibrational properties but does not directly describe electronic quantities such as band gaps or exciton binding energies. Consequently, conclusions regarding single-photon emission remain indirect and are based on vibrational signatures rather than explicit optical calculations.

Furthermore, the accuracy of the MLFF is inherently limited by the quality and diversity of the underlying DFT training data. Long-range interactions beyond the chosen cutoff radius are not explicitly captured, which may become relevant in more complex or weakly bonded systems.

Future work could extend the presented approach by incorporating a broader range of defect types, strain configurations, and larger supercells. Combining MLFF-based vibrational analysis with electronic structure or excitonic models would provide a more comprehensive picture of defect-bound excitons and their role in single-photon emission. In this context, the present thesis serves as a foundation for further investigations at the intersection of machine learning and quantum materials research.

---

## Citation
```bibtex
@thesis{kindl2025mlff_wse2,
  title={Machine Learning Force Fields for Defective WSe2},
  author={Kindl, Sebastian},
  school={TU Wien},
  year={2025},
  type={Bachelor's Thesis}
}
