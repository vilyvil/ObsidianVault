### Asymptotic Efficiency
When we study input sizes large enough that we only need to look at order of growth.

Concerned with running time as it increase with input size as it grows with no bound.

# O-notation, Ω-notation, Θ-Notation
Previously we learned about Θ-notation, where we threw away everything except for the term with the biggest degree (including that term's coefficient), but there exist other forms of asymptotic notation.

Bear in mind that the asymptotic notations we'll be looking at are designed so they characterize functions in general.

## O-notation
Provides an upper bound to the asymptotic behaviour of a function. The function should be guaranteed not to grow faster than the O indicates.

Ex. 7n^3 + 100n^2 - 20n + 6
Is O(n^3). But it is also O(n^4), O(n^5), O(n^6), O(n^7), etc.

## Ω-notation
Provides a lower bound on the asymptotic behaviour of a function. It guarantees that a function grows at least as fast as that rate.

Ex. 7n^3 + 100n^2 - 20n + 6
Is Ω(n^3). But also Ω(n^2), Ω(n^1) or even lower.

## Θ-Notation
Provides a tight bound on the asymptotic behaviour of a function. It specifies that a function grows precisely at the given rate. In other words, it guarantees that a function is within bounds of that rate from above and below. The above and below don't need to be equal.

If you can show that a function is O(f(n)) and Ω(f(n)), then you've shown that it's Θ(fn).

Ex. 7n^3 + 100n^2 - 20n + 6
Is O(n^3) & Ω(n^3), so it is Θ(n^3).

### Example with Insertion Sort
```
Insertion-Sort(A,n)
for i = 2 to n
	key = A[i]
	// Insert A[i] into the sorted subarray A[1:i - 1]
	j = i - 1
	while j > 0 and A[j] > key
		A[j + 1] = A[j]
		j = j - 1
	A[j + 1] = key
```

O(n)
Our implementation of insertion sort has two loops: The outer for loop that always runs n - 1 times, and the inner while loop that runs 1 to i - 1 times depending on the contents of the array. Since i is at most n, the inner while loop runs at most n - 1 times. Since everything else runs at constant time, that means the algorithm as a whole has (n - 1)^2 iterations, giving us O(n^2) time (in other words, the function is guaranteed to stay below n^2) for all inputs.

Ω(n)
For worst-case inputs, Ω is also Ω(n^2). Keep in mind, however, that this doesn't mean that all inputs are like this. Just that the worst are.

All we need to do to prove Ω(n^2) is prove that the function takes at least Ω(n^2) actions.

Now think of the worst-case input where the array is in reverse sorted order. Let's assume that the length of the array is a multiple of three for simplicity's sake. Now split the array into thirds and take a look at the first third. Since this is a worst-case input, we know that all of the keys in the first third actually belong in the last third. 

For them to get to the last third, each key must move at least n/3 places to the right. Since there are n/3 keys moving n/3 places to the right, this tells us that the alg will take at least (n^2)/9 moves.

Therefore, insertion sort is Ω(n^2).

Θ(n)
Because insertion sort runs in both O(n^2) and Ω(n^2) time in the worst cases, it runs in Θ(n^2) time in the worst cases.

