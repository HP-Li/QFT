# Dirac Field

## Lorentz Invariance in Wave Equations
$$
(\mathcal{J}^{\mu\nu})_{\alpha\beta}=i(\delta^\mu_\alpha\delta^\nu_\beta-\delta^\mu_\beta\delta^\nu_\alpha)
$$

$$
V^\alpha\to(\delta^\alpha_\beta-\frac{i}{2}\omega_{\mu\nu}(\mathcal{J}^{\mu\nu})^\alpha_\beta)V^\beta
$$

For example, consider the case $\omega_{12}=-\omega_{21}=\theta$, with all other components of $\omega$ equal to zero.
$$
V^\alpha\to(\delta^{\alpha}_{\beta}-\frac{i}{2}\omega_{\mu\nu}i(\delta^{\mu}_{\alpha'}\delta^{\nu}_{\beta}-\delta^{\mu}_{\beta}\delta^{\nu}_{\alpha'})g^{\alpha\alpha'})V^{\beta}
$$

$$
\begin{aligned}
V^\alpha\to&(\delta^{\alpha}_{\beta}-\frac{i}{2}\omega_{12}i(\delta^{1}_{\alpha'}\delta^{2}_{\beta}-\delta^{1}_{\beta}\delta^{2}_{\alpha'})g^{\alpha\alpha'}-\frac{i}{2}\omega_{21}i(\delta^{2}_{\alpha'}\delta^{1\beta}-\delta^{2\beta}\delta^{1}_{\alpha'})g^{\alpha\alpha'})V^{\beta}\\
&=(\delta^{\alpha}_{\beta}+\frac{1}{2}\theta(\delta^{1}_{\alpha'}\delta^{2}_{\beta}-\delta^{1}_{\beta}\delta^{2}_{\alpha'})g^{\alpha\alpha'}-\frac{1}{2}\theta(\delta^{2}_{\alpha'}\delta^{1}_{\beta}-\delta^{2}_{\beta}\delta^{1}_{\alpha'})g^{\alpha\alpha'})V^{\beta}\\
&=(\delta^{\alpha}_{\beta}+\theta\delta^{1}_{\alpha'}\delta^{2}_{\beta}g^{\alpha\alpha'}-\theta\delta^{1}_{\beta}\delta^{2}_{\alpha'}g^{\alpha\alpha'})V^{\beta}
\end{aligned}
$$

so
$$
V\to
\begin{pmatrix}
1&0&0&0\\
0&1&-\theta&0\\
0&\theta&1&0\\
0&0&0&1
\end{pmatrix}V
$$
which is just an infinitesimal rotation in the $xy$-plane. verify that setting $\omega_{01}=-\omega_{10}=\beta$
$$
\begin{aligned}
V^\alpha\to&(\delta^\alpha_\beta-\frac{i}{2}\omega_{01}i(\delta^{0}_{\alpha'}\delta^1_\beta-\delta^0_\beta\delta^{1}_{\alpha'})g^{\alpha\alpha'}-\frac{i}{2}\omega_{10}i(\delta^{1}_{\alpha'}\delta^0_\beta-\delta^1_\beta\delta^{0}_{\alpha'})g^{\alpha\alpha'})V^\beta\\
&=(\delta^\alpha_\beta+\frac{1}{2}\beta(\delta^{0}_{\alpha'}\delta^1_\beta-\delta^0_\beta\delta^{1}_{\alpha'})g^{\alpha\alpha'}-\frac{1}{2}\beta(\delta^{1}_{\alpha'}\delta^0_\beta-\delta^1_\beta\delta^{0}_{\alpha'})g^{\alpha\alpha'})V^\beta\\
&=(\delta^\alpha_\beta+\beta\delta^{0}_{\alpha'}\delta^1_\beta g^{\alpha\alpha'}-\beta\delta^0_\beta\delta^{1}_{\alpha'} g^{\alpha\alpha'})V^\beta
\end{aligned}
$$
so
$$
V\to
\begin{pmatrix}
1&\beta&0&0\\
\beta&1&0&0\\
0&0&1&0\\
0&0&0&1
\end{pmatrix}V
$$
an infinitesimal boost in the $x$-direction. The other components of $\omega$ generate the remaining boosts and rotations in a similar manner.

[^note]:I forget the $g$ when I first calculate it. Don’t forget it!

## The Dirac Equation

$$
\{\gamma^\mu,\gamma^\nu\}\equiv\gamma^\mu\gamma^\nu+\gamma^\nu\gamma^\mu=2g^{\mu\nu}\times1_{n\times n}
$$
we could write down an $n$-dimensional representation of the Lorentz algebra.
$$
S^{\mu\nu}=\frac{i}{4}[\gamma^\mu,\gamma^\nu]
$$

This computation goes through in any dimensionality, with Lorentz or Euclidean metric. In particular, it should work in three-dimensional Euclidean space, and in fact we can simply wirte
$$
\gamma^j\equiv i\sigma^j
$$
$$
so\ that\quad	\{\gamma^i,\gamma^j\}=-2\delta^{ij}
$$

The matrices representing the Lorentz algebra are then
$$
\begin{aligned}
S^{ij}=&\frac{i}{4}[\gamma^i,\gamma^j]\\
=&\frac{i}{4}[i\sigma^i,i\sigma^j]\\
=&-\frac{i}{4}[\sigma^i,\sigma^j]\\
=&-\frac{i}{4}2i\epsilon^{ijk}\sigma^k\\
=&\frac{1}{2}\epsilon^{ijk}\sigma^k
\end{aligned}
$$
Now let us find Dirac matrices $\gamma^\mu$ for four-dimensional Minkowski space.
$$
\gamma^0=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix};\quad
\gamma^i=
\begin{pmatrix}
0&\sigma^i\\
-\sigma^i&0
\end{pmatrix}
$$
This representations is called the *Weyl* or *chiral* representation.In our representation, the boost and rotation generators are

$$
\begin{aligned}
S^{0i}=&\frac{i}{4}[\gamma^0,\gamma^i]\\
=&\frac{i}{4}(\gamma^0\gamma^i-\gamma^0\gamma^i)\\
=&\frac{i}{4}
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
\begin{pmatrix}
0&\sigma^i\\
-\sigma^i&0
\end{pmatrix}-
\frac{i}{4}
\begin{pmatrix}
0&\sigma^i\\
-\sigma^i&0
\end{pmatrix}
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}\\
=&-\frac{i}{2}
\begin{pmatrix}
\sigma^i&0\\
0&-\sigma^i
\end{pmatrix}
\end{aligned}
\tag{3.26}
$$

