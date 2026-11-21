# The Music of the Primes

**21 November 2026.** The audit of Alessandro Maria Masullo’s 940-page manuscript closes with revision `2026-11-21.16` (1,060 pages). The full critical strip admits a trace formula. The proposed passage to a narrow strip fails, and the manuscript does not establish Hecke GRH.

**Current research question.** Can an iterated unitary theta lift retain the cubic ideal-class character of $K=\mathbb Q(\sqrt{-23})$ in its first double-step Bessel period? For the splitting field $M$ of $x^3-x-1$, one has $\zeta_M(s)=\zeta_K(s)L_K(s,\psi)^2$. The zeros of this last factor give the nonabelian part of ERH for $M$. This project studies the unitary-group construction separately from Masullo’s $\mathrm{GL}_1$ argument. [Active problem and its first test](OPEN_PROBLEMS.md) · [Serre’s weight-one example, §5.3](https://www.math.mcgill.ca/goren/SeminarOnCohomology/Serre.pdf)

[Original manuscript (PDF)](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf) · [Revised manuscript (PDF)](output/pdf/the-music-of-the-primes-revised.pdf) · [Editable revision (TeX)](src/the-music-of-the-primes-revised.tex) · [Dated results and proofs](PROGRESS.md)

## Findings of the manuscript audit

The revision identifies the arithmetic theta space with the closed space defined by the zero conditions, including the boundary multiplicities. A resolvent bound gives the projected convolution trace without a zero-spacing assumption. Comparison with Weil’s explicit formula gives the full-strip trace, and a residue detects each zero omitted on narrowing the strip. The finite-place semilocal trace has uniform error $O(Y/L)$ as the prime cutoff $Y$ grows. With $Y=e^2X$ and $L=X^2$ this error is $O(X^{-1})$. [Spectral trace, folios 446–463b](src/the-music-of-the-primes-revised.tex#L261) · [Uniform cutoff, folio 518i](src/the-music-of-the-primes-revised.tex#L2694)

| Folios | Obstruction in the original proof |
| --- | --- |
| 495–495b | At $p=2$, (11.3.2.1) gives $0$ on the left and $\log 2$ on the right. A single normalized norm-translation-invariant lift cannot recover the two required prime distributions. |
| 516, 518a–518d | The mixed additive cutoff fails to preserve the stated Schwartz–Bruhat space. The real lower endpoint contributes in the balanced regime, and a one-sided cutoff retains a small-norm term outside the range of polar-free lifts. |
| 518j, (17.12) | On one fixed smooth input the semilocal Fourier transforms have narrow-space norm at least $\exp(c_bY^{1/2+b}/\log Y)$ for $0<b<\alpha<1/2$. This rules out the proposed operator limit in that space. |
| 522e–522h | The full-strip formula accommodates zeros outside any narrower strip. A Hecke zero over $\mathbb Q(i)$ of order at least three contradicts the multiplicity cap of two in Chapter 13. |

These counterexamples rule out the indicated steps of the proof. The single-$L$-function calculation in §12.3 ends at (17.4s), an open bound for a signed prime sum. [Archived criterion, folio 514x](src/the-music-of-the-primes-revised.tex#L2314)

## The $S_3$ prototype

The methodological reference is Levent Alpöge’s November 2026 outline of a Dirichlet GRH argument. The source-level comparison uses a fixed revision of the external Lean project. An independent full rebuild is outside the scope of this audit. [Alpöge’s outline, p. 4](https://alpo.ge/remark.pdf#page=4) · [Lean source revision](https://github.com/TomasOrtega/RH/tree/a6ac91a412dcbaab31801355ec5707024a71bf65)

Two features prevent a direct specialization. First, the rational cyclotomic reciprocity map `recOf` cannot distinguish the identity of $S_3$ from a three-cycle for all primes. For example, $13\equiv59\pmod{23}$ while the standard character has $a_{13}=-1$ and $a_{59}=2$. Second, $M/\mathbb Q$ is Galois and totally imaginary, but complex conjugation is noncentral, so $M$ is not a CM field. The auxiliary tower also requires a distinguished element of two-power order and a prime $d$ growing with the window. [Reciprocity map](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Formalism/SharpRestriction/GlobalSchurBounds/TieGlobal.lean#L24) · [Tower generator](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Formalism/SharpRestriction/RamificationFrobenius/TotientGaloisClasses/FrameFacts.lean#L249) · [Window conditions](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AutomorphicArithmetic/CharacterBoxes/ExistsPageN.lean#L27)

For the norm-one torus of $K/\mathbb Q$, let $r$ be the class of a prime above $13$. The integral operator $P=2-r-r^{-1}$ kills the trivial component and acts by $3$ on each cubic component. In the relative model with definite ranks $1,4,7$, the Bessel row intertwines the embedded torus action. Taking the terminal form to be the cubic determinant character makes its first descending theta lift zero at $13$ for every Schwartz vector. The open problem is to find a terminal representation with a nonzero local lift and a global period nonzero on $P\delta_1$. [Proof and choice of splittings](PROGRESS.md#hecke-action-and-vanishing) · [Active problem](OPEN_PROBLEMS.md)

## Reading the revision

| Manuscript folios | What to read there |
| --- | --- |
| 29, 446–446d, 463–463b | A residue detects each omitted zero. The arithmetic theta space determines the multiplicities at the strip boundary. A resolvent estimate gives the trace without a zero-spacing assumption. |
| 495–495b, 514a–514b, 520 | The original local identity (11.3.2.1) gives $0$ on one side and $\log 2$ on the other. Equations (17) and (18) give the full-strip identity and the narrow-strip defect. |
| 514c–514e | The unramified local Fourier factor gives the prime weights. The endpoint trace (17.3) recovers the full sum of these weights with finite cutoffs under translation. |
| 514f–514j | The scalar comparison and its polar residue. For ordinary zeta, Hurst’s sieve through $10^{16}$ gives the filtered trace bound through $X=10^{32}/e^2$. [Hurst’s sieve](https://doi.org/10.1090/mcom/3275) |
| 514k–514n | A bound for the discarded pairs at every scale. A zero outside the strip forces a lower bound for the positive real part of the remaining signed sum on each interval $[Y,Y^2]$. |
| 514o–514t | The shared-prime bound for the original sum, Möbius inversion on the rational gcd, and the one-sided mean for the resulting sum over coprime norms. |
| 514u–514x | The squarefree product, its divisor weight and Euler multiplier, and the linear-term estimate that preserves detection of exterior zeros. |
| 518a–518f | The mixed additive cutoff fails. A lift on the rational semilocal quotient gives the finite trace (17.8). Its Fourier factor determines both the real and finite Weil terms in (17.9). |
| 518g–518j | Fourier descent for every Hecke component, the coefficient selected by the two cutoff profiles, the uniform error $O(Y/L)$ and a fixed-input obstruction to convergence in the narrow weighted space. |
| 520c–520n, 522–522b | A fixed smooth prime weight gives a criterion for the Riemann hypothesis in (21) and its per-character Hecke analogue in (24). |
| 520o–520r | A normalized test detects every missed zero. A zero-free region bounds the Hecke trace defect at all large scales. Finite-height verification for ordinary zeta yields the explicit inequalities (20w) and (20x). |
| 520s–520v | A zero-density bound makes the primitive of the strip defect continuous. The jump of the global trace primitive at $n$ is $\Lambda_\chi(n)/\sqrt n$. Equation (20aa) isolates all such jumps in a growing interval. |
| 522f–522h | A Hecke zero of order at least three gives a counterexample to the multiplicity cap used in Chapter 13. |
| 522l–522v | Principal prime ideals, finite-height Gaussian averages, and the two-sided oscillation in (42). |
| 522w–522y | A lower bound for the Weil form on a log interval, its dependence on the conductor, and the correlation that must stay bounded for widely separated translates. |
| 522z–522ac | Reconstruction from narrower tests, the resulting zero strip, a short-interval sieve bound valid at every large separation, and a fixed-width estimate for ordinary zeta. |
| 522ad–522ag | The diagonal prime weight, the lower limit of the signed distinct-pair contribution, and an upper bound for the part from nearby pairs. |
| 522ah–522aj | A mean-square estimate over norm twists, the zero-location criterion for any prescribed band with $1\le U=o(\log X)$, and simultaneous control at a continuum of prime scales for most high frequencies. |
| 522ak–522am | The diagonal contribution to a frequency average, an exact formula for the short-interval variance and the zero strip implied by a bound for that variance. |
| 522an–522ao | A finite-height bound for the sharp interval variance and an unconditional saving over $X/U$ for all $1\le U\le X^{a_\chi}$ with a fixed $a_\chi>0$. |

Folio numbers follow the manuscript. A letter suffix identifies an inserted page. Folios 514u–514x are PDF pages 557–560. The uniform finite-cutoff estimate on folio 518i is PDF page 573. The contents on manuscript folio 2 link to the proofs.

## Files and build

| Path | Contents |
| --- | --- |
| [ref/](ref/) | TeX for the facsimile of Alessandro Maria Masullo’s published manuscript, including its original page navigation. The facsimile imports the author’s PDF page by page. |
| [src/](src/) | The editable revision. The replacement pages, proofs and counterexamples are typeset here. |
| [output/pdf/](output/pdf/) | The [940-page reference facsimile](output/pdf/the-music-of-the-primes-reproduction.pdf) and the [compiled revision](output/pdf/the-music-of-the-primes-revised.pdf). |

To build the revision, run pdfLaTeX from the repository root. The reference PDF and navigation files it reads are included.

```sh
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=output/pdf src/the-music-of-the-primes-revised.tex
```

To rebuild the reference facsimile as well, save the author’s PDF as `ref/the-music-of-the-primes.pdf` and run the following command from the same directory.

```sh
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=output/pdf ref/the-music-of-the-primes-reproduction.tex
```
