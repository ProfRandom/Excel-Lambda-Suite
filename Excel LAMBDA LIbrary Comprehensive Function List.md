# Excel LAMBDA Suite — Complete Function Reference

> *Master Catalog of All Included Functions*  
> *Version: [insert version if you want]*

This document provides a comprehensive listing of all LAMBDA functions included in this repository, organized by functional suite.  
For detailed usage, examples, and documentation, refer to each suite's respective `README.md` file.

---

# Astronomy Excel LAMBDA Suite

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


# Conversion Excel LAMBDA Suite
 
 | Function | Summary |
|---------|---------|
| `CONVERT_TEMP_C_TO_F` | Converts Celsius to Fahrenheit with optional rounding precision. |
| `CONVERT_TEMP_F_TO_C` | Converts Fahrenheit to Celsius with optional rounding precision. |
| `FORMAT_FEET_AND_INCHES` | Converts decimal feet into formatted feet-and-inches strings, supporting decimal or fractional inches. |
| `FORMAT_INCH_FRACTION` | Converts decimal inches into simplified fractional inch format as text. |

# Epoch Conversion Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `EPOCH_GREG_TO_HOLO` | Converts Gregorian year (numeric or text format) to Holocene Era (HE). |
| `EPOCH_HOLO_TO_GREG` | Converts Holocene Era (HE) year into Gregorian year (signed integer). |

# General Utility Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `FORMAT_AS_LIST` | Formats a range into Excel array constant string syntax, optionally sorted, unique, and styled. |
| `COUNTA_STRICT` | Counts non-blank cells while excluding `FALSE` and error values for stricter dynamic array logic. |
| `FORMULA_TEXT` | Returns the text of a formula from a referenced cell (useful for debugging and auditing models). |
| `ROUND_FIX` | Rounds numbers, but preserves clean integer appearance when no decimals are present. |
| `FRAC` | Returns only the fractional part of a numeric value (portion after the decimal point). |
| `RECIP` | Calculates the reciprocal (`1/x`) of a value, returning `#DIV/0!` style errors safely for zero input. |
| `ROOT` | Computes any nth root of a number with basic error handling for invalid roots or negative inputs. |


# List Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `NUMNOTE_ENGINEERING` | Converts a number into engineering notation where exponents are multiples of 3 (e.g., `1.23E+06`). |
| `NUMNOTE_MAGNITUDE` | Converts numbers into human-readable SI-style magnitude suffixes (e.g., k, M, G, m, μ, n). |
| `NUMNOTE_POWERTAG` | Converts numbers into explicit exponential power tags (e.g., `1.23×10^6`) for publication-quality formatting. |

# Percentage Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `PCT_OF` | Calculates a percentage of a value, accepting decimal or whole-number percent inputs. |
| `PCT_POSITION` | Calculates the relative position of a target value within a min-max range (returns a 0–1 scale). |
| `PCT_REMAP` | Remaps a target’s position from one range to a corresponding value in a different output range. |
| `PCT_REMAP_ARRAY` | Applies `PCT_REMAP` to arrays of values for dynamic range remapping across datasets. |
| `PCT_RESOLVE` | Attempts to automatically resolve partial percent input into valid proportions (e.g., 0.75 vs 75). |
| `PCT_LBOUND` | Returns the lower bound (0%) value from a defined range structure. |
| `PCT_UBOUND` | Returns the upper bound (100%) value from a defined range structure. |
| `PCT_INTERPOLATE` | Calculates interpolated values between two percent/value pairs (useful for scoring rubrics or partial grading). |

# Randomizer Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `RND_DIGITS` | Generates a random whole number with a specified number of digits. |
| `RND_MIX` | Generates a random string containing a mix of letters, numbers, and symbols. |
| `RND_STR` | Generates a random string using only alphanumeric characters (letters and numbers). |
| `RND_BY_SEED` | Produces reproducible random output based on a seed value (deterministic randomization). |
| `RND_UNIQUE` | Generates a random permutation of distinct items from a list without repetition. |

