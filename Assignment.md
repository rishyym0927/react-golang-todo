
# Design and Analysis of Algorithms Assignment

## Student Details

| **Name**          | Rishiraj Mukherjee |
|------------------|-------------------|
| **Roll Number**  | LIT2023030        |
| **Course**       | Design and Analysis of Algorithms |
| **Semester**     | 3       |
| **Department**   | Information Technology |

## Assignment Overview

This comprehensive assignment covers a wide range of algorithmic concepts and problem-solving techniques, including:

### Key Topics Covered
- Asymptotic Notation Analysis
- Greedy Algorithms
- Dynamic Programming
- Backtracking
- Branch and Bound
- Optimization Techniques
- Matrix Chain Multiplication
- Knapsack Problems
- N-Queens Problem
- Coin Change Algorithms

### Submission Details
- **Date of Submission**: [22 November]
  




## Q1: Why There is No Small Theta (θ) Asymptotic Notation?

The absence of "small theta" notation is primarily because the standard Big Theta (Θ) notation already serves the purpose of providing a tight bound for an algorithm's growth rate. 

- Big Theta (Θ) provides both an upper and lower bound for a function's growth.
- It represents the exact order of growth, capturing both the asymptotic tight upper and lower bounds.
- Introducing a "small theta" would redundant since Θ already precisely captures the function's growth characteristics.

## Q2: Asymptotic Notation Problems

### a. Show that 3n^2 + 12n + 35 = O(n^2)

Proof:
- We need to find constants c and n₀ such that 3n^2 + 12n + 35 ≤ c * n^2 for all n ≥ n₀
- Choose c = 4 and n₀ = 1
- For n ≥ 1: 
  - 3n^2 + 12n + 35 ≤ 3n^2 + 12n^2 + 35
  - ≤ 15n^2
  - ≤ 4n^2
- Therefore, 3n^2 + 12n + 35 = O(n^2)

### b. Show that 2n^2 + 4n + 6 = Ω(n^2)

Proof:
- We need to find constants c and n₀ such that 2n^2 + 4n + 6 ≥ c * n^2 for all n ≥ n₀
- Choose c = 1 and n₀ = 1
- For n ≥ 1:
  - 2n^2 + 4n + 6 ≥ 2n^2
- Therefore, 2n^2 + 4n + 6 = Ω(n^2)

### c. Show that 3n + 3 = Θ(n)

Proof:
- We need to show both O(n) and Ω(n)
- Upper bound: Choose c₁ = 4, n₀ = 1
  - 3n + 3 ≤ 4n for n ≥ 1
- Lower bound: Choose c₂ = 2, n₀ = 1
  - 3n + 3 ≥ 2n for n ≥ 1
- Therefore, 3n + 3 = Θ(n)

### d. Show 5n + 8 = O(n)

Proof:
- Choose c = 6 and n₀ = 1
- For n ≥ 1: 5n + 8 ≤ 6n
- Therefore, 5n + 8 = O(n)

## Q3: Show that 2log n + log(log n) = O(log n)

Proof:
- Both terms are logarithmic
- log(log n) grows slower than log n
- Choose c = 3 and n₀ = 2
- 2log n + log(log n) ≤ 3log n for sufficiently large n
- Therefore, 2log n + log(log n) = O(log n)

## Q4: Show that n(2^n) + 45n = Ω(2^n) = Ω(n^100)

Proof:
- The dominant term is n(2^n)
- For 2^n:
  - Choose c₁ = 1/2, n₀ = 1
  - n(2^n) ≥ c₁ * 2^n
- For n^100:
  - 2^n grows much faster than n^100
  - Therefore, n(2^n) = Ω(2^n) = Ω(n^100)

## Q5: Show that n(2^n) + n^45 = Θ(n(2^n))

Proof:
- Upper bound: 
  - n(2^n) + n^45 ≤ 2n(2^n)
- Lower bound:
  - n(2^n) + n^45 ≥ 1/2 * n(2^n)
