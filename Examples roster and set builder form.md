# Roster Form and Set-Builder Form

## 📘 Description

In set theory, a set can be represented in different ways. Two commonly used methods are **Roster Form** and **Set-Builder Form**.

- **Roster Form:** Lists all the elements of a set explicitly inside curly brackets `{ }`.
- **Set-Builder Form:** Describes a set by specifying a common property or rule that all its elements satisfy.

Understanding both forms helps students represent mathematical sets clearly and convert between different representations.

---

## 🎯 Learning Objectives

After studying this topic, students should be able to:

- Understand the concept of a set.
- Represent sets using **Roster Form**.
- Represent sets using **Set-Builder Form**.
- Convert a set from Roster Form to Set-Builder Form.
- Convert a set from Set-Builder Form to Roster Form.
- Identify the common property of elements in a set.

---

## 1. Roster Form

### Definition

In **Roster Form**, all the elements of a set are listed explicitly inside curly brackets.

### General Form

```text
A = {a₁, a₂, a₃, ..., aₙ}
```

### Example

```text
A = {1, 2, 3, 4, 5}
```

Here, the elements of set `A` are explicitly listed.

---

## 2. Set-Builder Form

### Definition

In **Set-Builder Form**, a set is described using a variable and a condition or property that its elements satisfy.

### General Form

```text
A = {x : P(x)}
```

or

```text
A = {x | P(x)}
```

where `P(x)` represents the condition or property satisfied by `x`.

### Example

```text
A = {x ∈ ℕ : 1 ≤ x ≤ 5}
```

This represents:

```text
A = {1, 2, 3, 4, 5}
```

---

# 🔄 Examples of Roster and Set-Builder Forms

| No. | Roster Form | Set-Builder Form |
|:---:|---|---|
| **1** | `A = {1, 2, 3, 4, 5}` | `A = {x ∈ ℕ : 1 ≤ x ≤ 5}` |
| **2** | `B = {2, 4, 6, 8, 10}` | `B = {x ∈ ℕ : x is even and x ≤ 10}` |
| **3** | `C = {1, 3, 5, 7, 9}` | `C = {x ∈ ℕ : x is odd and x < 10}` |
| **4** | `D = {5, 10, 15, 20, 25}` | `D = {x ∈ ℕ : x is a multiple of 5 and x ≤ 25}` |
| **5** | `E = {1, 4, 9, 16, 25}` | `E = {x : x = n², n ∈ ℕ, 1 ≤ n ≤ 5}` |
| **6** | `F = {2, 3, 5, 7, 11}` | `F = {x ∈ ℕ : x is prime and x < 12}` |
| **7** | `G = {10, 20, 30, 40, 50}` | `G = {x ∈ ℕ : x = 10n, 1 ≤ n ≤ 5}` |
| **8** | `H = {3, 6, 9, 12, 15}` | `H = {x ∈ ℕ : x is divisible by 3 and x ≤ 15}` |
| **9** | `I = {1, 2, 4, 8, 16, 32}` | `I = {x : x = 2ⁿ, n ∈ ℕ₀, 0 ≤ n ≤ 5}` |
| **10** | `J = {-3, -2, -1, 0, 1, 2, 3}` | `J = {x ∈ ℤ : -3 ≤ x ≤ 3}` |

---

# 🧩 Detailed Examples

## Example 1: Natural Numbers

### Roster Form

```text
A = {1, 2, 3, 4, 5}
```

### Set-Builder Form

```text
A = {x ∈ ℕ : 1 ≤ x ≤ 5}
```

**Explanation:** The set contains all natural numbers from `1` to `5`.

---

## Example 2: Even Numbers

### Roster Form

```text
B = {2, 4, 6, 8, 10}
```

### Set-Builder Form

```text
B = {x ∈ ℕ : x is even and x ≤ 10}
```

**Explanation:** Every element of the set is an even natural number not greater than `10`.

---

## Example 3: Odd Numbers

