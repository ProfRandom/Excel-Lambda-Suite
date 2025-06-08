# Astronomy Utilities Suite

This Excel LAMBDA function suite provides a rich set of tools for modeling, simulating, and exploring astrophysical and planetary systems.

## 📘 How to Use

Each function is defined with full usage examples and parameter notes in the code file:  
**See `astro_lambda_listing.txt` for full documentation and formulas.**

## 🔭 Function Index

| Function Name               | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| ASTRO_HAB_INDEX            | Returns a normalized habitability index based on orbital distance          |
| ASTRO_SPECTRAL_DISTRIBUTION | Distributes stars by spectral class using inverse population factors       |
| ASTRO_CALC_TEMP            | Computes temperature for a given stellar subclass (e.g. "G2.5")             |
| ASTRO_TYPE_FROM_TEMP       | Returns spectral type from given temperature                               |
| ASTRO_DISPLAY_SPECTRAL     | Displays spectral classification matrix or subset                          |
| ASTRO_STAR_ATTRIBUTES      | Derives stellar mass, radius, luminosity, etc., from one known parameter   |
| ASTRO_HABITABLE_ZONES      | Returns scaled distances for circumstellar habitable zones                 |
| ASTRO_STAR_DENSITY_VOLUME  | Calculates star count for a volume or radius based on stellar density      |
| ASTRO_PLANET_METRICS       | Computes mass, radius, gravity, etc. from any valid parameter pair         |
| ASTRO_SYNODIC_SOLVER       | Flexible solver for sidereal/synodic period calculations                   |
| ASTRO_APPARENT_SOLAR_SIZE  | Computes angular size of a star from a given radius and distance           |
| ASTRO_ORBIT_CONFIGURATION_INDEX | Characterizes orbital nesting or crossing based on mass asymmetry     |
| ASTRO_ORBIT_SOLVER         | Solves orbital axis, period, or mass from two known values                 |
| DEG_DEC_DMS, DEG_DMS, etc. | Degree/minute/second format converters                                     |

… *(and so on through the rest of the suite)*

---

## 📎 Notes

- Many functions accept optional `precision` parameters (defaulting to 3 or 4 decimal places).
- Some solver functions offer multiple output formats: raw, labeled, verbose, tabular.
- See `astro_lambda_listing.txt` for implementation logic and example usage.

---

## 📂 File Reference

- `astro_lambda_listing.txt`: Full LAMBDA function definitions with inline documentation and examples.
