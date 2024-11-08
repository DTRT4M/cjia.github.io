# The prior and posterior distributions
In the absence of strong prior information about $V$ and $\sigma^2$, we suggest use of

$$\pi(V,\sigma^2)=(V+\sigma^2)^{-2}.$$

The motivation for this choice follows from writing

$$\pi(V,\sigma^2)=\pi(V\mid\sigma^2)\pi(\sigma^2)\equiv\frac1{\sigma^2}\left(1+\frac V{\sigma^2}\right)^{-2}\frac1{\sigma^2}.$$

# The prior on p
An obvious objective choice of this prior is $\pi(p)=1.$ Typically, however, one does have strong prior information about $p$ and, often, this information is that $p$ is large (i.e., that most of the $\mu_i$ are zero). A convenient functional form that represents this type of information is

$$\pi(p)=(\alpha+1)p^\alpha$$

where $\alpha$ is an adjustable parameter allowing one to control how much of $\pi(p)’$s mass is concentrated near 1. Note the case of $\alpha=0$, which defaults back to the uniform prior.

One simple way to specify $\alpha$ would be to make a ‘best guess’ $\hat{p}$,for $p$, and interpret this guess as the prior median. Solving for $\alpha$ leads to the choice

$$\alpha=\frac{\log(.5)}{\log(\hat{p})}-1.$$

As long as one does not choose $\hat{p}$ to be extremely close to 1,the resulting prior is not overly concentrated. For example, suppose the best guess for $p$ is .9,leading to $x=5.58.$ The resulting prior has fırst decile of .7,fırst quartile of .81, and third quartile of .96, reflecting a reasonable amount of variation.

# The posterior distribution
Under the above modeling assumptions, the posterior density of $\Theta=(p,V,\sigma^{2},\gamma,\mu)$ is

$$\pi(\Theta\mid x)=C_1^{-1}\cdot f(x\mid\sigma^2,\gamma,\mu)\cdot\left[\prod_{i:\gamma_i=1}^M\mathrm{N}(\mu_i\mid0,V)\right]\cdot\pi(\gamma\mid p)\cdot\pi(V,\sigma^2)\cdot\pi(p),$$

where $\pi(\gamma\mid p)=\prod_{i=1}^{M}p^{1-\gamma_{i}}(1-p)^{\gamma_{i}}$ and $C_{1}$ is the normalization constant.