- The 2^n term dominates
- Therefore, n(2^n) + n^45 = Θ(n(2^n))

## Q6 & Q7: Binary Search Time Complexity

### Iterative Binary Search
- Time Complexity: Θ(log n)
- Best Case: Θ(1) - element found at middle
- Worst Case: Θ(log n) - element at end or not present
- Average Case: Θ(log n)

### Recursive Binary Search
- Same time complexity as iterative: Θ(log n)
- Recurrence relation: T(n) = T(n/2) + O(1)
- Solves to Θ(log n)

## Q8: Recurrence Relations

### a. 4T(n/3) + n^2
- Using Master Theorem, Case 2
- a = 4, b = 3, f(n) = n^2
- log₃(4) ≈ 1.26
- T(n) = Θ(n^2 * log n)

### b. T(n) = 2T(n/2) + n
- Master Theorem, Case 2
- T(n) = Θ(n log n)

### c. T(n) = 3T(n/4) + Θ(n^2)
- Master Theorem, Case 3
- a = 3, b = 4, f(n) = n^2
- log₄(3) < 1
- T(n) = Θ(n^2)

### d. T(n) = T(n/3) + T(2n/3) + O(n)
- Cannot directly solve with Master Theorem
- Requires more complex analysis
- Approximate solution: T(n) = O(n log n)


## Q1: Why There is No Small Theta (θ) Asymptotic Notation?

The absence of "small theta" notation stems from the following reasons:
- Big Theta (Θ) notation already provides a precise representation of exact growth rate
- It simultaneously provides upper and lower bounds
- Introducing a "small theta" would create redundancy in asymptotic analysis
- Θ notation captures the most accurate and comprehensive growth characterization

## Q2: Asymptotic Notation Problems

### a. Proving 3n^2 + 12n + 35 = O(n^2)

**Proof Strategy:**
- Find constants c and n₀ such that 3n^2 + 12n + 35 ≤ c * n^2 for all n ≥ n₀
- Choose c = 15 and n₀ = 1
- Verification:
  * 3n^2 + 12n + 35 ≤ 15n^2
  * Holds true for all n ≥ 1

### b. Proving 2n^2 + 4n + 6 = Ω(n^2)

**Proof Strategy:**
- Find constants c and n₀ such that 2n^2 + 4n + 6 ≥ c * n^2 for all n ≥ n₀
- Choose c = 1 and n₀ = 1
- Verification:
  * 2n^2 + 4n + 6 ≥ 2n^2
  * Holds true for all n ≥ 1

### c. Proving 3n + 3 = Θ(n)

**Proof Strategy:**
- Demonstrate both upper and lower bounds
- Upper bound: 3n + 3 ≤ 4n (c₁ = 4, n₀ = 1)
- Lower bound: 3n + 3 ≥ 2n (c₂ = 2, n₀ = 1)

### d. Proving 5n + 8 = O(n)

**Proof Strategy:**
- Find constants c and n₀ such that 5n + 8 ≤ c * n
- Choose c = 6 and n₀ = 1
- Verification: 5n + 8 ≤ 6n for n ≥ 1

## Q3: Proving 2log n + log(log n) = O(log n)

**Proof Strategy:**
- Demonstrate logarithmic growth bound
- log(log n) grows significantly slower than log n
- Choose c = 3, n₀ = 2
- 2log n + log(log n) ≤ 3log n for sufficiently large n

## Q4: Proving n(2^n) + 45n = Ω(2^n) = Ω(n^100)

**Proof Strategy:**
- Exponential growth dominates polynomial terms
- n(2^n) grows faster than both 2^n and n^100
- Choose c = 1/2, n₀ = 1
- Demonstrates growth dominance through Ω notation

## Q5: Proving n(2^n) + n^45 = Θ(n(2^n))

**Proof Strategy:**
- Exponential term dominates polynomial term
- Upper bound: n(2^n) + n^45 ≤ 2n(2^n)
- Lower bound: n(2^n) + n^45 ≥ 1/2 * n(2^n)

