The hyperelastic, incompressible model can be summarized as
$$
\begin{align}
\nabla \cdot \mathbf{P} & =0,\qquad & \mathbf{X}\in\Omega, \\
\mathbf{u} & =\mathbf{u}_{D}, & \mathbf{X}\in \partial\Omega_{D}, \\
\mathbf{P}\mathbf{N} & =\mathbf{T}, & \mathbf{X}\in \partial\Omega_{N}, \\
\mathbf{P} & =\mathbf{P}_{p}+\mathbf{P}_{a} \\
\mathbf{P}_{p} & =\frac{ \partial \Psi_{p}(\mathbf{F}) }{ \partial \mathbf{F} }+Jp\mathbf{F}^{-T}, \\
\mathbf{P}_{a} & =\frac{ \partial \Psi_{a}(\mathbf{F}) }{ \partial \mathbf{F} },
\end{align}
$$
where the active and passive strain-energy functions are defined as
$$
\begin{align}
\Psi_{a}(I_{4\mathbf{f}_{0}}) & =\frac{JT_{a}}{2} (I_{4\mathbf{f}_{0}}-1), \\
\Psi_{p}(I_{1},I_{4\mathbf{f}_{0}}) & = \frac{a}{2b}\bigg(e^{ b(I_{1}-3) }-1\bigg)  + \frac{a_{f}}{2b_{f}}\bigg(e^{ b_{f}(I_{4\mathbf{f}_{0}}-1)^2_{+}}-1\bigg).
\end{align}
$$
$$
\begin{align}
I_{1} & =  \mathrm{Tr}\mathbf{C} \\
I_{4\mathbf{f}_{0}} & =\mathbf{f}_{0}\cdot(\mathbf{C}\mathbf{f}_{0}), \\
I_{4\mathbf{P}_{0}} & =\mathbf{P}_{0}\cdot(\mathbf{C}\mathbf{P}_{0}), \\
I_{4\mathbf{n}_{0}} & =\mathbf{n}_{0}\cdot(\mathbf{C}\mathbf{n}_{0}), \\ 
I_{8\mathbf{f}_{0}\mathbf{P}_{0}} & =\mathbf{P}_{0}\cdot(\mathbf{C}\mathbf{f}_{0}).
\end{align}
$$

---
We assume that the fibre direction is $\mathbf{f}_{0}=\begin{bmatrix}1&0&0\end{bmatrix}^T$ in the slab, and that there is a uniform electrical activation across the slab. Since the slab is transversely isotropic and incompressible, this leads to a diagonal deformation matrix of the form
$$
\begin{equation}
\mathbf{F}=\begin{bmatrix}
\lambda & 0 & 0 \\
0 & \frac{1}{\lambda} & 0 \\
0 & 0 & \frac{1}{\lambda} 
\end{bmatrix},
\end{equation}
$$
and the right Cauchy-Green deformation tensor becomes
$$
\begin{equation}
\mathbf{C}=\begin{bmatrix}
\lambda^2 & 0 & 0 \\
0 & \frac{1}{\lambda^2} & 0 \\
0 & 0 & \frac{1}{\lambda^2} 
\end{bmatrix}.
\end{equation}
$$
Then, the invariants simplify to
$$
\begin{align}
I_{1} & =\mathrm{Tr}\mathbf{C}=\lambda^2+\frac{2}{\lambda ^2}, \\
I_{4\mathbf{f}_{0}} & =\mathbf{f}_{0}\cdot(\mathbf{C}\mathbf{f}_{0})=\lambda^2.
\end{align}
$$

