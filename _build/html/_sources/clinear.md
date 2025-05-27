# Linear waves from complex potential

We use a complex potential $\Omega=\phi+i\psi$. We look for approximate solutions $\Omega=-cz+B\sin z$.

We have velocity components $u+iv=d\Omega/dz=-c+B\cos z$.

We are interested in small deviations from $d$ with a surface wave $\eta=d+a\cos x$, where the imaginary part of $\Omega$, $\psi$, is a constant, $-Q$. This is the kinematic boundary condition. The parameter $c$ represents the speed the wave is travelling, and we are working in the moving frame where the wave profile is stationary.

Assuming $a$ and $B$ small:

$$\Omega=-c(x+i\eta))+B\sin(x+i\eta))\approx -c(x+i(d+a\cos x))+B\sin(x+i(d+a\cos x))$$

We want the imaginary part of $\Omega$ to be constant to leading order in $a,B$:

$$\Omega\approx -c(x+i(d+a\cos x))+B\sin(x+id)$$

This will set up a relation between the small parameters when we resolve the imaginary part using trigonometric and hyperbolic relationships of the second part:

$$B\sin(x+id)=B(\sin x\cos(id)+\cos x\sin(id)))=B(\sin x\cosh d+i\cos x\sinh d)$$

For constant $\psi$ we impose the constraint $B\sinh d=ca$, giving:

$$\Omega\approx -c(x+id)+B\sin x\cosh d$$

The constant $Q=cd$. The original $\Omega$ form with $\sin z$ was chosen to give the peak at $x=0$.

The dynamic boundary condition is:

$$R=|U|^2/2+\eta$$

with $U=d\Omega/dz$

Again to leading order in $a,B$:

$$R\approx |-c+B\cos(x+id)|^2/2+d+a\cos x$$

The imaginary part of $U$ can be ignored as second order in $B$:

$$R\approx (-c+B\cos x\cosh d)^2/2+d+a\cos x$$

Expanding the square and dropping the second order term:

$$R\approx c^2/2-cB\cos x\cosh d+d+a\cos x$$

We need $a=cB\cosh d$ to  make $R$ approximately constant at the wave surface. Combining with the relation $B\sinh d=ca$, we get $\sinh d=c^2\cosh d$ or $c^2=\tanh d$.

Thus $R\approx c^2/2+d$.