# Sequence Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `SEQ_SPAN` | Generates an evenly spaced sequence between two bounds, given a total count of values (includes both endpoints). |
| `SEQ_STEP` | Generates a sequence from lower to upper bound using a fixed step size (direction auto-inferred). |

# Series Summing Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `SUM_N_TERMS` | Calculates sum of an arithmetic progression given start, length, and increment; optionally returns final term only. |
| `SUM_INTEGERS` | Calculates sum of natural numbers, evens, or odds up to a specified limit, based on mode selection. |
| `SUM_RANGE` | Calculates the sum of integers between any two inclusive bounds using closed formula (start to end). |
| `SUM_BETWEEN_BOUNDS` | Like `SUM_RANGE`, but validates and corrects bound order automatically (swaps if necessary). |

# Statistical Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `STAT_QNTILES` | Calculates quantiles or labeled percentile cuts with bin-mode slicing and precision control. |
| `STAT_FREQ_TABLE` | Generates frequency counts for categorical data ranges. |
| `STAT_SUMMARY` | Returns min, max, mean, median, and standard deviation for a numeric dataset. |
| `STAT_MIDRANGE` | Computes midrange (average of min and max). |
| `STAT_MINMAX` | Returns both minimum and maximum values as a paired array. |
| `STAT_STDERR` | Computes standard error of the mean. |
| `STAT_WTD_AVG` | Computes weighted averages using paired value and weight arrays. |
| `STAT_SELF_WTD_AVG` | Computes self-weighted average where each value serves as its own weight. |
| `STAT_PCT_OF_RANGE` | Calculates what percentage of the range a target value represents. |
| `STAT_VALUE_OF_PCT` | Returns the data value corresponding to a given percentile within a dataset. |
| `STAT_PCT_REMAP` | Remaps a target's position from one range onto a new range based on percentile alignment. |
| `STAT_VAL_BRACKET` | Assigns a value into its corresponding percentile bracket using quantile thresholds. |
| `STAT_VOLUME` | Computes volume from width, depth, and height (simple helper utility). |
| `STAT_BENFORD_TABLE` | Returns expected digit frequencies for Benford’s Law analysis (1st-digit forensic test). |
| `STAT_RND_BENFORD` | Generates random samples distributed according to Benford’s Law (for simulation and testing). |
| `STAT_SHAPE` | Reports array dimensions (rows, columns, total size). |
| `STAT_GEO5` | Calculates the 5-number summary (min, Q1, median, Q3, max). |

