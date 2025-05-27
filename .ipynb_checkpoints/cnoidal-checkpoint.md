# Cnoidal waves from Benjamin and Lighthill

We use a Taylor expansion in (small) $y$: $\psi=\sum_ny^nf_n(x)=f_0+yf_1+y^2f_2+\dots$. Imposing Laplace's equation gives $\sum_ny^n(f''_{n}(x)+(n+2)(n+1)f_{n+2}(x))$. We actually want $\psi(x,0)=0$, so we only want the odd terms, which can be generated from the single function $f=f_1$:

$$\psi=\sum_{n=0}(-1)^n\frac{y^{2n+1}}{(2n+1)!}\frac{d^{2n+1}}{dx^{2n+1}}f(x)=\sin(yD)f(x)$$

with the operator $D=d/dx$. The significance of this from the perspective of a complex potential will be studied elsewhere (I hope).

We only need the first two terms: $\psi\approx yf-y^3f''/3!$.

The constant $S$ is:

$$S=\int_0^\eta\left(R-gy+(u^2-v^2)/2\right) dy$$

The stream function determines $u=\partial\psi/\partial y\approx f-y^2f''/2$ and $v=-\partial\psi/\partial x\approx -yf'+y^3f'''/3!$. But Benjamin&ndash;Lighthill ignore terms fourth order in $y$ and higher, so we can use $v\approx-yf'$.

Performing the integral:

$$S\approx R\eta-g\eta^2/2+f^2\eta/2-ff''\eta^3/3!-f'^2\eta^3/3!$$

To the same order $Q=\psi(x,\eta)\approx \eta f-\eta^3f''/3!$

Also by differentiating with respect to $x$, $\eta'f+\eta f'-\eta^2\eta'f''/2-\eta^3f'''/3!\approx 0$

We use these relations to eliminate $f$ in favour of $\eta$ and $Q$.

First $f^2\eta/2\approx (Q/\eta+\eta^2f''/3!)^2\eta/2\approx Q^2/2\eta+\eta^2Qf''/3!$

Second $-ff''\eta^3/3!\approx -(Q/\eta+\eta^2f''/3!)f''\eta^3/3!\approx-\eta^2Qf''/3!$, conveniently cancelling the $f''$ in the previous expression.

Finally, we need $f'$ only up to zero order in $\eta$, $f'\approx -Q\eta'/\eta^2$. Gathering the bits:

$$\begin{align}S&\approx R\eta-g\eta^2/2+Q^2/2\eta-(-Q\eta'/\eta^2)^2\eta^3/3! \\
&\approx R\eta-g\eta^2/2+Q^2/2\eta-(Q\eta')^2/3!\eta
\end{align}$$

Rearranging ito a first order differential equation:

$$(Q\eta')^2=3Q^2-6S\eta+6R\eta^2-3g\eta^3$$

This is essentially (20) in Benjamin&ndash;Lighthill. We now need to explore the meaning of these equations in a more concrete fashion.