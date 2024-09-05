---
summary: important information about limits that was not immediately clear from Math 31
tags:
  - coursenote
---
# Replacement for "really small +/-"
This class uses the notation of 0+ or 0- to describe a value that approaches 0 from the positive or negative side

# Vertical Asymptotes special case
When a graph approaches a vertical asymptote from only one side (because it does not exist past that x-value), it is still considered a vertical asymptote

# When does a limit fail to exist? What does a function look like when its limit doesn't exist at a point?
1. The limit could approaches infinity
2. The right and left side limits of the point are not equal
3. The domain of the function does not include that point
4. \*!!! graph oscillates around that point, meaning we cannot pinpoint a specific y value even though the point does not violate any other rule
	- ex. when x approaches infinity, sin(x) oscillates between -1 and 1, never reaching a particular value
	- ex. when x approaches 0, sin(pi/x) oscillates violently, making it hard to pinpoint the exact limit

# Thought process for calculating a limit
Try to use the substitution rule (substitute the value that x approaches into the function) to get the limit.

This will only be possible if:
- The function is a normal function (ie. not piecewise and other funky business)
- The x-value exists in the domain

If this ends up not being possible, then try to use algebra and simplification to rewrite the function in a way that the substitution method is possible.
Possible steps:
- Factor out to allow for simplification of function
- Multiply top and bottom by a conjugate
- Find the common denominator between rational functions

# Indeterminacy
0/0, 0 * ∞, ∞ - ∞
it is considered indeterminate
we need to rewrite the expression in the limit to fix it

# Conditions for limit laws
- Both limits have to exist at the point

# This does not exist because:
![[Screenshot 2023-09-13 at 3.38.08 PM.png]]
As 1/x approaches -∞ and ∞, the value oscillates and never reaches a point.

Though 1/0 is not defined, that does not matter. The limit doesn't care about what actually happens at the point, just what happens as it approaches, and this limit in particular will approach infinity.