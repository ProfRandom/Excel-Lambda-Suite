# Excel LAMBDA Suite: Advanced Formula Library

## TL;DR

**A collection of reusable Excel LAMBDA functions for advanced modeling, analysis, and spreadsheet automation.**

This library provides fully self-contained Excel LAMBDA functions for scenarios where native formulas can be complex, verbose, or unintuitive. Each function wraps modeling patterns into easy-to-use, parameter-driven tools for simulation, data prep, statistics, text manipulation, randomization, and more.

> ✅ Fully documented  
> ✅ Self-contained functions  
> ✅ Excel 365 / Excel 2021+ compatible

For complete documentation, detailed examples, and function lists, see below.

---

## 📘 Purpose and Motivation

Modern Excel — particularly with the introduction of LAMBDA functions and dynamic arrays — has unlocked enormous potential for spreadsheet modeling, data analysis, and complex functional design.

However, while Excel's built-in functions are extremely powerful, certain modeling patterns remain either unintuitive or cumbersome for many users, especially when the native method requires careful chaining of several lower-level functions.

This library was built to:

- **Encapsulate reusable modeling patterns** into accessible, parameter-driven LAMBDA functions.
- **Simplify complex constructs** that may be technically possible using core functions, but are opaque to casual or even intermediate users.
- **Expose composable, readable LAMBDAs** that reduce formula clutter, promote maintainability, and empower users to build sophisticated models without needing to reconstruct low-level formula logic repeatedly.

> Example:  
> While Excel’s `SEQUENCE()` can technically generate bounded series through careful parameter calculation (`ROUND(SEQUENCE(rng - 1, , lbound + stp, stp), rnd)`), this may not be intuitive for many users.  
> The `SEQ_SPAN` and `SEQ_BOUND` functions in this library allow users to directly input lower bounds, upper bounds, step logic, rounding, and bracketing options — encapsulating both the power and the intent into a human-facing interface.

---

## ⚠️ A Personal Note

I make no claim to being an expert in all of the domains represented by these functions — astronomy, statistics, simulation, and modeling each have highly specialized best practices far beyond what’s captured here.

I am not an Excel MVP, nor a professional Excel trainer — simply an Excel user who discovered recurring patterns in my own modeling work that seemed unnecessarily opaque or complex to build repeatedly from scratch.

While some functions here could surely be written more elegantly or efficiently by true domain specialists, my goal was to encapsulate useful building blocks that I found myself repeatedly reaching for — and to share them in case they might prove equally helpful to others facing similar challenges.

---

## 🛠️ Repository Contents

| Suite | Description |
|---------|-------------|
| **Astronomy** | Astrophysical modeling, orbital mechanics, stellar classification |
| **Conversion** | Temperature conversions, imperial measurement formatting |
| **General Utility** | Formula helpers, rounding, roots, reciprocals, strict counting |
| **List** | Advanced list filtering, reshaping, duplicate analysis, enumeration |
| **Number Notation** | Engineering notation, SI suffixes, power tags |
| **Percentage** | Percentile calculations, remapping, interpolation |
| **Randomizer** | Random number, string, and sample generation |
| **Sequence** | Evenly spaced numeric sequences, step-based ranges |
| **Series Summing** | Closed-form summing of arithmetic progressions and natural numbers |
| **Statistical** | Quantiles, weighted averages, Benford analysis, statistical summaries |
| **String** | Character filtering, extraction, string sanitization |
| **Time Conversion** | Mixed-unit time calculations, clock format conversions |

Each suite includes:

- A `.txt` file containing all LAMBDA definitions with inline documentation.
- A `README.md` file explaining function usage and parameters.
- A `.zip` archive containing these files for easy offline download or backup.

---

## ⚙️ Requirements

- Microsoft Excel 365 or Excel 2021+  
- LAMBDA function support with dynamic arrays enabled  
- No external add-ins or packages required

---

## 🚀 Installation & Usage

