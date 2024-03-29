By Alexander Hatle
![[Pasted image 20231001160039.png|800]]
Let's use the derivative estimate
$$\begin{align*}
\lvert D^{\alpha }u(x) \rvert &\le \frac{C_{k}}{r^{d+\lvert \alpha  \rvert}} \lVert u \rVert_{L^{1}(B_{x,r})}\\
&\le \frac{C_{k}}{r^{d+\lvert \alpha \rvert } }\int_{B_{x,r}} C(1+\lvert y \rvert^{2})^{\frac{q}{2}} \text{ d}y\\
	&\le  \frac{C'}{r^{d+\lvert \alpha \rvert }} r^{d}(1+r^{2})^\frac{q}{2}\\
&\le C' \cdot r^{q-\lvert \alpha  \rvert }+\text{lower order terms}.
\end{align*}$$
Suppose that $\lvert \alpha  \rvert=\lfloor q \rfloor+1$. Then we have that $\lvert D^{\alpha }u(x) \rvert \le C'r^{q-\lfloor q \rfloor -1}\to0$ as $r\to \infty$. 

Since this is zero, it implies that $u$ must be a polynomial of degree at most $\lfloor q \rfloor$. 

![[Pasted image 20231001160132.png|800]]
As the hint suggests,
$$\begin{align*}
\frac{\text{d}^{2}}{\text{d}^{2}x} \left(\frac{1}{2}\lvert x\rvert\right) &= \frac{\text{d}}{\text{d}x}\begin{cases}
\frac{1}{2}  &  \quad\text{for }x>0 \\
- \frac{1}{2}  &  \quad\text{for }x<0
\end{cases}\\
&= \delta _{0}(x)
\end{align*}$$
Any fundamental solution $\tilde E$ has the property that $\frac{\text{d}^{2}}{\text{d}^{2}x}(\tilde E-E)=0$.

Then, a general fundamental solution, $\tilde E$, for $P$ is given by
$$\begin{align*}
\tilde E&= E+c_{1}x+c_{0}\\
	\tilde E&= \frac{1}{2}\lvert x \rvert+c_{1}x+c_{0},
\end{align*}$$
for $c_{0},c_{1}\in \mathbb{R}$.
![[Pasted image 20231001160212.png|800]]
$$\begin{align*}
u(x)&= u*\delta _{0}(x)\\
&= \mathbb 1_{(0,1)}u*E''(x)\\
&= (\delta _{0}-\delta _{1})u*E'(x)+\mathbb 1_{(0,1)}u'*E'(x)\\
&= (\delta _{0}-\delta _{1})u*E'(x)+(\delta _{0}-\delta _{1})u'*E(x)+\mathbb 1_{(0,1)}u''*E(x)
\end{align*}$$
The first term is 
$$\begin{align*}
\int_\mathbb{R}((\delta _{0}-\delta _{1})u)(y)E'(x-y)\text{ d}y&=  \int_\mathbb{R} (\delta _{0}u)(y)E'(x-y)-(\delta _{1}u)(y)E'(x-y) \text{ d}y\\
&= u(0)E'(x)-u(1)E'(x-1).
\end{align*}$$
The second term is similar,
$$\int_\mathbb{R} ((\delta _{0}-\delta _{1})u')(y)E(x-y)\text{ d}y=u'(0)E(x)-u'(1)E(x-1).$$
Finally, the third term is
$$\int_\mathbb{R} (\mathbb 1_{(0,1)}u'')(y)E(x-y)\text{ d}y=\int_{0}^{1}u''(y)E(x-y)\text{ d}y$$
Our representation formula for $u$ is
$$u(x)=u(0)E'(x)-u(1)E'(x-1)+u'(0)E(x)-u'(1)E(x-1)+\int_{0}^{1}u''(y)E(x-y)\text{ d}y.$$

![[Pasted image 20231001160224.png|800]]
(Feel free to skip, couldn't crack this one)
Since $E= \frac{1}{2}\lvert x \rvert+c_{1}x+c_{0},$ 
$E'(x)= \frac{1}{2}\text{sgn}x+c_{1}$.
Picking $c_{1}=\frac{1}{2}$ yields that $E(x-1)=- \frac{1}{2}+ \frac{1}{2}=0$ for $x \in (0,1)$, and the $u'(1)$ term vanishes.
$E(x-1)= \frac{1}{2}\lvert x-1 \rvert+ \frac{1}{2}x+c_{0}= \frac{1}{2}(1-x)+ \frac{1}{2}x+c_{0}$.  For this term to be 0, we need to pick $c_{0}=-1$.
$$E(x)=\frac{1}{2}\lvert x \rvert+ \frac{1}{2}x-1$$
$$\begin{align*}
u(x)&= u(0)E'(x)+u(0)E(x)+\int_{0}^{1}u''(y) \left(\frac{1}{2}\lvert x-y \rvert+ \frac{1}{2}(x-y)-1 \right)\text{ d}y\\
&= u(0)E'(x)+u'(0)E(x)+\int_{0}^{x}u''(y) \left[x-y-1 \right] \text{ d}y+\int_{x}^{1}-u''(y)\text{ d}y\\
&= u(0)E'(x)+u'(0)E(x)+\int_{0}^{x}u''(y)(x-y)\text{ d}y-\int_{0}^{1}u''(y) \text{ d}y
\end{align*}$$
$$\begin{align*}
&\quad \int_{0}^{1}u''(y)\left(\frac{1}{2}\lvert x-y \rvert +c_{1}(x-y)+c_{0} \right)\text{ d}y\\
&= c_{0}(u'(1)-u'(0))+\int_{0}^{1}u''(y) \left(\frac{1}{2}\lvert x-y \rvert+c_{1}(x-y) \right)\text{ d}y\\
&= c_{0}(u'(1)-u'(0))+\int_{0}^{x}u''(y) \left(\frac{1}{2}+c_{1} \right)(x-y) \text{ d}y+\int_{x}^{1}u''(y)\left(- \frac{1}{2}+c_{1} \right)(x-y)\text{ d}y
\end{align*}$$

![[Pasted image 20231001160239.png|800]]
Lemma 4.9:
Let $\tilde E_{0}$ be a fundamental solution for $-\Delta$ at 0. Then 
$$\begin{align*}
v(x)&= \int_{B_{r}(x)}\tilde E_{0}(x-y)(-\Delta v)(y)\text{ d}y-\int_{\partial B_{r}(x)}\nu (y) \cdot D_{y} \tilde E_{0}(x-y)v(y) \text{ d}S(y)\\
&+\int_{\partial B_{r}(x)}\tilde E_{0}(x-y)\nu (y) \cdot Dv(y) \text{ d}S(y)
\end{align*}$$
We can decide that $\tilde E_{0}(y)=E_{0}(\lvert y \rvert)-E_{0}(r)$, meaning that $\tilde E_{0}$ vanishes on the sphere $\partial B_{r}(x)$, and that the third term will vanish. The difference between this proof and the proof for mean-value property is that the first term,
$$\int_{B_{r}(x)} (E_{0}(\lvert x-y \rvert) -E_{0}(r))(-\Delta v)(y) \text{ d}y,$$
does not vanish.
The fundamental solution is
![[Pasted image 20231005214154.png]]
Since $\lvert x-y \rvert \le r$, we have that in the $d=2$ case
$$- \frac{1}{2\pi }\text{log} \lvert x-y \rvert \ge - \frac{1}{2\pi }\text{log}r,$$
and that in the $d \ge 3$ case
$$ \frac{1}{d(d-2)\alpha (d)} \frac{1}{\lvert x-y \rvert^{d-2}}\ge \frac{1}{d(d-2)\alpha (d)}\frac{1}{r^{d-2}}.$$
Thus $E_{0}(\lvert x-y \rvert)\ge E_{0}(r)$, and $E_{0}(\lvert x-y \rvert)-E_{0}(r)$ is positive. This, in combination with that $-\Delta v \le 0$, makes the the first integral negative. Then,
$$\begin{align*}
v(x) &\le -\int_{\partial B_{r}(x)}\nu (y) \cdot D_{y} \tilde E_{0}(x-y)v(y) \text{ d}S(y)\\
		&\le -\int_{\partial B_{r}(x)}\frac{y-x}{r} \cdot \left(-\frac{x-y}{r}E'_{0}(r) \right)v(y) \text{ d}S(y)\\
&\le \int_{\partial B_{r}(x)}-E_{0}'(r)v(y) \text{ d}S(y)
\end{align*}$$
Since $E'_{0}(r)= -\frac{1}{\lvert \partial B_{r}(x) \rvert}$, we have
$$v(x) \le \frac{1}{\lvert \partial B_{r}(x) \rvert}\int_{\partial B_{r}(x)}v(y)\text{ d}S(y).$$
Using this inequality,
$$\int_{B_{r}(x)}v(y) \text{ d}y=\int_{0}^{r}\int_{\partial B_{r'}(x)} v(y) \text{ d}S(y) \text{ d}r'\ge v(x)\int_{0}^{r}\int_{\partial B_{r'}(x)} \text{ d}S(y),$$
and our final result is
$$v(x) \le \frac{1}{\lvert B_{r}(x) \rvert}\int_{B_{r}(x)}v(y) \text{ d}y.$$
Which holds for all $\overline{B_{r}(x)} \subseteq U$. 
![[Pasted image 20231001160346.png|800]]
This proof is very similar to the one in the lecture notes, the only difference is replacing the equality in the mean-value property with the inequality we just proved. 

Let's assume that $v \in C^{2}(U) \cap C(\overline{U})$. Suppose that $v$ attains a maximum at a point $x_{0}\in U$, i.e. $v(x_{0})=\max_{\overline{U}}v$. 
Then,
$$V=\{x \in U:v(x)=\max_{\overline{U}}v \}$$
is nonempty closed subset of $U$. 

Now we want to show that $V$ is open as well. Using the inequality we proved in the last problem, and for any $x_{0}\in V$ (i.e. $v(x_{0})=\max_{\overline{U}}v$), we have
$$\begin{align*}
v(x_{0}) &\le \frac{1}{\lvert B_{r}(x_{0}) \rvert} \int_{B_{r}(x)}v(y) \text{ d}y\\
0 &\le \frac{1}{\lvert  B_{r}(x_{0}) \rvert} \int_{B_{r}(x)}(v-\max_{\overline{U}}v) \text{ d}y.
\end{align*}$$
Clearly, $v-\max_{\overline{U}}v\le 0$. As the integral must be nonnegative, it follows that $v=\max_{\overline{U}}v$ in $B_{r}(x)$, meaning that $B_{r}(x)\subseteq V$. Then $V$ is both open and closed subset of $U$, and since it is also nonempty, it must be the whole space, $V=U$. Thus we have the **strong maximum principle**
If $x_{0} \in U$ satisfies
$$v(x_{0})=\max_{\overline{U}}v,$$
then $v$ must be constant in $U$.

From this, we want to show the **weak maximum principle**
$$\max_{\overline{U}}v=\max_{\partial U}v.$$
If we first assume that there exists some $x_{0} \in U$ such that $v(x_{0})=\max_{\overline{U}}v$, then $v$ must be constant in $U$, and since $v \in C(\overline{U})$, it must be constant in $\overline{U}$ and the weak principle holds.

If there does not exists some $x_{0}\in U$ such that $v(x_{0})=\max_{\overline{U}}v$, the weak maximum principle holds trivially.


![[Pasted image 20231001160423.png|800]]
Suppose that there exists some $x^{*} \in U$ such that 
$$\max_{x \in \overline{U}} (v(x)-h(x))=v(x^{*})-h(x^{*})$$
Then for small $r$,
$$v(x^{*})-h(x^{*})\le \frac{1}{\lvert B_{r}(x^{*}) \rvert}\int_{B_{r}(x^{*})}v(y)-h(y) \text{ d}y$$
Since $v(x^{*})-h(x^{*})$ is maximal, $v(x^{*})-h(x^{*})\ge v(y)-h(y)$. 

The only way that the inequality holds is if $v(x^{*})-h(x^{*})=v(y)-h(y)\quad\text{for }y \in B_{r}(x^{*})$.

It follows (for example by setting each $y \in B_{r}(x^{*})$ to be the new $x^{*}$ and repeat the same argument) that if there exists some $x^{*}\in U$ that attains the maximum, then each $y \in \overline{U}$ attains that maximum. 

Now assume that that maximum is positive, $v(x^{*})-h(x^{*})>0$ for some $x^{*}\in U$. 
This is a contradiction since the same maximum must be achieved on the boundary, but there $v=h$. 
Therefore,
$$\max_{x \in \overline{U}}v(x)-h(x)\le0\quad\implies\quad v(x)\le h(x) \quad\text{in }U$$