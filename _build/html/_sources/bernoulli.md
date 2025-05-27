# Bernoulli principle

By considering the forces on a differential volume $dxdy(dz\dots)$ we have from Newton's mechanics:

$$\rho\frac{d\mathbf v}{dt}=-\nabla p-\rho\mathbf g$$

Multiplying by $\mathbf v=d\mathbf r/dt$ we have the energy (density) equation:

$$\rho\frac{d}{dt}\left[\frac 12 \mathbf v^2+\frac p\rho+\mathbf{g.r}\right]=0$$

We are assuming that $\rho$, the mass density, is constant throughout the flow, i.e. the fluid is "incompressible". Another assumptions is no friction or viscosity ("inviscid" flow).

We also want to declare the square bracket to be in some sense "constant". But constant where? At the point? Along a streamline? Everywhere?

We are implicitly assuming the flow here is "steady" ($\partial/\partial t$ is zero, for the wave problem we are moving at the wave speed in the positive direction so the general flow is in the negative direction), so the constant at a point inference would be a given.

In [Linear waves from complex potential](clinear.ipynb), I have plotted streamlines for a background flow plus a linear trigonometric wave. Also I have plotted $\mathbf v^2/2+gy=R$, which is the part of the energy density for that problem without the pressure term. In Benjamin and Lighthill $R$ is called the "total head". I suspect they a referring to the total head at "zero" pressure, or adjusted for atmospheric pressure. Also they are evaluating at the surface/interface with the atmosphere. Fenton includes pressure in $R=\mathbf v^2/2+p/\rho+gy$. Lower down in the Benjamin&ndash;Lighthill paper, they indeed include the pressure term in $R$, so I will assume that the expression without pressure is an evaluation at the surface rather than a definition and use the Fenton form. Looking around the internet one finds further "heads" for velocity, pressure, and elevation, which is merely splitting up the separate terms in the obvious way.

Without surface tension effects, the atmospheric pressure can be absorbed into $R$. It doesn't exactly match the expected streamline, because the "real" flow (well, not really "real", but theoretical on the basis of the nice assumptions of no friction and so on) involves nonlinear dependences between the wave amplitude and wave speed and so on. Improvements can be made by various series approximations, as given by Stokes, Kortweg-de Vries, Fourier etc., along with appropriate numerical procedures: finite-element/-difference, truncation . . .

Let us try to find the gradient of R:

$$\mathbf \nabla R=\nabla \left[\frac 12 \mathbf v^2+\frac p\rho+\mathbf{g.r}\right]$$

Using $\mathbf{\nabla (A.B)}=\mathbf{A.\nabla B+B.\nabla A+A\wedge(\nabla\wedge B)+B\wedge(\nabla\wedge A)}$ we have

$$\mathbf \nabla R=\mathbf{v.\nabla v+v\wedge(\nabla\wedge v)}+\frac {\mathbf\nabla p}\rho+\mathbf g$$

But $d\mathbf v/dt=\partial\mathbf v/\partial t+\mathbf{v.\nabla v}$, so in steady state:

$$\mathbf \nabla R=\mathbf{v\wedge(\nabla\wedge v)}$$

If $\mathbf v$ is irrotational, $\mathbf{\nabla\wedge v}=0$, the gradient of $R$ is zero, and thus the square bracket in Bernoulli's principle above is constant everywhere, not just on streamlines.

We probably should add that inviscid situations, a region where the flow is irrotational remains so by Kelivn's circulation theorem, if anybody needs to look that up.
