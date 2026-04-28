# IGCSE 0606 Additional Mathematics Complete Notes (English)

> These notes are based on the Cambridge IGCSE Additional Mathematics (0606) 2025-2027 syllabus, arranged in a cognitive order covering all topics. Includes derivations, typical examples, and common pitfalls. Suitable for self-study.

---

## Table of Contents

- [Chapter 1: Sequences, Permutations, Combinations and Binomial Theorem](#chapter-1-sequences-permutations-combinations-and-binomial-theorem)
- [Chapter 2: Vectors and Rates of Change](#chapter-2-vectors-and-rates-of-change)
- [Chapter 3: Quadratic Functions](#chapter-3-quadratic-functions)
- [Chapter 4: Functions (Linear, Cubic, Exponential, Logarithmic)](#chapter-4-functions-linear-cubic-exponential-logarithmic)
- [Chapter 5: Differentiation (Derivatives)](#chapter-5-differentiation-derivatives)
- [Chapter 6: Equations and Inequalities (Graphical Method)](#chapter-6-equations-and-inequalities-graphical-method)
- [Chapter 7: Integration (Indefinite and Definite Integrals)](#chapter-7-integration-indefinite-and-definite-integrals)
- [Chapter 8: Trigonometry](#chapter-8-trigonometry)
- [Chapter 9: Geometry (Straight Lines and Circles)](#chapter-9-geometry-straight-lines-and-circles)
- [Chapter 10: Comprehensive Applications](#chapter-10-comprehensive-applications)

---

# Chapter 1: Sequences, Permutations, Combinations and Binomial Theorem

This chapter is placed first for two reasons. First, it serves as an intellectual warm-up to train your algebraic manipulation skills and logical counting abilities before diving into more abstract calculus topics. Second, by covering sequences, counting, and the binomial theorem early, we will not need to interrupt later chapters when these topics are needed as tools.

---

## 1.1 Sequences – What Are They?

A sequence is simply an ordered list of numbers. For example, you might see 3, 7, 11, 15, … where each number follows a clear pattern. In mathematics, we are especially interested in two common types of sequences: **arithmetic sequences** (where we add the same fixed value each time) and **geometric sequences** (where we multiply by the same fixed value each time).

Before we study these in depth, let us first understand the notation we use for adding up the terms of a sequence.

### The Summation Symbol ∑

The Greek letter ∑ (sigma) tells us to add up a series of numbers. When we write

$$
∑_{k=1}^{n} a_k
$$

it means "add up all the numbers $a_k$ starting from $k=1$ and going up to $k=n$". In other words:

$$
∑_{k=1}^{n} a_k = a_1 + a_2 + a_3 + ... + a_n
$$

There are three basic rules that make working with sums much easier:

**Rule 1 – Constant factor**: If every term is multiplied by a constant $c$, we can pull that constant outside the sum. That is:

$$
∑ (c \cdot a_k) = c \cdot ∑ a_k
$$

**Rule 2 – Sum or difference**: Adding or subtracting two sequences term by term can be split into separate sums:

$$
∑ (a_k \pm b_k) = ∑ a_k \pm ∑ b_k
$$

**Rule 3 – Sum of a constant**: If we add the same constant $c$ over and over, $n$ times, the result is simply $n$ times that constant:

$$
∑_{k=1}^{n} c = n c
$$

Let us see these rules in action with a concrete example.

**Example**: Evaluate $∑_{k=1}^{4} (2k + 1)$.

We can split this into two separate sums:

$$
∑_{k=1}^{4} (2k + 1) = 2∑_{k=1}^{4} k + ∑_{k=1}^{4} 1
$$

The first sum is $2 \times (1 + 2 + 3 + 4) = 2 \times 10 = 20$. The second sum is $1 + 1 + 1 + 1 = 4$. Adding them gives $20 + 4 = 24$.

---

## 1.2 Arithmetic Sequences

### What Makes a Sequence Arithmetic?

An arithmetic sequence has a very simple defining property: starting from the second term, each term minus the previous term always equals the same constant. We call this constant the **common difference** and denote it by $d$. In symbols:

$$
a_{n+1} - a_n = d
$$

**Example**: Consider the sequence 3, 7, 11, 15, 19. If we subtract each term from the one that follows it, we get $7-3=4$, $11-7=4$, $15-11=4$, $19-15=4$. The common difference is $d=4$.

### Finding Any Term in the Sequence

Suppose the first term is $a$ (we usually denote $a_1 = a$). Then:

- The second term is $a_2 = a + d$
- The third term is $a_3 = a + 2d$
- The fourth term is $a_4 = a + 3d$

Do you see the pattern? For the $n$-th term, we add $d$ exactly $(n-1)$ times. So the formula for the $n$-th term is:

$$
a_n = a + (n-1)d
$$

Let us check: when $n=1$, the formula gives $a_1 = a + 0\cdot d = a$, which is correct.

**Example**: If the first term is $a=5$ and the common difference is $d=3$, what is the 10th term? Using the formula:

$$
a_{10} = 5 + (10-1)\times 3 = 5 + 27 = 32
$$

### Adding Up the First n Terms (The Sum Formula)

How do we find the sum of the first $n$ terms of an arithmetic sequence? Instead of memorizing the formula blindly, let us derive it – understanding the derivation will help you remember it forever.

Write the sum $S$ twice, once in the normal order and once in reverse order:

Forward: $S = a + (a+d) + (a+2d) + ... + (a+(n-1)d)$

Backward: $S = (a+(n-1)d) + (a+(n-2)d) + ... + a$

Now add these two equations term by term. Look at the first pair: $a + (a+(n-1)d) = 2a + (n-1)d$. The second pair: $(a+d) + (a+(n-2)d) = 2a + (n-1)d$. In fact, every pair adds up to exactly the same value: $2a + (n-1)d$. There are $n$ such pairs, so:

$$
2S = n \cdot [2a + (n-1)d]
$$

Dividing both sides by 2 gives us the sum formula:

$$
S_n = \frac{n}{2}[2a + (n-1)d]
$$

A useful alternative form: if we know the last term $l = a + (n-1)d$, then:

$$
S_n = \frac{n}{2}(a + l)
$$

**Example**: Find the sum of the arithmetic sequence 3, 7, 11, 15, 19.

Here $a=3$, $d=4$, and $n=5$. Plugging into the formula:

$$
S_5 = \frac{5}{2}[2\cdot 3 + (5-1)\cdot 4] = \frac{5}{2}[6 + 16] = \frac{5}{2} \times 22 = 55
$$

You can verify this by adding directly: $3+7+11+15+19 = 55$.

---

## 1.3 Geometric Sequences

### What Makes a Sequence Geometric?

In a geometric sequence, instead of adding a fixed number each time, we multiply by a fixed number. This fixed multiplier is called the **common ratio** and is denoted by $r$. In symbols:

$$
\frac{a_{n+1}}{a_n} = r
$$

**Example**: Look at the sequence 2, 6, 18, 54, … Dividing each term by the previous term gives $6/2=3$, $18/6=3$, $54/18=3$. So the common ratio is $r=3$.

### Finding Any Term in a Geometric Sequence

If the first term is $a$, then:

- The second term is $a_2 = a r$
- The third term is $a_3 = a r^2$
- The fourth term is $a_4 = a r^3$

For the $n$-th term, we multiply by $r$ a total of $(n-1)$ times:

$$
a_n = a r^{\,n-1}
$$

**Example**: If $a=2$ and $r=3$, what is the 5th term?

$$
a_5 = 2 \cdot 3^{4} = 2 \cdot 81 = 162
$$

### Adding Up the First n Terms

Let us derive the sum formula for a geometric sequence. Write out the sum:

$$
S = a + ar + ar^2 + ... + ar^{\,n-1}
$$

Now multiply both sides by $r$:

$$
rS = ar + ar^2 + ar^3 + ... + ar^{\,n}
$$

Subtract the second equation from the first. Notice that all the middle terms cancel:

$$
S - rS = a - ar^{\,n}
$$

Factor both sides:

$$
S(1 - r) = a(1 - r^n)
$$

If $r = 1$, then every term is just $a$, and the sum is simply $S_n = n a$.

If $r \neq 1$, we can divide both sides by $(1-r)$:

$$
S_n = a\frac{1-r^n}{1-r}
$$

**Example**: Find the sum of the first 4 terms of 2, 6, 18, 54.

Here $a=2$, $r=3$, $n=4$:

$$
S_4 = 2 \cdot \frac{1-3^4}{1-3} = 2 \cdot \frac{1-81}{-2} = 2 \cdot \frac{-80}{-2} = 80
$$

### Infinite Sum (When the Ratio is Between -1 and 1)

What happens if we keep adding terms forever? For a geometric sequence with common ratio $r$ satisfying $|r| < 1$, as $n$ gets larger and larger, $r^n$ gets closer and closer to 0. This means the sum approaches a finite limit:

$$
S_\infty = \frac{a}{1-r}
$$

This formula only works when $|r| < 1$. If $|r| \geq 1$, the terms either stay the same size or grow, and the sum diverges (goes to infinity).

**Example**: Consider the infinite sum $1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + ...$

Here $a=1$ and $r = 1/2$. Since $|1/2| < 1$, we can use the formula:

$$
S_\infty = \frac{1}{1 - 1/2} = \frac{1}{1/2} = 2
$$

This makes intuitive sense: if you keep adding half of what remains, you approach 2 but never quite reach it.

### A Special Type: Recurrence Relations of the Form $u_{n+1} = a u_n + b$

Sometimes a sequence is defined by a rule like $u_{n+1} = 3 u_n - 4$ with a starting value $u_1$. This is not purely arithmetic or geometric, but we can turn it into a geometric sequence using a clever trick.

The idea is to find a fixed point $p$ such that if the sequence ever reaches $p$, it stays there. We solve $p = a p + b$, which gives $p = b/(1-a)$, provided $a \neq 1$.

Now define a new sequence $v_n = u_n - p$. What happens when we compute $v_{n+1}$?

$$
v_{n+1} = u_{n+1} - p = (a u_n + b) - p = a(u_n - p) + (a p + b - p)
$$

Since $p = a p + b$, the term in parentheses equals 0, and we get:

$$
v_{n+1} = a v_n
$$

This is a geometric sequence! So $v_n = v_1 \cdot a^{\,n-1}$, and therefore:

$$
u_n = p + (u_1 - p) a^{\,n-1}
$$

**Example**: Let $u_1 = 2$ and $u_{n+1} = 3 u_n - 4$. Find $p$ by solving $p = 3p - 4$, which gives $2p = 4$, so $p = 2$. Then $v_n = u_n - 2$, and $v_1 = 2 - 2 = 0$. Since $v_1 = 0$, we have $v_n = 0$ for all $n$, so $u_n = 2$ (the sequence is constant).

> **Caution**: If $a = 1$, the recurrence becomes $u_{n+1} = u_n + b$, which is arithmetic – do not use the method above. Instead, handle it as an arithmetic sequence.

---

## 1.4 Permutations and Combinations

These two concepts answer one fundamental question: "How many ways can we choose or arrange things?" The key difference between them is whether **order matters** or not.

### 1.4.1 The Multiplication Principle (The Foundation of Counting)

Before we talk about permutations and combinations, we need to understand the most basic counting rule. Suppose a task can be broken down into a sequence of steps. If step 1 can be done in $m_1$ ways, step 2 in $m_2$ ways, and so on up to step $k$ in $m_k$ ways, then the total number of ways to complete the entire task is:

$$
m_1 \times m_2 \times ... \times m_k
$$

**Example**: Suppose there are 3 different roads from town A to town B, and 4 different roads from town B to town C. How many different routes can you take to go from A to C passing through B? By the multiplication principle, the answer is $3 \times 4 = 12$ routes.

### 1.4.2 Permutations – When Order Matters

A permutation is an arrangement of items where the order is important. For example, lining up students for a photo, creating passwords, or ranking contestants in a competition.

Suppose we have $n$ distinct items and we want to choose $r$ of them and arrange them in a specific order. The number of ways to do this is called $P(n, r)$.

Think about it step by step:
- For the first position, we have $n$ choices.
- For the second position, we have $n-1$ choices left.
- For the third position, we have $n-2$ choices left.
- ...
- For the $r$-th position, we have $n-r+1$ choices left.

Multiplying all these together:

$$
P(n, r) = n(n-1)(n-2)...(n-r+1)
$$

This can be written more compactly using factorials:

$$
P(n, r) = \frac{n!}{(n-r)!}
$$

where $n!$ (read as "n factorial") means $n \times (n-1) \times (n-2) \times ... \times 2 \times 1$.

**Example**: You have 5 different books and you want to choose 3 of them to place on a shelf from left to right (order matters). How many different arrangements are possible?

$$
P(5, 3) = 5 \times 4 \times 3 = 60
$$

### 1.4.3 Combinations – When Order Does Not Matter

A combination is a selection of items where the order does not matter. For example, choosing members for a committee, picking lottery numbers, or selecting players for a team.

The number of ways to choose $r$ items from $n$ distinct items (without regard to order) is denoted by $C(n, r)$ or $\binom{n}{r}$. The formula is:

$$
C(n, r) = \binom{n}{r} = \frac{n!}{r!(n-r)!}
$$

Why does this formula make sense? Notice that if order did matter, there would be $P(n, r) = n!/(n-r)!$ ways. But since order does not matter, each group of $r$ items could be arranged in $r!$ different orders. So we divide by $r!$ to remove the overcounting:

$$
C(n, r) = \frac{P(n, r)}{r!} = \frac{n!}{r!(n-r)!}
$$

**Example**: Choose 2 people out of 5 to clean a room (no roles assigned, so order does not matter).

$$
C(5, 2) = \frac{5!}{2! \times 3!} = \frac{5 \times 4}{2 \times 1} = 10
$$

### When to Use Which?

| Scenario | Order Matters? | Example |
|----------|----------------|---------|
| Queue, ranking, password | Yes (Permutation) | Choose 3 from 10 to stand in a line – $P(10,3)$ |
| Committee, lottery, team | No (Combination) | Choose 3 from 10 to join a contest – $C(10,3)$ |

### Special Cases: Circular and Repeated Permutations

**Circular permutations**: When arranging $n$ distinct objects around a circle, rotations are considered the same arrangement. To handle this, fix one person's position (to break the rotational symmetry) and arrange the remaining $n-1$ people relative to that fixed position. The number of ways is:

$$
(n-1)!
$$

**Example**: 5 people sitting around a circular table can be arranged in $(5-1)! = 24$ ways.

**Permutations with repetition**: If we choose $r$ items from $n$ types where repetition is allowed (like a PIN code where each digit can be any number 0-9), the number of possibilities is:

$$
n^r
$$

**Example**: A 4-digit PIN (each digit from 0 to 9) has $10^4 = 10000$ possible combinations.

### A Brief Connection to Probability

We can use combinations to calculate simple probabilities. Two important rules:

- **Mutually exclusive events** (cannot happen at the same time): $P(A \cup B) = P(A) + P(B)$
- **Independent events** (one does not affect the other): $P(A \cap B) = P(A) \cdot P(B)$

**Example**: A group has 5 boys and 3 girls. If we choose 2 people at random, what is the probability that at least one is a girl?

Total ways to choose any 2 people from 8: $C(8,2) = 28$.

Ways to choose 2 people with no girls (i.e., both boys): $C(5,2) = 10$.

The probability of "at least one girl" equals 1 minus the probability of "no girls":

$$
P = 1 - \frac{10}{28} = \frac{18}{28} = \frac{9}{14}
$$

> **Tip**: For "at least" problems, it is often easier to use the complement (1 minus the opposite case).

---

## 1.5 The Binomial Theorem

### Where Do the Coefficients Come From?

Have you ever wondered why expanding $(a+b)^2$ gives $a^2 + 2ab + b^2$, and $(a+b)^3$ gives $a^3 + 3a^2b + 3ab^2 + b^3$? Where do the numbers 1, 2, 1 and 1, 3, 3, 1 come from?

Think of $(a+b)^n$ as multiplying $n$ brackets together: $(a+b)(a+b)...(a+b)$. When we expand, each term comes from choosing either $a$ or $b$ from each bracket. To get a term like $a^{\,n-r}b^{\,r}$, we need to choose $b$ from exactly $r$ of the brackets and $a$ from the remaining $n-r$ brackets.

The number of ways to choose which $r$ brackets contribute $b$ is exactly $C(n, r) = \binom{n}{r}$. Therefore:

$$
(a+b)^n = \sum_{r=0}^{n} \binom{n}{r} a^{\,n-r} b^{\,r}
$$

This is the **binomial theorem**, and it works for any non-negative integer $n$.

### A Step-by-Step Example

Expand $(x+2)^3$:

- $r=0$: $\binom{3}{0} x^3 \cdot 2^0 = 1 \cdot x^3 = x^3$
- $r=1$: $\binom{3}{1} x^2 \cdot 2^1 = 3 \cdot 2 \cdot x^2 = 6x^2$
- $r=2$: $\binom{3}{2} x^1 \cdot 2^2 = 3 \cdot 4 \cdot x = 12x$
- $r=3$: $\binom{3}{3} x^0 \cdot 2^3 = 1 \cdot 8 = 8$

Adding them up: $(x+2)^3 = x^3 + 6x^2 + 12x + 8$.

### The General Term

The $(r+1)$-th term in the expansion (starting counting from $r=0$) is:

$$
T_{r+1} = \binom{n}{r} a^{\,n-r} b^{\,r}
$$

This is useful when we only need a specific term rather than the whole expansion.

### Application: Finding a Constant Term

**Example**: Find the constant term in the expansion of $(2x - \frac{1}{x})^6$.

Write the expression as $(2x + (-1/x))^6$, with $a = 2x$ and $b = -1/x$.

The general term is:

$$
\binom{6}{r} (2x)^{6-r} \left(-\frac{1}{x}\right)^r = \binom{6}{r} 2^{6-r} (-1)^r x^{6-r} \cdot x^{-r} = \binom{6}{r} 2^{6-r} (-1)^r x^{6-2r}
$$

For the term to be constant (no $x$), the exponent of $x$ must be 0: $6-2r = 0$, so $r=3$.

Plugging $r=3$ into the general term:

$$
\binom{6}{3} 2^{3} (-1)^3 = 20 \times 8 \times (-1) = -160
$$

So the constant term is $-160$.

### Important Distinction

- The **binomial coefficient** $\binom{n}{r}$ depends only on $n$ and $r$, not on the actual values of $a$ and $b$.
- The **coefficient of a term** in the expansion is the full numerical factor, including signs and constants from $a$ and $b$.

For example, in $(2x - 1/x)^6$, the coefficient of the constant term is $-160$, while the binomial coefficient for $r=3$ is $\binom{6}{3} = 20$.

---

## 1.6 Properties of Binomial Coefficients (Pascal's Triangle)

Binomial coefficients have two beautiful properties:

**Symmetry**: 

$$
\binom{n}{r} = \binom{n}{n-r}
$$

This makes sense because choosing $r$ items to include is the same as choosing $n-r$ items to exclude.

**Pascal's Rule (Recurrence)**:

$$
\binom{n}{r} + \binom{n}{r-1} = \binom{n+1}{r}
$$

This holds for $1 \leq r \leq n$.

Pascal's Triangle arranges these coefficients in a triangular shape. Each row corresponds to a value of $n$, and each number inside the triangle is the sum of the two numbers directly above it:

```
        1
       1 1
      1 2 1
     1 3 3 1
    1 4 6 4 1
   1 5 10 10 5 1
```

Notice how the coefficients match the binomial expansions we saw earlier.

---

## 1.7 Chapter Summary

Here are the key formulas and concepts from this chapter:

**Arithmetic Sequences**:
- Common difference $d$: $a_{n+1} - a_n = d$
- $n$-th term: $a_n = a + (n-1)d$
- Sum of $n$ terms: $S_n = \frac{n}{2}[2a + (n-1)d]$ or $S_n = \frac{n}{2}(a + l)$ where $l$ is the last term

**Geometric Sequences**:
- Common ratio $r$: $a_{n+1} / a_n = r$
- $n$-th term: $a_n = a r^{\,n-1}$
- Sum of $n$ terms: $S_n = \frac{a(1-r^n)}{1-r}$ (if $r \neq 1$), or $S_n = na$ (if $r=1$)
- Infinite sum (when $|r| < 1$): $S_\infty = \frac{a}{1-r}$

**Permutations** (order matters): $P(n,r) = \frac{n!}{(n-r)!}$

**Combinations** (order does not matter): $\binom{n}{r} = \frac{n!}{r!(n-r)!}$

**Binomial Theorem**: 
$$
(a+b)^n = \sum_{r=0}^{n} \binom{n}{r} a^{\,n-r} b^{\,r}
$$

**Binomial Coefficient Properties**:
- $\binom{n}{r} = \binom{n}{n-r}$ (symmetry)
- $\binom{n}{r} + \binom{n}{r-1} = \binom{n+1}{r}$ (Pascal's rule)

---

# Chapter 2: Vectors and Rates of Change

## 2.1 Why Start with Vectors?

In physics, quantities like position, velocity, and acceleration all have both magnitude and direction. These are best described using **vectors**. The concept of **rate of change** is the core idea of calculus – the rate of change of position is velocity, and the rate of change of velocity is acceleration. Vectors give us a geometric way to understand rates of change.

---

## 2.2 Basic Vector Concepts

### 2.2.1 What is a Vector?

A vector is a quantity that has both magnitude (size) and direction. In a two-dimensional plane, we can write a vector using its horizontal and vertical components:

$$
\mathbf{v} = (v_x, v_y)
$$

Alternatively, we can use the unit vectors $\mathbf{i}$ and $\mathbf{j}$, where $\mathbf{i} = (1,0)$ points to the right and $\mathbf{j} = (0,1)$ points upward:

$$
\mathbf{v} = v_x \mathbf{i} + v_y \mathbf{j}
$$

### 2.2.2 Magnitude (Length)

The magnitude (or length) of a vector $\mathbf{v} = (v_x, v_y)$ is found using the Pythagorean theorem:

$$
\|\mathbf{v}\| = \sqrt{v_x^2 + v_y^2}
$$

**Example**: The magnitude of $(3, 4)$ is $\sqrt{9 + 16} = \sqrt{25} = 5$.

### 2.2.3 Unit Vector

A unit vector is a vector with magnitude 1 that points in the same direction as the original vector. To find it, divide the vector by its magnitude:

$$
\mathbf{u} = \frac{\mathbf{v}}{\|\mathbf{v}\|}
$$

**Example**: The unit vector in the direction of $(3, 4)$ is $(3/5, 4/5)$.

### 2.2.4 Vector Operations

**Addition**: To add two vectors, add their corresponding components:

$$
(x_1, y_1) + (x_2, y_2) = (x_1 + x_2, y_1 + y_2)
$$

Geometrically, this follows the parallelogram law.

**Subtraction**: The vector from point $A$ to point $B$ is:

$$
\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A
$$

Remember: "tip minus tail" – the vector from $A$ to $B$ is the position of $B$ minus the position of $A$.

**Scalar Multiplication**: Multiplying a vector by a scalar $c$ stretches (or shrinks) it:

$$
c(x, y) = (cx, cy)
$$

If $c > 0$, the direction stays the same; if $c < 0$, the direction reverses.

**Example**: Let $\mathbf{u} = (1, 2)$ and $\mathbf{v} = (3, -1)$. Then:
- $\mathbf{u} + \mathbf{v} = (4, 1)$
- $\mathbf{u} - \mathbf{v} = (-2, 3)$
- $2\mathbf{u} = (2, 4)$

### Perpendicular Vectors

Two non-zero vectors $\mathbf{u}$ and $\mathbf{v}$ are perpendicular (orthogonal) if and only if their dot product equals zero:

$$
\mathbf{u} \cdot \mathbf{v} = u_x v_x + u_y v_y = 0
$$

Geometrically, this means the angle between them is $90^\circ$.

### Horizontal and Vertical Vectors

A horizontal vector has a zero $y$-component: $\mathbf{h} = (h_x, 0)$ with $h_x \neq 0$. Its direction is parallel to the $x$-axis.

A vertical vector has a zero $x$-component: $\mathbf{v} = (0, v_y)$ with $v_y \neq 0$.

A horizontal vector is always perpendicular to a vertical vector. You can check this with the dot product: $(h_x, 0) \cdot (0, v_y) = 0 + 0 = 0$.

### Perpendicularity via Slopes

If both vectors are non-zero and neither is vertical, we can also check perpendicularity using slopes. If the slopes are $k_1$ and $k_2$, then:

$$
\mathbf{u} \perp \mathbf{v} \iff k_1 \cdot k_2 = -1
$$

> Note: The zero vector is technically both perpendicular and parallel to every vector, but we usually exclude it from discussion.

---

## 2.3 Position Vector and Displacement

### 2.3.1 Position Vector

Take a fixed origin point $O$. The position of any point $P$ is given by the vector $\mathbf{r} = \overrightarrow{OP}$. If $P$ has coordinates $(x, y)$, then:

$$
\mathbf{r} = (x, y)
$$

It is important to distinguish between a point and a position vector: $P(x, y)$ is a location in space, while $\mathbf{r} = (x, y)$ is the vector from the origin to that point.

### 2.3.2 Displacement

The displacement from point $A$ to point $B$ is the vector that takes you from $A$ to $B$:

$$
\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A
$$

**Example**: If $A = (1, 1)$ and $B = (4, 5)$, then the displacement from $A$ to $B$ is $(4-1, 5-1) = (3, 4)$, and its magnitude is $5$.

---

## 2.4 From Average Velocity to Instantaneous Velocity (Understanding Limits)

Let us explore the idea of instantaneous velocity through a concrete example. Suppose an object moves along a straight line, and its position at time $t$ is given by $s(t) = t^2$. We want to know how fast it is moving at the exact moment $t = 1$.

### How Do We Calculate Average Velocity?

From time $1$ to time $1 + \Delta t$, the distance traveled is $s(1+\Delta t) - s(1)$. The average velocity over this interval is the distance divided by the time interval:

$$
\text{Average velocity} = \frac{s(1+\Delta t) - s(1)}{\Delta t}
$$

Let us try making $\Delta t$ smaller and smaller to see what happens:

- $\Delta t = 0.5$: position goes from 1 to 2.25, distance = 1.25, average velocity = $1.25 / 0.5 = 2.5$
- $\Delta t = 0.1$: position goes from 1 to 1.21, distance = 0.21, average velocity = $0.21 / 0.1 = 2.1$
- $\Delta t = 0.01$: position goes from 1 to 1.0201, distance = 0.0201, average velocity = $0.0201 / 0.01 = 2.01$
- $\Delta t = 0.001$: average velocity ≈ 2.001

Do you see the pattern? As $\Delta t$ gets closer and closer to 0, the average velocity gets closer and closer to 2. This "closer value" is what we call the **instantaneous velocity** at $t = 1$. We write $v(1) = 2$.

This is the fundamental idea of a **limit**: we never let $\Delta t$ become exactly 0 (because that would give $0/0$, which is meaningless), but we let it approach 0 and observe what number the average velocity approaches.

In general, for a position vector $\mathbf{r}(t)$, the instantaneous velocity is:

$$
\mathbf{v}(t) = \lim_{\Delta t \to 0} \frac{\mathbf{r}(t+\Delta t) - \mathbf{r}(t)}{\Delta t} = \left( \frac{dx}{dt}, \frac{dy}{dt} \right)
$$

And the acceleration is the rate of change of velocity:

$$
\mathbf{a}(t) = \frac{d\mathbf{v}}{dt} = \left( \frac{d^2 x}{dt^2}, \frac{d^2 y}{dt^2} \right)
$$

---

## 2.5 From Acceleration to Velocity and Position (Using Integration)

In physics, acceleration $a(t)$ is the rate of change of velocity $v(t)$. If we know the acceleration and want to recover the velocity, we need to do the opposite of differentiation – this is called **integration**.

The basic relationships are:

- Velocity $v(t) = \int a(t) \, dt + v_0$ (where $v_0$ is the initial velocity)
- Position $r(t) = \int v(t) \, dt + r_0$ (where $r_0$ is the initial position)

If we know the acceleration $\mathbf{a}(t)$ and the initial conditions $\mathbf{v}(0) = \mathbf{v}_0$ and $\mathbf{r}(0) = \mathbf{r}_0$, then:

$$
\mathbf{v}(t) = \int \mathbf{a}(t) \, dt + \mathbf{v}_0
$$

$$
\mathbf{r}(t) = \int \mathbf{v}(t) \, dt + \mathbf{r}_0
$$

Integration is performed component by component.

### Example: Projectile Motion

A ball is thrown from the ground. Its initial velocity has a horizontal component $v_{0x}$ and a vertical component $v_{0y}$. Gravity pulls downward with acceleration $g$. So the acceleration vector is $\mathbf{a}(t) = (0, -g)$.

First, integrate acceleration to get velocity:

- $v_x(t) = \int 0 \, dt = v_{0x}$ (constant, since no horizontal acceleration)
- $v_y(t) = \int (-g) \, dt = -g t + v_{0y}$

So $\mathbf{v}(t) = (v_{0x}, v_{0y} - g t)$.

Next, integrate velocity to get position, starting from $(0, 0)$:

- $x(t) = \int v_{0x} \, dt = v_{0x} \cdot t$
- $y(t) = \int (v_{0y} - g t) \, dt = v_{0y} \cdot t - \frac{1}{2} g t^2$

These are the well-known equations of projectile motion.

---

## 2.6 Relative Motion (Adding Velocities)

When you stand on the ground and watch a moving object, its velocity is actually the sum of two parts: the object's velocity relative to a moving reference frame, plus the velocity of that reference frame itself.

The simple rule is:

$$
\mathbf{v}_{A/C} = \mathbf{v}_{A/B} + \mathbf{v}_{B/C}
$$

In words: the velocity of $A$ relative to $C$ equals the velocity of $A$ relative to $B$ plus the velocity of $B$ relative to $C$.

**Example**: A boat can move at 4 m/s east relative to the water. The water current flows north at 3 m/s. What is the boat's velocity relative to the ground?

Let east be the positive $x$-direction and north be the positive $y$-direction.

Boat's velocity relative to water: $(4, 0)$
Water's velocity relative to ground: $(0, 3)$
Boat's velocity relative to ground: $(4, 0) + (0, 3) = (4, 3)$

Magnitude: $\sqrt{4^2 + 3^2} = 5$ m/s
Direction: at an angle $\arctan(3/4) \approx 36.87^\circ$ east of north.

---

## 2.7 More Examples to Help You Practice

**Example 1: Given position, find velocity and acceleration**

A particle moves with position vector $\mathbf{r}(t) = (t^3 - 3t, t^2 - 2t)$.

Velocity is the derivative of position (differentiate each component):

$$
v_x = 3t^2 - 3,\quad v_y = 2t - 2
$$

So $\mathbf{v}(t) = (3t^2 - 3, 2t - 2)$.

Acceleration is the derivative of velocity:

$$
a_x = 6t,\quad a_y = 2
$$

So $\mathbf{a}(t) = (6t, 2)$.

At $t = 2$: $\mathbf{v} = (9, 2)$ and $\mathbf{a} = (12, 2)$.

**Example 2: Given acceleration and initial conditions, find motion**

Acceleration $\mathbf{a}(t) = (6t, 4)$, initial velocity $\mathbf{v}_0 = (1, 0)$, initial position $\mathbf{r}_0 = (0, 0)$.

Integrate to get velocity:

- $\int 6t \, dt = 3t^2$, plus the initial $x$-component $1 \rightarrow v_x = 3t^2 + 1$
- $\int 4 \, dt = 4t$, plus the initial $y$-component $0 \rightarrow v_y = 4t$

So $\mathbf{v}(t) = (3t^2 + 1, 4t)$.

Then integrate velocity to get position:

- $\int (3t^2 + 1) \, dt = t^3 + t$, plus initial $x = 0 \rightarrow x = t^3 + t$
- $\int 4t \, dt = 2t^2$, plus initial $y = 0 \rightarrow y = 2t^2$

Thus $\mathbf{r}(t) = (t^3 + t, 2t^2)$.

**Example 3: One-dimensional motion (simpler)**

Displacement $s(t) = 3t^2 - 2t + 1$.
Velocity $v(t) = 6t - 2$.
Acceleration $a(t) = 6$.

---

## 2.8 Chapter Summary

In this chapter we started with vectors and saw that position, velocity, and acceleration can all be represented as vectors.

- Average velocity = change in position divided by time interval. When the time interval approaches zero, the limit of the average velocity is the **instantaneous velocity**.
- Velocity is the derivative (rate of change) of position; acceleration is the derivative of velocity.
- Going in reverse: given acceleration, we can use **integration** to find velocity; given velocity, we can integrate to find position.
- For relative motion: absolute velocity = relative velocity + velocity of the reference frame.
- The zero vector has no fixed direction, but by convention it is considered parallel to every vector.

If some of the differentiation or integration steps feel unfamiliar, do not worry – they will be explained in detail in Chapters 5 and 7. For now, just focus on understanding the relationships between position, velocity, and acceleration.

---

# Chapter 3: Quadratic Functions

## 3.1 Forms and Graph

A quadratic function has the form $f(x) = ax^2 + bx + c$ where $a \neq 0$. Its graph is a parabola.

- If $a > 0$, the parabola opens upward (like a U shape).
- If $a < 0$, the parabola opens downward (like an upside-down U).

The vertex (the highest or lowest point) is located at:

$$
x = -\frac{b}{2a},\quad y = f\left(-\frac{b}{2a}\right)
$$

The axis of symmetry is the vertical line $x = -\frac{b}{2a}$.

**Example**: For $f(x) = 2x^2 - 4x + 1$, the vertex $x$-coordinate is $x = 4/4 = 1$, and $y = 2 - 4 + 1 = -1$. So the vertex is at $(1, -1)$.

## 3.2 Vertex and Range

We can rewrite a quadratic function by **completing the square**:

$$
f(x) = a\left(x + \frac{b}{2a}\right)^2 + \frac{4ac - b^2}{4a}
$$

The range depends on the direction of opening:

- If $a > 0$, the range is $[f_{\min}, \infty)$.
- If $a < 0$, the range is $(-\infty, f_{\max}]$.

**Example**: $f(x) = x^2 - 4x + 3 = (x-2)^2 - 1$. The vertex is at $(2, -1)$, and since $a=1>0$, the range is $[-1, \infty)$.

## 3.3 Discriminant and Roots

For the equation $ax^2 + bx + c = 0$, the discriminant is:

$$
\Delta = b^2 - 4ac
$$

The value of $\Delta$ tells us about the roots:

- $\Delta > 0$: two distinct real roots
- $\Delta = 0$: one repeated root (also called a double root)
- $\Delta < 0$: no real roots

**Example**: $x^2 - 3x + 2 = 0$ has $\Delta = 9 - 8 = 1 > 0$, so there are two distinct real roots: $x = 1$ and $x = 2$.

## 3.4 Quadratic Inequalities

To solve an inequality like $ax^2 + bx + c > 0$ (or $< 0$):

1. Find the roots of the corresponding equation $ax^2 + bx + c = 0$.
2. Determine the sign of the quadratic expression in each interval created by the roots.
3. The sign pattern depends on whether $a > 0$ (parabola opens up) or $a < 0$ (parabola opens down).

**Example**: Solve $x^2 - 4x + 3 > 0$.

Factor: $(x-1)(x-3) > 0$. The roots are $x = 1$ and $x = 3$. Since $a = 1 > 0$, the parabola opens up, so the expression is positive outside the interval between the roots. Therefore, $x < 1$ or $x > 3$.

---

# Chapter 4: Functions (Linear, Cubic, Exponential, Logarithmic)

**Goal**: Master common function types, their graphs, rates of change, inverse and composite functions, preparing for differentiation.

## 4.1 Basic Function Concepts

A function assigns each input $x$ (from the domain) exactly one output $y = f(x)$. We are particularly interested in how $y$ changes as $x$ changes – this is the **rate of change**.

- **Domain**: the set of allowable $x$ values.
- **Range**: the set of possible $y$ values.

**Example**: $f(x) = x^2$ has domain all real numbers, and range $[0, \infty)$.

## 4.2 Linear Functions $f(x) = mx + c$

### Form and Graph

A linear function graphs as a straight line. The slope $m$ tells us how much $y$ increases for each unit increase in $x$. The intercept $c$ is the value of $f(0)$, where the line crosses the $y$-axis.

The rate of change of a linear function is constant: it is always $m$.

### Slope from Two Points

Given two points $(x_1, y_1)$ and $(x_2, y_2)$, the slope is:

$$
m = \frac{y_2 - y_1}{x_2 - x_1}
$$

For linear functions, the average rate of change over any interval equals the instantaneous rate of change at any point (they are the same).

**Example**: The line through $(1, 3)$ and $(4, 9)$ has slope $m = (9-3)/(4-1) = 6/3 = 2$.

## 4.3 Cubic Functions $f(x) = ax^3 + bx^2 + cx + d$

A cubic function's graph has an "S" shape (or a reverse S). It may have one local maximum and one local minimum, or neither (for example, $f(x) = x^3$ has a point of inflection rather than a max or min – in IGCSE we just describe the change in curvature).

The rate of change (derivative) of a cubic is a quadratic function, which can have two zeros (corresponding to the extreme points).

**Example**: $f(x) = x^3 - 3x$ has derivative $3x^2 - 3$, which equals zero at $x = \pm 1$. There is a local maximum at $x = -1$ and a local minimum at $x = 1$.

## 4.4 Exponential Function $f(x) = a^x$ $(a > 0, a \neq 1)$

### Form and Graph

Exponential functions grow (or decay) extremely quickly. When $a > 1$, $f(x)$ grows explosively as $x$ increases. When $0 < a < 1$, $f(x)$ approaches 0 as $x$ increases. The graph always passes through the point $(0, 1)$ because $a^0 = 1$ for any valid $a$.

### Logarithms – A Necessary Supplement

Before we discuss the rate of change of exponentials, we need to understand logarithms, which are the inverses of exponential functions.

#### Definition

- **Common logarithm**: base 10, written as $\log(x)$ or $\log_{10}(x)$. If $10^y = x$, then $\log(x) = y$.
- **Natural logarithm**: base $e$ (where $e \approx 2.71828$), written as $\ln(x)$. If $e^y = x$, then $\ln(x) = y$.

The relationship between them: $\ln(x) = \log(x) / \log(e)$, where $\log(e) \approx 0.4343$.

#### Basic Logarithm Rules

Let $a > 0$, $a \neq 1$, $M > 0$, $N > 0$, and $k$ be any real number:

| Rule | Formula | Explanation |
|------|---------|-------------|
| **Product** | $\log_a(M \cdot N) = \log_a(M) + \log_a(N)$ | Multiplication becomes addition |
| **Quotient** | $\log_a(M/N) = \log_a(M) - \log_a(N)$ | Division becomes subtraction |
| **Power** | $\log_a(M^k) = k \cdot \log_a(M)$ | Exponent becomes coefficient |
| **Change of base** | $\log_a(M) = \frac{\log_b(M)}{\log_b(a)}$ | Convert to any base |

**Derivation of the product rule**: Let $\log_a M = x$ and $\log_a N = y$. Then $a^x = M$ and $a^y = N$. So $M \cdot N = a^x \cdot a^y = a^{x+y}$, which means $\log_a(M \cdot N) = x + y = \log_a M + \log_a N$.

#### Common Forms of Change of Base

- To common log: $\log_a(M) = \frac{\log(M)}{\log(a)}$
- To natural log: $\log_a(M) = \frac{\ln(M)}{\ln(a)}$

Change of base is essential when you need to evaluate logarithms with bases other than 10 or $e$, especially without a calculator.

#### Common Pitfalls with Logarithms

- **No rule for sum**: $\log_a(M+N) \neq \log_a(M) + \log_a(N)$.
- **Power rule works for any exponent**: for example, $\log_a(\sqrt{M}) = \frac{1}{2} \log_a(M)$.
- **Argument must be positive**: $\log_a(0)$ and $\log_a(\text{negative})$ are undefined.

#### Special Values

| $x$ | $\log(x)$ | $\ln(x)$ |
|-----|-----------|----------|
| 1   | 0         | 0        |
| 10  | 1         | ≈2.3026  |
| 2   | ≈0.3010   | ≈0.6931  |
| 3   | ≈0.4771   | ≈1.0986  |
| $e$ | ≈0.4343   | 1        |

#### Worked Examples

**Example 1 (Simplify)**: Combine $\ln(3x^2) - \ln(6x)$ into a single logarithm.

Solution: $\ln(3x^2) - \ln(6x) = \ln\left(\frac{3x^2}{6x}\right) = \ln\left(\frac{x}{2}\right)$.

**Example 2 (Solve equation)**: Solve $\log_2(x) + \log_2(x-2) = 3$.

Solution: Using the product rule: $\log_2(x(x-2)) = 3$. Exponentiate both sides: $x(x-2) = 2^3 = 8$, which gives $x^2 - 2x - 8 = 0$, so $x = 4$ or $x = -2$. We reject $x = -2$ because the argument of a logarithm must be positive. So $x = 4$.

**Example 3 (Change of base)**: Evaluate $\log_8(16)$.

Solution: $\log_8(16) = \frac{\ln(16)}{\ln(8)} = \frac{\ln(2^4)}{\ln(2^3)} = \frac{4\ln 2}{3\ln 2} = \frac{4}{3}$.

Alternatively: $\log_8(16) = \frac{\log(16)}{\log(8)} = \frac{\log(2^4)}{\log(2^3)} = \frac{4\log 2}{3\log 2} = \frac{4}{3}$.

**Example 4 (Exponential equation)**: Solve $3^{2x-1} = 5$.

Solution: Take natural log of both sides: $(2x-1)\ln 3 = \ln 5$, so $2x-1 = \frac{\ln 5}{\ln 3}$, and $x = \frac{1 + \ln 5 / \ln 3}{2}$. Numerically, $\ln 5 \approx 1.6094$, $\ln 3 \approx 1.0986$, so $\ln 5 / \ln 3 \approx 1.465$, and $x \approx (1 + 1.465)/2 = 1.2325$.

**Example 5 (Proof)**: Prove $\log_a(b) \cdot \log_b(c) = \log_a(c)$.

Proof: $\log_a(b) \cdot \log_b(c) = \frac{\ln b}{\ln a} \cdot \frac{\ln c}{\ln b} = \frac{\ln c}{\ln a} = \log_a(c)$.

### Rate of Change of Exponential Functions

Take $f(x) = 2^x$ as an example. Let us compute the average rate of change at $x=1$ for different $\Delta x$ values:

| $\Delta x$ | Average rate $(2^{1+\Delta x} - 2) / \Delta x$ |
|------|-----------------------------------------------|
| 0.1  | $(2^{1.1} - 2)/0.1 \approx (2.1435 - 2)/0.1 = 1.435$ |
| 0.01 | $(2^{1.01} - 2)/0.01 \approx (2.0145 - 2)/0.01 = 1.45$ |
| 0.001| about 1.4427 |

As $\Delta x \to 0$, the average rate approaches $2 \cdot \ln(2) \approx 1.386$ (where $\ln(2) \approx 0.6931$).

**Important observation**: The rate of change of an exponential function is proportional to the function value itself. That is, the instantaneous rate of change is $f'(x) = a^x \cdot \ln(a)$. For example, $f(1) = 2$ gives a rate of about 1.386, and $f(2) = 4$ gives a rate of about 2.772 (exactly double). When the function value doubles, the rate also doubles.

**The special natural exponential function**: $f(x) = e^x$ (with $e \approx 2.71828$). Since $\ln(e) = 1$, its rate of change equals itself: $f'(x) = e^x$.

## 4.5 Logarithmic Function $f(x) = \log_a x$ $(a > 0, a \neq 1)$

### Form and Graph

The logarithmic function is the inverse of the exponential function. Its domain is $x > 0$, and its range is all real numbers.

- When $a > 1$, the function increases but at a decreasing rate (it gets slower and slower).
- When $0 < a < 1$, the function decreases.
- The graph always passes through $(1, 0)$ because $\log_a 1 = 0$ for any valid $a$.

**Inverse relationship**: The exponential function $y = a^x$ is strictly monotonic (increasing for $a > 1$, decreasing for $0 < a < 1$), so it has an inverse. That inverse is precisely $y = \log_a x$.

- Domain of exponential: all real numbers; range: $(0, \infty)$.
- Domain of logarithmic: $(0, \infty)$; range: all real numbers.
- Their graphs are symmetric about the line $y = x$.

**Understanding symmetry**: If point $(p, q)$ lies on the exponential graph, meaning $q = a^p$, then $p = \log_a q$, so point $(q, p)$ lies on the logarithmic graph. The points $(p, q)$ and $(q, p)$ are symmetric about $y = x$.

**Special bases**:
- $a = 10$ gives the common logarithm, sometimes written as $\lg x$.
- $a = e$ ($e \approx 2.71828$) gives the natural logarithm, denoted $\ln x$. The natural log has the simplest derivative: $1/x$, without extra constants.

**Graph features (for $a > 1$)**:
- As $x \to 0^+$, $\log_a x \to -\infty$ (very slow descent).
- It crosses the $x$-axis at $x = 1$.
- For large $x$, $\log_a x$ grows extremely slowly (e.g., $\log_{10} 1000 = 3$, $\log_{10} 10^6 = 6$).
- The curve is concave down, meaning it flattens out as $x$ increases.

For $\log_2(x)$ and $\log_{0.5}(x)$, they are symmetric about the $x$-axis. Since $0.5 = 1/2$:

$$
\log_{0.5}(x) = \frac{\log_2(x)}{\log_2(0.5)} = \frac{\log_2(x)}{-1} = -\log_2(x)
$$

So the two function values are opposites, and their graphs are reflections across the $x$-axis. This is a general property: when bases are reciprocals, the graphs are symmetric about the $x$-axis.

### Rate of Change of Logarithmic Functions

Take the natural logarithm $f(x) = \ln x$ as an example.

**Near $x = 1$**: Let us compute the average rate of change from $1$ to $1 + \Delta x$ for smaller and smaller $\Delta x$:

| $\Delta x$ | Average rate $(\ln(1+\Delta x) - \ln 1) / \Delta x$ |
|------|---------------------------------------------------|
| 0.1  | $\ln(1.1)/0.1 \approx 0.09531/0.1 = 0.9531$ |
| 0.01 | $\ln(1.01)/0.01 \approx 0.00995/0.01 = 0.9950$ |
| 0.001| about 0.9995 |

As $\Delta x \to 0$, the average rate approaches 1. Hence the instantaneous rate of change of $\ln x$ at $x=1$ is 1.

**At other points**:
- At $x = 2$, similar numerical experiments give a limit near 0.5.
- At $x = 10$, the limit is about 0.1.
- At $x = 0.5$, the limit is about 2.

**General pattern**: The instantaneous rate of change of $\ln x$ equals $1/x$. For a general base $a$, using the change-of-base formula $\log_a x = \ln x / \ln a$, the derivative becomes $1/(x \cdot \ln a)$.

**Comparison with exponential**:
- Exponential $a^x$ has derivative proportional to itself ($a^x \cdot \ln a$), so it grows faster and faster.
- Logarithmic $\log_a x$ has derivative proportional to $1/x$, so it grows slower and slower.

### Important Properties of Logarithms

**Algebraic properties**:
- $\log_a(M \cdot N) = \log_a M + \log_a N$
- $\log_a(M/N) = \log_a M - \log_a N$
- $\log_a(M^k) = k \cdot \log_a M$
- Change of base: $\log_a M = \frac{\log_b M}{\log_b a}$

These are essential for simplifying expressions and solving exponential equations. For example, to solve $2^x = 7$, take common logs: $x \cdot \log 2 = \log 7$, so $x = \log 7 / \log 2$.

**Inverse identities**:
- $a^{\log_a x} = x$ for all $x > 0$
- $\log_a(a^x) = x$ for all real $x$

### Applications of Logarithms

- **Sound intensity (decibels)**: $L = 10 \cdot \log_{10}(I/I_0)$
- **Earthquake magnitude (Richter scale)**: $M = \log_{10}(A/A_0)$
- **pH scale**: $\text{pH} = -\log_{10}[H^+]$
- **Information theory**: information content often uses base-2 logarithms.
- **Algorithm complexity**: many efficient algorithms run in $O(\log n)$ time (e.g., binary search).

Logarithms compress wide-ranging quantities into manageable scales and convert multiplication into addition.

### Common Pitfalls

- **Domain**: $\log_a x$ is defined only for $x > 0$. Beginners often forget this and introduce extraneous solutions.
- **Base restrictions**: $a > 0$ and $a \neq 1$. Negative, zero, or one are not allowed.
- **No distributive law**: $\log_a(x+y) \neq \log_a x + \log_a y$.
- **Change of base required** when comparing logs with different bases.
- **Solving exponential equations**: taking logs of both sides requires the right-hand side to be positive; otherwise there is no solution.

### Symmetry with Exponential – A Visual Description

Imagine a coordinate system. Plot $y = 2^x$: it curves upward from left to right, passes through $(0, 1)$ and $(1, 2)$, rising faster as $x$ increases. Now draw the line $y = x$. Then plot $y = \log_2 x$: it passes through $(1, 0)$ and $(2, 1)$, rising slowly and always staying below $y = x$ for $x > 1$ and above for $0 < x < 1$. The two curves are mirror images across $y = x$. For instance, the point $(1, 2)$ on the exponential graph reflects to $(2, 1)$ on the logarithmic graph. This symmetry vividly illustrates the inverse relationship.

### Derivative Examples

Find the derivative of $f(x) = \ln(2x)$.

Solution: Use the chain rule. The derivative of the outer function $\ln(u)$ is $1/u$, and the inner $u = 2x$ has derivative 2. Thus:

$$
f'(x) = \frac{1}{2x} \times 2 = \frac{1}{x}
$$

For a common logarithm $g(x) = \log_{10}(2x)$, change the base first:

$$
g(x) = \frac{\ln(2x)}{\ln(10)}
$$

Its derivative is:

$$
g'(x) = \frac{1}{x \cdot \ln(10)}
$$

An extra constant $1/\ln(10)$ appears. The natural logarithm $\ln$ avoids such extra constants.

---

## 4.6 Comparison of Rates of Change

| Function Type | Rate Characteristic | Derivative (later) |
|---------------|---------------------|--------------------|
| Linear $mx + c$ | constant | $m$ |
| Quadratic $ax^2 + bx + c$ | changes linearly with $x$ | $2ax + b$ |
| Cubic | changes quadratically | quadratic function |
| Exponential $a^x$ | proportional to $f(x)$ | $a^x \ln a$ |
| Logarithmic $\log_a x$ | decreases, ~ $1/x$ | $1/(x \ln a)$ |

---

## 4.7 Inverse and Composite Functions

### Inverse Function

- A **one-to-one** function has an inverse.
- $f^{-1}(y) = x \iff f(x) = y$.
- Graphs of $f$ and $f^{-1}$ are symmetric about $y = x$.

**Example**: $f(x) = 2x + 1$ has inverse $f^{-1}(x) = (x-1)/2$.

$f(x) = x^2$ on all real numbers is not one-to-one. But if we restrict the domain to $x \geq 0$, then the inverse is $f^{-1}(x) = \sqrt{x}$.

### Composite Function

$(f \circ g)(x) = f(g(x))$. The order matters: typically $f(g(x)) \neq g(f(x))$.

**Example**: If $f(x) = x^2$ and $g(x) = x+1$, then $f(g(x)) = (x+1)^2$ while $g(f(x)) = x^2 + 1$.

---

## 4.8 Absolute Value Function Transformations

$y = |f(x)|$ means: take the graph of $y = f(x)$ and reflect any part where $y < 0$ above the $x$-axis. The parts where $y \geq 0$ remain unchanged.

**Example**: For $f(x) = x^3 - 3x$, the absolute value graph has sharp corners (cusps) where the original function crosses zero.

---

## 4.9 Comprehensive Examples

**Example 1**: $f(x) = 3x + 2$, average rate of change on $[1, 3] = (11-5)/(2) = 3$, which equals the instantaneous rate (the slope).

**Example 2**: $f(x) = x^2$, average rate from $x=2$ to $2.1 = (4.41-4)/0.1 = 4.1$. From $2$ to $2.01$, it is $(4.0401-4)/0.01 = 4.01$. As the interval shrinks, the average rate approaches 4.

**Example 3**: Compare $2^x$ and $x^2$ at $x=4$: $2^4 = 16$, $2^5 = 32$ (average rate 16); $4^2 = 16$, $5^2 = 25$ (average rate 9). Exponential grows faster.

---

## 4.10 Chapter Summary

- Linear: constant rate.
- Quadratic: rate changes linearly.
- Cubic: rate changes quadratically.
- Exponential: rate is proportional to the function value.
- Logarithmic: rate is proportional to $1/x$.
- A function must be one-to-one to have an inverse; composition order matters.
- $|f(x)|$ reflects negative portions of the graph above the $x$-axis.

---

# Chapter 5: Differentiation (Derivatives)

**Learning path**:
5.1–5.3 → polynomials and chain rule (Paper 1 core)
5.4–5.5 → trig, exponential, log derivatives (advanced)
5.6–5.7 → tangents, extrema, kinematics (applications)

## 5.1 What is a Derivative?

The derivative is the mathematical name for **instantaneous rate of change**. It answers the question: how fast is a function changing at a single point?

### Average vs. Instantaneous Rate of Change

- **Average rate of change** over an interval $[x, x+\Delta x]$:

$$
\frac{f(x+\Delta x) - f(x)}{\Delta x}
$$

This is like driving from A to B: total distance divided by total time gives the **average speed**.

- **Instantaneous rate of change**: the limit of the average rate as $\Delta x$ approaches 0:

$$
f'(x) = \lim_{\Delta x \to 0} \frac{f(x+\Delta x) - f(x)}{\Delta x}
$$

This is like looking at the car's speedometer at an exact moment – the **instantaneous speed**.

### Geometric Meaning

$f'(a)$ is the **slope of the tangent line** to the curve $y = f(x)$ at the point $(a, f(a))$.

- The tangent line is the straight line that best "touches" the curve at that point.
- Positive slope: the curve is rising.
- Negative slope: the curve is falling.
- Zero slope: the curve is flat (possible maximum or minimum).

### A Concrete Example

Take $f(x) = x^2$ and find the derivative at $x = 1$.

Compute average rates with smaller and smaller $\Delta x$:

- $\Delta x = 0.1$: $(1.1^2 - 1^2)/0.1 = (1.21 - 1)/0.1 = 2.1$
- $\Delta x = 0.01$: $(1.01^2 - 1^2)/0.01 = (1.0201 - 1)/0.01 = 2.01$
- $\Delta x = 0.001$: approximately 2.001

As $\Delta x$ gets smaller, the average rate gets closer to 2. Thus $f'(1) = 2$.

Geometrically, the parabola $y = x^2$ has a tangent line at $(1, 1)$ with slope 2.

### Notation

- Lagrange notation: $f'(x)$
- Leibniz notation: $\frac{dy}{dx}$ (where $y = f(x)$)

Both mean the derivative of $f$ with respect to $x$.

### Summary

- Derivative = instantaneous rate of change = slope of the tangent.
- It uses a limit to define "instantaneous".
- Without limits, there is no calculus.

## 5.2 Limit Intuition

**Indeterminate form $0/0$**: factor and cancel.

Example: $\lim_{x \to 2} \frac{x^2-4}{x-2} = \lim_{x \to 2} \frac{(x-2)(x+2)}{x-2} = \lim_{x \to 2} (x+2) = 4$.

> Note: $x$ approaches 2, but never equals 2.

## 5.3 Polynomial Differentiation (Power Rule)

For $f(x) = x^n$ (where $n$ is a rational number):

$$
f'(x) = n x^{n-1}
$$

**Examples**:
- $x^2 \to 2x$
- $x^3 \to 3x^2$
- $x \to 1$
- $1 \to 0$
- $\sqrt{x} = x^{1/2} \to (1/2)x^{-1/2} = 1/(2\sqrt{x})$

**Constant multiple and sum/difference**:
- $(c \cdot u)' = c \cdot u'$
- $(u \pm v)' = u' \pm v'$

**Example**: $f(x) = 3x^2 - 4x + 5$ → $f'(x) = 6x - 4$.

> **Domain caution**: $f(x) = 1/x$ is defined for $x \neq 0$, and its derivative $-1/x^2$ is also only defined for $x \neq 0$.

### Implicit Differentiation (for relations like $x^2 + y^2 = r^2$)

Differentiate both sides with respect to $x$, treating $y$ as a function of $x$:

$$
2x + 2y \cdot \frac{dy}{dx} = 0 \quad \rightarrow \quad \frac{dy}{dx} = -\frac{x}{y} \quad (y \neq 0)
$$

## 5.4 Chain Rule (Composite Functions)

For $y = (ax+b)^n$, let $u = ax+b$:

$$
\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = n u^{n-1} \cdot a = a n (ax+b)^{n-1}
$$

**Examples**:
- $(2x+1)^3$ → $3(2x+1)^2 \cdot 2 = 6(2x+1)^2$
- $1/(x+1) = (x+1)^{-1}$ → $-(x+1)^{-2} \cdot 1 = -1/(x+1)^2$
- $\sqrt{3x-2} = (3x-2)^{1/2}$ → $(1/2)(3x-2)^{-1/2} \cdot 3 = 3/(2\sqrt{3x-2})$

## 5.5 Derivatives of Trig, Exponential, Log (Advanced)

> ⚠️ **Radians only!** Make sure your calculator is in Rad mode.

### Trigonometric Functions

$$
\frac{d}{dx} \sin x = \cos x
$$

$$
\frac{d}{dx} \cos x = -\sin x
$$

$$
\frac{d}{dx} \tan x = \sec^2 x
$$

**Examples**:
- $3\sin x \to 3\cos x$
- $\cos(2x) \to -\sin(2x) \cdot 2 = -2\sin 2x$
- $\tan(3x) \to \sec^2(3x) \cdot 3 = 3\sec^2(3x)$

### Exponential and Logarithmic

$$
\frac{d}{dx} e^x = e^x
$$

$$
\frac{d}{dx} a^x = a^x \ln a \quad (a > 0, a \neq 1)
$$

$$
\frac{d}{dx} \ln x = \frac{1}{x}
$$

$$
\frac{d}{dx} \log_a x = \frac{1}{x \ln a}
$$

**Examples**:
- $e^{2x} \to e^{2x} \cdot 2 = 2e^{2x}$
- $2^x \to 2^x \ln 2$
- $\ln(3x+1) \to \frac{1}{3x+1} \cdot 3 = \frac{3}{3x+1}$

## 5.6 Tangents and Normals (Three-Step Method)

1. **Find the point of tangency**: $(a, f(a))$.
2. **Find the slope**: $m = f'(a)$.
3. **Write the equation**: $y - f(a) = m(x - a)$.

**Example**: $f(x) = x^2$ at $x = 1$. $f(1) = 1$, $f'(x) = 2x$, $f'(1) = 2$. Tangent line: $y - 1 = 2(x - 1)$, or $y = 2x - 1$.

**Normal line**: perpendicular to the tangent. Its slope is $m_{\text{normal}} = -1/m$ (if $m \neq 0$). For the example above, the normal is $y - 1 = -\frac{1}{2}(x - 1)$.

> ⚠️ **Critical trap**:
> - "tangent at point $P$" → $P$ is the point of tangency.
> - "tangent passing through point $P$" → $P$ may not be the point of tangency; set an unknown point of tangency $(a, f(a))$, write the tangent equation, then substitute $P$ to solve for $a$.

## 5.7 Extreme Values (Maxima and Minima)

**Procedure**:
1. Find $f'(x)$.
2. Solve $f'(x) = 0$ to find stationary points.
3. Use the first derivative test (sign change):
   - Left positive, right negative → local maximum.
   - Left negative, right positive → local minimum.
   - Same sign on both sides → not an extremum (e.g., $x^3$ at $0$).

**Alternative (second derivative test)**:
- If $f'(a) = 0$ and $f''(a) > 0$ → local minimum.
- If $f'(a) = 0$ and $f''(a) < 0$ → local maximum.
- If $f''(a) = 0$, the test is inconclusive.

**Example**: $f(x) = x^3 - 3x$.
- $f'(x) = 3x^2 - 3 = 0$ → $x = \pm 1$.
- At $x = -1$: left $f'(-2) = 9 > 0$, right $f'(0) = -3 < 0$ → maximum, $f(-1) = 2$.
- At $x = 1$: left $f'(0) = -3 < 0$, right $f'(2) = 9 > 0$ → minimum, $f(1) = -2$.

## 5.8 Kinematics (Motion Along a Line)

For displacement $s(t)$:
- Velocity $v(t) = ds/dt$ (rate of change of displacement).
- Acceleration $a(t) = dv/dt = d^2s/dt^2$.

**Direction**:
- $v(t) > 0$ → moving in the positive direction.
- $v(t) < 0$ → moving in the negative direction.
- $v(t) = 0$ → instantaneously at rest.
- If $v(t)$ changes sign, the particle reverses direction.

**Example**: $s(t) = t^3 - 6t^2 + 9t$.
- $v(t) = 3t^2 - 12t + 9 = 3(t-1)(t-3)$.
- $v = 0$ at $t = 1$ and $t = 3$.
- Sign analysis: $t < 1$: $v > 0$; $1 < t < 3$: $v < 0$; $t > 3$: $v > 0$.
- The particle changes direction at $t = 1$ and $t = 3$.

## 5.9 Chapter Summary (Quick Reference)

| Task | How |
|------|-----|
| Derivative of $x^n$ | $n x^{n-1}$ |
| Derivative of $(ax+b)^n$ (chain rule) | $a n (ax+b)^{n-1}$ |
| Derivative of $\sin x$ | $\cos x$ |
| Derivative of $\cos x$ | $-\sin x$ |
| Derivative of $\tan x$ | $\sec^2 x$ |
| Derivative of $e^x$ | $e^x$ |
| Derivative of $\ln x$ | $1/x$ |
| Tangent line | three-step method |
| Max/min | solve $f'(x) = 0$, test sign change |
| Kinematics | $v = ds/dt$, $a = dv/dt$ |

---

# Chapter 6: Equations and Inequalities (Graphical Method)

**Goal**: Use graphs (especially sketches based on derivatives) to solve equations and inequalities, understand the link between intersections and solutions, and handle absolute value transformations.

## 6.1 Solutions and Intersections

**Key idea**: Solutions of $f(x) = g(x)$ are the $x$-coordinates of the intersection points of $y = f(x)$ and $y = g(x)$. A special case is $f(x) = 0$, which gives the intersections with the $x$-axis (also called zeros or roots).

**Example**: The equation $x^2 - 3x + 2 = 0$ corresponds to the graph of $y = x^2 - 3x + 2$ crossing the $x$-axis at $x = 1$ and $x = 2$.

## 6.2 Sketching Graphs Using Derivatives

For a good sketch, find:
- Intercepts ($x$- and $y$-intercepts)
- Monotonicity (where the function is increasing or decreasing)
- Extreme points (maxima and minima)
- End behaviour as $x \to \pm\infty$

**Steps**:
1. Find $f'(x)$ and solve $f'(x) = 0$ to find stationary points.
2. Classify each stationary point (max or min) using the sign of $f'$.
3. Compute $f$ at those points and at $x = 0$.
4. Consider the end behaviour by looking at the leading term.

**Example**: $f(x) = x^3 - 3x$.
- $f'(x) = 3x^2 - 3 = 0$ → $x = \pm 1$.
- $x = -1$: maximum, $f(-1) = 2$.
- $x = 1$: minimum, $f(1) = -2$.
- $f(0) = 0$.
- As $x \to \infty$, $f(x) \to \infty$; as $x \to -\infty$, $f(x) \to -\infty$.

## 6.3 Solving Inequalities with Graphs

$f(x) > 0$ means finding the $x$ values where the graph of $f$ is above the $x$-axis.

**Example**: $x^2 - 3x + 2 > 0$. The graph opens upward, zeros at 1 and 2, so the graph is above the $x$-axis for $x < 1$ or $x > 2$.

**Example**: $x^3 - 3x < 0$. From the sketch, the graph is below the $x$-axis for $x < -\sqrt{3}$ or $0 < x < \sqrt{3}$ (where $\sqrt{3} \approx 1.732$).

## 6.4 Absolute Value Equations and Inequalities

$y = |f(x)|$ reflects the negative parts of $f(x)$ above the $x$-axis.

**Equation $|f(x)| = k$ (with $k > 0$)**: equivalent to $f(x) = k$ or $f(x) = -k$.

**Inequality $|f(x)| < k$**: equivalent to $-k < f(x) < k$.

**Example**: Solve $|x^2 - 3x + 2| < 1$.

This means $-1 < x^2 - 3x + 2 < 1$.

Left inequality: $x^2 - 3x + 3 > 0$ – the discriminant is $9 - 12 = -3 < 0$, so this is always true.

Right inequality: $x^2 - 3x + 1 < 0$. The roots are $(3 \pm \sqrt{5})/2$, so the solution is $(3 - \sqrt{5})/2 < x < (3 + \sqrt{5})/2$.

## 6.5 Using Derivatives for Complex Inequalities

**Example**: $\frac{2x}{x^2 + 1} > 0$. The denominator is always positive, so the inequality is equivalent to $2x > 0$, giving $x > 0$.

**Example**: $x e^{-x} > 0$. Since $e^{-x} > 0$ for all $x$, this simplifies to $x > 0$.

**Example**: $\ln x > 0$. This gives $x > 1$.

## 6.6 Intersection of Two Functions and Inequalities

$f(x) > g(x)$ means the graph of $y = f(x)$ is above the graph of $y = g(x)$.

Procedure: find the intersections of $f$ and $g$, then test a point in each interval.

**Example**: $x^2 < 2x + 3$. Rearranging: $x^2 - 2x - 3 < 0$, which factors as $(x-3)(x+1) < 0$. The solution is $-1 < x < 3$.

## 6.7 Comprehensive Examples

**Example 1**: $f(x) = x^3 - 6x^2 + 9x = x(x-3)^2$.
$f(x) > 0$ when $x > 0$ and $x \neq 3$, so the solution is $(0, 3) \cup (3, \infty)$.

**Example 2**: $|x^2 - 4x + 3| = 2$.

Case 1: $x^2 - 4x + 3 = 2$ → $x^2 - 4x + 1 = 0$ → $x = 2 \pm \sqrt{3}$.

Case 2: $x^2 - 4x + 3 = -2$ → $x^2 - 4x + 5 = 0$. The discriminant is $16 - 20 = -4 < 0$, so no real solutions.

Solutions: $2 + \sqrt{3}$ and $2 - \sqrt{3}$.

**Example 3**: $|x-1| > |2x+3|$. Square both sides: $(x-1)^2 > (2x+3)^2$ → $x^2 - 2x + 1 > 4x^2 + 12x + 9$ → $0 > 3x^2 + 14x + 8$ → $3x^2 + 14x + 8 < 0$.

The roots are $(-14 \pm \sqrt{196 - 96})/6 = (-14 \pm 10)/6$, giving $-4$ and $-2/3$. Since the quadratic opens upward, the inequality holds between the roots: $-4 < x < -2/3$.

## 6.8 Chapter Summary

| Problem | Method |
|---------|--------|
| $f(x) = 0$ | $x$-intercepts of $f$ |
| $f(x) = g(x)$ | intersection of graphs |
| $f(x) > 0$ | where graph is above $x$-axis |
| $f(x) < g(x)$ | where $f$ is below $g$ |
| $|f(x)| = k$ | solve $f(x) = \pm k$ |
| $|f(x)| < k$ | $-k < f(x) < k$ |
| Complex inequality | sketch with derivative first |

---

# Chapter 7: Integration (Indefinite and Definite Integrals)

**Learning path**:
7.1–7.3 → indefinite integrals (antiderivatives)
7.4–7.5 → definite integrals and area
7.6 → integration in kinematics

## 7.1 What is Integration?

Integration is the reverse operation of differentiation – we call it finding the **antiderivative**.

**Example**: If $f'(x) = 2x$, what is $f(x)$? Since the derivative of $x^2$ is $2x$, we have $f(x) = x^2 + C$, where $C$ is any constant (because the derivative of a constant is 0). We write:

$$
\int 2x \, dx = x^2 + C
$$

## 7.2 Basic Integration Formulas (Reverse of Differentiation)

### Power Rule ($n \neq -1$)

$$
\int x^n dx = \frac{x^{n+1}}{n+1} + C
$$

**Examples**:
- $\int x^2 dx = x^3/3 + C$
- $\int x^{-3} dx = x^{-2}/(-2) + C = -1/(2x^2) + C$
- $\int \sqrt{x} dx = \int x^{1/2} dx = x^{3/2} / (3/2) + C = (2/3)x^{3/2} + C$

### Special Case $n = -1$

$$
\int \frac{1}{x} dx = \ln|x| + C
$$

### Exponential and Logarithmic

$$
\int e^x dx = e^x + C
$$

$$
\int a^x dx = \frac{a^x}{\ln a} + C \quad (a > 0, a \neq 1)
$$

### Trigonometric (Radians)

$$
\int \sin x dx = -\cos x + C
$$

$$
\int \cos x dx = \sin x + C
$$

$$
\int \sec^2 x dx = \tan x + C
$$

## 7.3 Linearity of Integration

$$
\int (a f(x) + b g(x)) dx = a \int f(x) dx + b \int g(x) dx
$$

**Example**: $\int (3x^2 - 4\sin x + 5e^x) dx = x^3 + 4\cos x + 5e^x + C$.

## 7.4 Definite Integrals and Area

A **definite integral** $\int_a^b f(x) dx$ gives the signed area between $y = f(x)$ and the $x$-axis from $x = a$ to $x = b$. Area above the axis is positive, area below is negative.

**Fundamental Theorem (Newton-Leibniz)**: If $F'(x) = f(x)$, then:

$$
\int_a^b f(x) dx = F(b) - F(a)
$$

**Example**: $\int_1^2 2x dx = [x^2]_1^2 = 4 - 1 = 3$.

**Total area** (absolute area): split the interval at zeros, integrate the absolute value of $f(x)$, or break into separate integrals where $f$ is positive and negative.

**Example**: $y = x^2 - 1$ on $[-2, 2]$. Zeros at $x = \pm 1$.

Total area = $\int_{-2}^{-1} (x^2 - 1) dx + \int_{-1}^{1} -(x^2 - 1) dx + \int_{1}^{2} (x^2 - 1) dx = \frac{4}{3} + \frac{4}{3} + \frac{4}{3} = 4$.

## 7.5 Area Between Two Curves

If $f(x) \geq g(x)$ on $[a, b]$, the area between them is:

$$
\int_a^b [f(x) - g(x)] dx
$$

**Steps**:
1. Find intersections (solve $f(x) = g(x)$).
2. Determine which function is above on each interval.
3. Integrate the difference.

**Example**: $y = x^2$ and $y = 2x$.

Intersections: $x^2 = 2x$ → $x = 0, 2$.

On $(0, 2)$, $2x \geq x^2$, so:

Area = $\int_0^2 (2x - x^2) dx = [x^2 - x^3/3]_0^2 = (4 - 8/3) - 0 = 4/3$.

## 7.6 Integration in Kinematics

Given acceleration $a(t)$:
- $v(t) = \int a(t) dt + v_0$ (initial velocity)
- $s(t) = \int v(t) dt + s_0$ (initial displacement)

**Example**: $a(t) = 6t - 2$, $v(0) = 1$, $s(0) = 0$.

$v(t) = \int (6t - 2) dt = 3t^2 - 2t + C$. Since $v(0) = 1$, we have $C = 1$, so $v(t) = 3t^2 - 2t + 1$.

$s(t) = \int (3t^2 - 2t + 1) dt = t^3 - t^2 + t + D$. Since $s(0) = 0$, we have $D = 0$, so $s(t) = t^3 - t^2 + t$.

**Displacement from $v(t)$**: $\int_{t_1}^{t_2} v(t) dt$ gives the net displacement (not total distance).

**Example**: $v(t) = t^2 - 4t + 3$, displacement from $t = 1$ to $3$:

$\int_1^3 (t^2 - 4t + 3) dt = [t^3/3 - 2t^2 + 3t]_1^3 = (9 - 18 + 9) - (1/3 - 2 + 3) = 0 - (4/3) = -4/3$.

The negative sign means the net displacement is in the negative direction.

## 7.7 Chapter Summary

| Task | How |
|------|-----|
| $\int x^n dx$ ($n \neq -1$) | $x^{n+1}/(n+1) + C$ |
| $\int 1/x dx$ | $\ln|x| + C$ |
| $\int e^x dx$ | $e^x + C$ |
| $\int \sin x dx$ | $-\cos x + C$ |
| $\int \cos x dx$ | $\sin x + C$ |
| $\int \sec^2 x dx$ | $\tan x + C$ |
| Definite integral $\int_a^b$ | $F(b) - F(a)$ |
| Area under curve | definite integral (watch sign) |
| Area between curves | $\int (\text{top} - \text{bottom}) dx$, find intersections |
| Kinematics (given $a$) | integrate to $v$, then to $s$ |

---

# Chapter 8: Trigonometry

**Goal**: Master the six trig functions, their graphs, basic identities, radian measure, solving trig equations, and proving identities.

**Learning path**:
8.1–8.2 → radian measure, definitions
8.3–8.4 → graphs, periodicity, symmetry
8.5–8.6 → identities and proofs
8.7 → solving trig equations (key)

## 8.1 Degrees and Radians

In calculus we always use **radians**. The definition: one radian is the angle subtended by an arc whose length equals the radius of the circle.

Full circle → $2\pi$ radians.

$$
360^\circ = 2\pi \text{ rad},\quad 180^\circ = \pi \text{ rad},\quad 1^\circ = \pi/180 \text{ rad}
$$

**Common conversions**:
- $0^\circ = 0$
- $30^\circ = \pi/6$
- $45^\circ = \pi/4$
- $60^\circ = \pi/3$
- $90^\circ = \pi/2$
- $180^\circ = \pi$

> ⚠️ **Critical**: Always set your calculator to **Rad** mode when differentiating, integrating, or solving trig equations.

### Unit Circle Applications

**Derivation of $\sin(180^\circ - \theta) = \sin\theta$**: On the unit circle, the point for $\theta$ is $(\cos\theta, \sin\theta)$. For $180^\circ - \theta$, the point is $(\cos(180^\circ - \theta), \sin(180^\circ - \theta))$. Symmetry about the $y$-axis gives the same $y$-coordinate.

**Special triangles**:
- $30^\circ-60^\circ-90^\circ$: sides $1$, $\sqrt{3}$, $2$ → $\sin 30^\circ = 1/2$, $\cos 30^\circ = \sqrt{3}/2$, $\tan 30^\circ = 1/\sqrt{3}$; $\sin 60^\circ = \sqrt{3}/2$, $\cos 60^\circ = 1/2$.
- $45^\circ-45^\circ-90^\circ$: sides $1, 1, \sqrt{2}$ → $\sin 45^\circ = \sqrt{2}/2$, $\cos 45^\circ = \sqrt{2}/2$, $\tan 45^\circ = 1$.

## 8.2 Six Trigonometric Functions (Unit Circle)

On the unit circle ($x^2 + y^2 = 1$), with angle angle $\theta$ measured from the positive $x$-axis:

- $\sin\theta = y$
- $\cos\theta = x$
- $\tan\theta = y/x = \sin\theta / \cos\theta$
- $\sec\theta = 1/\cos\theta$
- $\csc\theta = 1/\sin\theta$
- $\cot\theta = 1/\tan\theta = \cos\theta / \sin\theta$

### Signs (ASTC Rule)

The sign of each trigonometric function depends on which quadrant the angle lies in:

- Quadrant I ($0^\circ$–$90^\circ$): all six functions are positive.
- Quadrant II ($90^\circ$–$180^\circ$): only $\sin$ (and $\csc$) are positive.
- Quadrant III ($180^\circ$–$270^\circ$): only $\tan$ (and $\cot$) are positive.
- Quadrant IV ($270^\circ$–$360^\circ$): only $\cos$ (and $\sec$) are positive.

The mnemonic "ASTC" (All, Sin, Tan, Cos) helps you remember which functions are positive in each quadrant, starting from QI and going counterclockwise.

| Quadrant | sin | cos | tan | sec | csc | cot |
|----------|-----|-----|-----|-----|-----|-----|
| I | + | + | + | + | + | + |
| II | + | - | - | - | + | - |
| III | - | - | + | - | - | + |
| IV | - | + | - | + | - | - |

### Sum-to-Product Formulas (Extension)

These formulas convert sums of sines or cosines into products, which can be very useful for simplifying expressions or solving equations:

$$
\sin A + \sin B = 2 \sin\left(\frac{A+B}{2}\right) \cos\left(\frac{A-B}{2}\right)
$$

$$
\sin A - \sin B = 2 \cos\left(\frac{A+B}{2}\right) \sin\left(\frac{A-B}{2}\right)
$$

$$
\cos A + \cos B = 2 \cos\left(\frac{A+B}{2}\right) \cos\left(\frac{A-B}{2}\right)
$$

$$
\cos A - \cos B = -2 \sin\left(\frac{A+B}{2}\right) \sin\left(\frac{A-B}{2}\right)
$$

**Example**: $\sin 75^\circ + \sin 15^\circ = 2 \sin 45^\circ \cos 30^\circ = 2 \cdot (\sqrt{2}/2) \cdot (\sqrt{3}/2) = \sqrt{6}/2$.

---

## 8.3 Graphs of Trig Functions

### $y = \sin x$

- Domain: all real numbers.
- Range: $[-1, 1]$.
- Period: $2\pi$ (the graph repeats every $2\pi$ units).
- Odd function: $\sin(-x) = -\sin x$ (symmetric about the origin).
- Zeros at $x = n\pi$ (where $n$ is any integer).

The sine curve starts at 0, rises to 1 at $\pi/2$, returns to 0 at $\pi$, goes to $-1$ at $3\pi/2$, and back to 0 at $2\pi$.

### $y = \cos x$

- Domain: all real numbers.
- Range: $[-1, 1]$.
- Period: $2\pi$.
- Even function: $\cos(-x) = \cos x$ (symmetric about the $y$-axis).
- Zeros at $x = \pi/2 + n\pi$.

The cosine curve starts at 1 at $x=0$, goes to 0 at $\pi/2$, to $-1$ at $\pi$, back to 0 at $3\pi/2$, and returns to 1 at $2\pi$.

### $y = \tan x$

- Domain: all real numbers except $x = \pi/2 + n\pi$ (where $\cos x = 0$).
- Range: all real numbers.
- Period: $\pi$.
- Odd function: $\tan(-x) = -\tan x$.
- Vertical asymptotes at $x = \pi/2 + n\pi$.

The tangent curve passes through 0 at $x = n\pi$, rises to $+\infty$ as it approaches the asymptote from the left, and comes from $-\infty$ on the right side of the asymptote.

---

## 8.4 Amplitude, Period, Transformations

For a function of the form $y = A \sin(Bx + C) + D$:

- $|A|$ = **amplitude** (vertical stretch or compression). It determines how tall the waves are.
- $2\pi/|B|$ = **period** (horizontal stretch or compression). It determines how wide each cycle is.
- $-C/B$ = **phase shift** (horizontal translation). It moves the graph left or right.
- $D$ = **vertical shift**. It moves the graph up or down.

**Example**: $y = 3 \sin(2x + \pi/3)$.
- Amplitude = 3.
- Period = $2\pi/2 = \pi$.
- Phase shift = $-\pi/3 \div 2 = -\pi/6$ (shifted left by $\pi/6$).
- Vertical shift = 0.

---

## 8.5 Basic Trigonometric Identities

### Fundamental Identities (Pythagorean)

These are derived from the unit circle equation $x^2 + y^2 = 1$:

$$
\sin^2\theta + \cos^2\theta = 1
$$

Dividing by $\cos^2\theta$ gives:

$$
\sec^2\theta = 1 + \tan^2\theta
$$

Dividing by $\sin^2\theta$ gives:

$$
\csc^2\theta = 1 + \cot^2\theta
$$

### Double-Angle Formulas (Commonly Used)

These express trigonometric functions of $2\theta$ in terms of functions of $\theta$:

$$
\sin(2\theta) = 2 \sin\theta \cos\theta
$$

$$
\cos(2\theta) = \cos^2\theta - \sin^2\theta = 2\cos^2\theta - 1 = 1 - 2\sin^2\theta
$$

The three forms of $\cos(2\theta)$ are especially useful because they allow us to rewrite $\cos^2\theta$ or $\sin^2\theta$ in terms of $\cos(2\theta)$, which is helpful in integration.

$$
\tan(2\theta) = \frac{2\tan\theta}{1 - \tan^2\theta}
$$

---

## 8.6 Proving Trigonometric Identities

The general strategy for proving an identity is to start with the more complicated side and convert everything into $\sin$ and $\cos$, then simplify using algebraic manipulation and the fundamental identities.

**Example 1**: Prove $\tan x + \cot x = \sec x \csc x$.

Left side: $\frac{\sin x}{\cos x} + \frac{\cos x}{\sin x} = \frac{\sin^2 x + \cos^2 x}{\sin x \cos x} = \frac{1}{\sin x \cos x}$.

Right side: $\frac{1}{\cos x} \cdot \frac{1}{\sin x} = \frac{1}{\sin x \cos x}$.

Both sides are equal, so the identity is proved.

**Example 2**: Prove $\frac{\sin\theta}{1+\cos\theta} + \frac{1+\cos\theta}{\sin\theta} = 2\csc\theta$.

Find a common denominator:

$$
\frac{\sin^2\theta + (1+\cos\theta)^2}{\sin\theta(1+\cos\theta)} = \frac{\sin^2\theta + 1 + 2\cos\theta + \cos^2\theta}{\sin\theta(1+\cos\theta)}
$$

Since $\sin^2\theta + \cos^2\theta = 1$, the numerator becomes $1 + 1 + 2\cos\theta = 2 + 2\cos\theta = 2(1+\cos\theta)$.

So the expression simplifies to $\frac{2(1+\cos\theta)}{\sin\theta(1+\cos\theta)} = \frac{2}{\sin\theta} = 2\csc\theta$.

---

## 8.7 Solving Trigonometric Equations

### Basic Form $\sin x = k$

**Reference angle method**:

1. Find the reference angle $\alpha = \arcsin(|k|)$, which is an acute angle between $0$ and $\pi/2$.
2. Determine which quadrants contain solutions based on the sign of $k$:
   - If $k \geq 0$: solutions are in QI and QII: $x = \alpha$ and $x = \pi - \alpha$.
   - If $k < 0$: solutions are in QIII and QIV: $x = \pi + \alpha$ and $x = 2\pi - \alpha$.
3. Add $2n\pi$ (where $n$ is an integer) for general solutions.

**Example**: Solve $\sin x = 1/2$ on $[0, 2\pi)$.

$\alpha = \pi/6$. Since $k > 0$, solutions are in QI and QII: $x = \pi/6$ and $x = \pi - \pi/6 = 5\pi/6$.

**Example**: Solve $\sin x = -1/2$ on $[0, 2\pi)$.

$\alpha = \pi/6$. Since $k < 0$, solutions are in QIII and QIV: $x = \pi + \pi/6 = 7\pi/6$ and $x = 2\pi - \pi/6 = 11\pi/6$.

### $\cos x = k$

- If $k \geq 0$: $x = \alpha$ and $x = 2\pi - \alpha$ (QI and QIV).
- If $k < 0$: $x = \pi - \alpha$ and $x = \pi + \alpha$ (QII and QIII).

General solution: $x = \pm \alpha + 2n\pi$ (with $\alpha = \arccos(|k|) \in [0, \pi]$).

**Example**: Solve $\cos x = -1/2$ on $[0, 2\pi)$.

$\alpha = \pi/3$. Since $k < 0$, solutions are in QII and QIII: $x = \pi - \pi/3 = 2\pi/3$ and $x = \pi + \pi/3 = 4\pi/3$.

### $\tan x = k$

- $\alpha = \arctan(|k|)$ in $(0, \pi/2)$.
- Solutions: $x = \alpha + n\pi$ (since the period of $\tan$ is $\pi$).

**Example**: Solve $\tan x = \sqrt{3}$ on $[0, 2\pi)$.

$\alpha = \pi/3$. Solutions: $x = \pi/3$ and $x = \pi/3 + \pi = 4\pi/3$.

**Example**: Solve $\tan x = -1$ on $[0, 2\pi)$.

$\alpha = \pi/4$. Since $k < 0$, we can take $\alpha = -\pi/4$ and add $\pi$: $x = 3\pi/4$ and $x = 7\pi/4$.

### Equations Requiring Identities

Sometimes you need to use trigonometric identities to rewrite the equation into a form you can solve.

**Example**: Solve $2\sec^2 x + \tan x - 3 = 0$, for $0 \leq x < 2\pi$.

Use the identity $\sec^2 x = 1 + \tan^2 x$:

$$
2(1 + \tan^2 x) + \tan x - 3 = 0
$$

$$
2\tan^2 x + \tan x - 1 = 0
$$

Let $u = \tan x$. Then $2u^2 + u - 1 = 0$, which factors as $(2u-1)(u+1) = 0$, giving $u = 1/2$ or $u = -1$.

- $\tan x = 0.5$: $\alpha \approx 0.4636$, solutions $0.4636$ and $0.4636 + \pi \approx 3.6052$.
- $\tan x = -1$: $\alpha = \pi/4$, solutions $3\pi/4$ and $7\pi/4$.

Final solutions: $\{0.4636, 3.6052, 3\pi/4, 7\pi/4\}$.

> ⚠️ **Always check the domain**: exclude points where functions are undefined (e.g., $\tan x$ at $\pi/2 + n\pi$).

---

## 8.8 Chapter Summary

| Topic | Key Points |
|-------|------------|
| Radian measure | $180^\circ = \pi$ rad, calculator must be in Rad mode |
| Six trig functions | $\sin, \cos, \tan, \sec, \csc, \cot$; domains and ranges |
| Graphs | $\sin, \cos$ period $2\pi$, $\tan$ period $\pi$; amplitude, shift |
| Basic identities | $\sin^2 + \cos^2 = 1$, $\sec^2 = 1 + \tan^2$, $\csc^2 = 1 + \cot^2$ |
| Proving identities | convert to $\sin, \cos$, common denominator, use $\sin^2 + \cos^2 = 1$ |
| Solving trig equations | reference angle, quadrant signs, add periods, check domain |

---

# Chapter 9: Geometry (Straight Lines and Circles)

**Goal**: Master equations of lines and circles, find intersections, determine relative positions, and find tangents to circles.

**Learning path**:
9.1–9.2 → line equations, slope, parallel/perpendicular
9.3–9.4 → circle equations (standard, general), centre, radius
9.5 → line-circle intersection (discriminant)
9.6 → tangents to circles (three cases)

---

## 9.1 Line Equations

### Common Forms

There are three common ways to write the equation of a straight line:

- **Slope-intercept form**: $y = mx + c$, where $m$ is the slope and $c$ is the $y$-intercept (where the line crosses the $y$-axis).
- **Point-slope form**: $y - y_1 = m(x - x_1)$, where $(x_1, y_1)$ is a known point on the line and $m$ is the slope.
- **General form**: $Ax + By + C = 0$. If $B \neq 0$, the slope is $m = -A/B$.

### Slope from Two Points

Given two points $(x_1, y_1)$ and $(x_2, y_2)$, the slope is:

$$
m = \frac{y_2 - y_1}{x_2 - x_1}
$$

### Parallel and Perpendicular Lines

- **Parallel lines**: they have the same slope: $m_1 = m_2$.
- **Perpendicular lines**: the product of their slopes equals $-1$ (provided both slopes exist): $m_1 \cdot m_2 = -1$.

**Example**: The line $y = 2x + 3$ has slope 2. Any line parallel to it also has slope 2. Any line perpendicular to it has slope $-1/2$.

---

## 9.2 Distance from a Point to a Line

The perpendicular distance from a point $(x_0, y_0)$ to a line $Ax + By + C = 0$ is given by:

$$
d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}
$$

**Example**: Find the distance from $(1, 2)$ to the line $3x - 4y + 5 = 0$.

$$
d = \frac{|3(1) - 4(2) + 5|}{\sqrt{3^2 + (-4)^2}} = \frac{|3 - 8 + 5|}{5} = \frac{0}{5} = 0
$$

The distance is 0, which means the point lies on the line.

---

## 9.3 Circle Equations

### Standard Form

A circle with centre $(a, b)$ and radius $r$ has the equation:

$$
(x - a)^2 + (y - b)^2 = r^2
$$

**Example**: Centre $(2, -3)$, radius 4 → $(x - 2)^2 + (y + 3)^2 = 16$.

### General Form

The general form of a circle equation is:

$$
x^2 + y^2 + 2gx + 2fy + c = 0
$$

From this form, we can find:
- Centre: $(-g, -f)$
- Radius: $\sqrt{g^2 + f^2 - c}$ (must be positive for a real circle)

**Example**: $x^2 + y^2 - 4x + 6y + 9 = 0$.

Here $2g = -4$, so $g = -2$. $2f = 6$, so $f = 3$. $c = 9$.

Centre: $(-(-2), -3) = (2, -3)$.
Radius: $\sqrt{(-2)^2 + 3^2 - 9} = \sqrt{4 + 9 - 9} = \sqrt{4} = 2$.

---

## 9.4 Position of a Line and a Circle

To find where a line and a circle intersect, substitute the line equation into the circle equation. This gives a quadratic equation in $x$ (or $y$). The discriminant $\Delta$ of this quadratic tells us the relationship:

- $\Delta > 0$: two distinct intersection points (the line is a **secant** – it cuts through the circle).
- $\Delta = 0$: exactly one intersection point (the line is a **tangent** – it just touches the circle).
- $\Delta < 0$: no intersection (the line misses the circle entirely).

**Example**: Does the line $y = x + 1$ intersect the circle $x^2 + y^2 = 1$?

Substitute: $x^2 + (x+1)^2 = 1$ → $x^2 + x^2 + 2x + 1 = 1$ → $2x^2 + 2x = 0$ → $2x(x+1) = 0$.

This gives two solutions: $x = 0$ and $x = -1$. So the line intersects the circle at two points.

---

## 9.5 Tangents to a Circle (Three Cases)

### Case 1: Given the Point of Tangency $(x_1, y_1)$ on the Circle

For a circle $(x - a)^2 + (y - b)^2 = r^2$, the tangent line at the point $(x_1, y_1)$ on the circle is:

$$
(x_1 - a)(x - a) + (y_1 - b)(y - b) = r^2
$$

**Example**: Circle $x^2 + y^2 = 5$, point $(1, 2)$ on the circle.

Here $a = 0$, $b = 0$, $r^2 = 5$. The tangent is:

$$
1 \cdot x + 2 \cdot y = 5 \quad \rightarrow \quad x + 2y = 5
$$

### Case 2: Given the Slope $m$

For a circle with centre $(a, b)$ and radius $r$, the equations of the tangent lines with a given slope $m$ are:

$$
y - b = m(x - a) \pm r\sqrt{1 + m^2}
$$

If the centre is at the origin, this simplifies to:

$$
y = mx \pm r\sqrt{1 + m^2}
$$

**Example**: Circle $x^2 + y^2 = 9$, slope $m = 2$.

$$
y = 2x \pm 3\sqrt{1 + 4} = 2x \pm 3\sqrt{5}
$$

So the two tangent lines are $y = 2x + 3\sqrt{5}$ and $y = 2x - 3\sqrt{5}$.

### Case 3: Tangent from an External Point $(x_0, y_0)$

When the point is outside the circle, there are two tangent lines passing through it. Here is the method:

1. Let the tangent have slope $m$, so its equation is $y - y_0 = m(x - x_0)$.
2. Write this in general form: $mx - y + (y_0 - mx_0) = 0$.
3. Set the distance from the centre to this line equal to the radius.
4. Solve for $m$.
5. Also check if vertical lines ($x = x_0$) could be tangents.

**Example**: Circle $x^2 + y^2 = 4$, external point $(4, 0)$.

Let the tangent be $y = m(x - 4)$, or $mx - y - 4m = 0$.

Centre is $(0, 0)$, radius is 2. Distance from centre to line:

$$
\frac{| -4m |}{\sqrt{m^2 + 1}} = 2
$$

$$
4|m| = 2\sqrt{m^2 + 1}
$$

$$
2|m| = \sqrt{m^2 + 1}
$$

Square both sides: $4m^2 = m^2 + 1$ → $3m^2 = 1$ → $m = \pm 1/\sqrt{3}$.

So the two tangents are $y = (1/\sqrt{3})(x - 4)$ and $y = -(1/\sqrt{3})(x - 4)$.

Check the vertical line $x = 4$: distance from centre $(0,0)$ to $x = 4$ is 4, which is not equal to the radius 2, so $x = 4$ is not a tangent.

---

## 9.6 Comprehensive Examples

**Example 1**: A circle has its centre on the line $y = 2x$ and passes through the points $(1, 1)$ and $(2, 3)$. Find its equation.

Let the centre be $(a, 2a)$. Since both points lie on the circle, the distances from the centre to each point are equal (both equal the radius):

$$
(1-a)^2 + (1-2a)^2 = (2-a)^2 + (3-2a)^2
$$

Expand:

$$
(1 - 2a + a^2) + (1 - 4a + 4a^2) = (4 - 4a + a^2) + (9 - 12a + 4a^2)
$$

$$
2 - 6a + 5a^2 = 13 - 16a + 5a^2
$$

Cancel $5a^2$ from both sides: $2 - 6a = 13 - 16a$ → $10a = 11$ → $a = 1.1$.

So the centre is $(1.1, 2.2)$. The radius squared is:

$$
(1 - 1.1)^2 + (1 - 2.2)^2 = 0.01 + 1.44 = 1.45
$$

The equation is $(x - 1.1)^2 + (y - 2.2)^2 = 1.45$.

**Example 2**: Find the values of $k$ such that the line $y = x + k$ is tangent to the circle $x^2 + y^2 = 4$.

Substitute: $x^2 + (x + k)^2 = 4$ → $x^2 + x^2 + 2kx + k^2 = 4$ → $2x^2 + 2kx + (k^2 - 4) = 0$.

For tangency, the discriminant must be 0:

$$
\Delta = (2k)^2 - 4 \cdot 2 \cdot (k^2 - 4) = 4k^2 - 8k^2 + 32 = -4k^2 + 32 = 0
$$

So $k^2 = 8$, giving $k = \pm 2\sqrt{2}$.

---

## 9.7 Chapter Summary

| Topic | Key |
|-------|-----|
| Line equations | slope-intercept, point-slope, general form |
| Parallel/perpendicular | $m_1 = m_2$ or $m_1 m_2 = -1$ |
| Point-line distance | $d = |Ax_0 + By_0 + C| / \sqrt{A^2 + B^2}$ |
| Circle standard form | $(x-a)^2 + (y-b)^2 = r^2$, centre $(a,b)$, radius $r$ |
| Circle general form | $x^2 + y^2 + 2gx + 2fy + c = 0$, centre $(-g,-f)$, radius $\sqrt{g^2 + f^2 - c}$ |
| Line-circle intersection | discriminant of the quadratic after substitution |
| Tangent cases | given point on circle, given slope, from external point |

---

# Chapter 10: Comprehensive Applications

**Goal**: Combine knowledge from previous chapters to solve typical cross-topic problems, developing integrated mathematical thinking.

> Covers: functions, quadratics, polynomials, equations/inequalities, log/exponential, lines & circles, radian measure, trigonometry, permutations & combinations, binomial theorem, vectors, calculus (differentiation & integration).

---

## 10.1 Functions and Quadratics

**Example**: $f(x) = x^2 - 4x + 3$.

1. **Vertex and range**: Complete the square: $(x-2)^2 - 1$. Vertex at $(2, -1)$. Since $a = 1 > 0$, the range is $[-1, \infty)$.

2. **Max/min on $[0, 3]$**: The vertex lies inside the interval, so the minimum is $-1$. Check endpoints: $f(0) = 3$, $f(3) = 0$. So the maximum on this interval is 3.

3. **Solve $f(x) > 0$**: Factor: $(x-1)(x-3) > 0$. Since the parabola opens upward, the inequality holds outside the roots: $x < 1$ or $x > 3$.

---

## 10.2 Functions with Exponentials and Logarithms

**Example**: $f(x) = e^{2x}$, $g(x) = \ln x$.

1. **Composite**: $h(x) = f(g(x)) = e^{2\ln x} = e^{\ln(x^2)} = x^2$, with domain $x > 0$.

2. **Solve $h(x) = e^4$**: $x^2 = e^4$ → $x = e^2$ (only the positive root, since $x > 0$).

3. **Derivative**: $h'(x) = 2x$.

---

## 10.3 Trigonometric Equations and Identities

**Example**: Solve $2\sin^2 x + \cos x = 1$, for $0 \leq x < 2\pi$.

Use $\sin^2 x = 1 - \cos^2 x$:

$$
2(1 - \cos^2 x) + \cos x = 1
$$

$$
2 - 2\cos^2 x + \cos x - 1 = 0
$$

$$
-2\cos^2 x + \cos x + 1 = 0
$$

Multiply by $-1$: $2\cos^2 x - \cos x - 1 = 0$.

Let $u = \cos x$. Then $2u^2 - u - 1 = 0$, which factors as $(2u+1)(u-1) = 0$, giving $u = 1$ or $u = -1/2$.

- $\cos x = 1$ → $x = 0$.
- $\cos x = -1/2$ → $x = 2\pi/3$ or $4\pi/3$.

Solutions: $\{0, 2\pi/3, 4\pi/3\}$.

---

## 10.4 Lines, Circles, and Vectors

**Example**: Circle $(x-1)^2 + (y-2)^2 = 5$, line $y = x + k$.

1. **For $k = 1$**, substitute: $(x-1)^2 + (x+1-2)^2 = 5$ → $(x-1)^2 + (x-1)^2 = 5$ → $2(x-1)^2 = 5$ → $x = 1 \pm \sqrt{2.5}$, and $y = x + 1$.

2. **Tangency condition**: Centre is $(1, 2)$. The line in general form is $x - y + k = 0$. Distance from centre to line:

$$
d = \frac{|1 - 2 + k|}{\sqrt{1^2 + (-1)^2}} = \frac{|k-1|}{\sqrt{2}}
$$

Set $d = r = \sqrt{5}$:

$$
\frac{|k-1|}{\sqrt{2}} = \sqrt{5} \quad \rightarrow \quad |k-1| = \sqrt{10} \quad \rightarrow \quad k = 1 \pm \sqrt{10}
$$

---

## 10.5 Calculus with Kinematics and Extremes

**Example**: $s(t) = t^3 - 6t^2 + 9t + 2$, $t \geq 0$.

1. $v(t) = 3t^2 - 12t + 9$, $a(t) = 6t - 12$.

2. $v(t) = 0$ → $3t^2 - 12t + 9 = 0$ → $t^2 - 4t + 3 = 0$ → $t = 1$ or $t = 3$.

   Sign analysis: $t < 1$: $v > 0$; $1 < t < 3$: $v < 0$; $t > 3$: $v > 0$.
   The particle changes direction at $t = 1$ and $t = 3$.

3. $v(2) = 12 - 24 + 9 = -3$, $a(2) = 12 - 12 = 0$.

4. Displacement from $t = 0$ to $t = 4$: $s(4) - s(0) = (64 - 96 + 36 + 2) - 2 = 6 - 2 = 4$.

---

## 10.6 Permutations, Combinations, Binomial Theorem

**Example 1**: Choose 4 people from 5 boys and 3 girls, with at least 2 girls.

Total ways: $C(8, 4) = 70$.

Subtract cases with 0 girls ($C(5, 4) = 5$) and 1 girl ($C(3, 1) \cdot C(5, 3) = 3 \cdot 10 = 30$).

Answer: $70 - 5 - 30 = 35$.

**Example 2**: Find the constant term in $(x + 2/x)^6$.

General term: $\binom{6}{r} x^{6-r} (2/x)^r = \binom{6}{r} 2^r x^{6-2r}$.

Constant term means $6 - 2r = 0$ → $r = 3$.

Term: $\binom{6}{3} 2^3 = 20 \cdot 8 = 160$.

---

## 10.7 Vectors and Geometry

**Example**: $\mathbf{a} = (1, 2)$, $\mathbf{b} = (3, -1)$.

1. $\mathbf{a} + \mathbf{b} = (4, 1)$, magnitude $|(4, 1)| = \sqrt{17}$.

2. A vector perpendicular to $\mathbf{a}$: $(2, -1)$ (since $1 \cdot 2 + 2 \cdot (-1) = 0$). Its unit vector is $(2, -1)/\sqrt{5}$.

3. $\mathbf{a} + t\mathbf{b} = (1 + 3t, 2 - t)$ is parallel to $(1, 2)$ means the ratios of components are equal:

$$
\frac{1 + 3t}{1} = \frac{2 - t}{2}
$$

Cross-multiply: $2 + 6t = 2 - t$ → $7t = 0$ → $t = 0$.

---

## 10.8 Calculus: Area and Tangents

**Example**: Find the tangent to $y = x^2$ at $(1, 1)$ and the area between the curve and the tangent from $x = 0$ to $x = 1$.

Tangent slope: $f'(x) = 2x$, so $f'(1) = 2$. Tangent equation: $y - 1 = 2(x - 1)$, or $y = 2x - 1$.

On $(0, 1)$, the curve $y = x^2$ is above the tangent $y = 2x - 1$. The area between them is:

$$
\int_0^1 [x^2 - (2x - 1)] dx = \int_0^1 (x^2 - 2x + 1) dx = \int_0^1 (x-1)^2 dx
$$

$$
= \left[\frac{(x-1)^3}{3}\right]_0^1 = 0 - \frac{(-1)^3}{3} = \frac{1}{3}
$$

---

## 10.9 Logarithmic/Exponential with Calculus

**Example**: $f(x) = e^{2x} \ln x$.

Using the product rule:

$$
f'(x) = 2e^{2x} \ln x + e^{2x} \cdot \frac{1}{x} = e^{2x} \left(2\ln x + \frac{1}{x}\right)
$$

---

## 10.10 Trigonometric with Calculus

**Example**: Find the tangent to $y = \sin(2x)$ at $x = \pi/4$.

$y' = 2\cos(2x)$. At $x = \pi/4$:

- $y = \sin(\pi/2) = 1$
- $y' = 2\cos(\pi/2) = 0$

The tangent is horizontal: $y = 1$.

---

## 10.11 Chapter Summary

Comprehensive problems often combine:
- Function properties + inequalities
- Exponentials/logarithms + composites + derivatives
- Trig identities + solving equations
- Lines & circles + discriminant + distance
- Kinematics + derivatives + displacement/velocity/acceleration
- Permutations/combinations + binomial theorem
- Vectors + geometry
- Calculus + area/tangents

**Review advice**: Master basic formulas, especially derivatives, integrals, trig identities, and combinatorics. Practice cross-topic problems. Watch for domain restrictions, sign conventions, radian/degree mode, and always check your solutions.
