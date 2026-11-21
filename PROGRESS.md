# Proof progress

## 2026-11-21 · Revision `2026-11-21.4`

Folios 522ad–522ag are pages 591–594 of the [1,013-page edition][pdf4]. The test has fixed log support throughout.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [522ag · (53)][f522ag] | Pairs at distance at most $Y$ make an absolute contribution $O_{d,h}(Y)$. Along an unbounded sequence, pairs farther apart than a fixed positive multiple of $\log X$ supply at least half the diagonal term in negative signed contribution, with pole subtraction for the principal component. For ordinary zeta and both dihedral examples, the original correlation (45) vanishes at arbitrarily large separations. | [dbb1904][pairs] |
| [522af · (52)][f522af] | For each fixed Hecke character and all but finitely many frequencies in $[1,2]$, the ratio of the centered distinct-pair term to the diagonal has lower limit $-1$. A finite upper bound at all sufficiently large scales is equivalent to zero location for that character. | [dbb1904][pairs] |
| [522ae · (51)][f522ae] | The diagonal is of order $\log X$. Its leading coefficient, including the oscillation from the frequency shift, follows from the two character products on $F\otimes_{\mathbb Q} F$. | [dbb1904][pairs] |
| [522ad · (50)][f522ad] | The square of the centered real prime sum splits exactly into the diagonal and the signed contribution from distinct pairs. The prime sum recovers the real part of the translated trace up to bounded error. | [dbb1904][pairs] |

## 2026-11-21 · Revision `2026-11-21.3`

Folios 522z–522ac are pages 587–590 of the [1,009-page edition][pdf3]. Here $X$ is the central prime norm and $t=\log X$ is the separation of the two test functions.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [522ac · (49)][f522ac] | For ordinary zeta at fixed log support length $1/128$, the correlation bound holds for every $1\le X\le10^{19}e^{-1/128}$. The proof uses Büthe’s published square-root estimate for the Chebyshev function and an elementary bound at small $X$. | [41d0a7d][intervals] |
| [522ab · (48)][f522ab] | The Brun–Titchmarsh inequality gives positivity at every sufficiently large separation for all normalized unitary Hecke characters when the sampled prime interval has length comparable to $\sqrt X\log X$. The threshold is independent of field and character. | [41d0a7d][intervals] |
| [522aa · (47)][f522aa] | If the correlation bound holds at every large separation using widths $r_j$ with $\limsup j^{-1}\log(1/r_j)=\theta$, all zeros lie within $\theta$ of the critical line in real part. An independent bound for one sequence with $\log(1/r_j)=o(j)$ remains open for a fixed general character. | [41d0a7d][intervals] |
| [522z · (46)][f522z] | Splitting the dyadic uniforms that define the fixed test gives an exact positive-measure reconstruction from narrower tests. Its mass grows as $1/r$. At the widths established in (48), the resulting zero strip has half-width $1/2$. | [41d0a7d][intervals] |

## 2026-11-21 · Revision `2026-11-21.2`

Folios 522w–522y are pages 584–586 of this [1,005-page edition][pdf2]. They treat the full Weil form, including the terms at log norm zero.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [522y · (45)][f522y] | For one fixed smooth test, zero location for a given character is equivalent to bounding its correlation with every translate by its diagonal value. Equations (43)–(44) prove the bound for separations up to $1/64$ for every character. The bound at arbitrarily large separations for one fixed character remains open. | [f9159dc][positivity] |
| [522x · (43)–(44)][f522x] | If $R$ is the logarithm of the absolute conductor divided by the field degree, positivity holds for support lengths up to $(2-\epsilon)\log R$ whenever $0<\epsilon<2$ and $R$ is sufficiently large. The finite contribution uses only rational prime powers up to $e^L$, where $L$ is the support length. | [f9159dc][positivity] |
| [522w · (43)][f522w] | For every unitary Hecke character and every nonzero smooth test supported in a log interval of length at most $1/16$, the Weil quadratic form exceeds one quarter of the squared $L^2$ norm. The proof uses the archimedean integral, the finite conductor and the pole terms. | [f9159dc][positivity] |

## 2026-11-21 · Revision `2026-11-21.1`

