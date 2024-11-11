# Concept
**Definition (CD and asymptotic CD)** A function $H_{n}(\cdot)=H_{n}(x,\cdot)$ on $\mathcal{X}\times\Theta\to[0,1]$ is calleda CD for a parameter, if (1) For each given $x\in\mathcal{X},H_{n}(\cdot)$ is a (continuous) cumulative distribution function on O; (2)At the true parameter value $\theta=\theta_{0}$ ， $H_{n}(\theta_{0})\equiv H_{n}(x,\theta_{0})$ ,as a function of the sample 2L follows the uniform distribution $U(0,1).$ In addition, the function $H_{n}(\cdot)$ is called an asymptoticCDif condition (2）is replaced by (2')At the true parameter $\theta=\theta_{0}$ ， $H_{n}(\theta_{0})\stackrel{d}{\rightarrow}U(0,1)$ 0.8 $Tl\rightarrow\mathbf{x}$



# Example
**Example 1 (Singh et al.,2005)** Let $\tilde{\theta}$ be a consistent estimator of $\theta$ .For bootstrap, the distribution of $\hat{\theta}^\*-\theta$ is estimated by the bootstrap distribution $\hat{\theta}^{\*}-\hat{\theta}$ where $\tilde{\theta}^{\*}$ is the estimator of $\theta$ computed on a bootstrap sample (Efron and Tibshirani, 1993). An asymptotic CD for $\theta$ is given by $H_{n}(\theta)=1-Pr(\hat{\theta}^{\*}-\hat{\theta}\leq\hat{\theta}-\theta) = Pr(\hat{\theta}^{\*} \geq2\hat{\theta}-\theta)$ .In addition, when the limiting distribution of normalized $\tilde{\theta}$ is symmetric, the raw bootstrap distribution $H_{n}(\theta)=1-Pr(\hat{\theta}-\hat{\theta}^{\*}\leq\hat{\theta}-\theta)=Pr(\hat{\theta}^{\*}\leq\theta)$ is also an asymptotic CD.

**Example 2** Suppose we are interested in the location parameter $\theta$ of a continuous distribution.When the distribution $F$ is symmetric, i.e., $F(\theta-y)=1-F(\theta+y)$ ， $\theta$ is the median.The Wilcoxon rank test for $H_{0}:\theta=t$ ， $H_{1}:\theta\neq t$ is based on the summation of signed ranks of $Y_{i}-t$ ,ie.,the test statistic $W=\sum_{i=1}^{n}Z_{i}R_{i}$ ,where $R_{i}$ is the rank of $\left|Y_{i}-t\right|$ ， $Z_{i}$ is an indicator variable with 1 if $Y_{i}-t>0$ and -1 otherwise. Denote by $p(t)$ the $Y$ -value associated with the Wilcoxon rank test for $H_{0}:\theta=t$ ， $H_{1}:\theta\neq t$ When $t$ varies in $(-\infty,\infty)$ ,，the $P$ -value $p(t)$ is referred to as a $P$ -value function.We can prove that the $P$ -value function $p(t)$ is an asymptotic CD (Xie and Singh, 2013). Figures 2 provides illustrations of the asymptotic CD density $p^{\prime}(t)$ ,the asymptotic CD function $p(t)$ and the asymptotic CV $2min({p(t),1-p(t)\})$ for two sample sizes. The data are generated from $N(0,1)$ with sample sizes $n=10$ and 100, respectively



# CD-based inference
**Point estimation The natural choices of point estimators of the parameter** Given a CD $H_n(\cdot)$, include 

(i) the median $\widetilde{\theta}_n=H_n(1/2);$ 

(ii) the mean $\bar{\theta}_{n}=\int_{\theta\in\Theta}\theta dH_{n}(\theta);$ and

(iii) the mode $\widehat{\theta}_n=\arg\max_{\theta\in\Theta}h_n(\theta)$, where $h_n(\theta)=dH_n(\theta)/d\theta$ is the confidence density function. Under some moderate conditions, these three point estimators are consistent.

To further understand these three types of estimators, the median $\widetilde{\theta}_{n}$ is an unbiased estimator with 

$Pr_{\theta_0}(\widetilde{\theta}_{n} \leq \theta_0) = Pr_{\theta_0}(1/2 \leq H_n(\theta_0))=1/2$

The mean $\bar{\theta}_n$ can be viewed as a frequentist analog of Bayesian estimator under the squared loss function; The mode $\widehat{\theta}_n$ matches with the maximum likelihood estimator if the confidence densitv is from a normalized likelihood function (Xie and Singh, 2013)

**Confidence interval** As discussed in Section $\boxed2.1$, in a confidence curve, a line across the $y$-axis of the significance level $\alpha$ intersects with the confidence curve at two points, and these two points correspond to an $1-\alpha$ level, equal tailed, two-sided confidence interval for $\theta$, i.e., $(H_n^{-1}(\alpha/2),H_n^{-1}(1-\alpha/2)).$ Furthermore, $(-\infty,H_n^{-1}(1-\alpha)]$ and $[H_n^{-1}(\alpha),\infty)$ are one-sided $1-\alpha$ level confidence intervals for the parameter $\theta.$

**Hypothesis testing** From a CD, one can obtain p-values for various hypothesis testing problems The natural thinking is to measure the support that $H_n(\cdot)$ lends to a null hypothesis (Fraser, 1991) Xie and Singh (2013) summarized making inference for hypothesis testing from a CD in the following theorem.