# The Music of the Primes

**Last updated 21 November 2026.** Revision `2026-11-21.2` reaches manuscript folio **522y, equation (45)**. The revised manuscript has 1,005 pages.

For every unitary Hecke character, the Weil quadratic form is positive on every nonzero test function supported in an interval of length at most $1/16$ in logarithmic coordinates. Equation (43) gives an explicit lower bound from the archimedean factors, conductor and prime powers. The revision also identifies the full-strip trace, the zeros lost on narrowing the strip, and two-sided square-root fluctuations for the splitting of $x^3-x-1$ modulo primes. [Dated results and proof locations](PROGRESS.md)

**Open proof.** Fix the smooth test $g$ on folio 522y. For each character $\chi$, equation (45) shows that zero location is equivalent to bounding the correlation between $g$ and its translate by $Q_\chi(g)$ at every separation. The inequality is proved for separations up to $1/64$ for all characters. The estimate at arbitrarily large separations for the same character remains open. Chapter 12 expresses the gap as the geometric trace estimate (19) on folio 520. The general Hecke Riemann hypothesis remains open in this manuscript.

[Original manuscript (940-page PDF)](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf) · [Revised manuscript (PDF)](output/pdf/the-music-of-the-primes-revised.pdf) · [Editable revision (TeX)](src/the-music-of-the-primes-revised.tex)

## Reading the revision

| Manuscript folios | What to read there |
| --- | --- |
| 29, 446–446d, 463–463b | A residue detects each omitted zero. The arithmetic theta space determines the multiplicities at the strip boundary. A resolvent estimate gives the trace without a zero-spacing assumption. |
| 495–495b, 514a–514b, 520 | The original local identity (11.3.2.1) gives $0$ on one side and $\log 2$ on the other. Equations (17) and (18) give the full-strip identity and the narrow-strip defect. |
| 520c–520n, 522–522b | A fixed smooth prime weight gives a criterion for the Riemann hypothesis in (21) and its per-character Hecke analogue in (24). |
| 522f–522h | A Hecke zero of order at least three gives a counterexample to the multiplicity cap used in Chapter 13. |
| 522l–522v | Principal prime ideals, finite-height Gaussian averages, and the two-sided oscillation in (42). |
| 522w–522y | A lower bound for the Weil form on a log interval, its dependence on the conductor, and the correlation that must stay bounded for widely separated translates. |

Folio numbers follow the manuscript. An appended letter identifies an inserted page. For example, folios 522w–522y are PDF pages 584–586. The contents on manuscript folio 2 link to the proofs.

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
