- Louis is selling his art at an auction. However, he is afraid no one will show up to bid for his art. He can pay a random person $5 to show up and bid. Each bidder then bids $\$X$, where $X$ is a random variable distributed according to the density
	$$
f(x) = \begin{cases}
a\sin\left( 2\pi \frac{x}{1000} \right) + b  & 0 < x< 1000 \\
0 & else
\end{cases} 
$$
	for $a,b \in \mathbb{R}$
	- Find possible ranges for $a$ and $b$.
	- Let $a,b$ take their smallest possible values. Find the probability $p$ of a bid over $\$700$, and the expected bid amount.
	- Suppose all bidders place their bids independently. Suppose $n$ bidders appear at the auction. Let $N$ denote the number of bidders who bid over $\$700$
		- Find and simplify $g(k) = \frac{P(N = 1| n = k + 1)}{P(N = 1 | n = k)}$ in terms of $p$ and $k$. 
		- Find the smallest value of $k$ such that $g(k) < 1$. What does this represent?
	- Suppose instead $X$ had an unknown distribution with $\sigma = 70$
		- There are $n = 45$ bidders present at the auction, and $6$ of them bid over $\$700$. Find a $95\%$ confidence interval for the value of $P(X > 700)$.
		- ** A survey discovered that out of $n = k$ bidders, the average bid amount was $\$456.5$. It was previously assumed that the mean bid amount is $\$500$. Under a significance level of $\alpha = 0.05$, a hypothesis test was carried out for the mean amount.
			- State the null and alternative hypothesis
			- Find a $95\%$ confidence interval for the mean bid amount in terms of $n$. Suppose $P(-c<Z < c) = 0.95$. 
			- Using the above confidence interval, find the value(s) of $n$ for which we accept the null hypothesis
			- It was later found that the true mean was actually $\$520$. Find the value(s) of $n$ that results in a type 2 error rate of under $0.3$
	- As auctions usually do, the art will be sold to the highest bidder. Given $n$ bidders, maximum bid $X_{max}$ is distributed according to the density 
		$$
g(x) = \begin{cases}
n \frac{x^{n-1}}{1000^{n}}, & 0<x<1000 \\
0, & else
\end{cases}
$$
		- Find Louis's expected gain from this auction in terms of $n$
		- How many random people should Louis bribe to join his auction?
	- Suppose Louis's art can be resold. The resell value depends on whether he used real gold pigment or not. The probability he used real gold pigment was $0.3$. Given real gold pigment was used, the resell value is $U$. Otherwise, the resell value is $V$. $U \sim g$ where $g(x) = \frac{1}{1500}e^{-x/1500}, x> 0$ and $V$ is with mass function $p(x)$, where $p(0) = \frac{3}{10}, p(400) = p(600) = p(650) = \frac{7}{30}$. Find the expected resell value of his art.