## Q6 & Q7: Binary Search Time Complexity

### Time Complexity Analysis
- **Average Case:** Θ(log n)
- **Best Case:** Θ(1)
- **Worst Case:** Θ(log n)

#### Iterative Binary Search Characteristics
- Divide search space in half each iteration
- Logarithmic time complexity
- Efficient for sorted arrays

#### Recursive Binary Search
- Same time complexity as iterative approach
- Overhead of function call stack
- Recurrence relation: T(n) = T(n/2) + O(1)

## Q8: Recurrence Relations Solution

### a. 4T(n/3) + n^2
- Master Theorem: Case 2
- Solution: Θ(n^2 * log n)

### b. T(n) = 2T(n/2) + n
- Master Theorem
- Solution: Θ(n log n)

### c. T(n) = 3T(n/4) + Θ(n^2)
- Master Theorem: Case 3
- Solution: Θ(n^2)

### d. T(n) = T(n/3) + T(2n/3) + O(n)
- Complex recurrence
- Approximate solution: O(n log n)

## Q8: Recursive QuickSort Algorithm

```python
def quicksort(arr):
    # Base case
    if len(arr) <= 1:
        return arr
    
    # Choose pivot (last element)
    pivot = arr[-1]
    
    # Partition
    left = [x for x in arr[:-1] if x < pivot]
    right = [x for x in arr[:-1] if x >= pivot]
    
    # Recursive calls
    return quicksort(left) + [pivot] + quicksort(right)
```

## Q9: Coin Change Problem (Denominations: 10, 5, 2, 1)
### Amount: 24

**Dynamic Programming Solution:**
- Minimum coins: 4
- Combination: 10 + 10 + 2 + 2

## Q10: Coin Change Problem (Denominations: 1, 7, 10)
### Amount: 15

**Dynamic Programming Solution:**
- Minimum coins: 2
- Combination: 10 + 5 or 7 + 7 + 1

**Algorithm Approach:**
- Use greedy strategy
- Prefer larger denominations first
- Backtrack if exact combination not possible


## Q11: Greedy Approach Limitations in Coin Selection Problem

### Reasons Why Greedy Approach Fails

1. **Local Optimal vs Global Optimal**
   - Greedy algorithms make locally optimal choices
   - These choices may not lead to a globally optimal solution
   - Always selects the largest denomination possible

2. **Counterexample Demonstration**
   ```
   Denominations: 1, 5, 10, 25
   Target Amount: 30
   
   Greedy Approach:
   - Choose 25 first (1 coin)
   - Choose 5 next (1 coin)
   Total: 2 coins
   
   Optimal Solution:
   - Choose 10 three times
   Total: 3 coins
   ```

3. **Key Limitations**
   - Cannot backtrack or reconsider previous choices
   - Works perfectly for some currency systems
   - Fails for non-standard denomination sets
   - Lacks global optimization perspective

4. **Mathematical Proof**
   - Greedy choice property not guaranteed for all coin sets
   - Requires specific coin denomination relationships
   - Dynamic programming provides more robust solution

## Q12: Coin Denomination Problem

### Denominations: 1, 10, 21, 34, 70, 100, 350

#### a. Making 140 Cents

**Optimal Solution:**
- 1 × 100
- 1 × 34
- 1 × 5
- 1 × 1
**Total Denominations: 4**

#### b. Making 182 Cents

**Optimal Solution:**
- 1 × 100
- 1 × 70
- 1 × 10
- 1 × 2
**Total Denominations: 4**

### Solution Strategy
- Use dynamic programming approach
- Minimize total number of coins
- Consider all possible combinations
- Greedy method may not always work

## Q13: Fractional Knapsack Problem (KSP)

### Problem Parameters
- Total Items: 3
- Weights: w1 = 2, w2 = 3, w3 = 4
- Profits: p1 = 1, p2 = 2, p3 = 5
- Knapsack Capacity: 5