and
$$
\begin{aligned}
S^{ij}=&\frac{i}{4}[\gamma^i,\gamma^j]\\
=&\frac{i}{4}\left(
\begin{pmatrix}
0&\sigma^i\\
-\sigma^i&0
\end{pmatrix}
\begin{pmatrix}
0&\sigma^j\\
-\sigma^j&0
\end{pmatrix}-
\begin{pmatrix}
0&\sigma^j\\
-\sigma^j&0
\end{pmatrix}
\begin{pmatrix}
0&\sigma^i\\
-\sigma^i&0
\end{pmatrix}
\right)\\
=&\frac{i}{4}\left(
\begin{pmatrix}
-\sigma^i\sigma^j&0\\
0&-\sigma^i\sigma^j
\end{pmatrix}-
\begin{pmatrix}
-\sigma^j\sigma^i&0\\
0&-\sigma^j\sigma^i
\end{pmatrix}
\right)\\
=&\frac{i}{4}
\begin{pmatrix}
-[\sigma^i,\sigma^j]&0\\
0&-[\sigma^i,\sigma^j]
\end{pmatrix}\\
=&\frac{i}{4}
\begin{pmatrix}
-2i\epsilon^{ijk}\sigma^k&0\\
0&-2i\epsilon^{ijk}\sigma^k
\end{pmatrix}\\
=&\frac{1}{2}\epsilon^{ijk}
\begin{pmatrix}
\sigma^k&0\\
0&\sigma^k
\end{pmatrix}\\
\equiv&\frac{1}{2}\epsilon^{ijk}\Sigma^k
\end{aligned}
\tag{3.27}
$$

A four-component field $\psi$ that transforms under boosts and rotations according to $(3.26)$ and $(3.27)$ is called a Dirac spinor.  The boost generators $S^{0i}$ are not Hermitian, and thus our implementation of boosts is not unitary (this was also true of the vector representation). In fact the Lorentz group, being “noncompact”, has no faithful, finite-dimensional representations that are unitary. But that does not matter to us, since $\psi$ is not a wavefunction: it is a classical field.

One possibility is simply the Klein-Gordon equation:
$$
(\partial^2+m^2)\psi=0
$$
This works because the spinor transformation matrices (3.26) and (3.27) operate only in the “internal” space; they go right through the differential operator. But it is possible to write a stronger, first-order equation, which implies Klein-Gordon equation but contains additional information. To do this we need to know one more property of the $\gamma$ matrices. With a short computation you can verify that
[^note]: this case is $\mu,\rho,\sigma$ isn't equal to zero
$$
\begin{aligned}
[\gamma^\mu,S^{\rho\sigma}]=&[\gamma^\mu,\frac{1}{2}\epsilon^{\rho\sigma}_{\quad\alpha}\Sigma^\alpha]\\
=&\frac{1}{2}\epsilon^{\rho\sigma}_{\quad\alpha}[\gamma^\mu,\Sigma^\alpha]\\
=&\frac{1}{2}\epsilon^{\rho\sigma}_{\quad\alpha}
\begin{pmatrix}
0&[\sigma^\mu,\sigma^\alpha]\\
-[\sigma^\mu,\sigma^\alpha]&0
\end{pmatrix}\\
=&i\epsilon^{\rho\sigma}_{\quad\alpha}\epsilon^{\mu\alpha}_{\quad\nu}\gamma^\nu\\
=&i\epsilon^{\alpha\rho\sigma}\epsilon^{\alpha\nu\mu}\gamma^\nu\\
=&i(\delta^{\rho}_{\ \ \nu}\delta^{\sigma\mu}-\delta^{\rho\mu}\delta^{\sigma}_{\ \ \nu})\gamma^\nu\\
=&(\mathcal{J}^{\rho\sigma})^\mu_{\ \ \nu}\gamma^\nu
\end{aligned}
$$
[^note]:if $\rho$ is zero
$$
\begin{aligned}
	[\gamma^{\mu},S^{0\sigma}]=&[\gamma^{\mu},-\frac{i}{2}
\begin{pmatrix}
	\sigma^{\sigma} & 0 \\
	0 & -\sigma^{\sigma} \\
\end{pmatrix}
]\\
=&\frac{-i}{2}
\begin{pmatrix}
	0 & \sigma^{\mu} \\
	-\sigma^{\mu} &0  \\
