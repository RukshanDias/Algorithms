# Algorithms

## Concepts

-   #### Brute force

    -   Brute Force is a way to find the correct solutions by checking all the possible solutions.
    -   Ideal for solving small, simpler problems.
    -   But for large problems, this can be inefficient & slow.

-   #### Divide & Conquer [(view)](https://www.youtube.com/watch?v=YOh6hBtX5l0)

    -   This concept can divide into 3 parts,
        1. Divide - divide problem into sub-problems
        2. Conquer - Solve sub-problems recursively until solved.
        3. Combine - combine solved sub-problems to get the final solution.
    -   ![Divide & Conquer](imgs/divide%20&%20conquer.png)
    -   Divide & Conquer vs Dynamic Programming:
        -   D&C should be used when the same sub-problems are not evaluated many times
        -   Otherwise DP/memoization.
    -   Advantages:
        -   Parallelism: Sub-problems can be solved parallelly.
        -   Memory access: sub-problems are small enough to solve in cache, which is fast than main-memory. So it's a [cache oblivious algorithm](https://www.geeksforgeeks.org/cache-oblivious-algorithm/)
    -   Disadvantages:

        -   Complexity - Dividing a problem into smaller sub-problems can increase the complexity.
        -   Memory limitations - On larger dataset, storing results of sub-problems can be a limiting factor.

    -   Applications:
        -   Merge, Quick sort
        -   Strassen’s Algorithm
        -   binary search

-   #### Dynamic Programming [(View)](https://github.com/RukshanDias/Dynamic-Programming)

    -   A programming technique where an algorithmic problem is first broken down into sub-problems, & sub-problems are use to find the optimal solution.

    -   Memoization - store duplicate sub problems, so it can be reused when it occurs again.

    -   Applications: Fibonacci series

-   #### Backtracking
    -   Backtracking is an algorithm that use **brute force** approach to find the desired output.
    -   If the current solution is not suitable, then backtrack and try other solutions. This involves **Recursion**.
    -   Backtracking vs Dynamic Programming:
        -   Use BT if the problem have multiple solutions.
        -   If there's an optimal solution go for DP.
            ![Backtracking](imgs/backtracking.png)
    -   Types of Backtracking:
        -   Decision problem: search for a feasible solution.
        -   Optimization problem: search for the best solution.
        -   Enumeration problem: find all feasible solutions.
    -   Applications:
        -   n-queen problem
        -   The Knight's tour problem.

---

## 1. Two Pointers

-   This technique is used for searching pairs in a sorted array.
-   Behavior of algorithm:
    -   Q: find any numbers that sum is 50.
    1. set two pointers, one on the 0th index & one on the last index.
    2. Get the sum of 2 nums which're in pointers.
    3. if sum>50 ? reduce right/high pointer from 1 index : else, increase left/low pointer from 1 index.
    4. again check sum & continue.
-   ![two pointers](imgs/two%20pointers.png)

## 2. Sliding Window

## 3. K-Way merge

## 4. Greedy algorithms

## 5. Sorting algorithms

-   Top 5 main algos:
    1. Selection sort
    2. Insertion sort
    3. Bubble sort
    4. Merge sort
    5. Quick sort

## 6. Graph algorithms

    - BFS
    - DFS
    - Dijkstra algorithm
    - Floyd Warshall Algorithm
    - Bellman-Ford Algorithm
    - Prim’s algorithm
    - Kruskal’s algorithm

## 7. Shortest-path algorithms
