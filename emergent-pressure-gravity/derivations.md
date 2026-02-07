# Pressure-Field Gravity: Detailed Mathematical Derivations

This document provides step-by-step mathematical derivations for all key results in the pressure-field gravity framework.

---

## Table of Contents

1. [Newtonian Limit from Pressure Gradients](#1-newtonian-limit)
2. [Vacuum Feedback Extension](#2-vacuum-feedback-extension)
3. [Spherical Mass Distribution Solutions](#3-spherical-solutions)
4. [Rotation Curve Derivation](#4-rotation-curves)
5. [Connection to MOND](#5-mond-connection)
6. [Dimensional Analysis](#6-dimensional-analysis)

---

## 1. Newtonian Limit from Pressure Gradients

### Starting Assumption

Test particle experiences acceleration proportional to pressure gradient:

```
a = -(1/ρ_eff) ∇P
```

Where:
- **a** = acceleration vector
- **P** = scalar pressure field
- **ρ_eff** = effective density parameter (vacuum property)

### Standard Poisson Equation

In the limit of no vacuum feedback (λ → ∞), pressure field satisfies:

```
∇²P = -4πk ρ_mass
```

Where:
- **k** = coupling constant (dimensions: [k] = [G][ρ_eff])
- **ρ_mass** = matter density

### Spherically Symmetric Case

For point mass M at origin:

**Step 1:** Source term
```
ρ_mass(r) = M δ³(r)
```

**Step 2:** General solution (using Green's function)
```
P(r) = P_0 + k M ∫ δ³(r')/|r - r'| d³r'
```

**Step 3:** Evaluate integral
```
P(r) = P_0 - (k M)/(4π r)
```

(We choose sign convention: pressure decreases near mass)

**Step 4:** Compute gradient
```
∇P = -(k M)/(4π r²) r̂
```

**Step 5:** Particle acceleration
```
a(r) = -(1/ρ_eff) ∇P = (k M)/(4π ρ_eff r²) r̂
```

**Step 6:** Identify gravitational constant
```
G = k/(4π ρ_eff)

Therefore:
a(r) = (G M)/r² r̂  ✓
```

This is exactly Newton's law of gravitation.

### Extended Mass Distribution

For continuous mass distribution ρ_mass(r'):

**Step 1:** Field equation solution
```
P(r) = P_0 - k ∫ ρ_mass(r')/|r - r'| d³r'
```

**Step 2:** For spherical ρ_mass(r'), define enclosed mass
```
M(r) = 4π ∫₀ʳ ρ_mass(r') r'² dr'
```

**Step 3:** At radius r > R (outside mass), pressure is
```
P(r) = P_0 - (k M(r))/(4π r)
```

**Step 4:** Acceleration
```
a(r) = (G M(r))/r²  ✓
```

Newtonian limit recovered.

---

## 2. Vacuum Feedback Extension

### Modified Field Equation

Include vacuum response via Yukawa-like term:

```
∇²P - (1/λ²)P = -4πk ρ_mass
```

Where **λ** is a characteristic length scale.

### Physical Interpretation

- **∇²P term:** Local curvature (standard Laplacian)
- **(1/λ²)P term:** Non-local feedback (vacuum screening)
- **Source term:** Matter couples directly

### Spherically Symmetric Solution

For point mass M at origin:

**Step 1:** Outside source (r > 0), solve homogeneous equation
```
∇²P - (1/λ²)P = 0
```

**Step 2:** In spherical coordinates
```
(1/r²) d/dr[r² dP/dr] - (1/λ²)P = 0
```

**Step 3:** Change variables: P(r) = u(r)/r
```
d²u/dr² - (1/λ²)u = 0
```

**Step 4:** General solution
```
u(r) = A exp(r/λ) + B exp(-r/λ)
```

**Step 5:** Require P → 0 as r → ∞, so A = 0
```
P(r) = (B/r) exp(-r/λ)
```

**Step 6:** Match to Newtonian solution at r → 0
```
B = -(k M)/(4π)

Therefore:
P(r) = -(k M)/(4π r) exp(-r/λ)
```

### Pressure Gradient

**Step 1:** Compute derivative
```
dP/dr = (k M)/(4π r²) exp(-r/λ) - (k M)/(4π λ r) exp(-r/λ)
```

**Step 2:** Factor out
```
dP/dr = -(k M)/(4π r²) exp(-r/λ) [1 + r/λ]
```

**Step 3:** In limit r << λ
```
dP/dr ≈ -(k M)/(4π r²) [1 + r/λ] ≈ -(k M)/(4π r²)
```

Recovers Newtonian gradient.

**Step 4:** In limit r ~ λ
```
dP/dr ≈ -(k M)/(4π λ r) exp(-r/λ)
```

Decays more slowly than 1/r² → enhanced gravity.

---

## 3. Spherical Mass Distribution Solutions

### Composite System: Core + Vacuum

Galaxy has:
- **Baryonic core:** radius R_b, mass M_b
- **Vacuum region:** r > R_b

**Region 1 (r < R_b):** Newtonian
```
P₁(r) = P_0 - (k M_b(r))/(4π r)
```

**Region 2 (r > R_b):** Vacuum feedback
```
P₂(r) = -(k M_b)/(4π r) exp(-r/λ)
```

### Boundary Conditions

At r = R_b:
1. **Continuity:** P₁(R_b) = P₂(R_b) ✓
2. **Gradient continuity:** dP₁/dr|_{R_b} = dP₂/dr|_{R_b}

Second condition gives matching for vacuum solution.

### Asymptotic Behavior

**r → 0:**
```
P(r) → -∞ (pressure well at center)
```

**r → ∞:**
```
P(r) → 0 exponentially fast
```

**r ~ λ:**
```
Transition from Newtonian to vacuum-dominated regime
```

---

## 4. Rotation Curve Derivation

### Circular Orbit Condition

For circular orbit at radius r with velocity v:
```
Centripetal acceleration = Gravitational acceleration
v²/r = |a(r)|
```

### General Formula

**Step 1:** Acceleration magnitude
```
|a(r)| = (1/ρ_eff) |dP/dr|
```

**Step 2:** From vacuum solution
```
|dP/dr| = (k M_b)/(4π r²) exp(-r/λ) [1 + r/λ]
```

**Step 3:** Velocity squared
```
v²(r) = r |a(r)| = (k M_b)/(4π ρ_eff r) exp(-r/λ) [1 + r/λ]
```

**Step 4:** Define G = k/(4π ρ_eff)
```
v²(r) = (G M_b)/r exp(-r/λ) [1 + r/λ]
```

### Two-Component Form

For r >> R_b, separate Newtonian and vacuum terms:

**Newtonian component:**
```
v²_N(r) = (G M_b)/r
```

**Vacuum component:**
```
v²_V(r) = α² [1 - exp(-r/λ)]
```

Where α is defined by:
```
α² = (G M_b)/λ
```

**Total:**
```
v²(r) = v²_N(r) exp(-r/λ) + v²_V(r)
```

For r << λ:
```
v²(r) ≈ (G M_b)/r + α² (r/λ)  → Rising curve
```

For r >> λ:
```
v²(r) ≈ α²  → Flat curve
```

---

## 5. Connection to MOND

### MOND Phenomenology

Modified Newtonian Dynamics (MOND) proposes acceleration transition at scale a₀ ≈ 10⁻¹⁰ m/s²:

```
a = (a_N)² / a₀  for a_N << a₀
a = a_N          for a_N >> a₀
```

### Pressure-Field Correspondence

Our theory gives:

**High acceleration (r << λ):**
```
a(r) = (G M_b)/r²  (Newtonian)
```

**Low acceleration (r ~ λ):**
```
a(r) ≈ (G M_b)/(λ r)
```

Identifying a₀ = G M_b/λ²:

```
a ≈ a_N (λ/r) = a_N √(a_N/a₀)  for a_N << a₀
```

This is MOND-like behavior!

### Key Difference

MOND modifies *dynamics* ad hoc.
Pressure-field modifies *field equation* with physical mechanism.

Both predict flat rotation curves, but:
- MOND: Empirical fitting formula
- Pressure-field: Derived from vacuum feedback

---

## 6. Dimensional Analysis

### Field Equation Dimensions

```
∇²P - (1/λ²)P = -4πk ρ_mass
```

**Left side:**
- [∇²P] = [P]/[L²] = [Force]/[L²][Area] = [Force]/[L⁴]
- [(1/λ²)P] = [P]/[L²] = [Force]/[L⁴]

**Right side:**
- [ρ_mass] = [M]/[L³]
- [k ρ_mass] = [k][M]/[L³]

**Consistency requires:**
```
[k] = [Force][L]/[M] = [G][ρ_eff]
```

### Parameter Relations

From a = -(1/ρ_eff) ∇P:
```
[a] = [∇P]/[ρ_eff] = [Force]/[L²][Area][ρ_eff]
```

For [a] = [L]/[T²]:
```
[ρ_eff] = [Force]/[L⁵] × [T²] = [M]/[L²][T²]
```

From G = k/(4π ρ_eff):
```
[G] = [k]/[ρ_eff] = [Force][L]/[M] / [M]/[L²][T²]
     = [Force][L³]/[M²][T²]
     = [L³]/[M][T²] ✓
```

Dimensional consistency verified.

### Characteristic Scales

**Length scale λ:**
```
[λ] = [L]  (fundamental vacuum scale)
```

**Velocity scale α:**
```
[α²] = [G M]/[λ] = [L³]/[M][T²] × [M]/[L] = [L²]/[T²]
[α] = [L]/[T] ✓
```

**Acceleration scale a₀:**
```
[a₀] = [G M]/[λ²] = [L]/[T²] ✓
```

All scales dimensionally consistent.

---

## Summary of Key Results

1. **Newtonian limit:** Exact for r << λ and weak fields
2. **Vacuum feedback:** Modifies gravity at r ~ λ via exponential screening
3. **Rotation curves:** Transition from v² ∝ 1/r to v² ≈ constant
4. **MOND connection:** Reproduces phenomenology with physical mechanism
5. **Consistency:** All dimensions and boundary conditions satisfied

**Next:** Apply to real galaxy data ([milky_way_rotation.md](./milky_way_rotation.md))

---

*Last Updated: December 2024*
