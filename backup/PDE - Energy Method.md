# Preparation
Consider a heat equation 

$$
\begin{align}
\begin{cases}
&u_t-Du_{xx}=0,\quad in\ [0, L] \times [0, \infty] \\
&u(0, x)=g(x),\quad for\ x\in [0, L] \tag{1} \\
&u(0, t)=u(L, t),\quad for\ t>0
\end{cases}
\end{align}
$$

By multiplying the first equation by u, we get

$$
uu_t-Duu_{xx}=0 
$$

Then we integrate both sides in $[0, L]$, we get

$$\int_{o}^{L} uu_tdx - D \int_{0}^{L}uu_{xx}dx = 0$$

Now we focus on $\int_{o}^{L}uu_tdx$, we obtain

$$
\int_{o}^{L}uu_tdx = \frac{1}{2}\int_{0}^{L}\frac{d}{dt}(u^2)dx = \frac{d}{dt}(\frac{1}{2}\int_{0}^{L}u^2dx).
$$

Then we focus on $\int_{0}^{L}uu_{xx}dx$, we have
```math
\int_{0}^{L}uu_{xx}dx = uu_{x}|_{0}^{L} - \int_{0}^{L}u_{x}^{2}dx = -\int_{o}^{L} u_{x}^{2}dx
```

where we used boundary condition. Therefore we have

$$
\frac{d}{dt}(\frac{1}{2}\int_{0}^{L}u^2dx) = -D\int_{0}^{L}u_{x}^{2}dx \leq 0.
$$

We call $\varepsilon(t):=\frac{1}{2}\int_{0}^{L}u^2dx$ is the *energy of the system*, and we know 

$$
\frac{d}{dt} \varepsilon(t) = -D\int_{0}^{L}u_{x}^{2}dx \leq 0,
$$

which means the energy function is non-increasing in time.

# Proof of Uniqueness
We want to prove this heat equation have uniqueness solution. For it, we condsider $u, v$ is two solutions of $(1)$, then $w:=w-v$. By using the linearity of heat equation, we know $w$ satisfy: 

$$
\begin{align}
\begin{cases}
&w_t-Dw_{xx}=0,\ in\ [0, L] \times [0, \infty] \\
&w(0, x)=0, \ for\ x\in [0, L] \\
&w(0, t)=0, \ for\ t>0
\end{cases}
\end{align}
$$

> Recall (Heat Equation):
```math
\begin{align}
\begin{cases}
&u_t-Du_{xx}=0,\ in\ [0, L] \times [0, \infty] \\
&u(0, x)=g(x), \ for\ x\in [0, L]  \\
&u(0, t)=u(L, t), \ for\ t>0
\end{cases}
\end{align}
```

So we have 

$$
\frac{d}{dt} \varepsilon(t) = \frac{d}{dt}(\frac{1}{2}\int_{o}^{L}w(x, t)^2dx) \leq 0,
$$

and 

$$
\int_{o}^{L}w^2(x, 0)dx = 0,
$$

since the initial codition is the null function. 

Clearly, 

$$
\int_{o}^{L}w^2(x, t)dx \geq 0 \quad for \ t \geq 0,
$$

since $w^2$ is non-negative. Therefore we have

$$
\int_{o}^{L}w^2(x, t)dx = 0 \quad for \ t \geq 0,
$$

which means $w^2(x, t)=0 \Rightarrow w(x,t)=0$. 
> Recall: $\int_{o}^{L}w^2(x, 0)dx = 0$; $\frac{d}{dt} \varepsilon(t) = \frac{d}{dt}(\frac{1}{2}\int_{o}^{L}w(x, t)^2dx) \leq 0$

Thus $(1)$ admit a unique solution. 