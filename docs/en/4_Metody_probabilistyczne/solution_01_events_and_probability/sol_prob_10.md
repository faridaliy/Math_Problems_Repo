# Task 10 — 4-letter channel with confusion probabilities

## Given
Only three sequences can be transmitted:
$$
P(S=AAAA)=0.4,\quad P(S=BBBB)=0.3,\quad P(S=CCCC)=0.3,
$$
where $S$ is the transmitted 4-letter sequence.

Single-letter transition probabilities (independent for each position):
- If transmit $A$: receive $A$ with $0.8$, $B$ with $0.1$, $C$ with $0.1$
- If transmit $B$: receive $A$ with $0.1$, $B$ with $0.8$, $C$ with $0.1$
- If transmit $C$: receive $A$ with $0.1$, $B$ with $0.1$, $C$ with $0.8$

Let $R$ be the received 4-letter sequence.

## Key idea
Use total probability over the three possible transmitted sequences:
$$
P(R=r)=\sum_{s\in\{AAAA,BBBB,CCCC\}} P(S=s)\,P(R=r\mid S=s).
$$
Because positions are independent:
$$
P(R=r\mid S=s)=\prod_{k=1}^4 P(r_k\mid s_k).
$$

---

## 1) Find $P(R=AAAA)$

### If $S=AAAA$
All four letters must stay $A$:
$$
P(R=AAAA\mid S=AAAA)=0.8^4=0.4096.
$$

### If $S=BBBB$
Each $B$ must be received as $A$:
$$
P(R=AAAA\mid S=BBBB)=0.1^4=0.0001.
$$

### If $S=CCCC$
Each $C$ must be received as $A$:
$$
P(R=AAAA\mid S=CCCC)=0.1^4=0.0001.
$$

Total probability:
$$
P(R=AAAA)=0.4\cdot 0.4096 + 0.3\cdot 0.0001 + 0.3\cdot 0.0001
=0.16384+0.00003+0.00003=0.16390.
$$

---

## 2) Find $P(R=ACAA)$

### If $S=AAAA$
Need $A\to A$, $A\to C$, $A\to A$, $A\to A$:
$$
P(R=ACAA\mid S=AAAA)=0.8\cdot 0.1\cdot 0.8\cdot 0.8=0.0512.
$$

### If $S=BBBB$
Need $B\to A$, $B\to C$, $B\to A$, $B\to A$:
$$
P(R=ACAA\mid S=BBBB)=0.1\cdot 0.1\cdot 0.1\cdot 0.1=0.0001.
$$

### If $S=CCCC$
Need $C\to A$, $C\to C$, $C\to A$, $C\to A$:
$$
P(R=ACAA\mid S=CCCC)=0.1\cdot 0.8\cdot 0.1\cdot 0.1=0.0008.
$$

Total probability:
$$
P(R=ACAA)=0.4\cdot 0.0512 + 0.3\cdot 0.0001 + 0.3\cdot 0.0008
=0.02048+0.00003+0.00024=0.02075.
$$

## Final answers
$$
P(R=AAAA)=0.16390,\quad P(R=ACAA)=0.02075.
$$
