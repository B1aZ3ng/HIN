Big O efficiency
- Measures the upper bound of an algorithm's efficiency focusing on the worst case scenario
- It is used to measure the efficiency of an algorithm measure the efficiency of an algorithm in terms of the number of operation required to complete a task
- can be Time Complexity and Space Complexity
## Calculation Big O
To calculate the time complexity, consider how many operations of the algorithm changes with the size of the input

1. Count the no. of poerations. Identify the main operations of the algorithm and use these as a base of ur calculation
2. Ignore anything that is constant or ouside the algorithm, - so no input(), print() or anything that doesnt interact with input
3. Change the input size and count no. operations
	- if no change: O(1)
	- if increases proportionally: O(n)
	- if increases quadratically O(n^2)
	- if run time doubles with every linear increase of the input size: O(2^n)
	- if scales logarithmically: O(log n)