# String Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `STR_GETDIGITS` | Extracts all digit characters from a text string. |
| `STR_GETCHARS` | Extracts all non-digit characters from a text string. |
| `STR_FILTERCHARS` | Filters string content, returning only characters matching a custom character set. |
| `STR_COUNTCHAR` | Counts occurrences of a specific character within a string. |
| `STR_UNIQUECHARS` | Returns unique characters from a string, eliminating duplicates. |
| `STR_SPLITCHARS` | Splits a string into an array of single characters. |
| `STR_HASCAP_AFTERFIRST` | Tests if a string contains capital letters after the first character (camelCase detection). |
| `STR_REMOVE_ENCLOSED` | Removes substrings enclosed within specified start/end markers (e.g., parentheses). |
| `STR_SANITIZE` | Removes control characters (tabs, line breaks, non-printables) from text. |
| `STR_TEXTBETWEEN` | Extracts substring located between two delimiters (simplified version of Excel's native `TEXTBETWEEN`). |

# Time Conversion Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `TIME_UNITS_TO_DECIMAL` | Converts multiple time components (years, days, hours, minutes, seconds) into a decimal time value in any unit (Y, D, H, M, S). |
| `TIME_DECIMAL_TO_UNITS` | Decomposes a decimal time value back into its full component breakdown. |
| `TIME_DIFF` | Calculates the full difference between two decimal time values, returning signed and absolute unit deltas. |
| `TIME_CLOCK12_TO_MIL12` | Converts 12-hour clock time (e.g. `10:30 PM`) to 12-hour military format (0000–1159). |
| `TIME_MIL12_TO_CLOCK12` | Converts 12-hour military time (0000–1159) back to standard 12-hour AM/PM clock format. |
| `TIME_MIL12_TO_MIL24` | Converts 12-hour military format to 24-hour military format (0000–2359). |
| `TIME_MIL24_TO_MIL12` | Converts 24-hour military format back to 12-hour military format. |
| `TIME_MIL12_SHIFT` | Applies offset to 12-hour military time with wraparound adjustment. |
| `TIME_STD12_SHIFT` | Applies offset to standard 12-hour AM/PM clock time with wraparound correction. |

# Mathematics Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `MATH_LCM_SCALED` | Computes scaled least common multiple (LCM) of two decimal values using precision scaling. |
| `MATH_LCM_SCALED_ARRAY` | Computes LCM across an array of decimal or fractional values with precision scaling. |
| `MATH_SPLIT_FRACTION` | Splits a fraction string (e.g. `"3/4"`) into its numerator and denominator as a 2-element array. |
| `MATH_FRACTION_TO_DECIMAL` | Converts a fraction string into a decimal value. |
| `MATH_SPLIT_INTEGER_DECIMAL` | Separates a number into its integer and fractional parts, returning both as an array. |
| `MATH_GET_DECIMAL_PART` | Extracts the decimal portion of a number, optionally signed. |
| `MATH_DIGITAL_ROOT` | Computes the digital root (iterative digit sum) of a number. |
| `MATH_DIGITAL_SUM` | Computes the simple (single-pass) sum of all digits of a number. |
| `MATH_POLYGONAL` | Returns the nth polygonal (figurate) number for any sided polygon (triangular, square, hexagonal, etc). |
| `MATH_QUADRATIC_REAL_ROOTS` | Calculates the real roots of a quadratic equation using the quadratic formula. |
| `MATH_NORMALIZE_DECIMAL` | Normalizes any number to a decimal < 1, preserving significant digits. |
| `MATH_APPROXIMATE_FRACTION` | Approximates a decimal as a fraction or mixed number string. |
| `MATH_LIST_DIVISORS` | Returns all positive integer divisors of a given number as an array or formatted string. |
| `MATH_METALLIC_MEAN` | Calculates the nth metallic mean (golden, silver, bronze, etc) with optional reciprocal. |
| `MATH_FORMAT_AS_FRACTION` | Converts a decimal to a simplified fraction string based on a fixed denominator base. |

# Geometry Excel LAMBDA Suite

| Function | Summary |
|---------|---------|
| `GEOM_ECCENTRICITY` | Calculates the eccentricity of an ellipse from any two axis lengths (automatically assigns major and minor). |
| `GEOM_SEMI_MINOR` | Computes the semi-minor axis length from semi-major axis and eccentricity. |
| `GEOM_ELLIPSE_FROM_AE` | Returns 17 key ellipse parameters given semi-major axis and eccentricity. |
| `GEOM_ELLIPSE_FROM_AXES` | Returns 17 key ellipse parameters given both axes lengths. |
| `GEOM_SPHERE_RADIUS_FROM_VOLUME` | Calculates sphere radius from known volume. |


--- 

[... and continue for all your other suites exactly as you have it ...]

---

## 📄 About This Catalog

This index is provided as a **quick reference master list** of available functions across all Excel LAMBDA suites included in this repository.

- Full documentation, parameter descriptions, and usage examples are provided in each suite’s own README file.
- Functions are fully self-contained and require no external dependencies beyond native Excel LAMBDA support.

For questions or feedback, see repository contact information.