# Task 1 — Events (Union / Intersection / Difference)

## Given
$$
\Omega=\{\omega_1,\omega_2,\omega_3,\omega_4,\omega_5\}
$$
$$
A=\{\omega_1,\omega_3,\omega_5\},\quad B=\{\omega_2,\omega_3,\omega_4\}.
$$

## 1) $A\cup B$
Union means “in $A$ or in $B$ (or both)”, so we collect all elements:
$$
A\cup B=\{\omega_1,\omega_2,\omega_3,\omega_4,\omega_5\}=\Omega.
$$

## 2) $A\cap B$
Intersection means “in both $A$ and $B$”:
$$
A\cap B=\{\omega_3\}.
$$

## 3) $B\setminus A$
Elements in $B$ but not in $A$:
$$
B\setminus A=\{\omega_2,\omega_4\}.
$$

## 4) $A\setminus B$
Elements in $A$ but not in $B$:
$$
A\setminus B=\{\omega_1,\omega_5\}.
$$

## Final answers
$$
A\cup B=\Omega,\quad A\cap B=\{\omega_3\},\quad B\setminus A=\{\omega_2,\omega_4\},\quad A\setminus B=\{\omega_1,\omega_5\}.
$$


---

## Commentary

### Probability space (model)
- $\Omega$ is explicitly given.
- Elementary outcomes are the single symbols $\omega_i$.
- Events are subsets of $\Omega$ (here: $A$ and $B$). 

### Event meaning (plain language)
- $A\cup B$: in $A$ or in $B$.
- $A\cap B$: in both.
- $A^c$: not in $A$.
- $A\setminus B$: in $A$ but not in $B$. 

### Independence / conditional thinking
- Not used here (this task is pure event logic / set structure).

### Sanity checks
- $A\cap B\subseteq A$ and $A\cap B\subseteq B$.
- $A\cup B\subseteq \Omega$.
- $(A\setminus B)$ contains no elements from $B$.

### Reflection
- Core concept: events as sets and logical structure.