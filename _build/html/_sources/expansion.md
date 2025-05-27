# $\alpha$ expansion

The flux/kinetic boundary condition is:

$$\frac1\alpha\sin\left(\alpha\eta_*(\theta)\frac{d}{d\theta}\right)f_*(\theta)-1=0$$

The dynamic Bernoulli condition is:

$$\frac12\left(1+\left(\alpha\frac{d\eta_*}{d\theta}\right)^2\right)\left(\cos\left(\alpha\eta_*\frac{d}{d\theta}\right)f'_*(\theta)\right)^2+g_*\eta_*=R_*$$

with scaling according to [fenton](fenton.md)

Using the $\alpha\rightarrow0$ limits:

$$\eta_*=1+\sum_{j=1}^\infty\alpha^{2j}H_j(\theta)$$

$$f'_*=1+\sum_{j=1}^\infty\alpha^{2j}F_j(\theta)$$

$$g_*=1+\sum_{j=1}^\infty\alpha^{2j}G_j$$

$$R_*=\frac32+\sum_{j=1}^\infty\alpha^{2j}r_j$$

The kinetic equation at $\alpha^2$ gives $H_1+F_1=0$.

The dynamic $\alpha^2$ power leads to $F_1+g_1+H_1=r_1$ (first term is from the U^2/2 term, and the second and third from the cross terms of $g_*\eta_*$. Combining we determine that $H_1=-F_1$ and $g_1=r_1$.

At the next $\alpha^4$ order we start to see some derivatives:

$$H_2+F_2+H_1F_1-\frac{F''_1}6=0$$

from the kinetic consideration, and:

$$F_2+\frac12F_1^2-\frac12F''_2+g_2+g_1H_1=r_2$$

These equations can be combined:

$$\frac13F''_1-\frac32F_1^2+r_2-g_2+g_1F_1=0$$

Fenton compares this to the equation for $d^2cn^2(u)/du^2$:

$$\frac{d^2\mathrm{cn^2}u}{du^2}=2-2m+(8m-4)\mathrm{cn^2}u-6m\mathrm{cn^4}u$$

So we can assume $F_1(\theta)=A_1\mathrm{cn^2}\theta$ with $m$ as the assumed parameter. First comparing the double derivative and square term:

$$\frac92A_1=-6m\implies A_1=-\frac43m$$

In the same way, we derive $g_1=4(1-2m)/3$, and $r_2-g_2=2A_1(m-1)/3=8m(1-m)/9$.