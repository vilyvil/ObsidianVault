| Term           | Definition                             |
| -------------- | -------------------------------------- |
| Keys           | The things we want to sort             |
| Satellite Data | Data associated with individual keys   |
| Record         | Keys and Satellite Data taken together |
# Ex.
Spreadsheet contains student records with age, grades, courses. You can sort the students by any of these numbers, and of course their other data should follow. The whole record should be sorted along with the keys.

## Loop Invariant
Loop invariants help us show how an algorithm is correct. 

A property of a program loop that is true before and after a loop is run.
To show that something is loop invariant, you need to show three things:
1. Initialization: True before first iteration
2. Maintenance: If it is true before an iteration it remains true after
3. Termination: When the loop terminates the invariant gives us useful information as to why the algorithm is correct

Proving that a property is loop invariant is like doing an inductive proof. First you prove the base case (it's true before iteration) then you prove inductive step (it's true on each iteration). The place where it differs, however, is that our loop will terminate but mathematical induction goes on forever.

For insertion sort:
1. Initialization: When i = 2 (at the beginning of the loop), the left subarray consists of only one value. So, it is sorted.
2. Maintenance: We know that after each iteration the left subarray stays sorted since we specifically decided to insert values in the correct place. Therefore, the subarray stays sorted.
3. Termination: When the loop terminates, i = n + 1. Therefore the subarray is now A\[1:n], which is the same size as the original array. Since we know the subarray has been sorted the whole time, we know that the whole array is sorted now.

In this way, since the subarray being sorted the whole time is a loop invariant, we use it to show that the whole array itself sorted in the end.