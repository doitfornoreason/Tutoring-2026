Trying a new typesetting format for this topic, lmk if you end up preferring this format or the previous format (or dont care about it)

---

# Logic
- A statement in math can be either true or false (has a truth value of T or F). We often call it by a capital variable as shorthand
	- $P: \text{"The sky is blue right now"}$
	- $Q: \text{"It is night time"}$
	- These are two statements, each is either true or false, often called *primitive statements*
- We can construct more complicated statements out of these primitives, using *connectives*. They connect primitive statements together
	- The statement $S:$ "it is day time" should have the exact opposite truth value to $Q$ 
		- when its night: $Q = T$ and $S = F$
		- when its day: $Q = F$ and $S = T$
- when we create a new statement out of primitive statements and connectives, we call them *compound statements*
### Connectives
1. **Negation**: negation of a statement $p$ is the statement 'not $p$' and is denoted by $\sim p$, the truth value of $\sim p$ is opposite of $p$
2. **"and"** (conjunction) : basically "and" conjunction of $p$ and $q$ is the statement $p\wedge q$ which is true if only *both* $p$ and $q$ are true
3. **"or"** (disjunction): basically "or", disjunction of $p$ and $q$ is the statement $p \vee q$ which is true if either *or* both $p$ and $q$ are true 
	- Note: "Or" here works slightly different to English language. This is the inclusive or, meaning we accept the possibility of both statements being true
4. **implication**: The statement that $p$ implies $q$, which defaults to true *except for the case $T \implies  F$*
	This means that the statement $p \implies  q$ is true even if  $p= F$, regardless of the value of $q$ as it does not violate the statement
	- This means that the statement $p \implies  q$ being true does not imply anything about the values of $p$ or $q$ 
	- **Converse** of an implication $p \implies  q$ is the statement $q \implies  p$, i.e just swap the primitive statements around
5. **Double implication:** $p \iff q$, which is equivalent to $(p \implies  q) \wedge (q \implies p)$
- Examples: 
	- $P:$ I am wearing a jacket
	- $Q:$ It is winter
	1. $\sim P:$ I am not wearing my jacket
	2. $P\wedge Q:$ I am wearing my jacket and it is winter
	3. $P\vee Q:$ I am wearing my jacket or it is winter
		- This is NOT the same as "***either*** I am wearing my jacker or it is winter". Why?
		- $P\vee Q$ is true if any of $P$ or $Q$ is true, even if both of of them are true!
	4. $Q \implies  P:$ If its winter, I am wearing my jacket
		- its reasonable to say that $Q \implies P$ is a true statement. Whenever its cold, ill wear my jacket. But is $P\implies Q$ true?
		- The converse of a true implication is not always true...
- Remember, there is no rule saying I must use variables to represent my statements. Sometimes its clearer not to
	- Let $A = \{ 1,2 \}, B = \{ 2,3 \}$
	- Translate this into formal logic: "$2$ is in $A$ and $B$" 
### Quantifiers
- Way to quantify "how many"
	- $\forall$: for all (every one of)
	- $\exists$: there exists (at least one of)
- Often, "such that" is abbreviated for "s.t" after using the quantifiers
- Examples: say $S = \{ 2,4,5,6,10 \}$. We could say the following things about this set
	- $\;\forall \; x \in S,\; x > 1$ 
		- "For all elements $x$ in $S$, $x$ is bigger than one"
	- $\exists y \in S\text{  s.t  } y \text{ is odd}$ 
		- "There exists a value $y$ in $S$ such that $y$ is odd"
- Examples: describe what we would have to demonstrate in order to disprove each of the following statements
	- At every school in Melbourne, there is a student who is at least seven feet tall
	- For all schools in Melbourne, there exists a teacher who gives every student a grade of either A or B
	- There exists a school in Melbourne where every student is at least six feet tall

## Types of proofs, Truth Tables
- To prove the statement $A \implies  B$ (or $A \implies  \sim B$)
1. Direct Proof
2. Proof by contradiction
3. Proof by contrapositive
4. Proof by induction
### Proof by induction
- To prove a statement $S(n)$ for all $n \in \mathbb{N}$
- Show that $S(n)$ is true for some base case $n_{0}$
- Show that if $S(k)$ is true for some $k$, then it must also be true for $S(k + 1)$
	- This allows us to "cascade" the proof forward
	- As we know $S(n)$ is true for some base case $n_{0}$, it must be true for $n_{0} + 1$ which means its true for $n_{0} + 2$, ...
