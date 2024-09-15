# Monotonicity
A function is monotonically increasing if m <= n implies that f(m) <= f(n). It is monotonically decreasing if m <= n implies that f(m) >= f(n).

# Strict Increase/Decrease
Strict increase if m < n implies f(m) < f(n)
Strict decrease if m < n implies f(m) > f(n).

# Floors and Ceils
For any real number x, the greatest number less than or equal to x is floor(x).
The least integer greater than or equal to x is ceil(x).

The floor and ceil functions are monotonically increasing (they only ever grow).

For any int n, we have that floor(n) = n = ceil(n)

These are obvious
![[Pasted image 20240915155555.png]]
Floorx and ceilx never differ by more than one from x

![[Pasted image 20240915160042.png]]
1. When the same function applies multiple times to a fraction with multiple levels, you can still merge the denominators like normal.
2. Ceil and floor will not differ from an original fraction by more than (b-1)/b where b is the denom.

Flooring/ceil the sum of an integer and a real number is the same as only flooring/ceil the real number
![[Pasted image 20240915160309.png]]
# Modular Arithmetic
a mod n gives the remainder of $a / n$.
0 <= a mod n < n, even when a is negative.

For some reason they have a special way of showing equivalence of remainders.
a = b (mod n) if a and b have the same remainders when divided by n. In words we say this as **a is equal to b, modulo n.**
A special rule is that if a = b (mod n) (i.e. they have the same remainders from n), then b - a is divisible by n.

# Polynomials
A polynomial is asymptotically positive if and only if the coefficient of its biggest term > 0.
**For an asymptotically positive polynomial p(n) of degree d, we have p(n) = theta($n^d$).**
For any real constant a >= 0, the function $n^a$ is monotonically increasing.
For any real constant a <= 0, the function $n^a$ is monotonically decreasing.
We say that a function f(n) is polynomially bounded if $f(n) = O(n^k)$ for some constant k. (The top bound can be represented by a polynomial function)

# Exponentials
For all n and a >= 1, the function $a^n$ is monotonically increasing in n. When convenient, we assume that $0^0$ = 1.

We can relate the growth of polynomials and exponentials by the following fact. For all real constants a > 1 and b, we have
![[Pasted image 20240915162450.png]]
i.e. polynomial functions always grow slower than exponential functions, no matter the degree, as long as the base of exponential function > 1.

![[Pasted image 20240915162621.png]]
???

For all real x, we have
![[Pasted image 20240915162640.png]]
where equality is only true when x = 0.

When $|x| <= 1$, we have
![[Pasted image 20240915162753.png]]

x approaches 0
![[Pasted image 20240915162805.png]]
So the error of approximation runs at same as some quadratic function.

We have for all x,
![[Pasted image 20240915162937.png]]

# Logarithms
![[Pasted image 20240915162957.png]]

When no parentheses, the function only applies to the next term.
$lgn + 1 = lg(n) + 1$.

For any constant b > 1, $log_b(n)$ is undefined when n <= 0, strictly increasing when n > 0. It's negative if 0 < n < 1, positive if n > 1, and 0 if n = 1.

For all real a, b, c > 0 and n, we have
![[Pasted image 20240915163447.png]]
Should have already known all except bottom two.

For 3.19, changing the base of a logarithm from one constant to another only changes the value of the logarithm by a constant factor. We often use lg(n) because we don't care about constant factors and because so many algs and data structures involve splitting a problem into twos.

![[Pasted image 20240915163615.png]]

A function f(n) is polylogarithmically bounded if f(n) = O($lg^kn$) for some constant k.
For all real constants a > 0 and b, we have
![[Pasted image 20240915163909.png]]
Any positive polynomial function grows faster than any polylogarithmic function.

by the way $log^kn = (logn)^k$
# Factorials
