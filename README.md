# 💻 Decimal to Binary Converter
![status](https://img.shields.io/badge/status-Alpha-blue)

A **Java program** that converts any decimal number into its **binary representation**.  
Supports a wide range of inputs including:

- **Floating-point numbers** (small & large, e.g., `6.022e23`)  
- **Negative numbers** (e.g., `-13.625`)  
- **Fractions and mixed fractions** (e.g., `3 1/2` or `7/8`)  
- **Mathematical constants** (`pi`/`π`, `e`)  
- **Trigonometric functions** (`sin`, `cos`, `tan`, etc.)  
- **Logarithmic, exponential, and absolute functions** (`ln`, `log`, `exp`, `abs`)  
- **Square roots** (`√` or `sqrt`) and **factorials**  

This converter preserves the **true fractional binary expansion** for small values instead of rounding them to zero.

---

## 🧪 How It Works

1. **Expression Evaluation**  
   - Parses input strings to handle **operators** (`+`, `-`, `*`, `/`, `^`)  
   - Supports **implicit multiplication** (e.g., `2π` or `3(4)`)  
   - Evaluates **nested parentheses** and **functions**  

2. **Binary Conversion**  
   - Separates the **integer part** and the **fractional part**  
   - Converts the integer part to binary  
   - Converts the fractional part using repeated multiplication by 2  
   - Limits fractional conversion to **64 binary places** (configurable via `DECIMAL_PLACES_LIMIT`)  

3. **Edge Cases & Accuracy**  
   - Very small fractions are preserved (no automatic rounding to zero)  
   - Negative numbers are handled correctly  
   - Scientific notation (`e`) is supported  

---

## 📊 Output Example

```text
=====================================
|    Decimal to Binary Converter    |
=====================================
|       [Type 'STOP' to exit]       |
-------------------------------------

> Decimal: tan(π/4)
>> Binary: 0.1111111111111111111111111111111111111111111111111111100000000000

> Decimal: cos(π/2)
>> Binary: 0.0000000000000000000000000000000000000000000000000000010001101001

> Decimal: 6.022e23
>> Binary: 111111111111111111111111111111111111111111111111111111111111111.1111111111111111111111111111111111111111111111111111111111111111

> Decimal: -13.625
>> Binary: -1101.1010000000000000000000000000000000000000000000000000000000000000

> Decimal: sin(π/2)
>> Binary: 1
