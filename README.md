
# Universal Gravitational Scaling in Motion–TimeSpace  
### A Complete MTS Analysis Pipeline for Galaxy Structure (2026)

This repository contains the full Motion–TimeSpace (MTS) gravitational analysis pipeline used to extract, test, and verify a universal mass–geometry relation from galaxies, clusters, simulated systems, and planetary regimes.

This version supersedes all earlier drafts: it includes the full **28-step convergence, curvature, scaling, BTFR, and geometric-closure tests**, as well as the updated **SPARC vs TNG structural comparison**.

MTS interprets gravity not as a modified force law, but as an emergent expression of **mass geometry**.  
A single quantity controls the entire phenomenon:

\[
M(r) \propto r^{m(r)}
\]

and therefore the gravitational field follows:

\[
g(r) \propto r^{\,m(r) - 2}.
\]

The exponent \(m(r)\) is **directly measurable** from rotation curves and becomes the universal structural observable across galaxies.

---

# 🌌 1. Overview

The analysis reveals a **consistent geometric trend** across 73 SPARC galaxies:

- The **outer mass–scaling exponent** continues to fall with radius.
- The **curvature of \(\ln v\) vs \(\ln r\)** is **negative at the edge in all 73 galaxies**.
- A global regression of outer segments predicts:

\[
m_{\infty} \approx 1.60 \qquad s_\infty \approx 0.30
\]

where \(s = d\ln v / d\ln r\).

This is the asymptotic geometric state of real disk galaxies.

Simulations (IllustrisTNG) do **not** reach this regime—they asymptote to \(m \approx 0.90\), meaning they remain dark-matter dominated structurally.

---

# 🧭 2. Key Results (Short Summary)

### ✔ **True geometric asymptote (from Step 14–18)**  
Across 321 outer radial segments:

\[
m_\infty = 1.5997 \pm 0.02
\]
\[
s_\infty = 0.2999 \pm 0.01
\]

### ✔ **Curvature is negative for all galaxies**  
\[
\frac{d^2(\ln v)}{d(\ln r)^2} < 0 \quad \text{for all 73 galaxies}
\]

Sign test: **73 negative, 0 positive** (p ≈ 2e-22).  
Implication: the rotation curve is still bending downward — not flat.

### ✔ **Outer slope drift**  
Median drift:

\[
\Delta m = -0.093 \pm 0.02
\]

Galaxies are not converged, but trending toward the same universal limit.

### ✔ **Mass–size relation**  
\[
R_{\max} \propto M^{0.3693}
\]

### ✔ **BTFR convergence radius**  
Best match between local BTFR and asymptotic Vinf occurs at:

\[
r \approx 0.90\, R_{\max}
\]

### ✔ **RAR analytic prediction test**  
MTS-derived RAR matches empirical RAR with R² > 0.99.

### ✔ **Simulation vs observation structural gap**  
SPARC outer exponent:

\[
m_\text{SPARC} = 1.60-1.88  \quad (\text{radius-dependent})
\]

TNG galaxies:

\[
m_\text{TNG} \approx 0.90
\]

Difference ≈ **0.7–1.0**, i.e. **factor-2 structural mismatch**.

---

# 📊 3. What This Repository Contains

### ✔ Full MTS Galaxy Pipeline  
All Colab-compatible code, broken into clear, independent notebooks:

- **01_load_data.ipynb**
- **02_compute_outer_slopes.ipynb**
- **03_curvature_test.ipynb**
- **04_mass_size_exponent.ipynb**
- **05_btfr_radius_scan.ipynb**
- **06_rar_prediction_test.ipynb**
- **07_global_convergence_regression.ipynb**

Everything prints results to screen — no hidden files.

### ✔ Data  
- Cleaned SPARC rotation curves  
- Derived MTS tables (outer slopes, curvature, R_norm bins, etc.)  
- Galaxy metadata (baryonic mass, scale lengths)

### ✔ Results  
- Regression curves  
- RAR comparison plots  
- Curvature distributions  
- BTFR radius-scan plots  
- SPARC vs TNG structural comparison

---

# 🧪 4. The 2026 MTS Results in Detail

## 4.1 Outer-Slope Scaling (Steps 5–10)

Using last K=4 points for each galaxy:

- Median slope at R_norm=1:  
  \[
  s = 0.370
  \]
