Questions such as "Find the value(s) of parameter $k$ such that $f(x;k) = g(x;k)$ has $n$ solutions" are very common. 
- $f(x;k)$ here represents some function of $x$ that includes a parameter $k$, eg: $f(x;k) = x^{2} - k$
# 1) Via transformations
- Least common, graphical method
- Look at how the parameter(s) transforms the graphs of $f$ and $g$ and deduce when there are $n$ solutions
- eg:
	1. Find the values of $k$ such that the graph of $f(x) = x(x+1)(x-1) - p$ has 
		1. one root
		2. two roots
	2. Find the values of $h$ such that the graph of $f(x-h)$ has only one positive root
	
# 2) Tangential method
- It helps to first find the values of $k$ that makes the graphs tangential at the point (touching, same gradient)
1. Let $f(x)=2e^{kx}-2$, where $k >0$, find the value(s) of $k$ s.t $f$ and $f^{-1}$ only intersect once
	- Solution: **Method of tangency works best in questions where it is difficult to solve for the parameter such as these**
	- Graphically, changing the value of k dilates the graph of f and its inverse, and it can be noted that $f(x)=f^{-1}(x)$ always has a solution at x = 0.
	    - (This is also apparent as $f$ is strictly increasing, we can equate f to y = x )
	- For there to only be one solution, f and its inverse must be tangent to one another at their point of intersection. This is as $f$ is convex and $f^{-1}$ is concave, therefore the only way they can only one solution is if they are tangent at their point of intersection
	- we can use this fact by equating $f'(0)=f^{-1'} (0)$, as we know x = 0 is always a solution
		- Solving for k yields $k = \pm\frac{1}2$, since $k >0$, k = $\frac12$
2. Let $f(x)=\frac{k}{x-2}$, $g(x) = \sqrt{4-kx}$ where both $f$ and $g$ have their respective maximal domains, and $k \in R\setminus\{0\}$. Find the value(s) of k correct to two decimal places s.t there is only one intersection between $f$ and $g$

## 3) Solving for the parameter first
- Idea is to solve the equation $f(x;k) = g(x;k)$ for the **parameter** $k$ in terms of $x$
	- This expression for $k$ in terms of $x$ represents $x_{0}-k_{0}$ pairs that gives a solution to $f(x;k) = g(x;k)$ at $x$ value $x_{0}$ when the parameter $k = k_{0}$
	- Can look at the graph of $k$ to $x$ to determine the $k$ values that crosses the graph $n$ times, representing $n$ solutions
1. Try doing the questions from 2) with this method
	1. Watch out for discontinuities
2. Find the values of $a$ such that the graph of $f(x) = a\cos(x) + x^{2} - ax^{2}$ has 
	- 1 stationary point
	- 3 stationary points


