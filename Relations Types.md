
# Relations and Their Types (Properties)
 
## Introduction to Relations
 
A **relation** is a connection or association between the elements of two sets. A relation $R$ on a set $A$ is a subset of the Cartesian product $A \times A$.
 
**Example:**
 
Let $A = \{1,2,3\}$.
 
Then,
 
$$A \times A = \{(1,1),(1,2),(1,3),\ldots,(3,3)\}$$
 
Suppose we define a relation:
 
$$R = {(1,1),(2,2),(3,3),(1,2),(2,3)}$$
 
---
 
## Types of Relations
 
### 1. Reflexive Relation
 
**Definition:** A relation $R$ on a set $A$ is called reflexive if every element of the set is related to itself.
 
**Mathematical expression:**
 
$$\forall a \in A,\quad (a,a) \in R$$
 
Here, $\forall$ means "for all".
 
**Example:**
 
Let $A=\{1,2,3\}$.
 
$$R=\{(1,1),(2,2),(3,3),(1,2)\}$$
 
This relation is reflexive because all elements are related to themselves:
 
- $(1,1)$ is present.
- $(2,2)$ is present.
- $(3,3)$ is present.
**Key point:** All diagonal pairs must be present.
 
**Real-life example:** Every person is equal to themselves.
 
---
 
### 2. Irreflexive Relation
 
**Definition:** A relation $R$ on a set $A$ is called irreflexive if no element is related to itself.
 
**Mathematical expression:**
 
$$\forall a \in A,\quad (a,a) \notin R$$
 
**Example:**
 
Let $A=\{1,2,3\}$.
 
$$R=\{(1,2),(1,3),(2,3)\}$$
 
This relation is irreflexive because none of the following pairs exists:
 
- $(1,1)$
- $(2,2)$
- $(3,3)$
**Key point:** No diagonal pairs are present.
 
**Real-life example:** The relation "is greater than" ($>$).
 
A number cannot be greater than itself. For example, $5>5$ is false.
 
---
 
### 3. Symmetric Relation
 
**Definition:** A relation $R$ on a set $A$ is called symmetric if whenever an element $a$ is related to $b$, then $b$ must also be related to $a$.
 
**Mathematical expression:**
 
$$\forall a,b \in A,\quad (a,b) \in R \Rightarrow (b,a) \in R$$
 
**Example:**
 
Let $A=\{1,2,3\}$.
 
$$R=\{(1,2),(2,1),(2,3),(3,2)\}$$
 
This relation is symmetric because:
 
- $(1,2)$ exists, and $(2,1)$ also exists.
- $(2,3)$ exists, and $(3,2)$ also exists.
**Key point:** Every ordered pair must have its reverse pair.
 
**Real-life example:** The relation "is a friend of".
 
If A is a friend of B, then B is a friend of A (assuming friendship is mutual).
 
---
 
### 4. Antisymmetric Relation
 
**Definition:** A relation $R$ on a set $A$ is called antisymmetric if whenever $a$ is related to $b$ and $b$ is related to $a$, then both elements must be equal.
 
**Mathematical expression:**
 
$$\forall a,b \in A,\quad [(a,b) \in R \land (b,a) \in R] \Rightarrow a=b$$
 
**Example:**
 
Let $A=\{1,2,3\}$.
 
$$R=\{(1,1),(2,2),(3,3),(1,2),(1,3)\}$$
 
This relation is antisymmetric because:
 
- $(1,2)$ exists, but $(2,1)$ does not exist.
- $(1,3)$ exists, but $(3,1)$ does not exist.
- The reverse pairs of the diagonal pairs are themselves.
Therefore, there are no two distinct elements related in both directions.
 
**Key point:** Two different elements cannot be related in both directions.
 
**Real-life example:** The relation "less than or equal to" ($\leq$).
 
If $a \leq b$ and $b \leq a$, then $a=b$.
 
---
 
### 5. Asymmetric Relation
 
**Definition:** A relation $R$ on a set $A$ is called asymmetric if whenever $a$ is related to $b$, then $b$ cannot be related to $a$.
 
**Mathematical expression:**
 
$$\forall a,b \in A,\quad (a,b) \in R \Rightarrow (b,a) \notin R$$
 
**Example:**
 
Let $A=\{1,2,3\}$.
 
$$R=\{(1,2),(1,3),(2,3)\}$$
 
This relation is asymmetric because:
 
- $(1,2)$ exists, but $(2,1)$ does not.
- $(1,3)$ exists, but $(3,1)$ does not.
- $(2,3)$ exists, but $(3,2)$ does not.
**Key point:** If one direction exists, the reverse direction must not exist.
 
