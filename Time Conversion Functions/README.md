
# 📊 Excel Time Conversion Toolkit

🚀 **A powerful Excel toolkit for bidirectional time conversion!**  
These functions make it easy to convert between **decimal time** and **formatted time units**—perfect for **astronomy, physics, worldbuilding, and data analysis**.

---

## 📌 Included Functions

| Function | Purpose |
|----------|---------|
| **DECTIME()** | Convert Y/D/H/M/S → Decimal |
| **DECTIMEF()** | Convert Y/D/H/M/S → Decimal (Formatted) |
| **EXPTIMET()** | Convert Decimal → Readable Text |
| **EXPTIMEF()** | Convert Decimal → Formatted Colon-Separated Time |

✅ **How to Use:**  
1. **Download the `.xlsx` file** from this repo.  
2. Open Excel and **copy the LAMBDA functions into Name Manager**.  
3. Use them in your formulas—instant time conversion!  

---
### 🔄 **Example Conversions**
- `EXPTIMET("D", 987.654321)` → `"2y 257d 15h 42m 13.334s"`
- `EXPTIMEF("D", 987.654321)` → `"02:257:15:42:13.334"`
- `DECTIME("D", 2, 257, 15, 42, 13.334)` → `987.654321`

---
### **🔒 Why Use This?**
✔ **Prevents lost work—your functions are backed up!**  
✔ **Works entirely inside Excel (no add-ins required).**  
✔ **Handles both decimal & formatted time conversions.**  
✔ **Precision control (round seconds to 3-9 decimal places).**  

---
### 🎯 **Planned Features**
🏗 Future enhancements might include:
- Customizable unit displays (e.g., different calendar systems)
- Potential Excel Add-In version
- Improved array support for multi-cell outputs

---

📢 **Want to contribute?** Feel free to report issues, suggest improvements, or share how you're using these functions! 🚀


> Written with [StackEdit](https://stackedit.io/).
