<div align="center">

# 🧮 Set 
## Sets, Representation of Sets &Types of Numbers

[![Math](https://img.shields.io/badge/Subject-Discrete%20Mathematics-purple?logo=mathworks)]()
[![Level](https://img.shields.io/badge/Level-Fundamental-blue)]()
[![Source](https://img.shields.io/badge/Source-KnowledgeGate.AI-green)]()

> *"Sets are the fundamental discrete structures on which all other discrete structures are built."*

</div>

---

## 📋 Table of Contents

- [📖 What is a SET?](#-what-is-a-set)
- [✏️ Notation & Symbols](#️-notation--symbols)
- [📋 Representation of Sets](#-representation-of-sets)
  - [1️⃣ Tabular / Roster Form](#1️⃣-tabular--roster-form)
  - [2️⃣ Set Builder Form](#2️⃣-set-builder-form)
- [🔢 Hierarchy of Numbers](#-hierarchy-of-numbers)
  - [🔹 Natural Numbers (ℕ)](#-natural-numbers-)
  - [🔹 Whole Numbers (𝕎)](#-whole-numbers-)
  - [🔹 Integers (ℤ)](#-integers-)
  - [🔹 Rational Numbers (ℚ)](#-rational-numbers-)
  - [🔹 Irrational Numbers](#-irrational-numbers)
  - [🔹 Real Numbers (ℝ)](#-real-numbers-)
  - [🔹 Complex Numbers (ℂ)](#-complex-numbers-)
- [🌳 Number Hierarchy Diagram](#-number-hierarchy-diagram)

---

## 📖 What is a SET?

A **Set** is formally defined as:

> **"An unordered, well-defined collection of distinct objects (called elements or members of a set) of the same type."**

The **type** is defined by the person defining the set.

### Key Properties

| Property | Description |
|----------|-------------|
| 🔀 **Unordered** | The arrangement of elements does not matter |
| ✅ **Well-defined** | It must be clear whether an object belongs to the set or not |
| 🎯 **Distinct** | No duplicate elements allowed |
| 📦 **Same Type** | All elements share a common property or type |

### Examples

```
A = {0, 2, 4, 6, ...}        → Set of even whole numbers
B = {1, 3, 5, ...}           → Set of odd natural numbers
C = {x | x is a Natural number} → Set of all natural numbers
```

---

## ✏️ Notation & Symbols

| Symbol | Meaning | Example |
|--------|---------|---------|
| $A, B, C$ | Capital letters denote **sets** | $A = \{1, 2, 3\}$ |
| $a, b, c, x, y$ | Lowercase letters denote **elements** | $x \in A$ |
| $\in$ | **"is an element of"** / "belongs to" | $x \in A$ |
| $\notin$ | **"is NOT an element of"** | $x \notin A$ |
| $\{\}$ | Set braces — enclose the elements | $\{a, e, i, o, u\}$ |
| $\ldots$ | Ellipsis — indicates continuation | $\{1, 2, 3, \ldots\}$ |
| $\mid$ or $:$ | "Such that" (in set-builder) | $\{x \mid x > 0\}$ |

> 💡 **Convention:** Sets are denoted by **capital letters**; elements by **lowercase letters**.

---

## 📋 Representation of Sets

There are **two primary ways** to represent a set:

---

### 1️⃣ Tabular / Roster Form

In this method, a set is defined by **actually listing all its members** inside curly braces.

#### Examples

| Set | Roster Form | Description |
|-----|-------------|-------------|
| $A$ | $\{a, e, i, o, u\}$ | Set of vowels in English |
| $B$ | $\{1, 2, 3, 4\}$ | First four natural numbers |
| $C$ | $\{\ldots, -4, -2, 0, 2, 4, \ldots\}$ | Set of even integers |

#### When to Use
- ✅ When the set has a **small, finite** number of elements
- ✅ When listing elements is **straightforward**

---

### 2️⃣ Set Builder Form

In this method, we specify the **property** or **condition** that the elements must satisfy.

#### General Structure

```
S = { x | criteria }
    ↑   ↑     ↑
    │   │     └── Condition for x to be in S
    │   └──────── "Such that"
    └──────────── Element in S
```

#### Examples

| Set | Set Builder Form | Description |
|-----|------------------|-------------|
| $A$ | $\{x \mid x \text{ is an odd positive number less than } 10\}$ | Odd positives $< 10$ |
| $A$ | $\{x \mid x \in \text{English alphabet} \land x \text{ is a vowel}\}$ | English vowels |
| $B$ | $\{x \mid x \in \mathbb{N} \land x < 5\}$ | Natural numbers less than 5 |
| $C$ | $\{x \mid x \in \mathbb{Z} \land x \% 2 = 0\}$ | Even integers |

#### When to Use
- ✅ When the set has **infinite** elements
- ✅ When the defining **property** is more important than listing
- ✅ When listing all elements is **impractical**

---

## 🔢 Hierarchy of Numbers

The number system is organized in a nested hierarchy, from the most basic to the most general:

```
                    ┌─────────────────┐
                    │    ℂ Complex    │  ← Most General
                    │    Numbers      │
                    └────────┬────────┘
                             │
              ┌──────────────┴──────────────┐
              │                             │
        ┌─────┴─────┐               ┌───────┴───────┐
        │  ℝ Real   │               │  Imaginary    │
        │  Numbers  │               │   Numbers     │
        └─────┬─────┘               └───────────────┘
              │
     ┌────────┴────────┐
     │                 │
┌────┴────┐      ┌─────┴──────┐
│ ℚ Rational│      │ Irrational │
│ Numbers  │      │  Numbers   │
└────┬────┘      └────────────┘
     │
┌────┴────┐
│  ℤ Integers  │
│              │
└────┬────┘
     │
┌────┴────┐
│ 𝕎 Whole │
│ Numbers │
└────┬────┘
     │
┌────┴────┐
│ ℕ Natural│
│ Numbers │
└─────────┘      ← Most Basic
```

---

### 🔹 Natural Numbers (ℕ)

> **Definition:** Numbers that occur commonly and obviously in nature.

$$\mathbb{N} = \{1, 2, 3, 4, \ldots, \infty\}$$

| Property | Value |
|----------|-------|
| Starts at | $1$ |
| Includes | All positive counting numbers |
| Excludes | Zero, negatives, fractions |

---

### 🔹 Whole Numbers (𝕎)

> **Definition:** The set of natural numbers **including zero**.

$$\mathbb{W} = \{0, 1, 2, 3, 4, \ldots\}$$

| Property | Value |
|----------|-------|
| Starts at | $0$ |
| Includes | Zero + all natural numbers |
| Excludes | Negative numbers, fractions |

```
Number Line:
←——┬——┬——┬——┬——┬——┬——┬——→
   0  1  2  3  4  5  6  7  8  9  10 ...
   ↑  └──────────────────────────────────→ Natural Numbers
   └────────────────────────────────────→ Whole Numbers
```

---

### 🔹 Integers (ℤ)

> **Definition:** Numbers that can be written **without a fractional component**.

$$\mathbb{Z} = \{\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots\}$$

| Subset | Definition | Example |
|--------|------------|---------|
| **Positive Integers** $\mathbb{Z}^+$ | $\{1, 2, 3, \ldots\}$ | $1, 5, 100$ |
| **Negative Integers** $\mathbb{Z}^-$ | $\{\ldots, -3, -2, -1\}$ | $-1, -5, -100$ |
| **Zero** | Neither positive nor negative | $0$ |

```
Number Line:
←——┬——┬——┬——┬——┬——┬——┬——┬——┬——┬——┬——┬——→
  -6 -5 -4 -3 -2 -1  0  1  2  3  4  5  6
  ←─────────────────│─────────────────→
     Negative       │      Positive
                    │
                   Zero
```

---

### 🔹 Rational Numbers (ℚ)

> **Definition:** Any number that can be expressed as a fraction $\frac{p}{q}$ of two integers, where $p$ is the numerator and $q \neq 0$ is the denominator.

$$\mathbb{Q} = \left\{ \frac{p}{q} \mid p, q \in \mathbb{Z}, q \neq 0 \right\}$$

#### Examples

| Number | Fraction Form | Type |
|--------|---------------|------|
| $\frac{7}{8}$ | $\frac{7}{8}$ | Proper fraction |
| $\frac{1}{3}$ | $\frac{1}{3}$ | Repeating decimal |
| $0.\overline{21}$ | $\frac{7}{33}$ | Repeating decimal |
| $0.97$ | $\frac{97}{100}$ | Terminating decimal |
| $-3$ | $\frac{-3}{1}$ | Integer (also rational) |
| $\sqrt{16}$ | $\frac{4}{1}$ | Perfect square |

> 🔑 **Key Property:** Rational numbers have decimal representations that **either terminate** or **repeat periodically**.

---

### 🔹 Irrational Numbers

> **Definition:** Real numbers that **cannot** be expressed as a fraction $\frac{p}{q}$ of two integers.

#### Characteristics
- ❌ Cannot be written as a simple fraction
- ❌ Decimal expansion **never terminates**
- ❌ Decimal expansion **never repeats**

#### Examples

| Symbol | Approximate Value | Description |
|--------|-------------------|-------------|
| $\sqrt{2}$ | $1.41421356\ldots$ | Square root of 2 |
| $\sqrt{8}$ | $2.82842712\ldots$ | Square root of 8 |
| $\pi$ | $3.14159265\ldots$ | Ratio of circumference to diameter |
| $e$ | $2.71828182\ldots$ | Euler's number |
| $\sqrt{11}$ | $3.31662479\ldots$ | Square root of 11 |
| $0.3030030003\ldots$ | — | Non-repeating, non-terminating pattern |

---

### 🔹 Real Numbers (ℝ)

> **Definition:** A value that represents a quantity along a **continuous line**, containing **all rational and all irrational numbers**.

$$\mathbb{R} = \mathbb{Q} \cup \{\text{Irrational Numbers}\}$$

#### Real Number Line

```
←——┬————┬————┬————┬————┬——┬——┬——┬——┬——┬——┬——┬——→
  -5  -4   -3   -2   -1  0  1  2  3  4  5
      ↓        ↓        ↓     ↓     ↓     ↓
    -4.25   -1.75    -1/2  1/2   1.5   π≈3.14
    -7/2                        e≈2.72
```

| Number Type | Examples |
|-------------|----------|
| **Rational** | $-4.25, -\frac{7}{2}, -1.75, -\frac{1}{2}, \frac{1}{2}, 1.5$ |
| **Irrational** | $\pi \approx 3.14, e \approx 2.72$ |

> 📌 **Real numbers fill the entire number line** — there are no "gaps."

---

### 🔹 Complex Numbers (ℂ)

> **Definition:** A number that can be expressed in the form $a + bi$, where $a$ and $b$ are **real numbers**, and $i$ is the **imaginary unit** satisfying $i^2 = -1$.

$$\mathbb{C} = \{a + bi \mid a, b \in \mathbb{R}, i^2 = -1\}$$

#### Components

| Component | Symbol | Description |
|-----------|--------|-------------|
| **Real Part** | $a$ | The real number component |
| **Imaginary Part** | $b$ | Coefficient of the imaginary unit |
| **Imaginary Unit** | $i$ | Defined by $i^2 = -1$ |

#### Examples

| Complex Number | Real Part ($a$) | Imaginary Part ($b$) |
|----------------|-----------------|----------------------|
| $3 + 2i$ | $3$ | $2$ |
| $-3 + 3.5i$ | $-3$ | $3.5$ |
| $1 - 4i$ | $1$ | $-4$ |
| $5$ | $5$ | $0$ (purely real) |
| $7i$ | $0$ | $7$ (purely imaginary) |

#### Complex Plane

```
        Im (Imaginary)
          ↑
       4i ┤
          │
    -3+3.5i ●──────┤ 3.5i
          │        │
       2i ┤───────● 3+2i
          │        │
       1i ┤        │
 ─────┼───┼───┼───┼───┼───┼───→ Re (Real)
     -4  -3  -2  -1   0   1   2   3   4
          │        │
      -1i ┤        │
          │        │
      -2i ┤        │
          │        │
      -3i ┤        │
          │        │
      -4i ┤───────● 1-4i
          │
```

---

## 🌳 Number Hierarchy Diagram

### Complete Subset Relationship

```
┌─────────────────────────────────────────────────────────────┐
│                      ℂ COMPLEX NUMBERS                       │
│              {a + bi | a, b ∈ ℝ, i² = -1}                   │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────┐    │
│  │                 ℝ REAL NUMBERS                       │    │
│  │     {All rational + All irrational numbers}          │    │
│  ├─────────────────────────────────────────────────────┤    │
│  │  ┌─────────────────────────────────────────────┐    │    │
│  │  │           ℚ RATIONAL NUMBERS                 │    │    │
│  │  │        {p/q | p,q ∈ ℤ, q ≠ 0}               │    │    │
│  │  ├─────────────────────────────────────────────┤    │    │
│  │  │  ┌─────────────────────────────────────┐    │    │    │
│  │  │  │         ℤ INTEGERS                   │    │    │    │
│  │  │  │    {..., -2, -1, 0, 1, 2, ...}      │    │    │    │
│  │  │  ├─────────────────────────────────────┤    │    │    │
│  │  │  │  ┌─────────────────────────────┐    │    │    │    │
│  │  │  │  │      𝕎 WHOLE NUMBERS         │    │    │    │    │
│  │  │  │  │       {0, 1, 2, 3, ...}      │    │    │    │    │
│  │  │  │  ├─────────────────────────────┤    │    │    │    │
│  │  │  │  │  ┌─────────────────────┐    │    │    │    │    │
│  │  │  │  │  │   ℕ NATURAL NUMBERS  │    │    │    │    │    │
│  │  │  │  │  │     {1, 2, 3, ...}   │    │    │    │    │    │
│  │  │  │  │  └─────────────────────┘    │    │    │    │    │
│  │  │  │  └─────────────────────────────┘    │    │    │    │
│  │  │  └─────────────────────────────────────┘    │    │    │
│  │  └─────────────────────────────────────────────┘    │    │
│  │  ┌─────────────────────────────────────────────┐    │    │
│  │  │      IRRATIONAL NUMBERS (ℝ - ℚ)              │    │    │
│  │  │   {√2, π, e, ...}  ── Non-repeating,        │    │    │
│  │  │        non-terminating decimals              │    │    │
│  │  └─────────────────────────────────────────────┘    │    │
│  └─────────────────────────────────────────────────────┘    │
│  ┌─────────────────────────────────────────────────────┐    │
│  │           IMAGINARY NUMBERS                          │    │
│  │        {bi | b ∈ ℝ, b ≠ 0, i² = -1}                 │    │
│  └─────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────┘
```

### Summary Table

| Set | Symbol | Definition | Examples |
|-----|--------|------------|----------|
| **Natural Numbers** | $\mathbb{N}$ | Counting numbers | $1, 2, 3, 100$ |
| **Whole Numbers** | $\mathbb{W}$ | Natural numbers + 0 | $0, 1, 2, 50$ |
| **Integers** | $\mathbb{Z}$ | Whole numbers + negatives | $-3, 0, 7$ |
| **Rational Numbers** | $\mathbb{Q}$ | Fractions of integers | $\frac{1}{2}, -3, 0.75$ |
| **Irrational Numbers** | $\mathbb{R} \setminus \mathbb{Q}$ | Non-fraction reals | $\sqrt{2}, \pi, e$ |
| **Real Numbers** | $\mathbb{R}$ | All rationals + irrationals | $-5, \frac{2}{3}, \pi$ |
| **Complex Numbers** | $\mathbb{C}$ | $a + bi$ form | $3+2i, -1-4i$ |

---

<div align="center">

## 🎯 Key Takeaways

| Concept | Remember |
|---------|----------|
| **Set** | Unordered, well-defined, distinct collection |
| **Roster Form** | List all elements: $\{1, 2, 3\}$ |
| **Set Builder** | Define by property: $\{x \mid x > 0\}$ |
| **ℕ ⊂ 𝕎 ⊂ ℤ ⊂ ℚ ⊂ ℝ ⊂ ℂ** | Each set is a subset of the next |
| **Irrational** | Fills the "gaps" that rationals leave on the number line |
| **Complex** | Most general — includes real and imaginary parts |

[🔝 Back to Top](#-set-theory)

</div>