\end{pmatrix}
\begin{pmatrix}
	\sigma^{\sigma} & 0 \\
	0 & -\sigma^{\sigma} \\
\end{pmatrix}+\frac{i}{2}
\begin{pmatrix}
	\sigma^{\sigma} & 0 \\
	0 & -\sigma^{\sigma} \\
\end{pmatrix}
\begin{pmatrix}
	0 & \sigma^{\mu} \\
	-\sigma^{\mu} &0  \\
\end{pmatrix}\\
=&-\frac{i}{2}
\begin{pmatrix}
	0 & -\sigma^{\mu}\sigma^{\sigma} \\
	-\sigma^{\mu}\sigma^{\sigma} & 0 \\
\end{pmatrix}+\frac{i}{2}
\begin{pmatrix}
	0 & \sigma^{\sigma}\sigma^{\mu} \\
	\sigma^{\sigma}\sigma^{\mu} & 0 \\
\end{pmatrix}\\
=&\frac{i}{2}
\begin{pmatrix}
	0 & \{\sigma^{\mu},\sigma^{\sigma}\} \\
	 \{\sigma^{\mu},\sigma^{\sigma}\}& 0 \\
\end{pmatrix}\\
=&\frac{i}{2}
\begin{pmatrix}
	0 & 2\delta^{\mu\sigma} \\
	 2\delta^{\mu\sigma}& 0 \\
\end{pmatrix}\\
=&i\delta^{\mu\sigma}\gamma^{0}\\
=&(\mathcal{J}^{0\sigma})^{\mu}_{\ \ \nu}\gamma^{\nu}
\end{aligned}
$$
[^note]:if $\mu$ is zero
$$
\begin{aligned}
	[\gamma^{0},\frac{1}{2}\epsilon^{\rho\sigma\nu}\Sigma^{\nu}]=&\frac{1}{2}\epsilon^{\rho\sigma\nu}
\begin{pmatrix}
	0 & 1 \\
	1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
	\sigma^{\nu} & 0 \\
	0 & \sigma^{\nu} \\
\end{pmatrix}-\frac{1}{2}\epsilon^{\rho,\sigma,\nu}
\begin{pmatrix}
	\sigma^{\nu} & 0 \\
	0 & \sigma^{\nu} \\
\end{pmatrix}
\begin{pmatrix}
	0 & 1 \\
	1 & 0 \\
\end{pmatrix}\\
=&\frac{1}{2}\epsilon^{\rho\sigma\nu}
\begin{pmatrix}
	0 & \sigma^{\nu} \\
	\sigma^{\nu} & 0 \\
\end{pmatrix}-
\frac{1}{2}\epsilon^{\rho\sigma\nu}
\begin{pmatrix}
	0 & \sigma^{\nu} \\
	\sigma^{\nu} & 0 \\
\end{pmatrix}\\
=&0\\
=&(\mathcal{J}^{\rho\sigma})^{0}_{\ \ \nu}\gamma^{\nu}
\end{aligned}
$$
or equivalently,
$$
\begin{aligned}
	(1+\frac{i}{2}\omega_{\rho\sigma}S^{\rho\sigma})\gamma^{\mu}(1-\frac{i}{2}\omega_{\rho\sigma}S^{\rho\sigma})=&(\gamma^{\mu}+\frac{i}{2}\omega_{\rho\sigma}S^{\rho\sigma}\gamma^{\mu})(1-\frac{i}{2}\omega_{\rho\sigma}S^{\rho\sigma})\\
=&\gamma^{\mu}+\frac{i}{2}\omega_{\rho\sigma}S^{\rho\sigma}\gamma^{\mu}-\frac{i}{2}\omega_{\rho\sigma}\gamma^{\mu}S^{\rho\sigma}\\
=&\gamma^{\mu}-\frac{i}{2}\omega_{\rho\sigma}(\mathcal{J}^{\rho\sigma})^{\mu}_{\ \nu}\gamma^{\nu}\\
=&(g_{\nu}^{\mu}-\frac{i}{2}\omega_{\rho\sigma}(\mathcal{J}^{\rho\sigma})^{\mu}_{\ \nu})\gamma^{\nu}\\
=&(\delta_{\nu}^{\mu}-\frac{i}{2}\omega_{\rho\sigma}(\mathcal{J}^{\rho\sigma})^{\mu}_{\ \nu})\gamma^{\nu}
\end{aligned}
$$
This equation is just the infinitesimal from of
$$
	\Lambda^{-1}_{\frac{1}{2}}\gamma^{\mu}\Lambda_{\frac{1}{2}}=\Lambda^{\mu}_{\ \nu}\gamma^{\nu}\tag{3.29}
$$
where
$$
	\Lambda_{\frac{1}{2}}=exp(-\frac{i}{2}\omega_{\mu\nu}S^{\mu\nu})