- Corresponding mass exponent:  
  \[
  m = 1.740
  \]

Segment-by-segment regression to R_norm=1 gives:

\[
m_\infty = 1.60
\]

This is the correct asymptotic state.

---

## 4.2 Curvature Test (Steps 13–17)

Two independent curvature estimators:

1. **Segment-based curvature**
2. **Quadratic fit curvature**

Both yield:

\[
\text{curv} \approx -0.40
\]

Never positive in any galaxy.

Implication:  
**Rotation curves are still bending downward at the edge — not flattening.**

---

## 4.3 Stability vs RMAX_KEEP (Step 16)

m_inf computed by varying the outer cut:

| RMAX_KEEP | m_inf |
|-----------|--------|
| 0.80 | 1.563 |
| 0.85 | 1.584 |
| 0.90 | 1.584 |
| 0.92 | 1.583 |
| 0.94 | 1.574 |
| 0.95 | 1.600 |

Stable to ±0.02 across cuts.

---

## 4.4 Radius-90 Regime (Step 22)

m_R90K (K-nearest 4 points around R90):

\[
m_{R90} = 1.772 \pm 0.087
\]

At this radius:

- galaxies closest to geometric equilibrium  
- minimal scatter  
- cleanest BTFR prediction (but **not** the asymptotic value)

---

## 4.5 BTFR (Steps 23–24)

### Using V(0.9 Rmax):

\[
\alpha_{90} = 2.671,\quad R^2 = 0.931
\]

### Using Vinf:

\[
\alpha_{\infty} = 2.704,\quad R^2 = 0.939
\]

### Best-matching radius:

\[
r \approx 0.9 R_{\max}
\]

---

## 4.6 Mass–Size Scaling (Step 20)

\[
R_{\max} \propto M^{0.3693}
\]

This helps predict the BTFR and geometric closure.

---

## 4.7 Consistency Triangle (Step 25–27)

The relation between:

1. BTFR slope  
2. Mass–size scaling  
3. Geometric exponent m  

**Does not close** unless:

\[
m_{\infty} = 3.00
\]

Which is unphysical.  
Therefore the BTFR is **not** a primary law — it is a **projection** of the geometric scaling regime, consistent with MTS.

---

# 🛰 5. Physical Interpretation

### Gravity is geometric:

\[
g(r) \propto r^{m(r)-2}.
\]

- **Planets**: m = 0 → g ∝ r⁻²  
- **Clusters**: m ≈ 0.8 → intermediate  
- **Simulated galaxies**: m ≈ 0.9 → flat RC  
- **Real galaxies**: m → 1.6–1.9 → rising RC

The entire ladder of gravitational behavior follows a single exponent.

---

# 🆚 6. SPARC vs TNG Comparison (Updated)

### SPARC real galaxies:
\[
m \to 1.6 - 1.9
\]

### TNG simulated galaxies:
\[
m \approx 0.9
\]

Difference ≈ **0.7–1.0**, corresponding to:

- factor-2 difference in geometric structure  
- systematically more concentrated simulated galaxies  
- explains why TNG RCs flatten too early

---

# 📁 7. Repository Structure

Same directories as before, but updated with 2026 analysis scripts.

---

# 🚀 8. Quick Start

```bash
git clone https://github.com/Martin123132/mts-galaxy-analysis.git
cd mts-galaxy-analysis

Run the pipeline:

python3 step01_load_data.py
python3 step02_outer_slopes.py
...
python3 step28_triangle_closure.py

Or open the notebooks directly in Colab.

⸻

📚 9. How to Cite

@misc{ollett2026_mts_galaxy_scaling,
  author = {Martin Ollett},
  title = {Universal Gravitational Scaling in Motion--TimeSpace},
  year = {2026},
  publisher = {GitHub},
  url = {https://github.com/Martin123132/mts-galaxy-analysis}
}


⸻

🧩 10. Summary

This repository provides:
	•	the full MTS gravitational framework,
	•	a complete reproducible galaxy analysis,
	•	convergence, curvature, slope drift, and asymptotic predictions,
	•	and the first structurally quantitative comparison of real galaxies vs. simulations using a single geometric exponent.

What emerges is a simple principle:

Gravity = Mass Geometry.

m(r) is the universal observable.

From planets to galaxies, everything follows.

⸻

Last updated: February 2026

---

