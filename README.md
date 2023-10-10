# Data-Structures-and-Algorithms-Specialisation
My solution for the Data Structures and algorithms specialisation on Coursera:
https://www.coursera.org/specializations/data-structures-algorithms

Here are my notes from the specialisation:

## Course 1. Algorithmic Toolbox
#### Fibonacci Numbers
$$F_n = F_{n-1} + F_{n-2}$$
with $F_0 = 0$ and $F_1 = 1$
1. Fibonacci numbers grow rapidly: $F_n \geq 2^{n/2}$ for $n \geq 6$.
2. Naive algorithm using recursion leads to a tree of recursive calls. $T_n = = T_{n-1} + T_{n-2} + c$ for $n>1$. Grows the same way as Fibonacci numbers themselves - exponentially.
3. Improved algorithm using iterative approach. O(n) complexity.

#### Greatest Common Divisor
1. Naive Algorithm $T(a,b) = O(min(a, b))$
2. Lemma: Let $a'$ be the remainder when a is divided by b. Then, $GCD(a,b) = GCD(a',b) = GCD(b, a')$
3. Euclidean Algorithm is based on this lemma. Takes $log(ab)$ steps.

#### Compute  Runtimes
1. Actual runtime of a program on a computer depends on things like speed of the computer, system architecture, compiler used and details of memory hierarchy of the machine.
2. Key Idea - All these issues can multiply runtimes by (possibly large) constant. So, measure runtimes in a way that ignores constant multiples.
3. It is thus helpful to see how the algorithm scales with the input size - ASYMPTOTIC RUNTIMES.
4. Big O notation: $f(n) = O(g(n))$ means $f$ is bounded above by $g$.
5. $f(n) = \Omega(g(n))$ means $f$ is bounded below by $g$.
6. $f(n) = \Theta(g(n))$ means $f$ grows at the same rate as $g$.
$$log(n) \prec \sqrt n \prec n \prec n*log(n) \prec n^a \prec b^n$$
where $a > 0$ and $b>1$

### Greedy Algorithms
1. **Greedy Strategy:**
    1. Make a safe move: A greedy choice is called a safe move if there is an optimal solution consistent with this first move
    2. Reduce to smaller sub-problem
    3. Iterate

2. Example problems:
* **Largest number** that can be constructed using the digits in an array.
    * Naive solution: $ O(n!) $
    * Safe move: Choose the largest number to put at the most significant digit
    * Greedy solution: $ O(nlog(n)) $
* **Car fueling problem** minimising the number of refills.
    * Naive solution: $ O(2^n) $
    * Safe move: choose the farthest reachable gas station.
    * Greedy solution: $ O(n) $
* **Celebration Party problem:** Many children come to a celebration. Organise them into a minimum possible number of groups such that any 2 children in the same group differ by a maximum of x years.
    * Naive solution: $ \Omega(2^n) $
    * Safe move: If we represent each child as a point on the number line, the safe move is to cover the leftmost point with a segment of length x with left end at this point.
    * Greedy solution: $ O(nlog(n)) $
* **Fractional Knapsack problem:** We have n items with given weights and values. Given a bag which can carry a maximum weight W, if we can keep fractions of items, what items should we keep in what portion?
    * Safe move: Keep as much as possible of the item with the maximal value per unit weight.
    * Greedy solution: $ O(nlog(n)) $





