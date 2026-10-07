# Algebra of Sets and the Principle of Duality


---

## Table of Contents

1. [Learning Objectives](#1-learning-objectives)
2. [Quick Recap: Sets and Notation](#2-quick-recap-sets-and-notation)
3. [What is the Algebra of Sets?](#3-what-is-the-algebra-of-sets)
4. [Basic Set Operations](#4-basic-set-operations)
5. [Fundamental Laws of Set Algebra](#5-fundamental-laws-of-set-algebra)
6. [Proving Set Identities](#6-proving-set-identities)
7. [The Principle of Duality](#7-the-principle-of-duality)
8. [Worked Examples](#8-worked-examples)
9. [Common Mistakes](#9-common-mistakes)
10. [Practice Problems](#10-practice-problems)
11. [Summary](#11-summary)

---

## 1. Learning Objectives

After this lecture you should be able to:

- State what is meant by the *algebra of sets*.
- Define union, intersection, complement and difference, and compute them for small sets.
- State and apply the fundamental laws (commutative, associative, distributive, identity, complement, De Morgan's and others).
- Prove a set identity using the element method.
- State the **principle of duality** and write the dual of any set identity.

---

## 2. Quick Recap: Sets and Notation

| Symbol | Meaning |
|---|---|
| $x \in A$ | $x$ is an element of $A$ |
| $A \subseteq B$ | every element of $A$ is also in $B$ ($A$ is a subset of $B$) |
| $\emptyset$ | the empty set (no elements) |
| $U$ | the **universal set** (everything under discussion) |

**Running example** used throughout these notes:

$$
U = \{1,2,3,4,5,6,7,8\}
$$

$$
A = \{1,2,3,4\}, \qquad B = \{3,4,5,6\}, \qquad C = \{4,5,6,7\}
$$

---

## 3. What is the Algebra of Sets?

The **algebra of sets** studies the **laws and properties satisfied by set operations**.

Just as ordinary algebra tells us that $a + b = b + a$ for numbers, the algebra of sets tells us that $A \cup B = B \cup A$ for sets. These laws let us:

- **simplify** complicated set expressions,
- **prove** that two expressions are equal without listing elements,
- **transform** one valid identity into another (this is *duality*).

The same laws appear in **Boolean algebra**, **digital logic** (AND, OR, NOT) and **propositional logic** (∧, ∨, ¬). Learning them once pays off in many areas of computer science.

---

## 4. Basic Set Operations

### 4.1 Union ($\cup$)

Combines the elements of both sets.

$$
A \cup B = \{x \mid x \in A \ \text{or}\ x \in B\}
$$

**Example:** $A \cup B = \{1,2,3,4\} \cup \{3,4,5,6\} = \{1,2,3,4,5,6\}$

### 4.2 Intersection ($\cap$)

Keeps only the elements common to both sets.

$$
A \cap B = \{x \mid x \in A \ \text{and}\ x \in B\}
$$

**Example:** $A \cap B = \{3,4\}$

### 4.3 Complement ($A'$ or $A^c$)

Contains the elements of the universal set that are **not** in $A$.

$$
A' = \{x \in U \mid x \notin A\}
$$

**Example:** $A' = \{5,6,7,8\}$ and $B' = \{1,2,7,8\}$

### 4.4 Difference ($A - B$)

Elements in $A$ but not in $B$. It can be written using the other operations:

$$
A - B = A \cap B'
$$

**Example:** $A - B = \{1,2\}$

### 4.5 Disjoint Sets

$A$ and $B$ are **disjoint** if $A \cap B = \emptyset$.

### 4.6 Venn Diagram Idea (text version)

```
+---------------------- U ----------------------+
|     +-----------+     +-----------+           |
|     |     A     |     |     B     |           |
|     |      +----+-----+----+      |           |
|     |      |   A ∩ B        |     |           |
|     |      +----+-----+----+      |           |
|     +-----------+     +-----------+           |
+-----------------------------------------------+
   A ∪ B  = everything inside either circle
   A ∩ B  = the overlapping region
   A'     = everything in U outside circle A
```

---

## 5. Fundamental Laws of Set Algebra

For all sets $A, B, C$ that are subsets of a universal set $U$:

### 5.1 Commutative Laws

$$
A \cup B = B \cup A \qquad\qquad A \cap B = B \cap A
$$

*Meaning:* the order of the two sets does not matter.

### 5.2 Associative Laws

$$
(A \cup B) \cup C = A \cup (B \cup C)
$$

$$
(A \cap B) \cap C = A \cap (B \cap C)
$$

*Meaning:* grouping does not matter, so we can write $A \cup B \cup C$ without brackets.

**Check with numbers:**
$(A \cup B) \cup C = \{1,\dots,6\} \cup \{4,5,6,7\} = \{1,\dots,7\}$
$A \cup (B \cup C) = \{1,2,3,4\} \cup \{3,4,5,6,7\} = \{1,\dots,7\}$ ✔

### 5.3 Distributive Laws

$$
A \cup (B \cap C) = (A \cup B) \cap (A \cup C)
$$

$$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C)
$$

**Check with numbers (first law):**

- $B \cap C = \{4,5,6\}$, so $A \cup (B \cap C) = \{1,2,3,4,5,6\}$
- $A \cup B = \{1,\dots,6\}$ and $A \cup C = \{1,\dots,7\}$, so their intersection is $\{1,\dots,6\}$ ✔

**Check with numbers (second law):**

- $B \cup C = \{3,4,5,6,7\}$, so $A \cap (B \cup C) = \{3,4\}$
- $(A \cap B) \cup (A \cap C) = \{3,4\} \cup \{4\} = \{3,4\}$ ✔

> Note: unlike ordinary algebra, **both** operations distribute over each other.

### 5.3 Identity Laws

$$
A \cup \emptyset = A \qquad\qquad A \cap U = A
$$

*Meaning:* $\emptyset$ is neutral for union (like $0$ for addition); $U$ is neutral for intersection (like $1$ for multiplication).

### 5.4 Complement Laws

$$
A \cup A' = U \qquad\qquad A \cap A' = \emptyset
$$

**Example:** $A \cup A' = \{1,2,3,4\} \cup \{5,6,7,8\} = U$ and $A \cap A' = \emptyset$.

### 5.5 De Morgan's Laws

$$
(A \cup B)' = A' \cap B'
$$

$$
(A \cap B)' = A' \cup B'
$$

*In words:* the complement of a union is the intersection of complements, and vice versa.

**Check with numbers:**

- $(A \cup B)' = \{1,\dots,6\}' = \{7,8\}$ and $A' \cap B' = \{5,6,7,8\} \cap \{1,2,7,8\} = \{7,8\}$ ✔
- $(A \cap B)' = \{3,4\}' = \{1,2,5,6,7,8\}$ and $A' \cup B' = \{5,6,7,8\} \cup \{1,2,7,8\} = \{1,2,5,6,7,8\}$ ✔

### 5.6 Other Useful Laws

| Law | Union form | Intersection form |
|---|---|---|
| **Idempotent** | $A \cup A = A$ | $A \cap A = A$ |
| **Domination (Null/Universal bound)** | $A \cup U = U$ | $A \cap \emptyset = \emptyset$ |
| **Absorption** | $A \cup (A \cap B) = A$ | $A \cap (A \cup B) = A$ |
| **Complement of $U$ and $\emptyset$** | $\emptyset' = U$ | $U' = \emptyset$ |
| **Involution (double complement)** | $(A')' = A$ | |

**Absorption example:** $A \cap B = \{3,4\}$, so $A \cup (A \cap B) = \{1,2,3,4\} = A$ ✔

### 5.7 Master Table of Laws

| # | Law | Form 1 | Form 2 |
|---|---|---|---|
| 1 | Commutative | $A \cup B = B \cup A$ | $A \cap B = B \cap A$ |
| 2 | Associative | $(A \cup B) \cup C = A \cup (B \cup C)$ | $(A \cap B) \cap C = A \cap (B \cap C)$ |
| 3 | Distributive | $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$ | $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$ |
| 4 | Identity | $A \cup \emptyset = A$ | $A \cap U = A$ |
| 5 | Complement | $A \cup A' = U$ | $A \cap A' = \emptyset$ |
| 6 | Idempotent | $A \cup A = A$ | $A \cap A = A$ |
| 7 | Domination | $A \cup U = U$ | $A \cap \emptyset = \emptyset$ |
| 8 | Absorption | $A \cup (A \cap B) = A$ | $A \cap (A \cup B) = A$ |
| 9 | De Morgan | $(A \cup B)' = A' \cap B'$ | $(A \cap B)' = A' \cup B'$ |
| 10 | Involution | $(A')' = A$ | (self-paired) |

**Observe the pattern:** every law (except involution) comes in a *pair* of forms. This is exactly the **principle of duality** (Section 7).

---

## 6. Proving Set Identities

### Method 1: Element (membership) method

To prove $X = Y$, show $X \subseteq Y$ and $Y \subseteq X$ by picking an arbitrary element $x$.

**Example: prove $(A \cup B)' = A' \cap B'$**

*Part 1: $(A \cup B)' \subseteq A' \cap B'$*

1. Let $x \in (A \cup B)'$.
2. Then $x \notin A \cup B$.
3. So $x \notin A$ **and** $x \notin B$.
4. Hence $x \in A'$ and $x \in B'$, i.e. $x \in A' \cap B'$.

*Part 2: $A' \cap B' \subseteq (A \cup B)'$*

1. Let $x \in A' \cap B'$.
2. Then $x \notin A$ and $x \notin B$.
3. So $x \notin A \cup B$, i.e. $x \in (A \cup B)'$.

Both inclusions hold, so the sets are equal. ∎

### Method 2: Use known laws (algebraic proof)

**Example: simplify $A \cup (A' \cap B)$**

$$
\begin{aligned}
A \cup (A' \cap B) &= (A \cup A') \cap (A \cup B) && \text{(distributive)} \\
&= U \cap (A \cup B) && \text{(complement law)} \\
&= A \cup B && \text{(identity law)}
\end{aligned}
$$

### Method 3: Membership table

Like a truth table: `1` means "$x$ is in the set", `0` means "not in".

| $A$ | $B$ | $A \cup B$ | $(A \cup B)'$ | $A'$ | $B'$ | $A' \cap B'$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 0 | 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 | 0 | 0 |
| 1 | 0 | 1 | 0 | 0 | 1 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 | 0 |

The columns for $(A \cup B)'$ and $A' \cap B'$ are identical, so the identity holds.

---

## 7. The Principle of Duality

### 7.1 Statement

> **Principle of Duality:** If an identity involving sets, the operations $\cup$, $\cap$, and the special sets $\emptyset$, $U$ is true, then the identity obtained by **interchanging** $\cup \leftrightarrow \cap$ and $\emptyset \leftrightarrow U$ is also true.

The new identity is called the **dual** of the original one.

In plain words: the algebra of sets is *symmetric*. Every valid identity automatically gives you a second valid identity for free.

### 7.2 How to Write the Dual

Swap the following in the given statement; leave everything else (sets $A, B, C$ and complements) unchanged:

| Original | Dual |
|:-:|:-:|
| $\cup$ (union) | $\cap$ (intersection) |
| $\cap$ (intersection) | $\cup$ (union) |
| $\emptyset$ | $U$ |
| $U$ | $\emptyset$ |

**For statements with inclusion**, also reverse the inclusion sign:

| Original | Dual |
|:-:|:-:|
| $\subseteq$ | $\supseteq$ |
| $\supseteq$ | $\subseteq$ |

### 7.3 Simple Examples of Duality

| Original identity | Dual identity | Law |
|---|---|---|
| $A \cup B = B \cup A$ | $A \cap B = B \cap A$ | Commutative |
| $A \cup (B \cup C) = (A \cup B) \cup C$ | $A \cap (B \cap C) = (A \cap B) \cap C$ | Associative |
| $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$ | $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$ | Distributive |
| $A \cup \emptyset = A$ | $A \cap U = A$ | Identity |
| $A \cup A' = U$ | $A \cap A' = \emptyset$ | Complement |
| $A \cup A = A$ | $A \cap A = A$ | Idempotent |
| $A \cup U = U$ | $A \cap \emptyset = \emptyset$ | Domination |
| $A \cup (A \cap B) = A$ | $A \cap (A \cup B) = A$ | Absorption |
| $(A \cup B)' = A' \cap B'$ | $(A \cap B)' = A' \cup B'$ | De Morgan |

So the "two forms" in each law of Section 5 are **dual to each other**: you only need to prove one.

### 7.4 Step-by-Step Example

**Find the dual of:** $\;A \cup (B \cap U) = A \cup B$

1. Replace $\cup$ by $\cap$: &nbsp; $A \cap (B \cup U) = A \cap B$
2. Replace $\cap$ by $\cup$: this is already done together with step 1, so we now handle all symbols at once.
3. Replace $U$ by $\emptyset$: &nbsp; $A \cap (B \cup \emptyset) = A \cap B$

**Dual:** $A \cap (B \cup \emptyset) = A \cap B$

Verify with our numbers: $B \cup \emptyset = B$, so the left side is $A \cap B = \{3,4\}$ ✔ 

### 7.5 Why Does Duality Work?

Every axiom of set algebra (the laws in Section 5) comes in a dual pair, and swapping $\cup \leftrightarrow \cap$ and $\emptyset \leftrightarrow U$ turns each axiom into another axiom. So if a proof of an identity uses certain axioms step by step, applying the dual of each step gives a valid proof of the dual identity.

> A good way to see it: De Morgan's laws act like a "mirror" that turns unions into intersections and vice versa. The algebra of sets looks the same on both sides of the mirror.

### 7.6 Using Duality to Save Work

**Task:** Prove $A \cap (A \cup B) = A$ (absorption).

If we already know $A \cup (A \cap B) = A$, then the required identity is its **dual** (swap $\cup \leftrightarrow \cap$), so it is true automatically; no second proof is needed.

Only to be sure, here is the direct proof of the first form:

$$
\begin{aligned}
A \cup (A \cap B) &= (A \cap U) \cup (A \cap B) && \text{(identity)} \\
&= A \cap (U \cup B) && \text{(distributive)} \\
&= A \cap U && \text{(domination)} \\
&= A && \text{(identity)}
\end{aligned}
$$

### 7.7 Self-Dual Statements

A statement is **self-dual** if its dual is the same statement. Example: the double complement law $(A')' = A$ (it contains no $\cup$, $\cap$, $\emptyset$ or $U$ to swap).

### 7.8 Duality and Other Areas (Preview)

The same principle holds in related systems:

| Set theory | Propositional logic | Digital logic |
|:-:|:-:|:-:|
| $\cup$ | $\vee$ (OR) | OR gate |
| $\cap$ | $\wedge$ (AND) | AND gate |
| $A'$ | $\neg A$ (NOT) | NOT gate |
| $U$ | True ($T$) | 1 |
| $\emptyset$ | False ($F$) | 0 |

Dual in logic: swap $\vee \leftrightarrow \wedge$ and $T \leftrightarrow F$. For example, $p \vee F = p$ has dual $p \wedge T = p$.

---

## 8. Worked Examples

### Example 1: Simplify using the laws

Simplify $(A \cup B) \cap (A \cup B')$.

$$
\begin{aligned}
(A \cup B) \cap (A \cup B') &= A \cup (B \cap B') && \text{(distributive)} \\
&= A \cup \emptyset && \text{(complement)} \\
&= A && \text{(identity)}
\end{aligned}
$$

**Dual result:** $(A \cap B) \cup (A \cap B') = A$.

**Quick check:** $A \cap B = \{3,4\}$ and $A \cap B' = \{1,2\}$; union $= \{1,2,3,4\} = A$ ✔

### Example 2: Use De Morgan's law

Simplify $(A' \cup B')'$.

$$
(A' \cup B')' = (A')' \cap (B')' = A \cap B
$$

using De Morgan and then the double complement law.

### Example 3: Real-life flavour

A class has the following clubs:
$A$ = students in the Coding Club, $B$ = students in the Chess Club.

| Expression | Plain meaning |
|---|---|
| $A \cup B$ | in at least one of the clubs |
| $A \cap B$ | in both clubs |
| $A'$ | not in the Coding Club |
| $(A \cup B)'$ | in neither club |
| $A' \cap B'$ | not in Coding **and** not in Chess (same as "neither") |

The last two rows being equal is De Morgan's law in everyday language.

### Example 4: Prove and write the dual

**Prove:** $A \cup (A' \cap B) = A \cup B$ &nbsp; (done in Section 6).

**Dual:** $A \cap (A' \cup B) = A \cap B$.

**Check:** $A' \cup B = \{5,6,7,8\} \cup \{3,4,5,6\} = \{3,4,5,6,7,8\}$, then $A \cap \{3,\dots,8\} = \{3,4\} = A \cap B$ ✔

---

## 9. Common Mistakes

1. **Swapping complements.** In writing a dual, do **not** remove or change the complement signs. Only $\cup, \cap, \emptyset, U$ (and $\subseteq, \supseteq$) are swapped.
2. **Forgetting to swap $\emptyset$ and $U$.** Swapping only the operations gives a *wrong* statement. For example, $A \cup \emptyset = A$ becomes $A \cap \emptyset = A$ (false) if $\emptyset$ is not changed to $U$.
3. **Confusing dual with complement.** The dual of $X = Y$ is *not* $X' = Y'$.
4. **Applying duality to non-identities.** Duality applies to *valid identities in the algebra of sets*. Statements involving specific numeric sets (such as $A = \{1,2,3\}$) do not necessarily have duals that are true.
5. **Treating difference as commutative.** $A - B \ne B - A$ in general.

---

## 10. Practice Problems

**Q1.** Write the dual of each statement:

- (a) $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
- (b) $A \cup U = U$
- (c) $(A \cup B)' = A' \cap B'$
- (d) $(A \cap B) \cup (A \cap B') = A$

**Q2.** Let $U = \{1,\dots,10\}$, $A = \{1,3,5,7,9\}$, $B = \{2,3,5,7\}$. Compute $A \cup B$, $A \cap B$, $A'$, $B'$, $A - B$, and verify both De Morgan laws.

**Q3.** Prove using the element method: $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$.

**Q4.** Simplify: $(A \cup B') \cap (A' \cup B')$.

**Q5.** Use a membership table to prove $A \cup (A \cap B) = A$. Then state its dual.

---

### Answers (Selected)

**Q1.**

- (a) $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$
- (b) $A \cap \emptyset = \emptyset$
- (c) $(A \cap B)' = A' \cup B'$
- (d) $(A \cup B) \cap (A \cup B') = A$

**Q2.**

- $A \cup B = \{1,2,3,5,7,9\}$, $A \cap B = \{3,5,7\}$
- $A' = \{2,4,6,8,10\}$, $B' = \{1,4,6,8,9,10\}$
- $A - B = \{1,9\}$
- $(A \cup B)' = \{4,6,8,10\} = A' \cap B'$ ✔
- $(A \cap B)' = \{1,2,4,6,8,9,10\} = A' \cup B'$ ✔

**Q4.** $(A \cup B') \cap (A' \cup B') = (A \cap A') \cup B' = \emptyset \cup B' = B'$ (distributive, complement, identity). The dual is $(A \cap B') \cup (A' \cap B') = B'$.

---

## 11. Summary

- The **algebra of sets** is the collection of laws that union, intersection and complement obey: commutative, associative, distributive, identity, complement, idempotent, domination, absorption, De Morgan's, and involution.
- Identities can be **proved** by the element method, by algebraic manipulation with known laws, or by membership tables.
- The **principle of duality** says: swap $\cup \leftrightarrow \cap$ and $\emptyset \leftrightarrow U$ (and $\subseteq \leftrightarrow \supseteq$) in any valid identity, and you get another valid identity.
- Duality **halves the work**: prove one law and its dual comes free.
- The same structure appears in **Boolean algebra**, **propositional logic** and **digital circuits**.

---

### References

- Wikipedia: [Algebra of sets](https://en.wikipedia.org/wiki/Algebra_of_sets)
- Study.com: [The Algebra of Sets: Properties & Laws of Set Theory](https://study.com/academy/lesson/the-algebra-of-sets-properties-laws-of-set-theory.html)
- Scribd: [Algebra of Sets and Duality](https://www.scribd.com/presentation/846592627/Algebra-of-Sets-and-Duality)
