# Complex potential flow

In two-dimensional (2D) problems a potential giving the velocity profile as a gradient $\mathbf{v}=(u,v)=\mathbf{\nabla} \phi$ is often a useful simplification.

Firstly this requires _irrotational_ flow, i.e. the "curl" pseudoscalar is zero:

$$\nabla\wedge\mathbf{v}=0$$

We will investigate this aspect more closely shortly.

Our main interest will be _incompressible_ flows $\mathbf{\nabla}.\mathbf{v}=0$. This implies that the potential satisfies the Laplace equation, $\mathbf{\nabla}^2\phi=0$, i.e. $\phi$ is a "harmonic function".

In 2D harmonic functions are closely connected with analytic function theory. Harmonic functions have a conjugate that is unique up to a constant. The conjugate is also harmonic and forms the imaginary part of an analytic function with the original harmonic as the real part. Let us provisionally label the conjugate as $\psi$, so $f=\phi+i\psi$ is analytic in a variable $z=x+iy$.

The Cauchy-Riemann equations specify that:

$$\frac{df}{dz}=\frac{\partial f}{\partial x}=\frac{\partial f}{i\partial y}$$

Expanding the $f$ in the partial derivatives into real and imaginary parts gives:

$$\Re\frac{df}{dz}=\frac{\partial \phi}{\partial x}=\frac{\partial \psi}{\partial y}$$

$$\Im\frac{df}{dz}=-\frac{\partial \phi}{\partial y}=\frac{\partial \psi}{\partial x}$$

Remembering that the velocity components are the gradient components of $\phi$:

$$u=\frac{\partial \phi}{\partial x}=\Re\frac{df}{dz}$$

$$v=\frac{\partial \phi}{\partial y}=-\Im\frac{df}{dz}$$

So we can define a complex velocity $w=u-iv=df/dz$ as a gradient of $f$ in $z$.

We can now define $f$ as a line integral of $w$, $f=\int_P wdz$ over some path from a fixed point $z_0$. The Cauchy–Goursat (integral) theorem tells us that $f$ will be independent of the path $P$ so long as it is constrained to simply-connected domains. This means no holes to allow for poles, or crossing of branch cuts without understanding that $f$ most likely doesn't have the original value (Riemann sheets and all that).

In the simply-connected case imagine two paths, $P_1,P_2$, say, giving values at $z$ of $F_1$ and $F_2$. We can caculate the difference $F_2-F_1=\int_{P_2-P_1}wdz$, but $P_2-P_1$ is a closed loop enclosing a region where $w$ is analytic throughout, so the integral theorem tells us that $F_2-F_1=0\implies F_2=F_1$, i.e. the value is path independent within the terms stated.

The possible different constants for the conjugate function $\psi$ can now be seen to result from different choices of the base point $z_0$. When evaluating $w$ the constant is irrelevant.

We now look at the meaning of these line integrals. The real part is $\phi(z)-\phi(z_0)$ in what I hope is an obvious notation using $z=x+iy$ instead of $x,y$ as the argument. In terms of the line integral we have:

$$\phi(z)-\phi(z_0)=\Re\int_P wdz=\int_P udx+vdy=\int_P \mathbf{v.dr}$$

This is what it means for a vector to be derived from a potential.

The imaginary part gives meaning to $\psi$ beyond being a harmonic conjugate of $\phi$:

$$\psi(z)-\psi(z_0)=\Im\int_P wdz=\int_P udy-vdx=\int_P \mathbf{v\wedge dr}$$

The path independence reduces to the 2D gauss theorem, resulting from the incompressibility. The difference in value of $\psi$ between two points gives the matter rate of flow from left to right facing $z$ through the gap from $z_0$. In terms of differentials $\mathbf {dr}$: e.g. when $dx=0$ the differential mass flow is $udy$, and when $dy=0$ the flow is $-vdx$.

A particularly important observation is that if $\psi$ is constant along a path no mass flows across it: in other words the flow is parallel to the path, a stream line, giving $\psi$ its official name as the _stream function_.