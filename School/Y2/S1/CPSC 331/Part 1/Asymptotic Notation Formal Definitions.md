# Useful Example
![[Pasted image 20240908143802.png]]
a) We write that f(n) = O(g(n)) as long as there is some n value n0 and value c such that for all n values right of n0, cg(n) >= f(n)

b) We write that f(n) = Ω(g(n)) as long as there is some n value n0 and value c such that for all n values right of n0, cg(n) <= f(n)

c) We write that f(n) = Θ(g(n)) as long as there is some n value n0, values c1 and c2 such that for all n values right of n0, c<sub>1</sub>g(n) <= f(n) <= c<sub>2</sub>g(n)
# O-notation
We use O-notation to give an upper bound to a function to within a constant factor.
![[Pasted image 20240912200516.png]]
O(g(n)) is the set of functions where there exist positive constants c and n<sub>0</sub> s.t. f(n) is non-negative AND on or below cg(n) for all n past n<sub>0</sub>.

Also, g(n) must also be asymptotically non-negative (non-negative for all values past n<sub>0</sub>)

### Example
4n<sup>2</sup> + 100n + 500 = O(n<sup>2</sup>) 

To do this we want a c and n<sub>0</sub> such that 4n<sup>2</sup> + 100n + 500 = *O*(n<sup>2</sup>)
If we choose c = 604, then n<sub>0</sub> works.

n<sup>3</sup> - 100n<sup>2</sup> doesn't belong to O(n<sup>2</sup>).
To do this, we want to prove that n<sup>3</sup> - 100n<sup>2</sup> <= cn<sup>2</sup>.
This gives n - 100 <= c
then n <= c + 100 for all n greater than n<sub>0</sub>. We can see that n will eventually outgrow c + 100 no matter what, so this can't be true.

# Ω-notation
Ω-notation provides an asymptotic lower bound. For a given function g(n), 
![[Pasted image 20240912202517.png]]
There must exist constants g and n<sub>0</sub> such that cg(n) is non-negative AND below f(n) for all n ≥ n<sup>0</sup>

Now we want to show
$$4n^2 + 100n + 500 = Ω(n^2)$$
To do this we want a $c$ and $n^0$ such that
$$4n^2 + 100n + 500 ≥ cn^2$$ for all $n≥n_0$.

Any positive $n_0$ works and $c=4$.

# Θ-notation
Represents asymptotically tight bounds. 
![[Pasted image 20240912203536.png]]

# Theorem
For any two functions f(n) and g(n), we have f(n) = Θ(g(n)) iff f(n) = O(g(n)) and  f(n) = Ω(g(n))

# Asymptotic Notation and Running Times
When using asymptotic notation for running times, try to get it as precise as possible. For example we can say insertion sort is at worst case $O(n^2), Ω(n^2), and Θ(n^2)$, but we should stick with $Θ(n^2)$ because it is the most precise.

Precision also requires us to get rid of the extra terms and coefficients, which lets us more simply categorize different algorithms.

# Asymptotic Notation in Equations and Inequalities
We already know what it means when we do $function=O(n)$, but what do we mean when we put the notation in a formula like $2n^2+3n+1=2n^2+O(n)$? Well O(n) just represents a function within the set O(n) that we don't care to name.
Like we did with merge sort's running time.
![[Pasted image 20240912205150.png]]

This lets us ignore pointless things. If we are only interested in T(n) as it grows, then we were going to throw away the constants and other terms of the function anyway, so might as well do it now to make analysis easier.

Also, the number of anonymous functions in an expression is equal to be the number of times the asymptotic notation appears. 
![[Pasted image 20240912205511.png]]
In this formula, since O(i) only appears once, there is only one anon function.

In some cases, asymptotic notation appears on the left-hand side of equation, like 
![[Pasted image 20240912205545.png]]
Follow this rule: No matter how the anonymous functions are chosen on the left of the equal sign, there is a way to choose the anonymous functions on the right of the equal sign to make the equation valid.

So for any f(n) in Θ(n), there is some function g(n) in $Θ(n^2)$ s.t. $2n^2+f(n)=g(n)$ for all n.

Additionally, we can chain together such relationships like
![[Pasted image 20240912205741.png]]
$Θ(n)$ means some function, then $Θ(n^2)$ means $2n^2 + Θ(n)$ is within $Θ(n^2)$.

# Proper Abuses of Asymptotic Notation
Asymptotic notation is based on some variable tending to infinity, but we don't specify which, that should be gleaned from context. 

Things like $T(n) = O(1)$ for n<3 are kind of meaningless by our formal definition, since T is bound. However, we can interpret this as being that T(n) is less than some constant as long as n<3.

Also sometimes a description of running time might only apply to input sizes that are exact powers of 2. In this case we just tell from context.

# o-notation
In O-notation our upper bound MIGHT NOT be asymptotically tight. Using o-notation we can denote if something IS NOT asymptotically tight.

![[Pasted image 20240912210846.png]]
Note how it's < and not ≤ $cg(n)$ now.

For example, $2n=o(n^2)$, but $2n^2≠0(n^2)$, because $2n^2$ is too tight with $n^2$. You can say that in O notation the bound only holds for some constants c>0 (there's a chance that the constant helps overcome), but in o notation the bound holds for ALL constants c>0, because it eventually becomes insignificant.

# ω-notation
To omega-notation as o-notation is to O-notation. Lower bound that is not asymptotically tight.
One definition: $f(n)$ in $ω(g(n))$ iff $g(n)$ in $o(f(n))$

Formally:
![[Pasted image 20240912211626.png]]
Note again that cg(n) < f(n) and not ≤.

For example, $n^2/2 = ω(n)$, but $n^2/2 ≠ ω(n^2)$, because $n^2/2$ is tight.

# Comparing Functions
