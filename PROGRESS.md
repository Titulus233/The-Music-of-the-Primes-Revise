# Proof progress

## 2026-11-21 · The cubic Bessel period at 13

**The determinant character gives a zero double-step row for every Schwartz vector in the relative models below.** The first descending theta lift already has zero local Hom space at 13. Changing the splitting can restore a nonzero local functional, while cancelling the terminal cubic character in the global integral. A global row retaining that character remains open. [Proof commit](https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/e1c8d0eb94444da08beb4e3dd2f6459a88b9e697) · [Manuscript audit and statement of the period problem](https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/3eeb84b) · [Active problem](OPEN_PROBLEMS.md)

### Spaces and the period

Write $K=\mathbb Q(\delta)$, $\delta=\sqrt{-23}$, $T=U(1)$ and $\nu(t)=\psi([\mathfrak a(t)])$ for the character of $T(\mathbb A)$ read from the fractional ideal of a norm-one idèle. The finite torus quotient by its maximal compact subgroup maps isomorphically to $C_3$. The ideal of $x/\bar x$ has square class $[\mathfrak a(x)]^2$, and squaring is bijective on $C_3$. A principal ideal of a norm-one idèle has a generator of norm one since that norm is a positive rational unit at every finite prime. A prime $\mathfrak p\mid13$ generates the class group. The local element $z=(13,13^{-1})$ represents $[\mathfrak p/\bar{\mathfrak p}]=r^2$ for $r=[\mathfrak p]$, so $\nu_{13}(13)$ is a primitive cube root of unity. [Serre, §5.3](https://www.math.mcgill.ca/goren/SeminarOnCohomology/Serre.pdf)

Let $I_a$ denote the positive identity Hermitian form, $H$ the hyperbolic plane with Gram matrix $\left(\begin{smallmatrix}0&1\\1&0\end{smallmatrix}\right)$, and $L^-=\langle-1\rangle$. The definite spaces have Gram matrices $I_a,\delta I_b,I_c$. The two dual pairs used in the descending integral are $(U(V),U(W))$ and $(U(W),U(V'))$, where

$$
V=H\oplus I_a\oplus L^-,\qquad W=\delta(H\oplus I_b),\qquad V'=I_c\oplus L^-.
$$

The choice $(a,b,c)=(1,4,7)$ starts on the torus. The choice $(76,94,112)$ uses its determinant pullback $i(f)(u)=f([\mathfrak a(\det u)])$ and has the top and lower ranks prescribed by the external grid for $(k,m,t)=(8,4,17)$. In that grid $r_0=k+m-1$ and $\dim X_j=r_0+1+m(r_0+5)+j(t+1)$. Thus $\dim X_0\ge32$ for $m\ge2$ and $\dim X_0\ge76$ for a recursive double step ($m\ge4$). The field and period data here define relative models. [Rank constraints](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Formalism/LocalRingCardinality/Params.lean#L6) · [Grid dimensions](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AbelianVarietyTheory/Definitions/Divisors/LeastSplitAuxiliaryPrimeThetaChainSpec.lean#L121) · [Bessel and Fourier–Jacobi spaces](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AbelianVarietyTheory/Proofs/TwistedOperators/ExistsWeilDatumAnisotropicKernelPair.lean#L24)

Use the free $\mathcal O_K$-lattices in these bases, the standard additive character of $\mathbb A/\mathbb Q$, and self-dual additive measures. Take trivial splitting characters for even-dimensional spaces. For an odd-dimensional space choose a unitary extension $\eta$ of $\chi_{-23}$. One choice on principal ideals prime to $(\delta)$ is $\eta((u))=(\frac{u\bmod\delta}{23})u/|u|$. It is unchanged under $u\mapsto-u$. Write $w=(1+\delta)/2$ and choose $\mathfrak p=(13,w-5)$. Then $\mathfrak p^3=(31+12w)$, so taking the principal complex cube root of $\eta((31+12w))$ for $\eta(\mathfrak p)$ fixes an extension. Standard lattice indicators at finite places and a Gaussian on a real Schrödinger polarization give test vectors. The vanishing holds for every choice of those vectors.

Write $[G]=G(\mathbb Q)\backslash G(\mathbb A)$. With $e,f_0$ the hyperbolic basis of $H$ and $\ell$ the basis of $L^-$, let $N$ be the unipotent radical stabilizing $Ke$ in $U(V)$. Set $n\ell=\ell+u(n)e$ and $\xi_N(n)=\mathbf e(\operatorname{Tr}_{K/\mathbb Q}(\delta u(n)))$. Embed $U(I_a)$ by the identity on $H\oplus L^-$. For the nonzero automorphic function $F(v)=\nu(\det v)$ on $[U(V')]$, define

$$
B_1(f)(g)=\int_{[U(I_a)]}\!\int_{[N]} i(f)(h)\overline{\xi_N(n)}
\bigl(\Theta_{W\to V,\Phi_1}\Theta_{V'\to W,\Phi_2}F\bigr)(n\iota(h)g)\,dn\,dh .
$$

Here $\Theta_{A\to B,\Phi}F(b)=\int_{[U(A)]}F(a)\sum_x(\omega(a,b)\Phi)(x)\,da$ in a rational Schrödinger polarization. This is the rank-one Bessel integral of a double lift on the left of the source unfolding. The chosen terminal determinant character is bounded and need not be rapidly decreasing. The inner integral converges absolutely: in the doubled unitary group the Siegel rank is $e_0=b+2$ and $(c+1)-\operatorname{Witt}(V')=c>e_0$ in both models. Weil convergence applied to the product of the theta kernel with its conjugate gives square integrability, then absolute integrability by finite volume. [Double-step integrand](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AbelianVarietyTheory/Definitions/LatticeFrames/IsQuasiFam.lean#L77) · [Quotient-integral formulation](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AbelianVarietyTheory/Proofs/DecoratedLatticeProofs/BesselPeriodDoubleStepIteratedQuotientIntegral.lean#L56) · [Column-period identity](https://github.com/TomasOrtega/RH/blob/a6ac91a412dcbaab31801355ec5707024a71bf65/extracted/lean/src/Development/AbelianVarietyTheory/Proofs/TwistedOperators/QEqColPer.lean#L21) · [Gan–Qiu–Takeda, §3.2](https://arxiv.org/pdf/1207.4709#page=14)

### Hecke action and vanishing

Put $D_z=\iota(zI_a)$. Since $a\equiv1\pmod3$ in both models, right translation of the determinant pullback by $zI_a$ and its inverse gives $i(Sf)$ after summation. Changing $h$ in the integral proves, for any convergent endpoint and every $g$,

$$
B_1(Sf)(g)=B_1(f)(D_zg)+B_1(f)(D_z^{-1}g).
$$

This is the Hecke action of the embedded torus on the period row. At $g=1$ it acts on the first Schwartz vector by $\omega(D_z,1)+\omega(D_z^{-1},1)$. In the $1,4,7$ model this is $13^3\Phi_1(D_z^{-1}X)+13^{-3}\Phi_1(D_zX)$ on $4\times6$ matrices. The ambient spherical action has a separate description on the definite theta lifts in dimensions $76,94,112$. With the trivial splittings the split matrix action is $\omega(g,h)\Phi(X)=|\det g|^{-b/2}|\det h|^{a/2}\Phi(g^{-1}Xh)$ for a pair of ranks $a,b$. Simultaneous central translation acts trivially. Thus the central spherical correspondence $R_{13I_{112}}+R_{13^{-1}I_{112}}$ transfers $S$ through both lifts. The embedded $D_z$ on the lower Bessel group fixes its complementary three-dimensional subspace. [Split matrix model, Mínguez, §1.4](https://www.numdam.org/item/10.24033/asens.2080.pdf)

For the inner lift let $d=c+1$, $e_0=b+2$ and $k_v=\mathbb Q_{13}$. Its large factor $G=\mathrm{GL}_d(k_v)$ acts on $\mathcal S(M_{d,e_0}(k_v))$ by $|\det g|^{-e_0/2}\Phi(g^{-1}X)$. Its splitting character on this factor is trivial because the chosen character for $W$ is trivial. With all other data fixed, a nonzero global lift would give a local functional transforming by $\nu_{13}^{-1}\circ\det$.

Filter the matrix space by rank $j$. On each stratum, fixing the kernel leaves the space of injective $d\times j$ matrices, a single $G$-orbit. Lebesgue measure on that orbit transforms in the normalized model by $|\det|^{j-e_0/2}$. Any relatively equivariant distribution must have the same character on the stabilizer, by Frobenius reciprocity. Since $j\le e_0<d$, the standard stabilizer contains a diagonal matrix of determinant $13$ acting identically on the image. It would require $\nu_{13}(13)^{-1}=13^{e_0/2-j}$, impossible on every stratum. The kernel Grassmannian has local trivializations, and the rank filtration of compactly supported locally constant functions exhausts the matrix space. Hence the local Hom space is zero. The inner theta lift and $B_1(P\delta_1)$ vanish for every test vector. This obstruction occurs before evaluation of the Bessel functional.

For comparison, twist the action on the large factor by $\nu_{13}^{-1}\circ\det$. With $j=e_0/2$, integration of $\Phi([Y\;0])$ over $M_{d,j}(k_v)$ now gives an equivariant functional taking the value $1$ on the standard lattice indicator. The Jacobian cancels the modulus in the Weil action. The character $x\mapsto\nu(x/\bar x)$ on $\mathbb A_K^\times$ is trivial on rational idèles and permits this change of splitting. Twisting the large-group action globally by $\nu^{-1}\circ\det$ cancels $F(v)=\nu(\det v)$ in the inner theta integral. A terminal representation with a compatible local theta quotient and a surviving global cubic period is the next problem.

## 2026-11-21 · Revision `2026-11-21.16`

Folios 514u–514x are pages 557–560 of the [1,060-page edition][pdf16]. Section 12.3 restricts the product of the outer norms to a squarefree integer and groups all its factorizations into a single divisor weight. [Archived interval criterion][f514x]

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [514u · (17.4p)][f514u] | Over the required Galois fields, the contributing products consist of distinct completely split rational primes. For the trivial character, each prime contributes the factor $-[F:\mathbb Q]$. The nonnegative divisor weight counts every allowed factorization with its smooth cutoff. | [8f1027a][split] |
| [514v–514w · (17.4q)–(17.4r)][f514v] | The linear term in the prime-sum comparison is $O_\varepsilon(X^{b_*/2+\varepsilon})$, where $b_*=\sup_\rho(\operatorname{Re}\rho-1/2)$. Hu’s $7/8$ input gives exponent $3/16+\varepsilon$ uniformly on the moving intervals for each fixed character. | [8f1027a][split] |
| [514x · (17.4s)][f514x] | A bounded one-sided mean of the squarefree sum along arbitrarily distant intervals is equivalent to zero location at the fixed width. If $b_*>\alpha$, there exists an exterior zero beyond both $\alpha$ and the linear-error exponent, including when the supremum is unattained. | [8f1027a][split] |

[split]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2
[pdf16]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/output/pdf/the-music-of-the-primes-revised.pdf
[f514u]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L2183
[f514v]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L2230
[f514x]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L2314

## 2026-11-21 · Revision `2026-11-21.15`

Folios 514o–514t are pages 551–556 of the [1,056-page edition][pdf15]. Section 12.3 bounds the part of the original trace from a large common rational prime and reduces the one-sided estimate to a sum over coprime integer norms. [Open proof obligation in this edition](https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/f71026622960f3b08485f4dcbf72439fefe8834d/OPEN_PROBLEMS.md)

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [514o · (17.4j)][f514o] | For any fixed $0<\alpha<3/8$, all pairs in (17.4g) sharing a prime greater than $X^{1/2-4\alpha/3}$ together satisfy $O(X^{\alpha+\varepsilon})$ at every sufficiently large $X$. The exponent uses Hu’s $7/8$ theorem. | [d855aa1][coprime] |
| [514p–514q · (17.4k)–(17.4l)][f514p] | Möbius inversion on the rational gcd gives the Euler multiplier $\prod_{p>P}(1-(L_p-1)^2)$ and an $O_\varepsilon(X^\varepsilon)$ arithmetic remainder uniform in the common-prime cutoff. | [d855aa1][coprime] |
| [514r–514s · (17.4m)–(17.4n)][f514r] | Deleting the small Euler factors from the kernel and coefficients gives an arithmetic comparison uniform on $[Y,Y^2]$. Only $O(X(1+\log P)/P)$ candidate pairs remain, where $P\to\infty$ is fixed throughout each interval. | [d855aa1][coprime] |
| [514t · (17.4o)][f514t] | For each fixed width, a bounded one-sided mean of the coprime sum on an unbounded sequence of intervals is equivalent to zero location in the closed strip. | [d855aa1][coprime] |

[coprime]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/d855aa10dddc64d3603af4b4890a8b4817c81204
[pdf15]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/output/pdf/the-music-of-the-primes-revised.pdf
[f514o]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L1935
[f514p]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L1975
[f514r]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L2055
[f514t]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L2135

## 2026-11-21 · Revision `2026-11-21.14`

Folios 514k–514n are pages 547–550 of the [1,050-page edition][pdf14]. The outstanding estimate in §12.3 concerns the positive real part of the separated Möbius sum, averaged over arbitrarily distant intervals. [Open proof obligation in this edition](https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/15cfb9950bb688e8c779bf2c44a6db4af1699c50/OPEN_PROBLEMS.md)

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [514n · (17.4i)][f514n] | At each fixed width and for every $\varepsilon>0$, a bounded mean of $X^{-\alpha-\varepsilon}[\operatorname{Re}Q_{\alpha,\chi}(X)]_+$ on one unbounded sequence of intervals $[Y,Y^2]$ is equivalent to zero location in the closed strip. The sequence can depend on the field, character, width and exponent. | [92c242e][windows] |
| [514l · (17.4g)–(17.4h)][f514l] and [514m][f514m] | If a zero lies outside the strip, there is a centered real part $b>\alpha$ such that the mean of $X^{-b}[\operatorname{Re}Q_{\alpha,\chi}(X)]_+$ is at least $c/\sqrt{\log Y}$ on every sufficiently distant interval $[Y,Y^2]$. The proof uses a positive measure and includes real zeros and complex characters. | [92c242e][windows] |
| [514k · (17.4f)][f514k] | For $D=[F:\mathbb Q]$, the kernel of the fixed test has decay $O(\exp(-c y^{1/(4D)}))$. All pairs with $dn\le eX/(\log(2X))^{4D+1}$ together cost $O_A(X^{-A})$ in absolute value for every fixed $A>0$. | [92c242e][windows] |

[windows]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/92c242ebbfb35cef729d4f52b3caa88451ddd002
[pdf14]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/output/pdf/the-music-of-the-primes-revised.pdf
[f514k]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1759
[f514l]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1800
[f514m]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1848
[f514n]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1892

## 2026-11-21 · Revision `2026-11-21.13`

Folios 514f–514j are pages 542–546 of the [1,046-page edition][pdf13]. Section 12.3 compares the global narrow-strip trace directly with the finite trace of (17.11) at $Y=e^2X$ and $L=X^2$.

The open proof obligation is the signed estimate in (17.4d) on folio 514i for all sufficiently large $X$. By the zero transfer in (36) on folio 522n, the estimate for the trivial character and the normalized infinite-order characters of finite conductor one over totally imaginary Galois fields would give the full Hecke claim. [Open proof obligation in this edition](https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/780bf0c039d64f66fddec6f6f91f2e4d876b199e/OPEN_PROBLEMS.md) · [780bf0c][obligation]

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [514i · (17.4d)][f514i] | For any fixed $0<\alpha<1/2$ and $0<\eta<1/2$, all pairs except $X^{1/2-\eta}<d,e\le e\sqrt X$ with $|d-e|>X^\alpha$ are already within $O(X^{\alpha+\epsilon})$. This holds for each nonprincipal character and for the filtered principal test. An all-scale bound for the separated pairs gives (19) for the original tests. | [5b96f53][scalar] |
| [514h · (17.4c)][f514h] | Double partial summation bounds the normalized quadratic term by a fixed kernel variation times $B_\chi(e\sqrt X)^2/\sqrt X$, where $B_\chi(T)$ is the largest absolute Möbius partial sum through $T$. A third-order differential operator removes the principal residue while retaining every nontrivial zero of the fixed detector. | [5b96f53][scalar] |
| [514j · (17.4e)][f514j] | For zeta, Hurst’s complete sieve through $10^{16}$ bounds the filtered scalar difference by $C_g X^\alpha+eC_{1,g}^{(2)}+O_g(X^{-1/2})$ for $1\le X\le10^{32}/e^2$. At unbounded scales the cited Mertens estimate gives $O_{\alpha,h}(X^\alpha+\sqrt X\exp[-c(\log X)^{3/5}(\log\log X)^{-1/5}])$ for every original test. | [5b96f53][scalar] |
| [514f · (17.4a)][f514f] and [514g · (17.4b)][f514g] | Squaring the error of a truncated reciprocal Euler series puts its first possible coefficient beyond the test support. The scalar trace difference becomes a finite quadratic sum of ideal Möbius coefficients, the projected convolution and an explicit principal residue. | [5b96f53][scalar] |

[obligation]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/780bf0c039d64f66fddec6f6f91f2e4d876b199e
[scalar]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/5b96f531c6139993e1e6505301e56b6480500703
[pdf13]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/output/pdf/the-music-of-the-primes-revised.pdf
[f514f]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1549
[f514g]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1591
[f514h]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1638
[f514i]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1677
[f514j]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1719

## 2026-11-21 · Revision `2026-11-21.12`

Folios 518g–518j are pages 552–555 of the [1,041-page edition][pdf12]. The finite-place cutoff is $Y=e^2X$ and the real parameter $L$ measures cutoff width in the logarithm of the norm.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [518i · (17.11)][f518i] | For every fixed unitary Hecke character over a number field, the semilocal trace with the specified two cutoffs differs from the full Weil distribution of the translated test by $O(Y/L)$. Setting $L=X^{1+A}$ yields $O(X^{-A})$ at all translates. The proof uses the local gamma and Euler factors and Chebyshev’s prime bound independently of the global zero sum. | [c50ccd1][joint] |
| [518j · (17.12)][f518j] | For ordinary zeta the semilocal Fourier transforms of the same nonnegative smooth input have weighted norm at least a constant times $\exp(c_bY^{1/2+b}/\log Y)$ at every $0<b<\alpha<1/2$. Their scalar traces approximate the Weil distribution, but the transforms do not converge on this test in the narrow weighted Hilbert space. Equation (19) still requires a comparison with its arithmetic projection. | [c50ccd1][joint] |
| [518h · (17.10)][f518h] | The first-order term is the Weil distribution times the negative integral of the first cutoff’s derivative against the reflected second cutoff. Explicit smooth profiles give coefficient one. Two even profiles give zero in this dilation limit. | [c50ccd1][joint] |
| [518g · extension of (17.8)–(17.9)][f518g] | Tate’s local equations descend additive Fourier transformation to the centered norm line for each unitary Hecke character, using smooth compact lifts on the semilocal quotient. | [c50ccd1][joint] |

[joint]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/c50ccd138c29a89f800a8740d16b49a525fd52d6
[pdf12]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/c50ccd138c29a89f800a8740d16b49a525fd52d6/output/pdf/the-music-of-the-primes-revised.pdf
[f518g]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/c50ccd138c29a89f800a8740d16b49a525fd52d6/src/the-music-of-the-primes-revised.tex#L1804
[f518h]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/c50ccd138c29a89f800a8740d16b49a525fd52d6/src/the-music-of-the-primes-revised.tex#L1851
[f518i]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/c50ccd138c29a89f800a8740d16b49a525fd52d6/src/the-music-of-the-primes-revised.tex#L1888
[f518j]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/c50ccd138c29a89f800a8740d16b49a525fd52d6/src/the-music-of-the-primes-revised.tex#L1930

## 2026-11-21 · Revision `2026-11-21.11`

Folios 518b–518f are pages 547–551 of the [1,037-page edition][pdf11]. The statements concern Step II on original folio 516 and the trace at a finite set of places in Theorem 12.4.1.1.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [518f · (17.9)][f518f] | On the rational semilocal quotient, the logarithm of the norm and its additive Fourier conjugate give the real and finite Weil terms as one localized trace. This holds for every translate once the set contains the conductor primes and the primes seen by the test. | [d7b1531][semilocal] |
| [518e · (17.8)][f518e] | Tate’s local functional equations give a unitary Fourier operator after theta descent. The trace with two smooth compact norm cutoffs is an absolutely convergent integral of the ratio of its Fourier factors at two frequencies. | [d7b1531][semilocal] |
| [518c · (17.6)][f518c] and [518d · (17.7)][f518d] | Every two-sided smooth cutoff of a rational semilocal theta function has an explicit polar-free lift. For a Gaussian and $r$ finite primes, the one-sided cutoff preserves a leading term proportional to $\log^r(1/y)$ at small norm $y$. No polar-free lift can have this asymptotic. | [d7b1531][semilocal] |
| [518b · (17.5)][f518b] | A continuous multiplier invariant under the diagonal action of $p$ on $\mathbb R\times\mathbb Q_p$ is constant if it carries the Gaussian times the unit ball indicator into the additive Schwartz–Bruhat space. The cutoff and its Fourier conjugate therefore fail the mapping asserted on folio 516. | [d7b1531][semilocal] |

[semilocal]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/d7b15313b1de29afa474b83b804efe50f125cc58
[pdf11]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d7b15313b1de29afa474b83b804efe50f125cc58/output/pdf/the-music-of-the-primes-revised.pdf
[f518b]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d7b15313b1de29afa474b83b804efe50f125cc58/src/the-music-of-the-primes-revised.tex#L1601
[f518c]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d7b15313b1de29afa474b83b804efe50f125cc58/src/the-music-of-the-primes-revised.tex#L1640
[f518d]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d7b15313b1de29afa474b83b804efe50f125cc58/src/the-music-of-the-primes-revised.tex#L1680
[f518e]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d7b15313b1de29afa474b83b804efe50f125cc58/src/the-music-of-the-primes-revised.tex#L1717
[f518f]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d7b15313b1de29afa474b83b804efe50f125cc58/src/the-music-of-the-primes-revised.tex#L1763

## 2026-11-21 · Revision `2026-11-21.10`

Folios 520s–520v are pages 567–570 of the [1,032-page edition][pdf10]. They compare the arithmetic projection of Chapter 10 directly with the prime weights in (17.4).

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [520v · (20aa)][f520v] | Small neighborhoods of all prime-power norms in one translate recover the entire finite-place sum up to $O(X^{-A})$ for any prescribed $A>0$. For zeta, fixed primitive Dirichlet characters and imaginary quadratic ideal class characters this also holds at half-width $1/\log X$. Equation (19) reduces to a bound on the test left after removing those neighborhoods. | [0ed27d3][jumps] |
| [520u · (20z)][f520u] | A test of height one shrinking to $\log n$ gives the limit $\Lambda_\chi(n)/\sqrt n$ for the global distribution. The trace of the projected convolution has the opposite limit. At all integer norms the error can be made $o(n^{-1/2})$ with a single power-law choice of radius at fixed width. | [0ed27d3][jumps] |
| [520t · range of (20y)][f520t] | The zero-density input holds for the three families above at every fixed positive half-width below $1/2$. For arbitrary Hecke characters the log-free density theorem gives an explicit condition on the strip in terms of its density exponent. | [0ed27d3][jumps] |
| [520s · (20y)][f520s] | A count $O(T^{1-\delta}\log^B T)$ for the omitted copies gives a defect $O(\sqrt{x}\,r^\delta\log^B(3/r))$ for a smooth test centered at log norm $\log x$ with radius $r$. The defect has a continuous primitive. Both assertions include omitted boundary multiplicities. | [0ed27d3][jumps] |

[jumps]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/0ed27d39e765e328893116eb8c7ab38d0b23b319
[pdf10]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/0ed27d39e765e328893116eb8c7ab38d0b23b319/output/pdf/the-music-of-the-primes-revised.pdf
[f520s]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/0ed27d39e765e328893116eb8c7ab38d0b23b319/src/the-music-of-the-primes-revised.tex#L2478
[f520t]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/0ed27d39e765e328893116eb8c7ab38d0b23b319/src/the-music-of-the-primes-revised.tex#L2521
[f520u]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/0ed27d39e765e328893116eb8c7ab38d0b23b319/src/the-music-of-the-primes-revised.tex#L2564
[f520v]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/0ed27d39e765e328893116eb8c7ab38d0b23b319/src/the-music-of-the-primes-revised.tex#L2604

## 2026-11-21 · Revision `2026-11-21.9`

Folios 514c–514e are pages 539–541 of the [1,028-page edition][pdf9]. The cutoffs act on the weighted norm line used for the arithmetic quotient in Chapter 10.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [514e · (17.4)][f514e] | The left endpoint gives every positive finite-place term for every translate with source cutoff $Y=e^2X$. One prime already requires $Y$ of order $X$ along a sequence. The two endpoints together have zero trace. Comparison with the global projection to the precision of (19) remains open. | [ecaa340][edge] |
| [514d · (17.3)][f514d] | For a finite set of unramified prime ideals, ideal Möbius inversion turns the endpoint trace into the sum over prime ideal powers. It holds at every strip width, including the full width, and every Sobolev degree $s\ge0$. | [ecaa340][edge] |
| [514c · (17.1)–(17.2)][f514c] | Fourier transformation of local balls determines both signs of the prime distribution. On the weighted line a half-line commutator gives its positive part as an ordinary trace at widths below $1/2$. | [ecaa340][edge] |

[edge]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/ecaa340b043c1de031fdec792eb528931f80ed64
[pdf9]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/ecaa340b043c1de031fdec792eb528931f80ed64/output/pdf/the-music-of-the-primes-revised.pdf
[f514c]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/ecaa340b043c1de031fdec792eb528931f80ed64/src/the-music-of-the-primes-revised.tex#L1424
[f514d]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/ecaa340b043c1de031fdec792eb528931f80ed64/src/the-music-of-the-primes-revised.tex#L1464
[f514e]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/ecaa340b043c1de031fdec792eb528931f80ed64/src/the-music-of-the-primes-revised.tex#L1509

## 2026-11-21 · Revision `2026-11-21.8`

Folios 520o–520r are pages 560–563 of the [1,025-page edition][pdf8]. All four statements use the same fixed test. The logarithmic translation is $\tau=\log X$.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [520r · (20x)][f520r] | For ordinary zeta and the explicit weight $v_*$, the weighted prime-sum error is at most $10^5\sqrt X$ throughout $1\le X\le e^{300000}$. With this numerical constant its extension to every $X\ge1$ is equivalent to RH. | [aae3b39][detector] |
| [520q · (20w)][f520q] | In degree four, the absolute trace defect for ordinary zeta is less than $e^{-140000}$ for $0\le\tau\le300000$ at every strip half-width, including zero. The published simplicity and location of the zeros up to $3\cdot10^{12}$ remove their contributions exactly. An inverse-square sum bounds all higher ordinates. | [aae3b39][detector] |
| [520p · (20v)][f520p] | For every fixed normalized unitary Hecke character, removing margins of width $b_\chi/((\log\tau)^{2/3}(\log\log\tau)^{1/3})$ from the full strip leaves absolute trace defect $O_\chi(\exp(-a\tau^2/4))$. These widths approach the full strip. The geometric estimate at arbitrarily small fixed widths remains open. | [aae3b39][detector] |
| [520o · (20u)][f520o] | A nonnegative smooth log-space test has integral one, a nonvanishing transform throughout the critical strip and absolute transform bounded by $8\exp(-a\sqrt{\lvert u\rvert})$ at height $u$, with $a=(\log 2)/4$. Every omitted zero retains a nonzero Laplace residue. | [aae3b39][detector] |

## 2026-11-21 · Revision `2026-11-21.7`

Folios 522an–522ao are pages 601–602 of the [1,021-page edition][pdf7]. Both estimates apply to the sharp intervals and the fixed character in (58).

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [522ao · (61)][f522ao] | At $U=\exp(\sqrt{\log X})$, the bound $X/U$ for the normalized variance gains the factor $\exp(-c_\chi (\log X)^{3/5}/(\log\log X)^{1/5})$. The general estimate also covers $U\le X^{a_\chi}$ for some fixed $a_\chi>0$. The logarithm of the bound divided by $\log X$ still tends to one at the stated subpower scale. | [fafb857][density] |
| [522an · (60)][f522an] | For each cutoff $R\ge\max(2,U)$, the arithmetic frequency tail costs $O_{F,h}(U\log X/R+XU/R^2)$. The other term reduces to an explicit positive sum over zeros up to height $2R$, to which the fixed-character zero-free region and density theorem apply. | [fafb857][density] |

## 2026-11-21 · Revision `2026-11-21.6`

Folios 522ak–522am are pages 598–600 of the [1,019-page edition][pdf6]. Near prime norm $X$, an interval of log length $1/U$ has ordinary length of order $X/U$.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [522am · (59)][f522am] | For any prescribed $U=X^{o(1)}\ge1$, a normalized short-interval variance of $O_{\chi,h,U,\epsilon}(X^\epsilon)$ for every $\epsilon>0$ is equivalent to RH for the fixed character. For $U=X^\theta$, the same upper bound confines every nontrivial zero to within $\theta/2$ of the critical line. The estimate for $U=\exp(\sqrt{\log X})$ remains open. | [9abdc42][variance] |
| [522al · (58)][f522al] | Integrating squared local prime counts gives a triangular kernel on pairs and a squared sinc weight in frequency. Distinct pairs enter only at log distance at most $1/U$. Their total contribution, including the continuous pole subtraction when present, has absolute value $O_{F,h}(X/U)$. | [9abdc42][variance] |
| [522ak · (57)][f522ak] | On every frequency interval of length $U\ge X/\log X$ the unweighted mean square is $O_{F,h}(\log X)$. If $U\log X/X\to\infty$, its leading term is $r_\chi J(0)\log X$, uniformly in the position of the interval. The two-prime sieve controls the error for a smooth frequency weight. | [9abdc42][variance] |

## 2026-11-21 · Revision `2026-11-21.5`

Folios 522ah–522aj are pages 595–597 of the [1,016-page edition][pdf5]. The field and Hecke character stay fixed. The mean is over the real frequency $v$ of the norm twist in $[U,2U]$.

| Folios and equations | Result | Commit |
| --- | --- | --- |
| [522aj · (56)][f522aj] | For all but a set of frequencies of measure $O_{\chi,h}(U/\log U)$, the same twist has correlation at most half its diagonal value in absolute value at every scale $e\le X\le\sqrt{U\log U}$. Each fixed zero contributes $O_{\rho,h,A}(U^{-A})$ throughout this range for every $A>0$. | [7913485][frequency] |
| [522ai · (55)][f522ai] | For any prescribed $1\le U=o(\log X)$, a mean-square bound of $O_{\chi,h,U,\epsilon}(X^\epsilon)$ at every sufficiently large $X$ for every $\epsilon>0$ is equivalent to RH for the fixed character. Polynomial interpolation recovers the frequency-zero value. An independent estimate in this range remains open. | [7913485][frequency] |
| [522ah · (54)][f522ah] | When $U\ge X$, the centered prime sum has mean square $O_{F,h}(1+\log X)$. This also bounds the mean of the positive part of the distinct-pair contribution from (50). The proof uses a Dirichlet polynomial mean-value estimate and includes the pole subtraction for the principal character. | [7913485][frequency] |

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

[detector]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/aae3b391e90cc5b32d9349990f5a2abe0d2ccde1
[pdf8]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/aae3b391e90cc5b32d9349990f5a2abe0d2ccde1/output/pdf/the-music-of-the-primes-revised.pdf
[f520r]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/aae3b391e90cc5b32d9349990f5a2abe0d2ccde1/src/the-music-of-the-primes-revised.tex#L2311
[f520q]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/aae3b391e90cc5b32d9349990f5a2abe0d2ccde1/src/the-music-of-the-primes-revised.tex#L2270
[f520p]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/aae3b391e90cc5b32d9349990f5a2abe0d2ccde1/src/the-music-of-the-primes-revised.tex#L2226
[f520o]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/aae3b391e90cc5b32d9349990f5a2abe0d2ccde1/src/the-music-of-the-primes-revised.tex#L2187
[density]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/fafb857ea87e094942ba72e8c6f7623aa67ceda6
[pdf7]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/fafb857ea87e094942ba72e8c6f7623aa67ceda6/output/pdf/the-music-of-the-primes-revised.pdf
[f522ao]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/fafb857ea87e094942ba72e8c6f7623aa67ceda6/src/the-music-of-the-primes-revised.tex#L4094
[f522an]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/fafb857ea87e094942ba72e8c6f7623aa67ceda6/src/the-music-of-the-primes-revised.tex#L4055
[variance]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/9abdc42fd396b4c6f3d7b8dca3a9aebf594b0881
[pdf6]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/9abdc42fd396b4c6f3d7b8dca3a9aebf594b0881/output/pdf/the-music-of-the-primes-revised.pdf
[f522am]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/9abdc42fd396b4c6f3d7b8dca3a9aebf594b0881/src/the-music-of-the-primes-revised.tex#L4013
[f522al]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/9abdc42fd396b4c6f3d7b8dca3a9aebf594b0881/src/the-music-of-the-primes-revised.tex#L3974
[f522ak]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/9abdc42fd396b4c6f3d7b8dca3a9aebf594b0881/src/the-music-of-the-primes-revised.tex#L3933
[frequency]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/commit/7913485a8dd1d3461711d5822d1ecc5453be52bc
[pdf5]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/7913485a8dd1d3461711d5822d1ecc5453be52bc/output/pdf/the-music-of-the-primes-revised.pdf
[f522aj]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/7913485a8dd1d3461711d5822d1ecc5453be52bc/src/the-music-of-the-primes-revised.tex#L3890
[f522ai]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/7913485a8dd1d3461711d5822d1ecc5453be52bc/src/the-music-of-the-primes-revised.tex#L3848
[f522ah]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/7913485a8dd1d3461711d5822d1ecc5453be52bc/src/the-music-of-the-primes-revised.tex#L3806
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
