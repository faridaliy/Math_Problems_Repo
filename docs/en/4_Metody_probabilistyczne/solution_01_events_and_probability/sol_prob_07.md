# Task 7 — Noisy binary channel (3-bit messages)

## Given
Only two messages are transmitted:
$$
P(S=111)=0.65,\quad P(S=000)=0.35,
$$
where $S$ is the sent (transmitted) 3-bit signal.

Noise model (independent for each bit):
- $1\to 0$ with probability $0.2$, so $1\to 1$ with probability $0.8$
- $0\to 1$ with probability $0.2$, so $0\to 0$ with probability $0.8$

Let $R$ be the received 3-bit signal.

## 1) Find $P(R=111)$
Use total probability over the two possible sent signals:

If $S=111$, to receive $111$ all three bits must stay 1:
$$
P(R=111\mid S=111)=0.8^3=0.512.
$$

If $S=000$, to receive $111$ all three bits must flip 0→1:
$$
P(R=111\mid S=000)=0.2^3=0.008.
$$

Therefore:
$$
P(R=111)=0.65\cdot 0.512 + 0.35\cdot 0.008
=0.3328+0.0028=0.3356.
$$

## 2) Find $P(R=000)$
If $S=111$, to receive $000$ all bits must flip 1→0:
$$
P(R=000\mid S=111)=0.2^3=0.008.
$$

If $S=000$, to receive $000$ all bits must stay 0:
$$
P(R=000\mid S=000)=0.8^3=0.512.
$$

So:
$$
P(R=000)=0.65\cdot 0.008 + 0.35\cdot 0.512
=0.0052+0.1792=0.1844.
$$

## 3) Find $P(R=010)$
Compute conditional probabilities:

From $S=111$ to get $010$:
- first bit: 1→0 (0.2)
- second bit: 1→1 (0.8)
- third bit: 1→0 (0.2)
$$
P(R=010\mid S=111)=0.2\cdot 0.8\cdot 0.2=0.032.
$$

From $S=000$ to get $010$:
- first bit: 0→0 (0.8)
- second bit: 0→1 (0.2)
- third bit: 0→0 (0.8)
$$
P(R=010\mid S=000)=0.8\cdot 0.2\cdot 0.8=0.128.
$$

Total probability:
$$
P(R=010)=0.65\cdot 0.032 + 0.35\cdot 0.128
=0.0208+0.0448=0.0656.
$$

## Final answers
$$
P(R=111)=0.3356,\quad P(R=000)=0.1844,\quad P(R=010)=0.0656.
$$

## Commentary

### Probability space (model)
- Hidden sent signal: $S\in\{111,000\}$ with given prior probabilities.
- Observed received signal: $R$. 

### Conditional structure
- Compute $P(R=r)$ by conditioning on what was sent (total probability). 

### Independence check
- Multiplying bit probabilities is valid only because bit errors are assumed independent. 

### Sanity checks
- More flips required → smaller conditional probability (typically).
- Result must be in [0,1].

### Reflection
- Core concept: conditional modeling + independence justification.