$$
is the spinor representation of the Lorentz transformation $\Lambda$. Equation (3.29) says that the $\gamma$ matrices are invariant under simultaneous rotations of their vector and spinor indices (just like the $\sigma^{i}$ under spatial rotations). In other words, we can "take the vector index $\mu$ on $\gamma^{\mu}$ seriously," and dot $\gamma^{\mu}$ into $\partial_{\mu}$ to form a Lorentz-invariant differential operator.
We are now ready to wirte down the Dirac equation. Here it is:
$$
	(i\gamma^{\mu}\partial_{\mu}-m)\psi(x)=0\tag{3.31}
$$
To show that it is Lorentz invariant, write down the Lorentz-transformed version of the left-hand side and calculate:
$$
\begin{aligned}
	[i\gamma^{\mu}\partial_{\mu}]\psi(x)\to&[i\gamma^{\mu}(\Lambda^{-1})^{\nu}_{\ \ \mu}\partial_{\nu}-m]\Lambda_{\frac{1}{2}}\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}\Lambda_{\frac{1}{2}}^{-1}[i\gamma^{\mu}(\Lambda^{-1})^{\nu}_{\mu}\partial_{\nu}-m]\Lambda_{\frac{1}{2}}\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}[i\Lambda^{-1}_{\frac{1}{2}}\gamma^{\mu}\Lambda_{\frac{1}{2}}(\Lambda^{-1})^{\nu}_{\mu}\partial_{\nu}-m]\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}[i\Lambda^{\mu}_{\ \ \sigma}\gamma^{\sigma}(\Lambda^{-1})^{\nu}_{\ \ \mu}\partial_{\nu}-m]\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}[i\gamma^{\nu}\partial_{\nu}-m]\psi(\Lambda^{-1}x)\\
=&0
\end{aligned}
$$
To see that the Dirac equation implies the Klein-Gordon equation, act on the left with $(-i\gamma^{\mu}\partial_{\mu}-m)$:
$$
\begin{aligned}
0=&(-i\gamma^{\mu}\partial_{\mu}-m)(i\gamma^{\nu}\partial_{\nu}-m)\psi\\
=&(\gamma^{\mu}\gamma^{\nu}\partial_{\mu}\partial_{\nu}-m^2)\psi\\
=&(\frac{1}{2}\{\gamma^{\mu},\gamma^{\nu}\}\partial_{\mu}\partial_{\nu}+m^2)\psi
=(\partial^2+m^2)\psi
\end{aligned}
$$
To write down a Lagrangian for the Dirac theory, we must figure out how to multiply two Dirac spinors to form a Lorentz scalar. The obvious guess, $\psi^{\dagger}\psi$, does not work. Under a Lorentz boost this becomes $\psi^{\dagger}\Lambda^{\dagger}_{\frac{1}{2}}\Lambda_{\frac{1}{2}}\psi$; if the boost matrix were unitary, we would have $\Lambda^{\dagger}_{\frac{1}{2}}=\Lambda^{-1}_{\frac{1}{2}}$ and everything would be fine. But $\Lambda_{\frac{1}{2}}$ is not unitary, because the generators (3.26) are not Hermitian.
The solution is to define
$$
	\bar{\psi}\equiv\psi^{\dagger}\gamma^{0}
$$
Under an infinitesimal Lorentz transformation parametrized by $\omega_{\mu\nu}$, we have $\bar{\psi}\to\psi^{\dagger}(1+\frac{i}{2}\omega_{\mu\nu}(S^{\mu\nu})^{\dagger})\gamma^{0}$. The sum over $\mu$ and $\nu$ has six distinct nonzero terms. In the rotation terms, where $\mu$ and $\nu$ are both nonzero, $(S^{\mu\nu})^{\dagger}=S^{\mu\nu}$ and $S^{\mu\nu}$ commutes with $\gamma^{0}$. In the boost terms, where $\mu$ or $\nu$ is 0, $(S^{\mu\nu})^{\dagger}=-(S^{\mu\nu})$ but $S^{\mu\nu}$ anticommutes with $\gamma^{0}$. Passing the $\gamma^{0}$ to the left therefore removes the dagger from $S^{\mu\nu}$, yielding the transformation law
$$
	\bar{\psi}\to\bar{\psi}\Lambda^{-1}_{\frac{1}{2}}
$$
and therefore the quantity $\bar{\psi}\psi$ is a Lorentz scalar. Similarly you can show (with the aid of (3.29)) that $\bar{\psi}\gamma^{\mu}\psi$ is a Lorentz vector.
The correct, Lorentz-invariant Dirac Lagrangian is therefore
$$
	\mathcal{L}_{Dirac}=\bar{\psi}(i\gamma^{\mu}\partial_{\mu}-m)\psi
$$
The Euler-Lagrange equation for $\bar{\psi}$ (or $\psi^{\dagger}$) immediately yields the Dirac equation in the form (3.31); the Euler-Lagrange equation for $\psi$ gives the same equation, in Hermitian-conjugate form:
$$
	-i\partial_{\mu}\bar{\psi}\gamma^{\mu}-m\bar{\psi}=0
$$
## Weyl Spinors
From the block-diagonal from of the generators (3.26) and (3.27), it is apparent that the Dirac representation of the Lorentz group is reducible. We can form two 2-dimensional representations by considering each block separately, and writing
$$
	\psi=
\begin{pmatrix}
	\psi_{L} \\
	\psi_{R} \\