**Real-life example:** The relation "is taller than".
 
If A is taller than B, then B cannot be taller than A.
 
> **Important:** Every asymmetric relation is irreflexive, but not every irreflexive relation is asymmetric.
 
---
 
### 6. Transitive Relation
 
**Definition:** A relation $R$ on a set $A$ is called transitive if whenever an element $a$ is related to $b$, and $b$ is related to $c$, then $a$ must also be related to $c$.
 
**Mathematical expression:**
 
$$\forall a,b,c \in A,\quad [(a,b) \in R \land (b,c) \in R] \Rightarrow (a,c) \in R$$
 
**Example:**
 
Let $A=\{1,2,3\}$.
 
$$R=\{(1,2),(2,3),(1,3)\}$$
 
This relation is transitive because:
 
- $(1,2)$ exists.
- $(2,3)$ exists.
- Therefore, $(1,3)$ must exist, and it does.
**Key point:** If two consecutive relationships exist, the direct relationship must also exist.
 
**Real-life example:** The relation "less than" ($<$).
 
If:
 
$$2<5 \quad \text{and} \quad 5<8$$
 
Then:
 
$$2<8$$
 
Therefore, the relation is transitive.
 
---
 
## Comparison of All Six Properties
 
| Property      | Main condition                    | Example        |
| ------------- | --------------------------------- | -------------- |
| Reflexive     | Every element relates to itself   | $a=a$          |
| Irreflexive   | No element relates to itself      | $a<a$ (false)  |
| Symmetric     | Reverse pair must exist           | Friendship     |
| Antisymmetric | Both directions imply equality    | $\leq$         |
| Asymmetric    | Reverse pair must not exist       | $<$            |
| Transitive    | Two relationships imply a third   | $<$            |
 
---
 
## Important Differences for Examinations
 
These differences are particularly important for understanding and solving questions in Discrete Mathematics.
 
| Symmetric                     | Antisymmetric                                            | Asymmetric                       |
| ----------------------------- | -------------------------------------------------------- | -------------------------------- |
| Reverse pair must exist.      | Reverse pair can exist only when elements are equal.     | Reverse pair must never exist.   |
| $(1,2)$ requires $(2,1)$.     | $(1,2)$ and $(2,1)$ cannot both exist for distinct elements. | $(1,2)$ prohibits $(2,1)$.  |
| Diagonal pairs are allowed.   | Diagonal pairs are allowed.                              | Diagonal pairs are not allowed.  |
 
### Remember these important facts
 
1. Every reflexive relation contains all diagonal pairs.
2. Every irreflexive relation contains no diagonal pairs.
3. Every asymmetric relation is irreflexive.
4. Every asymmetric relation is antisymmetric.
5. A relation can be both symmetric and antisymmetric.
6. A relation can be both reflexive and symmetric.
7. A relation can be neither symmetric nor antisymmetric.
---
 
## Practice MCQs
 
**Q1.** Let $A = \{1,2,3\}$ and $R = \{(1,1),(2,2),(3,3)\}$. Which property does $R$ satisfy?
 
- A. Reflexive
- B. Irreflexive
- C. Asymmetric
**Correct answer:** A. Reflexive
 
**Explanation:** All three diagonal pairs are present, so $R$ is reflexive.
 
---
 
**Q2.** $R = \{(1,2),(2,1)\}$. Which property does this relation satisfy?
 
- A. Asymmetric
- B. Symmetric
- C. Irreflexive only
**Correct answer:** B. Symmetric
 
**Explanation:** Both $(1,2)$ and its reverse $(2,1)$ are present, so it is symmetric.
 
---
 
**Q3.** If $aRb$ and $bRa$ imply $a = b$, which property is satisfied?
 
- A. Symmetric
- B. Transitive
- C. Antisymmetric
**Correct answer:** C. Antisymmetric
 
**Explanation:** This is the definition of an antisymmetric relation.
 
---
 
**Q4.** The relation "greater than ($>$)" on integers is:
 
- A. Reflexive
- B. Asymmetric
- C. Symmetric
**Correct answer:** B. Asymmetric
 
**Explanation:** If $a > b$, then $b$ cannot be greater than $a$. It is asymmetric.
 
---
 
**Q5.** If $(1,2)$ and $(2,3)$ are in $R$, which pair must exist for transitivity?
 
- A. $(3,1)$
- B. $(2,1)$
- C. $(1,3)$
**Correct answer:** C. $(1,3)$
 
**Explanation:** Transitivity requires $(1,3)$ to be present.
 
