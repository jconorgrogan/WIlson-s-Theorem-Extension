### Extended Wilson-Set Theorem 

Let \( n \) be a positive integer, and let \( S = \{1, 2, \ldots, n-1\} \).

1. **Function \( G \)**
    - Define \( G: Perm(S) \rightarrow \mathbb{Z}/n\mathbb{Z} \) as \( G(\sigma) = \left( \prod_{k=1}^{n-1} \sigma(k) \right) \mod n \).

2. **Set \( R \)**
    - Define \( R = \{ G(\sigma) \,|\, \sigma \in Perm(S) \} \).

#### Statement 1
\( n \) is prime if and only if \( R \) is closed under multiplication mod \( n \) and every non-zero element in \( R \) has a unique multiplicative inverse in \( R \).

#### Statement 2
\( R \) contains exactly one \( r \) where \( r = -1 \mod n \) if and only if \( n \) is prime.

---

### Proof

1. **Forward Direction**
    - **Closure**: Assume \( n \) is prime. For any \( a, b \in R \), \( ab \mod n = G(\sigma_1)G(\sigma_2) \mod n = G(\sigma_1 \circ \sigma_2) \mod n \). This shows \( R \) is closed.
    - **Invertibility**: In \( \mathbb{Z}/n\mathbb{Z} \), every \( a \) has an inverse \( a^{-1} \) under multiplication when \( n \) is prime. Therefore, \( a^{-1} \mod n \) exists in \( R \) as well, demonstrating invertibility.

2. **Reverse Direction**
    - **Closure Implication**: If \( R \) is closed, \( R \) forms a subgroup of \( \mathbb{Z}/n\mathbb{Z} \). If \( n \) is composite, this subgroup would necessarily include non-trivial divisors, contradicting the assumption that \( R \) is closed.
    - **Invertibility Implication**: If each \( a \in R \) has a unique inverse, \( n \) cannot be composite. In composite \( n \), the set \( R \) could contain elements that share an inverse, which would contradict our assumption of unique inverses.