\end{pmatrix}\tag{3.36}
$$
The two-component objects $\psi_{L}$ and $\psi_{R}$ are called left-handed and right-handed *Weyl spinors*. You can easily verify that their transformation laws, under infinitesimal rotations $\theta$ and boosts $\beta$, are
$$
\begin{aligned}
	\psi_{L}\to&(1-i\theta\cdot\frac{\sigma}{2}-\beta\cdot\frac{\sigma}{2})\psi_{L};\\
\psi_{R}\to&(1-i\theta\cdot\frac{\sigma}{2}+\beta\cdot\frac{\sigma}{2})\psi_{R}.
\end{aligned}
$$
These transformation laws are connected by complex conjugation; using the identity
$$
	\sigma^2\sigma^{*}=-\sigma\sigma^2
$$
it is not hard to show that the quantity $\sigma^2\psi_{L}^{*}$ transforms like a right-handed spinor.
In terms of $\psi_{L}$ and $\psi_{R}$, the Dirac equation is
$$
	(i\gamma^{\mu}\partial_{\mu}-m)\psi=
\begin{pmatrix}
	-m & i(\partial_{0}+\sigma\cdot\nabla) \\
	i(\partial_{0}-\sigma\cdot\nabla) &-m  \\
\end{pmatrix}
\begin{pmatrix}
	\psi_{L} \\
	\psi_{R} \\
\end{pmatrix}=0
$$
The two Lorentz group representations $\psi_{L}$ and $\psi_{R}$ are mixed by the mass term in the Dirac equation. But if we set $m=0$, the equations for $\psi_{L}$ and $\psi_{R}$ decouple:
$$
\begin{aligned}
	i(\partial_{0}-\sigma\cdot\nabla)\psi_{L}=0;\\
i(\partial_{0}+\sigma\cdot\nabla)\psi_{R}=0.
\end{aligned}
$$
These are called the *Weyl equations*; they are especially important when treating neutrinos and the theory of weak interactions.
It is possible to clean up this notation slightly. Define
$$
	\sigma^{\mu}\equiv(1,\sigma),\quad\bar{\sigma}\equiv(1,-\sigma),
$$
so that
$$
	\gamma^{\mu}=
\begin{pmatrix}
	0 & \sigma^{\mu} \\
	\bar{\sigma}^{\mu} & 0 \\
\end{pmatrix}
$$
(The bar on $\bar{\sigma}$ has absolutely nothing to do with the bar on $\bar{\psi}$) Then the Dirac equation can be written
$$
\begin{pmatrix}
		-m & i\sigma\cdot\partial \\
		i\bar{\sigma}\cdot\partial & -m \\
	\end{pmatrix}
\begin{pmatrix}
	\psi_{L} \\
	\psi_{R} \\
\end{pmatrix}=0
$$

and the Weyl equations become
$$
i\bar{\sigma}\cdot\partial\psi_L=0;\quad i\sigma\cdot\partial\psi_R=0.
$$
## Free-Particle Solutions of the Dirac Equation

To get some feel for the physics of the Dirac equation, let us now discuss its plane-wave solutions. Since a Dirac field $\psi$ obeys the Klein-Gordon equation, we know immediately that it can be written as a linear combination of plane waves:
$$
\psi(x)=u(p)e^{-ip\cdot x},\quad where\quad p^2=m^2\tag{3.45}
$$

[^note]:This $p$ is four-momentum.

For the moment we will concentrate on solutions with positive frequency, that is, $p^0>0$. The column vector $u(p)$ must obey an additional constraint, found by plugging (3.45) into the Dirac equation:
$$
(\gamma^\mu p_\mu-m)u(p)=0\tag{3.46}
$$
It is easiest to analyze this equation in the rest frame, where $p=p_0=(m,0)$; the solution for general $p$ can then be found by boosting with $\Lambda_{\frac{1}{2}}$. In the rest frame, Eq.(3.46) becomes
$$
(m\gamma^0-m)u(p_0)=m
\begin{pmatrix}
-1&1\\
-&-1
\end{pmatrix}u(p_0)=0
$$
and the solutions are
$$
u(p_0)=\sqrt{m}
\begin{pmatrix}
\xi\\
\xi
\end{pmatrix},\tag{3.47}
$$
for any numerical two-component spinor $\xi$. We conventionally normalize $\xi$ so that $\xi^{\dagger}\xi=1$; the factor $\sqrt{m}$ has been inserted for future convenience. We can interpret the spinor $\xi$ by looking at the rotation generator (3.27): $\xi$ transforms under rotations as an ordinary two-component spinor of the rotation group, and therefore determines the spin orientation of the Dirac solution in the usual way. For example, when $\xi=\begin{pmatrix}1\\0\end{pmatrix}$, the particle has spin up along the 3-direction.
	Notice that after applying the Dirac equation, we are free to choose only two of the four components of $u(p)$. This is just what we want, since a spin-1/2 particle has only two physical states—spin up and spin down.(Of course we are being a bit premature in talking about particles and spin. We will prove that the spin angular momentum of a Dirac particle is $\hbar/2$ when we quantize the Dirac theory in Section 3.5; for now, just notice that there are two possible solutions $u(p)$ for any momentum p.)
	Now that we have the general form of $u(p)$ in the rest frame, we can obtain $u(p)$ in any other frame by boosting. Consider a boost along the 3-direction. First we should remind ourselves of what the boost does to the 4-momentum vector. In infinitesimal form,
