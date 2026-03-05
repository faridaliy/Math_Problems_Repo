# Task 4 — Two parallel elements

## Given
Two elements $a_1,a_2$ are connected in parallel.

Let:
- $A_i$ = event “element $a_i$ works for at least time $t$”
- $P(A_1)=P(A_2)=p$
- $P(A_1\cap A_2)=p^2$

## Required
Find the probability that current flows for at least time $t$.

## Solution
In a parallel connection, current flows if at least one element works:
$$
A = A_1 \cup A_2.
$$

Use the union formula:
$$
P(A_1\cup A_2)=P(A_1)+P(A_2)-P(A_1\cap A_2).
$$

Substitute the given values:
$$
P(A)=p+p-p^2=2p-p^2.
$$

Equivalent form (sometimes nicer):
$$
P(A)=1-(1-p)^2.
$$

## Final answer
$$
P(\text{current flows}) = 2p - p^2.
$$


---

## Commentary

### Probability space (model)
- Outcomes describe whether each component works/fails.
- Event of interest: “system works” in parallel = at least one works. 

### Independence check (explicit)
- Given $P(A_1\cap A_2)=p^2$ and $P(A_1)=P(A_2)=p$,
  so $P(A_1\cap A_2)=P(A_1)P(A_2)$ ⇒ independence is justified. 

### Sanity checks
- If $p=0$ then system works with probability 0.
- If $p=1$ then system works with probability 1.

### Reflection
- Core concept: independence must be justified before multiplication.