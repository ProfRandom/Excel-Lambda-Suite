### `TIME_UNITS_TO_DECIMAL(unit, [y], [d], [h], [m], [s], [outputMode])`

Converts a time duration expressed in years, days, hours, minutes, and seconds into a single decimal value in the specified unit.

#### Parameters:
- `unit` *(required)* – The unit to convert to: `"Y"`, `"D"`, `"H"`, `"M"`, or `"S"`  
- `y`, `d`, `h`, `m`, `s` *(optional)* – Component values (default = 0)
- `outputMode` *(optional)*:
  - `0` (default): returns numeric result (e.g. `26.5`)
  - `1`: returns text with unit suffix (e.g. `"26.5h"`)

#### Examples:
```excel
TIME_UNITS_TO_DECIMAL("H", 0, 1, 2, 30, 0)
→ 26.5

TIME_UNITS_TO_DECIMAL("H", 0, 1, 2, 30, 1)
→ "26.5h"
```

#### Notes:
- All inputs default to `0` if omitted.
- Accepts partial or full unit labels (e.g., `"Hours"` becomes `"H"`).
- Rounds text output to 9 decimal places.
- Based on astronomical conversions: 1 year = 365.25 days = 8766 hours, etc.

---
### `TIME_DECIMAL_TO_UNITS(unit, value, [mode], [decimalPlaces])`

Converts a decimal value in a given time unit into a formatted breakdown of **years, days, hours, minutes, and seconds**.

#### Parameters:
- `unit` *(required)* – The source unit of the decimal time:
  - `"Y"`, `"D"`, `"H"`, `"M"`, or `"S"` (case-insensitive)
- `value` *(required)* – A decimal value to convert (e.g., `1.75` days)
- `mode` *(optional)* – Output format:
  - `0`: `"00:000:00:00:00.000"` — padded colon-separated format
  - `1`: `"0y 0d 0h 0m 0.000s"` — labeled natural-language format
- `decimalPlaces` *(optional)* – Number of decimal places to show for seconds (default is `3`)

#### Examples:
```excel
TIME_DECIMAL_TO_UNITS("H", 1.999999997, 1, 3)
→ "0y 0d 1h 59m 59.999s"

TIME_DECIMAL_TO_UNITS("H", 1.999999997, 0, 3)
→ "00:000:01:59:59.999"
```

#### Notes:
- Accepts any time unit as the base: years, days, hours, minutes, or seconds.
- Seconds are **never rounded up** to avoid time overflow errors (e.g., `59.999s` stays below `60s`).
- Padding and formatting are standardized across modes.
- Use mode `0` for **machine-friendly** outputs; use mode `1` for **human-readable** display.

---
### `TIME_DIFF(start, end, [mode], [roundPlaces])`

Calculates the time difference between two time values, supporting multiple output formats.

#### Parameters:
- `start` *(required)* – The starting time (Excel time or string like `"08:30"`).
- `end` *(required)* – The ending time.
- `mode` *(optional)*:
  - `0` (default): `"hh:mm:ss"` format string
  - `1`: Decimal hours (e.g., `1.75`)
  - `2`: Verbose label format (e.g., `"1h 45m 0s"`)
- `roundPlaces` *(optional)* – Number of decimal places (only applies to mode `1`, default = `9`)

#### Examples:
```excel
TIME_DIFF("08:00", "10:00")
→ "02:00:00"

TIME_DIFF("08:00", "10:00", 1)
→ 2.000000000

TIME_DIFF("08:00", "10:00", 2)
→ "2h 0m 0s"

TIME_DIFF("08:00", "10:45", 1, 2)
→ 2.75
```

#### Notes:
- Automatically handles times that cross midnight (e.g., `"23:30"` to `"01:00"` will return `"01:30:00"`).
- All modes calculate based on a 24-hour clock.
- In mode `1`, use `roundPlaces` to control the decimal precision of the result.

---

### `TIME_MIL12_TO_MIL24(incoming)`

Converts a time string in compact military 12-hour format (e.g., `"0930AM"` or `"1215PM"`) into a standard 24-hour military format (`"0930"`, `"1215"`, `"2030"`, etc).

#### Parameters:
- `incoming` *(required)* — A 6-character string representing time in 12-hour military format:
  - `"hhmmAM"` or `"hhmmPM"`
  - Example: `"0830AM"`, `"1245PM"`

#### Returns:
A 4-digit string representing the time in **24-hour military format** (`"HHMM"`).

#### Examples:
```excel
TIME_MIL12_TO_MIL24("0830PM")
→ "2030"

TIME_MIL12_TO_MIL24("1200AM")
→ "0000"

TIME_MIL12_TO_MIL24("1215PM")
→ "1215"
```

#### Notes:
- `"12:00 AM"` is returned as `"0000"` (midnight).
- `"12:00 PM"` is returned as `"1200"` (noon).
- Useful for converting legacy schedules, shift logs, or export data where compact AM/PM strings are used.

---

### `TIME_MIL24_TO_MIL12(incoming)`

Converts a 24-hour military time string (e.g., `"1345"`, `"0000"`) into a compact 12-hour format with AM/PM suffix (e.g., `"0145PM"` or `"1200AM"`).