$$
\begin{pmatrix}
E\\p^3
\end{pmatrix}=\left[1+\eta
\begin{pmatrix}
0&1\\1&0
\end{pmatrix}\right]
\begin{pmatrix}
m\\0
\end{pmatrix},
$$
where $\eta$ is some infinitesimal parameter. For finite $\eta$ we must write
$$
\begin{aligned}
\begin{pmatrix}
E\\p^3
\end{pmatrix}=&\exp\left[\eta
\begin{pmatrix}
0&1\\1&0
\end{pmatrix}\right]
\begin{pmatrix}
m\\0
\end{pmatrix}\\
=&\biggl[\cosh\eta
\begin{pmatrix}
1&0\\0&1
\end{pmatrix}+\sinh\eta
\begin{pmatrix}
	0&1\\
	1&0
\end{pmatrix}\biggr]
\begin{pmatrix}
	m\\0
\end{pmatrix}\\
=&\begin{pmatrix}
	m\cosh\eta\\m\sinh\eta
\end{pmatrix}
\end{aligned}
$$
The parameter $\eta$ is called the *rapidity*. It is the quantity that is additive under successsive boosts.
	Now apply the same boost to $u(p)$. According to Eqs(3.26) and (3.30),
$$
\begin{aligned}
	u(p)=&\exp\biggl[-\frac{1}{2}\eta
\begin{pmatrix}
	\sigma^{3} & 0 \\
	0 & -\sigma^{3} \\
\end{pmatrix}
\biggr]\sqrt{m}
\begin{pmatrix}
	\xi \\
	\xi \\
\end{pmatrix}\\
=&\biggl[\cosh\Bigl(\frac{1}{2}\eta\Bigr)
\begin{pmatrix}
	1&0\\0&1
\end{pmatrix}-\sinh\Bigl(\frac{1}{2}\eta\Bigr)
\begin{pmatrix}
	\sigma^{3}&0\\0&\sigma^{3}
\end{pmatrix}
\biggr]\sqrt{m}
\begin{pmatrix}
	\xi \\
	\xi \\
\end{pmatrix}\\
=&
\begin{pmatrix}
	e^{\eta/2}(\frac{1-\sigma^{3}}{2})+e^{-\eta/2}(\frac{1+\sigma^{3}}{2}) & 0 \\
	0 & e^{\eta/2}(\frac{1+\sigma^{3}}{2})+e^{-\eta/2}(\frac{1-\sigma^{3}}{2}) \\
\end{pmatrix}
\sqrt{m}
\begin{pmatrix}
	\xi \\
	\xi \\
\end{pmatrix}\\
=&
\begin{pmatrix}
	\Bigl[\sqrt{E+p^{3}}(\frac{1-\sigma^{3}}{2})+\sqrt{E-p^{3}}(\frac{1+\sigma^{3}}{2})\Bigr]\xi \\
\\
	 \Bigl[\sqrt{E+p^{3}}(\frac{1+\sigma^{3}}{2})+\sqrt{E-p^{3}}(\frac{1-\sigma^{3}}{2})\Bigr]\xi\\
\end{pmatrix}
\end{aligned}
$$
The last line can be simplified to give
$$
	u(p)=
\begin{pmatrix}
	\sqrt{p\cdot\sigma}\xi \\
	\sqrt{p\cdot\bar{\sigma}}\xi \\
\end{pmatrix}\tag{3.50}
$$
where it is understood that in taking the square root of a matrix, we take the positive root of each eigenvalue. This expression for $u(p)$ is not only more compact, but is also valid for an arbitrary direction of $p$. When working with expressions of this form, it is often useful to know the identity
$$
	(p\cdot\sigma)(p\cdot\bar{\sigma})=p^2=m^2.
$$
You can then verify directly that (3.50) is a solution of the Dirac equation in the form of (3.43).
	In practice it is often convenient to work with specific spinors $\xi$. A useful choice here would be eigenstates of $\sigma^3$. For example, if $\xi=\begin{pmatrix}1\\0\end{pmatrix}$(spin up along the 3-axis), we get
$$
	u(p)=
\begin{pmatrix}
	\sqrt{E-p^3}\begin{pmatrix}1\\0\end{pmatrix} \\
	\sqrt{E+p^3}\begin{pmatrix}1\\0\end{pmatrix} \\
\end{pmatrix}\xrightarrow[large\ boost]{}\sqrt{2E}
\begin{pmatrix}
	0 \\
	\begin{pmatrix}1\\0\end{pmatrix} \\
\end{pmatrix}\tag{3.52}
$$
while for $ \xi=\begin{pmatrix}0\\1\end{pamtarix}$(spin down along the 3-axis) we have
$$
	u(p)=
\begin{pmatrix}
	\sqrt{E+p^3}
\begin{pmatrix}
	0 \\
	1 \\
\end{pmatrix}
 \\
	\sqrt{E-p^3}
\begin{pmatrix}
	0 \\
	1 \\
\end{pmatrix}
 \\
\end{pmatrix}\xrightarrow[large\ boost]{}\sqrt{2E}
\begin{pmatrix}
\begin{pmatrix}
	0 \\
	1 \\
\end{pmatrix}
 \\
	0\\
\end{pmatrix}\tag{3.53}
$$
In the limit $\eta\rightarrow\infty$ the states degenerate into the two-component spinors of a massless particle. (We now see the reason for the factor of \sqrt{m} in (3.47): It keeps the spinor expressions finite in the massless limit.)
The solutions (3.52) and (3.53) are eigenstates of the helicity operator,
$$
	h\equiv\hat{p}\cdot S=\frac{1}{2}\hat{p}_{i}
