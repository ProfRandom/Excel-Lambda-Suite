# RND_ Utilities Suite

This suite provides a collection of Excel LAMBDA functions for generating random values in various formats—digits, characters, unique sequences, and mixed-case strings. These tools are designed for use in test data creation, randomized workflows, mockup generation, and secure input scaffolding.

> All functions are self-contained, input-validating, and return scalar or array outputs depending on usage.

---

## 🎲 Function Index

| Function Name   | Description |
|-----------------|-------------|
| `RND_DIGITS`    | Returns a random number with a specified number of digits. |
| `RND_MIX`       | Generates a random string of mixed-case letters, numbers, and symbols. |
| `RND_STR`       | Produces a random alphabetic string with configurable case (lower, upper, or mixed). |
| `RND_UNIQUE`    | Returns a randomized, non-repeating sequence of numbers. |
| `RND_ID`*       | *(Deprecated alias)* Former name of `RND_MIX`. Retain for compatibility if used previously. |
| `RND_BY_SEED`     | Generates a deterministic pseudo-random number from a seed using Lehmer RNG. |


---

## 📘 Usage Notes

- **Validation**: All functions enforce numeric input where appropriate. Invalid types raise `#VALUE!`; invalid ranges raise `#NUM!`.
- **Defaults**: Length arguments default to 5 where omitted or set to 0.
- **ASCII Ranges**: Character generation uses ASCII codes via `CHAR()`, supporting a full alphanumeric and symbol set.
- **Composable Output**: Results may be wrapped with functions like `SORT()`, `TEXT()`, or `LOWER()` as needed.
- **Functionality Focus**: This suite is for generation, not for statistical analysis or probability-weighted sampling (e.g. `RND_WEIGHTED`, `RND_PROB`)—which may be added in a separate advanced suite.
- **Deterministic Randomness**: Use `RND_BY_SEED(seed)` for reproducible pseudo-random generation, useful in test automation or seeded shuffling.
- **Benford Distribution**: For randomization functions based on the Benford Distribution, see the `STAT_` Functions Suite.


---

## 📂 Files

- `rnd_utils.txt`: Full suite with function definitions, inline documentation, and test examples.
