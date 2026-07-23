Given $k(x) = \frac{x^{4} + bx^{2} + 2}{1-x^{2}}$, find values of $b$ such that the graph of $k(x)$ has no inflection points?

- Generally to find inflection points, we want to find values of $x$ s.t $k''(x) = 0$ s.t $x$ is a turning point of the graph of $k'(x)$. To test whether $x$ is a t.p of $k'$, we can use a sign test or check if $k'''(x)$ is non-zero.
- Playing around with a manipulated plot, what should we expect from our final answers?
	- ![[Pasted image 20260723191543.png]]
	- Seems like for $b <-3$ the graph of $k'$ pretty much stays this shape
	- ![[Pasted image 20260723191702.png]]
	- For $-3<b<-2$ the graph completely changes shape, and there seems to be two tp's near the centre
	- ![[Pasted image 20260723191803.png]]
	- For $b>-2$ The graph pretty much stays in this shape, with no inflection points!
- Building cases:
	- Clearly for $b > -2$ there are no tp's of $k'$ hence no inflection points of $k$
	- for $b\in (-\infty, -3  ) \cup (-3,-2)$ there seems to exist some tp's of $k'$ and hence inflection points of $k$
	- Lets check cases
		- $b = -3$: by cancelllation of factors in the numerator and denominator, $k$ becomes  a parabola, so no inflection points
		- $b = -2$: Verify yourself; no inflection point. Why?
	- So overall, for $b =\in \{ -3 \} \cup [-2,\infty)$ there are no inflection points on the graph of $k$
Lets actually show why this is the case:
1. Lets plot $k''(x) = 0$ on a $b-x$ plane (i.e, solve for the parameter and plot the "parameter" graph) 
	![[Pasted image 20260723192644.png]]
2. For a given value of $b = \beta$, if $k(x)$ does NOT have an inflection point then one of the following must be true: 
	1. $k''(x) = 0$ has no solutions ($k'$ graph has no stationary points so they cant have any tps!)
		- $k''(x) =0$ has no solutions only when $b > -2$. This is when the inflection point in the centre stops being stationary, and becomes a non stationary infl. point.
	2. all solutions of $k''(x) = 0$ satisfy $k'''(x) = 0$ ($k'$ graph has stationary points, but they are inflection points NOTE THIS IS ON THE $k'$ GRAPH)
		- lets plot all the $(b,x)$ pairs of values for $b$ and $x$ that satisfy $k''(x) = 0$ (i.e the parameter graph) and $k'''(x) =0$ (also a parameter graph, but for a different equation of interest!)![[Pasted image 20260723195223.png]]
			- The parameter graph from $k'''(x) = 0$ actually gives us two straight lines.
		- We want solutions to $k''(x) = 0$ that also satisfy $k'''(x) =0$. Translating this to refer to our parameter graphs:
			- we want points on the red curve (red points satisfy $k''(x) = 0$) to also lie on the green lines (green points satisfy $k'''(x) = 0$)
			- we want the points in the intersection of the red and green "curves"!
				- quotation marks bc here the green "curve" is just a pair of lines. But in general it can be a more complicated curve
			- These are points corresponding to $b = -3, -2$
				- Why does $b = -2$ work? :)
- Putting the above two points together,
	1. No inflection points when $b > -2$
	2. No inflection points when $b = -3$ and $b = -2$