The [1,002-page edition][pdf1] records the following results. Folio numbers are printed in the manuscript. Each source link opens the corresponding proof in this revision.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [522v · (42)][f522v] | For the cubic class character of the field of discriminant −23, the signed discrepancy between completely split and irreducible cubics among split rational primes takes both signs on the square-root scale, with the original smooth weight and no Gaussian average. | [4a9ad57][edition] |
| [522u · (41)][f522u] | The number of elements whose square is the identity determines the prime-square term in a completely split prime count. For the splitting field of $x^3-x-1$, the averaged principal prime error has leading term $-2 V_2(1/2)\sqrt X$ for each fixed $1/600\leq\kappa<1$. | [4a9ad57][edition] |
| [522r–522t · (39)–(40)][f522r] | For the fourth-power Gaussian angular character and the cubic ideal class character of discriminant −23, inert prime squares contribute the leading term $-V_2(1/2)\sqrt X/2$ to the averaged signed prime count. The range $1/600\leq\kappa<1$ uses published low-zero computations. The subrange $1/4\leq\kappa<1$ follows from the two eta products alone. | [4a9ad57][edition] |
| [522p–522q · (38)][f522p] | At fixed $\kappa$, a one-sided prime bound is equivalent to a parabolic constraint on the zeros. Only heights below $\sqrt{1/(2\kappa)+1/4}$ can violate it. The independent bound along a sequence $\kappa\downarrow0$ for each required character remains open. | [4a9ad57][edition] |
| [522l–522o · (35)–(37)][f522l] | A lower bound on weighted counts of principal prime ideals gives a zero-location criterion. Passing to a Galois closure preserves any offending zero. Equation (37) isolates the contribution from the maximal abelian subextension. | [4a9ad57][edition] |
| [522f–522h · (28)–(31)][f522f] | A CM elliptic curve gives a Gaussian Hecke zero of order at least three. A permitted norm section and a test satisfying the prescribed moments detect the missing multiplicity in the original (13.3.1.2). | [4a9ad57][edition] |
| [522–522b · (21)–(24)][f522] | One fixed smooth weight has nonzero Mellin transform throughout the open critical strip. Its square-root prime-sum bound is equivalent to RH over the rationals, with an analogous criterion for each unitary Hecke character. | [4a9ad57][edition] |
| [520c–520n · (20h), (20p), (20t)][f520c] | The prime sums reduce to balanced ideal factors. In the principal component the two terms of size $X/\log X$ in (20p) cancel. Equation (20t) bounds the contribution of indices with many prime factors in the nontrivial components. | [4a9ad57][edition] |
| [514a–514b · (17)][f514a] and [520 · (18)–(19)][f520] | The full-strip trace agrees with the classical explicit formula. Shrinking the strip loses the exterior zeros and any uncounted boundary multiplicity. Equation (18) computes the defect. Equation (19) is the independent geometric growth estimate still needed for zero location. | [4a9ad57][edition] |
| [495–495b · original (11.3.2.1), revised (14)–(16)][f495] | At the prime 2 the specified lift gives zero by Haar measure, while the proposed local term equals $\log 2$. Two normalized lifts assign different weights to the first shell while preserving the total trace. | [4a9ad57][edition] |
| [488a–489b · (13e)–(13j)][f488a] | Finite-level projections exhaust the indicated Hecke component. Reversing projection and convolution introduces the operator in (13g). Its cutoff trace vanishes in the limit by (13i), and the translated correction already satisfies the required growth rate by (13j). | [4a9ad57][edition] |
| [463–463b · (10)–(13a)][f463] | A Hilbert–Schmidt resolvent bound and the rank-one term from the weight at the origin give trace class and convergence of the cutoff traces without assuming a minimum zero spacing. | [4a9ad57][edition] |
| [446–446d · (4)–(9), original Theorem 10.2.2.1][f446] | Translates of an arithmetic theta generator span the closed space defined by the zero conditions. Formula (4) gives the exact boundary multiplicity at every strip width and Sobolev degree, including width zero. | [4a9ad57][edition] |
| [29 · (1)–(3)][f29] | Translating a compactly supported test and taking a Laplace transform produces a pole at each omitted zero. Equality of the full and narrow traces on all these tests forces the omitted set to be empty. | [4a9ad57][edition] |

[pairs]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/dbb190435bdd4a21e7ba4c37a3818b763af9495e
[pdf4]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/dbb190435bdd4a21e7ba4c37a3818b763af9495e/output/pdf/the-music-of-the-primes-revised.pdf
[f522ag]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/dbb190435bdd4a21e7ba4c37a3818b763af9495e/src/the-music-of-the-primes-revised.tex#L3758
[f522af]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/dbb190435bdd4a21e7ba4c37a3818b763af9495e/src/the-music-of-the-primes-revised.tex#L3709
[f522ae]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/dbb190435bdd4a21e7ba4c37a3818b763af9495e/src/the-music-of-the-primes-revised.tex#L3670
[f522ad]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/dbb190435bdd4a21e7ba4c37a3818b763af9495e/src/the-music-of-the-primes-revised.tex#L3627
[intervals]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/41d0a7dda379e7a0443c68e1dc35fd6c7d852266
[pdf3]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/41d0a7dda379e7a0443c68e1dc35fd6c7d852266/output/pdf/the-music-of-the-primes-revised.pdf
[f522ac]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/41d0a7dda379e7a0443c68e1dc35fd6c7d852266/src/the-music-of-the-primes-revised.tex#L3578
[f522ab]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/41d0a7dda379e7a0443c68e1dc35fd6c7d852266/src/the-music-of-the-primes-revised.tex#L3539
[f522aa]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/41d0a7dda379e7a0443c68e1dc35fd6c7d852266/src/the-music-of-the-primes-revised.tex#L3495
[f522z]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/41d0a7dda379e7a0443c68e1dc35fd6c7d852266/src/the-music-of-the-primes-revised.tex#L3453
[positivity]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/f9159dc95c748a43c0eefad4b801c9f993302220
[pdf2]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/f9159dc95c748a43c0eefad4b801c9f993302220/output/pdf/the-music-of-the-primes-revised.pdf
[f522y]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/f9159dc95c748a43c0eefad4b801c9f993302220/src/the-music-of-the-primes-revised.tex#L3400
[f522x]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/f9159dc95c748a43c0eefad4b801c9f993302220/src/the-music-of-the-primes-revised.tex#L3356
[f522w]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/f9159dc95c748a43c0eefad4b801c9f993302220/src/the-music-of-the-primes-revised.tex#L3307
[edition]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/4a9ad5765d4a2dfb237f874695ee4f4a07817867
[pdf1]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/output/pdf/the-music-of-the-primes-revised.pdf
[f522v]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L3256
[f522u]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L3203
[f522r]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L3059
[f522p]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L2959
[f522l]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L2759
[f522f]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L2471
[f522]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L2187
[f520c]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L1615
[f514a]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L1333
[f520]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L1476
[f495]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L1164
[f488a]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L784
[f463]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L482
[f446]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L260
[f29]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/4a9ad5765d4a2dfb237f874695ee4f4a07817867/src/the-music-of-the-primes-revised.tex#L161
