# Task 8 — Random arrangement of pulses (A, B, C)

## Given
There are 7 pulses in total:
- 4 pulses of type $A$
- 2 pulses of type $B$
- 1 pulse of type $C$

All arrangements are equally likely, which is equivalent to drawing pulses randomly **without replacement**.

## 1) Probability that the first pulse is $A$
The first position is equally likely to be any of the 7 pulses.
There are 4 pulses of type $A$, so:
$$
P(\text{first is }A)=\frac{4}{7}.
$$

## 2) Probability that the first pulse is $A$ or $C$
There are $4$ pulses of type $A$ and $1$ pulse of type $C$, so $5$ favorable pulses out of $7$:
$$
P(\text{first is }A \text{ or } C)=\frac{5}{7}.
$$

## 3) Probability that the first two pulses are $A$ then $C$
This is a draw without replacement:
- first is $A$: $\frac{4}{7}$
- after that, 6 pulses remain and only 1 is $C$: $\frac{1}{6}$

So:
$$
P(A\text{ then }C)=\frac{4}{7}\cdot\frac{1}{6}
=\frac{4}{42}=\frac{2}{21}.
$$

## Final answers
$$
\frac{4}{7},\quad \frac{5}{7},\quad \frac{2}{21}.
$$


---

## Commentary

### Probability space (model)
- Outcomes are pulse types appearing in the first position (or first two positions).

### Conditional thinking (informal)
- “Without replacement” means the second draw is conditional on the first draw:
  the denominator changes from 7 to 6.

### Independence check
- Not independent draws (because without replacement).
  That is why we update counts after the first draw.

### Sanity checks
- Probability(first is A or C) must be larger than probability(first is A).
- Two-step probability must be ≤ first-step probability. 

### Reflection
- Core concept: modeling sequential draws correctly (dependence).