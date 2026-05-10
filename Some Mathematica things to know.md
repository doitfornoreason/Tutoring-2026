# When to use Surd[...]

- Mathematica doesn't like having negative values raised to fractional powers when rendering
	- Usually not a problem for algebraic manipulation
	- IS a problem when visualising
- This means you won't see certain parts (usually negative) of fractional power graphs
	- Eg: Inverse of $f(x) = x^{3}$
	![[Pasted image 20260503184007.png]]
	- Where did the negative part of the graph go?
- Need to use `Surd[x, 3]` instead.
	![[Pasted image 20260503184045.png]]
- Alternative: can also use `CubeRoot[x]` - Although I don't recommend this, just go for `Surd[x, n]` to get $x^{1/n}$ for any $n$
# Difference between SolveAlways and FindInstance
- `SolveAlways`: Finds values of unknown parameters that makes an equation of $x,y$ true for all values of $x, y$  
	- This treats $x,y$ as variables of a function, whereas the parameters are fixed
	- Takes in the function variables (variables that are free)
- `FindInstance`: Finds a set of values for unknown variables that makes the equation true
	- This doesn't distinguish between the types of variables 
	- You are not letting any of the variables be free. All are considered fixed
	- Takes in all unknown variables
-  $f(x) = ax^{2}$, $x$ is a function variable and $a$ is a parameter, they are treated
	- differently in `SolveAlways`, same in `FindInstance`
## EXAMPLES
1. Q: "Find values of $a, b,c$ such that $x^{2} - 3x + b y + a = (x-b)(x - c) + c y \quad \;\forall \; x,y \in \mathbb{R}$
	- Finding values of unknown PARAMETERS so that the equation holds. $x, y$ are function variables that are free (can be anything)
```mathematica
SolveAlways[x^2 - 3 x + b y  + a == (x - b) (x - c) + c y, {x,y}]
		
> {{a -> 9/4, b -> 3/2, c -> 3/2}}
```
2. Q: "Find values of $a,b,c \in \mathbb{R}$ such that $\frac{a + b - c}{3} - 2= \frac{a}{c}(b - 10)+ 1$ "
	- Simply just finding values of all unknowns so that the equation holds. None of them are function variables.
```mathematica
FindInstance[(a + b - c)/3 - 2 == a/c (b - 10) + 1, {a, b, c}]

> {{a -> -(7/26), b -> 1, c -> -1}}
```