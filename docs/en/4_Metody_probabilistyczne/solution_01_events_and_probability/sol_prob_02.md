# Task 2 — Circuit reliability as events

## Given
- $A_i$ = event “element $a_i$ works at time $t$”, for $i=1,2,3$.
- $a_1$ is in **series** with a block where $a_2$ and $a_3$ are **parallel**.

## Required
Describe event $A$: “during time interval $t$, current flow is not interrupted”.

## Solution (logic)
- **Series** part: the circuit needs $a_1$ to work  $\Rightarrow$ must have $A_1$.
- **Parallel** block: at least one of $a_2$ or $a_3$ works $\Rightarrow$ need $(A_2\cup A_3)$.

So the whole circuit works when:
$$
A = A_1 \cap (A_2 \cup A_3).
$$

Equivalent expanded form:
$$
A=(A_1\cap A_2)\cup(A_1\cap A_3).
$$

## Final answer
$$
A = A_1 \cap (A_2 \cup A_3).
$$
