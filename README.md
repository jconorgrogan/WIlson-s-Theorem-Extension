# Wilson-s-Theorem-Extension

### Theorem (Extended Wilson-Set Theorem)

Let \( n \) be a positive integer, and let \( S = \{1, 2, \ldots, n-1\} \).

1. Define \( G: Perm(S) \to \mathbb{Z}/n\mathbb{Z} \) by \( G(\sigma) = (\prod_{k=1}^{n-1} \sigma(k)) \mod n \).

2. Define \( R = \{ G(\sigma) : \sigma \in Perm(S) \} \).

#### Statement 1
\( n \) is prime if and only if \( R \) is closed under multiplication mod \( n \) and every non-zero element in \( R \) has a unique multiplicative inverse in \( R \).

#### Statement 2
\( R \) contains exactly one element \( r \) such that \( r = -1 \mod n \) if and only if \( n \) is prime.

### Proof

1. **Forward Direction**: 
    - Closure and Invertibility are inherited from \( S \), which is a group mod \( n \) when \( n \) is prime.

2. **Reverse Direction**: Assume \( R \) is closed and invertible.
    - **Closure Implication**: For any \( a, b \in R \), \( ab \in R \). This implies that \( R \) is a subgroup of \( \mathbb{Z}/n\mathbb{Z} \). If \( n \) were composite, this subgroup would contain non-trivial divisors, breaking closure.
    - **Invertibility Implication**: Each \( a \in R \) has a unique inverse. This would not be the case if \( n \) were composite, as elements co-prime to \( n \) wouldn't guarantee unique inverses in \( R \).
    - **Statement 2**: If \( R \) contains exactly one \( r = -1 \mod n \), then by the property of \( R \) being invertible, \( n \) must be prime.

