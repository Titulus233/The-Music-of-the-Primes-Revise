# Open proof obligation for Hecke GRH

## Bound the positive part of the separated Möbius sum on arbitrarily distant intervals

In revision `2026-11-21.14`, the outstanding arithmetic estimate is (17.4i). Fix the field $F$, the character $\chi$, and a strip half-width $0<\alpha<1/2$. For every $\varepsilon>0$, prove that some sequence $Y_j\to\infty$ satisfies

$$
\frac{1}{\log Y_j}\int_{Y_j}^{Y_j^2}
   \frac{[\operatorname{Re}Q_{\alpha,\chi}(X)]_+}{X^{\alpha+\varepsilon}}\,
   \frac{dX}{X}\ \le\ C_{F,\chi,\alpha,\varepsilon}
\quad\text{for every }j .
$$

Here $[r]_+=\max(r,0)$. The positive part is taken **after** summing all the pairs. The interval sequence may depend on $F,\chi,\alpha,\varepsilon$. For Hecke GRH it suffices to use the widths $\alpha=2^{-k}$, $k\ge2$. [Criterion, (17.4i)][criterion]

**The sum to estimate.** Put $D=[F:\mathbb Q]$ and $H_X=\mathrm e^{-1}(\log(2X))^{4D+1}$. Then

$$
Q_{\alpha,\chi}(X)=\frac{1}{\sqrt X}
\sum_{\substack{d,n\le\mathrm e\sqrt X,\ dn>X/H_X\\ |d-n|>X^\alpha}}
  u_\chi(d)u_\chi(n)K_2\!\left(\frac{X}{dn}\right).
$$

The coefficient is $u_\chi(n)=\sum_{N\mathfrak a=n}\mu_F(\mathfrak a)\chi(\mathfrak a)$. The kernel $K_2$ on folio 514g uses the fixed test $g=(\partial_x+1/2)^3h_*$ from folios 514h and 520o. For every fixed $A>0$, the pairs with $dn\le X/H_X$ contribute $O_A(X^{-A})$ in absolute value. [Kernel definition][kernel] · [Norm cutoff, (17.4f)][cutoff] · [Signed sum, (17.4g)][sum]

**Characters required.** It suffices to treat the trivial character and the normalized infinite-order characters unramified at every finite place, over totally imaginary fields Galois over $\mathbb Q$. The real parts of zeros survive normalization and transfer to these cases. [Field and character reduction, folio 522n][transfer]

**Why this proves (19).** A zero outside the strip forces a centered real part $b>\alpha$ for which the displayed mean grows at least as $Y^{b-\alpha-\varepsilon}/\sqrt{\log Y}$ on every sufficiently distant interval when $0<\varepsilon<b-\alpha$. Bounded means on the chosen sequence would exclude that zero. Taking the widths to zero gives zero location, and the strip defect formula then gives (19). [Local lower bound, (17.4h)][sum] · [Strip defect, (18)–(19)][defect]

[criterion]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1892
[kernel]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1591
[cutoff]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1759
[sum]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L1800
[transfer]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L4115
[defect]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/92c242ebbfb35cef729d4f52b3caa88451ddd002/src/the-music-of-the-primes-revised.tex#L2355
