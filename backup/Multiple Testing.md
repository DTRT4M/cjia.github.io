# False discovery
Consider these hypothesis testing questions:
$$H_{0j} vs H_{1j}, j=1,2...,n$$.
We want to test these an the same time, then we will receive these four results:

Table 1:Four potential outcomes in multiple hypothesis testing

<table>
	<tbody>
		<tr>
			<th> </th>
			<th>Fail to reject $H_{0}$</th>
			<th>Reject $H_0$</th>
			<th>Overall</th>
		</tr>
		<tr>
			<td>$$H_0$$ is true</td>
			<td>$V$</td>
			<td>$U$</td>
			<td>$p_0$</td>
		</tr>
		<tr>
			<td>$$H_0$$ is false</td>
			<td>$S$</td>
			<td>$T$</td>
			<td>$P1$</td>
		</tr>
		<tr>
			<td>Overall</td>
			<td>$p-R$</td>
			<td>$R$</td>
			<td>$\mathcal{D}=\mathcal{D}_{0}+\mathcal{L}$</td>
		</tr>
	</tbody>
</table>

From this table, we could find out there are two types of error in multiple testing:
+ $p_0$ = # {Null}
+ $p_1$ = # {Alternative}
+ U = # {Fales discovery/ False postive} $\longleftarrow$ type-I error
+ S = # {False negative} $\longleftarrow$  type-II error
+ T = # {True positive}
+ R = # {Total rejection}
Therefore question is that --- How to control typr-I error?



# Familywise Error Rate(FWER)
The traditional method to control gobal hypothesis test hope to strictlt control familywise error rate
$$FEWR = P(U\geq 1) \leq \alpha,$$
which means the probability of controlling for the rejection of at least one of the true original hypotheses does not exceed a given significance level $\alpha$.



## Benforonni correction

Step 1: For each hypothesis $${H_{0j}}_{j=1}^p$$, construct the test statistic $$\{T_j\}_j=1^p$$, compute the p-value $$\{p_j\}_j=1^p$$

Step 2: For $$j=1,\cdots,p$$, reject the corresponding original hypothesis $$h_{0j}$$, if $$p_j\leq \frac{\alpha}{p}$$. 

Define $S_{0}={j:H_{0j}}$ is true , and the Benforonni correction method satisfies

$$\text{FWER}=\mathbb{P}\left(\bigcup_{j\in S_0}\{p_j\leq\alpha/p\}\right)\leq\sum_{j\in S_0}\mathbb{P}(p_j\leq \alpha/p) = p_0 \frac{\alpha}{p}<\alpha.$$

Two flaws in the FWER criterion: 
+ Theorem 1 states that the Benforonni correction will actually control the FEWR below the level of $p_0 \frac{\alpha}{p}$. The Benforonni correction is conservative when the difference between $p_0$ and $p$ is large;
+ When the scale of multiple tests $p$ is large or even divergent, the rejection threshold $\alpha/p$ of Benforonni correction degenerates and tends to cause the FWER criterion to be too strict and not to reject any hypothesis .

Therefore, we need a new method to improve this situation.