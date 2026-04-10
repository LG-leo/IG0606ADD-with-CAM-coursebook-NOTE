# IGCSE 0606 Additional Mathematics Complete Notes (English)

> These notes are based on the Cambridge IGCSE Additional Mathematics (0606) 2025-2027 syllabus, arranged in a cognitive order covering all topics. Includes derivations, typical examples, and common pitfalls. Suitable for self-study.

---

## Table of Contents

- [Chapter 0: Sequences, Permutations, Combinations and Binomial Theorem](#chapter-0-sequences-permutations-combinations-and-binomial-theorem)
- [Chapter 1: Vectors and Rates of Change](#chapter-1-vectors-and-rates-of-change)
- [Chapter 2: Quadratic Functions](#chapter-2-quadratic-functions)
- [Chapter 3: Functions (Linear, Cubic, Exponential, Logarithmic)](#chapter-3-functions-linear-cubic-exponential-logarithmic)
- [Chapter 4: Differentiation (Derivatives)](#chapter-4-differentiation-derivatives)
- [Chapter 5: Equations and Inequalities (Graphical Method)](#chapter-5-equations-and-inequalities-graphical-method)
- [Chapter 6: Integration (Indefinite and Definite Integrals)](#chapter-6-integration-indefinite-and-definite-integrals)
- [Chapter 8: Trigonometry](#chapter-8-trigonometry)
- [Chapter 9: Geometry (Straight Lines and Circles)](#chapter-9-geometry-straight-lines-and-circles)
- [Chapter 10: Comprehensive Applications](#chapter-10-comprehensive-applications)

---

# Chapter 0: Sequences, Permutations, Combinations and Binomial Theorem

This chapter is placed first for two purposes:
1. As an "intellectual warm‑up" to train algebraic manipulation and logical counting.
2. To avoid being interrupted later when these topics are needed.

## 0.1 Sequences

A sequence is an ordered list of numbers, e.g. 3, 7, 11, 15, …  
We focus on two common types: **arithmetic sequences** (adding a fixed value) and **geometric sequences** (multiplying by a fixed value).

The summation symbol ∑ means adding a series of numbers. For example:
$$
∑_{k=1}^{n} a_k = a_1 + a_2 + … + a_n
$$

**Basic rules**:
- Constant factor: $∑ (c·a_k) = c·∑ a_k$
- Sum/difference: $∑ (a_k ± b_k) = ∑ a_k ± ∑ b_k$
- Constant sum: $∑_{k=1}^{n} c = n c$

**Example**: Evaluate $∑_{k=1}^{4} (2k + 1)$.  
Solution: $= 2∑ k + ∑ 1 = 2(1+2+3+4) + 4 = 2×10 + 4 = 24$.

### 0.1.1 Arithmetic Sequences

**Definition**: From the second term onward, each term minus the previous term equals a constant $d$ (common difference).  
That is $a_{n+1} - a_n = d$.

**Example**: 3, 7, 11, 15, 19  
7-3=4, 11-7=4, … → common difference $d=4$.

**General term $a_n$**:
- First term $a_1 = a$ (denote first term by $a$).
- Second term $a_2 = a + d$.
- Third term $a_3 = a + 2d$.
- For the $n$‑th term we add $d$ $(n-1)$ times. So:
$$
a_n = a + (n-1)d
$$
Check: $n=1$ gives $a_1 = a + 0·d = a$.

**Example**: Given $a=5, d=3$, find the 10th term.  
$a_{10} = 5 + (10-1)×3 = 5+27 = 32$.

**Sum of the first $n$ terms** (derive, not memorise):

Write the sum twice, once forwards and once backwards:

Forward: $S = a + (a+d) + (a+2d) + … + (a+(n-1)d)$  
Backward: $S = (a+(n-1)d) + (a+(n-2)d) + … + a$

Add term‑wise: each pair sums to $2a + (n-1)d$, and there are $n$ pairs.  
Thus $2S = n·[2a+(n-1)d]$, so
$$
S_n = \frac{n}{2}[2a + (n-1)d]
$$
If the last term $l = a+(n-1)d$ is known, $S_n = \frac{n}{2}(a+l)$.

**Example**: Sum of 3,7,11,15,19.  
$a=3, d=4, n=5$, $S_5 = (5/2)[2·3+(5-1)·4] = (5/2)[6+16] = (5/2)·22 = 55$.

### 0.1.2 Geometric Sequences

**Definition**: From the second term onward, each term divided by the previous term equals a constant $r$ (common ratio).  
That is $a_{n+1} / a_n = r$.

**Example**: 2, 6, 18, 54, …  
6/2=3, 18/6=3, 54/18=3 → common ratio $r=3$.

**General term**:
$$
a_n = a r^{\,n-1}
$$

**Example**: $a=2, r=3$, find the 5th term.  
$a_5 = 2·3^{4} = 2·81 = 162$.

**Sum of the first $n$ terms**:

Let $S = a + ar + ar^2 + … + ar^{\,n-1}$.  
Multiply by $r$: $rS = ar + ar^2 + … + ar^{\,n-1} + ar^{\,n}$.  
Subtract: $S - rS = a - ar^{\,n}$ → $S(1-r) = a(1 - r^n)$.

- If $r = 1$, the sequence is constant $a, a, a, …$, then $S_n = n a$.
- If $r ≠ 1$,
$$
S_n = a\frac{1-r^n}{1-r}
$$

**Example**: Sum of 2,6,18,54 ($n=4$).  
$r=3$, $S_4 = 2·(1-3^4)/(1-3) = 2·(1-81)/(-2) = 2·(-80)/(-2) = 80$.

**Infinite sum**: If $|r| < 1$, then $r^n → 0$ and
$$
S_∞ = \frac{a}{1-r}
$$
(Condition: $|r|<1$; otherwise the series diverges.)

**Example**: $1 + 1/2 + 1/4 + 1/8 + …$  
$a=1, r=1/2$, $S_∞ = 1/(1-1/2) = 2$.

### Recurrence $u_{n+1} = a u_n + b$ (extension)

For $a ≠ 1$, find a constant $p$ such that $p = a p + b$ → $p = b/(1-a)$.  
Let $v_n = u_n - p$, then $v_{n+1} = a v_n$ (geometric).  
So $v_n = v_1·a^{n-1}$, thus $u_n = p + (u_1 - p)a^{n-1}$.

**Example**: $u_1=2$, $u_{n+1}=3u_n-4$.  
$p = -4/(1-3)=2$, $v_n = u_n-2$, $v_1=0$ → $u_n=2$ (constant).

> **Caution**: If $a=1$, the recurrence is arithmetic – do not use this method.

---

## 0.2 Permutations and Combinations

These count "how many possibilities". The key difference: **order matters or not**.

### 0.2.1 Multiplication Principle

If a task consists of $k$ steps, step 1 has $m_1$ ways, step 2 has $m_2$ ways, …, total ways = $m_1 × m_2 × … × m_k$.

**Example**: 3 roads from A to B, 4 roads from B to C → $3×4=12$ routes from A to C via B.

### 0.2.2 Permutations (order matters)

Choose $r$ distinct items from $n$ distinct items and arrange them in order.  
Number of permutations:
$$
P(n,r) = n(n-1)…(n-r+1) = \frac{n!}{(n-r)!}
$$

**Example**: Choose 3 out of 5 books and place them on a shelf (order matters).  
$P(5,3)=5×4×3=60$.

### 0.2.3 Combinations (order does not matter)

Number of ways to choose a set of $r$ items from $n$ distinct items:
$$
C(n,r) = \binom{n}{r} = \frac{n!}{r!(n-r)!}
$$

**Example**: Choose 2 out of 5 people to clean (no assignment of roles).  
$C(5,2)=10$.

**When to use which?**
| Scenario | Order matters? | Example |
|----------|----------------|---------|
| Queue, ranking, password | Yes | Choose 3 from 10 to stand in a line |
| Committee, lottery, team | No | Choose 3 from 10 to join a contest |

#### Extensions: Circular and repeated permutations

- **Circular permutation**: $n$ distinct objects around a circle (rotations considered same): $(n-1)!$ ways.  
  Example: 5 people around a table → $(5-1)! = 24$ seatings.
- **Permutations with repetition**: choose $r$ items from $n$ types, repetition allowed: $n^r$ ways.  
  Example: 4‑digit PIN (each digit 0‑9) → $10^4 = 10000$.

#### Basic probability with combinations

- Mutually exclusive events: $P(A ∪ B) = P(A) + P(B)$
- Independent events: $P(A ∩ B) = P(A)·P(B)$

**Example**: Choose 2 from 5 boys and 3 girls, probability of at least one girl.  
Total ways $C(8,2)=28$. No girl: $C(5,2)=10$.  
So $P = 1 - 10/28 = 9/14$.

> **Tip**: For "at least" problems, use the complement.

---

## 0.3 Binomial Theorem

**Question**: When expanding $(a+b)^n$, what are the coefficients?

Think of $(a+b)^n$ as $n$ brackets multiplied: $(a+b)(a+b)…(a+b)$.  
To get $a^{\,n-r}b^{\,r}$, we choose $r$ brackets to contribute $b$ and the rest $a$.  
Number of ways = $\binom{n}{r}$. Hence
$$
(a+b)^n = ∑_{r=0}^{n} \binom{n}{r} a^{\,n-r} b^{\,r} \qquad (n \text{ non‑negative integer})
$$

**Example**: $(x+2)^3$  
$r=0$: $\binom{3}{0}x^3·2^0 = x^3$  
$r=1$: $\binom{3}{1}x^2·2^1 = 3·2 x^2 = 6x^2$  
$r=2$: $\binom{3}{2}x^1·2^2 = 3·4 x = 12x$  
$r=3$: $\binom{3}{3}x^0·2^3 = 8$  
Result: $x^3+6x^2+12x+8$.

**General term** (the $(r+1)$‑th term, $r$ starting from 0):
$$
T_{r+1} = \binom{n}{r} a^{\,n-r} b^{\,r}
$$

**Application**: Find the constant term in $(2x - 1/x)^6$.  
Write as $(2x + (-1/x))^6$, $a=2x$, $b=-1/x$.  
General term: $\binom{6}{r}(2x)^{6-r}(-1/x)^r = \binom{6}{r}2^{6-r}(-1)^r x^{6-2r}$.  
Constant term ⇒ $6-2r=0$ ⇒ $r=3$.  
Then term = $\binom{6}{3}2^{3}(-1)^3 = 20×8×(-1) = -160$.

**Distinguish**:
- Binomial coefficient: $\binom{n}{r}$ (depends only on $n,r$).
- Coefficient of a term: the full numerical factor including signs and constants from $a,b$.

---

## 0.4 Properties of Binomial Coefficients (Pascal’s Triangle)

- Symmetry: $\binom{n}{r} = \binom{n}{n-r}$
- Recurrence: $\binom{n}{r} + \binom{n}{r-1} = \binom{n+1}{r}$ (for $1 ≤ r ≤ n$)

Pascal’s Triangle arranges these coefficients in a triangular shape; each number is the sum of the two above it.

---

## 0.5 Chapter Summary

- **Arithmetic sequence**: constant difference $d$, $a_n = a+(n-1)d$, $S_n = (n/2)[2a+(n-1)d]$.
- **Geometric sequence**: constant ratio $r$, $a_n = a r^{\,n-1}$, $S_n = na$ if $r=1$, else $a(1-r^n)/(1-r)$. Infinite sum $a/(1-r)$ when $|r|<1$.
- **Permutations**: order matters, $P(n,r) = n!/(n-r)!$.
- **Combinations**: order irrelevant, $\binom{n}{r} = n!/(r!(n-r)!)$.
- **Binomial theorem**: $(a+b)^n = ∑_{r=0}^{n} \binom{n}{r} a^{\,n-r} b^{\,r}$.

---

# Chapter 1: Vectors and Rates of Change

## 1.1 Why start with vectors?

In physics, position, velocity, and acceleration are all quantities with both magnitude and direction – best described by **vectors**.  
**Rate of change** is the core of calculus: rate of change of position is velocity, rate of change of velocity is acceleration. Vectors give a geometric intuition for rates of change.

---

## 1.2 Basic Vector Concepts

### 1.2.1 Definition

A vector has magnitude and direction. In the plane, we write:
$$
\mathbf{v} = (v_x, v_y)
$$
or using unit vectors $\mathbf{i}, \mathbf{j}$:
$$
\mathbf{v} = v_x \mathbf{i} + v_y \mathbf{j}
$$
where $\mathbf{i}=(1,0), \mathbf{j}=(0,1)$.

### 1.2.2 Magnitude (length)
$$
\|\mathbf{v}\| = \sqrt{v_x^2 + v_y^2}
$$
Example: $\|(3,4)\| = √(9+16)=5$.

### 1.2.3 Unit vector
$$
\mathbf{u} = \frac{\mathbf{v}}{\|\mathbf{v}\|}
$$
Example: unit vector of (3,4) is $(3/5, 4/5)$.

### 1.2.4 Vector operations

- **Addition**: $(x_1,y_1)+(x_2,y_2) = (x_1+x_2, y_1+y_2)$ (parallelogram law).
- **Subtraction**: $\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A$ (tip minus tail).
- **Scalar multiplication**: $c(x,y) = (cx, cy)$. $c>0$ keeps direction, $c<0$ reverses direction.

Example: $\mathbf{u}=(1,2), \mathbf{v}=(3,-1)$ → $\mathbf{u}+\mathbf{v}=(4,1)$, $\mathbf{u}-\mathbf{v}=(-2,3)$, $2\mathbf{u}=(2,4)$.
#### Definition of Perpendicular
Two non-zero vectors u and v are perpendicular (orthogonal) iff their dot product is zero:
u · v = u_x * v_x + u_y * v_y = 0
Geometrically, the angle between them is 90°.

#### Horizontal Vector
A vector h is horizontal if its y-component is zero:
h = (h_x, 0), with h_x ≠ 0
Its direction is parallel to the x-axis (left or right).

#### Perpendicularity via Slopes
If both non-zero vectors are not vertical (i.e., their slopes exist), let their slopes be k₁ and k₂. Then
u ⟂ v  if and only if  k₁ · k₂ = -1

#### Special Case: Horizontal and Vertical
A horizontal vector h = (h_x, 0) is perpendicular to a vertical vector v = (0, v_y). In this case:
- The slope of h is 0
- The slope of v is undefined (infinite)
Dot product check: (h_x, 0) · (0, v_y) = 0 + 0 = 0, satisfying the perpendicular condition.

> Note: The zero vector is both perpendicular and parallel to every vector, but we usually exclude it in ordinary discussions.

---

## 1.3 Position Vector and Displacement

### 1.3.1 Position vector

Take a fixed origin $O$. The position of point $P$ is $\mathbf{r} = \overrightarrow{OP}$.  
If $P(x,y)$, then $\mathbf{r} = (x,y)$.  
**Distinguish**: $P(x,y)$ is a point; $\mathbf{r}=(x,y)$ is the vector from origin to $P$.

### 1.3.2 Displacement

Displacement from $A$ to $B$ is $\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A$.  
Example: $A(1,1), B(4,5)$ → displacement $(3,4)$, magnitude 5.

---
## 1.4 From Average Velocity to Instantaneous Velocity (Understanding Limits)

Let’s start with a simple example. Suppose an object moves along a straight line, and its position at time t is given by s(t) = t². We want to know how fast it is moving at the exact moment t = 1.

### How do we calculate average velocity?
From time 1 to time 1 + Δt, the distance traveled is s(1+Δt) − s(1). Average velocity = distance divided by Δt.

$$
\mathbf{v}(t) = \lim_{\Delta t\to 0} \frac{\mathbf{r}(t+\Delta t) - \mathbf{r}(t)}{\Delta t} = \left( \frac{dx}{dt}, \frac{dy}{dt} \right)
$$

The variation of speed over time：
$$
\mathbf{a}(t) = \frac{d\mathbf{v}}{dt} = \left( \frac{d^2 x}{dt^2}, \frac{d^2 y}{dt^2} \right)
$$

Let’s try smaller and smaller Δt:

- Δt = 0.5 : position goes from 1 to 2.25, distance = 1.25, average = 1.25 / 0.5 = 2.5
- Δt = 0.1 : position goes from 1 to 1.21, distance = 0.21, average = 0.21 / 0.1 = 2.1
- Δt = 0.01 : position goes from 1 to 1.0201, distance = 0.0201, average = 0.0201 / 0.01 = 2.01
- Δt = 0.001 : average ≈ 2.001

As Δt gets closer and closer to 0, the average velocity gets closer and closer to 2. That “closer value” is the **instantaneous velocity** at t = 1. We write v(1) = 2.

This is the idea of a limit: we never let Δt become exactly 0 (because that would give 0/0, which is meaningless), but we let it approach 0 and see what number the average velocity approaches.

---

## 1.5 From Acceleration to Velocity and Position (Using Integration)

In physics, acceleration a(t) is the rate of change of velocity v(t). If we know acceleration and want to recover velocity, we need to do the opposite of differentiation – that is **integration**.

The basic formulas (for vectors, but they work for one‑dimensional motion too):

- Velocity v(t) = ∫ a(t) dt + initial velocity v₀
- Position r(t) = ∫ v(t) dt + initial position r₀

If we know the acceleration $\mathbf{a}(t)$ and the condition $\mathbf{v}(0) = \mathbf{v}_0,\ \mathbf{r}(0) = \mathbf{r}_0$，then：
$$
\mathbf{v}(t) = \int \mathbf{a}(t)\, dt + \mathbf{v}_0
$$
$$
\mathbf{r}(t) = \int \mathbf{v}(t)\, dt + \mathbf{r}_0
$$
Integration is carried out component by component.

**Example: Projectile motion**  
A ball is thrown from the ground. Its initial velocity has horizontal component v₀x and vertical component v₀y. Gravity pulls downward with acceleration g. So a(t) = (0, -g).

First, integrate acceleration to get velocity:  
v_x(t) = ∫ 0 dt = constant = v₀x  
v_y(t) = ∫ (-g) dt = -g t + v₀y  
Thus v(t) = (v₀x, v₀y - g t)

Next, integrate velocity to get position (starting from (0,0)):  
x(t) = ∫ v₀x dt = v₀x · t  
y(t) = ∫ (v₀y - g t) dt = v₀y · t - ½ g t²

These are the well‑known equations of projectile motion.

---

## 1.6 Relative Motion (Adding Velocities)

If you stand on the ground and watch a moving object, its velocity is actually the sum of two parts: the object’s velocity relative to a moving reference frame, plus the velocity of that reference frame itself.

A simple rule: **Absolute velocity = Relative velocity + Velocity of the reference frame**.  
In symbols: v_(A/C) = v_(A/B) + v_(B/C)

**Example**: A boat can move at 4 m/s east relative to the water. The water current flows north at 3 m/s. What is the boat’s velocity relative to the ground?

Choose east as the positive x‑direction, north as positive y.  
Boat’s velocity relative to water = (4, 0)  
Water’s velocity relative to ground = (0, 3)  
Then boat’s velocity relative to ground = (4, 0) + (0, 3) = (4, 3)

Magnitude = √(4² + 3²) = 5 m/s  
Direction = east of north, angle = arctan(3/4) ≈ 36.87°

---

## 1.7 More Examples to Help You Practice

**Example 1: Given position, find velocity and acceleration**  
A particle moves with position vector r(t) = (t³ − 3t, t² − 2t).  
Velocity v(t) is the derivative of position (differentiate each component):  
v_x = 3t² − 3, v_y = 2t − 2, so v(t) = (3t² − 3, 2t − 2)  
Acceleration a(t) is the derivative of velocity: a_x = 6t, a_y = 2, so a(t) = (6t, 2)  
At t = 2: v = (9, 2), a = (12, 2)

**Example 2: Given acceleration and initial conditions, find motion**  
Acceleration a(t) = (6t, 4), initial velocity v₀ = (1, 0), initial position r₀ = (0, 0).  
First integrate to get velocity:  
∫6t dt = 3t², plus the initial x‑component 1 → v_x = 3t² + 1  
∫4 dt = 4t, plus the initial y‑component 0 → v_y = 4t  
So v(t) = (3t² + 1, 4t)  

Then integrate velocity to get position:  
∫(3t² + 1) dt = t³ + t, plus initial x = 0 → x = t³ + t  
∫4t dt = 2t², plus initial y = 0 → y = 2t²  
Thus r(t) = (t³ + t, 2t²)

**Example 3: One‑dimensional motion (simpler)**  
Displacement s(t) = 3t² − 2t + 1  
Velocity v(t) = 6t − 2  
Acceleration a(t) = 6

---

## 1.8 Chapter Summary

In this chapter we started with vectors and saw that position, velocity, and acceleration can all be represented as vectors.

- Average velocity = change in position divided by time interval. When the time interval approaches zero, the limit of the average velocity is the **instantaneous velocity**.
- Velocity is the derivative (rate of change) of position; acceleration is the derivative of velocity.
- Going the other way: given acceleration, we can use **integration** to find velocity; given velocity, we can integrate to find position.
- For relative motion: absolute velocity = relative velocity + velocity of the reference frame.
- Finally, the zero vector has no fixed direction, but by convention it is considered parallel to every vector (and opposite vectors are also parallel).

If some of the differentiation or integration steps feel unfamiliar, don’t worry – they will be explained in detail in Chapters 4 and 6. For now, just focus on understanding the relationships between position, velocity, and acceleration.

---

# Chapter 2: Quadratic Functions

## 2.1 Forms and Graph

$f(x)=ax^2+bx+c$ ($a≠0$) is a parabola.
- $a>0$: opens upward; $a<0$: opens downward.
- Vertex at $x = -b/(2a)$, $y = f(-b/(2a))$.
- Axis of symmetry/Vertex point x coordinate axis: $x = -b/(2a)$.
- Vertex point y coordinate axis: $y = 4ac-b^2/(4a)$.

**Example**: $f(x)=2x^2-4x+1$, vertex $x=4/4=1$, $y=2-4+1=-1$.

## 2.2 Vertex and Range

Complete the square: $f(x)=a(x + b/(2a))^2 + (4ac-b^2)/(4a)$.

Range depends on opening:
- $a>0$: $[f_{\min}, ∞)$
- $a<0$: $(-∞, f_{\max}]$

**Example**: $f(x)=x^2-4x+3 = (x-2)^2-1$, vertex $(2,-1)$, range $[-1,∞)$.

## 2.3 Discriminant and Roots

For $ax^2+bx+c=0$, $Δ = b^2-4ac$:
- $Δ>0$: two distinct real roots
- $Δ=0$: one repeated root
- $Δ<0$: no real roots

**Example**: $x^2-3x+2=0$, $Δ=9-8=1>0$, roots 1 and 2.

## 2.4 Quadratic Inequalities

Solve $ax^2+bx+c > 0$ (or $<0$):
- Find roots, then determine intervals using the sign of $a$.

**Example**: $x^2-4x+3>0$ → $(x-1)(x-3)>0$ → $x<1$ or $x>3$.

---

# Chapter 3: Functions (Linear, Cubic, Exponential, Logarithmic)

**Goal**: Master common function types, their graphs, rates of change, inverse and composite functions, preparing for differentiation.

## 3.1 Basic Function Concepts

A function assigns each input $x$ (in the domain) exactly one output $y=f(x)$.  
We care about how $y$ changes as $x$ changes – the **rate of change**.

- Domain: set of allowable $x$.
- Range: set of possible $y$.

Example: $f(x)=x^2$, domain all reals, range $[0,∞)$.

## 3.2 Linear Functions $f(x)=mx+c$

### 3.2.1 Form and Graph

Straight line, slope $m$ = increase in $y$ per unit increase in $x$, intercept $c = f(0)$.  
**Rate of change**: constant $m$.

### 3.2.2 Slope from two points
$$
m = \frac{y_2-y_1}{x_2-x_1}
$$
For linear functions, average = instantaneous.

**Example**: Line through $(1,3)$ and $(4,9)$: $m=(9-3)/(4-1)=6/3=2$.

## 3.3 Cubic Functions $f(x)=ax^3+bx^2+cx+d$

Graph has an “S” shape (or reverse S), may have one local max and one local min (or none, e.g. $f(x)=x^3$ which has a point of inflection – IGCSE does not require the term “inflection point”, just describe the change in curvature).  
Rate of change (derivative) is quadratic, can have two zeros (for extreme points).

**Example**: $f(x)=x^3-3x$ – derivative $3x^2-3$; local max at $x=-1$, local min at $x=1$.

## 3.4 Exponential function $f(x) = a^x$ $(a>0, a≠1)$

### 3.4.1 Form and Graph

Exponential functions grow (or decay) extremely fast. When $a>1$, $f(x)$ grows explosively as $x$ increases; when $0<a<1$, $f(x)$ approaches 0 as $x$ increases.  
The graph passes through $(0,1)$.

### 3.4.2 Rate of change – numerical approximation

Take $f(x)=2^x$ as an example. Compute the average rate of change at $x=1$ for different $Δx$:

| $Δx$ | average rate $(2^{1+Δx} - 2) / Δx$ |
|------|----------------------------------|
| 0.1  | $(2^{1.1} - 2)/0.1 ≈ (2.1435 - 2)/0.1 = 1.435$ |
| 0.01 | $(2^{1.01} - 2)/0.01 ≈ (2.0145 - 2)/0.01 = 1.45$ |
| 0.001| about 1.4427 |

As $Δx → 0$, the average rate approaches $2·ln(2) ≈ 1.386$ (where $ln(2) ≈ 0.6931$). The approximate values in the table (1.435, 1.45, 1.4427) have not fully converged due to precision, but the trend is clear.

**Important observation**: The rate of change of an exponential function is proportional to the function value itself. That is, the instantaneous rate of change is $f'(x) = a^x · ln(a)$.  
For example, $f(1)=2$ gives a rate ≈ 1.386; $f(2)=4$ gives a rate ≈ 2.772 (exactly twice). When the function value doubles, the rate also doubles.

**Special natural exponential function**: $f(x) = e^x$ (with $e ≈ 2.71828$). Since $ln(e)=1$, its rate of change equals itself: $f'(x) = e^x$.

## 3.5 Logarithmic Functions $f(x)=\log_a x$ $(a>0, a≠1)$

Inverse of exponential. Domain $x>0$, range all reals.  
$f(x)=\ln x$ (natural log) has derivative $1/x$ (to be learned).  
Rate of change decreases as $x$ increases.

**Numerical approximation for $\ln x$ at $x=1$**:

| $Δx$ | $(\ln(1+Δx)-0)/Δx$ |
|------|---------------------|
| 0.1  | 0.9531 |
| 0.01 | 0.9950 |
| 0.001| 0.9995 |

Limit = 1. At $x=2$, limit = 0.5; at $x=10$, limit = 0.1.

## 3.6 Comparison of Rates of Change

| Function type | Rate characteristic | (Derivative later) |
|---------------|----------------------|---------------------|
| Linear $mx+c$ | constant | $m$ |
| Quadratic $ax^2+bx+c$ | changes linearly with $x$ | $2ax+b$ |
| Cubic | changes quadratically | quadratic function |
| Exponential $a^x$ | proportional to $f(x)$ | $a^x \ln a$ |
| Logarithmic $\log_a x$ | decreases, ~ $1/x$ | $1/(x\ln a)$ |

## 3.7 Inverse and Composite Functions

### 3.7.1 Inverse function

- A **one‑to‑one** function has an inverse.  
- $f^{-1}(y)=x ⇔ f(x)=y$.  
- Graphs of $f$ and $f^{-1}$ are symmetric about $y=x$.

**Example**: $f(x)=2x+1$ → $f^{-1}(x)=(x-1)/2$.  
$f(x)=x^2$ on whole reals is not one‑to‑one; restrict domain to $x≥0$ → $f^{-1}(x)=√x$.

### 3.7.2 Composite function

$(f∘g)(x) = f(g(x))$. Order matters generally.

**Example**: $f(x)=x^2$, $g(x)=x+1$ → $f(g(x))=(x+1)^2$, $g(f(x))=x^2+1$.

## 3.8 Absolute Value Function Transformations

$y=|f(x)|$: reflect the part of $y=f(x)$ where $y<0$ above the $x$‑axis.  
Example: $f(x)=x^3-3x$; its absolute value has cusps where the original crosses zero.

## 3.9 Comprehensive Examples

**Example 1**: $f(x)=3x+2$, average rate on $[1,3] = (11-5)/(2)=3$, same as instantaneous.

**Example 2**: $f(x)=x^2$, average rate from $x=2$ to $2.1 = (4.41-4)/0.1=4.1$; to $2.01$ → 4.01, approaching 4.

**Example 3**: Compare $2^x$ and $x^2$ at $x=4$: $2^4=16$, $2^5=32$ (avg rate 16); $4^2=16$, $5^2=25$ (avg rate 9). Exponential grows faster.

## 3.10 Chapter Summary

- Linear: constant rate.
- Quadratic: rate changes linearly.
- Cubic: rate changes quadratically.
- Exponential: rate ∝ function value.
- Logarithmic: rate ∝ $1/x$.
- One‑to‑one required for inverse; composition order matters.
- $|f(x)|$ reflects negative parts.

---

# Chapter 4: Differentiation (Derivatives)

**Learning path**:  
4.1–4.3 → polynomials and chain rule (Paper 1 core)  
4.4–4.5 → trig, exponential, log derivatives (advanced)  
4.6–4.7 → tangents, extrema, kinematics (applications)

## 4.1 What is a Derivative?

Derivative = instantaneous rate of change.

- Average rate over $[x, x+Δx]$: $(f(x+Δx)-f(x))/Δx$.
- Instantaneous rate: limit as $Δx→0$, denoted $f'(x)$ or $dy/dx$.

**Geometric meaning**: $f'(a)$ is the slope of the tangent line at $(a, f(a))$.

## 4.2 Limit Intuition

**Indeterminate form $0/0$**: factor and cancel.

Example: $\lim_{x→2} (x^2-4)/(x-2) = \lim_{x→2} (x-2)(x+2)/(x-2) = \lim_{x→2} (x+2) = 4$.

> Note: $x$ approaches 2, not equals.

## 4.3 Polynomial Differentiation (Power Rule)

For $f(x)=x^n$ ($n$ rational):
$$
f'(x) = n x^{n-1}
$$

**Examples**:
- $x^2 → 2x$
- $x^3 → 3x^2$
- $x → 1$
- $1 → 0$
- $√x = x^{1/2} → (1/2)x^{-1/2} = 1/(2√x)$

**Constant multiple and sum/difference**:
- $(c·u)' = c·u'$
- $(u±v)' = u'±v'$

**Example**: $f(x)=3x^2-4x+5$ → $f'(x)=6x-4$.

> **Domain caution**: $f(x)=1/x$ defined for $x≠0$, derivative $-1/x^2$ also for $x≠0$.

### 4.3.1 Implicit differentiation (for relations like $x^2+y^2=r^2$)

Differentiate both sides w.r.t $x$, treating $y$ as a function of $x$:  
$2x + 2y·(dy/dx) = 0$ → $dy/dx = -x/y$ ($y≠0$).

## 4.4 Chain Rule (Composite Functions)

For $y = (ax+b)^n$, let $u=ax+b$:
$$
dy/dx = (dy/du)·(du/dx) = n u^{n-1}·a = a n (ax+b)^{n-1}
$$

**Examples**:
- $(2x+1)^3$ → $3(2x+1)^2·2 = 6(2x+1)^2$
- $1/(x+1) = (x+1)^{-1}$ → $-(x+1)^{-2}·1 = -1/(x+1)^2$
- $√(3x-2) = (3x-2)^{1/2}$ → $(1/2)(3x-2)^{-1/2}·3 = 3/(2√(3x-2))$

## 4.5 Derivatives of Trig, Exponential, Log (Advanced)

> **⚠️ Radians only!** Put your calculator in Rad mode.

### 4.5.1 Trigonometric functions
$$
\frac{d}{dx} sin x = cos x
$$
$$
\frac{d}{dx} cos x = - sin x
$$
$$
\frac{d}{dx} tan x = sec^2 x
$$

**Examples**:
- $3 sin x → 3 cos x$
- $cos(2x)$ → $- sin(2x)·2 = -2 sin 2x$
- $tan(3x)$ → $sec^2(3x)·3 = 3 sec^2(3x)$

### 4.5.2 Exponential and Logarithmic
$$
\frac{d}{dx} e^x = e^x
$$
$$
\frac{d}{dx} a^x = a^x \ln a \quad (a>0, a≠1)
$$
$$
\frac{d}{dx} \ln x = \frac{1}{x}
$$
$$
\frac{d}{dx} \log_a x = \frac{1}{x\ln a}
$$

**Examples**:
- $e^{2x}$ → $e^{2x}·2 = 2e^{2x}$
- $2^x$ → $2^x \ln 2$
- $\ln(3x+1)$ → $\frac{1}{3x+1}·3 = \frac{3}{3x+1}$

## 4.6 Tangents and Normals (Three‑Step Method)

1. **Find the point of tangency**: $(a, f(a))$.
2. **Find slope**: $m = f'(a)$.
3. **Write equation**: $y - f(a) = m(x-a)$.

**Example**: $f(x)=x^2$ at $x=1$: $f(1)=1$, $f'(x)=2x$, $f'(1)=2$ → tangent: $y-1=2(x-1)$ → $y=2x-1$.

**Normal**: perpendicular, slope $m_{\text{normal}} = -1/m$ (if $m≠0$).  
Above normal: $y-1 = -\frac12 (x-1)$.

> **⚠️ Critical trap**:  
> - "tangent at point $P$" → $P$ is the point of tangency.  
> - "tangent passing through point $P$" → $P$ may not be the point of tangency; set unknown point of tangency $(a, f(a))$, write tangent, then substitute $P$ to solve for $a$.

## 4.7 Extreme Values (Maxima and Minima)

**Procedure**:
1. Find $f'(x)$.
2. Solve $f'(x)=0$ → stationary points.
3. Use first derivative test (sign change):
   - Left positive, right negative → local maximum.
   - Left negative, right positive → local minimum.
   - Same sign on both sides → not an extremum (e.g. $x^3$ at $0$).

**Alternative (second derivative test)**:  
If $f'(a)=0$ and $f''(a)>0$ → local minimum; $f''(a)<0$ → local maximum. If $f''(a)=0$, test fails.

**Example**: $f(x)=x^3-3x$.  
$f'(x)=3x^2-3=0$ → $x=±1$.  
- $x=-1$: left $f'(-2)=9>0$, right $f'(0)=-3<0$ → maximum, $f(-1)=2$.  
- $x=1$: left $f'(0)=-3<0$, right $f'(2)=9>0$ → minimum, $f(1)=-2$.

## 4.8 Kinematics (Motion along a line)

For displacement $s(t)$:
- Velocity $v(t) = ds/dt$ (rate of change of displacement).
- Acceleration $a(t) = dv/dt = d^2s/dt^2$.

**Direction**:  
$v(t)>0$ → moving in positive direction; $v(t)<0$ → negative direction; $v(t)=0$ → instantaneously at rest. If $v$ changes sign, the particle reverses direction.

**Example**: $s(t)=t^3-6t^2+9t$.  
$v(t)=3t^2-12t+9=3(t-1)(t-3)$.  
$v=0$ at $t=1,3$. Sign: $t<1$: $v>0$; $1<t<3$: $v<0$; $t>3$: $v>0$ → direction changes at $t=1$ and $t=3$.

**Example**: $v(t)=2t^2-5t+3$, $a(t)=4t-5$, $a(3)=7$.

## 4.9 Chapter Summary (Quick Reference)

| Task | How |
|------|-----|
| Derivative of $x^n$ | $n x^{n-1}$ |
| Derivative of $(ax+b)^n$ (chain rule) | $a n (ax+b)^{n-1}$ |
| Derivative of $sin x$ | $cos x$ |
| Derivative of $cos x$ | $- sin x$ |
| Derivative of $tan x$ | $sec^2 x$ |
| Derivative of $e^x$ | $e^x$ |
| Derivative of $\ln x$ | $1/x$ |
| Tangent line | three‑step method |
| Max/min | solve $f'(x)=0$, test sign change |
| Kinematics | $v=ds/dt$, $a=dv/dt$, $v=0$ and sign change → turning point |

---

# Chapter 5: Equations and Inequalities (Graphical Method)

**Goal**: Use graphs (especially sketches based on derivatives) to solve equations and inequalities, understand the link between intersections and solutions, and handle absolute value transformations.

## 5.1 Solutions and Intersections

**Key idea**: Solutions of $f(x)=g(x)$ are the $x$‑coordinates of intersection points of $y=f(x)$ and $y=g(x)$.  
Special case $f(x)=0$ → intersections with the $x$‑axis (zeros).

**Example**: $x^2-3x+2=0$ → graph of $y=x^2-3x+2$ crosses $x$‑axis at $x=1,2$.

## 5.2 Sketching Graphs Using Derivatives

For a sketch, find:
- Intercepts ($x$‑ and $y$‑intercepts)
- Monotonicity (where increasing/decreasing)
- Extremes (max/min)
- End behaviour as $x→±∞$

**Steps**:
1. Find $f'(x)$, solve $f'(x)=0$ → stationary points.
2. Classify each stationary point (max/min) using sign of $f'$.
3. Compute $f$ at those points and at $x=0$.
4. Consider $x→±∞$ (look at leading term).

**Example**: $f(x)=x^3-3x$  
$f'(x)=3x^2-3=0$ → $x=±1$.  
$x=-1$: max, $f(-1)=2$; $x=1$: min, $f(1)=-2$.  
$f(0)=0$. As $x→∞$, $f→∞$; as $x→-∞$, $f→-∞$.

## 5.3 Solving Inequalities with Graphs

**$f(x)>0$** → $x$ where graph is above $x$‑axis.

**Example**: $x^2-3x+2>0$ → graph opens upward, zeros at 1,2 → above axis for $x<1$ or $x>2$.

**Example**: $x^3-3x<0$ → sketch shows negative intervals: $x<-√3$ or $0<x<√3$ (since $√3≈1.732$).

## 5.4 Absolute Value Equations and Inequalities

$y=|f(x)|$: reflect negative parts of $f(x)$ above the $x$‑axis.

**Equation $|f(x)|=k$ ($k>0$)** ⇔ $f(x)=k$ or $f(x)=-k$.

**Inequality $|f(x)|<k$** ⇔ $-k < f(x) < k$.

**Example**: $|x^2-3x+2|<1$ → $-1 < x^2-3x+2 < 1$.  
Left inequality $x^2-3x+3>0$ always true (discriminant <0).  
Right inequality $x^2-3x+1<0$ → roots $(3±√5)/2$ → solution $(3-√5)/2 < x < (3+√5)/2$.

## 5.5 Using Derivatives for Complex Inequalities

**Example**: $2x/(x^2+1) > 0$ → denominator always positive → $2x>0$ → $x>0$.

**Example**: $x e^{-x} > 0$ → $e^{-x}>0$ always → $x>0$.

**Example**: $\ln x > 0$ → $x>1$.

## 5.6 Intersection of Two Functions and Inequalities

$f(x) > g(x)$ → $y=f(x)$ above $y=g(x)$.

Procedure: find intersections of $f$ and $g$, then test an $x$ in each interval.

**Example**: $x^2 < 2x+3$ → $x^2-2x-3<0$ → $(x-3)(x+1)<0$ → $-1<x<3$.

## 5.7 Comprehensive Examples

**Example 1**: $f(x)=x^3-6x^2+9x = x(x-3)^2$.  
$f(x)>0$ when $x>0$ and $x≠3$ → $(0,3)∪(3,∞)$.

**Example 2**: $|x^2-4x+3|=2$.  
Case 1: $x^2-4x+3=2$ → $x^2-4x+1=0$ → $x=2±√3$.  
Case 2: $x^2-4x+3=-2$ → $x^2-4x+5=0$, discriminant $16-20<0$ → no real.  
Solutions: $2+√3$ and $2-√3$.

**Example 3**: $|x-1| > |2x+3|$ → square both sides: $(x-1)^2 > (2x+3)^2$ → $x^2-2x+1 > 4x^2+12x+9$ → $0 > 3x^2+14x+8$ → $3x^2+14x+8<0$. Roots: $(-14±√(196-96))/6 = (-14±10)/6$ → $-4$ and $-2/3$. Parabola opens up → inequality holds between roots: $-4 < x < -2/3$.

## 5.8 Chapter Summary

| Problem | Method |
|---------|--------|
| $f(x)=0$ | $x$‑intercepts of $f$ |
| $f(x)=g(x)$ | intersection of graphs |
| $f(x)>0$ | where graph above $x$‑axis |
| $f(x)<g(x)$ | where $f$ below $g$ |
| $|f(x)|=k$ | solve $f(x)=±k$ |
| $|f(x)|<k$ | $-k<f(x)<k$ |
| Complex inequality | sketch with derivative first |

---

# Chapter 6: Integration (Indefinite and Definite Integrals)

**Learning path**:  
6.1–6.3 → indefinite integrals (antiderivatives)  
6.4–6.5 → definite integrals and area  
6.6 → integration in kinematics

## 6.1 What is Integration?

Integration is the reverse operation of differentiation (finding antiderivative).

**Example**: If $f'(x)=2x$, what is $f(x)$? $f(x)=x^2+C$, where $C$ is any constant.  
Notation: $∫ 2x\, dx = x^2 + C$.

## 6.2 Basic Integration Formulas (reverse of differentiation)

### 6.2.1 Power rule ($n≠-1$)
$$
∫ x^n dx = \frac{x^{n+1}}{n+1} + C
$$

**Examples**:
- $∫ x^2 dx = x^3/3 + C$
- $∫ x^{-3} dx = x^{-2}/(-2) + C = -1/(2x^2) + C$
- $∫ √x dx = ∫ x^{1/2} dx = x^{3/2}/(3/2) = (2/3)x^{3/2} + C$

### 6.2.2 Special case $n=-1$
$$
∫ \frac{1}{x} dx = \ln|x| + C
$$

### 6.2.3 Exponential and logarithmic
$$
∫ e^x dx = e^x + C
$$
$$
∫ a^x dx = \frac{a^x}{\ln a} + C \quad (a>0, a≠1)
$$

### 6.2.4 Trigonometric (radians)
$$
∫ sin x dx = - cos x + C
$$
$$
∫ cos x dx = sin x + C
$$
$$
∫ sec^2 x dx = tan x + C
$$

## 6.3 Linearity of Integration
$$
∫ (a f(x) + b g(x)) dx = a∫ f(x) dx + b∫ g(x) dx
$$

**Example**: $∫(3x^2 - 4 sin x + 5e^x) dx = x^3 + 4 cos x + 5e^x + C$.

## 6.4 Definite Integrals and Area

**Definite integral** $∫_a^b f(x) dx$ gives the signed area between $y=f(x)$ and the $x$‑axis from $x=a$ to $x=b$ (above axis positive, below negative).

**Fundamental Theorem (Newton‑Leibniz)**: If $F'(x)=f(x)$, then
$$
∫_a^b f(x) dx = F(b) - F(a)
$$

**Example**: $∫_1^2 2x dx = [x^2]_1^2 = 4-1 = 3$.

**Total area** (absolute area): split at zeros, integrate absolute value or take $∫|f(x)|dx$.

**Example**: $y=x^2-1$ on $[-2,2]$. Zeros at $x=±1$.  
Total area = $∫_{-2}^{-1}(x^2-1)dx + ∫_{-1}^{1}(-(x^2-1))dx + ∫_{1}^{2}(x^2-1)dx = 4/3+4/3+4/3=4$.

## 6.5 Area Between Two Curves

If $f(x) ≥ g(x)$ on $[a,b]$, area between them is
$$
∫_a^b [f(x)-g(x)] dx
$$

**Steps**:
1. Find intersections (solve $f(x)=g(x)$).
2. Determine which function is above.
3. Integrate.

**Example**: $y=x^2$ and $y=2x$. Intersections: $x^2=2x$ → $x=0,2$. On $(0,2)$, $2x ≥ x^2$.  
Area = $∫_0^2 (2x - x^2) dx = [x^2 - x^3/3]_0^2 = (4-8/3)-0 = 4/3$.

## 6.6 Integration in Kinematics

Given acceleration $a(t)$:
- $v(t) = ∫ a(t) dt + v_0$ (initial velocity)
- $s(t) = ∫ v(t) dt + s_0$ (initial displacement)

**Example**: $a(t)=6t-2$, $v(0)=1$, $s(0)=0$.  
$v(t)=∫(6t-2)dt = 3t^2-2t + C$, $v(0)=1$ → $C=1$ → $v(t)=3t^2-2t+1$.  
$s(t)=∫(3t^2-2t+1)dt = t^3 - t^2 + t + D$, $s(0)=0$ → $D=0$ → $s(t)=t^3-t^2+t$.

**Displacement from $v(t)$**: $∫_{t_1}^{t_2} v(t) dt$.

**Example**: $v(t)=t^2-4t+3$, displacement from $t=1$ to $3$ = $∫_1^3 (t^2-4t+3)dt = [t^3/3 -2t^2+3t]_1^3 = (9-18+9)-(1/3-2+3) = 0 - (4/3) = -4/3$ (negative means opposite direction).

## 6.7 Chapter Summary

| Task | How |
|------|-----|
| $∫ x^n dx$ ($n≠-1$) | $x^{n+1}/(n+1) + C$ |
| $∫ 1/x dx$ | $\ln|x|+C$ |
| $∫ e^x dx$ | $e^x + C$ |
| $∫ sin x dx$ | $-cos x + C$ |
| $∫ cos x dx$ | $sin x + C$ |
| $∫ sec^2 x dx$ | $tan x + C$ |
| Definite integral $∫_a^b$ | $F(b)-F(a)$ |
| Area under curve | definite integral (watch sign) |
| Area between curves | $∫(top-bottom)dx$, find intersections |
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

In calculus we use **radians**.  
Definition: radian = arc length / radius. Full circle → $2π$ radians.  
$$
360° = 2π \text{ rad},\quad 180° = π \text{ rad},\quad 1° = π/180 \text{ rad}
$$

**Common conversions**:
- $0°=0$
- $30°=π/6$
- $45°=π/4$
- $60°=π/3$
- $90°=π/2$
- $180°=π$

> **⚠️ Critical**: Always set calculator to **Rad** mode when differentiating, integrating, or solving trig equations.

### 8.1.1 Unit circle applications

**Derivation of $\sin(180°-θ)=\sinθ$**: On unit circle, point for $θ$ is $(\cosθ,\sinθ)$; for $180°-θ$ the point is $(\cos(180°-θ),\sin(180°-θ))$. Symmetry about $y$‑axis gives same $y$‑coordinate.

**Special triangles**:
- $30°-60°-90°$: sides $1, √3, 2$ → $\sin30°=1/2$, $\cos30°=√3/2$, $\tan30°=1/√3$; $\sin60°=√3/2$, $\cos60°=1/2$.
- $45°-45°-90°$: sides $1,1,√2$ → $\sin45°=√2/2$, $\cos45°=√2/2$, $\tan45°=1$.

## 8.2 Six Trigonometric Functions (Unit Circle)

On unit circle ($x^2+y^2=1$), angle $θ$ from positive $x$‑axis:
- $\sinθ = y$
- $\cosθ = x$
- $\tanθ = y/x = \sinθ/\cosθ$
- $\secθ = 1/\cosθ$
- $\cscθ = 1/\sinθ$
- $\cotθ = 1/\tanθ = \cosθ/\sinθ$

**Signs (ASTC)**:
- Quadrant I (0°–90°): all positive
- II (90°–180°): only $\sin$ positive
- III (180°–270°): only $\tan$ positive
- IV (270°–360°): only $\cos$ positive

| Quadrant | sin | cos | tan | sec | csc | cot |
|----------|-----|-----|-----|-----|-----|-----|
| I | + | + | + | + | + | + |
| II | + | - | - | - | + | - |
| III | - | - | + | - | - | + |
| IV | - | + | - | + | - | - |

### 8.2.1 Sum‑to‑product formulas (extension)
$$
sin A + sin B = 2 sin((A+B)/2) cos((A-B)/2)
$$
$$
sin A - sin B = 2 cos((A+B)/2) sin((A-B)/2)
$$
$$
cos A + cos B = 2 cos((A+B)/2) cos((A-B)/2)
$$
$$
cos A - cos B = -2 sin((A+B)/2) sin((A-B)/2)
$$

**Example**: $sin75°+sin15° = 2 sin45° cos30° = 2·(√2/2)·(√3/2)=√6/2$.

## 8.3 Graphs of Trig Functions

### 8.3.1 $y = sin x$
- Domain: all reals, range $[-1,1]$, period $2π$
- Odd: $sin(-x) = - sin x$
- Zeros at $x = nπ$

### 8.3.2 $y = cos x$
- Range $[-1,1]$, period $2π$
- Even: $cos(-x) = cos x$
- Zeros at $x = π/2 + nπ$

### 8.3.3 $y = tan x$
- Domain: $x ≠ π/2 + nπ$, range all reals, period $π$
- Odd, vertical asymptotes at $x = π/2 + nπ$

## 8.4 Amplitude, Period, Transformations

For $y = A sin(Bx + C) + D$:
- $|A|$ = amplitude (vertical stretch)
- $2π/|B|$ = period (horizontal stretch)
- $-C/B$ = phase shift (horizontal translation)
- $D$ = vertical shift

**Example**: $y = 3 sin(2x + π/3)$ → amplitude 3, period $π$, shift left $π/6$.

## 8.5 Basic Trigonometric Identities

**Fundamental**:
$$
sin^2θ + cos^2θ = 1
$$
$$
sec^2θ = 1 + tan^2θ
$$
$$
csc^2θ = 1 + cot^2θ
$$

**Double‑angle** (commonly used):
$$
sin(2θ) = 2 sinθ cosθ
$$
$$
cos(2θ) = cos^2θ - sin^2θ = 2 cos^2θ - 1 = 1 - 2 sin^2θ
$$
$$
tan(2θ) = \frac{2 tanθ}{1 - tan^2θ}
$$

## 8.6 Proving Trigonometric Identities

Strategy: start with the more complicated side, convert everything to $sin$ and $cos$, simplify.

**Example 1**: Prove $tan x + cot x = sec x csc x$.

Left: $sin x/cos x + cos x/sin x = (sin^2 x + cos^2 x)/(sin x cos x) = 1/(sin x cos x)$  
Right: $1/(cos x)·1/(sin x) = 1/(sin x cos x)$ → equal.

**Example 2**: Prove $\frac{sinθ}{1+cosθ} + \frac{1+cosθ}{sinθ} = 2 cscθ$.

Common denominator: $\frac{sin^2θ + (1+cosθ)^2}{sinθ(1+cosθ)} = \frac{sin^2θ+1+2cosθ+cos^2θ}{sinθ(1+cosθ)} = \frac{2+2cosθ}{sinθ(1+cosθ)} = \frac{2(1+cosθ)}{sinθ(1+cosθ)} = 2/sinθ = 2 cscθ$.

## 8.7 Solving Trigonometric Equations

### 8.7.1 Basic form $sin x = k$

**Reference angle method**:
1. Reference angle $α = arcsin(|k|)$ (acute, $0≤α≤π/2$).
2. Determine quadrants based on sign of $k$:
   - $k ≥ 0$: solutions in QI and QII: $x = α$ and $x = π - α$.
   - $k < 0$: solutions in QIII and QIV: $x = π+α$ and $x = 2π-α$.
3. Add $2nπ$ for general solutions.

**Example**: $sin x = 1/2$ on $[0,2π)$ → $α=π/6$, solutions $π/6$ and $5π/6$.

**Example**: $sin x = -1/2$ → $α=π/6$, negative → $π+π/6=7π/6$ and $2π-π/6=11π/6$.

### 8.7.2 $cos x = k$
- $k ≥ 0$: $x = α$ and $x = 2π-α$ (QI and QIV)
- $k < 0$: $x = π-α$ and $x = π+α$ (QII and QIII)
General: $x = ±α + 2nπ$ (with $α = arccos(|k|)∈[0,π]$).

**Example**: $cos x = -1/2$ → $α=π/3$ → $π-π/3=2π/3$, $π+π/3=4π/3$.

### 8.7.3 $tan x = k$
- $α = arctan(|k|)$ in $(0,π/2)$.
- Solutions: $x = α + nπ$ (since period $π$).

**Example**: $tan x = √3$ → $α=π/3$ → $π/3$, $4π/3$ on $[0,2π)$.

**Example**: $tan x = -1$ → $α = -π/4$ → add $π$: $3π/4$, $7π/4$.

### 8.7.4 Equations requiring identities

**Example**: $2 sec^2 x + tan x - 3 = 0$, $0≤x<2π$.  
$sec^2 x = 1+tan^2 x$ → $2(1+tan^2 x)+tan x-3=0$ → $2 tan^2 x + tan x -1 =0$.  
Let $u=tan x$ → $2u^2+u-1=0$ → $u=1/2$ or $u=-1$.  
- $tan x = 0.5$: $α≈0.4636$, solutions $0.4636$ and $0.4636+π≈3.6052$.
- $tan x = -1$: $α = -π/4$, solutions $3π/4$ and $7π/4$.  
Final: $\{0.4636, 3.6052, 3π/4, 7π/4\}$.

> **⚠️ Always check domain**: exclude points where functions are undefined (e.g., $tan x$ at $π/2 + nπ$).

## 8.8 Chapter Summary

| Topic | Key points |
|-------|-------------|
| Radian measure | $180°=π$ rad, calculator must be in Rad |
| Six trig functions | $sin, cos, tan, sec, csc, cot$; domains and ranges |
| Graphs | $sin, cos$ period $2π$, $tan$ period $π$; amplitude, shift |
| Basic identities | $sin^2+cos^2=1$, $sec^2=1+tan^2$, $csc^2=1+cot^2$ |
| Proving identities | convert to $sin, cos$, common denominator, use $sin^2+cos^2=1$ |
| Solving trig equations | reference angle, quadrant signs, add periods, check domain |

---

# Chapter 9: Geometry (Straight Lines and Circles)

**Goal**: Master equations of lines and circles, find intersections, determine relative positions, and find tangents to circles.

**Learning path**:  
9.1–9.2 → line equations, slope, parallel/perpendicular  
9.3–9.4 → circle equations (standard, general), centre, radius  
9.5 → line‑circle intersection (discriminant)  
9.6 → tangents to circles (three cases)

## 9.1 Line Equations

### 9.1.1 Common forms
- Slope‑intercept: $y = mx + c$ ($m$ = slope, $c$ = y‑intercept)
- Point‑slope: $y - y_1 = m(x - x_1)$
- General: $Ax + By + C = 0$ (slope $m = -A/B$ if $B≠0$)

### 9.1.2 Slope from two points
$$
m = \frac{y_2-y_1}{x_2-x_1}
$$

### 9.1.3 Parallel and perpendicular
- Parallel: $m_1 = m_2$
- Perpendicular: $m_1·m_2 = -1$ (if both slopes exist)

**Example**: $y=2x+3$ slope 2. Parallel lines have slope 2; perpendicular slope $-1/2$.

## 9.2 Distance from a Point to a Line

Point $(x_0,y_0)$ to line $Ax+By+C=0$:
$$
d = \frac{|Ax_0+By_0+C|}{\sqrt{A^2+B^2}}
$$

**Example**: Distance from $(1,2)$ to $3x-4y+5=0$: $|3-8+5|/5 = 0$ (point lies on line).

## 9.3 Circle Equations

### 9.3.1 Standard form
Centre $(a,b)$, radius $r$:
$$
(x-a)^2 + (y-b)^2 = r^2
$$

**Example**: Centre $(2,-3)$, radius 4 → $(x-2)^2+(y+3)^2=16$.

### 9.3.2 General form
$$
x^2 + y^2 + 2gx + 2fy + c = 0
$$
- Centre: $(-g, -f)$
- Radius: $\sqrt{g^2+f^2-c}$ (must be positive)

**Example**: $x^2+y^2-4x+6y+9=0$ → $2g=-4$ → $g=-2$, $2f=6$ → $f=3$, $c=9$ → centre $(2,-3)$, radius $√(4+9-9)=2$.

## 9.4 Position of a Line and a Circle

Substitute line into circle → quadratic equation in $x$ (or $y$).  
Discriminant $Δ$:
- $Δ>0$: two distinct intersection points (secant)
- $Δ=0$: tangent (one intersection)
- $Δ<0$: no intersection (line misses circle)

**Example**: $y=x+1$ and $x^2+y^2=1$ → $x^2+(x+1)^2=1$ → $2x^2+2x=0$ → $2x(x+1)=0$ → two solutions → intersect.

## 9.5 Tangents to a Circle (Three Cases)

### 9.5.1 Given point of tangency $(x_1,y_1)$ on the circle

For circle $(x-a)^2+(y-b)^2=r^2$, tangent:
$$
(x_1-a)(x-a) + (y_1-b)(y-b) = r^2
$$

**Example**: Circle $x^2+y^2=5$, point $(1,2)$ → tangent $1·x + 2·y = 5$ → $x+2y=5$.

### 9.5.2 Given slope $m$

For centre $(a,b)$, radius $r$, lines with slope $m$ tangent to the circle:
$$
y - b = m(x-a) ± r\sqrt{1+m^2}
$$
If centre at origin: $y = mx ± r√(1+m^2)$.

**Example**: Circle $x^2+y^2=9$, slope 2 → $y = 2x ± 3√(1+4) = 2x ± 3√5$.

### 9.5.3 Tangent from an external point $(x_0,y_0)$

**Steps**: Let tangent have slope $m$, equation $y-y_0 = m(x-x_0)$. Write in general form, set distance from centre to line equal to radius, solve for $m$. Check also vertical lines ($x=x_0$) separately.

**Example**: Circle $x^2+y^2=4$, external point $(4,0)$. Let $y=m(x-4)$ → $mx - y -4m=0$. Centre $(0,0)$, distance $| -4m |/√(m^2+1) = 2$ → $4|m|/√(m^2+1)=2$ → $2|m|=√(m^2+1)$ → $4m^2=m^2+1$ → $3m^2=1$ → $m=±1/√3$. Tangents: $y = (1/√3)(x-4)$ and $y = -(1/√3)(x-4)$. Also check $x=4$: distance from centre to $x=4$ is $4$, not equal to radius → not tangent.

## 9.6 Comprehensive Examples

**Example 1**: Circle with centre on $y=2x$, passing through $(1,1)$ and $(2,3)$.  
Let centre $(a,2a)$. Then $(1-a)^2+(1-2a)^2 = (2-a)^2+(3-2a)^2$. Expand: $(1-2a+a^2)+(1-4a+4a^2) - [(4-4a+a^2)+(9-12a+4a^2)] =0$ → $(2-6a+5a^2)-(13-16a+5a^2)=0$ → $-11+10a=0$ → $a=1.1$. Centre $(1.1,2.2)$, radius squared $=(1-1.1)^2+(1-2.2)^2=0.01+1.44=1.45$. Equation $(x-1.1)^2+(y-2.2)^2=1.45$.

**Example 2**: Line $y=x+k$ tangent to $x^2+y^2=4$. Substitute: $x^2+(x+k)^2=4$ → $2x^2+2kx+k^2-4=0$. Discriminant $= (2k)^2 - 4·2·(k^2-4) = 4k^2-8k^2+32 = -4k^2+32 = 0$ → $k^2=8$ → $k=±2√2$.

## 9.7 Chapter Summary

| Topic | Key |
|-------|-----|
| Line equations | slope‑intercept, point‑slope, general |
| Parallel/perpendicular | $m_1=m_2$ or $m_1m_2=-1$ |
| Point‑line distance | $d = |Ax_0+By_0+C|/√(A^2+B^2)$ |
| Circle standard | $(x-a)^2+(y-b)^2=r^2$, centre $(a,b)$, radius $r$ |
| Circle general | $x^2+y^2+2gx+2fy+c=0$, centre $(-g,-f)$, radius $√(g^2+f^2-c)$ |
| Line‑circle intersection | discriminant of quadratic |
| Tangent cases | given point on circle, given slope, from external point |

---

# Chapter 10: Comprehensive Applications

**Goal**: Combine knowledge from previous chapters to solve typical cross‑topic problems, developing integrated mathematical thinking.

> Covers: functions, quadratics, polynomials, equations/inequalities, log/exponential, lines & circles, radian measure, trigonometry, permutations & combinations, binomial theorem, vectors, calculus (differentiation & integration).

## 10.1 Functions and Quadratics

**Example**: $f(x)=x^2-4x+3$.
1. Vertex and range: complete square $(x-2)^2-1$ → vertex $(2,-1)$, range $[-1,∞)$.
2. Max/min on $[0,3]$: vertex inside → min $-1$; endpoints $f(0)=3$, $f(3)=0$ → max $3$.
3. Solve $f(x)>0$ → $(x-1)(x-3)>0$ → $x<1$ or $x>3$.

## 10.2 Functions with Exponentials and Logarithms

**Example**: $f(x)=e^{2x}$, $g(x)=\ln x$.
1. $h(x)=f(g(x)) = e^{2\ln x}=e^{\ln(x^2)}=x^2$, domain $x>0$.
2. Solve $h(x)=e^4$ → $x^2=e^4$ → $x=e^2$ (positive root only).
3. $h'(x)=2x$.

## 10.3 Trigonometric Equations and Identities

**Example**: Solve $2 sin^2 x + cos x = 1$, $0≤x<2π$.  
$sin^2 x = 1-cos^2 x$ → $2(1-cos^2 x)+cos x =1$ → $2-2cos^2 x+cos x-1=0$ → $-2cos^2 x+cos x+1=0$ → $2cos^2 x - cos x -1=0$. Let $u=cos x$ → $2u^2-u-1=0$ → $u=1$ or $u=-1/2$.  
$cos x=1$ → $x=0$; $cos x=-1/2$ → $x=2π/3$ or $4π/3$. Solutions $\{0, 2π/3, 4π/3\}$.

## 10.4 Lines, Circles, and Vectors

**Example**: Circle $(x-1)^2+(y-2)^2=5$, line $y=x+k$.
1. For $k=1$, substitute: $(x-1)^2+(x+1-2)^2=5$ → $(x-1)^2+(x-1)^2=5$ → $2(x-1)^2=5$ → $x=1±√2.5$, $y=x+1$.
2. Tangency: centre $(1,2)$, distance from centre to line $x-y+k=0$: $d=|1-2+k|/√2 = |k-1|/√2$. Set $d=r=√5$ → $|k-1|/√2 = √5$ → $|k-1|=√10$ → $k=1±√10$.
3. Distance formula already used.

## 10.5 Calculus with Kinematics and Extremes

**Example**: $s(t)=t^3-6t^2+9t+2$, $t≥0$.
1. $v(t)=3t^2-12t+9$, $a(t)=6t-12$.
2. $v(t)=0$ → $t=1$ or $3$. Sign: $t<1$: $v>0$; $1<t<3$: $v<0$; $t>3$: $v>0$ → direction changes at $t=1$ and $t=3$.
3. $v(2)=12-24+9=-3$, $a(2)=12-12=0$.
4. Displacement $s(4)-s(0)= (64-96+36+2)-2 = 6-2=4$.

## 10.6 Permutations, Combinations, Binomial Theorem

**Example 1**: Choose 4 from 5 boys and 3 girls, at least 2 girls.  
Total $C(8,4)=70$. Subtract cases with 0 girls ($C(5,4)=5$) and 1 girl ($C(3,1)·C(5,3)=3·10=30$) → $70-5-30=35$.

**Example 2**: Constant term in $(x + 2/x)^6$.  
General term $\binom{6}{r} x^{6-r} (2/x)^r = \binom{6}{r} 2^r x^{6-2r}$. Constant ⇒ $6-2r=0$ ⇒ $r=3$ → term $=\binom{6}{3}2^3=20·8=160$.

## 10.7 Vectors and Geometry

**Example**: $\mathbf{a}=(1,2)$, $\mathbf{b}=(3,-1)$.
1. $\mathbf{a}+\mathbf{b}=(4,1)$, $|(4,1)|=√17$.
2. A vector perpendicular to $\mathbf{a}$: $(2,-1)$; unit vector $= (2,-1)/√5$.
3. $\mathbf{a}+t\mathbf{b}=(1+3t, 2-t)$ parallel to $(1,2)$ ⇒ $(1+3t)/1 = (2-t)/2$ ⇒ $2+6t = 2-t$ ⇒ $7t=0$ ⇒ $t=0$.

## 10.8 Calculus: Area and Tangents

**Example**: Find tangent to $y=x^2$ at $(1,1)$ and area between curve and tangent from $x=0$ to $1$.  
Tangent slope $2$, equation $y=2x-1$. Curve above tangent on $(0,1)$: area $=∫_0^1 [x^2-(2x-1)]dx = ∫_0^1 (x^2-2x+1)dx = ∫_0^1 (x-1)^2 dx = [(x-1)^3/3]_0^1 = 0 - (-1)^3/3 = 1/3$.

## 10.9 Logarithmic/Exponential with Calculus

**Example**: $f(x)=e^{2x} \ln x$.  
$f'(x) = 2e^{2x} \ln x + e^{2x}·(1/x) = e^{2x}(2\ln x + 1/x)$.

## 10.10 Trigonometric with Calculus

**Example**: Tangent to $y= sin(2x)$ at $x=π/4$.  
$y'=2 cos(2x)$. At $x=π/4$, $y= sin(π/2)=1$, $y'=2 cos(π/2)=0$ → tangent $y=1$.

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

**Review advice**: Master basic formulas, especially derivatives, integrals, trig identities, and combinatorics. Practice cross‑topic problems. Watch for domain, sign, radian/degree, and checking solutions.
