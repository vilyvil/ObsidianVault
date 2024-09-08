Insertion sort uses the incremental method, but another design is the "divide-and-conquer" method.

# Divide and Conquer
Breaking the problem into smaller subproblems, solving those problems recursively, and then combining solutions into one big solution.

Typically ends when you reach base case, where you solve the problem directly without any recursion.

Three Steps:
1. Divide into multiple subproblems that are smaller instances of the same problem
2. Conquer the subproblems recursively
3. Combine subproblem solutions to form a solution to the og problem

Merge sort follows divide and conquer closely.
1. Divide the array into two adjacent subarrays, each half the size of the og.
2. Conquer by sorting each of the two subarrays using merge sort
3. Combine by merging the two sorted subarrays

The merging procedure is a big part of the sorting algorithm. It, in the worst case, takes n time, which is when both subarrays run out of keys at the same time so the keys must be compared n - 1 times.

# Analyzing Divide and Conquer
Since divide-and-conquer algs are recursive by nature, you can use recursive equations to find their running time.

Suppose that the division of a problem gives a subproblems, where the size of each n/b. For example, for merge sort a = 2 and b = 2, since we split each array in half, giving 2 subarrays to sort, and each array has an input size of n/2. It takes T(n/b) time to solve one subproblem, so it takes aT(n/b) time to solve all of them. In our case, that means 2T(n/2).

Then suppose that it takes D(n) time to divide the problem and C(n) time to combine subproblems.

T(n) then becomes: 
![[Pasted image 20240906203422.png]]
Where n < n0 represents the base case being solved in constant time. (Constant time is Θ(1) since we're ignoring the coefficient)

Sometimes dividing doesn't result in entirely equal parts, but it'll always result in a difference of at most one between each part, so we're going to ignore it.

We're going to **ignore base cases** since they're almost always constant time so who cares.

# Analysis of Merge Sort
- Divide: D(n) = Θ(1) since we're just finding the middle of the subarray
- Conquer: 2T(n/2), since each subproblem takes T(n/2) time and there are 2 of them
- Combine: As shown before, merging takes Θ(n) time.

Together, the Θ(1) + Θ(n) just result in a linear equation, so Θ(n) again.
T(n) = 2T(n/2) + Θ(n)

Later we're going to have a master proof to prove that this = Θ(n * log2(n)).

#finished