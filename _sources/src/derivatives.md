# Derivatives

We start from the defining equations:

$$u=\int_0^{\phi}\frac{d\theta}{\sqrt{1-m\sin^2\theta}}$$

We consider $u=\mathrm{am}\phi$. The Jacobi elliptic functions $\mathrm{sn}u:=\sin\phi$ and $\mathrm{cn}u:=\cos\phi$ can be differentiated relatively straightforwardly:

$$\frac{d\mathrm{sn}u}{du}=\frac{d\mathrm{sin}\phi}{d\phi}\frac{d\phi}{du}=\mathrm{cn}u{d\phi}\frac{d\phi}{du}$$

$$\frac{d\mathrm{cn}u}{du}=-\mathrm{sn}u\frac{d\phi}{du}$$

so long as we get a decent expression for $d\phi/du$.


Differentiating the integral gives:

$$\frac{du}{d\phi}=\frac{1}{\sqrt{1-m\mathrm{sn}^2u}}=:\frac{1}{\mathrm{dn}u}$$

Inverting gives:

$$\frac{d\mathrm{sn}u}{du}=\mathrm{cn}u\mathrm{dn}u$$

$$\frac{d\mathrm{cn}u}{du}=-\mathrm{sn}u\mathrm{dn}u$$

It is also handy to be able to differentiate $\mathrm{dn}$. We use $\mathrm{dn}^2u+m\mathrm{sn}^2u=1$:

$$2\mathrm{dn}u\frac{d\mathrm{dn}u}{du}+2m\mathrm{sn}u\frac{d\mathrm{sn}u}{du}=0$$

Thus:

$$\frac{d\mathrm{dn}u}{du}=-m\mathrm{sn}u\mathrm{cn}u$$

At this stage we consider only real $0\lt m\lt1$ to avoid having to consider integrating around branch cuts etc. (What about negative $m\le0$?) In particular this means that $\phi$ increases strictly monotonically with $u$ (and _vice versa_), giving continuous one-to-one correspondence (bijection). It seems a little silly to describe this as a diffeomorphism.

To tie in with the cnoidal wave differential equation we need:

$$\frac{d\mathrm{cn^2}u}{du}=-2\mathrm{sn}u\mathrm{cn}u\mathrm{dn}u$$

Similarly:

$$\frac{d\mathrm{sn^2}u}{du}=2\mathrm{sn}u\mathrm{cn}u\mathrm{dn}u$$

$$\frac{d\mathrm{dn^2}u}{du}=-2m\mathrm{sn}u\mathrm{cn}u\mathrm{dn}u$$

If we square:

$$\left(\frac{d\mathrm{cn^2}u}{du}\right)^2=4\mathrm{sn}^2u\mathrm{cn}^2u\mathrm{dn}^2u=4\mathrm{cn}^2u(1-\mathrm{cn}^2u)(1-m+m\mathrm{cn}^2u)$$

Differentiating once more:

$$\begin{align}\frac{d^2\mathrm{cn^2}u}{du^2}&=-2\mathrm{cn^2}u\mathrm{dn^2}u+2\mathrm{sn^2}u\mathrm{dn^2}u+2m\mathrm{sn^2}u\mathrm{cn^2}u \\
&=2-2m+(8m-4)\mathrm{cn^2}u-6m\mathrm{cn^4}u\end{align}$$