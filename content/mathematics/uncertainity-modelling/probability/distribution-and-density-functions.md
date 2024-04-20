[Home](1%20Introduction.md)
<div style="text-align: justify;">

# Distribution and Density Functions

As discussed earlier, at any given instance a random variable takes on outcome from a set of possible outcomes. Consequently, for each random variable, a distinct set of probabilities is associated, contingent upon the potential outcomes. This is represented by the probability distribution function.

# Cumulative Distribution Function
The probability distribution function $F(x)$ of any random variable $X$ gives us the probability of $X$ taking on any value lower than a specified value $x$. It is known more appropriately as the `cumulative distribution function` (c.d.f).

> $F(x) = Pr(X \leq x)$

Probability distributions (functions) are either theoretically known or are determined through experiments.

> Theoretical, or first-principles approaches require a fair amount of process knowledge - Ogunnaike (2010).

The c.d.f.s may be described by theoretical (or closed-form) expressions, while many others are only known empirically in the form of tables. 

# Criterion for c.d.f 
For any function to qualify as the probability distribution function, it has to satisfy the following properties (implications provided in parentheses):

1. $0 \leq F(x) \leq 1, \forall x$
2. $\lim\limits_{x\to-\infty} F(x) = 0$,  $\lim\limits_{x\to\infty} F(x) = 1\quad$ (Probability of no and any occurrence is 0 and 1, respectively)
3. $F(x)$ is a `non-decreasing function` in the sense that, for any $h \geq 0$ and all $x$,
$F(x + h) \geq F(x)$ (Probability cannot be negative)
4. $F(x)$ is right-continuous for all $x$, i.e., $\lim\limits_{h\to 0+}F(x + h) = F(x)\quad$ ($F(x)$ can have “jumps” )

Depending on the type of random variable , a c.d.f can be continuous or discontinuous (discrete). The salient differences between these distributions are listed below.

**Continuous c.d.f.s**
1. $F(x)$ is `continuous and differentiable` for almost all $x$ (e.g., Gaussian).
2. For these distributions, a `density` function (like in mechanics) exists.

**Discrete c.d.f.s**
1. $F(x)$ is a simple step function with jumps at points (e.g., Binomial).
2. No density function exists for this case. Instead a `probability mass function` that determines $Pr(X = x)$ is defined (e.g., counts of number of heads in a coin toss, face value on a die).
3. The probability of taking on a value between jump points is zero.

One could also encounter phenomena with mixed or hybrid distributions. The Lebesgue’s decomposition theorem (Priestley, 1981) states that `any distribution function can be decomposed into a sum of continuous and discrete distributions, and a third term which is singular in nature`. The third type arises only in pathological situations and is largely of academic interest.

# Probability mass function (p.m.f)
Let $X$ be a discrete random variable with range $R_X={\lbrace x_1,x_2,x_3,...\rbrace}$
 (finite or countably infinite). The function
$P_X(x_k)=P(X=x_k), \forall k=1,2,3,...,$ is called the probability mass function (PMF) of $X$.

Note that by definition the p.m.f is a probability measure, so it satisfies all properties of a probability measure. The properties of a p.m.f are
1. $0 \leq P_X(x) \leq 1,\forall x$
2. $\displaystyle\sum_{x\in R_X}P_X(x)=1$
3. for any set, $A \subset R_X, P(X \in A)= \displaystyle\sum_{x\in A}P_X(x)$

# Probability density function (p.d.f)
To determine the distribution of a discrete random variable we can either provide its p.m.f or c.d.f. For continuous random variables, the c.d.f is well-defined so we can provide the c.d.f. However, the p.m.f does not work for continuous random variables, because for a continuous random variable, $P(X=x)=0, \forall x \in \mathbb{R}$. Instead, we can usually define the probability density function. The p.d.f is the density of probability rather than the probability mass. This leads to the formal definition of a probability density function (for readers seeking an intuitive understanding of its derivation, we encourage them to explore Pishro-Nik, 2014).

Consider a continuous random variable $X$ with an absolutely continuous c.d.f $F_X(x)$. The function $f_X(x)$ defined by

> $f_X(x)=dF_X(x)dx=F'_X(x)$, if $F_X(x)$ is differentiable at $x$

is called the probability density function (p.d.f) of $X$. Since the p.d.f is the derivative of the c.d.f, the c.d.f can be obtained from p.d.f by integration (assuming absolute continuity):
> $F_X(x)=\int\limits_{-\infty}^x f_X(u)du$

Note that by definition the p.d.f is a probability measure, so it satisfies all properties of a probability measure. The properties of a p.d.f are
1. $f_X(x)\geq 0, \forall x \in \R$
2. $\int\limits_{-\infty}^{\infty} f_X(u)du=1$
3. $P(a \lt X\leq b)=F_X(b)−F_X(a)=\int\limits_a^b f_X(u)du$
4. More generally, for a set $A$, $P(X\in A)=\int\limits_Af_X(u)du$

> For a continuous random variable $X$, $Pr(X=x) = 0, \forall x \in \R. $ Why?

For a continuous random variable, the probability of any specific value (let's say $x$) being exactly equal to a specific point in the real number line ($x \in \mathbb{R}$) is zero. In mathematical terms, $P(X = x) = 0$ for any specific \(x\) in the range of the continuous random variable.

This is because in the context of continuous random variables, we are dealing with an uncountably infinite number of possible values within a range. The probability of any single point in that infinite range is infinitesimally small and, mathematically speaking, it is considered to be zero. In essence, when dealing with continuous random variables, we focus on the probability of a random variable falling within a certain range rather than at a specific point. The probability is defined over intervals rather than individual points due to the continuous nature of the variable.

# Summary: Distribution functions

A c.d.f exists for all random variables, whereas the probability density function (p.d.f) exists only for continuous random variables and the probability mass function (p.m.f) exists for only discrete random variables.

1. **Probability Mass Function (p.m.f):**
   - **Definition:** The p.m.f is associated with discrete random variables.
   - **Purpose:** It gives the probability that a discrete random variable is equal to a specific value.
   - **Denoted as:** $P(X = x)$, where $X$ is the random variable, and $x$ is a specific value it can take.
   - **Example:** For a fair six-sided die, the p.m.f might be $P(X = 1) = \frac{1}{6}$, $P(X = 2) = \frac{1}{6}$, and so on.

2. **Probability Density Function (p.d.f):**
   - **Definition:** The p.d.f is associated with continuous random variables.
   - **Purpose:** It describes the relative likelihood of the variable taking on a particular value.
   - **Denoted as:** $f(x)$, where x is a specific value.

3. **Cumulative Distribution Function (c.d.f):**
   - **Definition:** The c.d.f, whether for discrete or continuous random variables, gives the probability that a random variable is less than or equal to a specified value.
   - **Denoted as:** $F(x)$ for any random variable.
   - **Calculation:** For a continuous variable, $F(x) = \int\limits_{-\infty}^{x} f(t) dt$. For a discrete variable, $F(x) = P(X \leq x) = \sum\limits_{t \leq x} P(X = t)$.

The c.d.f provides the cumulative probability up to a certain point, and the p.d.f/p.m.f gives the probability density or mass at a specific point. In practice, we work with either the p.d.f or the p.m.f. 

# Model vs Distribution
</div>
<br>
<div style="display: flex;justify-content: space-between; text-align: end;">
<div></div>
<div>

[Previous](laws-of-probability.md)</div>
<div style="text-align: end;">

[Next](file_name.md)</div>
</div>