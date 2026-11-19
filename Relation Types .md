# 🔗 Relations & Their Properties

> A visual, exam-ready guide to the six core properties of relations in Discrete Mathematics — reflexive, irreflexive, symmetric, antisymmetric, asymmetric, and transitive.

![Topic](https://img.shields.io/badge/Topic-Discrete%20Mathematics-blue?style=flat-square)
![Chapter](https://img.shields.io/badge/Chapter-Relations%20%26%20Types-orange?style=flat-square)
![Level](https://img.shields.io/badge/Level-Beginner%20Friendly-brightgreen?style=flat-square)

---

## 📖 Introduction

A **relation** is a connection or association between the elements of two sets. A relation $R$ on a set $A$ is a **subset** of the Cartesian product $A \times A$.

**🧪 Example**

Let $A = \{1,2,3\}$. Then the Cartesian product is:

$$A \times A = \{(1,1),(1,2),(1,3),\ldots,(3,3)\}$$

Suppose we define a relation:

$$R = \{(1,1),(2,2),(3,3),(1,2),(2,3)\}$$

> 💡 Every relation on $A$ is just some collection of ordered pairs drawn from $A \times A$.

---

## 🎯 The Six Types of Relations

| # | Property | Core Idea | Symbolic Form |
|---|----------|-----------|---------------|
| 1️⃣ | [Reflexive](#1️⃣-reflexive-relation) | Every element relates to itself | $\forall a \in A,\ (a,a) \in R$ |
| 2️⃣ | [Irreflexive](#2️⃣-irreflexive-relation) | No element relates to itself | $\forall a \in A,\ (a,a) \notin R$ |
| 3️⃣ | [Symmetric](#3️⃣-symmetric-relation) | Reverse pair must exist | $(a,b) \in R \Rightarrow (b,a) \in R$ |
| 4️⃣ | [Antisymmetric](#4️⃣-antisymmetric-relation) | Both directions $\Rightarrow$ equality | $[(a,b) \in R \land (b,a) \in R] \Rightarrow a=b$ |
| 5️⃣ | [Asymmetric](#5️⃣-asymmetric-relation) | Reverse pair must *not* exist | $(a,b) \in R \Rightarrow (b,a) \notin R$ |
| 6️⃣ | [Transitive](#6️⃣-transitive-relation) | Two steps imply one direct step | $[(a,b) \in R \land (b,c) \in R] \Rightarrow (a,c) \in R$ |

---

### 1️⃣ Reflexive Relation

> **Definition:** A relation $R$ on $A$ is **reflexive** if every element of the set is related to itself.

$$\forall a \in A,\quad (a,a) \in R$$

**🧪 Example:** Let $A=\{1,2,3\}$

$$R=\{(1,1),(2,2),(3,3),(1,2)\}$$

✅ Reflexive, because all diagonal pairs are present:

- $(1,1)$ ✔️
- $(2,2)$ ✔️
- $(3,3)$ ✔️

**🔑 Key point:** *All* diagonal pairs must be present.
**🌍 Real-life:** Every person is equal to themselves.

---

### 2️⃣ Irreflexive Relation

> **Definition:** A relation $R$ on $A$ is **irreflexive** if *no* element is related to itself.

$$\forall a \in A,\quad (a,a) \notin R$$

**🧪 Example:**

$$R=\{(1,2),(1,3),(2,3)\}$$

✅ Irreflexive, because none of $(1,1)$, $(2,2)$, $(3,3)$ exists.

**🔑 Key point:** *No* diagonal pairs are present.
**🌍 Real-life:** The relation "is greater than" ($>$) — $5 > 5$ is false.

---

### 3️⃣ Symmetric Relation

> **Definition:** $R$ is **symmetric** if whenever $a$ is related to $b$, then $b$ is also related to $a$.

$$\forall a,b \in A,\quad (a,b) \in R \Rightarrow (b,a) \in R$$

**🧪 Example:**

$$R=\{(1,2),(2,1),(2,3),(3,2)\}$$

✅ Symmetric, because:

- $(1,2) \leftrightarrow (2,1)$ ✔️
- $(2,3) \leftrightarrow (3,2)$ ✔️

**🔑 Key point:** Every ordered pair must have its reverse pair.
**🌍 Real-life:** "Is a friend of" — friendship is mutual.

---

### 4️⃣ Antisymmetric Relation

> **Definition:** $R$ is **antisymmetric** if $aRb$ and $bRa$ together force $a = b$.

$$\forall a,b \in A,\quad [(a,b) \in R \land (b,a) \in R] \Rightarrow a=b$$

**🧪 Example:**

$$R=\{(1,1),(2,2),(3,3),(1,2),(1,3)\}$$

✅ Antisymmetric, because:

- $(1,2)$ exists, but $(2,1)$ does **not** ✔️
- $(1,3)$ exists, but $(3,1)$ does **not** ✔️
- No two *distinct* elements are related in both directions.

**🔑 Key point:** Two different elements cannot be related in both directions.
**🌍 Real-life:** "Less than or equal to" ($\leq$) — if $a \le b$ and $b \le a$, then $a = b$.

---

### 5️⃣ Asymmetric Relation

> **Definition:** $R$ is **asymmetric** if whenever $a$ is related to $b$, then $b$ cannot be related to $a$.

$$\forall a,b \in A,\quad (a,b) \in R \Rightarrow (b,a) \notin R$$

**🧪 Example:**

$$R=\{(1,2),(1,3),(2,3)\}$$

✅ Asymmetric, because every pair's reverse is absent:

- $(1,2)$ → $(2,1)$ absent ✔️
- $(1,3)$ → $(3,1)$ absent ✔️
- $(2,3)$ → $(3,2)$ absent ✔️

**🔑 Key point:** If one direction exists, the reverse must never exist.
**🌍 Real-life:** "Is taller than" — if A is taller than B, B cannot be taller than A.

> ⚠️ **Important:** Every asymmetric relation is **irreflexive**, but not every irreflexive relation is asymmetric.

---

### 6️⃣ Transitive Relation

> **Definition:** $R$ is **transitive** if $aRb$ and $bRc$ together force $aRc$.

$$\forall a,b,c \in A,\quad [(a,b) \in R \land (b,c) \in R] \Rightarrow (a,c) \in R$$

**🧪 Example:**

$$R=\{(1,2),(2,3),(1,3)\}$$

✅ Transitive, because:

- $(1,2) \in R$
- $(2,3) \in R$
- Therefore $(1,3)$ must exist — and it does ✔️

**🔑 Key point:** Two consecutive relationships imply the direct relationship.
**🌍 Real-life:** "Less than" ($<$) — if $2<5$ and $5<8$, then $2<8$.

---

## ⚖️ Quick Comparison of All Six Properties

| Property | Main condition | Example |
|----------|----------------|---------|
| 🔁 Reflexive | Every element relates to itself | $a = a$ |
| 🚫 Irreflexive | No element relates to itself | $a < a$ (false) |
| ↔️ Symmetric | Reverse pair must exist | Friendship |
| ⛓️ Antisymmetric | Both directions imply equality | $\leq$ |
| ➡️ Asymmetric | Reverse pair must not exist | $<$ |
| 🔂 Transitive | Two relationships imply a third | $<$ |

---

## 📝 Exam-Critical Differences

These distinctions are frequently tested in Discrete Mathematics exams:

| 🔁↔️ Symmetric | ⛓️ Antisymmetric | ➡️ Asymmetric |
|----------------|------------------|----------------|
| Reverse pair **must exist** | Reverse pair exists **only when elements are equal** | Reverse pair **must never exist** |
| $(1,2)$ requires $(2,1)$ | $(1,2)$ & $(2,1)$ can't both exist for distinct elements | $(1,2)$ **prohibits** $(2,1)$ |
| Diagonal pairs allowed ✅ | Diagonal pairs allowed ✅ | Diagonal pairs **not allowed** ❌ |

### 🧠 Facts Worth Memorizing

1. ✅ Every reflexive relation contains **all** diagonal pairs.
2. ✅ Every irreflexive relation contains **no** diagonal pairs.
3. ✅ Every asymmetric relation is irreflexive.
4. ✅ Every asymmetric relation is antisymmetric.
5. ✅ A relation can be **both** symmetric and antisymmetric.
6. ✅ A relation can be **both** reflexive and symmetric.
7. ✅ A relation can be **neither** symmetric nor antisymmetric.

---

## ✍️ Practice MCQs

<details>
<summary><b>Q1.</b> $A=\{1,2,3\}$, $R=\{(1,1),(2,2),(3,3)\}$. Which property does $R$ satisfy?</summary>

- A. Reflexive
- B. Irreflexive
- C. Asymmetric

**✅ Correct answer: A. Reflexive**

> All three diagonal pairs are present, so $R$ is reflexive.

</details>

<details>
<summary><b>Q2.</b> $R=\{(1,2),(2,1)\}$. Which property does this relation satisfy?</summary>

- A. Asymmetric
- B. Symmetric
- C. Irreflexive only

**✅ Correct answer: B. Symmetric**

> Both $(1,2)$ and its reverse $(2,1)$ are present, so it is symmetric.

</details>

<details>
<summary><b>Q3.</b> If $aRb$ and $bRa$ imply $a=b$, which property is satisfied?</summary>

- A. Symmetric
- B. Transitive
- C. Antisymmetric

**✅ Correct answer: C. Antisymmetric**

> This is the definition of an antisymmetric relation.

</details>

<details>
<summary><b>Q4.</b> The relation "greater than ($>$)" on integers is:</summary>

- A. Reflexive
- B. Asymmetric
- C. Symmetric

**✅ Correct answer: B. Asymmetric**

> If $a > b$, then $b$ cannot be greater than $a$.

</details>

<details>
<summary><b>Q5.</b> If $(1,2)$ and $(2,3)$ are in $R$, which pair must exist for transitivity?</summary>

- A. $(3,1)$
- B. $(2,1)$
- C. $(1,3)$

**✅ Correct answer: C. $(1,3)$**

> Transitivity requires $(1,3)$ to be present.

</details>

---

## 📚 Summary Cheat Sheet

```text
Diagonal pairs?   All → Reflexive | None → Irreflexive
Reverse pair?     Must exist → Symmetric
                  Never exist  → Asymmetric
                  Only if a=b  → Antisymmetric
Chained pairs?    a→b→c requires a→c → Transitive
```

---

<div align="center">

**Made for learners 📘 — Relations made simple!**

⭐ If this helped you, give it a star!

</div>
