# The Music of the Primes

**Last updated 21 November 2026.** Revision `2026-11-21.3` reaches manuscript folio **522ac, equation (49)**. The revised manuscript has 1,009 pages.

For every normalized unitary Hecke character and every sufficiently large $X$, equation (48) bounds the correlation between a test and its translate when the prime powers it samples lie in an interval of length comparable to $\sqrt X\log X$. The test narrows as $X$ grows. For ordinary zeta, equation (49) also proves the correlation bound at a single fixed width for $1\le X\le 10^{19}e^{-1/128}$. [Dated results and proof locations](PROGRESS.md)

**Open proof.** For each fixed character, it would suffice to prove the correlation bound at every sufficiently large $X$ for one sequence of relative interval widths $r=X^{-o(1)}$. Equation (46) reconstructs the original test exactly with a factor $1/r$. At the widths covered by (48), that factor has exponent $1/2$. The estimate at the wider intervals required by (47) remains open, as does the independent geometric trace estimate (19) on folio 520. The manuscript therefore leaves the Hecke Riemann hypothesis open.

[Original manuscript (940-page PDF)](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf) · [Revised manuscript (PDF)](output/pdf/the-music-of-the-primes-revised.pdf) · [Editable revision (TeX)](src/the-music-of-the-primes-revised.tex)

## Reading the revision

| Manuscript folios | What to read there |
| --- | --- |
| 29, 446–446d, 463–463b | A residue detects each omitted zero. The arithmetic theta space determines the multiplicities at the strip boundary. A resolvent estimate gives the trace without a zero-spacing assumption. |
| 495–495b, 514a–514b, 520 | The original local identity (11.3.2.1) gives $0$ on one side and $\log 2$ on the other. Equations (17) and (18) give the full-strip identity and the narrow-strip defect. |
| 520c–520n, 522–522b | A fixed smooth prime weight gives a criterion for the Riemann hypothesis in (21) and its per-character Hecke analogue in (24). A continuous tent gives another Mellin transform with no zeros for $0<\Re s<1$, namely $(b^s-1)(b^s-b)/(s(s-1))$ for $b>1$. [Crossley (2026)](https://doi.org/10.5281/zenodo.24410836) |
| 522f–522h | A Hecke zero of order at least three gives a counterexample to the multiplicity cap used in Chapter 13. |
| 522l–522v | Principal prime ideals, finite-height Gaussian averages, and the two-sided oscillation in (42). |
| 522w–522y | A lower bound for the Weil form on a log interval, its dependence on the conductor, and the correlation that must stay bounded for widely separated translates. |
| 522z–522ac | Reconstruction from narrower tests, the resulting zero strip, a short-interval sieve bound valid at every large separation, and a fixed-width estimate for ordinary zeta. |

Folio numbers follow the manuscript. A letter suffix identifies an inserted page. Folios 522z–522ac are PDF pages 587–590. The contents on manuscript folio 2 link to the proofs.

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
