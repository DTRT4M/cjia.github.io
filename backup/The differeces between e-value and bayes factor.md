# False discovery
Consider these hypothesis testing questions:
$$H_{0j} vs H_{1j}, j=1,2...,n$$.
We want to test these an the same time, then we will receive these four results:
Table 1:多重假设检验中的四种潜在结果

<table>
	<tbody>
		<tr>
			<th> </th>
			<th>Fail to reject $H_{0}$</th>
			<th>Reject $H_{0}$</th>
			<th>Overall</th>
		</tr>
		<tr>
			<td>$H_{0}$is true</td>
			<td>$V$</td>
			<td>$U$</td>
			<td>$p_0$</td>
		</tr>
		<tr>
			<td>$\mathrm{H}_{0}$is false</td>
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

## Familywise Error Rate(FWER)
The traditional method to control gobal hypothesis test hope to strictlt control familywise error rate
$$FEWR = P(U\geq 1) \leq \alpha,$$
which means the probability of controlling for the rejection of at least one of the true original hypotheses does not exceed a given significance level $\alpha$.