\begin{pmatrix}
	\sigma^{i} & 0 \\
	0 & \sigma^{i} \\
\end{pmatrix}
$$
A particle with $h=+\frac{1}{2}$ is called *right-handed*, while one with $h=-\frac{1}{2}$ is called *lift-handed*. The helicity of a massive particle depends on the frame of in the opposite direction (but its spin is unchanged). For a massless particle, which travels at the speed of light, one cannot perform such a boost.
	The extremely simple form of $u(p)$ for a massless particle in a helicity eigenstate makes the behavior of such a particle easy to understand. In Chapter 1, it enabled us to guess the form of the $e^{+}e^{-}\to\mu^{+}\mu^{-}$ cross section in the massless limit. In subsequent chapters we will often do a mindless calculation first, then look at helicity eigenstates in the high-energy limit to understand what we have done.
	Incidentally, we are now ready to understand the origin of the notation $\phi_{L}$ and $\phi_{R}$ for Weyl spinors. The solutions of the Weyl equations are states of definite helicity, corresponding to left- and right-handed particles, respectively. The Lorentz invariance of helicity (for a massless particle) is manifest in the notation of Weyl spinors, since $\phi_{L}$ and $\phi_{R}$ live in different representations of the Lorentz group.
	It is covenient to write the normaliaztion condition for $u(p)$ in a Lorentz invariant way. We saw above that $\phi^{\dagger}\phi$ is not Lorentz invariant. Similary,
$$
\begin{aligned}
	u^{\dagger}u=&
\begin{pmatrix}
	\xi^{\dagger}\sqrt{p\cdot\sigma} & \xi^{\dagger}\sqrt{p\cdot\bar{\sigma}} \\
\end{pmatrix}\cdot
\begin{pmatrix}
	\sqrt{p\cdot\sigma}\xi \\
	\sqrt{p\cdot\bar{\sigma}}\xi \\
\end{pmatrix}\\
=&2E_{p}\xi^{\dagger}\xi
\end{aligned}\tag{3.55}
$$
To make a Lorentz scalar we define
$$
	\bar{u}(p)=u^{\dagger}(p)\gamma^{0}
$$
Then by an almost identical calculation,
$$
	\bar{u}u=2m\xi^{\dagger}\xi\tag{3.57}
$$
This will be our normalization condition, once we also require that the two-component spinor $\xi$ be normalized as usual: $\xi^{\dagger}\xi=1$. It is also conventional to choose basis spionrs $\xi^{1}$ and $\xi^{2}$ (such as $\begin{pmatrix}1\\0\end{pmatrix}$ and $\begin{pmatrix}0\\1\end{pmatrix}$) that are orthogonal. For a massless particle Eq.(3.57) is trivial, so we must write the normalization condition in the form of (3.55)
	Let us summarize our dicussion so far. The general solution of the Dirac equation can be wirtten as linear combination of plane waves. The positive-frequency waves are of the form
$$
	\psi(x)=u(p)e^{-ip\cdot x},\quad p^2=m^2,\quad p^{0}>0.
$$
There are two linearly independent solutions for $u(p)$,
$$
	u^{s}(p)=
\begin{pmatrix}
	\sqrt{p\cdot\sigma}\xi^{s} \\
	\sqrt{p\cdot\bar{\sigma}}\xi^{s} \\
\end{pmatrix},\quad s=1,2
$$
which we normalize according to
$$
\bar{u}^{r}(p)u^{s}(p)=2m\delta^{rs}\quad or u^{r\dagger}(p)u^{s}(p)=2E_{p}\delta^{rs}
$$
In exactly the same way, we can find the negative-frequency solutions:
$$
	\psi(x)=v(p)e^{+ip\cdot x},\quad p^2=m^2,\quad p^{0}>0
$$
(Note that we have chosen to put the + sign into the exponential, rather than having $p^{0}<0$.) There are two linearly independent solutions for $v(p)$,
$$
	v^{s}(p)=
\begin{pmatrix}
	\sqrt{p\cdot\sigma}\eta^{s} \\
	-\sqrt{p\cdot\bar{\sigma}}\eta^{s} \\
\end{pmatrix},\quad s=1,2
$$
where $\eta^{s}$ is another basis of two-component spinors. These solutions are normalized according to
$$
	\bar{v}^{r}v^{s}(p)=-2m\delta^{rs}\quad or v^{r\dagger}(p)v^{s}(p)=+2E_{p}\delta^{rs}.
$$
The u's and v's are also orthogonal to each other:
$$
	\bar{u}^{r}(p)v_{s}(p)=\bar{v}^{r}(p)u^{s}(p)=0
$$
Be careful, since $u^{r\dagger}(p)v^{s}(p)\neq0$ and $v^{r\dagger}(p)u^{s}(p)\neq0$. However, note that
$$
	u^{r\dagger}(p)v^{s}(-p)=v^{r\dagger}(-p)u^{s}(p)=0,
$$
where we have changed the sign of the 3-momentum in one factor of each spinor product.
### Spin Sums
In evaluating Feynman diagrams, we will often wish to sum over the polarizationg states of a fermion. We can derive the relevant completeness relations with a simple calculation:
$$
\begin{aligned}
\sum_{s=1,2}u^{s}(p)\bar{u}^{s}(p)=&\sum_{s}
\begin{pmatrix}
	\sqrt{p\cdot\sigma}\xi^{s} \\
	\sqrt{p\cdot\bar{\sigma}}\xi^{s} \\
