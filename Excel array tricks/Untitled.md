## 🧠 **Excel Array-Broadcasting Cheat Sheet**

### 🎯 **Basic Element-wise Operations**

|Expression|Description|Example Result (for input `{"a", "b", "c"}`)|
|---|---|---|
|`array = "b"`|Compares each element to `"b"`|`{FALSE; TRUE; FALSE}`|
|`ISNUMBER(VALUE(array))`|Checks if each element can be converted to a number|`{#VALUE!; 1; 3.5} → {FALSE; TRUE; TRUE}`|
|`LEN(array)`|Gets the length of each string in the array|`{"cat"; "lion"; "panther"} → {3; 4; 7}`|
|`LEFT(array, 1)`|Gets the first character of each string|`{"cat"; "lion"; "tiger"} → {"c"; "l"; "t"}`|

---

### 🧪 **Useful Character Filters**

excel

CopyEdit

`CODE(array)                  → ASCII codes of each character array = "."                  → TRUE where character is a period array >= "0" AND array <= "9"  → TRUE where character is numeric`

These comparisons auto-broadcast across the array.

---

### 🔁 **Using `SEQUENCE` to Iterate**

excel

CopyEdit

`SEQUENCE(LEN("F5.6V"))  → {1; 2; 3; 4; 5}`

Used with `MID()`:

excel

CopyEdit

`MID("F5.6V", SEQUENCE(5), 1) → {"F"; "5"; "."; "6"; "V"}`

---

### 🧩 **Combining Arrays with Boolean Filters**

excel

CopyEdit

`FILTER(array, condition)`

Returns only values in `array` where corresponding `condition` is TRUE.

excel

CopyEdit

`chars = {"F"; "5"; "."; "6"; "V"} isNum = ISNUMBER(VALUE(chars) + (chars = ".")) FILTER(chars, isNum) → {"5"; "."; "6"}`

---

### 🛠️ **Other Handy Broadcast Operations**

|Function|Use Case|
|---|---|
|`TEXT(array, format)`|Apply a number/text format to each item|
|`IF(condition, A, B)`|Returns element from A or B for each row|
|`BYROW(array, lambda)`|Apply row-wise transformation|
|`BYCOL(array, lambda)`|Apply column-wise transformation|
|`MAKEARRAY(r, c, lambda)`|Custom generate arrays row-by-row|

---

### ⚠️ **Tips for Array Debugging**

- Use **`LET()`** liberally to store and label intermediate steps.
    
- Wrap intermediate arrays with `TEXTJOIN(", ", , array)` to quickly visualize them.
    
- You can "peek" inside a formula step-by-step using **Evaluate Formula** (on the Formulas tab).

## 🧠 Why `LEN(array)` _doesn't_ mean "length of the array"

### ⚠️ The Confusion

When you write:

excel

CopyEdit

`LEN("F5.6V")`

You get:

CopyEdit

`→ 5`

Which is the number of **characters** in the **string**, not the number of elements in an array.

But if you write:

excel

CopyEdit

`LEN({"dog", "cat", "moose"})`

Excel returns:

CopyEdit

`→ {3, 3, 5}`

Each value is the **length of the corresponding string**, not the number of items in the array (which would be 3 in this case).

---

## ✅ What `LEN(...)` Actually Measures

- **Strings** → character count
    
- **Arrays of strings** → array of character counts
    
- **Numbers** → digit count (kinda)
    

**It doesn't count how many elements are in an array** — that’s the job of `COUNTA()` or `ROWS()` / `COLUMNS()` depending on layout.

---

## ✅ What SEQUENCE(LEN("F5.6V")) Really Does

It expands into:

excel

CopyEdit

`SEQUENCE(5) → {1; 2; 3; 4; 5}`

Because `"F5.6V"` is a **string with 5 characters**, so LEN returns 5 — and **that** becomes the number of rows in the SEQUENCE.

---

## 🧩 So, What If You Do Want the Number of Elements in an Array?

Let’s say you have:

excel

CopyEdit

`{"a", "b", "c", "d"}`

You can get:

|Desired Info|Use This|Returns|
|---|---|---|
|Total elements|`COUNTA(array)`|`4`|
|Rows in vertical|`ROWS(array)`|(e.g.) `4`|
|Columns in horizontal|`COLUMNS(array)`|(e.g.) `4`|

---

So:

- `LEN()` → character count
    
- `COUNTA()` → element count
    
- `SEQUENCE(LEN(string))` → get character positions in string
    
- `MID(string, SEQUENCE(LEN(string)), 1)` → explode string into array of characters