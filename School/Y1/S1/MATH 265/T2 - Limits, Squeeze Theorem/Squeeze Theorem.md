---
summary: Explanation and example for squeeze theorem
tags:
  - coursenote
---
a last resort for calculating limits

# Basis
If two other functions enclose the function top and bottom, ie. g(x) <= F(x) <= h(x), and both of them approach some limit at the same x value, then we can say that F(x) also approaches that limit. In other words:
![[Pasted image 20230912161230.png]]
### Examples (rewrite this entirely in handwriting to make it make more sense)
![[Screenshot 2023-09-13 at 3.44.43 PM.png]]
We know that
-1 ≤ cos(1/x) ≤ 1

if we multiply both sides by x^2,
-x^2 ≤ x^2 * cos(1/x) ≤ x^2

and both -x^2 and x^2 approach 0 as x approaches 0. 
Hence, by the Squeeze Theorem, x^2 * cos(1/x) must also approach 0 as x approaches 0.