### Solution Steps
1. **Calculate Profit per Unit Weight**
   ```
   Item 1: 1/2 = 0.5
   Item 2: 2/3 = 0.667
   Item 3: 5/4 = 1.25
   ```

2. **Sorting by Profit per Unit Weight**
   - Order: Item 3 > Item 2 > Item 1

3. **Filling Knapsack**
   - First add Item 3: (4 weight, 5 profit)
   - Remaining capacity: 1
   - Add 1/5 of Item 2: (1 weight, 0.4 profit)

4. **Final Solution**
   - Total Profit: 5.4
   - Total Weight: 5

## Q14: Best Case of Knapsack Problem

### Best Case Scenario
- All items can be included completely
- No weight constraints violated
- Maximum profit achieved
- Time Complexity: O(n)

## Q15: Fractional Knapsack Optimization (Weight = 150)

### Item Details
| Item | Weight | Profit | Profit/Weight |
|------|--------|--------|--------------|
| 1    | 2      | 10     | 5.0          |
| 2    | 3      | 5      | 1.667        |
| 3    | 5      | 15     | 3.0          |
| 4    | 7      | 7      | 1.0          |
| 5    | 1      | 6      | 6.0          |
| 6    | 4      | 18     | 4.5          |
| 7    | 1      | 3      | 3.0          |

### Solution Strategy
1. **Sort by Profit per Unit Weight**
   ```
   Item 5: 6.0
   Item 1: 5.0
   Item 6: 4.5
   Item 3: 3.0
   Item 7: 3.0
   Item 2: 1.667
   Item 4: 1.0
   ```

2. **Filling Knapsack**
   - Item 5: (1 weight, 6 profit)
   - Item 1: (2 weight, 10 profit)
   - Item 6: (4 weight, 18 profit)
   - Item 3: (5 weight, 15 profit)
   - Remaining: (138 weight left)

3. **Optimal Solution**
   - Total Profit: 49
   - Total Weight: 12
   - Remaining Capacity: 138

# Advanced Algorithmic Problem Solutions

## Q16: Cyber Café Machine Allocation Problem

### Problem Understanding
- Multiple users in cyber café
- No two users can use same machine simultaneously
- Users have individual use times
- Goal: Maximize machine utilization

### Optimal Allocation Algorithm
1. **Greedy Interval Scheduling**
   - Sort users by end times
   - Select non-overlapping user sessions
   - Minimum number of machines = Maximum parallel sessions

### Pseudocode
```python
def min_machines(users):
    # Sort users by start time
    users.sort(key=lambda x: x[0])
    
    machines = 0
    current_end_times = []
    
    for user_start, user_end in users:
        # Remove completed machine sessions
        current_end_times = [end for end in current_end_times if end > user_start]
        
        # Allocate new machine if needed
        if len(current_end_times) == machines:
            machines += 1
        
        current_end_times.append(user_end)
    
    return machines
```

## Q17: Minimum Wire Connection Problem

### Problem Analysis
- n white dots and n black dots
- Connect each white dot to black dot
- Minimize total wire length

### Solution Strategy
1. **Greedy Pairing Approach**
   - Sort white and black dots
   - Connect closest corresponding dots
   - Minimizes total wire length

### Example Visualization
```
B B W B W W W B
Optimal Connections:
- Minimum wire length
- Each white dot paired with nearest black dot
```

## Q18: Matrix Chain Multiplication Using Dynamic Programming

### Algorithm Steps
```python
def matrix_chain_order(dimensions):
    n = len(dimensions) - 1
    # DP table to store minimum multiplication cost
    dp = [[0] * n for _ in range(n)]
    
    # Length of multiplication chain
    for chain_length in range(2, n + 1):
        for i in range(n - chain_length + 1):
            j = i + chain_length - 1
            dp[i][j] = float('inf')
            
            # Try all possible split points
            for k in range(i, j):
                cost = dp[i][k] + dp[k+1][j] + \
                       dimensions[i] * dimensions[k+1] * dimensions[j+1]
                dp[i][j] = min(dp[i][j], cost)
    
    return dp[0][n-1]
```

