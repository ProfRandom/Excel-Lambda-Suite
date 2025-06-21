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
| `ASTRO_HABITABLE_ZONES` | Returns habitable zone bands (Z0–Z5) based on stellar luminosity. |
| `NASTRO_HABITABLE_ZONES` | Alternate wrapper for habitable zone calculation. |
| `ASTRO_SPECTRAL_DISTRIBUTION` | Distributes stars across spectral types (O–M) based on abundance. |
| `ASTRO_CALC_TEMP` | Returns interpolated temperature (K) from a spectral subclass (e.g., G7.3). |
| `ASTRO_TYPE_FROM_TEMP` | Returns subclass from a temperature input (e.g., 5529 K → G7.3). |
| `ASTRO_DISPLAY_SPECTRAL` | Displays temperature/spans for O3–M9 classes; filtered or full. |
| `ASTRO_STAR_ATTRIBUTES` | Derives stellar parameters (mass, radius, luminosity, lifetime) from any key input. |
| `ASTRO_STAR_DENSITY_VOLUME` | Computes stellar counts within a radius or volume. |
| `ASTRO_PLANET_METRICS` | Calculates planetary mass, radius, density, gravity, velocity from any valid input pair. |
| `ASTRO_PLANET_METRICS_SAFETY` | Error-tolerant variant of `ASTRO_PLANET_METRICS`. |
| `ASTRO_SYNODIC_SOLVER` | Solves synodic and sidereal period relationships. |
| `ASTRO_SYNODIC_PQ` | Sidereal P/Q calculator from synodic period. |
| `ASTRO_SYNODIC_PS` | Sidereal P/S calculator from synodic period. |
| `ASTRO_SYNODIC_QS` | Sidereal Q/S calculator from synodic period. |
| `ASTRO_APPARENT_SOLAR_SIZE` | Calculates angular solar diameter relative to observer. |
| `ASTRO_ORBIT_CONFIGURATION_INDEX` | Computes two-body orbital configuration symmetry index. |
| `ASTRO_ORBIT_SOLVER` | Full two-body Keplerian solver for mass, period, and axis relationships. |
| `ASTRO_ORBIT_AXIS` | Calculates semi-major axis from mass and period. |
| `ASTRO_ORBIT_PERIOD` | Calculates orbital period from mass and axis. |
| `ASTRO_ORBIT_SUM_MASSES` | Calculates total system mass from period and axis. |
| `ASTRO_SPHERICAL_TO_CARTESIAN` | Converts spherical coordinates into Cartesian coordinates. |
| `ASTRO_CARTESIAN_TO_SPHERICAL` | Converts Cartesian coordinates into spherical coordinates. |
| `ASTRO_DEGREES_TO_DMS_NUM` | Converts decimal degrees to numeric DMS. |
| `ASTRO_DEGREES_TO_DMS_TEXT` | Converts decimal degrees to text DMS. |
| `ASTRO_DMS_NUM_TO_DEGREES` | Converts numeric DMS back into decimal degrees. |
| `DEG_DEC_DMS` | General decimal degree to DMS converter. |
| `DEG_DMS` | General DMS formatter. |
| `DEG_DMS_DEC` | General DMS-to-decimal degree converter. |

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
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Astronomy Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
