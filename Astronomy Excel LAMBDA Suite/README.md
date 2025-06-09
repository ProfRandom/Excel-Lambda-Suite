# 🔭 Astronomy LAMBDA Suite for Excel

This suite offers a rich collection of parameter-driven Excel LAMBDA functions tailored for astrophysical modeling, exoplanet metrics, orbital mechanics, and celestial classification. Built for dynamic array compatibility and composability, these tools support everything from habitability analysis to spectral classification and synodic calculations.

---

## 📘 Overview

Each function is self-contained and documented with parameters, expected outputs, return types, and usage examples. Designed for pedagogical, speculative, or modeling scenarios, these tools can be combined into custom spreadsheets for interactive exploration of astronomical concepts.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `ASTRO_HAB_INDEX` | Calculates a normalized habitability index from orbital distance. |
| `ASTRO_SPECTRAL_DISTRIBUTION` | Distributes stars across spectral types (O–M) based on abundance. |
| `ASTRO_CALC_TEMP` | Returns interpolated temperature (K) from a spectral subclass (e.g., G7.3). |
| `ASTRO_TYPE_FROM_TEMP` | Returns subclass from a temperature input (e.g., 5529 K → G7.3). |
| `ASTRO_DISPLAY_SPECTRAL` | Displays temperature/spans for O3–M9 classes; filtered or full. |
| `ASTRO_STAR_ATTRIBUTES` | Derives all key stellar parameters from one known value (K, M, etc.). |
| `ASTRO_HABITABLE_ZONES`, `NASTRO_HABITABLE_ZONES` | Returns zone bands (Z0–Z5) around stars by luminosity. |
| `ASTRO_STAR_DENSITY_VOLUME` | Computes stellar counts within a radius or volume. |
| `ASTRO_PLANET_METRICS`, `ASTRO_PLANET_METRICS_SAFETY` | Computes planetary M, R, d, g, v from any valid pair. |
| `ASTRO_SYNODIC_SOLVER`, `ASTRO_SYNODIC_PQ`, `ASTRO_SYNODIC_PS`, `ASTRO_SYNODIC_QS` | Solve for synodic or sidereal periods between orbiting bodies. |
| `ASTRO_APPARENT_SOLAR_SIZE` | Calculates angular diameter relative to solar norm. |
| `ASTRO_ORBIT_CONFIGURATION_INDEX` | Returns a configuration index of two-body orbital symmetry. |
| `ASTRO_ORBIT_SOLVER`, `ASTRO_ORBIT_AXIS`, `ASTRO_ORBIT_PERIOD`, `ASTRO_ORBIT_SUM_MASSES` | Keplerian two-body system solvers (mass, period, axis). |
| `ASTRO_SPHERICAL_TO_CARTESIAN`, `ASTRO_CARTESIAN_TO_SPHERICAL` | Converts between spherical and Cartesian coordinates. |
| `ASTRO_DEGREES_TO_DMS_NUM`, `ASTRO_DEGREES_TO_DMS_TEXT`, `ASTRO_DMS_NUM_TO_DEGREES`, `DEG_DEC_DMS`, `DEG_DMS`, `DEG_DMS_DEC` | Conversions between decimal degrees and sexagesimal formats. |

---

## 🧩 Highlights and Tips

- 🌎 **Habitability Modeling**: Use `ASTRO_HAB_INDEX` with `ASTRO_HABITABLE_ZONES` to evaluate planet positions dynamically.
- 🔥 **Stellar Profiles**: Derive mass, radius, luminosity, and lifetime using `ASTRO_STAR_ATTRIBUTES` from just temperature or mass.
- 🌀 **Orbital Mechanics**: Solve for any two-body orbital attribute (`axis`, `mass`, `period`) using intuitive wrappers or the unified solver.
- 🌈 **Spectral Tools**: Visualize or convert stellar classifications with `ASTRO_DISPLAY_SPECTRAL`, `ASTRO_CALC_TEMP`, and `ASTRO_TYPE_FROM_TEMP`.
- 🪐 **Planet Design**: Generate plausible planetary profiles using `ASTRO_PLANET_METRICS` from gravity/density, mass/radius, etc.
- ⏳ **Synodic Calculations**: Get conjunction intervals or estimate missing sidereal periods via `ASTRO_SYNODIC_SOLVER` or its wrappers.
- 🗺️ **Coordinate Conversion**: Spherical/Cartesian mapping is supported for 3D modeling or plotting simulations.
- 📏 **Angle Tools**: Seamless conversions between degrees and DMS for all observation-based workflows.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 📦 Optional pairing with `ASTROCON_` constants set (not included here).

---

## 📎 File Contents

- `astro_lambda_listing.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
