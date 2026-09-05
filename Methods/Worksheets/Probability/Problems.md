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

---
1. Ranges for a and b
* $\int_0^{1000} f(x)\,dx = 1 \implies b = \frac{1}{1000} = 0.001$
* $f(x) \ge 0 \implies |a| \le b \implies a \in \left[-\frac{1}{1000}, \frac{1}{1000}\right]$

2. Smallest a, b, Probability p, and E[X]
* Smallest values: $a = -\frac{1}{1000}$, $b = \frac{1}{1000}$
* $p = P(X > 700) = \int_{700}^{1000} \left(-\frac{1}{1000}\sin\left(\frac{2\pi x}{1000}\right) + \frac{1}{1000}\right)dx = 0.3 + \frac{1 - \cos(1.4\pi)}{2\pi} \approx 0.5083$
* $\mathbb{E}[X] = \int_0^{1000} x f(x)\,dx = 500 + \frac{500}{\pi} \approx 659.15$

3. Expression for g(k)
* $N \sim \text{Binomial}(n, p) \implies P(N = 1 \mid n) = n p (1 - p)^{n-1}$
* $g(k) = \frac{(k+1)p(1-p)^k}{k p(1-p)^{k-1}} = \frac{k+1}{k}(1-p)$

4. Smallest k such that g(k) < 1
* $\frac{k+1}{k}(1-p) < 1 \iff k > \frac{1-p}{p} \implies k = \left\lfloor\frac{1-p}{p}\right\rfloor + 1$
* Represents the sample size $k$ at which $P(N=1 \mid n)$ reaches its maximum mode and starts declining

5. 95% Confidence Interval for P(X > 700)
* $\hat{p} = \frac{6}{45} = \frac{2}{15} \approx 0.1333$, $\text{SE} = \sqrt{\frac{\hat{p}(1-\hat{p})}{45}} \approx 0.0507$
* $\text{CI}_{0.95} = \hat{p} \pm 1.96 \cdot \text{SE} = [0.0340, 0.2327]$

6. Hypothesis Testing on Mean Bid
* Hypotheses: $H_0: \mu = 500$ vs. $H_1: \mu \ne 500$
* 95% CI: $\left[456.5 - c\frac{70}{\sqrt{n}}, \, 456.5 + c\frac{70}{\sqrt{n}}\right]$ (with $c \approx 1.96$)
* Accept $H_0$ if $500 \le 456.5 + 1.96\frac{70}{\sqrt{n}} \implies \sqrt{n} \le 3.154 \implies n \le 9$, so $n \in \{1, 2, \dots, 9\}$
* Type II error $\beta < 0.3$ when $\mu = 520$: $\beta \approx \Phi\left(1.96 - \frac{20\sqrt{n}}{70}\right) < 0.3 \implies 1.96 - \frac{2\sqrt{n}}{7} < -0.5244 \implies n \ge 76$

7. Louis's Expected Gain and Bribes
* $\mathbb{E}[X_{\max}] = \int_0^{1000} x \cdot \frac{n x^{n-1}}{1000^n}\,dx = \frac{1000n}{n+1}$
* $\mathbb{E}[\text{Gain}(n)] = \frac{1000n}{n+1} - 5n$
* Maximize: $\frac{d}{dn}\mathbb{E}[\text{Gain}] = \frac{1000}{(n+1)^2} - 5 = 0 \implies n+1 = \sqrt{200} \approx 14.14 \implies n = 13$ (gain $\approx \$863.57$)

8. Expected Resell Value
* $\mathbb{E}[U] = 1500$
* $\mathbb{E}[V] = 0(0.3) + (400 + 600 + 650)\frac{7}{30} = 385$
* $\mathbb{E}[\text{Resell}] = 0.3\mathbb{E}[U] + 0.7\mathbb{E}[V] = 0.3(1500) + 0.7(385) = 719.5$