Substitution into the passive and active strain-energy functions gives
$$
\begin{align}
\Psi_{a}(I_{4\mathbf{f}_{0}}) & =\frac{JT_{a}}{2} (\lambda^2-1), \\
\Psi_{p}(I_{1},I_{4\mathbf{f}_{0}}) & = \frac{a}{2b}\bigg(e^{ b(\lambda^2 +\frac{2}{\lambda^2}-3) }-1\bigg)  + \frac{a_{f}}{2b_{f}}\bigg(e^{ b_{f}(\lambda^2-1)^2_{+}}-1\bigg).
\end{align}
$$
The active first Piola-Kirchoff stress components are (could have used chain rule instead of $\gamma=\frac{1}{\lambda}$)
$$
\begin{align}
(\mathbf{P}_{a})_{11} & = \frac{ \partial \Psi_{a} }{ \partial \lambda } =JT_{a}\lambda, \\
(\mathbf{P}_{a})_{22}=(\mathbf{P}_{a})_{33} & = \frac{ \partial \Psi_{a} }{ \partial \left( \frac{1}{\lambda} \right) }  \\
 & = \frac{ \partial  }{ \partial \gamma } \left( \frac{JT_{a}}{2}\left( \frac{1}{\gamma^2}-1 \right) \right)  \\
 & =-JT_{a}\gamma^{-3} \\
 & =-JT_{a}\lambda^3,
\end{align}
$$
while the off-diagonal components are zero. The passive stress components are
$$
\begin{align}
(\mathbf{P}_{p})_{11} & =\frac{ \partial \Psi_{p} }{ \partial \lambda } +Jp(\mathbf{F}^{-T})_{11} \\
 & = \frac{a}{2}(2\lambda -4\lambda^{-3})e^{ b\left( \lambda^2 +\frac{2}{\lambda^2}-3 \right) }+ a_{f}(\lambda^2-1)_{+}2\lambda e^{ b_{f}(\lambda^2-1)^2_{+} }+\frac{Jp}{\lambda} \\
  & =a(\lambda-2\lambda^{-3})e^{ b(\lambda^2+2\lambda^{-2}-3) }+2\lambda a_{f}(\lambda^2-1)_{+}e^{ b_{f}(\lambda^2-1)_{+}^2 }+Jp\lambda^{-1},\\
(\mathbf{P}_{p})_{22}=(\mathbf{P}_{p})_{33} & =\frac{ \partial \Psi_{p} }{ \partial \left( \frac{1}{\lambda} \right) }  \\
 & =\frac{ \partial  }{ \partial \gamma } \left[ \frac{a}{2b}\bigg(e^{ b(\gamma^{-2} +2\gamma^2-3) }-1\bigg)  + \frac{a_{f}}{2b_{f}}\bigg(e^{ b_{f}(\gamma^{-2}-1)^2_{+}}-1\bigg) \right]  \\
 & =\frac{a}{2}(-2\gamma^{-3}+4\gamma)e^{ b(\gamma^{-2} +2\gamma^2-3) }+a_{f}(\gamma^{-2}-1)_{+}(-2\gamma^{-3})e^{ b_{f}(\gamma^{-2}-1)^2_{+}} \\
 & =a(-\lambda^3+4\lambda^{-1})e^{ b(\lambda^2+2\lambda^{-2}-3) }-2a_{f}\lambda^3(\lambda^2-1)_{+}e^{ b_{f}(\lambda^2-1)^2_{+} }.
\end{align}
$$

Summing up the stresses gives the total stress components,
$$
\begin{align}
\mathbf{P}_{11} & =(\mathbf{P}_{p})_{11}+(\mathbf{P}_{a})_{11} \\
 & =a(\lambda-2\lambda^{-3})e^{ b(\lambda^2+2\lambda^{-2}-3) }+2\lambda a_{f}(\lambda^2-1)_{+}e^{ b_{f}(\lambda^2-1)_{+}^2 }+Jp\lambda^{-1}+JT_{a}\lambda, \\
\mathbf{P}_{33}=\mathbf{P}_{22} & =(\mathbf{P}_{p})_{22}+(\mathbf{P}_{a})_{22} \\
 & =a(-\lambda^3+4\lambda^{-1})e^{ b(\lambda^2+2\lambda^{-2}-3) }-2a_{f}\lambda^3(\lambda^2-1)_{+}e^{ b_{f}(\lambda^2-1)^2_{+} }-JT_{a}\lambda^3.
\end{align}
$$
We assume that the slab is unloaded, and we ignore body and inertia forces, such that the active and passive stresses must balance at all points:
$$
\begin{equation}
\mathbf{P}=\mathbf{P}_{p}+\mathbf{P}_{a}=0.
\end{equation}
$$
Substitution of the components gives
$$
\begin{align}
\mathbf{P}_{11} & =
\end{align}
$$
