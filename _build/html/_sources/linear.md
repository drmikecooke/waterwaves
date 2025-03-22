# Linear theory from stream function

The work is based on {cite}`fenton99`, where the formal situation is discussed at length. We use units $k,g=1,1$. The linear solution will be used in or numerical solution software as the 'first guess' for the equation solver component of the code (coming from the scipy module). The first order laterally ($x$-axis) periodic stream function is:

$$\psi(x,y)=-\bar Uy+B\frac{\sinh y}{\cosh d}\cos x$$

The frame is moving in the positive $x$-direction at speed $\bar U$. The depth of the water is $d$. The surface when $B=0$ is at $y=d$.

We tickle the surface $y=\eta(x)=d+a\cos x$ with $a$ small.

The kinematic boundary condition is $\psi(x,\eta)=-Q$ with $Q$ a constant. We will see that the minus sign will give $Q>0$.

We have:

$$\sinh \eta=\sinh d \cosh(a\cos x)+\cosh d \sinh(a\cos x)$$

Keeping the linear $a$ term:

$$\sinh \eta\approx\sinh d +a\cosh d \cos x$$

We assume that $B$ will be proportional to $a$ at a first approximation.

Therefore:

$$\psi(x,\eta)\approx-\bar U(d+a\cos x)+B\tanh d\cos x$$

We see that $Q\approx\bar Ud$ and $B\approx\bar Ua\coth d$.

We now must consider the dynamic boundary condition that the pressure is constant at the top boundary. In terms of the instantaneous fluid velocity, $(u,v)$, we have:

$$\frac12(u^2+v^2)+\eta=R$$

where $R$ is a constant, and velocity is determined at $y=\eta$. The velocity components can be derived from:

$$u,v=\frac{\partial\psi}{\partial y},-\frac{\partial\psi}{\partial x}$$

With $$\psi(x,y)\approx-\bar U\left(y-a\coth d\frac{\sinh y}{\cosh d}\cos x\right)$$

we get:

$$u\approx-\bar U\left(1-a\coth d\frac{\cosh y}{\cosh d}\cos x\right)$$

$$v\approx a\bar U\coth d\frac{\sinh y}{\cosh d}\sin x$$

Keeping only terms linear in $a$, the dynamic boundary condition is:

$$R\approx\bar U^2\frac12(1-2a\coth d\cos x)+d+a\cos x$$

since $\cosh\eta\approx\cosh d$ to this order. To make this expression constant we need $\bar U^2\approx\tanh d$. We then have:

$$R\approx\frac12\bar U^2+d$$

## Getting out of deep water

These formulae get tricky when $d\rightarrow\infty$, requiring a certain amount of reworking to avoid infinite quanities.

First we redefine the y origin from bottom to the top: i.e. the flat water surface, $y\rightarrow y-d$. The hyperbolic functions in $\psi$ have large arguments, so $\sinh,\cosh\approx\exp/2$, and we have (dropping an infinite constant from the first term):

$$\psi(x,y)=-\bar Uy+B\exp y\cos x$$

We now have $\eta(x)=a\cos x$ with $a$ small.

The condition $\psi(x,\eta)=-Q$ gives:

$$\psi(x,\eta)\approx-\bar Ua\cos x+B\cos x$$

so $B=\bar Ua$ and $Q=0$. Pretty much as expected for $B$, and $Q$ has been renormalized as a result of dropping the infinite constant $\bar Ud$.

The velocity components:

$$u\approx\bar U(-1+a\cos x)$$

$$v\approx\bar Ua\sin x$$

Therefore:

$$R=\frac12(u^2+v^2)+\eta\approx\bar U^2(1-2a\cos x)/2+a\cos x$$

So $\bar U\approx1$, and $R\approx\frac12$.