### Roster Form

```text
C = {1, 3, 5, 7, 9}
```

### Set-Builder Form

```text
C = {x ∈ ℕ : x is odd and x < 10}
```

**Explanation:** The set contains all odd natural numbers less than `10`.

---

## Example 4: Multiples of 5

### Roster Form

```text
D = {5, 10, 15, 20, 25}
```

### Set-Builder Form

```text
D = {x ∈ ℕ : x = 5n, 1 ≤ n ≤ 5}
```

**Explanation:** Each element is obtained by multiplying `5` by a natural number from `1` to `5`.

---

## Example 5: Perfect Squares

### Roster Form

```text
E = {1, 4, 9, 16, 25}
```

### Set-Builder Form

```text
E = {x : x = n², n ∈ ℕ, 1 ≤ n ≤ 5}
```

**Explanation:**

```text
1² = 1
2² = 4
3² = 9
4² = 16
5² = 25
```

Therefore:

```text
E = {1, 4, 9, 16, 25}
```

---

# 🔢 Common Number Sets

| Symbol | Meaning | Examples |
|---|---|---|
| `ℕ` | Natural Numbers | `{1, 2, 3, ...}` |
| `ℕ₀` | Non-negative Integers | `{0, 1, 2, 3, ...}` |
| `ℤ` | Integers | `{..., -2, -1, 0, 1, 2, ...}` |
| `ℚ` | Rational Numbers | `{1/2, 2/3, -4, ...}` |
| `ℝ` | Real Numbers | All rational and irrational numbers |

> **Note:** The definition of `ℕ` can vary by textbook. Some texts include `0` in the natural numbers, while others begin with `1`.

---

# 🔁 Conversion Between the Two Forms

## Roster Form → Set-Builder Form

### Steps

1. List the elements of the set.
2. Identify the common property among the elements.
3. Express that property using a variable and mathematical condition.

### Example

```text
A = {2, 4, 6, 8, 10}
```

All elements are even numbers.

Therefore:

```text
A = {x ∈ ℕ : x is even and x ≤ 10}
```

---

## Set-Builder Form → Roster Form

### Steps

1. Read the condition given in the set-builder form.
2. Determine the values satisfying the condition.
3. List those values inside curly brackets.

### Example

Given:

```text
B = {x ∈ ℕ : x < 6}
```

The natural numbers satisfying the condition are:

```text
1, 2, 3, 4, 5
```

Therefore:

```text
B = {1, 2, 3, 4, 5}
```

---

# 📝 Practice Questions

Convert the following sets into the other form.

1. `A = {2, 4, 6, 8, 10, 12}`
2. `B = {1, 4, 9, 16, 25}`
3. `C = {5, 10, 15, 20, 25, 30}`
4. `D = {-2, -1, 0, 1, 2}`
5. `E = {3, 6, 9, 12, 15}`
6. `F = {2, 3, 5, 7, 11, 13}`
7. `G = {10, 20, 30, 40}`
8. `H = {1, 3, 5, 7, 9, 11}`
9. `I = {0, 1, 4, 9, 16}`
10. `J = {-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5}`

---

# 💡 Key Takeaways

- **Roster Form** explicitly lists every element.
- **Set-Builder Form** describes elements using a common property.
- Curly brackets `{ }` are used in both forms.
- The symbol `:` or `|` means **"such that."**
- Always specify the appropriate number system, such as `ℕ`, `ℤ`, or `ℝ`, when necessary.

---

## 📚 Quick Reference

```text
Roster Form:
A = {a₁, a₂, a₃, ..., aₙ}

Set-Builder Form:
A = {x ∈ U : P(x)}
```

### Example

```text
Roster Form:
A = {2, 4, 6, 8, 10}

Set-Builder Form:
A = {x ∈ ℕ : x is even and x ≤ 10}
```

> **In short:**  
> **Roster Form = List the elements**  
> **Set-Builder Form = Describe the rule**