\end{pmatrix}
\begin{pmatrix}
	\xi^{s\dagger}\sqrt{p\cdot\bar{\sigma}} & \xi^{s\dagger}\sqrt{p\cdot\sigma} \\
\end{pmatrix}\\
=&
\begin{pmatrix}
	\sqrt{p\cdot\sigma}\sqrt{p\cdot\bar{\sigma}} & \sqrt{p\cdot\sigma}\sqrt{p\cdot\sigma} \\
	\sqrt{p\cdot\bar{\sigma}}\sqrt{p\cdot\bar{\sigma}} & \sqrt{p\cdot\bar{\sigma}}\sqrt{p\cdot\sigma} \\
\end{pmatrix}\\
=&
\begin{pmatrix}
	m & p\cdot\sigma \\
	p\cdot\bar{\sigma} & m \\
\end{pmatrix}
\end{aligned}
$$
In the second line we have used
$$
	\sum_{s=1,2}\xi^{s}\xi^{s\dagger}=1=
\begin{pmatrix}
	1 & 0 \\
	0 & 1 \\
\end{pmatrix}.
$$
Thus we arrive at the desired formula,
$$
	\sum_{s}u^{s}(p)\bar{u}^{s}(p)=\gamma\cdot p+m.
$$
Similarly,
$$
	\sum_{s}v^{s}(p)\bar{v}^{s}(p)=\gamma\cdot p-m.
$$
The combination $\gamma\cdot p$ occurs so often that Feynman introduced the notation $\not p\equiv\gamma^{\mu}p_{\mu}$. We will use this notation frequently from now on.
## Dirac Matrices and Dirac Field Bilinears
We saw in Section 3.2 that the quantity $\bar{\psi}\psi$ is a Lorentz scalar. It is also easy to show that $\bar{\psi}\gamma\psi$ ia a 4-vector —— we used this fact in writing down the Dirac Lagrangian(3.34). Now let us ask a more general question: Consider the expression $\bar{\psi}\Gamma\psi$, where $\Gamma$ is any $4\times4$ constant matrix. Can we decompose this expression into terms that have definite transformation properties under the Lorentz group? The answer is yes, if we write $\Gamma$ in terms of the following basis of sixteen $4\times4$ matrices, defined as antisymmetric combinations of $\gamma$-matrices:
| |  |
|:---  |:---:  |
| 1 | 1 of these|
| $\gamma^{\mu}$ | 4 of these |
| $\gamma^{\mu\nu}=\frac{1}{2}[\gamma^{\mu},\gamma^{\nu}]\equiv\gamma^{[\mu}\gamma^{\nu]}\equiv-i\sigma^{\mu\nu}$ | 6 of these |
| $\gamma^{\mu\nu\rho}=\gamma^{[\mu}\gamma^{\nu}\gamma^{\rho]}$ | 4 of these |
| $\gamma^{\mu\nu\rho}\sigma=\gamma^{[\mu}\gamma^{\nu}\gamma^{\rho}\gamma^{\sigma]}$ | 1 of these |
|  | 16 total |
The Lorentz-transformation properties of these matrices are easy to determine. For example,
$$
\begin{aligned}
	\bar{\psi}\gamma^{\mu\nu}\psi\to&(\bar{\psi}\Lambda^{-1}_{\frac{1}{2}})(\frac{1}{2}[\gamma^{\mu},\gamma^{\nu}])(\Lambda_{\frac{1}{2}}\psi)\\
=&\frac{1}{2}\bar{\psi}(\Lambda^{-1}_{\frac{1}{2}}\gamma^{\mu}\Lambda_{\frac{1}{2}}\Lambda_{\frac{1}{2}}^{-1}\gamma^{\nu}\Lambda_{\frac{1}{2}}-\Lambda^{-1}_{\frac{1}{2}}\gamma^{\nu}\Lambda_{\frac{1}{2}}\Lambda_{\frac{1}{2}}^{-1}\gamma^{\mu}\Lambda_{\frac{1}{2}})\psi\\
=&\Lambda^{\mu}_{\ \alpha}\Lambda^{\nu}_{\ \beta}\bar{\psi}\gamma^{\alpha\beta}\psi
\end{aligned}
$$
Each set of matrices transforms as an antisymmetric tensor of successively higher rank.
The last two sets of matrices can be simplified by introducing an additional gamma matrix,
$$
	\gamma^{5}\equiv i\gamma^{0}\gamma^{1}\gamma^{2}\gamma^{3}=-\frac{i}{4!}\epsilon^{\mu\nu\rho\sigma}\gamma_{\mu}\gamma_{\nu}\gamma_{\rho}\gamma_{\sigma}\tag{3.68}
$$
Then $\gamma^{\mu\nu\rho\sigma}=-i\epsilon^{\mu\nu\rho\sigma}\gamma^{5}$ and $\gamma^{a\mu\nu\rho}=+i\epsilon^{a\mu\nu\rho\sigma}\gamma_{\sigma}\gamma^{5}$. The matrix $\gamma^{5}$ has the following properties, all of which can be verified using (3.68) and the anti-commutation relations (3.22)

