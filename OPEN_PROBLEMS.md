# Open proof obligation for Hecke GRH

## Bound the interval mean over coprime norms

In revision `2026-11-21.15`, the outstanding arithmetic estimate is (17.4o). Fix a number field $F$, a normalized Hecke character $\chi$ and a half-width $0<\alpha<1/2$. For every $\varepsilon>0$, prove that there is a sequence $Y_j\to\infty$ on which

$$
\frac{1}{\log Y_j}\int_{Y_j}^{Y_j^2} X^{-\alpha-\varepsilon}
       [\operatorname{Re} C_{Y_j}(X)]_+\,\frac{dX}{X}
       \le C_{F,\chi,\alpha,\varepsilon}.
$$

Here $[r]_+=\max(r,0)$ is taken after the signed sum. The sequence may depend on all four parameters. The fixed widths $\alpha=2^{-k}$, $k\ge2$, suffice. [Criterion, (17.4o)][criterion]

**The sum to estimate.** Put $D=[F:\mathbb Q]$. On $[Y,Y^2]$ let $R=\prod_{p\le P}p$ be the largest product of consecutive primes starting at $2$ with $R^{2D}\le\sqrt{\log(2Y)}$. Keep this $R$ fixed across the interval. Write $H_X=\mathrm e^{-1}(\log(2X))^{4D+1}$. The two integer norms are coprime to one another and have all prime factors greater than $P$.

$$
C_Y(X)=\frac1{\sqrt X}
\sum_{\substack{d,n\le\mathrm e\sqrt X,\ \gcd(d,n)=\gcd(dn,R)=1\\
 X/H_X<dn<\mathrm e^{7/4}X/P,\ |d-n|>X^\alpha}}
 u_\chi(d)u_\chi(n)K_{2,R}\!\left(\frac{X}{dn}\right).
$$

The coefficients are $u_\chi(n)=\sum_{N\mathfrak a=n}\mu_F(\mathfrak a)\chi(\mathfrak a)$. The kernel uses the fixed test $g=(\partial_x+1/2)^3h_*$ and $-L_R L_R'$, where $L_R$ omits every Euler factor above a rational prime dividing $R$. This gives $O(X(1+\log P)/P)=o(X)$ candidate pairs uniformly on the interval. [Sum and kernel, (17.4m)][pairs]

**Why this closes the proof.** The arithmetic comparison (17.4n) has error $O_{F,\chi,\alpha,\varepsilon}(X^{\alpha+\varepsilon})$ uniformly across the intervals. An exterior zero would give $b>\alpha$ for which the displayed mean is at least $cY^{b-\alpha-\varepsilon}/\sqrt{\log Y}$ on every sufficiently distant interval when $0<\varepsilon<b-\alpha$. The bounded subsequence would exclude that zero. It suffices to treat the trivial character and the normalized infinite-order characters unramified at every finite place over totally imaginary fields Galois over $\mathbb Q$. [Arithmetic comparison][comparison] · [Exterior-zero lower bound][criterion] · [Character reduction][transfer]

[criterion]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L2135
[pairs]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L2055
[comparison]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L2094
[transfer]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/d855aa10dddc64d3603af4b4890a8b4817c81204/src/the-music-of-the-primes-revised.tex#L4363
