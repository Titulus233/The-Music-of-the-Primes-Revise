# Open proof obligation for Hecke GRH

## Bound the global trace minus the finite trace at all large scales

In revision `2026-11-21.13`, §12.3, the open step is to prove

$$
\left|G_{\alpha,\chi}(g_{\log X})-\mathcal T_{S(\mathrm e^2X),X^2}(g_{\log X})\right|
\ll_{F,\chi,\alpha,\varepsilon} X^{\alpha+\varepsilon}
$$

for all sufficiently large $X$ and every $\varepsilon>0$. One sequence of fixed half-widths tending to zero suffices, for example $\alpha=2^{-j}$ for integers $j\ge 2$. The constant may depend on the field, character and width. Use the single test $g=(\partial_x+1/2)^3h_*$, with $g_t(x)=g(x-t)$. Its Mellin weight removes the principal pole and is nonzero at every nontrivial zero. [Fixed test, (20u)][detector] · [Pole removal, folio 514h][filter]

**The arithmetic estimate.** With $\eta=1/4$, equation (17.4d) makes the trace bound equivalent to

$$
\left|\frac{1}{\sqrt X}
\sum_{\substack{X^{1/4}<d,n\le \mathrm e\sqrt X\\ |d-n|>X^\alpha}}
u_\chi(d)u_\chi(n)K_2\!\left(\frac{X}{dn}\right)\right|
\ll_{F,\chi,\alpha,\varepsilon} X^{\alpha+\varepsilon}.
$$

Here $u_\chi(n)=\sum_{N\mathfrak a=n}\mu_F(\mathfrak a)\chi(\mathfrak a)$, and $K_2$ is the kernel formed from $-L_f(s,\chi)L_f'(s,\chi)$ and $g$ on folio 514g. The absolute value surrounds the entire sum, so cancellation between separated pairs counts toward the bound. [Kernel, folio 514g][kernel] · [Separated pairs, (17.4d)][pairs]

**Characters required.** It suffices to prove this estimate over totally imaginary fields $F$ that are Galois over $\mathbb Q$, for the trivial character and for each normalized infinite-order character unramified at every finite place. Removing a norm twist preserves the real parts of zeros. If the normalized character has finite order, its zeros persist in a Dedekind zeta function of such a field. If it has infinite order, its zeros persist in a character of the second kind. [Zero transfer, folio 522n][transfer]

**Why this closes the proof.** At $Y=\mathrm e^2X$ and $L=X^2$, (17.11) bounds the finite trace minus the Weil distribution by $O(X^{-1})$. The trace bound would then give (19) for $g$, making the Laplace transform of the translated strip defect holomorphic on $\Re z>\alpha$. A zero $\rho$ with $\Re\rho>1/2+\alpha$ would give a nonzero residue at $z=\rho-1/2$. Letting the widths tend to zero and applying the functional equation gives Hecke GRH. Conversely, under Hecke GRH every zero is interior at each positive width, so (18) makes the global trace equal the Weil distribution and (17.11) gives the required bound. [Finite trace, (17.11)][finite] · [Strip defect, (18)–(19)][defect] · [Residue argument, folio 29][residue]

[detector]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L2889
[filter]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1665
[kernel]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1591
[pairs]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L1677
[transfer]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L3939
[finite]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L2098
[defect]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L2179
[residue]: https://github.com/Titulus233/The-Music-of-the-Primes-Revise/blob/5b96f531c6139993e1e6505301e56b6480500703/src/the-music-of-the-primes-revised.tex#L194
