# Open proof obligation for Hecke GRH

## Bound the interval mean over squarefree products of split primes

In revision `2026-11-21.16`, equation (17.4s) is the outstanding arithmetic estimate. Fix $F,\chi$, a strip half-width $0<\alpha<1/2$, and $\varepsilon>0$. Prove that there is a sequence $Y_j\to\infty$ on which

$$
\frac{1}{\log Y_j}\int_{Y_j}^{Y_j^2} X^{-\alpha-\varepsilon}
       [\operatorname{Re} S_{Y_j}(X)]_+\,\frac{dX}{X}
       \le C_{F,\chi,\alpha,\varepsilon}.
$$

The positive part $[r]_+=\max(r,0)$ is taken after the signed sum. The intervals may depend on all four parameters. The fixed widths $\alpha=2^{-\ell}$ for integers $\ell\ge2$ suffice. [Interval criterion, (17.4s)][criterion]

**The sum.** For each window $[Y,Y^2]$, put $D=[F:\mathbb Q]$ and let $R=\prod_{p\le P}p$ be the largest primorial satisfying $R^{2D}\le\sqrt{\log(2Y)}$. Put $H_X=\mathrm e^{-1}(\log(2X))^{4D+1}$, $T=\mathrm e\sqrt X$, and fix a smooth $0\le\omega\le1$ equal to one on $[0,1]$ and zero on $[2,\infty)$. With the fields below, at all sufficiently large $Y$ the sum has the single-index form

$$
S_Y(X)=\frac1{\sqrt X}
\sum_{\substack{X/H_X<k<\mathrm e^{7/4}X/P,\ k\ \mathrm{squarefree}\\
 p\mid k\ \Longrightarrow\ p>P\ \mathrm{and}\ p\ \mathrm{splits\ completely\ in}\ F}}
 u_\chi(k)\,W_{\alpha,X}(k)\,K_{2,R}(X/k).
$$

Here $W_{\alpha,X}(k)$ sums $\omega(d/T)\omega(k/(dT))$ over divisors $d\mid k$ with $|d-k/d|>X^\alpha$. The kernel uses the fixed test $g=(\partial_x+1/2)^3h_*$ and $-L_R L_R'$, with the Euler factors above $p\le P$ removed. For the trivial character $u_\chi(k)=(-D)^{\#\{p:p\mid k\}}$. In general $u_\chi(k)=\prod_{p\mid k}(-\sum_{N\mathfrak p=p}\chi(\mathfrak p))$. [Product and divisor weights, folio 514u][sum] · [Kernel definition, folio 514r][kernel]

**Why it suffices.** Write $b_*=\sup_\rho(\operatorname{Re}\rho-1/2)$. The new linear term costs $O_\varepsilon(X^{b_*/2+\varepsilon})$. If $b_*>\alpha$, a zero exists strictly beyond both $\alpha$ and $b_*/2$. For some $\varepsilon>0$ it forces the displayed means to diverge on every sufficiently distant window. It suffices to prove the bound for the trivial character and for normalized infinite-order characters unramified at every finite place over totally imaginary fields Galois over $\mathbb Q$. [Linear term, folio 514w][linear] · [Zero detection, folio 514x][criterion] · [Character reduction][transfer]

[criterion]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L2314
[sum]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L2183
[kernel]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L2055
[linear]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L2271
[transfer]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/8f1027abb49e5c42b38ee7ce978b4b6de814d7d2/src/the-music-of-the-primes-revised.tex#L4535