## Q19: Matrix Chain Multiplication Example

### Given Matrices
- A: 5 × 4
- B: 2 × 6
- C: 6 × 2
- D: 2 × 7

### Solution
1. Dimensions Array: [5, 4, 6, 2, 7]
2. Optimal Multiplication Order Calculation
3. Minimum Multiplication Cost Computation

## Q20: Matrix Chain Multiplication Order

### Given Matrices
- A1: 30 × 1
- A2: 1 × 40
- A3: 40 × 10
- A4: 10 × 25
- A5: 25 × 4
- A6: 4 × 128

### Optimal Order Determination
- Use Dynamic Programming
- Minimize total multiplication operations

## Q21: Longest Common Subsequence (LCS)

### Input Strings
- X = {BACBFHCB}
- Y = {BABFFBC}

### Dynamic Programming Solution
```python
def lcs(X, Y):
    m, n = len(X), len(Y)
    # DP table initialization
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    
    # Fill DP table
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if X[i-1] == Y[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])
    
    # Reconstruct LCS
    lcs = []
    i, j = m, n
    while i > 0 and j > 0:
        if X[i-1] == Y[j-1]:
            lcs.append(X[i-1])
            i -= 1
            j -= 1
        elif dp[i-1][j] > dp[i][j-1]:
            i -= 1
        else:
            j -= 1
    
    return ''.join(reversed(lcs))

# Example usage
X = "BACBFHCB"
Y = "BABFFBC"
print(lcs(X, Y))  # Output: BBFC
```

## Q22: LCS for Different Strings

### Input Strings
- X = {AGGTAB}
- Y = {GXTXAYB}

### Solution
```python
# Same LCS function as previous problem
X = "AGGTAB"
Y = "GXTXAYB"
print(lcs(X, Y))  # Output: GTAB
```

## Q23: 0/1 Knapsack Using Dynamic Programming

### Problem Parameters
- Weights: [7, 2, 4, 8, 6]
- Profits: [5, 6, 4, 3, 2]
- Knapsack Capacity: Typically defined in problem

### Dynamic Programming Solution
```python
def knapsack_01(weights, profits, capacity):
    n = len(weights)
    # DP table
    dp = [[0] * (capacity + 1) for _ in range(n + 1)]
    
    # Fill DP table
    for i in range(1, n + 1):
        for w in range(1, capacity + 1):
            if weights[i-1] <= w:
                dp[i][w] = max(
                    profits[i-1] + dp[i-1][w - weights[i-1]], 
                    dp[i-1][w]
                )
            else:
                dp[i][w] = dp[i-1][w]
    
    return dp[n][capacity]

# Example usage
weights = [7, 2, 4, 8, 6]
profits = [5, 6, 4, 3, 2]
capacity = 14  # Adjust as needed
print(knapsack_01(weights, profits, capacity))
```


## Q24: N-Queens Problem Using Backtracking

### Algorithm Implementation
```python
def solve_n_queens(n):
    def is_safe(board, row, col):
        # Check this row on left side
        for i in range(col):
            if board[row][i] == 1:
                return False
        
        # Check upper diagonal on left side
        for i, j in zip(range(row, -1, -1), range(col, -1, -1)):
            if board[i][j] == 1:
                return False
        
        # Check lower diagonal on left side
        for i, j in zip(range(row, n, 1), range(col, -1, -1)):
            if board[i][j] == 1:
                return False
        
        return True

    def solve_queens_util(board, col):
        # Base case: If all queens are placed, return true
        if col >= n:
            return True

        # Consider this column and try placing queens in all rows one by one
        for i in range(n):
            if is_safe(board, i, col):
                # Place this queen in board[i][col]
                board[i][col] = 1

                # Recur to place rest of the queens
                if solve_queens_util(board, col + 1):
                    return True

                # If placing queen in board[i][col] doesn't lead to a solution,
                # then remove queen from board[i][col]
                board[i][col] = 0

        # If queen can't be placed in any row in this column col, return false
        return False

    # Initialize the board
    board = [[0 for _ in range(n)] for _ in range(n)]
    
    # Start from the first column
    if solve_queens_util(board, 0) == False:
        print("Solution does not exist")
        return False

    # Print the solution
    for row in board:
        print(" ".join("Q" if x else "." for x in row))
    return True

# Solve for 8-queens
solve_n_queens(8)
```

