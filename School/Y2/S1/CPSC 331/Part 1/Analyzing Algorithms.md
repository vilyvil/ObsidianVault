Predicting the resources needed by an algorithm. Though you might care about memory, bandwidth, or energy consumption, you'll mostly care about computational time. 

For the textbook we will assume that we have one processor, random-access machine model where operations happen one after the other instead of concurrently. Each instruction will take the same amount of time and each data access will take the same amount of time as other data accesses.

The basic instructions of RAM will be things like math (add, subtract, multiply, divide, remainder, floor, ceiling), data movement (load, store, copy), and control (conditional/unconditional branch, subroutine call and return).

Data types will be int, float, char. 

Some instructions are in a gray area, however. Exponentiation can vary in time when the resulting number is too big to store in a single computer word, and the multiplication has to happen different numbers of times. However finding powers of two is easy because you just have to shift all your bits n positions to the left (where we're looking for 2^n).

# Analysis of Insertion Sort
We can't just analyze algorithms by running timed tests, since so many things can differ. The computer itself will differ from others, you can't test every single input, your libraries will affect performance, your language, etc.

- Running time depends on input size
	- Although running time also depends on whether or not the list is almost sorted, input size has the greatest effect so we'll focus on that.

If we do this, then we have to be clear if we're talking about best-case, worst-case or some other case.

#### Input Size
Can vary, but in general it'll be things like "number of things in the list" or "total number of bits (like for multiplication)" or "number of vertices and edges in the graph"

#### Running time
Number of instructions and data accesses needed. We will assume that each line will always take the same amount of time between runs (this doesn't mean that every line of code takes the same amount of time. just that one particular line always takes the same amt of time)

## Notation
Let n be the input size
Let ti denote the number of times the while loop test is executed for that value of i.
- Also, when a for or while loop finishes, the test is executed one more time than the body
Let ck be the steps it takes for a statement to execute
Let m be the amount of times that statement executes
Let T(n) represent the running time of an algorithm for the input size n

To find T(n), we add up the products of costs and times.
![[Pasted image 20240906195211.png]]

## Analysis
In the best case, the array is already sorted. In this case, line 1 is run n times, line 2 is run n - 1 times, line 4 is run n - 1 times, line 5 is run n - 1 times, line 6/7 are skipped, and line 8 is run n - 1 times.
![[Pasted image 20240906195609.png]]

In the worst case, the array is in reverse sorted order. In this case, every time we add something to the sorted subarray we need to compare it with every single number in the subarray before we can place it. Lines 5, 6, and 7 are run 2 + 3 + 4 + ... + n times, which results in that stupid formula.
![[Pasted image 20240906195916.png]]

For the rest of the book we're going to focus on the worst case running time, since:
- It gives an upper limit on the running time.
- Worst case can happen quite often
- Average case is usually just as bad as the worst case.

Sometimes, however, we'll be interested in average case analysis, which we'll do later.

## Order of growth
We're not actually interested in all that disgusting math with all the c's. What we really want is just the rate of growth of the algorithm: Polynomial, linear, logarithmic, etc. 

To do this we just consider the exponent of the leading term, ignoring the coefficient as well as the other terms, since the exponent has the greatest effect as the input size grows. 

To highlight order of growth we use theta: Θ(n). think of Θ-notation as saying "roughly proportional when n is large." 

We usually consider an algorithm to be slower than another if it has a higher order of growth in the worst case.

# Limitations
Since we're ignoring constants, order of growth comparison is not going to be accurate for lower input sizes. However, it will always work for some big enough n.

#finished