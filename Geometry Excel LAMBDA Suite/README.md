# 🧮 Geometry LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for performing key geometric calculations on ellipses, spheres, and derived parameters. These tools are useful for modeling, scientific applications, worldbuilding, and orbital mechanics where ellipse geometry commonly appears.

---

## 📘 Overview

The suite includes eccentricity calculations, full ellipse property extraction, conversion between axis forms, and sphere radius determination from volume. These functions simplify common geometric computations directly within Excel using LAMBDA logic.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `GEOM_ECCENTRICITY` | Calculates the eccentricity of an ellipse from any two axis lengths (automatically assigns major and minor). |
| `GEOM_SEMI_MINOR` | Computes the semi-minor axis length from semi-major axis and eccentricity. |
| `GEOM_ELLIPSE_FROM_AE` | Returns 17 key ellipse parameters given semi-major axis and eccentricity. |
| `GEOM_ELLIPSE_FROM_AXES` | Returns 17 key ellipse parameters given both axes lengths. |
| `GEOM_SPHERE_RADIUS_FROM_VOLUME` | Calculates sphere radius from known volume. |

---

## 🧩 Highlights and Tips

- 🔵 **Axis-Agnostic Eccentricity**: `GEOM_ECCENTRICITY` handles unordered axes automatically — no need to pre-sort inputs.
- 🟠 **Full Ellipse Attributes**: Use `GEOM_ELLIPSE_FROM_AE` or `GEOM_ELLIPSE_FROM_AXES` to obtain full sets of geometric, orbital, and focal parameters.
- 🟣 **Spherical Reverse Calculations**: `GEOM_SPHERE_RADIUS_FROM_VOLUME` directly reverses volume-to-radius calculations for spherical bodies.
- 🧮 **Ramanujan Approximation**: Ellipse perimeter calculations use high-accuracy Ramanujan approximation formulas.
- 🛰 **Ideal for Worldbuilding**: Supports orbital mechanics, planet modeling, and elliptical system design directly inside Excel.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Geometry Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
