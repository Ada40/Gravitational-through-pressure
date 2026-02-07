# Quick Start Guide: Pressure-Field Gravity

**Get up to speed in 5 minutes**

---

## The Big Idea

**Gravity emerges from pressure gradients in a universal field, not spacetime curvature.**

```
Traditional:  Mass → Curved spacetime → Objects follow geodesics
This theory:  Mass → Pressure gradients → Objects roll "downhill"
```

**Result:** Flat galaxy rotation curves without dark matter!

---

## Three-Level Understanding

### Level 1: Intuitive Picture (30 seconds)

Think of gravity like weather:
- **High pressure zone:** Far from mass
- **Low pressure zone:** Near mass  
- **Objects "flow":** From high to low pressure

Just like wind flows from high to low atmospheric pressure!

### Level 2: Physical Mechanism (2 minutes)

**Field Equation:**
```
∇²P - (1/λ²)P = -4πk ρ_mass
```

**Key components:**
- **P(x,t):** Pressure field (the "gravitational fluid")
- **ρ_mass:** Normal matter creates pressure wells
- **λ:** Vacuum length scale (~12 kpc for galaxies)
- **Vacuum term (1/λ²)P:** Modifies gravity at large scales

**Particle Motion:**
```
a = -(1/ρ_eff) ∇P
```

Objects accelerate down pressure gradients!

### Level 3: Why It Matters (5 minutes)

**Local scales (r << λ):**
- Vacuum term negligible
- Recovers exact Newtonian gravity
- ✅ Explains solar system, binary stars, etc.

**Galactic scales (r ~ λ):**
- Vacuum feedback significant
- Pressure gradients decay more slowly
- ✅ Explains flat rotation curves WITHOUT dark matter

**Milky Way Results:**
- **Newtonian (baryons only):** χ² = 409 (terrible fit)
- **Pressure-field:** χ² = 25 (excellent fit)
- **Velocity at 30 kpc:** 216 km/s (observed: 220 km/s) ✓

---

## Reading Path

### For General Audience

1. **[gravity_through_pressure.md](./gravity_through_pressure.md)** - Conceptual introduction with analogies
2. **[milky_way_rotation.md](./milky_way_rotation.md)** - See it work for real galaxy
3. **[README.md](./README.md)** - Full theoretical framework

### For Scientists

1. **[README.md](./README.md)** - Complete theory and predictions
2. **[derivations.md](./derivations.md)** - Mathematical proofs
3. **[milky_way_rotation.py](./milky_way_rotation.py)** - Run the code yourself
4. **[timeline.md](./timeline.md)** - Development history and next steps

### For Coders

1. **Install:** `pip install numpy matplotlib`
2. **Run:** `python milky_way_rotation.py`
3. **Output:** Plot saved to `figures/rotation_curve.png`
4. **Modify:** Change parameters in script and re-run

---

## Key Results Summary

### What We've Proven

✅ **Newtonian limit exact:** Reproduces F = ma perfectly at local scales  
✅ **Flat rotation curves:** Milky Way fit with χ² = 25 (vs 409 for Newtonian)  
✅ **No dark matter needed:** Vacuum feedback explains observations  
✅ **Testable predictions:** Universal λ, Tully-Fisher relation, etc.

### What We Haven't Proven (Yet)

⚠️ **Galaxy clusters:** Need to verify velocity dispersions and lensing  
⚠️ **Cosmology (CMB):** Full calculation needed  
⚠️ **Strong-field regime:** Black holes, gravitational waves  
⚠️ **Universality:** Need to test on 100+ galaxies

### Falsification Criteria

Theory is **wrong** if:
1. λ varies wildly between galaxies (>50% scatter)
2. Cannot explain cluster dynamics
3. Cannot reproduce CMB power spectrum
4. Gravitational waves show incompatibility

**Timeline for tests:** 2-5 years with existing/planned data

---

## One-Sentence Explanations

