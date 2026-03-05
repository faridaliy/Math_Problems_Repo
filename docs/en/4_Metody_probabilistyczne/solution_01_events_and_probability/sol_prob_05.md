# Task 5 — Complements, intersection, and De Morgan

## Given
$$
P(A)=0.6,\quad P(B)=0.7,\quad P(A\cup B)=0.8.
$$

## 1) Find $P(A')$
By complement rule:
$$
P(A') = 1 - P(A) = 1 - 0.6 = 0.4.
$$

## 2) Find $P(A\cap B)$
Use inclusion–exclusion:
$$
P(A\cup B)=P(A)+P(B)-P(A\cap B).
$$
So:
$$
P(A\cap B)=P(A)+P(B)-P(A\cup B)
=0.6+0.7-0.8=0.5.
$$

## 3) Find $P(A'\cap B')$
By De Morgan's law, $A'\cap B'=(A\cup B)'$, hence:
$$
P(A'\cap B') = 1 - P(A\cup B) = 1 - 0.8 = 0.2.
$$

## Final answers
$$
P(A')=0.4,\quad P(A\cap B)=0.5,\quad P(A'\cap B')=0.2.
$$

---

## Commentary

### Probability space (model)
- Abstract events $A$ and $B$; focus is on probability laws.

### Event meaning (plain language)
- $A^c$: not $A$.
- $A^c\cap B^c$: neither $A$ nor $B$.
- By De Morgan: $A^c\cap B^c=(A\cup B)^c$. 

### Independence check
- Independence is NOT assumed unless stated.
- You should never replace $P(A\cap B)$ by $P(A)P(B)$ automatically. 

### Sanity checks
- $P(A\cap B)\le \min(P(A),P(B))$.
- $P(A\cup B)\ge \max(P(A),P(B))$.

### Reflection
- Core concept: additivity via inclusion–exclusion + De Morgan logic.