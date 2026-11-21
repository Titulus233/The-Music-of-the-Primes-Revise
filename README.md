# The Music of the Primes

**Last updated 21 November 2026.** Revision `2026-11-21.1` reaches manuscript folio **522v, equation (42)**. The revised manuscript has 1,002 pages.

The revision identifies the spectral trace on the full critical strip for each unitary Hecke character and gives the exact contribution lost when the strip narrows. The latest result concerns the splitting of the cubic polynomial $x^3-x-1$ modulo primes. Its signed, smoothly weighted prime count has both positive and negative fluctuations of order at least $\sqrt X$ along unbounded sequences. [Dated results and proof locations](PROGRESS.md)

**Open proof.** Chapter 12 still needs an independent estimate for the geometric trace defect under translation, equation (19) on folio 520, at arbitrarily small strip widths. In the prime-sum formulation it suffices, for each required Hecke character, to prove the one-sided bound (38) on folio 522p along a sequence of averaging parameters $\kappa\downarrow0$. A fixed $\kappa$ tests only a bounded range of zero heights. The general Hecke Riemann hypothesis remains open in this manuscript.

[Original manuscript (940-page PDF)](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf) · [Revised manuscript (PDF)](output/pdf/the-music-of-the-primes-revised.pdf) · [Editable revision (TeX)](src/the-music-of-the-primes-revised.tex)

## Reading the revision

| Manuscript folios | What to read there |
| --- | --- |
| 29, 446–446d, 463–463b | A residue detects each omitted zero. The arithmetic theta space determines the multiplicities at the strip boundary. A resolvent estimate gives the trace without a zero-spacing assumption. |
| 495–495b, 514a–514b, 520 | The original local identity (11.3.2.1) gives $0$ on one side and $\log 2$ on the other. Equations (17) and (18) give the full-strip identity and the narrow-strip defect. |
| 520c–520n, 522–522b | A fixed smooth prime weight gives a criterion for the Riemann hypothesis in (21) and its per-character Hecke analogue in (24). |
| 522f–522h | A Hecke zero of order at least three gives a counterexample to the multiplicity cap used in Chapter 13. |
| 522l–522v | Principal prime ideals, finite-height Gaussian averages, and the two-sided oscillation in (42). |

Folio numbers follow the manuscript. An appended letter identifies an inserted page. For example, folio 522v is PDF page 583. The contents on manuscript folio 2 link to the proofs.

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
