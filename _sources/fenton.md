# Fenton's approach

[Fenton](https://johndfenton.com/Papers/Fenton99Cnoidal-The-cnoidal-theory-of-water-waves.pdf) uses a series expansion for the stream function about the bed of the flow:

$$\psi=-\sin\left(Y\frac{d}{dX}\right)f(X)=-\sum_{n=1}^\infty(-1)^n\frac{Y^{2n+1}}{(2n+1)!}\frac{d^{2n+1}}{dX^{2n+1}}f(X)$$

This form imposes the Laplace equation $\nabla^2\psi=0$, and the boundary condition, $\psi(X,0)=0$ on the flow bed.

The surface wave form $\eta(X)$ is such that $\psi(X,\eta(X))=-Q$, a constant.

More complex is imposing the Bernoulli equation.

We need the velocity $(U,V)$ in terms of $f$:

$$U=\frac{\partial\psi}{\partial Y}=-\cos\left(Y\frac{d}{dX}\right)f'(X)$$

$$V=-\frac{\partial\psi}{\partial X}=\sin\left(Y\frac{d}{dX}\right)f'(X)$$

So we have:

$$Q=-\psi(X,\eta(X))=\sin\left(\eta(X)\frac{d}{dX}\right)f(X)$$

the flux equation, and

$$R=\frac12(U^2+V^2)+g\eta$$

The Bernoulli equation at the surface.

Differentiating the flux equation with respect to $X$:

$$0=\frac{dQ}{dX}=\cos\left(\eta\frac{d}{dX}\right)f'(X)\frac{d\eta}{dX}+\sin\left(\eta\frac{d}{dX}\right)f'(X)$$

giving:

$$R=\left(1+\left(\frac{d\eta}{dX}\right)^2\right)\left(\cos\left(\eta\frac{d}{dX}\right)f'(X)\right)^2+g\eta$$

Fenton considers $\eta\approx h$ the undistubed depth. He replaces $X$ with a scaled dimensionless variable $\theta=\alpha X/h$. The surface profile $\eta$ is also scaled as $\eta_*=\eta/h$. Finally, $f_*=\alpha f/Q$, differing from Fenton's paper by a factor of $\alpha$.

In these terms $d/dX=(\alpha/h)d/d\theta$.

The factor in $f_*$ of $\alpha$ maintains the character of being an expansion in powers of $\alpha^2$ in the first term of Fenton's recasting of the flux/kinetic equation:

$$\frac1\alpha\sin\left(\alpha\eta_*(\theta)\frac{d}{d\theta}\right)f_*(\theta)-1=0$$

The dynamic Bernoulli condition becomes:

$$\frac12\left(1+\left(\alpha\frac{d\eta_*}{d\theta}\right)^2\right)\left(\cos\left(\alpha\eta_*\frac{d}{d\theta}\right)\frac{d}{d\theta}f_*(\theta)\right)^2+g_*\eta_*=R_*$$

with $g_*=gh^3/Q^2$ and $R_*=Rh^2/Q^2$.

Looking at these equations in the $\alpha\rightarrow0$ limit, assuming $\eta\rightarrow h$, a flat surface:

$$\eta_*\rightarrow1$$

$$f_*'(\theta)\rightarrow1$$

From the flux equation we have $Q=-Uh$, and the Bernoulli equation is $R=U^2/2+gh$.

Thus $R_*=\frac12+g_*$, and assuming the scaling is such that $g_*=1$, we get $R_*=\frac32$.