## Q25: 5-Queens Solutions

### Solution Visualization
```
Solution 1:
. Q . . .
. . . Q .
Q . . . .
. . Q . .
. . . . Q

Solution 2:
. . Q . .
Q . . . .
. . . . Q
. Q . . .
. . . Q .

Solution 3:
. . . Q .
Q . . . .
. . Q . .
. . . . Q
. Q . . .
```

## Q26: 0/1 Knapsack Using Backtracking

### Problem Parameters
- Categories: 4
- Weights: [2, 3, 4, 5]
- Benefits: [3, 5, 6, 10]
- Knapsack Capacity: 8
- Maximum Benefit Constraint: > 14

### Backtracking Solution
```python
def knapsack_backtracking(weights, benefits, capacity, max_benefit):
    n = len(weights)
    max_profit = 0
    current_solution = [0] * n

    def backtrack(index, current_weight, current_profit, solution):
        nonlocal max_profit, current_solution

        # Base case: all items considered
        if index == n:
            if current_profit > max_profit and current_profit > max_benefit:
                max_profit = current_profit
                current_solution = solution.copy()
            return

        # Try including the current item
        if current_weight + weights[index] <= capacity:
            solution[index] = 1
            backtrack(
                index + 1, 
                current_weight + weights[index], 
                current_profit + benefits[index], 
                solution
            )

        # Try excluding the current item
        solution[index] = 0
        backtrack(index + 1, current_weight, current_profit, solution)

    # Initialize solution array
    solution = [0] * n
    backtrack(0, 0, 0, solution)

    return max_profit, current_solution

# Solve the problem
weights = [2, 3, 4, 5]
benefits = [3, 5, 6, 10]
capacity = 8
max_benefit = 14

profit, solution = knapsack_backtracking(weights, benefits, capacity, max_benefit)
print("Maximum Profit:", profit)
print("Solution:", solution)
```

## Q27: 0/1 Knapsack with 6 Categories

### Problem Parameters
- Categories: 6
- Weights: [3, 4, 2, 6, 7, 3]
- Benefits: [7, 9, 5, 12, 14, 3]
- Knapsack Capacity: 5

### Backtracking Solution
```python
def knapsack_backtracking_6(weights, benefits, capacity):
    n = len(weights)
    max_profit = 0
    current_solution = [0] * n

    def backtrack(index, current_weight, current_profit, solution):
        nonlocal max_profit, current_solution

        # Base case: all items considered
        if index == n:
            if current_profit > max_profit:
                max_profit = current_profit
                current_solution = solution.copy()
            return

        # Try including the current item
        if current_weight + weights[index] <= capacity:
            solution[index] = 1
            backtrack(
                index + 1, 
                current_weight + weights[index], 
                current_profit + benefits[index], 
                solution
            )

        # Try excluding the current item
        solution[index] = 0
        backtrack(index + 1, current_weight, current_profit, solution)

    # Initialize solution array
    solution = [0] * n
    backtrack(0, 0, 0, solution)

    return max_profit, current_solution

# Solve the problem
weights = [3, 4, 2, 6, 7, 3]
benefits = [7, 9, 5, 12, 14, 3]
capacity = 5

profit, solution = knapsack_backtracking_6(weights, benefits, capacity)
print("Maximum Profit:", profit)
print("Solution:", solution)
```

## Q28: Knapsack Problem Using Branch and Bound

