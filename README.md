# The Music of the Primes

**Last updated 21 November 2026.** Revision `2026-11-21.8` adds **folios 520o–520r, equations (20u)–(20x)** in Chapter 12. The Chapter 13 variance estimate is on folio 522ao, equation (61). The revised manuscript has 1,025 pages.

For ordinary zeta, one fixed smooth weight gives a prime-sum error at most $10^5\sqrt X$ for every $1\le X\le e^{300000}$. With the same test, the strip defect $G_\alpha-W$ in (18) has absolute value less than $e^{-140000}$ at **every** strip half-width, including zero, for $0\le\log X\le300000$ in Sobolev degree four. The proof uses the published verification of the zeros through height $3\cdot10^{12}$ and bounds the entire remaining tail analytically. [Dated results and proofs](PROGRESS.md) · [Platt and Trudgian](https://doi.org/10.1112/blms.12460)

**Open proof.** For ordinary zeta the square-root inequality (20x) for all $X\ge1$ is equivalent to RH. For every fixed Hecke character, equation (20v) gives a trace defect exponentially small in $(\log X)^2$ on strips whose half-width tends to $1/2$. Equation (19) still needs an independent estimate at arbitrarily small fixed half-widths as $X\to\infty$. The general Hecke zero-location claim remains open.

[Original manuscript (940-page PDF)](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf) · [Revised manuscript (PDF)](output/pdf/the-music-of-the-primes-revised.pdf) · [Editable revision (TeX)](src/the-music-of-the-primes-revised.tex)

## Reading the revision

Crossley uses the same verified zero height as (20x) to prove that the tent-weighted sum over ordinary primes at width $3/2$ stays strictly below its main term for every $0<y\le10^{28}$. For comparison with (22), the tent at any width $b>1$ has Mellin transform $(b^s-1)(b^s-b)/(s(s-1))$, which has no zeros for $0<\Re s<1$. [Finite-range proof](https://doi.org/10.5281/zenodo.24410819) and [Mellin transform](https://doi.org/10.5281/zenodo.24410836).

| Manuscript folios | What to read there |
| --- | --- |
| 29, 446–446d, 463–463b | A residue detects each omitted zero. The arithmetic theta space determines the multiplicities at the strip boundary. A resolvent estimate gives the trace without a zero-spacing assumption. |
| 495–495b, 514a–514b, 520 | The original local identity (11.3.2.1) gives $0$ on one side and $\log 2$ on the other. Equations (17) and (18) give the full-strip identity and the narrow-strip defect. |
| 520c–520n, 522–522b | A fixed smooth prime weight gives a criterion for the Riemann hypothesis in (21) and its per-character Hecke analogue in (24). |
| 520o–520r | A normalized test detects every missed zero. A zero-free region bounds the Hecke trace defect at all large scales. Finite-height verification for ordinary zeta yields the explicit inequalities (20w) and (20x). |
| 522f–522h | A Hecke zero of order at least three gives a counterexample to the multiplicity cap used in Chapter 13. |
| 522l–522v | Principal prime ideals, finite-height Gaussian averages, and the two-sided oscillation in (42). |
| 522w–522y | A lower bound for the Weil form on a log interval, its dependence on the conductor, and the correlation that must stay bounded for widely separated translates. |
| 522z–522ac | Reconstruction from narrower tests, the resulting zero strip, a short-interval sieve bound valid at every large separation, and a fixed-width estimate for ordinary zeta. |
| 522ad–522ag | The diagonal prime weight, the lower limit of the signed distinct-pair contribution, and an upper bound for the part from nearby pairs. |
| 522ah–522aj | A mean-square estimate over norm twists, the zero-location criterion for any prescribed band with $1\le U=o(\log X)$, and simultaneous control at a continuum of prime scales for most high frequencies. |
| 522ak–522am | The diagonal contribution to a frequency average, an exact formula for the short-interval variance and the zero strip implied by a bound for that variance. |
| 522an–522ao | A finite-height bound for the sharp interval variance and an unconditional saving over $X/U$ for all $1\le U\le X^{a_\chi}$ with a fixed $a_\chi>0$. |

Folio numbers follow the manuscript. A letter suffix identifies an inserted page. Folios 520o–520r are PDF pages 560–563. Folios 522an–522ao are pages 605–606 in this edition. The contents on manuscript folio 2 link to the proofs.

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
