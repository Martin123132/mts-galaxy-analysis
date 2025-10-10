# Universal Gravitational Scaling Analysis
## From Planets to Superclusters: The α ∝ r^n Framework

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Active Development](https://img.shields.io/badge/Status-Active%20Development-brightgreen)]()

## Overview

This repository contains a comprehensive analysis of gravitational systems across all scales, revealing universal scaling relationships from planetary orbits to galaxy superclusters. The core discovery is that the relationship α = P/r follows a power law α ∝ r^n, where the exponent n encodes the mass distribution of the system.

**Key Universal Relation:**
```
α ∝ r^n  where  n = (1-m)/2  and  M(r) ∝ r^m
```

This single framework describes:
- Planetary systems (n = +0.500, m = 0.00)
- Binary stars (n = +0.500, m = 0.00)
- Galaxy clusters (n = +0.21, m = 0.79)
- Single galaxies (n = -0.533, m = 1.878)

**Span:** 10+ orders of magnitude in size, 15+ orders of magnitude in mass

---

## 🎯 Major Discovery: Simulation-Observation Discrepancy

**NEW:** Comparison with IllustrisTNG reveals fundamental structural differences between simulated and observed galaxies.

| Dataset | M(r) Exponent | Physical Interpretation |
|---------|--------------|------------------------|
| **SPARC (observed)** | m = 1.878 ± 0.084 | Disk-dominated, extended profiles |
| **TNG (simulated)** | m = 0.895 ± 0.106 | DM-dominated, concentrated profiles |
| **Difference** | Δm = 0.983 (11.7σ) | Factor of 2 structural mismatch |

**Implication:** State-of-the-art cosmological simulations produce galaxies approximately **twice as concentrated** as real galaxies, quantifying the long-standing cusp-core problem with a single parameter.

See: [Universal Gravitational Scaling Reveals Systematic Structure Differences Between IllustrisTNG and Observed Galaxies](./TNG_comparison.md)

---

## Table of Contents
- [Key Results](#key-results)
- [TNG vs SPARC Comparison](#tng-vs-sparc-comparison)
- [Repository Structure](#repository-structure)
- [Quick Start](#quick-start)
- [Complete Analysis Suite](#complete-analysis-suite)
- [Physical Interpretation](#physical-interpretation)
- [Data Sources](#data-sources)
- [Applications](#applications)
- [Future Work](#future-work)
- [How to Cite](#how-to-cite)

---

## Key Results

### 1. Planetary Systems
- **Exponent:** n = 0.500 ± 0.002
- **Systems analyzed:** Solar System, TRAPPIST-1, Kepler-90
- **Universality:** 100% within ±0.01 of n = 0.5
- **Interpretation:** Point-mass (Keplerian) dynamics

### 2. Binary Star Systems  
- **Exponent:** n = 0.500 (identical to planets)
- **Systems analyzed:** Alpha Centauri, Sirius, Procyon, 8 total
- **Finding:** NOT intermediate regime as hypothesized
- **Interpretation:** From orbital perspective, binary = point mass

### 3. Galaxy Clusters
- **Exponent:** n = +0.21 ± 0.05
- **Mass distribution:** M(r) ∝ r^0.79
- **Systems analyzed:** Coma, Virgo, Perseus, Fornax, 7 total
- **Finding:** TRUE intermediate regime between point mass and galaxies
- **Interpretation:** Collections of galaxies + diffuse dark matter

### 4. Single Galaxies (SPARC)
- **Exponent:** n = -0.533 ± 0.084  
- **Mass distribution:** M(r) ∝ r^1.878 ± 0.064
- **Systems analyzed:** 80+ galaxies from SPARC database
- **Universality:** 76% within ±0.10 of universal value
- **Interpretation:** Disk-dominated systems with rising rotation curves

### 5. Simulated Galaxies (TNG) ⚠️
- **Exponent:** n = +0.05 ± 0.11
- **Mass distribution:** M(r) ∝ r^0.895 ± 0.106
- **Systems analyzed:** 23 galaxies from IllustrisTNG-100
- **Discrepancy:** 11.7σ offset from observations
- **Interpretation:** DM-dominated systems with flat rotation curves

### 6. Mass-Velocity Scaling
- **Relation:** v_∞ = 43.9 × (M_baryon / 10⁹ M☉)^0.331 km/s
- **Exponent:** α = 0.331 ± 0.013
- **Sample:** 53 galaxies with published masses
- **Accuracy:** 13.2% mean error
- **Connection:** Links to Tully-Fisher relation (M ∝ v^3.02)

---

## TNG vs SPARC Comparison

### The Discrepancy

Analysis of IllustrisTNG simulations reveals systematic structural differences from observed galaxies:

```
SPARC (Real Galaxies):
  M(r) ∝ r^1.88  →  Rising rotation curves, disk-dominated
  
TNG (Simulated Galaxies):  
  M(r) ∝ r^0.90  →  Flat rotation curves, DM-dominated
  
Δm = 0.98 (11.7σ difference)
```

### Physical Meaning

**SPARC galaxies (m ≈ 1.88):**
- Baryonic disk contributes ~60-70% of enclosed mass
- Extended mass distributions  
- v(r) ∝ r^0.44 (rising rotation curves)
- Disk dominates gravitational potential

**TNG galaxies (m ≈ 0.90):**
- Dark matter dominates at all radii
- Concentrated mass distributions
- v(r) ≈ constant (flat rotation curves)
- Weak disk influence on potential

### Implications

This discrepancy quantifies the **cusp-core problem**:

1. **Insufficient feedback:** TNG's baryonic processes don't flatten inner halos enough
2. **Adiabatic contraction:** Baryon infall may over-concentrate dark matter
3. **Alternative physics needed:** SIDM, modified gravity, or different feedback
4. **Resolution effects:** Though complete absence of m > 1.1 suggests robust trend

**Bottom line:** State-of-the-art simulations still don't reproduce observed galaxy structure.

---

## Repository Structure

```
.
├── README.md                          # This file
├── TNG_comparison.md                  # Full TNG analysis paper
├── code/
│   ├── planetary_systems/
│   │   ├── planetary_analysis.js      # Solar System, exoplanets
│   │   └── binary_analysis.js         # Binary star systems
│   ├── galactic_systems/
│   │   ├── galaxy_analysis.js         # SPARC galaxies
│   │   ├── cluster_analysis.js        # Galaxy clusters
│   │   ├── outlier_analysis.js        # Outlier identification
│   │   └── tng_analysis.py           # IllustrisTNG comparison
│   └── complete_workflow.js           # Full analysis pipeline
├── data/
│   ├── sparc_galaxies.csv            # SPARC rotation curves
│   ├── planetary_systems.json        # Solar System + exoplanets
│   ├── binary_stars.json             # Binary orbital data
│   ├── galaxy_clusters.json          # Cluster profiles
│   └── tng_results.npz               # TNG analysis results
├── results/
│   ├── figures/                      # All plots
│   └── tables/                       # Statistical summaries
└── docs/
    ├── methodology.md                # Detailed methods
    ├── physical_interpretation.md    # Theory & interpretation
    └── tutorials/                    # How-to guides
```

---

## Quick Start

### Installation
```bash
git clone https://github.com/Martin123132/mts-galaxy-analysis.git
cd mts-galaxy-analysis
```

All JavaScript code requires **no dependencies**! Python code for TNG requires:
```bash
pip install numpy scipy matplotlib illustris_python
```

### Run Complete Analysis
```javascript
// Load the complete workflow
const { runCompleteAnalysis } = require('./code/complete_workflow.js');

// Run full pipeline
const results = runCompleteAnalysis();

// Results contain:
// - planetary: Planetary system analysis
// - galactic: Galaxy analysis  
// - clusters: Cluster analysis
// - outliers: Outlier identification
// - correlations: Statistical patterns
```

### Run TNG Comparison
```python
# Requires TNG data access
python code/galactic_systems/tng_analysis.py

# Outputs:
# - tng_m_results.npz: Raw exponents
# - tng_vs_sparc_comparison.png: Main figure
# - Statistical comparison
```

---

## Complete Analysis Suite

### 1. Planetary Systems Analysis

**Method:**
- Calculate α = P / (a × (1-e) × ε)
- Fit power law α ∝ a^n
- Verify Keplerian scaling

**Results:**

| System | N_planets | Exponent | R² | Deviation from 0.5 |
|--------|-----------|----------|----|--------------------|
| Solar System | 8 | 0.497 | 0.9986 | 0.003 |
| TRAPPIST-1 | 7 | 0.502 | 0.9998 | 0.002 |
| Kepler-90 | 8 | 0.501 | 0.9995 | 0.001 |

**Conclusion:** Perfect confirmation of Keplerian mechanics

### 2. Binary Star Analysis

**Hypothesis tested:** Are binaries intermediate between planets and galaxies?

**Result:** NO - binaries are point-mass systems
- n = 0.500 (identical to planets)
- From orbital perspective, binary separation << orbital radius
- M(r) = M₁ + M₂ = constant

**Systems analyzed:**
- Alpha Centauri AB (79.91 yr period)
- Sirius AB (50.09 yr)
- Procyon AB (40.82 yr)
- 61 Cygni AB (659 yr)
- Plus 4 additional systems

### 3. Galaxy Cluster Analysis

**Discovery:** Clusters ARE the true intermediate regime

**Method:**
- Use velocity dispersion: M(r) = 3σ²r/G
- Calculate α = 2π/v
- Fit power laws for M(r) and α(r)

**Results:**

| Cluster | M(r) exponent | α exponent | Total Mass (M☉) |
|---------|--------------|------------|----------------|
| Coma | 0.82 | +0.18 | 1.2×10¹⁵ |
| Virgo | 0.76 | +0.24 | 1.2×10¹⁵ |
| Perseus | 0.79 | +0.21 | 6.7×10¹⁴ |
| Fornax | 0.71 | +0.29 | 7×10¹³ |

**Mean:** M(r) ∝ r^0.79, α ∝ r^+0.21

**Interpretation:**
- More concentrated than single galaxies (m = 1.88)
- More extended than point masses (m = 0.00)
- Collections of galaxies + smooth dark matter distribution

### 4. Galaxy Systems Analysis (SPARC)

**Dataset:** 80 galaxies from SPARC (Lelli et al. 2016)

**Universal Finding:** M(r) ∝ r^1.878 ± 0.064

**Breakdown by mass:**

| Mass Range (10⁹ M☉) | N | Mean m | σ | Convergence |
|-------------------|---|--------|---|-------------|
| <1 (Ultra-dwarf) | 6 | 1.812 | 0.078 | Diverse |
| 1-5 (Dwarf) | 14 | 1.906 | 0.027 | Approaching |
| 5-20 (Small) | 5 | 1.911 | 0.022 | Universal |
| 20-80 (Medium) | 4 | 1.869 | 0.003 | Converged |
| 80-200 (Large) | 3 | 1.872 | 0.001 | Converged |
| >200 (Giant) | 1 | 1.875 | 0.000 | Converged |

**Threshold:** Convergence above 5×10⁹ M☉

### 5. Simulated Galaxies (IllustrisTNG)

**Dataset:** 23 galaxies from TNG-100 at z=0

**Systematic Finding:** M(r) ∝ r^0.895 ± 0.106

**Comparison:**

| Source | M(r) ∝ r^m | Interpretation | Sample |
|--------|-----------|----------------|--------|
| SPARC | 1.878 ± 0.084 | Disk-dominated | 80 observed |
| TNG | 0.895 ± 0.106 | DM-dominated | 23 simulated |
| Δm | 0.983 | **11.7σ** | Systematic |

**Critical findings:**
- Zero overlap between distributions
- No TNG galaxy within ±0.20 of SPARC mean
- Complete absence of disk-dominated profiles
- Quantifies cusp-core problem

### 6. Systematic Trends

**By Morphology:**

| Type | N | M(r) ∝ r^ | Interpretation |
|------|---|----------|----------------|
| Irregular | 16 | 1.880 | Halo-dominated |
| Magellanic | 2 | 1.854 | Transitional |
| Early Spiral (Sb) | 3 | 1.872 | Perfect equilibrium |
| Mid Spiral (Sc) | 7 | 1.884 | Standard |
| Late Spiral (Sd) | 5 | 1.898 | Disk-heavy |

**By Environment:**

| Environment | N | M(r) ∝ r^ | Processing |
|------------|---|----------|------------|
| Isolated | 13 | 1.858 | None |
| Group | 12 | 1.878 | Moderate |
| Cluster (Fornax) | 8 | 1.925 | Strong |

**Environmental gradient:** +0.067 from isolated to cluster

---

## Physical Interpretation

### The Universal Relation

From virial equilibrium: v² ∝ GM(r)/r

If M(r) ∝ r^m, then:
- v ∝ r^((m-1)/2)
- α = 2π/v ∝ r^(-(m-1)/2)

Therefore: **n = (1-m)/2**

### What Different Exponents Mean

| M(r) Scaling | n | v Behavior | System Type |
|--------------|---|------------|-------------|
| r^0 (point mass) | +0.50 | r^-0.5 (Keplerian) | Planets, binaries |
| r^0.79 (intermediate) | +0.21 | r^-0.21 (slight drop) | Clusters |
| r^0.90 (TNG) | +0.05 | constant (flat) | **Simulated galaxies** |
| r^1.0 (isothermal) | 0.00 | constant (flat) | Critical point |
| r^1.88 (SPARC) | -0.53 | r^+0.44 (rising) | **Observed galaxies** |
| r^2.0 (disk) | -0.67 | r^+0.5 (linear rise) | Pure disk |

**Sign change at m = 1.0:**
- Below: Concentrated systems, positive n
- Above: Extended systems, negative n

### NFW + Disk Composite Model (SPARC)

The galaxy value m = 1.878 arises from:
- **60-70% disk contribution:** M ∝ r^1.95
- **30-40% halo contribution:** M ∝ r^1.0 (inner NFW)
- **Weighted average:** M ∝ r^1.87

Standard parameters:
- Disk scale length: R_d ~ 3 kpc
- Halo scale radius: r_s ~ 10 kpc
- NFW concentration: c ~ 10-15

### Why TNG Differs

TNG's m ≈ 0.90 indicates:
- **Dark matter dominates** at all radii
- **Weak disk influence** on gravitational potential
- **Insufficient core formation** from baryonic feedback
- **Adiabatic contraction** may over-concentrate DM
- **Resolution or physics** limitations in simulations

---

## Complete Hierarchy

```
System Type          Scale           M(r) ∝ r^m    α ∝ r^n      σ_n
────────────────────────────────────────────────────────────────────
Planets/Binaries     0.01-30 AU      r^0.00        r^+0.500     0.002
Galaxy Clusters      0.5-3 Mpc       r^0.79        r^+0.21      0.05
TNG Galaxies        1-30 kpc        r^0.90        r^+0.05      0.11
SPARC Galaxies      1-30 kpc        r^1.878       r^-0.533     0.084
Superclusters*      100-200 Mpc     r^0.35        r^+0.38      ???
```
*Extrapolated, not directly measured

**Span:**
- Size: 10^-6 to 10^5 kpc (11 orders of magnitude)
- Mass: 10^-1 to 10^17 M☉ (18 orders of magnitude)

---

## Data Sources

### Planetary Systems
- Solar System: JPL Horizons ephemerides
- Exoplanets: NASA Exoplanet Archive
- Binary stars: Orbital catalogs, literature

### Galactic Systems
- **SPARC database:** Lelli et al. 2016 (AJ, 152, 157)
  - 80 galaxies with HI rotation curves
  - Spitzer 3.6μm photometry
  - Mass range: 0.4 to 310 × 10⁹ M☉

### Simulated Galaxies
- **IllustrisTNG:** Nelson et al. 2019
  - TNG-100 at z=0
  - Particle-level mass profiles
  - 23 galaxies analyzed

### Galaxy Clusters
- X-ray observations: Velocity dispersion
- Gravitational lensing: Mass profiles
- Literature: Coma, Virgo, Perseus, Fornax

---

## Applications

### 1. Simulation Validation
- **Benchmark:** Target m = 1.88 for realistic galaxies
- **Diagnostic:** Single parameter reveals structure
- **Testing:** Compare feedback models, DM physics

### 2. Galaxy Evolution Tracker
- Monitor convergence to m = 1.878
- Identify virialization threshold (~5×10⁹ M☉)
- Track maturation via decreasing scatter

### 3. Environment Diagnostics
- Higher m → more processed
- Identify cluster members via compaction
- Quantify environmental effects (+0.067)

### 4. Dark Matter Constraints
- m = 1.878 sets disk/halo ratio (~60:40)
- Universal value tests ΛCDM predictions
- Deviations probe DM physics

### 5. Mass Estimation
Given rotation curve:
1. Fit v(r) to get asymptotic velocity
2. Use v_∞ = 43.9 × M^0.331 to estimate mass
3. Or use M(r) exponent for structure

---

## Future Work

### Immediate Priorities
- ✅ Binary star systems (completed)
- ✅ Galaxy cluster analysis (completed)
- ✅ Outlier characterization (completed)
- ✅ **TNG comparison (completed)**
- ☐ TNG-50 higher resolution analysis
- ☐ FIRE/EAGLE simulation comparison
- ☐ Gas fraction quantification

### Medium-term (1-2 years)
- ☐ Alternative DM models (SIDM from AIDA-TNG)
- ☐ High-z rotation curves (evolution)
- ☐ Modified feedback prescriptions
- ☐ Complete Local Volume survey
- ☐ Globular cluster analysis

### Long-term (3-5 years)
- ☐ First-principles derivation of m = 1.878
- ☐ Modified gravity tests (MOND, f(R))
- ☐ BIG-SPARC analysis (~4000 galaxies)
- ☐ Supercluster measurements
- ☐ Proto planetary disk evolution

---

## How to Cite

If you use this work in your research:

```bibtex
@misc{ollett2025_universal_scaling,
  author = {Martin Ollett},
  title = {Universal Gravitational Scaling Analysis: From Planets to Superclusters},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/Martin123132/mts-galaxy-analysis}
}

@article{ollett2025_tng_comparison,
  author = {Martin Ollett},
  title = {Universal Gravitational Scaling Reveals Systematic Structure 
           Differences Between IllustrisTNG and Observed Galaxies},
  year = {2025},
  note = {In preparation}
}
```

**Original Data Sources:**

SPARC Database:
```bibtex
@article{Lelli2016,
  author = {Lelli, Federico and McGaugh, Stacy S. and Schombert, James M.},
  title = {SPARC: Mass Models for 175 Disk Galaxies},
  journal = {The Astronomical Journal},
  volume = {152},
  pages = {157},
  year = {2016}
}
```

IllustrisTNG:
```bibtex
@article{Nelson2019,
  author = {Nelson, Dylan and others},
  title = {The IllustrisTNG simulations: public data release},
  journal = {Computational Astrophysics and Cosmology},
  volume = {6},
  pages = {2},
  year = {2019}
}
```

---

## Contributing

Contributions welcome! Priority areas:

**Data:**
- Additional TNG analysis (TNG-50, TNG-300)
- FIRE/EAGLE simulations
- More galaxy clusters
- Supercluster measurements

**Analysis:**
- Alternative dark matter models
- Modified gravity predictions
- Bayesian statistics
- Machine learning applications

**Code:**
- Python optimization
- Unit tests
- Documentation
- Tutorials

To contribute: Fork → Branch → Changes → Pull Request

---

## FAQ

### What's the main discovery?
A single relation α ∝ r^n describes all gravitational systems, where n = (1-m)/2 encodes mass distribution M(r) ∝ r^m.

### Why is m = 1.878 for observed galaxies?
Composite structure: ~60-70% exponential disk (M ∝ r²) + ~30-40% NFW halo (M ∝ r) → m ≈ 1.88

### Why do simulations get m ≈ 0.90?
TNG galaxies are dark matter-dominated with insufficient core formation from feedback. Either:
1. Feedback too weak
2. Adiabatic contraction too strong
3. Alternative DM/gravity needed
4. Resolution limitations

### Are binary stars intermediate?
No - hypothesis disproven. Binaries show n = +0.500 identical to planets (point masses from orbital perspective).

### What about galaxy clusters?
Yes! Clusters ARE intermediate with n = +0.21, between point masses and extended galaxies.

### How accurate is mass prediction?
Using v_∞ = 43.9 × M^0.331: Mean error 13.2%, 64% within 15%, comparable to other methods.

### Connection to Tully-Fisher?
Our v ∝ M^0.331 implies M ∝ v^3.02, consistent with Baryonic TF (M ∝ v^3.5-4.0).

### Can simulations be fixed?
Target is clear: increase m from 0.90 to 1.88. Possible solutions:
- Stronger/burstier feedback
- Self-interacting dark matter
- Modified gravity
- Better resolution

---

## License

MIT License - see LICENSE file

Free for academic and commercial use with attribution.

---

## Contact

- **Issues:** Open GitHub issue for bugs/questions
- **Email:** ollett123123@outlook.com
- **Twitter:** @nodicephysics

---

## Summary

This work demonstrates a universal framework for understanding gravitational dynamics across all scales. The single relation n = (1-m)/2 connects orbital timescales to mass distributions, providing a diagnostic tool for structure, evolution, and dark matter.

**From Mercury to superclusters, one pattern emerges: α ∝ r^n**

**NEW:** Comparison with IllustrisTNG reveals that state-of-the-art simulations produce galaxies systematically more concentrated than observations, quantifying fundamental challenges in reproducing observed galaxy structure.

---

**Last updated:** October 2025  
**Status:** Planetary ✓ | Binaries ✓ | Clusters ✓ | Galaxies ✓ | **TNG ✓** | Outliers ✓
