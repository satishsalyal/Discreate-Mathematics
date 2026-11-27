# Propositional Logic

> **Learning objectives:** Understand propositions and truth values,
> identify simple and compound statements, use logical connectives,
> construct truth tables, and classify formulas as tautologies,
> contradictions, or contingencies.

------------------------------------------------------------------------

## Contents

1.  [Introduction](#1-introduction)
2.  [Proposition or Sentence](#2-proposition-or-sentence)
3.  [Truth Value](#3-truth-value)
4.  [Types of Propositions](#4-types-of-propositions)
5.  [Logical Connectives](#5-logical-connectives)
6.  [Conjunction (AND)](#6-conjunction-and)
7.  [Disjunction (OR)](#7-disjunction-or)
8.  [Negation (NOT)](#8-negation-not)
9.  [Tautology, Contradiction and
    Contingency](#9-tautology-contradiction-and-contingency)
10. [Important Logical Laws](#10-important-logical-laws)
11. [Implication and Biconditional](#11-implication-and-biconditional)
12. [Solved Questions](#12-solved-questions)
13. [Truth Table Construction](#13-truth-table-construction)
14. [Practice Questions](#14-practice-questions)
15. [Quick Revision](#15-quick-revision)
16. [Examination Tips](#16-examination-tips)
17. [Self-Assessment](#17-self-assessment)

------------------------------------------------------------------------

## 1. Introduction

**Propositional Logic** is a branch of mathematical logic that studies
statements (propositions) that can be either **True (T)** or **False
(F)**. It provides rules for combining statements and determining the
truth of compound statements.

It is also known as statement logic or sentential logic. In computing,
it is closely related to Boolean logic.

### Examples

  Statement                            Truth value
  ------------------------------------ -------------
  The Earth revolves around the Sun.   True
  5 + 3 = 8                            True
  10 is an odd number.                 False

### Applications

-   Computer programming and conditional statements
-   Digital circuits and Boolean algebra
-   Artificial intelligence and knowledge representation
-   Database queries
-   Mathematical proofs and logical reasoning

## 2. Proposition or Sentence

A **proposition** is a declarative sentence that expresses a complete
statement and has exactly one truth value: either True or False.

In simple words, a sentence that can be identified as true or false is a
proposition.

### 2.1 Examples of propositions

  Statement                     Truth value Proposition?
  --------------------------- ------------- --------------
  2 + 3 = 5                            True Yes
  10 is less than 5                   False Yes
  Jammu is in India                    True Yes
  7 is an even number                 False Yes
  The Sun rises in the east            True Yes

### 2.2 Sentences that are not propositions

  Sentence                        Reason
  ------------------------------- ---------------------------
  What is your name?              Question
  Please open the door.           Command
  How beautiful this flower is!   Exclamation
  x + 5 = 10                      Depends on the value of x
  May you succeed!                Wish

> **Important:** An expression containing an unspecified variable, such
> as `x + 5 = 10`, is not a proposition until the variable is assigned a
> value or quantified.

### 2.3 Representation

Propositions are generally represented by lowercase letters: `p`, `q`,
`r`, `s`, ...

For example:

-   `p`: 5 is an odd number.
-   `q`: 10 is greater than 20.
-   `r`: Jammu is in India.

Therefore, `p = T`, `q = F`, and `r = T`.

## 3. Truth Value

The **truth value** of a proposition indicates whether the statement is
true or false. Classical propositional logic has two truth values:

-   **T (1):** True
-   **F (0):** False

In computer science, these are commonly represented by binary values 1
and 0.

### Examples

1.  Let `p: 8 > 5`. Since 8 is greater than 5, `p = T`.
2.  Let `q: 15 < 10`. Since this is false, `q = F`.
3.  Let `r: 12 is an even number`. Therefore, `r = T`.

  Proposition            Truth value
  ---------------------- -------------
  4 + 4 = 8              T
  9 is a prime number    F
  20 is divisible by 5   T
  3 is greater than 10   F

## 4. Types of Propositions

Propositions are broadly classified into two types.

### 4.1 Simple (Atomic) Proposition

A **simple proposition** expresses a single idea and cannot be divided
into smaller propositions using logical connectives.

Examples:

-   `p`: Ram is a student.
-   `q`: 10 is an even number.
-   `r`: Delhi is the capital of India.

### 4.2 Compound Proposition

A **compound proposition** is formed by combining two or more simple
propositions using logical connectives such as AND, OR and NOT.

Let:

-   `p`: It is raining.
-   `q`: It is cold.

Then:

-   `p ∧ q`: It is raining **and** it is cold.
-   `p ∨ q`: It is raining **or** it is cold.

### Simple vs compound propositions

  -----------------------------------------------------------------------
  Simple proposition                  Compound proposition
  ----------------------------------- -----------------------------------
  Contains one basic statement        Combines two or more statements

  Example: 5 is odd                   Example: 5 is odd AND 8 is even

  Represented by `p`, `q`, `r`        Represented by expressions such as
                                      `p ∧ q`
  -----------------------------------------------------------------------

## 5. Logical Connectives

Logical connectives are symbols or operators used to combine or modify
propositions to form compound propositions.

  Connective      Symbol   Meaning
  --------------- -------- ----------------
  Conjunction     `∧`      AND
  Disjunction     `∨`      OR
  Negation        `¬`      NOT
  Implication     `→`      If ... then
  Biconditional   `↔`      If and only if

Let `p`: 10 is an even number, and `q`: 15 is an odd number.

-   `p ∧ q`: 10 is even AND 15 is odd.
-   `p ∨ q`: 10 is even OR 15 is odd.
-   `¬p`: 10 is not even.
-   `p → q`: If 10 is even, then 15 is odd.
-   `p ↔ q`: 10 is even if and only if 15 is odd.

## 6. Conjunction (AND)

**Conjunction** combines two propositions using AND. It is represented
by `p ∧ q`.

A conjunction is **True only when both propositions are True**. In every
other case, it is False.

### Example

Let:

-   `p`: 10 is an even number.
-   `q`: 15 is an odd number.

Both are true, so `p ∧ q` is True.

### Truth table

  p   q   `p ∧ q`
  --- --- ---------
  T   T   **T**
  T   F   F
  F   T   F
  F   F   F

### Explanation

1.  Both p and q are True → result is True.
2.  p is True and q is False → result is False.
3.  p is False and q is True → result is False.
4.  Both are False → result is False.

**Real-life example:** A student may be eligible to appear in an
examination if the student has completed registration **and** paid the
examination fee. Both conditions must be satisfied.

## 7. Disjunction (OR)

**Disjunction** combines two propositions using OR. It is represented by
`p ∨ q`.

A disjunction is **True when at least one proposition is True**. It is
False only when both propositions are False.

### Example

Let:

-   `p`: 8 is an even number.
-   `q`: 9 is an even number.

Since `p` is True, `p ∨ q` is True.

### Truth table

  p   q   `p ∨ q`
  --- --- ---------
  T   T   **T**
  T   F   **T**
  F   T   **T**
  F   F   F

> **Important:** In propositional logic, OR normally means **inclusive
> OR**. Both propositions may be true at the same time.

**Real-life example:** A student can choose Mathematics OR Economics as
an elective subject. Under inclusive OR, having both options available
also satisfies the OR condition.

## 8. Negation (NOT)

**Negation** reverses the truth value of a proposition. It is
represented by `¬p`.

-   If p is True, `¬p` is False.
-   If p is False, `¬p` is True.

### Examples

1.  `p`: 10 is an even number. `¬p`: 10 is not an even number. Since p
    is True, `¬p` is False.
2.  `q`: 7 is an even number. Since q is False, `¬q` is True.

### Truth table

  p   `¬p`
  --- ------
  T   F
  F   T

### Double Negation Law

`¬(¬p) = p`

A double negation has the same truth value as the original proposition.

## 9. Tautology, Contradiction and Contingency

These concepts help determine whether a compound proposition is always
true, always false, or sometimes true.

### 9.1 Tautology

A **tautology** is a compound proposition that is True for every
possible combination of truth values of its component propositions.

Example:

`p ∨ ¬p`

  p   `¬p`   `p ∨ ¬p`
  --- ------ ----------
  T   F      **T**
  F   T      **T**

The final column contains only True values. Therefore, `p ∨ ¬p` is a
**tautology**.

### 9.2 Contradiction

A **contradiction** is a compound proposition that is False for every
possible combination of truth values.

Example:

`p ∧ ¬p`

  p   `¬p`   `p ∧ ¬p`
  --- ------ ----------
  T   F      **F**
  F   T      **F**

The final column contains only False values. Therefore, `p ∧ ¬p` is a
**contradiction**.

### 9.3 Contingency

A **contingency** is a compound proposition that is True for some
combinations and False for others.

Example: `p ∧ q`

  p   q   `p ∧ q`
  --- --- ---------
  T   T   T
  T   F   F
  F   T   F
  F   F   F

The final column contains both T and F. Therefore, it is a contingency.

### Comparison

  -----------------------------------------------------------------------
  Tautology               Contradiction           Contingency
  ----------------------- ----------------------- -----------------------
  Always True             Always False            Sometimes True,
                                                  sometimes False

  Final column: all T     Final column: all F     Final column: mixture
                                                  of T and F

  `p ∨ ¬p`                `p ∧ ¬p`                `p ∧ q`
  -----------------------------------------------------------------------

> **Quick rule:** All T = Tautology · All F = Contradiction · Mixed T
> and F = Contingency.

## 10. Important Logical Laws

These laws are used to simplify logical expressions and solve problems.

### 10.1 Identity Laws

-   `p ∧ T = p`
-   `p ∨ F = p`

### 10.2 Domination Laws

-   `p ∨ T = T`
-   `p ∧ F = F`

### 10.3 Idempotent Laws

-   `p ∧ p = p`
-   `p ∨ p = p`

### 10.4 Complement Laws

-   `p ∨ ¬p = T`
-   `p ∧ ¬p = F`

### 10.5 Double Negation Law

-   `¬(¬p) = p`

### 10.6 Commutative Laws

-   `p ∧ q = q ∧ p`
-   `p ∨ q = q ∨ p`

Changing the order of propositions does not change the result.

### 10.7 Associative Laws

-   `(p ∧ q) ∧ r = p ∧ (q ∧ r)`
-   `(p ∨ q) ∨ r = p ∨ (q ∨ r)`

### 10.8 Distributive Laws

-   `p ∧ (q ∨ r) = (p ∧ q) ∨ (p ∧ r)`
-   `p ∨ (q ∧ r) = (p ∨ q) ∧ (p ∨ r)`

### 10.9 De Morgan's Laws

**First law:**

`¬(p ∧ q) = ¬p ∨ ¬q`

The negation of AND becomes OR, and each proposition is negated.

**Second law:**

`¬(p ∨ q) = ¬p ∧ ¬q`

The negation of OR becomes AND, and each proposition is negated.

**Example:** Let p = "I am studying" and q = "I am working".

The negation of "I am studying AND I am working" is:

"I am not studying OR I am not working."

Symbolically: `¬(p ∧ q) = ¬p ∨ ¬q`.

## 11. Implication and Biconditional

### 11.1 Implication (If--Then)

Implication represents a conditional statement and is written as
`p → q`, read as "If p, then q".

It is **False only when p is True and q is False**.

Example:

-   p: A number is divisible by 4.
-   q: A number is even.

Statement: If a number is divisible by 4, then it is even.

  p   q   `p → q`
  --- --- ---------
  T   T   T
  T   F   **F**
  F   T   T
  F   F   T

### 11.2 Biconditional (If and Only If)

Biconditional is written as `p ↔ q`, read as "p if and only if q".

It is True when both propositions have the same truth value.

  p   q   `p ↔ q`
  --- --- ---------
  T   T   **T**
  T   F   F
  F   T   F
  F   F   **T**

### Summary of connectives

  Operation       Symbol    When is it True?
  --------------- --------- --------------------------
  AND             `p ∧ q`   Both T
  OR              `p ∨ q`   At least one T
  NOT             `¬p`      When p is F
  Implication     `p → q`   Except when T → F
  Biconditional   `p ↔ q`   Both have the same value

## 12. Solved Questions

### Question 1 --- Based on Tautology

**Prove using a truth table that the following proposition is a
tautology:**

`(p ∧ q) → p`

**Step 1: Identify the propositions.**

There are two propositions, p and q. The number of possible combinations
is:

`2ⁿ = 2² = 4`

**Step 2: Construct the truth table.**

  p   q   `p ∧ q`   `(p ∧ q) → p`
  --- --- --------- ---------------
  T   T   T         **T**
  T   F   F         **T**
  F   T   F         **T**
  F   F   F         **T**

**Step 3: Observe the final column.**

The final column contains only True values.

**Conclusion:** `(p ∧ q) → p` is a **tautology**.

#### Another example

Determine whether `(p ∨ q) → (q ∨ p)` is a tautology.

  p   q   `p ∨ q`   `q ∨ p`   Result
  --- --- --------- --------- --------
  T   T   T         T         T
  T   F   T         T         T
  F   T   T         T         T
  F   F   F         F         T

All values in the final column are True. Therefore, it is a
**tautology**.

### Question 2 --- Based on Basic Logical Operations

Let:

-   p: 8 is an even number.
-   q: 9 is an even number.

Find the truth values of:

1.  `p ∧ q`
2.  `p ∨ q`
3.  `¬p`
4.  `¬q`
5.  `p → q`
6.  `p ↔ q`

**Step 1: Determine the truth values.**

-   8 is even, so `p = T`.
-   9 is even, which is false, so `q = F`.

Therefore, `p = T` and `q = F`.

**Step 2: Solve each operation.**

1.  Conjunction: `p ∧ q = T ∧ F = F`
2.  Disjunction: `p ∨ q = T ∨ F = T`
3.  Negation of p: `¬p = ¬T = F`
4.  Negation of q: `¬q = ¬F = T`
5.  Implication: `p → q = T → F = F`
6.  Biconditional: `p ↔ q = T ↔ F = F`

**Final answer:**

  Logical operation   Result
  ------------------- --------
  `p ∧ q`             F
  `p ∨ q`             T
  `¬p`                F
  `¬q`                T
  `p → q`             F
  `p ↔ q`             F

### Question 3 --- Tautology, Contradiction or Contingency

Determine whether the following proposition is a tautology,
contradiction or contingency:

`(p ∧ q) ∨ ¬p`

**Step 1:** There are two variables, p and q. The number of combinations
is `2² = 4`.

**Step 2: Construct the truth table.**

  p   q   `p ∧ q`   `¬p`   `(p ∧ q) ∨ ¬p`
  --- --- --------- ------ ----------------
  T   T   T         F      **T**
  T   F   F         F      **F**
  F   T   F         T      **T**
  F   F   F         T      **T**

**Step 3: Examine the final column.**

The final column contains three True values and one False value.

**Conclusion:** The expression is a **contingency** because it is
neither always True nor always False.

### Another solved example --- Contradiction

Determine whether the following is a tautology or contradiction:

`(p ∨ q) ∧ ¬(p ∨ q)`

Let `A = (p ∨ q)`. The expression becomes `A ∧ ¬A`.

  p   q   `p ∨ q`   `¬(p ∨ q)`   Final result
  --- --- --------- ------------ --------------
  T   T   T         F            **F**
  T   F   T         F            **F**
  F   T   T         F            **F**
  F   F   F         T            **F**

A proposition AND its negation is always False.

**Conclusion:** It is a **contradiction**.

## 13. Truth Table Construction

### 13.1 Number of rows

The number of rows depends on the number of distinct propositions:

**Number of rows = 2ⁿ**

where `n` is the number of distinct propositions.

    Number of propositions   Number of rows
  ------------------------ ----------------
                         1                2
                         2                4
                         3                8
                         4               16
                         5               32

For example, if an expression contains p, q and r:

`2³ = 8 rows`

### 13.2 Truth table for three propositions

  p   q   r
  --- --- ---
  T   T   T
  T   T   F
  T   F   T
  T   F   F
  F   T   T
  F   T   F
  F   F   T
  F   F   F

### 13.3 Order of operations

When solving a compound logical expression, follow this practical order:

1.  Parentheses `( )`
2.  Negation (NOT)
3.  Conjunction (AND)
4.  Disjunction (OR)
5.  Implication
6.  Biconditional

Always evaluate expressions inside parentheses first. Use intermediate
columns to avoid mistakes.

## 14. Practice Questions for Students

### A. Short-answer questions

1.  Define propositional logic with an example.
2.  What is a proposition?
3.  Differentiate between simple and compound propositions.
4.  What is a truth value?
5.  Define logical connectives.
6.  What is conjunction? Give an example.
7.  What is disjunction? Give an example.
8.  Define negation with a truth table.
9.  What is a tautology?
10. Differentiate between tautology and contradiction.

### B. Truth table questions

**Q1.** Construct the truth table for `p ∧ ¬q`.

**Q2.** Construct the truth table for `p ∨ ¬q`.

**Q3.** Construct the truth table for `¬(p ∧ q)`.

**Q4.** Construct the truth table for `(p ∨ q) ∧ p`.

**Q5.** Determine whether `p ∨ ¬p` is a tautology, contradiction or
contingency.

**Q6.** Determine whether `p ∧ ¬p` is a tautology, contradiction or
contingency.

**Q7.** Determine whether `(p → q) ∨ (q → p)` is a tautology,
contradiction or contingency.

**Q8.** Construct the truth table for `(p ∧ q) ∨ r`.

### C. Application-based questions

**Q1.** Let:

-   p: A student has completed the assignment.
-   q: A student has attended the practical class.

Write the following statements symbolically:

1.  The student has completed the assignment AND attended the practical
    class.
2.  The student has completed the assignment OR attended the practical
    class.
3.  The student has NOT completed the assignment.
4.  If the student has completed the assignment, then the student has
    attended the practical class.

**Q2.** Suppose `p = T`, `q = F`, and `r = T`. Find the truth values of:

1.  `p ∧ q`
2.  `p ∨ q`
3.  `¬q`
4.  `p ∧ q ∧ r`
5.  `p ∨ q ∨ r`
6.  `(p ∧ q) ∨ r`

## 15. Quick Revision

  Concept                Definition / rule                 Example
  ---------------------- --------------------------------- -----------
  Proposition            Statement having a truth value    5 is odd
  Truth value            True or False                     T or F
  Simple proposition     Single statement                  8 is even
  Compound proposition   Combination of statements         `p ∧ q`
  Conjunction            True when both are True           `p ∧ q`
  Disjunction            True when at least one is True    `p ∨ q`
  Negation               Reverses truth value              `¬p`
  Implication            Conditional statement             `p → q`
  Biconditional          Both have the same truth value    `p ↔ q`
  Tautology              Always True                       `p ∨ ¬p`
  Contradiction          Always False                      `p ∧ ¬p`
  Contingency            Sometimes True, sometimes False   `p ∧ q`

## 16. Important Points for Examinations

> ### Five rules to remember
>
> -   **AND (`∧`):** Both propositions must be True.
> -   **OR (`∨`):** At least one proposition must be True.
> -   **NOT (`¬`):** Reverses the truth value.
> -   **Tautology:** Final column contains all True values.
> -   **Contradiction:** Final column contains all False values.
>
> **Truth table rows:** For `n` distinct propositions, the number of
> rows is `2ⁿ`.

### Suggested lecture plan

-   **Lecture 1:** Introduction, propositions, truth values, types of
    propositions and logical connectives.
-   **Lecture 2:** Conjunction, disjunction, negation, tautology,
    contradiction and contingency.
-   **Practice session:** Truth tables, solved questions and student
    exercises.

------------------------------------------------------------------------

## 17. Self-Assessment Quiz

Try answering these questions without referring to the notes.

1.  Which of the following is a proposition?
    -   What is your name?
    -   Please sit down.
    -   5 + 3 = 8
    -   How beautiful!
2.  When is conjunction (`p ∧ q`) True?
    -   When both p and q are True
    -   When either is True
    -   When both are False
    -   When p is False
3.  What is the truth value of `T ∨ F`?
    -   False
    -   True
    -   Both
    -   Neither
4.  Which expression represents a tautology?
    -   `p ∧ ¬p`
    -   `p ∨ ¬p`
    -   `p ∧ q`
    -   `p → ¬p`
5.  Which expression represents a contradiction?
    -   `p ∨ q`
    -   `p → q`
    -   `p ∧ ¬p`
    -   `p ∨ ¬p`
6.  How many rows are required for three propositions?
    -   4
    -   6
    -   8
    -   16

### Answer key

    Question Correct answer
  ---------- ----------------------------
           1 5 + 3 = 8
           2 When both p and q are True
           3 True
           4 `p ∨ ¬p`
           5 `p ∧ ¬p`
           6 8

------------------------------------------------------------------------


