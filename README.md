# Extended Wilson-Set Theorem 

## Definitions

1. **Function \( G \)**
    - \( G: Perm(S) \rightarrow \mathbb{Z}/n\mathbb{Z} \) where \( G(\sigma) = \left( \prod_{k=1}^{n-1} \sigma(k) \right) \mod n \).

2. **Set \( R \)**
    - \( R = \{ G(\sigma) \,|\, \sigma \in Perm(S) \} \).

## Statement 1

\( n \) is prime if and only if \( R \) is closed under multiplication mod \( n \) and every non-zero element in \( R \) has a unique multiplicative inverse in \( R \).

### Proof for Statement 1

1. **Forward Direction**
    - **Invertibility**: Given \( a = G(\sigma) \), consider \( a^{-1} \mod n \). Utilizing Fermat's Little Theorem, \( a^{n-2} \equiv a^{-1} \mod n \) for \( \gcd(a, n) = 1 \). The inverse permutation \( \sigma^{-1} \) must satisfy \( G(\sigma^{-1}) = a^{-1} \mod n \). This is proven as \( a \times a^{-1} \equiv (\prod_{k=1}^{n-1} \sigma(k)) \times (\prod_{k=1}^{n-1} \sigma^{-1}(k)) \equiv 1 \mod n \).

2. **Reverse Direction**
    - **Closure Implication**: Assume \( n \) is composite with \( n = d \times e \) where \( 1 < d, e < n \). For \( \sigma_d \) and \( \sigma_e \) in \( Perm(S) \), assume \( G(\sigma_d) = d \) and \( G(\sigma_e) = e \). Then \( d \times e \mod n = 0 \), violating closure.

    - **Invertibility Implication**: For \( n \) composite, Euler's theorem states \( a^{\phi(n)} \equiv 1 \mod n \). Given \( a, b \) coprime to \( n \), their inverses are \( a^{\phi(n)-1} \) and \( b^{\phi(n)-1} \). A concrete example with \( n = 15 \) shows that \( 2^{7-1} = 7^{7-1} \), proving the non-uniqueness of inverses when \( n \) is composite.

## Statement 2

\( R \) contains exactly one \( r \) where \( r = -1 \mod n \) if and only if \( n \) is prime.

### Proof for Statement 2

1. **Forward Direction**: By Wilson's theorem, \( (n-1)! \equiv -1 \mod n \), thus \( R \) contains exactly one \( r \) where \( r = -1 \mod n \).

2. **Reverse Direction**: Assume \( R \) contains only one \( r \) where \( r = -1 \mod n \). If \( n \) is composite, then \( \phi(n) < n - 1 \). Utilize the Chinese Remainder Theorem to argue that \( f_1 \) and \( f_2 \), distinct factors of \( (n - 1)! \) that are coprime to \( n \), yield \( f_1 \equiv f_2 \equiv -1 \mod n \). The CRT guarantees that \( f_1 \) and \( f_2 \) result in distinct \( r \)'s in \( R \), contradicting the assumption.
