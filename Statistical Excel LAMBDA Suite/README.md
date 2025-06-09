# 📊 STAT_ Utilities Suite

This suite provides a collection of Excel LAMBDA functions for statistical analysis, distribution summaries, percentile quantiles, shape metrics, and data characterization. Designed for educators, analysts, and data stewards who want immediate insights from raw data—without complex setup or external tools.

> All functions are self-contained, input-validating, and support scalar or array output depending on use. Most functions support label-enhanced output via a `"LBL"` parameter.

---

## 📘 Function Index

| Function Name         | Description |
|-----------------------|-------------|
| `STAT_QNTILES`        | Returns deciles, quartiles, or custom quantile cut points from a dataset. |
| `STAT_STDERR`         | Computes standard error of the mean (population or sample). |
| `STAT_MINMAX`         | Reports min and max values, optionally with labels and layout options. |
| `STAT_SUMMARY`        | Compact 5- or 6-point summary around the mean and standard deviation. |
| `STAT_GEO5`           | Reports geometric 5-point spread: min, lower-mid, midrange, upper-mid, max. |
| `STAT_VOLUME`         | Returns count, sum, and mean of a dataset. |
| `STAT_SHAPE`          | Measures central tendency and shape: mean, median, skewness, kurtosis. |
| `STAT_MIDRANGE`       | Returns the midpoint between the dataset’s minimum and maximum. |
| `STAT_FREQ_TABLE`     | Builds a frequency table with value counts and weighted product sums. |
| `STAT_WTD_AVG`        | Computes a weighted average of two parallel arrays. |
| `STAT_SELF_WTD_AVG`   | Computes a self-weighted average using each value as its own weight. |
| `STAT_PCT_REMAP`      | Maps a value from one range to another based on relative position. |
| `STAT_PCT_OF_RANGE`   | Determines what percentage a value represents between a given min and max. |
| `STAT_VALUE_OF_PCT`   | Calculates the value that corresponds to a given percent position in a range. |
| `STAT_BENFORD_TABLE`  | Lists theoretical Benford digit probabilities for digits 1 through 9. |
| `STAT_RND_BENFORD`    | Returns a random digit (or multi-digit number) weighted by Benford probabilities. |
| `STAT_VAL_BRACKET`    | Locates the bounding values surrounding a specified number in a dataset. |

---

## 📘 Usage Notes

- **Label Output**: Most functions accept `"LBL"` as a flag to return two-column labeled outputs. This enables immediate interpretation without sacrificing numeric accessibility.
- **Precision Handling**: The `[prec]` argument controls rounding; default is 3 decimals unless otherwise noted.
- **Validation**: Functions enforce valid ranges and parameter types. Invalid input returns `#NUM!` or `#VALUE!` as appropriate.
- **Flexible Formats**: Where applicable, vertical, horizontal, and string outputs are supported via keywords (`"VER"`, `"HOR"`, `"STR"`).
- **Benford Support**: The Benford-related functions enable both distribution inspection and probability-weighted random digit generation. See also: `STAT_BENFORD_TABLE`, `STAT_RND_BENFORD`.
- **Symmetry vs Distribution**: Functions like `STAT_GEO5` are symmetry-based (geometric intervals) rather than percentile-driven.

---

## 🔍 Related Functions

- **Quantile Analysis**: `STAT_QNTILES`
- **Summary Reporting**: `STAT_SUMMARY`, `STAT_GEO5`
- **Shape Detection**: `STAT_SHAPE`, `STAT_STDERR`
- **Range Mapping**: `STAT_PCT_REMAP`, `STAT_PCT_OF_RANGE`, `STAT_VALUE_OF_PCT`
- **Data Frequency**: `STAT_FREQ_TABLE`, `STAT_WTD_AVG`, `STAT_SELF_WTD_AVG`

---

## 📂 Files

- `stat_utils.txt`: Full suite of function definitions with inline comments and usage examples.
- `stat_utils_readme.md`: This README file.

