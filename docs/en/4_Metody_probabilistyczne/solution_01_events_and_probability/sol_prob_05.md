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

## What he can ask (quick answers)
- **Why is $A'\cap B'$ equal to $(A\cup B)'$?** De Morgan’s law: “not A and not B” equals “not (A or B)”.
- **What would $P(A\setminus B)$ be?**
$$
P(A\setminus B)=P(A)-P(A\cap B)=0.6-0.5=0.1.
$$
- **Are $A$ and $B$ independent here?** No, because $P(A\cap B)=0.5$ but $P(A)P(B)=0.42$.