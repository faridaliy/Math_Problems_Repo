# Task 9 — One item from each plant, then choose one at random

## Given
Three plants produce first-quality items with probabilities:
$$
p_1=0.97,\quad p_2=0.90,\quad p_3=0.86.
$$

We have 3 items total: one from each plant.
Then one of these three items is chosen uniformly at random.

## Required
Find the probability that the chosen item is first-quality.

## Solution
Let $P_i$ be the event “the chosen item came from plant $i$”.
Since the choice is uniform among the 3 items:
$$
P(P_1)=P(P_2)=P(P_3)=\frac{1}{3}.
$$

By the law of total probability:
$$
P(\text{first-quality})=\sum_{i=1}^3 P(\text{first-quality}\mid P_i)\,P(P_i).
$$

Here $P(\text{first-quality}\mid P_i)=p_i$, so:
$$
P(\text{first-quality})=\frac{1}{3}(p_1+p_2+p_3)
=\frac{1}{3}(0.97+0.90+0.86)
=\frac{2.73}{3}=0.91.
$$

## Final answer
$$
P(\text{first-quality})=0.91.
$$


---

## Commentary

### Probability space (model)
- Hidden choice: which plant the chosen item came from (1,2,3).
- Because one item from each plant and uniform choice: each plant has probability 1/3.

### Conditional thinking
- Total probability: overall quality probability is a weighted sum (here equal weights). 

### Sanity checks
- Result must lie between min and max of the plant probabilities.

### Reflection
- Core concept: total probability as weighted averaging.
- What changes if plants provide different counts? weights are not equal.