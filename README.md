# The Music of the Primes

**Last updated 21 November 2026.** Revision `2026-11-21.11` adds **folios 518b–518f, equations (17.5)–(17.9)** to Chapter 12. The revised manuscript has 1,037 pages.

The rational semilocal Fourier operator gives the Weil terms for ordinary zeta and fixed primitive Dirichlet characters. Step II on original folio 516 fails on the additive test space already for the real place and the prime 2. On the idelic quotient a two-sided norm cutoff has an explicit polar-free lift. The one-sided cutoff preserves a logarithmic term that rules out any such lift. [Dated results and proofs](PROGRESS.md)

The arithmetic projection on a narrow strip recovers the weight of each prime power. This holds for ordinary zeta, fixed primitive Dirichlet characters and imaginary quadratic ideal class characters at every positive half-width below $1/2$. It also holds for any fixed Hecke character in the wider strips specified on folio 520t. For the first three cases, tests confined to small neighborhoods of the prime norms recover their entire weighted sum up to $O(X^{-A})$ for any fixed $A>0$, even at half-width $1/\log X$.

**Open proof.** In the ranges just stated, equation (20aa) reduces (19) to the trace on a test that vanishes around every prime-power norm. The local weights follow from the full-strip explicit formula and unconditional zero-density estimates. The remaining trace still needs an independent growth bound for arbitrarily small fixed half-widths as $X\to\infty$. For ordinary zeta the all-scale square-root bound (20x) is equivalent to RH. It holds for the specified weight up to $e^{300000}$. The general Hecke zero-location claim remains open.

[Original manuscript (940-page PDF)](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf) · [Revised manuscript (PDF)](output/pdf/the-music-of-the-primes-revised.pdf) · [Editable revision (TeX)](src/the-music-of-the-primes-revised.tex)

## Reading the revision

| Manuscript folios | What to read there |
| --- | --- |
| 29, 446–446d, 463–463b | A residue detects each omitted zero. The arithmetic theta space determines the multiplicities at the strip boundary. A resolvent estimate gives the trace without a zero-spacing assumption. |
| 495–495b, 514a–514b, 520 | The original local identity (11.3.2.1) gives $0$ on one side and $\log 2$ on the other. Equations (17) and (18) give the full-strip identity and the narrow-strip defect. |
| 514c–514e | The unramified local Fourier factor gives the prime weights. The endpoint trace (17.3) recovers the full sum of these weights with finite cutoffs under translation. |
| 518a–518f | The mixed additive cutoff fails. A lift on the rational semilocal quotient gives the finite trace (17.8). Its Fourier factor determines both the real and finite Weil terms in (17.9). |
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

Folio numbers follow the manuscript. A letter suffix identifies an inserted page. Folios 518b–518f are PDF pages 547–551. Folios 520o–520v and 522an–522ao are pages 568–575 and 617–618. The contents on manuscript folio 2 link to the proofs.

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
