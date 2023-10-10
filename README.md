# Data-Structures-and-Algorithms-Specialisation
My solution for the Data Structures and algorithms specialisation on Coursera

Here are some of my key takeaways from the specialisation:

## Course 1. Algorithmic Toolbox
#### Fibonacci Numbers
$$F_n = F_{n-1} + F_{n-2}$$
with $F_0 = 0$ and $F_1 = 1$
1. Fibonacci numbers grow rapidly: $ F_n \geq 2^{n/2} $ for $ n \geq 6$.
2. Naive algorithm using recursion leads to a tree of recursive calls. $ T_n = = T_{n-1} + T_{n-2} + c$ for $n>1$. Grows the same way as Fibonacci numbers themselves - exponentially.
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
$$ log(n) \prec \sqrt n \prec n \prec n*log(n) \prec n^a \prec b^n$$
where $a > 0$ and $b>1$

