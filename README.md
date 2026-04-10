# 🏛️ LeetCode 12: Integer to Roman (C++)

A clean and efficient implementation to convert an integer to its Roman numeral representation using a greedy approach.

## 📖 Problem Description
Roman numerals are represented by seven different symbols: `I`, `V`, `X`, `L`, `C`, `D` and `M`. Given an integer, convert it to a Roman numeral.

### Example
- **Input:** `num = 1994`
- **Output:** `"MCMXCIV"`
- **Explanation:** M = 1000, CM = 900, XC = 90 and IV = 4.

## 🛠️ Technical Approach
This solution uses a **Greedy Strategy** based on a pre-defined mapping:
1. **Symbol Mapping:** We store Roman numeral values (including subtractive cases like `IV`, `IX`, `XL`, etc.) and their corresponding symbols in descending order.
2. **Iterative Extraction:** Starting from the largest value (1000):
   - While the current number `num` is greater than or equal to the current Roman value, we append the symbol to our result string.
   - We subtract the value from `num` and repeat.
3. **Efficiency:** By handling the "subtractive" cases (like 4 and 900) as distinct symbols in the list, we avoid complex conditional logic.

## 📊 Complexity Analysis
- **Time Complexity:** $O(1)$ — Since the input range is limited (up to 3999) and the number of Roman symbols is fixed, the loop runs a constant maximum number of times.
- **Space Complexity:** $O(1)$ — The amount of extra space used for the mapping arrays and result string is bounded by the constraints.

## 💡 Key Edge Cases Handled
- **Subtractive Combinations:** Correctly handles 4 (`IV`), 9 (`IX`), 40 (`XL`), 90 (`XC`), 400 (`CD`), and 900 (`CM`).
- **Maximum Value:** Efficiently processes numbers up to 3999.
- **Single Digits:** Correctly converts small integers like 1, 2, or 3.
