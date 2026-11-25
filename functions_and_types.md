# Functions and Their Types

> A complete guide to **One-to-One**, **Onto**, and **Invertible** functions with definitions, diagrams, and solved examples.

---

## 📌 Table of Contents

- [1. What is a Function?](#1-what-is-a-function)
- [2. One-to-One Functions (Injective)](#2-one-to-one-functions-injective)
- [3. Onto Functions (Surjective)](#3-onto-functions-surjective)
- [4. Invertible Functions (Bijective)](#4-invertible-functions-bijective)
- [5. Quick Comparison Table](#5-quick-comparison-table)
- [6. Solved Examples](#6-solved-examples)

---

## 1. What is a Function?

A **function** `f : A → B` is a rule that assigns **every** element of set **A** (the *domain*) to **exactly one** element of set **B** (the *codomain*).

```
     A (Domain)          B (Codomain)
   ┌─────────┐        ┌─────────┐
   │    a    │ ─────→ │    1    │
   │    b    │ ──┐    │    2    │
   │    c    │ ──┼──→ │    3    │
   └─────────┘   └──→ │    4    │
                      └─────────┘
```

✅ **Valid function** — every input has exactly one output.
❌ **Not a function** — an input maps to two outputs, or an input has no output.

---

## 2. One-to-One Functions (Injective)

### Definition
A function `f : A → B` is **one-to-one (injective)** if **distinct elements of A have distinct images** in B.

> **f(a₁) = f(a₂)  ⟹  a₁ = a₂**

In other words: **no two different inputs give the same output.**

### Diagram — One-to-One

```
     A                   B
   ┌─────┐           ┌─────┐
   │  a  │ ────────→ │  1  │
   │  b  │ ────────→ │  2  │
   │  c  │ ────────→ │  3  │
   └─────┘           │  4  │   ← element with NO pre-image (allowed!)
                    └─────┘
```

### Diagram — NOT One-to-One

```
     A                   B
   ┌─────┐           ┌─────┐
   │  a  │ ──┐       │  1  │
   │  b  │ ──┼────→ │  2  │   ← two arrows land here ❌
   │  c  │ ──→      │  3  │
   └─────┘           └─────┘
```

### Algebraic Test
- **Horizontal Line Test (graphs):** every horizontal line cuts the graph **at most once**.
- Or show: if `f(x₁) = f(x₂)` leads to `x₁ = x₂`, the function is injective.

### Examples

| Function | Injective? | Reason |
|---|---|---|
| `f(x) = 2x + 3` (ℝ → ℝ) | ✅ Yes | Strictly increasing line |
| `f(x) = x²` (ℝ → ℝ) | ❌ No | `f(2) = f(-2) = 4` |
| `f(x) = x²` (ℝ⁺ ∪ {0} → ℝ) | ✅ Yes | Domain restricted to non-negatives |
| `f(x) = eˣ` (ℝ → ℝ) | ✅ Yes | Never repeats values |
| `f(x) = sin x` (ℝ → ℝ) | ❌ No | Periodic, repeats values |

**Proof that f(x) = 2x + 3 is one-to-one:**
```
Suppose f(x₁) = f(x₂)
   2x₁ + 3 = 2x₂ + 3
        x₁ = x₂   ✔  Hence injective.
```

---

## 3. Onto Functions (Surjective)

### Definition
A function `f : A → B` is **onto (surjective)** if **every element of B is the image of at least one element of A**.

> Range of f = Codomain B, i.e. **∀ b ∈ B, ∃ a ∈ A such that f(a) = b**

In other words: **every output in B gets "hit" — nothing is left over.**

### Diagram — Onto

```
     A                   B
   ┌─────┐           ┌─────┐
   │  a  │ ────────→ │  1  │
   │  b  │ ──┐       │  2  │
   │  c  │ ──┼────→ │  3  │
   │  d  │ ──┘      │  4  │ ← hit by some input
   └─────┘           └─────┘
        (sharing is fine — only "missing" is not)
```

### Diagram — NOT Onto

```
     A                   B
   ┌─────┐           ┌─────┐
   │  a  │ ────────→ │  1  │
   │  b  │ ────────→ │  2  │
   └─────┘           │  3  │   ← NO arrow reaches here ❌
                    └─────┘
```

### Examples

| Function | Onto? | Reason |
|---|---|---|
| `f(x) = 2x + 3` (ℝ → ℝ) | ✅ Yes | Solve 2x+3 = y → x = (y−3)/2 always exists |
| `f(x) = x²` (ℝ → ℝ) | ❌ No | Negative numbers have no pre-image |
| `f(x) = x²` (ℝ → ℝ⁺ ∪ {0}) | ✅ Yes | Every non-negative y has √y |
| `f(x) = eˣ` (ℝ → ℝ) | ❌ No | Range is (0, ∞), misses 0 and negatives |
| `f(x) = x³` (ℝ → ℝ) | ✅ Yes | Cube root exists for every real y |

**Proof that f(x) = 2x + 3 is onto (ℝ → ℝ):**
```
Let y ∈ ℝ be arbitrary. We need x with f(x) = y:
   2x + 3 = y   ⟹   x = (y − 3)/2
Since (y−3)/2 ∈ ℝ, every y has a pre-image. ✔ Hence surjective.
```

---

## 4. Invertible Functions (Bijective)

### Definition
A function `f : A → B` is **invertible** if there exists a function `g : B → A` such that:

> **g(f(a)) = a** for all a ∈ A, and **f(g(b)) = b** for all b ∈ B

`g` is written as **f⁻¹** (the inverse of f).

### Key Fact
> **f is invertible ⟺ f is BOTH one-to-one AND onto (bijective).**

- One-to-one guarantees the inverse is **well-defined** (no two inputs share an output — so the reverse rule is unambiguous).
- Onto guarantees the inverse is **defined everywhere on B** (every output has something to map back from).

### Diagram — Bijective (Invertible)

```
        f                     f⁻¹
   A ────────→ B         B ────────→ A
 ┌─────┐     ┌─────┐   ┌─────┐     ┌─────┐
 │  a  │ ──→ │  1  │   │  1  │ ──→ │  a  │
 │  b  │ ──→ │  2  │   │  2  │ ──→ │  b  │
 │  c  │ ──→ │  3  │   │  3  │ ──→ │  c  │
 └─────┘     └─────┘   └─────┘     └─────┘
 Perfect pairing — every arrow reverses cleanly!
```

### How to Find the Inverse (3 steps)

For `y = f(x)`:
1. **Swap** x and y →  `x = f(y)`
2. **Solve** for y
3. Write `y = f⁻¹(x)`

### Example 1 — Linear function
```
f(x) = 2x + 3

Step 1:  y = 2x + 3
Step 2:  swap:  x = 2y + 3
Step 3:  solve: y = (x − 3)/2

∴  f⁻¹(x) = (x − 3)/2

Check:  f(f⁻¹(x)) = 2·(x−3)/2 + 3 = x  ✔
        f⁻¹(f(x)) = (2x + 3 − 3)/2 = x  ✔
```

### Example 2 — Cube function
```
f(x) = x³  (ℝ → ℝ)

y = x³  ⟹  x = y³  ⟹  y = x^(1/3)

∴  f⁻¹(x) = ∛x
```

### ⚠️ Non-Example — Square function
```
f(x) = x²  (ℝ → ℝ)  is NOT invertible:
  • Not one-to-one: f(2) = f(−2) = 4
  • Not onto: −1 has no pre-image
If we restrict to f : ℝ⁺ ∪ {0} → ℝ⁺ ∪ {0}, then f⁻¹(x) = √x. ✔
```

---

## 5. Quick Comparison Table

| Type | Condition | Arrows rule | f(x) = x² on ℝ→ℝ | f(x) = 2x+3 on ℝ→ℝ |
|---|---|---|---|---|
| **One-to-One** (injective) | `f(a₁)=f(a₂) ⟹ a₁=a₂` | No merging ❌→❌ | ❌ No | ✅ Yes |
| **Onto** (surjective) | Range = Codomain | No element of B left out | ❌ No | ✅ Yes |
| **Invertible** (bijective) | One-to-one **AND** onto | Perfect pairing ↔ | ❌ No | ✅ Yes |

```
        ┌─────────────────────────────┐
        │      ALL FUNCTIONS A → B     │
        └──────────────┬──────────────┘
                       │
        ┌──────────────┴──────────────┐
        ▼                             ▼
  ┌───────────┐                ┌───────────┐
  │ ONE-TO-ONE│                │   ONTO    │
  │(injective)│                │(surjective)│
  └─────┬─────┘                └─────┬─────┘
        └───────────┬────────────────┘
                    ▼
          ┌───────────────────┐
          │   INVERTIBLE /    │
          │   BIJECTIVE       │
          │  (invertible ⇔    │
          │  injective + onto)│
          └───────────────────┘
```

---

## 6. Solved Examples

### Example 1 — Classify f : ℝ → ℝ, f(x) = 3x − 5
```
One-to-one:  f(x₁) = f(x₂) ⟹ 3x₁ − 5 = 3x₂ − 5 ⟹ x₁ = x₂ ✔
Onto:        For any y, x = (y + 5)/3 ∈ ℝ ✔
Conclusion:  Bijective ⟹ Invertible, and f⁻¹(x) = (x + 5)/3
```

### Example 2 — Classify f : ℝ → ℝ, f(x) = x² + 1
```
One-to-one:  f(1) = f(−1) = 2  ✘  Not injective
Onto:        x² + 1 ≥ 1, so y = 0 has no pre-image  ✘  Not surjective
Conclusion:  Neither ⟹ Not invertible
```

### Example 3 — Finite sets: f : {1,2,3} → {p,q,r}, f(1)=p, f(2)=r, f(3)=q
```
Every input has a unique output ✔ (it is a function)
All outputs distinct        ✔ One-to-one
Every element of B is hit   ✔ Onto
Conclusion: Bijective ⟹ Invertible: f⁻¹(p)=1, f⁻¹(q)=3, f⁻¹(r)=2
```

### Example 4 — Prove f : ℝ → ℝ, f(x) = (2x − 1)/(x + 2) is invertible and find f⁻¹
```
Step 1:  y = (2x − 1)/(x + 2)
Step 2:  x = (2y − 1)/(y + 2)
Step 3:  x(y + 2) = 2y − 1
         xy + 2x = 2y − 1
         xy − 2y = −2x − 1
         y(x − 2) = −(2x + 1)
         y = −(2x + 1)/(x − 2) = (2x + 1)/(2 − x)

∴  f⁻¹(x) = (2x + 1)/(2 − x),  x ≠ 2

Since a unique inverse exists, f is one-to-one and onto (bijective). ✔
```

---

## 📝 Summary

| Concept | One-line memory hook |
|---|---|
| **One-to-One** | "No two inputs share an output" — arrows **never merge** |
| **Onto** | "Every output gets hit" — **no element of B is lonely** |
| **Invertible** | "Perfect match" — **arrows reverse exactly** ⟺ injective + onto |

> 💡 **Golden Rule:** A function is invertible **if and only if** it is both one-to-one and onto.
