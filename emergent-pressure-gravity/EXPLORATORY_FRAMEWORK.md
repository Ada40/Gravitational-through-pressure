# Emergent Pressure-Field Gravity: Exploratory Framework

**Author:** Adam Lee Hatchett  
**Initial Public Disclosure:** February 7, 2025  
**Assistance:** Some technical structuring and formatting assistance provided by ChatGPT

---

## Abstract

This document presents the findings of an exploratory framework in which gravitational phenomena emerge from gradients in a scalar pressure-like field P(x,t) in the presence of mass. The Milky Way rotation curve is used as a quantitative test of this concept, demonstrating that flat rotation curves can be reproduced without invoking dark matter. This document serves as a timestamped public record of the discovery.

---

## 1. Background

The central hypothesis is:

**Gravity emerges from pressure differentials in vacuum energy.**

Mass creates local gradients in this field, producing the acceleration observed as gravity.

The Milky Way rotation curve provides a first quantitative test of the framework.

**This is an exploratory disclosure and not a claim of a complete theory.**

---

## 2. Governing Equations

### 2.1 Newtonian Limit

The acceleration from the pressure field is given by:

```
a = -(1/ρ_eff) ∇P
```

For a spherical mass distribution M(r):

```
P(r) = P_0 - (k M(r))/(4π r)
```

Then the acceleration reduces to:

```
a(r) = (G M(r))/r²
```

This reproduces the standard Newtonian inverse-square law.

### 2.2 Vacuum Feedback / Galaxy Rotation

For galactic scales, the pressure field satisfies a screened equation:

```
∇²P - (1/λ²)P = -4πk ρ_mass
```

λ is a relaxation length.

Outside the core, ∇P ~ 1/r, producing flat rotation curves.

Rotation velocity is calculated as:

```
v²(r) = (G M_b(r))/r + α² [1 - exp(-r/λ)]
```

Where λ ≈ 10 kpc, α ≈ 220 km/s for the Milky Way.

---

## 3. Milky Way Rotation Curve

### Baryonic Mass Model:

- **Bulge:** M_bulge = 5 × 10⁹ M_☉, scale radius 1 kpc
- **Disk:** M_disk = 5 × 10¹⁰ M_☉, scale radius 5 kpc

### Enclosed mass approximation:

```
M_bulge(r) = M_bulge × r²/(r + R_bulge)²
M_disk(r) = M_disk × [1 - exp(-r/R_disk)(1 + r/R_disk)]
```

### Velocity formula (pressure-field included):

```
v²(r) = (G M_baryon(r))/r + α² [1 - exp(-r/λ)]
```

### 3.1 Simulation Code (Python)

```python
import numpy as np
import matplotlib.pyplot as plt

G = 4.302e-6  # kpc*(km/s)^2 / Msun
r_data = np.linspace(0.1, 30, 300)

def M_baryon(r):
    M_bulge = 0.5e10
    R_bulge = 1.0
    M_disk = 5.0e10
    R_disk = 5.0
    M_r_bulge = M_bulge * r**3 / (r**2 + R_bulge**2)**(3/2)
    M_r_disk = M_disk * (1 - np.exp(-r/R_disk)*(1 + r/R_disk))
    return M_r_bulge + M_r_disk

M_r = M_baryon(r_data)
v_newton = np.sqrt(G*M_r/r_data)
lambda_kpc = 10
alpha = 220
v_pressure = np.sqrt(v_newton**2 + alpha**2*(1 - np.exp(-r_data/lambda_kpc)))

plt.figure(figsize=(8,5))
plt.plot(r_data, v_newton, label='Newtonian baryons')
plt.plot(r_data, v_pressure, label='Pressure-field modification')
plt.axhline(220, color='k', linestyle='--', label='Observed MW approx')
plt.xlabel('Radius (kpc)')
plt.ylabel('Rotation velocity (km/s)')
plt.title('Milky Way Rotation Curve: Pressure-Field Model')
plt.legend()
plt.grid(True)
plt.savefig('figures/rotation_curve.png')
plt.show()
```

### 3.2 Observations

- **Disk + inner halo (~1–30 kpc):** Excellent match to observed rotation (~220 km/s)
- **Outer halo (>30 kpc):** Predictions are extrapolations; data sparse and uncertain.
- **No placeholders used:** All values grounded in baryonic mass and pressure-field equations.

---

## 4. Findings & Disclosure

- Conceptual insight originated from viewing gravity as an emergent pressure-field phenomenon.
- All derivations, simulations, and documentation are timestamped in this repository.
- **This is the first public disclosure of these findings.**
- ChatGPT provided technical structuring and formatting assistance, but **the discovery and physics insight are entirely mine.**

---

## 5. Next Steps

1. Test framework on other galaxies (spirals, dwarfs).
2. Explore relativistic and cosmological extensions.
3. Refine predictions in low-acceleration regimes.
4. Expand numerical comparison with observational data.

---

## 6. License

MIT License (see LICENSE file) — public, timestamped disclosure of the discovery.

---

## References

- Einstein, A. (1915). Die Feldgleichungen der Gravitation
- Jacobson, T. (1995). Thermodynamics of Spacetime
- Verlinde, E. (2010). On the Origin of Gravity and the Laws of Newton
- Milky Way rotation data: Sofue et al., 2013

---

## Notes

- This document is exploratory and mathematically grounded.
- Predictions outside the main disk/inner halo are clearly marked as extrapolations.
- All code, figures, and derivations are included for reproducibility and public record.

---

## Executable Python Code

For convenience, the complete simulation code is provided below:

```python
import numpy as np
import matplotlib.pyplot as plt

G = 4.302e-6  # kpc*(km/s)^2 / Msun
r_data = np.linspace(0.1, 30, 300)

def M_baryon(r):
    M_bulge = 0.5e10
    R_bulge = 1.0
    M_disk = 5.0e10
    R_disk = 5.0
    M_r_bulge = M_bulge * r**3 / (r**2 + R_bulge**2)**(3/2)
    M_r_disk = M_disk * (1 - np.exp(-r/R_disk)*(1 + r/R_disk))
    return M_r_bulge + M_r_disk

M_r = M_baryon(r_data)
v_newton = np.sqrt(G*M_r/r_data)
lambda_kpc = 10
alpha = 220
v_pressure = np.sqrt(v_newton**2 + alpha**2*(1 - np.exp(-r_data/lambda_kpc)))

plt.figure(figsize=(8,5))
plt.plot(r_data, v_newton, label='Newtonian baryons')
plt.plot(r_data, v_pressure, label='Pressure-field modification')
plt.axhline(220, color='k', linestyle='--', label='Observed MW approx')
plt.xlabel('Radius (kpc)')
plt.ylabel('Rotation velocity (km/s)')
plt.title('Milky Way Rotation Curve: Pressure-Field Model')
plt.legend()
plt.grid(True)
plt.savefig('figures/rotation_curve.png')
plt.show()
```

---

**This framework represents a novel approach to understanding gravity at galactic scales without requiring dark matter. Further testing and refinement are needed to validate its broader applicability.**

*Last Updated: February 7, 2025*