- Functions may be copied directly into Excel’s **Name Manager**.
- Functions are fully self-contained and composable.
- Use included `README.md` files for each suite to understand available functions, parameters, and examples.
- Download `.zip` archives of each suite for offline storage or sharing.

---

## 🤖 AI Co-Author Contribution

This project was developed with **heavy assistance from ChatGPT (OpenAI)** as a collaborative pair-programming assistant.

The AI contributed to:

- Formula design and error handling
- Pattern encapsulation for LAMBDA workflows
- Parameter validation techniques
- Documentation writing
- Example generation
- README creation

The human author provided overall design goals, testing, packaging, integration, and use-case refinement.

---

## 🙏 Acknowledgements

- The Excel LAMBDA engineering team for opening an entirely new world of functional composition within spreadsheets.
- The Excel community and numerous LAMBDA enthusiasts for sharing creative patterns, prompting many of the use cases here.
- OpenAI ChatGPT for its tireless (and lightning-fast) co-authoring assistance in both code and documentation development.
- The general spreadsheet modeling community whose real-world problems provided inspiration for simplifying common modeling patterns.

---

## 📬 Feedback & Contact

This project is provided as-is for the community.

If you encounter issues, have suggestions, or wish to provide feedback, feel free to open an issue on this repository.

At this time, pull requests are not being accepted.

While I’m happy to share these functions as a resource, I’m not currently able to take on the time commitment required to review, test, and integrate external code submissions. Maintaining design consistency and avoiding support obligations are important goals for keeping this library sustainable.

---

## 🚧 Known Limitations and Future Directions

While this library demonstrates much of what is already possible with modern Excel's LAMBDA and dynamic array support, it also exposes several current limitations that remain obstacles for more scalable LAMBDA-based application design:

### 🔄 Distribution & Versioning

- LAMBDA functions are currently bound to individual workbooks.
- No built-in support exists for shared libraries or central package repositories.
- Updates and version control across multiple workbooks are entirely manual, creating friction for team-based development or iterative model refinement.
- Ideally, Excel would support native LAMBDA function packages, with versioning, publishing, and managed imports.

### 🔧 Lack of Scoped Helper Functions

- Many functions in this library reuse similar calculation logic internally.
- Currently, helper logic must either:
  - Be repeated inline inside every primary function (leading to redundancy and harder maintenance), or
  - Be defined as separate LAMBDAs in the Name Manager (which introduces fragile dependencies if not copied together).
- Excel LAMBDA would greatly benefit from supporting **locally scoped helper functions** — allowing private subfunctions to exist within a parent LAMBDA definition (similar to `LET` scoping or local DEF blocks).

### 📦 No Native Package Format

- There is no way to bundle related LAMBDA functions into a coherent package or module.
- Users must manually manage groups of functions when copying between workbooks.
- A future Excel-native LAMBDA package format would enable safe imports, clear dependency resolution, and controlled updates.

### 🔁 Limited Composability for Library Distribution

- The current design forces a trade-off between:
  - **Self-contained functions** (safe for isolated use but prone to duplication),
  - and **inter-dependent helper structures** (efficient, but fragile without awareness of dependencies).
- As Excel evolves, introducing better **dependency resolution tools** could help end-users safely adopt larger LAMBDA-based libraries without unexpected breakage.

### 🔮 The Future of Spreadsheet-Native Functional Programming

Despite these current limitations, Excel LAMBDA is rapidly transforming spreadsheets into fully composable, human-facing functional programming environments. With continued development — especially around local scoping, packaging, and dependency management — LAMBDA has the potential to eventually replace VBA for many modeling, automation, and spreadsheet application design use cases, even for casual users.

This library aims to anticipate that direction by demonstrating reusable design patterns that wrap complex formula logic into **accessible, parameter-driven, safe, and composable functions**.

---

## 📄 License

This project is licensed under the **MIT License**.  
See the LICENSE file for details.