#### Parameters:
- `incoming` *(required)* — A 4-digit string in the format `"HHMM"` representing time in 24-hour clock.

#### Returns:
A 6-character string in `"hhmmAM"` or `"hhmmPM"` format.

#### Examples:
```excel
TIME_MIL24_TO_MIL12("1345")
→ "0145PM"

TIME_MIL24_TO_MIL12("1200")
→ "1200PM"

TIME_MIL24_TO_MIL12("0000")
→ "1200AM"
```

#### Notes:
- `"0000"` (midnight) becomes `"1200AM"`
- `"1200"` (noon) remains `"1200PM"`
- Useful for converting internal schedule times to human-readable formats or for exporting to legacy formats.

---

### `TIME_MIL12_TO_CLOCK12(incoming)`

Converts a compact military-style 12-hour time string (e.g., `"0930AM"`, `"1245PM"`) into a standard human-readable 12-hour clock format (`"9:30AM"`, `"12:45PM"`).

#### Parameters:
- `incoming` *(required)* — A 6-character string representing 12-hour military time:
  - Format: `"hhmmAM"` or `"hhmmPM"`

#### Returns:
A string in `"h:mmAM"` or `"h:mmPM"` format, suitable for display.

#### Examples:
```excel
TIME_MIL12_TO_CLOCK12("0930AM")
→ "9:30AM"

TIME_MIL12_TO_CLOCK12("1245PM")
→ "12:45PM"
```

#### Notes:
- Input `"1200AM"` (midnight) returns `"12:00AM"`
- Input `"1200PM"` (noon) returns `"12:00PM"`
- Leading zeros in hour are dropped for readability (e.g., `"09"` → `"9"`)
- Use this function for formatting purposes when converting legacy or compact time strings

___
### `TIME_CLOCK12_TO_MIL12(incoming)`

Converts a standard 12-hour clock value (e.g., `"9:30 AM"` or Excel serial time) into a compact military-style 12-hour format with no colon (`"0930AM"`, `"1245PM"`).

#### Parameters:
- `incoming` *(required)* — A 12-hour time string (e.g., `"9:30 AM"`) or a serial time value.

#### Returns:
A fixed-length `"hhmmAM"` or `"hhmmPM"` string for use in scheduling, reporting, or system export.

#### Examples:
```excel
TIME_CLOCK12_TO_MIL12("9:30 AM")
→ "0930AM"

TIME_CLOCK12_TO_MIL12("12:45 PM")
→ "1245PM"

TIME_CLOCK12_TO_MIL12(TIME(8, 5, 0))
→ "0805AM"
```

#### Notes:
- Pads both hours and minutes with leading zeros.
- Works with both strings and serial date/time values.
- Complements `TIME_MIL12_TO_CLOCK12()` to support round-trip conversion.

---
### `TIME_MIL12_SHIFT(incoming, adjustment)`

Shifts a compact 12-hour military-style time string (e.g., `"0930AM"`) by a number of hours (positive, negative, or fractional).

#### Parameters:
- `incoming` *(required)* — Time string in `"hhmmAM"` or `"hhmmPM"` format
- `adjustment` *(required)* — Number of hours to add (e.g., `2`, `-1.5`, `0.25`)

#### Returns:
A new time in the same `"hhmmAM"`/`"hhmmPM"` format.

#### Examples:
```excel
TIME_MIL12_SHIFT("0930AM", 2.25)
→ "1145AM"

TIME_MIL12_SHIFT("1145AM", -2.25)
→ "0930AM"

TIME_MIL12_SHIFT("1130PM", 2)
→ "0130AM"
```

#### Notes:
- Automatically wraps over midnight (e.g., `"1130PM" + 2` → `"0130AM"`)
- Useful for calculating **class end times**, **shift planning**, or **time block scheduling**
- Works with fractional hours (e.g., 1.75 = 1 hour 45 minutes)

---

### `TIME_STD12_SHIFT(startTime, adjustment, [formatted])`

Shifts a standard Excel 12-hour time (e.g., `"9:30 AM"`) forward or backward by a number of hours.

#### Parameters:
- `startTime` *(required)* — Excel 12-hour time value (e.g., `"9:30 AM"` or `TIME(9,30,0)`)
- `adjustment` *(required)* — Number of hours to shift (can be negative or fractional)
- `formatted` *(optional)* — 
  - `TRUE`: return `"hh:mm AM/PM"` string
  - `FALSE` or omitted: return raw Excel time serial

#### Returns:
A new time value adjusted by `adjustment`, either as a number (default) or a formatted string.

#### Examples:
```excel
TIME_STD12_SHIFT("9:30 AM", 2.5)
→ 0.52083  // Excel serial time for 12:00 PM

TIME_STD12_SHIFT("9:30 AM", 2.5, TRUE)
→ "12:00 PM"

TIME_STD12_SHIFT("11:45 PM", 1.25, TRUE)
→ "01:00 AM"
```

#### Notes:
- Handles wraparound past midnight using `MOD(...)`.
- Compatible with native Excel time logic (fractional days).
- Use `formatted` to control whether result is visual or computational.


