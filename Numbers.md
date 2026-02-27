### List of **equations (formulae)** to calculate the **sum of numbers** under different conditions:

---

### 🧮 1. **Sum of First *n* Natural Numbers**

$$
S = \frac{n(n + 1)}{2}
$$

> e.g. $1 + 2 + 3 + ... + n$

---

### 🧮 2. **Sum of First *n* Odd Numbers**

$$
S = n^2
$$

> e.g. $1 + 3 + 5 + ...$ (n terms)

---

### 🧮 3. **Sum of First *n* Even Numbers**

$$
S = n(n + 1)
$$

> e.g. $2 + 4 + 6 + ...$ (n terms)

---

### 🧮 4. **Sum of Squares of First *n* Natural Numbers**

$$
S = \frac{n(n + 1)(2n + 1)}{6}
$$

---

### 🧮 5. **Sum of Cubes of First *n* Natural Numbers**

$$
S = \left( \frac{n(n + 1)}{2} \right)^2
$$

---

### 🧮 6. **Sum of Arithmetic Progression (AP)**

If the first term is $a$, common difference is $d$, number of terms is $n$:

$$
S = \frac{n}{2}[2a + (n - 1)d]
$$

OR

$$
S = \frac{n}{2}(a + l) \quad \text{where } l = \text{last term}
$$

---

### 🧮 7. **Sum of Geometric Progression (GP)**

If the first term is $a$, common ratio is $r$, number of terms is $n$:

* If $r \neq 1$:

$$
S = a \cdot \frac{1 - r^n}{1 - r}
$$

* If $r = 1$:

$$
S = a \cdot n
$$

---

### 🧮 8. **Sum of Digits of a Number**

No fixed formula; you loop through the digits:

$$
\text{Example (Python): } \sum = \sum_{i=1}^{k} \text{int}(digit_i)
$$

## 🔢 Sum Formulas (Basic & Series)

| Type                     | Formula                           | Example                                   |
| ------------------------ | --------------------------------- | ----------------------------------------- |
| Natural numbers          | $\frac{n(n+1)}{2}$                | 1+2+3+...+10 = 55                         |
| Odd numbers (first *n*)  | $n^2$                             | 1+3+5+7+9 = 25                            |
| Even numbers (first *n*) | $n(n+1)$                          | 2+4+6+8+10 = 30                           |
| Squares                  | $\frac{n(n+1)(2n+1)}{6}$          | 1²+2²+...+5² = 55                         |
| Cubes                    | $\left(\frac{n(n+1)}{2}\right)^2$ | 1³+2³+3³ = 36                             |
| AP                       | $\frac{n}{2}(2a + (n - 1)d)$      | a = 1, d = 3, n = 4 → sum = 1+4+7+10 = 22 |
| GP                       | $a \cdot \frac{1 - r^n}{1 - r}$   | a = 2, r = 3, n = 3 → 2+6+18 = 26         |

---

## 🔍 Special Number Types

### ⭐ 9. Armstrong Number (Narcissistic Number)

> A number equal to the **sum of its digits each raised to the power of the number of digits**.

* **Formula**:

$$
\text{If } n = d_1^k + d_2^k + ... + d_k^k \text{ then it's Armstrong}
$$

* Example: 153 → $1^3 + 5^3 + 3^3 = 153$

---

### 😊 10. Happy Number

> A number which eventually reaches 1 when replaced by the **sum of squares of its digits**, repeatedly.

* **Process**:
  Keep replacing the number with the **sum of the squares** of its digits until:

  * You reach **1** (Happy)
  * Or it loops endlessly (Unhappy)

* Example: 19 → $1^2 + 9^2 = 82 → 8^2 + 2^2 = 68 → ... → 1$

---

### 💯 11. Perfect Number

> A number equal to the **sum of its proper divisors** (excluding itself).

* Example: 28 → 1 + 2 + 4 + 7 + 14 = 28

---

### 🔁 12. Palindrome Number

> A number that reads the **same forward and backward**.

* Example: 121, 1331

---

### 🔄 13. Harshad Number (Niven Number)

> A number divisible by the **sum of its digits**.

* Example: 18 → 1 + 8 = 9 → 18 % 9 = 0 ✔️

---

### 🧠 14. Strong Number

> A number equal to the **sum of factorials of its digits**.

* Example: 145 → $1! + 4! + 5! = 145$

---

### 🧮 15. Automorphic Number

> A number whose **square ends in the same digits** as the number itself.

* Example: 76 → $76^2 = 5776$ → ends in 76 ✔️

---

### 🧊16. Kaprekar Number

> A number where square of the number can be split into two parts that add up to the number itself.

* Example: 45 → $45^2 = 2025$, $20 + 25 = 45$

