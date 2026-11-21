# Open problems for the $S_3$ prototype

## The first double-step Bessel period

Let $K=\mathbb Q(\sqrt{-23})$, let $M$ be the splitting field of $x^3-x-1$, and let $\psi$ be a nontrivial character of $\mathrm{Cl}(K)=C_3$. The Hilbert class field of $K$ is $M$. Once the zeros of $\zeta_K$ are accounted for, ERH for $M$ reduces to zero location for $L_K(s,\psi)$ by $\zeta_M=\zeta_K L_K(\psi)^2$. [Serre, §5.3](https://www.math.mcgill.ca/goren/SeminarOnCohomology/Serre.pdf)

For the norm-one torus $T$ of $K/\mathbb Q$ with maximal compact subgroup $U$ at the finite places, the quotient $T(\mathbb Q)\backslash T(\mathbb A_f)/U$ is $C_3$. Write $\delta_c$ for the point mass at $c$. With $r$ a prime-ideal class above $13$, put $S=r+r^{-1}$ on $\mathbb Z[C_3]$ and $P=2-S$. Then $P^2=3P$ and $P\delta_1=2\delta_1-\delta_r-\delta_{r^{-1}}$. The two nontrivial characters give the same eigenvalue $-1$ for $S$.

**Active problem.** Construct a terminal automorphic representation $\Pi'$ for the relative double step with positive definite ranks $1,4,7$ and descending ranks $8,6,4$. At $13$, find a $\mathrm{GL}_4$ representation with a Bessel functional for $\nu_{13}^{\pm1}$ and $\xi_N$, lift it to $\mathrm{GL}_6$ and then $\mathrm{GL}_8$, and realize that last local type globally. The two descending lifts must recover the chosen Bessel model. For specified global vectors, show that the period retains that component and identify its integral Hecke action. The target is

$$
B_1 S=S_{13}^{(1)}B_1,\qquad B_1(P\delta_1)\ne0.
$$

The embedded torus acts on the full row by the sum of its two translates. For the terminal cubic determinant character and the specified splittings, the first local theta Hom space is zero on every matrix-rank stratum. An inverse twist restores a local functional but cancels the terminal character in the global integral. The weight-one class theta series has eigenvalue $-1$ at $13$. Nonvanishing of the prescribed global Bessel period is open. [Relative spaces and proof](PROGRESS.md#spaces-and-the-period) · [Double-step integral](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AbelianVarietyTheory/Proofs/DecoratedLatticeProofs/BesselPeriodDoubleStepIteratedQuotientIntegral.lean#L56) · [Identification with a column period](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AbelianVarietyTheory/Proofs/TwistedOperators/QEqColPer.lean#L21)

## From a nonzero row to a zero-free window

1. Extend Hecke compatibility to the good prime ideals and propagate the cubic component through the chain. Establish its integral divisibility and norm bounds. The integral operator $P$ permits this question at $3$, where $P/3$ need not preserve the lattice.
2. Determine which cohomology enters that divisibility bound. For $A=K\mathbb Q(\zeta_N)$ the extension $AM/A$ is cyclic of degree three and unramified at finite places. The existing weak Vandiver bound concerns cyclotomic auxiliary fields. A reduction to the cubic component of the negative-twist cohomology would need an integral argument, including at $3$. [Weak Vandiver window](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AutomorphicArithmetic/CharacterBoxes/ExistsPageN.lean#L12)
3. Identify the resulting geometric weights with ideal-class reciprocity and the logarithmic derivative of $L_K(s,\psi)$. Prove a one-sided prime-sum bound on arbitrarily distant power windows and apply the Hecke explicit formula. [Arithmetic input in the Dirichlet construction](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AutomorphicArithmetic/PrimitiveCosets/CoreAtH.lean#L18) · [Window criterion](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AutomorphicArithmetic/DedekindLFunctions/LandauTheorems/ZeroFreeOfRpowWindow.lean#L11)

## Archived condition from Masullo’s §12.3

Revision `2026-11-21.16` ends the single-$L$-function calculation at (17.4s). For fixed $F,\chi$, narrow half-width $\alpha$ and each $\varepsilon>0$, it asks for a sequence $Y_j\to\infty$ on which

$$
\frac{1}{\log Y_j}\int_{Y_j}^{Y_j^2}X^{-\alpha-\varepsilon}
[\operatorname{Re}S_{Y_j}(X)]_+\,\frac{dX}{X}
\le C_{F,\chi,\alpha,\varepsilon}.
$$

This bound remains open and belongs to the archived $\mathrm{GL}_1$ argument. [Squarefree sum, folio 514u](src/the-music-of-the-primes-revised.tex#L2183) · [Interval criterion, folio 514x](src/the-music-of-the-primes-revised.tex#L2314) · [Record of the revision](PROGRESS.md)