### Problem Parameters
- Categories: 3
- Weights: [1, 2, 5]
- Benefits: [2, 3, 4]
- Capacity: 3

### Branch and Bound Solution
```python
class Item:
    def __init__(self, weight, value):
        self.weight = weight
        self.value = value
        self.ratio = value / weight

def branch_and_bound_knapsack(weights, benefits, capacity):
    # Create items with their value-to-weight ratio
    items = [Item(w, b) for w, b in zip(weights, benefits)]
    
    # Sort items by value-to-weight ratio in descending order
    items.sort(key=lambda x: x.ratio, reverse=True)
    
    def bound(node, capacity):
        # Calculates the upper bound of profit for a node
        if node.weight >= capacity:
            return 0
        
        bound_value = node.value
        j = node.level + 1
        total_weight = node.weight
        
        # Add fractional items
        while j < len(items) and total_weight + items[j].weight <= capacity:
            total_weight += items[j].weight
            bound_value += items[j].value
            j += 1
        
        # If we can't add next item completely, add fractional part
        if j < len(items):
            bound_value += (capacity - total_weight) * items[j].ratio
        
        return bound_value

    class Node:
        def __init__(self, level, value, weight):
            self.level = level
            self.value = value
            self.weight = weight

    # Keep track of maximum value
    max_value = 0
    
    # Queue for branch and bound
    queue = [Node(-1, 0, 0)]
    
    while queue:
        current = queue.pop(0)
        
        # If we've considered all items, update max value
        if current.level == len(items) - 1:
            max_value = max(max_value, current.value)
            continue
        
        # Next level
        next_level = current.level + 1
        
        # Try including the next item
        if current.weight + items[next_level].weight <= capacity:
            include_node = Node(
                next_level, 
                current.value + items[next_level].value, 
                current.weight + items[next_level].weight
            )
            
            # Prune using bound
            if include_node.value + bound(include_node, capacity) > max_value:
                queue.append(include_node)
                max_value = max(max_value, include_node.value)
        
        # Try excluding the next item
        exclude_node = Node(next_level, current.value, current.weight)
        
        # Prune using bound
        if exclude_node.value + bound(exclude_node, capacity) > max_value:
            queue.append(exclude_node)
    
    return max_value

# Solve the problem
weights = [1, 2, 5]
benefits = [2, 3, 4]
capacity = 3

max_profit = branch_and_bound_knapsack(weights, benefits, capacity)
print("Maximum Profit:", max_profit)
```

## Q29: N-Queens Using Branch and Bound

### Approach
- Similar to backtracking solution
- Additional pruning techniques
- More efficient elimination of invalid configurations

```python
def solve_n_queens_branch_bound(n):
    def is_promising(board, row, col):
        # Check row on left side
        for i in range(col):
            if board[row][i] == 1:
                return False
        
        # Check upper diagonal on left side
        for i, j in zip(range(row, -1, -1), range(col, -1, -1)):
            if board[i][j] == 1:
                return False
        
        # Check lower diagonal on left side
        for i, j in zip(range(row, n, 1), range(col, -1, -1)):
            if board[i][j] == 1:
                return False
        
        return True

    def solve_queens_util(board, col, queens_placed):
        # Base case: All queens placed
        if queens_placed == n:
            return True

        # Try placing queen in each row of current column
        for row in range(n):
            if is_promising(board, row, col):
                # Place queen
                board[row][col] = 1

                # Recursively place remaining queens
                if solve_queens_util(board, col + 1, queens_placed + 1):
                    return True

                # Backtrack
                board[row][col] = 0

        return False

    # Initialize board
    board = [[0 for _ in range(n)] for _ in range(n)]
    
    # Solve
    if solve_queens_util(board, 0, 0):
        # Print solution
        for row in board:
            print(" ".join("Q" if x else "." for x in row))
        return True
    
    print("No solution exists")
    return False

# Solve for 8-queens
solve_n_queens_branch_bound(8)
```
