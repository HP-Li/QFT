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
\end{aligned}\tag{3.29}
$$
This equation is just the infinitesimal from of
$$
	\Lambda^{-1}_{\frac{1}{2}}\gamma^{\mu}\Lambda_{\frac{1}{2}}=\Lambda^{\mu}_{\ \nu}\gamma^{\nu}
$$
where
$$
	\Lambda_{\frac{1}{2}}=exp(-\frac{i}{2}\omega_{\mu\nu}S^{\mu\nu})
$$
is the spinor representation of the Lorentz transformation $\Lambda$. Equation (3.29) says that the $\gamma$ matrices are invariant under simultaneous rotations of their vector and spinor indices (just like the $\sigma^{i}$ under spatial rotations). In other words, we can "take the vector index $\mu$ on $\gamma^{\mu}$ seriously," and dot $\gamma^{\mu}$ into $\partial_{\mu}$ to form a Lorentz-invariant differential operator.
We are now ready to wirte down the Dirac equation. Here it is:
$$
	(i\gamma^{\mu}\partial_{\mu}-m)\psi(x)=0
$$
To show that it is Lorentz invariant, write down the Lorentz-transformed version of the left-hand side and calculate:
$$
\begin{aligned}
	[i\gamma^{\mu}\partial_{\mu}]\psi(x)\to&[i\gamma^{\mu}(\Lambda^{-1})^{\nu}_{\ \ \mu}\partial_{\nu}-m]\Lambda_{\frac{1}{2}}\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}\Lambda_{\frac{1}{2}}^{-1}[i\gamma^{\mu}(\Lambda^{-1})^{\nu}_{\mu}\partial_{\nu}-m]\Lambda_{\frac{1}{2}}\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}[i\Lambda^{-1}_{\frac{1}{2}}\gamma^{\mu}\Lambda_{\frac{1}{2}}(\Lambda^{-1})^{\nu}_{\mu}\partial_{\nu}-m]\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}[i\Lambda^{\mu}_{\ \ \sigma}\gamma^{\sigma}(\Lambda^{-1})^{\nu}_{\ \ \mu}\partial_{\nu}-m]\psi(\Lambda^{-1}x)\\
=&\Lambda_{\frac{1}{2}}[i\gamma^{\nu}\partial_{\nu}-m]\psi(\Lambda^{-1}x)\\
=0n
\end{aligned}
$$
To see that the Dirac equation implies the Klein-Gordon equation, act on the left with $(-i\gamma^{\mu}\partial_{\mu}-m)$:
$$
\begin{aligned}
	0=&(-i\gamma^{\mu}\partial_{\mu}-m)(i\gamma^{\nu}\partial_{\nu}-m)\psi\\
=&(\gamma^{\mu}\gamma^{\nu}\partial_{\mu}\partial_{\nu}_m^2)\psi\\
=&(\frac{1}{2}\{\gamma^{\mu},\gamma^{\nu}\}\partial_{\mu}\partial_{\nu}+m^2)\psi
=(\partial^2+m^2)\psi
\end{aligned}
$$
To write down a Lagrangian for the Dirac theory, we must figure out how to multiply two Dirac spinors to form a Lorentz scalar. The obvious guess, $\psi^{\dagger}\psi$, does not work. Under a Lorentz boost this becomes $\psi^{\dagger}\Lambda^{\dagger}_{\frac{1}{2}}\Lambda_{\frac{1}{2}}\psi$; if the boost matrix were unitary, we would have $\Lambda^{\dagger}_{\frac{1}{2}}=\Lambda^{-1}_{\frac{1}{2}}$ and everything would be fine. But $\Lambda_{\frac{1}{2}}$ is not unitary, because the generators (3.26) are not Hermitian.
The solution is to define
$$
	\bar{\psi}\equiv\psi^{\dagger}\gamma^{0}
$$
Under an infinitesimal Lorentz transformation parametrized by $\omega_{\mu\nu}$, we have $\bar{\psi}\to\psi^{\dagger}(1+\frac{i}{2}\omega_{\mu\nu}(S^{\mu\nu})^{\dagger})\gamma^{0}$. The sum over $\mu$ and $\nu$ has six distinct nonzero terms. In the rotation terms, where $\mu$ and $\nu$ are both nonzero, $(S^{\mu\nu})^{\dagger}=S^{\mu\nu}$ and $S^{\mu\nu}$ commutes with $\gamma^{0}$. In the boost terms, where $\mu$ or $\nu$ is 0,
