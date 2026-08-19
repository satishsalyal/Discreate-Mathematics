<div align="center">

# 📐 Discrete Mathematics: Sets and Elements

## A Comprehensive Lecture on Set Theory Fundamentals

[![Mathematics](https://img.shields.io/badge/Discrete%20Mathematics-1E88E5?logo=mathworks&logoColor=white&style=for-the-badge)]()
[![Set Theory](https://img.shields.io/badge/Set%20Theory-FF6F00?style=for-the-badge)]()
[![Logic](https://img.shields.io/badge/Mathematical%20Logic-8E44AD?style=for-the-badge)]()

</div>

---

## 📑 Table of Contents

1. [Introduction to Discrete Mathematics](#1-introduction-to-discrete-mathematics)
2. [Sets and Elements](#2-sets-and-elements)
3. [Mathematical Definition of a Set](#3-mathematical-definition-of-a-set)
4. [Key Characteristics of Sets](#4-key-characteristics-of-sets)
5. [Universal Set](#5-universal-set)
6. [Finite Sets](#6-finite-sets)
7. [Infinite Sets](#7-infinite-sets)
8. [Empty Set (Null Set)](#8-empty-set-null-set)
9. [Subsets](#9-subsets)
10. [Set Operations Overview](#10-set-operations-overview)
11. [Practice Problems](#11-practice-problems)
12. [Summary](#12-summary)

---

## 1. Introduction to Discrete Mathematics

### What is Discrete Mathematics?

> **Discrete Mathematics** is the branch of mathematics dealing with objects that can assume only distinct, separated values. It is the mathematical foundation of computer science, logic, and digital systems.

Unlike **continuous mathematics** (calculus, geometry) which deals with smooth, unbroken quantities, discrete mathematics focuses on **countable, distinct, and separate** objects.

### Why Study Discrete Mathematics?

| Field | Application of Discrete Math |
|-------|------------------------------|
| 💻 **Computer Science** | Algorithms, data structures, complexity theory |
| 🔐 **Cryptography** | Encryption, security protocols |
| 🤖 **Artificial Intelligence** | Logic, graph theory, decision trees |
| 🗄️ **Database Systems** | Relational algebra, query optimization |
| 🌐 **Networking** | Graph theory, routing algorithms |
| 🧮 **Digital Logic** | Boolean algebra, circuit design |
| 📊 **Data Science** | Combinatorics, probability, statistics |
| 🎮 **Game Development** | Graph algorithms, pathfinding |

### Core Topics in Discrete Mathematics

```
Discrete Mathematics
├── Set Theory
├── Logic & Propositional Calculus
├── Relations & Functions
├── Combinatorics & Counting
├── Graph Theory
├── Number Theory
├── Boolean Algebra
└── Algebraic Structures
```

### Discrete vs. Continuous

| Aspect | Discrete Mathematics | Continuous Mathematics |
|--------|----------------------|------------------------|
| **Values** | Distinct, separate | Continuous range |
| **Examples** | Integers, sets, graphs | Real numbers, curves |
| **Tools** | Logic, counting, graphs | Calculus, limits |
| **Applications** | CS, AI, cryptography | Physics, engineering |
| **Nature** | Countable | Uncountable |

---

## 2. Sets and Elements

### What is a Set?

A **set** is a well-defined collection of distinct objects, considered as an object in its own right. The objects in a set are called **elements** or **members** of the set.

> 💡 **Intuitive Definition:** A set is like a "bag" or "container" that holds distinct objects. The order of objects does not matter, and duplicates are not allowed.

### Examples of Sets in Daily Life

| Set Name | Elements |
|----------|----------|
| **Days of the week** | {Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday} |
| **Vowels in English** | {a, e, i, o, u} |
| **Prime numbers less than 10** | {2, 3, 5, 7} |
| **Colors of a rainbow** | {Red, Orange, Yellow, Green, Blue, Indigo, Violet} |
| **Binary digits** | {0, 1} |

### Notation

| Symbol | Meaning | Example |
|--------|---------|---------|
| `{}` | Denotes a set | `A = {1, 2, 3}` |
| `∈` | "is an element of" | `2 ∈ {1, 2, 3}` |
| `∉` | "is NOT an element of" | `4 ∉ {1, 2, 3}` |
| `\|` or `:` | "such that" | `{x \| x > 5}` |
| `n(A)` or `\|A\|` | Cardinality (number of elements) | `\|{1, 2, 3}\| = 3` |

### Examples of Element Membership

```python
# In Python, sets are represented using curly braces or set()
A = {1, 2, 3, 4, 5}

print(3 in A)       # True  ->  3 ∈ A
print(7 in A)       # False ->  7 ∉ A
print(2 not in A)   # False ->  2 ∉ A is False, so 2 ∈ A
print(len(A))       # 5     ->  |A| = 5
```

### Representing Sets

#### 1. Roster Method (Tabular Form)
Listing all elements inside curly braces, separated by commas.

```
A = {1, 2, 3, 4, 5}
B = {a, e, i, o, u}
C = {red, green, blue}
```

#### 2. Set-Builder Notation (Rule Method)
Describing the property that all elements satisfy.

```
A = {x | x is a natural number less than 6}
  = {x ∈ N | x < 6}
  = {1, 2, 3, 4, 5}

B = {x | x is an even integer between 1 and 10}
  = {x ∈ Z | 1 < x < 10 and x is even}
  = {2, 4, 6, 8}
```

#### 3. Venn Diagrams
Visual representation using overlapping circles.

```
    +---------------------+
    |    Universal Set U  |
    |                     |
    |    +-----+          |
    |    |  A  |          |
    |    | 1,2 |          |
    |    | 3,4 |          |
    |    +-----+          |
    |                     |
    +---------------------+
```

---

## 3. Mathematical Definition of a Set

### Formal Definition

> A **set** is an unordered collection of distinct objects, called **elements** or **members**, in which each element occurs exactly once.

### Axiomatic Definition (Zermelo-Fraenkel Set Theory)

In formal mathematics, sets are defined axiomatically. The **Zermelo-Fraenkel (ZF)** axioms provide the foundation:

| Axiom | Description |
|-------|-------------|
| **Extensionality** | Two sets are equal if they have the same elements |
| **Empty Set** | There exists a set with no elements |
| **Pairing** | For any two sets, there exists a set containing both |
| **Union** | The union of any collection of sets is a set |
| **Power Set** | The set of all subsets of a set is a set |
| **Infinity** | There exists an infinite set |
| **Separation** | A subset defined by a property is a set |
| **Replacement** | The image of a set under a function is a set |

### Georg Cantor's Definition (1874)

> *"A set is a gathering together into a whole of definite, distinct objects of our perception or of our thought — which are called elements of the set."*
>
> — **Georg Cantor**, Founder of Set Theory

### Key Properties from the Definition

```
1. WELL-DEFINED: Every object is either in the set or not (no ambiguity)
2. DISTINCT: No duplicate elements allowed
3. UNORDERED: {1, 2, 3} = {3, 2, 1} = {2, 1, 3}
4. UNIQUE MEMBERSHIP: Each element appears exactly once
```

### Well-Defined vs. Not Well-Defined

| Well-Defined Set | NOT Well-Defined |
|------------------|------------------|
| Set of even numbers | Set of "good" students |
| Set of prime numbers < 20 | Set of "tall" people |
| Set of vowels in English | Set of "beautiful" paintings |
| Set of binary digits {0, 1} | Set of "difficult" problems |

> ⚠️ A set must be **well-defined**: given any object, we must be able to determine definitively whether it belongs to the set or not.

---

## 4. Key Characteristics of Sets

### Characteristic 1: Unordered Collection

The order of elements in a set does **not** matter.

```
{1, 2, 3} = {3, 2, 1} = {2, 1, 3} = {1, 3, 2}
```

All of the above represent the **same set**.

```python
A = {1, 2, 3}
B = {3, 2, 1}
print(A == B)   # True - order does not matter
```

### Characteristic 2: Distinct Elements (No Duplicates)

A set cannot contain duplicate elements. If duplicates are listed, they are considered as a single element.

```
{1, 2, 2, 3, 3, 3} = {1, 2, 3}
```

```python
A = {1, 2, 2, 3, 3, 3}
print(A)        # {1, 2, 3}
print(len(A))   # 3
```

### Characteristic 3: Well-Defined Membership

For any given object, it must be possible to determine definitively whether it is a member of the set.

```
Set A = {x | x is an even number}

Is 4 ∈ A?  -> YES (4 is even)
Is 7 ∈ A?  -> NO  (7 is odd)
Is -2 ∈ A? -> YES (-2 is even)
```

### Characteristic 4: Elements Can Be of Any Type

Elements of a set can be numbers, letters, objects, or even other sets.

```python
# Mixed types
A = {1, "hello", 3.14, True}

# Set of sets (in Python, use frozenset for nested sets)
B = {frozenset({1, 2}), frozenset({3, 4})}
```

### Characteristic 5: Sets Can Be Finite or Infinite

| Type | Description | Example |
|------|-------------|---------|
| **Finite** | Countable number of elements | {1, 2, 3, 4, 5} |
| **Infinite** | Uncountable number of elements | Set of all natural numbers |

### Summary Table of Characteristics

| Characteristic | Description | Symbol/Example |
|----------------|-------------|----------------|
| **Unordered** | Order of elements irrelevant | {1,2,3} = {3,2,1} |
| **Distinct** | No duplicates allowed | {1,2,2} = {1,2} |
| **Well-defined** | Clear membership criteria | x ∈ A or x ∉ A |
| **Heterogeneous** | Any type of elements | {1, "a", 3.5} |
| **Finite/Infinite** | Can have any cardinality | |A| = n or ∞ |

---

## 5. Universal Set

### Definition

> The **Universal Set**, denoted by **U** (or sometimes **ξ**), is the set of all elements under consideration for a particular discussion or problem. It serves as the "universe" or "background" within which all other sets are defined.

### Key Points

- The universal set contains **all possible elements** relevant to the context.
- Every set being discussed is a **subset** of the universal set.
- The choice of universal set depends on the **context** of the problem.
- There is **no absolute universal set** — it is always relative to the discussion.

### Examples of Universal Sets

| Context | Universal Set U | Subsets |
|---------|-----------------|---------|
| Studying vowels | U = {a, b, c, d, e, ..., z} | V = {a, e, i, o, u} |
| Studying primes < 20 | U = {1, 2, 3, ..., 20} | P = {2, 3, 5, 7, 11, 13, 17, 19} |
| Binary operations | U = {0, 1} | A = {0}, B = {1} |
| Student grades | U = {A, B, C, D, F} | Pass = {A, B, C, D} |
| Days of the week | U = {Mon, Tue, Wed, Thu, Fri, Sat, Sun} | Weekend = {Sat, Sun} |

### Venn Diagram Representation

```
        +-----------------------------+
        |           U                 |
        |    (Universal Set)          |
        |                             |
        |    +----------+             |
        |    |    A     |             |
        |    |   +--+   |   +-----+   |
        |    |   |A∩B|  |   |  B  |   |
        |    |   +--+   |   +-----+   |
        |    +----------+             |
        |                             |
        |    (Elements outside        |
        |     A and B but in U)      |
        |                             |
        +-----------------------------+
```

### Formal Properties

```
For any set A under discussion:
  A ⊆ U    (A is a subset of the universal set)
  A ∪ U = U    (Union with U gives U)
  A ∩ U = A    (Intersection with U gives A)
  A' = U - A    (Complement of A is relative to U)
```

### Python Example

```python
# Define universal set and subsets
U = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
A = {2, 4, 6, 8}
B = {1, 3, 5, 7, 9}

print("A is subset of U:", A.issubset(U))   # True
print("B is subset of U:", B.issubset(U))   # True
print("A union U:", A | U)                   # {1,2,3,4,5,6,7,8,9,10} = U
print("A intersection U:", A & U)            # {2,4,6,8} = A
print("Complement of A:", U - A)             # {1,3,5,7,9,10}
```

---

## 6. Finite Sets

### Definition

> A **finite set** is a set that contains a **countable** (limited) number of elements. The number of elements in a finite set is called its **cardinality** or **order**, denoted by **n(A)** or **|A|**.

### Characteristics

- Has a definite, countable number of elements.
- The counting process **terminates**.
- Can be listed completely using the roster method.
- Cardinality is a **non-negative integer**.

### Examples of Finite Sets

| Set | Elements | Cardinality |
|-----|----------|-------------|
| A = {1, 2, 3} | 1, 2, 3 | n(A) = 3 |
| B = {a, e, i, o, u} | a, e, i, o, u | n(B) = 5 |
| C = {red, green, blue} | red, green, blue | n(C) = 3 |
| D = {x ∈ N | x < 100} | 1, 2, ..., 99 | n(D) = 99 |
| E = {days in a week} | Mon, Tue, ..., Sun | n(E) = 7 |
| F = ∅ (empty set) | none | n(F) = 0 |

### Cardinality Formula

For a finite set A:
```
n(A) = number of distinct elements in A
```

### Counting Principle

If A and B are finite sets:
```
n(A ∪ B) = n(A) + n(B) - n(A ∩ B)
```

This is the **Inclusion-Exclusion Principle** for two sets.

### Python Examples

```python
# Finite sets
A = {1, 2, 3, 4, 5}
B = {"apple", "banana", "cherry"}
C = set()  # Empty set

print(f"Set A: {A}")
print(f"Cardinality of A: {len(A)}")
print(f"Set B: {B}")
print(f"Cardinality of B: {len(B)}")
print(f"Set C (empty): {C}")
print(f"Cardinality of C: {len(C)}")

# Checking if a set is finite
def is_finite(s):
    try:
        len(s)
        return True
    except TypeError:
        return False

print(f"Is A finite? {is_finite(A)}")  # True
```

### Visual Representation

```
Finite Set A = {1, 2, 3, 4, 5}

    +-----+
    |  1  |
    |  2  |
    |  3  |
    |  4  |
    |  5  |
    +-----+
    n(A) = 5
```

---

## 7. Infinite Sets

### Definition

> An **infinite set** is a set that contains an **uncountable** or **unlimited** number of elements. The counting process **never terminates** — no matter how many elements you count, there are always more.

### Characteristics

- Has an unlimited number of elements.
- The counting process **never ends**.
- Cannot be completely listed using the roster method.
- Cardinality is **infinite** (∞ or ℵ₀ for countably infinite).

### Types of Infinite Sets

| Type | Description | Example | Cardinality |
|------|-------------|---------|-------------|
| **Countably Infinite** | Elements can be put in one-to-one correspondence with natural numbers | ℕ = {1, 2, 3, ...} | ℵ₀ (aleph-null) |
| **Uncountably Infinite** | Cannot be put in one-to-one correspondence with natural numbers | ℝ = set of real numbers | 𝔠 (continuum) |

### Examples of Infinite Sets

| Set | Description | Notation |
|-----|-------------|----------|
| **Natural Numbers** | {1, 2, 3, 4, 5, ...} | ℕ |
| **Whole Numbers** | {0, 1, 2, 3, 4, ...} | 𝕎 |
| **Integers** | {..., -2, -1, 0, 1, 2, ...} | ℤ |
| **Rational Numbers** | {p/q | p, q ∈ ℤ, q ≠ 0} | ℚ |
| **Real Numbers** | All numbers on the number line | ℝ |
| **Even Numbers** | {2, 4, 6, 8, 10, ...} | 2ℕ |
| **Prime Numbers** | {2, 3, 5, 7, 11, 13, ...} | ℙ |
| **Multiples of 5** | {5, 10, 15, 20, 25, ...} | 5ℕ |

### Set-Builder Notation for Infinite Sets

```
ℕ = {x | x is a natural number}
  = {1, 2, 3, 4, 5, ...}

ℤ = {x | x is an integer}
  = {..., -3, -2, -1, 0, 1, 2, 3, ...}

ℚ = {p/q | p, q ∈ ℤ and q ≠ 0}
  = {..., -1/2, 0, 1/2, 1, 3/2, ...}
```

### Countably vs. Uncountably Infinite

```
Countably Infinite (ℵ₀):
  - Can be "listed" or "counted" (even if the list never ends)
  - Examples: ℕ, ℤ, ℚ
  - There exists a bijection with ℕ

Uncountably Infinite (𝔠):
  - Cannot be listed or counted
  - Examples: ℝ, interval [0, 1]
  - No bijection with ℕ exists
  - 𝔠 > ℵ₀ (Cantor's Theorem)
```

### Visual Representation

```
Infinite Set ℕ = {1, 2, 3, 4, 5, ...}

    +-----+  +-----+  +-----+  +-----+  +-----+  ...
    |  1  |  |  2  |  |  3  |  |  4  |  |  5  |  ...
    +-----+  +-----+  +-----+  +-----+  +-----+  ...
    n(ℕ) = ∞ (never ends)
```

### Python Note

```python
# Python sets are always finite in practice
# But we can represent infinite sets conceptually using generators

def natural_numbers():
    """Generator for natural numbers (infinite)"""
    n = 1
    while True:
        yield n
        n += 1

# Get first 10 natural numbers
nat = natural_numbers()
first_10 = [next(nat) for _ in range(10)]
print(first_10)  # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

---

## 8. Empty Set (Null Set)

### Definition

> The **Empty Set** (also called the **Null Set** or **Void Set**), denoted by **∅** (empty set symbol) or **{}**, is the unique set that contains **no elements** at all.

### Key Properties

- It is the **only set** with cardinality **zero**: n(∅) = 0
- It is a **subset of every set**: ∅ ⊆ A for any set A
- The empty set is **unique**: there is only one empty set
- It is **not the same** as {∅} (a set containing the empty set)

### Notation

```
∅ = {} = {x | x ≠ x}  (set of all x such that x is not equal to itself)
```

### Examples of Empty Sets

| Description | Set Notation |
|-------------|--------------|
| Set of natural numbers less than 1 | {x ∈ ℕ | x < 1} = ∅ |
| Set of odd numbers divisible by 2 | {x ∈ odd numbers | x % 2 = 0} = ∅ |
| Set of living dinosaurs | {x | x is a living dinosaur} = ∅ |
| Set of squares with 5 sides | {x | x is a square with 5 sides} = ∅ |
| Intersection of even and odd numbers | Even ∩ Odd = ∅ |

### Important Distinctions

```
∅      = {}          -> Empty set (contains nothing)
{∅}    = {{}}        -> Set containing the empty set (contains 1 element)
{0}    = {0}         -> Set containing the number 0 (contains 1 element)

n(∅)   = 0
n({∅}) = 1
n({0}) = 1
```

### Formal Properties

```
For any set A:
  ∅ ⊆ A          (Empty set is a subset of every set)
  A ∩ ∅ = ∅      (Intersection with empty set is empty)
  A ∪ ∅ = A      (Union with empty set gives A)
  A - A = ∅      (Set minus itself is empty)
  ∅' = U         (Complement of empty set is universal set)
```

### Python Examples

```python
# Creating empty sets
empty_set = set()       # Correct way
not_empty = {}          # This creates an empty DICTIONARY, not a set!

print(type(empty_set))  # <class 'set'>
print(type(not_empty))  # <class 'dict'>

print(len(empty_set))   # 0
print(bool(empty_set))  # False (empty set is falsy)

# Empty set is subset of every set
A = {1, 2, 3}
print(empty_set.issubset(A))  # True
print(empty_set <= A)          # True

# Operations with empty set
print(A | empty_set)   # {1, 2, 3} = A
print(A & empty_set)   # set() = ∅
print(A - A)           # set() = ∅
```

### Visual Representation

```
Empty Set ∅ = {}

    +-----+
    |     |
    |     |  <- Nothing inside!
    |     |
    +-----+
    n(∅) = 0
```

---

## 9. Subsets

### Definition

> A set **A** is called a **subset** of set **B**, denoted by **A ⊆ B**, if **every element of A is also an element of B**.

In other words: if x ∈ A, then x ∈ B for all x.

### Types of Subsets

| Type | Symbol | Definition | Example |
|------|--------|------------|---------|
| **Subset** | A ⊆ B | Every element of A is in B | {1, 2} ⊆ {1, 2, 3} |
| **Proper Subset** | A ⊂ B | A ⊆ B but A ≠ B | {1, 2} ⊂ {1, 2, 3} |
| **Not a Subset** | A ⊄ B | At least one element of A is not in B | {1, 4} ⊄ {1, 2, 3} |
| **Superset** | A ⊇ B | B is a subset of A | {1, 2, 3} ⊇ {1, 2} |
| **Proper Superset** | A ⊃ B | A ⊇ B but A ≠ B | {1, 2, 3} ⊃ {1, 2} |

### Key Properties of Subsets

```
1. REFLEXIVE: A ⊆ A (Every set is a subset of itself)
2. TRANSITIVE: If A ⊆ B and B ⊆ C, then A ⊆ C
3. EMPTY SET: ∅ ⊆ A for every set A
4. EQUALITY: A = B if and only if A ⊆ B and B ⊆ A
5. POWER SET: The set of all subsets of A is called the Power Set, denoted P(A)
```

### Number of Subsets

If a set has **n** elements, then:
```
Number of subsets = 2^n
Number of proper subsets = 2^n - 1
```

### Examples

```
Set A = {1, 2}
Subsets of A:
  ∅ = {}
  {1}
  {2}
  {1, 2}

Total subsets = 2^2 = 4
Proper subsets = 2^2 - 1 = 3 (excluding {1,2} itself)
```

```
Set B = {a, b, c}
Subsets of B:
  ∅ = {}
  {a}, {b}, {c}
  {a, b}, {a, c}, {b, c}
  {a, b, c}

Total subsets = 2^3 = 8
Proper subsets = 2^3 - 1 = 7
```

### Power Set

> The **Power Set** of a set A, denoted by **P(A)** or **2^A**, is the set of **all possible subsets** of A, including the empty set and A itself.

```
If A = {1, 2}, then:
P(A) = {∅, {1}, {2}, {1, 2}}

n(P(A)) = 2^n(A) = 2^2 = 4
```

### Python Examples

```python
from itertools import combinations

A = {1, 2, 3}
B = {1, 2, 3, 4, 5}
C = {1, 2, 6}

# Check subset
print(A.issubset(B))       # True  -> A ⊆ B
print(A <= B)              # True  -> A ⊆ B
print(C.issubset(B))       # False -> C ⊄ B (because 6 ∉ B)

# Check proper subset
print(A < B)               # True  -> A ⊂ B
print(A < A)               # False -> A is NOT a proper subset of itself

# Check superset
print(B.issuperset(A))     # True  -> B ⊇ A
print(B >= A)              # True  -> B ⊇ A

# Generate all subsets (power set)
def power_set(s):
    s = list(s)
    result = []
    for i in range(len(s) + 1):
        for combo in combinations(s, i):
            result.append(set(combo))
    return result

ps = power_set({1, 2})
print(f"Power set of {{1,2}}: {ps}")
print(f"Number of subsets: {len(ps)}")  # 4 = 2^2
```

### Venn Diagram: Subset Relationship

```
A ⊆ B (A is a subset of B)

    +---------------------+
    |         B           |
    |    +---------+      |
    |    |    A    |      |
    |    |  (1,2)  |      |
    |    +---------+      |
    |    (3,4,5...)       |
    +---------------------+
```

---

## 12. Summary

### Quick Reference Table

| Concept | Definition | Symbol | Example |
|----------|------------|--------|---------|
| **Set** | Collection of distinct, well-defined objects | { } | A = {1, 2, 3} |
| **Element** | An object in a set | ∈, ∉ | 2 ∈ A, 4 ∉ A |
| **Universal Set** | Set of all elements under consideration | U | U = {1, 2, ..., 10} |
| **Finite Set** | Set with countable number of elements | |A| = n | {1, 2, 3}, n=3 |
| **Infinite Set** | Set with unlimited elements | |A| = ∞ | ℕ = {1, 2, 3, ...} |
| **Empty Set** | Set with no elements | ∅ or {} | ∅ = {} |
| **Subset** | Every element of A is in B | A ⊆ B | {1,2} ⊆ {1,2,3} |
| **Proper Subset** | A ⊆ B but A ≠ B | A ⊂ B | {1,2} ⊂ {1,2,3} |
| **Power Set** | Set of all subsets of A | P(A) | P({1,2}) = {∅,{1},{2},{1,2}} |
| **Cardinality** | Number of elements in a set | n(A) or |A| | |{a,b,c}| = 3 |

### Key Formulas

```
Number of subsets of A          = 2^n(A)
Number of proper subsets of A   = 2^n(A) - 1
n(A ∪ B) = n(A) + n(B) - n(A ∩ B)     [Inclusion-Exclusion]
n(A - B) = n(A) - n(A ∩ B)
n(A') = n(U) - n(A)
```

### Key Takeaways

1. ✅ A **set** is a well-defined collection of **distinct** objects.
2. ✅ Sets are **unordered** — {1,2,3} = {3,2,1}.
3. ✅ The **universal set** U contains all elements under consideration.
4. ✅ **Finite sets** have a countable number of elements; **infinite sets** do not.
5. ✅ The **empty set** ∅ contains no elements and is a subset of every set.
6. ✅ A **subset** contains only elements from another set.
7. ✅ The **power set** contains all possible subsets.
8. ✅ Set theory is the foundation of discrete mathematics, logic, and computer science.

---

<div align="center">

## 🎓 Master the Fundamentals of Set Theory!

> *"Set theory is the foundation of all mathematics. Understand sets, and you understand the language of logic."*

[![Discrete Math](https://img.shields.io/badge/Discrete%20Mathematics-1E88E5?style=for-the-badge)]()
[![Set Theory](https://img.shields.io/badge/Set%20Theory-FF6F00?style=for-the-badge)]()

</div>

---

*Lecture Material: Introduction to Discrete Mathematics & Set Theory*

*Last Updated: August 2026*