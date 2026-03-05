# Task 6 — Total probability and Bayes

## Given
Two machines produce items in ratio $3:2$ (machine 1 : machine 2), so:
$$
P(M_1)=\frac{3}{5},\quad P(M_2)=\frac{2}{5}.
$$

First-grade probabilities:
$$
P(F\mid M_1)=0.65,\quad P(F\mid M_2)=0.85,
$$
where $F$ means “the product is first-grade”.

## 1) Find $P(F)$
By the law of total probability:
$$
P(F)=P(F\mid M_1)P(M_1)+P(F\mid M_2)P(M_2).
$$

Compute:
$$
P(F)=0.65\cdot\frac{3}{5}+0.85\cdot\frac{2}{5}
=0.65\cdot 0.6 + 0.85\cdot 0.4
=0.39+0.34=0.73.
$$

## 2) Find $P(M_1\mid F)$
By Bayes' theorem:
$$
P(M_1\mid F)=\frac{P(F\mid M_1)P(M_1)}{P(F)}
=\frac{0.65\cdot\frac{3}{5}}{0.73}
=\frac{0.39}{0.73}
=\frac{39}{73}\approx 0.534.
$$

## Final answers
$$
P(F)=0.73,\quad P(M_1\mid F)=\frac{39}{73}\approx 0.534.
$$