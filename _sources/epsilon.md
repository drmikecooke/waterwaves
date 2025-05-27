# Jacobi epsilon function

The epsilon function is defined as $\mathscr E(u,m)=E(\mathrm{am}(u,m),m)$. Here $E$ is the incomplete elliptic integral function of the second kind. The $\mathrm{am}$ function is the function connecting the elliptic and circular functions: $\mathrm{sn}(u,m)=\sin(am(u,m))$.

For the Jacobi zeta function there seems to be divergence between [DLMF &sect;22.16](https://dlmf.nist.gov/22.16) and [wikipedia](https://en.wikipedia.org/wiki/Elliptic_integral#Jacobi_zeta_function).

DLMF presents it as a function of $u=x$, and the modulus $k^2=m$:

$$Z(u,k)=\mathscr E(u,k)-E(k)u/K(k)$$

Wikipedia sees it rather as a function of $\phi=\mathrm{am}(u,m)$

$$Z(\phi,k)=E(\phi,k)-E(k)u/K(k)F(\phi,k)$$

where $F$ is the incomplete elliptic integral of the first kind. Wikipedia then goes on to define:

$$\mathrm{zn}(u,k)=Z(\mathrm{am}(u,k),k)$$

which is essentially DLMF's $Z$.

We will use the DLMF version, but using the parameter $m$, rather than the modulus $k$.

Abramowitz and Stegun use the forms $Z(\phi\textbackslash\alpha)$ and $Z(u|m)$ to distinguish the two cases. Here $\sin^2\alpha=m$. They seem to use the same convention, but not mentioning "Jacobi's epsilon" in the form $\mathscr E(u,m)=E(u)$, dropping the reference to m.

Let us look a bit more closely at $\mathscr E(u,m)$:

$$\frac{d\mathscr E(u,m)}{du}=\frac{dE(\phi,m)}{d\phi}\frac{d\phi}{du}$$

In [Derivatives](derivatives.md) we show that $d\phi/du=\mathrm{dn}u$.

We also have:

$$E(\phi|m)=\int_0^\phi\sqrt{1-m\sin^2\theta}d\theta$$

so $dE/d\phi=\sqrt{1-m\sin^2\phi}=\mathrm{dn}u$, and

$$\frac{d\mathscr E(u,m)}{du}=\mathrm{dn}^2u$$

If $m\lt1$, there is no branch cut problem, at least for $u\in\mathbb R$.

Tranferring this result to $Z$:

$$\frac{Z(u,m)}{du}=\mathrm{dn}^2u-E(m)/K(m)$$