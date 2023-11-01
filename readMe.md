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

-   #### Dynamic Programming
-   #### Backtracking

## 1. Two Pointers

## 2. K-Way merge

## 3. Sliding Window

## 4. Greedy

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
