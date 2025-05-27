# Momentum flux

The momentum of a flow cell is $\rho \mathbf vdxdy(dz\dots)$. The flux is a (symmetric) tensor $\rho v_i v_j$.

To measure the momentum flow through a surface, say the vertical $x=\mathrm{constant}$, so that the normal is in the $x$-direction. In 2D we have:

$$\mathbf M=\int\rho \mathbf v udy$$

where $u=(\mathbf v)_x$.

Benjamin&ndash;Lighthill show that the horizontal momentum flux, with a correction for pressure forces, is constant. First the corrected flux per unit mass is:

$$S=\int_0^\eta\left(\frac p\rho+u^2\right) dy$$

We also have $R=\mathbf v^2/2+p/\rho+gy$, so:

$$S=\int_0^\eta\left(R-gy-(u^2+v^2)/2+u^2\right) dy$$

At the moment, $S$ might be a function of $x$. Differentiating:

$$\frac{dS}{dx}=\frac{d\eta}{dx}\left(R-gy-(u^2+v^2)/2+u^2\right)+\int_0^\eta \left(u\frac{\partial u}{\partial x}-v\frac{\partial v}{\partial x}\right)dy$$

The first part is evaluated at $y=\eta$. We can make the integrand partials be over $y$ rather than $x$, assuming incompressibility and irrotationality:

$$\frac{\partial u}{\partial x}=-\frac{\partial v}{\partial y}$$

$$\frac{\partial v}{\partial x}=+\frac{\partial u}{\partial y}$$

$$\begin{align}
\frac{dS}{dx}&=\frac{d\eta}{dx}\left(R-gy-(u^2+v^2)/2+u^2\right)-\int_0^\eta \left(u\frac{\partial v}{\partial y}+v\frac{\partial u}{\partial y}\right)dy \\
&= \frac{d\eta}{dx}\left(R-gy-(u^2+v^2)/2+u^2\right)-uv
\end{align} $$

The new $uv/2$ term replacing the integral is also evaluated at $y=\eta$, since the terms for $y=0$, since we assume $v=0$ there.

The value of $d\eta/dx=v/u$, hence $uv=u^2(d\eta/dx)$, so

$$\frac{dS}{dx}=\frac{d\eta}{dx}\left(R-gy-\frac12(v^2+u^2)\right)=0$$

Benjamin&ndash;Lighthill seem to take it as obvious (not to me) that $S$ is constant, and derive instead the Bernoulli principle at the surface:

$$R=\frac12(u^2+v^2)+g\eta$$

with $p=0$. Perhaps it is a matter of experience and taste.