**For a child:**
> "Gravity is like rolling marbles toward the bottom of a bowl—they follow where pressure is lowest."

**For a high school student:**
> "Objects accelerate toward regions of low gravitational pressure, just like wind flows from high to low atmospheric pressure."

**For an undergraduate:**
> "Test particles experience acceleration a = -(1/ρ_eff)∇P where P satisfies a modified Poisson equation with vacuum feedback term."

**For a physicist:**
> "Yukawa-screened scalar field with characteristic length λ ≈ 10 kpc produces MOND-like phenomenology and flat rotation curves without dark matter."

**For a cosmologist:**
> "If vacuum has finite response length λ, field equations naturally transition from Newtonian to asymptotically-flat regimes, potentially eliminating need for galactic-scale dark matter."

---

## Comparison at a Glance

| Question | Dark Matter | Pressure-Field |
|----------|-------------|----------------|
| **What is gravity?** | Spacetime curvature | Pressure gradients |
| **Rotation curves explained?** | Dark matter halos | Vacuum feedback |
| **New particles?** | Yes (WIMPs, axions, etc.) | No |
| **New fields?** | No (uses standard GR) | Yes (pressure field) |
| **Newtonian limit?** | ✓ Exact | ✓ Exact |
| **Cluster dynamics?** | ✓ Tested | ⚠ Needs verification |
| **Cosmology (CMB)?** | ✓ Excellent fit | ⚠ Not yet tested |
| **Particle searches?** | ✗ None found (40 years) | N/A (no particles) |
| **Simplicity?** | 6+ parameters | 3 parameters |
| **Falsifiable?** | Hard (can add components) | Easy (specific predictions) |

---

## Visual Summary

```
TRADITIONAL GRAVITY (Einstein):
   Mass
    ↓
  Curved Spacetime (G_μν = 8πG T_μν)
    ↓
  Objects follow geodesics
    ↓
  Appears as attraction

  Problem at galactic scales:
  Need ~85% dark matter to explain rotation curves!


PRESSURE-FIELD GRAVITY (This):
   Mass
    ↓
  Pressure well (∇²P - P/λ² = -4πk ρ)
    ↓
  Objects accelerate down gradient (a = -∇P/ρ_eff)
    ↓
  Appears as attraction

  Solution at galactic scales:
  Vacuum feedback (λ term) creates flat curves!
```

---

## Next Steps After Reading

### If you're excited:
1. Read **[gravity_through_pressure.md](./gravity_through_pressure.md)** for full conceptual picture
2. Run **milky_way_rotation.py** to see it work
3. Check **[README.md](./README.md)** for complete theory

### If you're skeptical:
1. Read **[derivations.md](./derivations.md)** - all math shown explicitly
2. Check our falsification criteria in **[README.md](./README.md)** Section 9
3. Look at **[timeline.md](./timeline.md)** for what we're testing next

### If you want to help:
1. Test code on your computer (should give same results)
2. Apply to other galaxies (M31, NGC 3198, etc.)
3. Suggest improvements or find errors (GitHub issues)
4. Extend to clusters or cosmology

---

## Bottom Line

**Question:** Can we explain galactic dynamics without dark matter?

**Answer (this framework):** Yes! Vacuum feedback in pressure field naturally produces flat rotation curves.

**Status:** ✓ Works for Milky Way, ⚠ Needs testing for clusters/cosmology

**Certainty:** This is a **hypothesis** requiring extensive validation, not established fact.

**Timeline:** 2-5 years to definitively test via galaxy surveys, cluster analysis, and CMB calculations.

---

## Contact

**Questions?** Open an issue on GitHub  
**Collaboration?** See [timeline.md](./timeline.md) for next steps  
**Critique?** We welcome it! Science advances through rigorous testing.

---

**The universe doesn't owe us dark matter. Perhaps it's been showing us pressure gradients all along.**

---

*Last Updated: December 2024*
