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

## 2. Sliding Window [(view)](https://www.youtube.com/shorts/3V8YcmxtRLQ)

-   Q: from the given array which of 4 length has the highest sum.
    -   here instead of calculating the values if index [0 1 2 3], [1 2 3 4], [2 3 4 5], ...
    -   we can **reduce** the removing value & **add** the new value.
    -   This can be very efficient when the window length gets larger.
-   ![Sliding Window](imgs/sliding%20window.png)
-   Where to use Sliding Window:
    -   Array, sub-array
    -   String, sub-string
    -   maximum sum, minimum sum

## 3. K-Way merge [(view)](https://www.youtube.com/watch?v=vO961e332A4)

-   Falls under merge algos.
-   Used to merge multiple sorted arrays into one sorted array.
-   This algo will use the concept of divide & conquer.
-   Behavior of algorithm:
    1. Get the main array that contains K number of arrays.
    2. Divide the array into individual arrays.
    3. Couple 2 arrays and start comparing.
        - a pointer on 0th index of each 2 arrays.
        - Compare which val is smaller, & select it.
        - increase the index of selected array.
        - Continue & get the final sorted array.
    4. Combine the reset of arrays 2 by 2 & get the final sorted array.

## 4. Sorting algorithms [(view)](https://www.geeksforgeeks.org/sorting-algorithms/)

-   A method to reorganizing number of items into a specific order.
-   Top 5 sorting algos:
    1. Bubble sort
    2. Insertion sort
    3. Selection sort
    4. Merge sort
    5. Quick sort

## 5. Graph algorithms

-   [view article](https://towardsdatascience.com/10-graph-algorithms-visually-explained-e57faa1336f3)
-   **What's a Graph?**
    -   A graph consists of a set of vertices/nodes and a set of edges connecting these vertices.
    -   ![Graphs](imgs/graphs.png)

#### 1. BFS [(view)](https://www.youtube.com/watch?v=HZ5YTanv5QE)

-   Breadth-First Search is a Traversing algo.
-   Since breath = broad/wide, this algo will process **horizontally**, level by level.
-   A queue is used to keep track of visited nodes.
-   Application:
    -   determine shortest path.
    -   Minimum spanning tree.

#### 2. DFS [(view)](https://www.youtube.com/watch?v=Urx87-NMm6c)

-   Depth-First Search is also a Traversing algo.
-   Depth = **vertical** before horizontal, will travel branch by branch.
-   A stack is used to keep track of visited nodes.
-   Application:
    -   Finding paths between 2 nodes.
    -   detecting cycle in graph.
    -   topological sorting

#### 3. Minimum spanning tree

##### What is Spanning tree?

-   A graph which stays connected with minimum no of edges. (cover all vertices with minimum no of edges)
-   Spanning tree is a subset of graph. It’s minimally connected, removing 1 edge will disconnect graph.
-   ST can not be disconnected
-   if original graph no of vertices = V then no of edges of ST = V-1
-   A connected & undirected graph has at least 1 ST.
-   A complete(every node is connected w/ every other nodes) undirected graph has N(n-2) no of ST.

##### What is Minimum Spanning tree?

-   A spanning tree with min cost in a weighted graph.
-   **Example**: Cable company laying line to multiple neighbors with minimum cable length.
-   in below STs the Minimum ST will be the graph with total weight of 30.
    -   cause 30< 40< 50
    -   ![Minimum Spanning Tree](imgs/Minimum-spanning-tree.png)

##### Popular MST algorithms?

1.  **Prim's algo**

    -   [Prim's algorithm in 2 minutes - YouTube](https://www.youtube.com/watch?v=cplfcGZmX7I)
    -   Steps:
        -   start with a root node.
        -   and follows the smallest weighted edge, which has not connected to a node that’ve visited .
        -   Finally the MST.

2.  **Kruskal’s algo**

    -   [Kruskal's algorithm in 2 minutes - YouTube](https://www.youtube.com/watch?v=71UQH7Pr9kU)
    -   Steps:
        -   Sort the graph edges based on weight.
        -   find the smallest weighted edge, & highlight the edge with connected 2 nodes.
        -   find the next smallest edge, which has not connected to a node that’ve visited before.
        -   finally the MST.

-   Prims vs Kruskal’s
    -   lots of edges ⇒ Prims is faster
    -   Both are greedy algo.
    -   Prims → having a tree that continually add to until it becomes a MST.
    -   Kruskal’s → Having a disconnected graph until a tree is formed.

## 6. Shortest-path/Path-finding algorithms

-   These algorithms are used to find the shortest path between 2 points.
-   [A Comparison of Pathfinding Algorithms - YouTube](https://www.youtube.com/watch?v=GC-nBgi9r0U)
-   There are 2 types of Shortest path algos:
    -   **Single-source**:
        -   from a given node to all other
        -   Dijkstra algorithm, Bellman-Ford Algorithm
    -   **All-pairs**:
        -   between every pair of nodes.
        -   Floyd Warshall Algorithm, Johnson's Algorithm

#### 1. Dijkstra algorithm [(view)](https://www.youtube.com/watch?v=EFg3u_E6eHU)

-   Shortest-path from 1 : all, negative edges not allowed.
-   is a Greedy algo.
-   Steps: ![Dijkstra algo steps](https://raw.githubusercontent.com/kdn251/interviews/master/images/dijkstra.gif)

#### 2. Bellman-Ford algorithm

-   Shortest-path from 1 : all, negative edges allowed.
-   Steps: https://youtu.be/obWXjtg0L64?t=32

#### 3. Floyd Warshall algorithm

-   Shortest-path from all : all, negative edges allowed.
-   Can be used to find the shortest path between every node.
-   ![Floyd Warshall Algorithm](imgs/Floyd%20Warshall%20Algorithm.png)

#### 4. A\* algorithm

-   Best on average
-   Use concept of ‘Potential reweighing’

## 7. Greedy algorithms

-   Greedy algos are quick decision makers. Solves problems fast.
-   Grabs the "best" choice right away without reconsidering.
-   Example algos:
    -   Dijkstra's algo
    -   Kruskal's algo
    -   Fractional Knapsack
-   Advantages:
    -   easy to understand.
    -   Much faster
-   Disadvantages
    -   Might miss the perfect answer.
    -   forced on immediate wins.
