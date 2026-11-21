# The Music of the Primes

**Last updated 21 November 2026.** Revision `2026-11-21.12` adds **folios 518g–518j, equations (17.10)–(17.12)** to Chapter 12. The revised manuscript has 1,041 pages.

For every fixed number field and unitary Hecke character, a trace with two smooth cutoffs recovers the Weil distribution on translated tests. Include all prime ideals up to norm $Y=e^2X$, where $\log X$ is the translation. The error is $O(Y/L)$ with cutoff width $L$ in log norm. Taking $L=X^{1+A}$ gives $O(X^{-A})$ for any fixed $A>0$. The proof uses local Fourier factors and the elementary prime count. The choice of cutoff endpoints determines the coefficient of the Weil term. [Dated results and proofs](PROGRESS.md)

For ordinary zeta, fixed primitive Dirichlet characters and imaginary quadratic ideal class characters, the narrow arithmetic projection recovers every prime-power weight. This holds even at half-width $1/\log X$ when the neighborhoods of the prime norms shrink as in (20aa). For general Hecke characters, folio 520t gives the range from the available density bound.

**Open proof.** Equation (19) requires comparison of the trace in ordinary $L^2$ with the global arithmetic projection on an arbitrarily narrow fixed strip. For zeta, (17.12) shows that the semilocal Fourier transforms of one fixed test already grow without bound in the required weighted norm. In the ranges of (20aa), the remaining discrepancy can be tested away from every prime-power norm. Its growth as $X\to\infty$ is open. For ordinary zeta the all-scale square-root bound (20x) is equivalent to RH. The general Hecke zero-location claim remains open.

[Original manuscript (940-page PDF)](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf) · [Revised manuscript (PDF)](output/pdf/the-music-of-the-primes-revised.pdf) · [Editable revision (TeX)](src/the-music-of-the-primes-revised.tex)

## Reading the revision

Crossley uses the same verified zero height as (20x) to prove that the tent-weighted sum over ordinary primes at width $3/2$ stays strictly below its main term for every $0<y\le10^{28}$. For comparison with (22), the tent at any width $b>1$ has Mellin transform $(b^s-1)(b^s-b)/(s(s-1))$, which has no zeros for $0<\Re s<1$. [Finite-range proof](https://doi.org/10.5281/zenodo.24410819) and [Mellin transform](https://doi.org/10.5281/zenodo.24410836).

At $n=31$, each of the eight Dirichlet characters in Crossley’s 547/727 field has value $-1$. Summing their limits for $G_{\alpha,\chi}$ in (20z) gives $-8\log(31)/\sqrt{31}$. The second difference of three signed prime-ideal sums at $30/4$, $31/4$ and $32/4$ is $8\log(31)/31$, which gives the same value after multiplication by $-\sqrt{31}$. [Three finite prime-race scores](https://doi.org/10.5281/zenodo.24413207).

| Manuscript folios | What to read there |
| --- | --- |
| 29, 446–446d, 463–463b | A residue detects each omitted zero. The arithmetic theta space determines the multiplicities at the strip boundary. A resolvent estimate gives the trace without a zero-spacing assumption. |
| 495–495b, 514a–514b, 520 | The original local identity (11.3.2.1) gives $0$ on one side and $\log 2$ on the other. Equations (17) and (18) give the full-strip identity and the narrow-strip defect. |
| 514c–514e | The unramified local Fourier factor gives the prime weights. The endpoint trace (17.3) recovers the full sum of these weights with finite cutoffs under translation. |
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

Folio numbers follow the manuscript. A letter suffix identifies an inserted page. Folios 518g–518j are PDF pages 552–555. Folios 520s–520v and 522an–522ao are pages 576–579 and 621–622. The contents on manuscript folio 2 link to the proofs.

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
