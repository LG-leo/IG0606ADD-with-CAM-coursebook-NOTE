# IGCSE 0606 Additional Mathematics Complete Notes (English)

> Based on Cambridge IGCSE Additional Mathematics (0606) syllabus 2025–2027.  
> Order follows cognitive progression: Sequences/Combinatorics → Vectors → Quadratics → Functions → Differentiation → Inequalities → Integration → Trigonometry → Geometry → Mixed Applications.  
> Contains step‑by‑step derivations, typical examples, common traps, and self‑study tips.

---

## Table of Contents

- [Topic 0 – Sequences, Permutations, Combinations, Binomial Theorem](#topic-0)
- [Topic 1 – Vectors and Rates of Change](#topic-1)
- [Topic 2 – Quadratic Functions](#topic-2)
- [Topic 3 – Functions (Linear, Cubic, Exponential, Logarithmic)](#topic-3)
- [Topic 4 – Differentiation](#topic-4)
- [Topic 5 – Equations and Inequalities (Graphical Methods)](#topic-5)
- [Topic 6 – Integration](#topic-6)
- [Topic 8 – Trigonometry](#topic-8)
- [Topic 9 – Coordinate Geometry (Lines and Circles)](#topic-9)
- [Topic 10 – Mixed Applications](#topic-10)

---

## Topic 0 – Sequences, Permutations, Combinations, Binomial Theorem

This chapter is placed first for two reasons:  
1. It serves as a “mental warm‑up” for algebraic manipulation and logical counting.  
2. It prevents interruptions later when these concepts are needed in calculus or probability.

### 0.1 Sequences

A sequence is an ordered list of numbers, e.g. 3, 7, 11, 15, …  
We focus on two common types: **arithmetic** (constant difference) and **geometric** (constant ratio).

**Summation notation** $\sum$ means add a series of terms:  
$$
\sum_{k=1}^{n} a_k = a_1 + a_2 + \dots + a_n
$$

**Basic rules**:  
- Constant factor: $\sum (c \cdot a_k) = c \sum a_k$  
- Sum/difference: $\sum (a_k \pm b_k) = \sum a_k \pm \sum b_k$  
- Constant: $\sum_{k=1}^{n} c = n c$

**Example**: Compute $\sum_{k=1}^{4} (2k + 1)$.  
Solution: $= 2\sum k + \sum 1 = 2(1+2+3+4) + 4 = 2·10 + 4 = 24$.

#### 0.1.1 Arithmetic sequences

**Definition**: The difference between consecutive terms is constant $d$ (common difference).  
$a_{n+1} - a_n = d$.

**Example**: 3, 7, 11, 15, 19 → $d = 4$.

**n‑th term**:  
$a_1 = a$ (first term).  
$a_2 = a + d$, $a_3 = a + 2d$, …  
After $n-1$ steps:  
$$
a_n = a + (n-1)d
$$

**Sum of first n terms** (derivation):  
Write $S = a + (a+d) + (a+2d) + \dots + (a+(n-1)d)$.  
Reverse: $S = (a+(n-1)d) + (a+(n-2)d) + \dots + a$.  
Add term‑wise: each pair sums to $2a + (n-1)d$, there are $n$ pairs.  
So $2S = n[2a + (n-1)d]$, hence  
$$
S_n = \frac{n}{2}[2a + (n-1)d]
$$
If the last term $l = a+(n-1)d$ is known: $S_n = \frac{n}{2}(a+l)$.

**Example**: Sum of 3,7,11,15,19.  
$a=3, d=4, n=5$ → $S_5 = \frac{5}{2}[6+16] = \frac{5}{2}·22 = 55$.

#### 0.1.2 Geometric sequences

**Definition**: Ratio between consecutive terms is constant $r$ (common ratio).  
$a_{n+1} / a_n = r$.

**Example**: 2, 6, 18, 54, … → $r = 3$.

**n‑th term**:  
$a_n = a r^{\,n-1}$.

**Sum of first n terms** (derivation):  
$S = a + ar + ar^2 + \dots + ar^{n-1}$.  
Multiply by $r$: $rS = ar + ar^2 + \dots + ar^{n-1} + ar^n$.  
Subtract: $S - rS = a - ar^n$ → $S(1-r) = a(1-r^n)$.  

**Important**: If $r = 1$, the sequence is constant $a, a, a, \dots$ and $S_n = n a$.  
If $r \neq 1$:  
$$
S_n = a\frac{1-r^n}{1-r}
$$

**Example**: Sum of 2,6,18,54 ($n=4$).  
$r=3 \neq 1$ → $S_4 = 2·\frac{1-81}{1-3} = 2·\frac{-80}{-2} = 80$.

**Infinite sum** (converges only when $|r| < 1$):  
$$
S_\infty = \frac{a}{1-r}
$$

**Example**: $1 + \frac12 + \frac14 + \frac18 + \dots$ → $a=1, r=\frac12$ → $S_\infty = \frac{1}{1-1/2}=2$.

#### 0.1.3 Recurrence $u_{n+1} = a u_n + b$ (extension)

For $a \neq 1$, find constant $p$ such that $p = a p + b$ → $p = \frac{b}{1-a}$.  
Let $v_n = u_n - p$, then $v_{n+1} = a v_n$ (geometric).  
Thus $v_n = v_1 a^{n-1}$, and $u_n = p + (u_1 - p) a^{n-1}$.

**Example**: $u_1=2$, $u_{n+1}=3u_n-4$.  
$p = \frac{-4}{1-3}=2$, $v_n = u_n-2$, $v_{n+1}=3v_n$, $v_1=0$ → $v_n=0$ → $u_n=2$ (constant).

> **Common trap**: When $a=1$, the recurrence is arithmetic – do not use this method.

### 0.2 Permutations and Combinations

These count “how many possibilities”. Difference: **order matters or not**.

#### 0.2.1 Multiplication principle

If a task can be done in $k$ steps, step $i$ has $m_i$ ways, total ways = $m_1 × m_2 × \dots × m_k$.

**Example**: 3 roads A→B, 4 roads B→C → total routes A→C = $3×4=12$.

#### 0.2.2 Permutations (order matters)

Number of ways to arrange $r$ distinct objects chosen from $n$ distinct objects:  
$$
P(n,r) = n(n-1)(n-2)\dots(n-r+1) = \frac{n!}{(n-r)!}
$$

**Example**: Choose 3 books from 5 and place on a shelf (order matters): $P(5,3)=5·4·3=60$.

#### 0.2.3 Combinations (order irrelevant)

Number of ways to choose $r$ objects from $n$ (unordered):  
$$
C(n,r) = \binom{n}{r} = \frac{P(n,r)}{r!} = \frac{n!}{r!(n-r)!}
$$

**Example**: Choose 2 people from 5 to clean (no distinction): $C(5,2)=10$.  
If choose a captain and a vice‑captain (order matters): $P(5,2)=20$.

**When to use which?**  
| Scenario | Order matters? | Example |
|----------|----------------|---------|
| Queue, ranking, password | Yes | 3 people from 10 standing in line |
| Committee, lottery, team | No | 3 people from 10 to form a team |

#### Extensions: circular permutations & repetitions

- **Circular** (rotations considered same): $(n-1)!$ arrangements.  
  Example: 5 people around a table → $(5-1)! = 24$.
- **Repetitions allowed**: $n^r$ ways.  
  Example: 4‑digit PIN (0‑9) → $10^4 = 10000$.

#### Probability with combinations (extension)

- Mutually exclusive: $P(A \cup B) = P(A) + P(B)$  
- Independent: $P(A \cap B) = P(A) \cdot P(B)$

**Example**: Choose 2 from 5 boys, 3 girls. Probability of at least one girl.  
Total choices $C(8,2)=28$, no girl $C(5,2)=10$ → probability $= 1 - 10/28 = 9/14$.

> **Trap**: “At least” problems often easier using complement.

### 0.3 Binomial Theorem

Expand $(a+b)^n$ for non‑negative integer $n$:  
$$
(a+b)^n = \sum_{r=0}^{n} \binom{n}{r} a^{\,n-r} b^{\,r}
$$

**Reason**: Each of the $n$ factors contributes either $a$ or $b$. To get $a^{n-r}b^r$, choose $r$ factors to give $b$; number of ways = $\binom{n}{r}$.

**Example**: $(x+2)^3$  
$r=0: \binom{3}{0}x^3·2^0 = x^3$  
$r=1: \binom{3}{1}x^2·2 = 6x^2$  
$r=2: \binom{3}{2}x·4 = 12x$  
$r=3: \binom{3}{3}·8 = 8$  
Result: $x^3+6x^2+12x+8$.

**General term** ( $(r+1)$-th term, $r$ starting from 0):  
$$
T_{r+1} = \binom{n}{r} a^{\,n-r} b^{\,r}
$$

**Application**: Find constant term in $\left(2x - \frac{1}{x}\right)^6$.  
Treat as $(2x + (-\frac1x))^6$.  
General term: $\binom{6}{r} (2x)^{6-r} \left(-\frac1x\right)^r = \binom{6}{r} 2^{6-r} (-1)^r x^{6-2r}$.  
Constant term: $6-2r=0$ → $r=3$.  
Value: $\binom{6}{3}·2^3·(-1)^3 = 20·8·(-1) = -160$.

**Distinguish**:  
- Binomial coefficient $\binom{n}{r}$  
- Coefficient of a term includes all numerical factors from $a$ and $b$.

### 0.4 Properties of binomial coefficients (Pascal’s triangle)

- **Symmetry**: $\binom{n}{r} = \binom{n}{n-r}$  
- **Recurrence**: $\binom{n}{r} + \binom{n}{r-1} = \binom{n+1}{r}$ (for $1 \le r \le n$)

---

## Topic 1 – Vectors and Rates of Change

### 1.1 Why start with vectors?

In physics, position, velocity and acceleration are **vectors** (magnitude + direction).  
The concept of **rate of change** is the core of calculus: velocity is the rate of change of position; acceleration is the rate of change of velocity. Vectors give geometric intuition for these rates.

### 1.2 Basic vector concepts

#### 1.2.1 Definition

A vector in the plane can be written as coordinates:  
$\mathbf{v} = (v_x, v_y)$ or using unit vectors $\mathbf{i}, \mathbf{j}$:  
$\mathbf{v} = v_x\mathbf{i} + v_y\mathbf{j}$, where $\mathbf{i}=(1,0),\ \mathbf{j}=(0,1)$.

#### 1.2.2 Magnitude (length)

$$
\|\mathbf{v}\| = \sqrt{v_x^2 + v_y^2}
$$

**Example**: $\|(3,4)\| = 5$.

#### 1.2.3 Unit vector

In the same direction: $\mathbf{u} = \frac{\mathbf{v}}{\|\mathbf{v}\|}$.

**Example**: unit vector of $(3,4)$ is $(\frac35, \frac45)$.

#### 1.2.4 Vector operations

- **Addition**: $(x_1,y_1)+(x_2,y_2) = (x_1+x_2, y_1+y_2)$  
- **Subtraction**: $\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A$ (tip minus tail)  
- **Scalar multiplication**: $c(x,y) = (cx, cy)$; if $c>0$ same direction, $c<0$ opposite.

**Note**: Opposite direction vectors are also parallel (collinear). Zero vector has arbitrary direction and is parallel to every vector.

**Example**: $\mathbf{u}=(1,2),\ \mathbf{v}=(3,-1)$  
$\mathbf{u}+\mathbf{v}=(4,1),\ \mathbf{u}-\mathbf{v}=(-2,3),\ 2\mathbf{u}=(2,4)$.

### 1.3 Position and displacement

- **Position vector** of point $P$: $\mathbf{r} = \overrightarrow{OP}$. If $P(x,y)$, then $\mathbf{r}=(x,y)$.  
- **Displacement** from $A$ to $B$: $\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A$.

**Example**: $A(1,1), B(4,5)$ → displacement $(3,4)$, magnitude 5.

### 1.4 Rate of change: from average to instantaneous

#### 1.4.1 Average velocity

For position $\mathbf{r}(t)$ over $[t, t+\Delta t]$:  
$$
\mathbf{v}_{\text{avg}} = \frac{\mathbf{r}(t+\Delta t) - \mathbf{r}(t)}{\Delta t}
$$

#### 1.4.2 Numerical approximation – understanding limits

For 1D motion $x(t)=t^2$, compute average velocity near $t=1$:

| $\Delta t$ | Average velocity $(x(1+\Delta t)-x(1))/\Delta t$ |
|------------|--------------------------------------------------|
| 0.5        | $(2.25-1)/0.5 = 2.5$ |
| 0.1        | $(1.21-1)/0.1 = 2.1$ |
| 0.01       | $(1.0201-1)/0.01 = 2.01$ |
| 0.001      | $2.001$ |

As $\Delta t \to 0$, average velocity → $2$. That limit is the **instantaneous velocity** at $t=1$.

#### 1.4.3 Instantaneous velocity (derivative)

$$
\mathbf{v}(t) = \lim_{\Delta t\to 0} \frac{\mathbf{r}(t+\Delta t) - \mathbf{r}(t)}{\Delta t} = \left( \frac{dx}{dt}, \frac{dy}{dt} \right)
$$

**Example**: $\mathbf{r}(t) = (t^2, 2t)$ → $\mathbf{v}(t) = (2t, 2)$. At $t=1$, $\mathbf{v}=(2,2)$.

#### 1.4.4 Acceleration

$$
\mathbf{a}(t) = \frac{d\mathbf{v}}{dt} = \left( \frac{d^2x}{dt^2}, \frac{d^2y}{dt^2} \right)
$$

**Example**: $\mathbf{v}(t) = (2t, 2)$ → $\mathbf{a}(t) = (2, 0)$.

### 1.5 From acceleration to velocity to position (integration)

If acceleration $\mathbf{a}(t)$ is known, with initial conditions $\mathbf{v}(0)=\mathbf{v}_0$, $\mathbf{r}(0)=\mathbf{r}_0$:  
$$
\mathbf{v}(t) = \int \mathbf{a}(t)\,dt + \mathbf{v}_0
$$
$$
\mathbf{r}(t) = \int \mathbf{v}(t)\,dt + \mathbf{r}_0
$$
Integration is performed component‑wise.

**Example** (projectile motion): $\mathbf{a}(t) = (0, -g)$, $\mathbf{v}_0 = (v_{0x}, v_{0y})$, $\mathbf{r}_0 = (0,0)$.  
$\mathbf{v}(t) = (v_{0x},\ v_{0y} - g t)$  
$\mathbf{r}(t) = (v_{0x}t,\ v_{0y}t - \frac12 g t^2)$.

### 1.6 Circular motion (optional preview of chain rule)

A particle moves on a circle of radius $R$ with constant angular speed $\omega$:  
$$
\mathbf{r}(t) = (R\cos(\omega t), R\sin(\omega t))
$$
Differentiate (using chain rule, see Topic 4.3):  
$\mathbf{v}(t) = (-R\omega\sin(\omega t), R\omega\cos(\omega t))$  
Speed $= R\omega$ (constant)  
$\mathbf{a}(t) = (-R\omega^2\cos(\omega t), -R\omega^2\sin(\omega t)) = -\omega^2 \mathbf{r}(t)$  
Acceleration points toward the centre, magnitude $R\omega^2$.

### 1.7 Relative velocity

If an object moves in a moving reference frame:  
**Velocity of A relative to C** = **Velocity of A relative to B** + **Velocity of B relative to C**.  
In symbols: $\mathbf{v}_{A/C} = \mathbf{v}_{A/B} + \mathbf{v}_{B/C}$.

**Example**: Boat speed in still water $4$ m/s east, current $3$ m/s north.  
$\mathbf{v}_{\text{boat/ground}} = (4,0)+(0,3) = (4,3)$ m/s, magnitude $5$ m/s, direction $\arctan(3/4)$ north of east.

### 1.8 Worked examples

**Example 1**: $\mathbf{r}(t) = (t^3-3t,\ t^2-2t)$. Find $\mathbf{v}(2)$ and $\mathbf{a}(2)$.  
$\mathbf{v}(t) = (3t^2-3,\ 2t-2)$ → $\mathbf{v}(2) = (9,2)$  
$\mathbf{a}(t) = (6t,\ 2)$ → $\mathbf{a}(2) = (12,2)$.

**Example 2**: $\mathbf{a}(t) = (6t,4)$, $\mathbf{v}_0=(1,0)$, $\mathbf{r}_0=(0,0)$. Find motion.  
$\mathbf{v}(t) = (3t^2,4t)+(1,0) = (3t^2+1,\ 4t)$  
$\mathbf{r}(t) = (t^3+t,\ 2t^2)+(0,0) = (t^3+t,\ 2t^2)$.

**Example 3** (1D, scalars): $x(t)=3t^2-2t+1$ → $v(t)=6t-2$, $a(t)=6$.

### 1.9 Topic 1 Summary

- Vectors represent position, velocity, acceleration.  
- Average velocity → instantaneous velocity via limit (numerical examples).  
- Velocity = derivative of position; acceleration = derivative of velocity.  
- Integration reverses: from acceleration to velocity to position.  
- Parallel vectors include opposite directions; zero vector is parallel to everything.

---

## Topic 2 – Quadratic Functions

### 2.1 Forms and graphs

A quadratic function $f(x) = ax^2 + bx + c$ ($a \neq 0$) graphs as a parabola.  
- If $a > 0$, parabola opens upward; if $a < 0$, opens downward.  
- Vertex $x$-coordinate: $x = -\frac{b}{2a}$, $y$-coordinate: $f\!\left(-\frac{b}{2a}\right)$.  
- Axis of symmetry: $x = -\frac{b}{2a}$.

**Example**: $f(x) = 2x^2 - 4x + 1$, vertex at $x = \frac{4}{4}=1$, $y = 2-4+1=-1$.

### 2.2 Vertex and range

Complete the square: $f(x) = a\left(x + \frac{b}{2a}\right)^2 + \frac{4ac-b^2}{4a}$ gives vertex directly.

Range depends on opening direction:  
- If $a>0$, range $[f_{\min}, \infty)$  
- If $a<0$, range $(-\infty, f_{\max}]$

**Example**: $f(x)=x^2-4x+3 = (x-2)^2 -1$, vertex $(2,-1)$, range $[-1,\infty)$.

### 2.3 Discriminant and roots

For $ax^2+bx+c=0$, discriminant $\Delta = b^2 - 4ac$:  
- $\Delta > 0$: two distinct real roots  
- $\Delta = 0$: one repeated root  
- $\Delta < 0$: no real roots

**Example**: $x^2-3x+2=0$, $\Delta=9-8=1>0$, roots $1$ and $2$.

### 2.4 Quadratic inequalities

Solve $ax^2+bx+c > 0$ (or $<0$):  
- Find roots, then determine intervals based on opening direction.

**Example**: $x^2-4x+3>0$ → solution $x<1$ or $x>3$.

---

## Topic 3 – Functions (Linear, Cubic, Exponential, Logarithmic)

**Goal**: Master common function types, their graphs, rate of change characteristics, and understand inverse and composite functions – foundation for calculus.

### 3.1 Basic function concepts (review)

A function assigns to each input $x$ (in the domain) a unique output $y = f(x)$.  
We care about how $y$ changes as $x$ changes – that is the **rate of change**.

- **Domain**: set of allowed $x$ values.  
- **Range**: set of possible $y$ values.

Example: $f(x)=x^2$, domain all reals, range $[0,\infty)$.

### 3.2 Linear function $f(x) = mx + c$

#### 3.2.1 Form and graph

Graph is a straight line. Slope $m$ = change in $y$ per unit increase in $x$. Intercept $c$ = $y$ when $x=0$.

**Rate of change**: constant $m$.

#### 3.2.2 Finding slope

Given two points $(x_1,y_1)$, $(x_2,y_2)$:  
$$
m = \frac{y_2 - y_1}{x_2 - x_1}
$$

**Example**: Line through $(1,3)$ and $(4,9)$ → $m = (9-3)/(4-1)=6/3=2$.

### 3.3 Cubic function $f(x) = ax^3 + bx^2 + cx + d$

#### 3.3.1 Form and graph

Graph is “S” shaped (or reverse S). May have one local maximum and one local minimum (or none, e.g. $f(x)=x^3$ changes curvature at $x=0$ – called a point of inflection, though IGCSE 0606 does not require that term).  
Rate of change (derivative) is quadratic, may have two zeros (corresponding to extrema).

#### 3.3.2 Rate of change features

For $f(x)=x^3$:  
- From $x=0$ to $1$, average rate $=1$;  
- From $x=1$ to $2$, average rate $=(8-1)/(2-1)=7$.  
Rate increases faster. Instantaneous rate at $x=0$ is $0$, positive and increasing for $x>0$.  
(Derivative formula $f'(x)=3x^2$ – see Topic 4.)

**Example**: $f(x)=x^3-3x$. Near $x=-1$, rate changes from negative to positive → local maximum; near $x=1$, rate changes from positive to negative → local minimum.

### 3.4 Exponential function $f(x) = a^x \quad (a>0, a\neq 1)$

#### 3.4.1 Form and graph

Grows (or decays) extremely fast. For $a>1$, $f(x)$ increases rapidly; for $0<a<1$, $f(x)$ approaches $0$ as $x$ increases. Graph passes through $(0,1)$.

#### 3.4.2 Rate of change – numerical approximation

For $f(x)=2^x$, near $x=1$:

| $\Delta x$ | Average rate $(2^{1+\Delta x} - 2^1)/\Delta x$ |
|------------|------------------------------------------------|
| 0.1        | $(2^{1.1}-2)/0.1 \approx (2.1435-2)/0.1 = 1.435$ |
| 0.01       | $(2^{1.01}-2)/0.01 \approx (2.0145-2)/0.01 = 1.45$ |
| 0.001      | ≈ 1.4427 |

The limit is $2\ln2 \approx 1.386$ (more precise).  
**Important observation**: The instantaneous rate of change of $a^x$ is proportional to $a^x$ itself: $f'(x) = a^x \ln a$ (formula to be learned later).  
Special case $f(x)=e^x$ ($e\approx2.71828$) has rate of change equal to itself.

### 3.5 Logarithmic function $f(x) = \log_a x \quad (a>0, a\neq 1)$

#### 3.5.1 Form and graph

Logarithm is the inverse of exponential. Domain $x>0$, range all reals.  
For $a>1$, increasing but slowing down; for $0<a<1$, decreasing. Graph passes through $(1,0)$.

#### 3.5.2 Rate of change – numerical approximation

For $f(x)=\ln x$, near $x=1$:

| $\Delta x$ | Average rate $(\ln(1+\Delta x)-\ln1)/\Delta x$ |
|------------|------------------------------------------------|
| 0.1        | $\ln1.1/0.1 \approx 0.09531/0.1 = 0.9531$ |
| 0.01       | $\ln1.01/0.01 \approx 0.00995/0.01 = 0.9950$ |
| 0.001      | ≈ 0.9995 |

Limit → $1$. At $x=2$, limit → $0.5$; at $x=10$, limit → $0.1$.  
So rate of change of $\ln x$ is $1/x$; for $\log_a x$, it is $1/(x\ln a)$.

### 3.6 Comparison of rates of change

| Function type | Rate of change characteristic | Pattern (derivative later) |
|---------------|-------------------------------|----------------------------|
| Linear $mx+c$ | constant | $m$ |
| Quadratic $ax^2+bx+c$ | changes linearly with $x$ | $2ax+b$ |
| Cubic $ax^3+\cdots$ | changes quadratically | $3ax^2+2bx+c$ |
| Exponential $a^x$ | proportional to function value | $a^x \ln a$ |
| Logarithmic $\log_a x$ | decreasing, proportional to $1/x$ | $1/(x\ln a)$ |

### 3.7 Inverse and composite functions (syllabus extension)

#### 3.7.1 Inverse function

- **One‑to‑one function**: each output corresponds to exactly one input. Only one‑to‑one functions have inverses.
- If $f$ is one‑to‑one, its inverse $f^{-1}$ satisfies $f^{-1}(y)=x \iff f(x)=y$.
- Graph: $y=f(x)$ and $y=f^{-1}(x)$ are symmetric about $y=x$.

**Example**: $f(x)=2x+1$ is one‑to‑one. Solve $y=2x+1$ → $x=(y-1)/2$, so $f^{-1}(x)=(x-1)/2$.  
**Not one‑to‑one**: $f(x)=x^2$ on all reals ($f(2)=f(-2)=4$). Restrict domain to $x\ge0$ → inverse $f^{-1}(x)=\sqrt{x}$.

#### 3.7.2 Composite functions

- Composite $f \circ g$ is written $fg(x)=f(g(x))$.
- Order matters: generally $fg \neq gf$.

**Example**: $f(x)=x^2$, $g(x)=x+1$ → $fg(x)=(x+1)^2$, $gf(x)=x^2+1$.

### 3.8 Absolute value of a function (syllabus extension)

**Graph of $y=|f(x)|$**: reflect the parts where $y=f(x)$ is negative above the $x$-axis; keep positive parts unchanged.  
For a cubic like $f(x)=x^3-3x$, the absolute value graph has cusps (sharp points) where the original crosses the axis.

### 3.9 Worked examples

**Example 1**: $f(x)=3x+2$, find average rate on $[1,3]$ and compare to instantaneous rate.  
Average $= (f(3)-f(1))/(3-1) = (11-5)/2=3$. Linear function has constant instantaneous rate $3$, so equal.

**Example 2**: $f(x)=x^2$, average rate from $x=2$ to $2.1$: $(4.41-4)/0.1=4.1$.  
From $2$ to $2.01$: $(4.0401-4)/0.01=4.01$. Limit → $4$, so instantaneous rate ≈ $4$.

**Example 3**: Compare $f(x)=2^x$ and $g(x)=x^2$ near $x=4$.  
$f(4)=16,f(5)=32$, average rate $16$; $g(4)=16,g(5)=25$, average rate $9$. Exponential grows faster.

**Example 4**: $f(x)=x^3-2x$, restrict domain to make it one‑to‑one. On $x\ge0$, $f$ is increasing, so inverse exists, but solving algebraically is difficult.

### 3.10 Topic 3 Summary

- Linear: constant rate of change (slope).  
- Quadratic: rate changes linearly (derivative is linear).  
- Cubic: rate changes quadratically (derivative is quadratic); may have inflection.  
- Exponential: rate proportional to function value.  
- Logarithmic: rate decreasing, proportional to $1/x$.  
- Inverse exists only for one‑to‑one functions; composite order matters.  
- Absolute value graph: reflect negative parts upward.

## Topic 4 – Differentiation

**Goal**: First learn polynomial differentiation (Paper 1 core), then chain rule (Paper 2 core), then apply to tangents, extrema, and kinematics.

> Learning path:  
> 4.1–4.3 → Polynomials and chain rule (foundation)  
> 4.4–4.5 → Trig, exponential, logarithmic derivatives (advanced)  
> 4.6–4.7 → Tangents, extrema, kinematics (applications)

### 4.1 What is a derivative?

The derivative describes how fast a function changes at a point – the **instantaneous rate of change**.

- **Average rate of change** over $[x, x+\Delta x]$: $\displaystyle \frac{f(x+\Delta x)-f(x)}{\Delta x}$
- **Instantaneous rate of change** (derivative) $f'(x)$ or $\frac{dy}{dx}$: the limit as $\Delta x \to 0$ of the average rate.

**Intuition**: Your car's speedometer shows instantaneous speed – how fast you are going at that exact moment.

**Geometric meaning**: $f'(a)$ is the slope of the tangent line to $y=f(x)$ at the point $(a, f(a))$.

### 4.2 Limit intuition – the $0/0$ form

When $x$ approaches a value, both numerator and denominator may approach $0$. We simplify by factoring.

**Example**: Find $\displaystyle \lim_{x\to 2} \frac{x^2-4}{x-2}$.  
Factor numerator: $(x-2)(x+2)$, cancel $x-2$ (since $x\neq2$ in the limit) → $\lim_{x\to2}(x+2)=4$.

> **Note**: Limit is about approaching, not equalling. $x$ never equals $2$.

### 4.3 Polynomial differentiation (power rule)

For $f(x)=x^n$ where $n$ is a rational number:
$$
f'(x) = n x^{\,n-1}
$$

**Examples**:
- $f(x)=x^2 \to f'(x)=2x$
- $f(x)=x^3 \to f'(x)=3x^2$
- $f(x)=x \to f'(x)=1$
- $f(x)=1 \to f'(x)=0$
- $f(x)=\sqrt{x}=x^{1/2} \to f'(x)=\frac12 x^{-1/2}=\frac{1}{2\sqrt{x}}$

**Constant multiple and sum/difference rules**:
- $(c\cdot u)' = c\cdot u'$
- $(u \pm v)' = u' \pm v'$

**Derivation by pattern**:  
For $f(x)=ax^2+bx+c$, derivative = $a\cdot2x + b\cdot1 + 0 = 2ax+b$.  
For $f(x)=ax^3+bx^2+cx+d$, derivative = $3ax^2+2bx+c$.

**Example**: $f(x)=3x^2-4x+5 \to f'(x)=6x-4$.

> **Important**: Before differentiating, check the domain. For $f(x)=1/x$, domain is $x\neq0$; derivative $f'(x)=-1/x^2$ is also only valid there.

#### 4.3.1 Implicit differentiation (extension)

When $y$ is not isolated but given by an equation $F(x,y)=0$, differentiate both sides with respect to $x$, treating $y$ as a function of $x$, then solve for $dy/dx$.

**Example**: Circle $x^2+y^2=r^2$. Differentiate: $2x + 2y\frac{dy}{dx}=0 \Rightarrow \frac{dy}{dx}=-\frac{x}{y}$ (provided $y\neq0$).

> **Trap**: Derivative of $y^2$ is $2y \frac{dy}{dx}$, not $2y$.

### 4.4 Chain rule (composite functions)

**Why?** We know $(x^2)'=2x$, but what about $(2x+1)^2$? Expanding works, but for $(2x+1)^{10}$ expansion is messy. The chain rule gives a shortcut.

**Formula**: For $y = (ax+b)^n$, let $u=ax+b$. Then
$$
\frac{dy}{dx} = \frac{dy}{du}\cdot\frac{du}{dx} = n u^{\,n-1} \cdot a = a n (ax+b)^{n-1}
$$

**Mnemonic**: “Differentiate outer, keep inner, multiply by derivative of inner.”

**Examples**:
- $f(x)=(2x+1)^3$: outer derivative $3(2x+1)^2$, inner derivative $2$ → $3(2x+1)^2\cdot2 = 6(2x+1)^2$
- $f(x)=\frac{1}{x+1} = (x+1)^{-1}$: outer $-1(x+1)^{-2}$, inner $1$ → $-(x+1)^{-2} = -\frac{1}{(x+1)^2}$
- $f(x)=\sqrt{3x-2} = (3x-2)^{1/2}$: outer $\frac12(3x-2)^{-1/2}$, inner $3$ → $\frac{3}{2\sqrt{3x-2}}$

### 4.5 Derivatives of trigonometric, exponential, logarithmic functions (advanced)

> **⚠️ Critical reminder**: All angles in **radians** when differentiating trig functions. Set calculator to **Rad** mode.

#### 4.5.1 Trigonometric functions (IGCSE requires sin, cos, tan only)

$$
\frac{d}{dx}\sin x = \cos x
$$
$$
\frac{d}{dx}\cos x = -\sin x
$$
$$
\frac{d}{dx}\tan x = \sec^2 x \quad (\text{where } \sec x = 1/\cos x)
$$

**Memory aid**: sin → cos, cos → -sin, tan → sec².

**Examples**:
- $f(x)=3\sin x \to f'(x)=3\cos x$
- $f(x)=\cos(2x)$: chain rule → $-\sin(2x)\cdot2 = -2\sin 2x$
- $f(x)=\tan(3x)$: chain rule → $\sec^2(3x)\cdot3 = 3\sec^2(3x)$

#### 4.5.2 Exponential and logarithmic functions

$$
\frac{d}{dx} e^x = e^x
$$
$$
\frac{d}{dx} a^x = a^x \ln a \quad (a>0, a\neq1)
$$
$$
\frac{d}{dx} \ln x = \frac{1}{x} \quad (x>0)
$$
$$
\frac{d}{dx} \log_a x = \frac{1}{x\ln a}
$$

**Examples**:
- $f(x)=e^{2x} \to e^{2x}\cdot2 = 2e^{2x}$ (chain rule)
- $f(x)=2^x \to 2^x \ln 2$
- $f(x)=\ln(3x+1) \to \frac{1}{3x+1}\cdot3 = \frac{3}{3x+1}$

### 4.6 Tangent and normal lines (3‑step method – never lose marks)

**Three steps** (like a recipe):
1. **Find point**: plug $x=a$ into $f(x)$ → $y_0=f(a)$. Point is $(a, y_0)$.
2. **Find slope**: compute $f'(x)$, then $m = f'(a)$.
3. **Write equation**: point‑slope $y - y_0 = m(x-a)$, simplify to $y=mx+c$.

**Example** (Paper 1 style): $f(x)=x^2$ at $x=1$.  
- $f(1)=1$ → point $(1,1)$  
- $f'(x)=2x$, $f'(1)=2$ → slope $m=2$  
- Tangent: $y-1=2(x-1)$ → $y=2x-1$

**Normal line**: perpendicular to tangent, so slope $m_{\text{normal}} = -\frac{1}{m}$ (if $m\neq0$).  
For the above: $m_{\text{normal}} = -\frac12$, equation $y-1=-\frac12(x-1)$.

> **⚠️ Deadly trap**:  
> - **“At point P”** → P is the point of tangency. One tangent. Use 3 steps.  
> - **“Through point P”** → P may not be on the curve. **Set a generic point of tangency** $(a, f(a))$, write tangent equation, then substitute P's coordinates to solve for $a$ (may give two tangents). This is a high‑frequency mistake.

### 4.7 Stationary points (maxima and minima – peaks and valleys)

**What are they?**  
- **Maximum**: like a peak – slope changes from positive to negative.  
- **Minimum**: like a valley – slope changes from negative to positive.

**Procedure**:
1. Compute $f'(x)$.
2. Solve $f'(x)=0$ to get **critical points** (stationary points).  
   (Note: a stationary point is not necessarily an extremum; e.g. $f(x)=x^3$ at $x=0$ has zero derivative but is not a max/min.)
3. Use **first derivative test** (sign change):
   - Pick a point just left of the critical point, plug into $f'(x)$.
   - Pick a point just right.
   - Left +, right − → **local maximum**
   - Left −, right + → **local minimum**
   - Same sign on both sides → not an extremum (point of inflection, not required but good to know).

**Shortcut (second derivative test)**: If $f''(x)$ is easy to compute:
   - $f'(a)=0$ and $f''(a)>0$ → local minimum
   - $f'(a)=0$ and $f''(a)<0$ → local maximum
   - $f''(a)=0$ → test fails, revert to first derivative test.

**Example**: $f(x)=x^3-3x$  
- $f'(x)=3x^2-3=0$ → $x=\pm1$  
- For $x=-1$: left $x=-2$, $f'(-2)=12-3=9>0$; right $x=0$, $f'(0)=-3<0$ → left +, right − → **maximum** at $x=-1$, $f(-1)=2$  
- For $x=1$: left $x=0$, $f'(0)=-3<0$; right $x=2$, $f'(2)=12-3=9>0$ → left −, right + → **minimum** at $x=1$, $f(1)=-2$

> **Note**: Critical points must lie in the domain. For $f(x)=1/x$, derivative $-1/x^2$ is never zero → no stationary points.

### 4.8 Kinematics (displacement → velocity → acceleration)

In straight‑line motion, displacement $s(t)$ is a function of time $t$.

**Core formulas**:
- Velocity $v(t) = \frac{ds}{dt}$ (rate of change of displacement)
- Acceleration $a(t) = \frac{dv}{dt} = \frac{d^2s}{dt^2}$ (rate of change of velocity)

**Determining direction of motion**:
- $v(t) > 0$ → moving in positive direction
- $v(t) < 0$ → moving in negative direction
- $v(t) = 0$ → instantaneously at rest. **Key**: If $v$ changes sign (positive ↔ negative), the particle **reverses direction** at that instant. Example: throwing a ball upward – at the top, $v=0$ then it turns around.

**Graphical relationships**:
- Slope of $s$‑$t$ graph = velocity
- Slope of $v$‑$t$ graph = acceleration
- Area under $v$‑$t$ graph = displacement (will be covered in integration)

**Example** (Paper 1 style): $s(t)=t^3-6t^2+9t$. Find when particle reverses direction.  
- $v(t)=3t^2-12t+9=3(t-1)(t-3)$  
- $v=0$ at $t=1$ and $t=3$  
- Sign test:  
  $t<1$: $v>0$ (positive)  
  $1<t<3$: $v<0$ (negative)  
  $t>3$: $v>0$ (positive)  
- $v$ changes sign at both $t=1$ and $t=3$ → particle reverses direction at those times.

**Example** (Paper 2 style): $v(t)=2t^2-5t+3$, find acceleration at $t=3$.  
- $a(t)=4t-5$, $a(3)=12-5=7$.

> **Note**: Negative acceleration does not always mean slowing down. If velocity is negative and acceleration is negative, speed actually increases in the negative direction. IGCSE usually only asks for direct calculation, not sign analysis of acceleration.

### 4.9 Topic 4 Summary – Quick reference table

| What you want to do | How to do it |
|--------------------|---------------|
| Differentiate $x^n$ | $n x^{n-1}$ |
| Differentiate $(ax+b)^n$ (chain rule) | $a n (ax+b)^{n-1}$ |
| Differentiate $\sin x$ | $\cos x$ |
| Differentiate $\cos x$ | $-\sin x$ |
| Differentiate $\tan x$ | $\sec^2 x = 1/\cos^2 x$ |
| Differentiate $e^x$ | $e^x$ |
| Differentiate $\ln x$ | $1/x$ |
| Write tangent line | 3 steps: point, slope, equation |
| Find local max/min | Solve $f'(x)=0$, test sign change (left + right − → max; left − right + → min) |
| Kinematics | $v = ds/dt$, $a = dv/dt$, $v=0$ with sign change → reversal |

---

## Topic 5 – Equations and Inequalities (Graphical Methods)

**Goal**: Use graphs (especially sketches aided by derivatives) to solve equations and inequalities. Understand that intersections of graphs correspond to solutions of equations. Learn absolute value graph transformations.

> Prerequisite: Topic 4 (differentiation, monotonicity, extrema).

### 5.1 Solutions of equations and intersections of graphs

**Core idea**: The equation $f(x) = g(x)$ is solved by the $x$‑coordinates of the intersection points of $y=f(x)$ and $y=g(x)$.

**Special case**: $f(x)=0$ → solutions are the $x$‑intercepts (zeros) of $y=f(x)$.

**Example**: Solve $x^2-3x+2=0$.  
Graph $y=x^2-3x+2$; it crosses the $x$‑axis at $x=1$ and $x=2$ → solutions $x=1$ or $x=2$.

**Why graphical?** Some equations cannot be solved algebraically (e.g. $x^3-3x+1=0$), but a sketch tells you how many solutions exist and roughly where, then numerical methods can refine.

### 5.2 Sketching graphs using derivatives (preparation for solving)

To sketch $y=f(x)$, we need:
- Intercepts ($x$‑intercepts and $y$‑intercept)
- Monotonicity (where increasing/decreasing)
- Stationary points (maxima, minima)
- End behaviour as $x\to\pm\infty$

**Steps**:
1. Compute $f'(x)$, solve $f'(x)=0$ to find stationary points.
2. Use first derivative test to classify each as max or min.
3. Compute $f(x)$ at those points and at $x=0$ ($y$‑intercept).
4. Consider $\lim_{x\to\infty} f(x)$ and $\lim_{x\to-\infty} f(x)$ (look at the highest degree term).

**Example**: Sketch $f(x)=x^3-3x$.
- $f'(x)=3x^2-3=0 \Rightarrow x=\pm1$.
- $x=-1$: left $f'(-2)=9>0$, right $f'(0)=-3<0$ → maximum, $f(-1)=2$.
- $x=1$: left $f'(0)=-3<0$, right $f'(2)=9>0$ → minimum, $f(1)=-2$.
- $f(0)=0$ → passes through origin.
- As $x\to\infty$, $f(x)\to\infty$; as $x\to-\infty$, $f(x)\to-\infty$.

> **Note**: Sketches need not be perfectly scaled, but must show key points (intercepts, stationary points).

### 5.3 Solving inequalities using graphs

**Inequality $f(x) > 0$**: solution set is where the graph of $y=f(x)$ lies **above** the $x$‑axis.

**Steps**:
1. Sketch $y=f(x)$ (or use monotonicity and zeros).
2. Find all $x$‑intercepts (solutions of $f(x)=0$).
3. Determine intervals where graph is above or below axis.
4. Write solution set.

**Example**: Solve $x^2-3x+2 > 0$.
- Graph: upward parabola, zeros at $x=1,2$.
- Above axis for $x<1$ and $x>2$.
- Solution: $x<1$ or $x>2$.

**Example**: Solve $x^3-3x < 0$.
- Zeros: $x(x^2-3)=0 \Rightarrow x=0, \pm\sqrt{3}\approx\pm1.732$.
- Test intervals:
  - $x=-2$: $(-8)+6=-2<0$ → below axis
  - $x=-1$: $(-1)+3=2>0$ → above
  - $x=1$: $1-3=-2<0$ → below
  - $x=2$: $8-6=2>0$ → above
- $f(x)<0$ for $x<-\sqrt{3}$ or $0<x<\sqrt{3}$.

### 5.4 Absolute value graphs and equations/inequalities

**Graph of $y=|f(x)|$**: reflect the parts where $y=f(x)$ is negative up above the $x$‑axis; keep positive parts unchanged.

**Example**: $y=|x^2-3x+2|$.  
First sketch $y=x^2-3x+2$ (upward parabola, zeros at 1,2). On interval $1<x<2$, the original graph is below axis; reflect that portion to get a “V‑shaped” dip.

**Equation $|f(x)| = k$** (with $k>0$):  
Equivalent to $f(x)=k$ or $f(x)=-k$.

**Inequality $|f(x)| < k$**:  
Equivalent to $-k < f(x) < k$.

**Example**: Solve $|x^2-3x+2| < 1$.
- Write $-1 < x^2-3x+2 < 1$.
- Left inequality: $x^2-3x+2 > -1 \Rightarrow x^2-3x+3 > 0$, discriminant $9-12=-3<0$, always true.
- Right inequality: $x^2-3x+2 < 1 \Rightarrow x^2-3x+1 < 0$. Solve quadratic: roots $\frac{3\pm\sqrt5}{2}\approx0.382,\ 2.618$, parabola opens up → inequality true between roots.
- Solution: $\frac{3-\sqrt5}{2} < x < \frac{3+\sqrt5}{2}$.

### 5.5 Using derivatives for inequalities with complex functions

When the function is not a simple quadratic or cubic, sketch it using derivative analysis first.

**Example**: Solve $\frac{2x}{x^2+1} > 0$.
- Denominator $x^2+1>0$ always, so sign determined by numerator $2x$.
- $2x>0 \Rightarrow x>0$. Solution: $(0,\infty)$.

**Example**: Solve $x e^{-x} > 0$.
- $e^{-x}>0$ always, so sign determined by $x$. Solution: $(0,\infty)$.

**Example**: Solve $\ln x > 0$.
- $\ln x > 0 \Rightarrow x > 1$ (since $\ln 1=0$ and $\ln x$ increasing). Solution: $(1,\infty)$.

### 5.6 Intersection of two graphs and inequalities $f(x) > g(x)$

**Solution of $f(x) > g(x)$**: $x$ where the graph of $f$ is **above** the graph of $g$.

**Steps**:
1. Sketch both graphs (or study $h(x)=f(x)-g(x)$).
2. Find all intersection points (solutions of $f(x)=g(x)$).
3. Test a point in each interval to see which function is larger.

**Example**: Solve $x^2 < 2x+3$.
- Rearrange: $x^2-2x-3<0 \Rightarrow (x-3)(x+1)<0$.
- Graph of $y=x^2-2x-3$ is upward parabola, zeros at $-1$ and $3$, negative between roots.
- Solution: $-1 < x < 3$.

**Example**: Solve $e^x > x^2$.
- Algebraic solution difficult. Study $h(x)=e^x-x^2$, find its zeros by sketching or numerically. Not required for IGCSE but shows the idea.

### 5.7 Worked examples

**Example 1**: $f(x)=x^3-6x^2+9x$, solve $f(x)>0$.
- Factor: $f(x)=x(x^2-6x+9)=x(x-3)^2$.
- Zeros: $x=0$ and $x=3$ (double root).
- $(x-3)^2 \ge 0$, so sign determined by $x$. For $x>0$ and $x\neq3$, $f(x)>0$; for $x<0$, $f(x)<0$; at zeros $f=0$.
- Solution: $x>0$ and $x\neq3$, i.e. $(0,3)\cup(3,\infty)$.

**Example 2**: Solve $|x^2-4x+3| = 2$.
- Solve $x^2-4x+3=2 \Rightarrow x^2-4x+1=0 \Rightarrow x=2\pm\sqrt3$.
- Solve $x^2-4x+3=-2 \Rightarrow x^2-4x+5=0$, discriminant $16-20=-4<0$, no real roots.
- Solution: $x=2+\sqrt3$ and $x=2-\sqrt3$.

**Example 3**: Solve $|x-1| > |2x+3|$.
- Square both sides (non‑negative): $(x-1)^2 > (2x+3)^2$.
- Expand: $x^2-2x+1 > 4x^2+12x+9 \Rightarrow 0 > 3x^2+14x+8 \Rightarrow 3x^2+14x+8 < 0$.
- Discriminant: $196-96=100$, roots $\frac{-14\pm10}{6}$ → $-4$ and $-\frac23$.
- Parabola opens up → inequality true between roots: $-4 < x < -\frac23$.

### 5.8 Topic 5 Summary

| Problem type | Method |
|--------------|--------|
| Solve $f(x)=0$ | Find $x$‑intercepts of $y=f(x)$ |
| Solve $f(x)=g(x)$ | Find intersections of $y=f(x)$ and $y=g(x)$ |
| Solve $f(x)>0$ | Intervals where graph above $x$‑axis |
| Solve $f(x)<g(x)$ | Intervals where $f$ graph below $g$ graph |
| Absolute equation $|f(x)|=k$ | Solve $f(x)=k$ and $f(x)=-k$ |
| Absolute inequality $|f(x)|<k$ | Solve $-k<f(x)<k$ |
| Complex function inequality | Sketch using derivatives, then read intervals |

---

## Topic 6 – Integration

**Goal**: Understand integration as the reverse of differentiation. Learn basic indefinite integrals. Use definite integrals to compute area under curves. Apply to kinematics (from acceleration/velocity to displacement).

> Learning path:  
> 6.1–6.3 → Indefinite integrals (antiderivatives)  
> 6.4–6.5 → Definite integrals and area  
> 6.6 → Kinematics with integration

### 6.1 What is integration? – Reverse of differentiation

If you know a function’s derivative and want to recover the original function, you **integrate** (find an antiderivative).

**Example**: Given $f'(x)=2x$, what is $f(x)$?  
You might guess $f(x)=x^2$, because derivative of $x^2$ is $2x$. But $x^2+1$, $x^2-5$ also have derivative $2x$. So antiderivatives differ by a constant. We write:
$$
\int 2x \, dx = x^2 + C
$$
where $C$ is the **constant of integration** (any real number).

**Notation**: $\int f(x) \, dx$ means the indefinite integral (family of all antiderivatives).

### 6.2 Basic integration formulas (mirroring differentiation)

Because integration is the reverse of differentiation, each derivative rule gives an integration rule.

#### 6.2.1 Power rule ($n \neq -1$)

$$
\int x^n \, dx = \frac{x^{n+1}}{n+1} + C
$$

**Examples**:
- $\int x^2 \, dx = \frac{x^3}{3} + C$
- $\int x^{-3} \, dx = \frac{x^{-2}}{-2} + C = -\frac{1}{2x^2} + C$
- $\int \sqrt{x} \, dx = \int x^{1/2} \, dx = \frac{x^{3/2}}{3/2} + C = \frac{2}{3}x^{3/2} + C$

#### 6.2.2 Special case $n = -1$

$$
\int \frac{1}{x} \, dx = \ln|x| + C
$$
(because $\frac{d}{dx}\ln|x| = \frac{1}{x}$)

#### 6.2.3 Exponential and logarithmic

$$
\int e^x \, dx = e^x + C
$$
$$
\int a^x \, dx = \frac{a^x}{\ln a} + C \quad (a>0, a\neq1)
$$

#### 6.2.4 Trigonometric functions (angles in radians)

$$
\int \sin x \, dx = -\cos x + C
$$
$$
\int \cos x \, dx = \sin x + C
$$
$$
\int \sec^2 x \, dx = \tan x + C
$$
($\int \tan x \, dx$ is not required, but can be written as $\ln|\sec x|+C$ as an extension)

### 6.3 Linearity of integration

Constants factor out, sums/differences split:
$$
\int (a f(x) + b g(x)) \, dx = a \int f(x) \, dx + b \int g(x) \, dx
$$

**Example**:
$$
\int (3x^2 - 4\sin x + 5e^x) \, dx = 3\cdot\frac{x^3}{3} - 4\cdot(-\cos x) + 5e^x + C = x^3 + 4\cos x + 5e^x + C
$$

### 6.4 Definite integrals and area

**Definite integral** $\int_a^b f(x) \, dx$ represents the **signed area** between $y=f(x)$ and the $x$‑axis from $x=a$ to $x=b$ (positive above axis, negative below).

**Evaluation (Fundamental Theorem of Calculus)**: If $F'(x)=f(x)$, then
$$
\int_a^b f(x) \, dx = F(b) - F(a)
$$

**Example**: Compute $\int_1^2 2x \, dx$.  
$F(x)=x^2$, so $F(2)-F(1)=4-1=3$. This is the area under $y=2x$ from $x=1$ to $2$.

**Handling negative area**: If the function changes sign, split the integral at zeros and take absolute values to get **total area**.

**Example**: Find total area between $y=x^3-3x$ and the $x$‑axis on $[-2,2]$.  
Zeros: $x=0, \pm\sqrt{3}\approx\pm1.732$. Split into $[-2,-1.732]$, $[-1.732,0]$, $[0,1.732]$, $[1.732,2]$. Compute each absolute area and sum. (Due to odd symmetry, the positive and negative areas are symmetric, but the method is shown.)

**Simpler example**: $y=x^2-1$ on $[-2,2]$. Zeros at $x=\pm1$.  
Area $= \int_{-2}^{-1}(x^2-1)dx + \int_{-1}^{1}[-(x^2-1)]dx + \int_{1}^{2}(x^2-1)dx = \frac43 + \frac43 + \frac43 = 4$.

### 6.5 Area between two curves

If $f(x) \ge g(x)$ on $[a,b]$, the area between the curves is:
$$
\int_a^b [f(x) - g(x)] \, dx
$$

**Steps**:
1. Find intersection points by solving $f(x)=g(x)$.
2. Determine which function is on top in each interval.
3. Integrate (top minus bottom).

**Example**: Find area between $y=x^2$ and $y=2x$.  
- Intersections: $x^2=2x \Rightarrow x(x-2)=0 \Rightarrow x=0,2$.  
- On $(0,2)$, $2x \ge x^2$.  
- Area $= \int_0^2 (2x - x^2) \, dx = [x^2 - \frac{x^3}{3}]_0^2 = (4 - \frac83) - 0 = \frac43$.

### 6.6 Kinematics with integration

Given acceleration $a(t)$, integrate to get velocity $v(t)$; integrate velocity to get displacement $s(t)$.

- $v(t) = \int a(t) \, dt + v_0$ (where $v_0$ is initial velocity)
- $s(t) = \int v(t) \, dt + s_0$ (where $s_0$ is initial displacement)

**Example**: $a(t)=6t-2$, $v(0)=1$, $s(0)=0$.  
- $v(t) = \int (6t-2) dt = 3t^2 - 2t + C$. Using $v(0)=1$ → $C=1$, so $v(t)=3t^2-2t+1$.  
- $s(t) = \int (3t^2-2t+1) dt = t^3 - t^2 + t + D$. Using $s(0)=0$ → $D=0$, so $s(t)=t^3-t^2+t$.

**Definite integral for displacement**: Displacement from $t=a$ to $t=b$ is $\int_a^b v(t) \, dt$.

**Example**: $v(t)=t^2-4t+3$, find displacement from $t=1$ to $t=3$.  
$\int_1^3 (t^2-4t+3) dt = [\frac{t^3}{3} - 2t^2 + 3t]_1^3 = (9-18+9) - (\frac13 - 2 + 3) = 0 - (\frac13+1) = -\frac43$.  
Negative sign means net displacement is in the negative direction.

### 6.7 Topic 6 Summary

| What you want to do | How to do it |
|--------------------|---------------|
| Integrate $x^n$ ($n\neq-1$) | $\frac{x^{n+1}}{n+1} + C$ |
| Integrate $1/x$ | $\ln|x| + C$ |
| Integrate $e^x$ | $e^x + C$ |
| Integrate $\sin x$ | $-\cos x + C$ |
| Integrate $\cos x$ | $\sin x + C$ |
| Integrate $\sec^2 x$ | $\tan x + C$ |
| Compute definite integral $\int_a^b f(x)dx$ | Find antiderivative $F$, compute $F(b)-F(a)$ |
| Area under curve | Definite integral (watch signs) |
| Area between curves | $\int (\text{top} - \text{bottom}) dx$, find intersections |
| Kinematics: from $a$ to $v$ | $v = \int a dt + v_0$ |
| Kinematics: from $v$ to displacement | $s = \int v dt + s_0$ or $\int v dt$ (definite) |
## Topic 8 – Trigonometry

**Goal**: Master the six trigonometric functions, their graphs, basic identities, radian measure, solving trigonometric equations, and proving simple identities.

> Learning path:  
> 8.1–8.2 → Degrees vs radians, unit circle definitions  
> 8.3–8.4 → Graphs, periodicity, symmetry, transformations  
> 8.5–8.6 → Basic identities, proving identities  
> 8.7 → Solving trigonometric equations (key and difficult)

### 8.1 Degrees and radians

In calculus and advanced mathematics, we use **radians**, not degrees.

**Definition**: radian = arc length / radius.  
Full circle: arc length = $2\pi r$ → $360^\circ = 2\pi$ radians.  
Thus:
$$
180^\circ = \pi \text{ radians}, \quad 1^\circ = \frac{\pi}{180} \text{ rad}, \quad 1 \text{ rad} = \frac{180}{\pi}^\circ \approx 57.3^\circ
$$

**Common conversions**:
- $0^\circ = 0$
- $30^\circ = \frac{\pi}{6}$
- $45^\circ = \frac{\pi}{4}$
- $60^\circ = \frac{\pi}{3}$
- $90^\circ = \frac{\pi}{2}$
- $180^\circ = \pi$

> **⚠️ Life‑or‑death reminder**: When differentiating, integrating, or solving trig equations, your calculator **must** be in **Rad (radian) mode**! Otherwise all answers will be wrong.

#### 8.1.1 Unit circle insights

**Derivation of $\sin(180^\circ - \theta) = \sin \theta$**:  
On unit circle, angle $\theta$ gives point $P(\cos\theta,\sin\theta)$; angle $180^\circ-\theta$ gives $Q(\cos(180^\circ-\theta),\sin(180^\circ-\theta))$. By symmetry, $Q$ is the reflection of $P$ across the $y$-axis, so their $y$-coordinates are equal: $\sin(180^\circ-\theta)=\sin\theta$.

**Special triangles**:
- $30^\circ$-$60^\circ$-$90^\circ$ triangle: side ratios $1:\sqrt3:2$
- $45^\circ$-$45^\circ$-$90^\circ$ triangle: side ratios $1:1:\sqrt2$

Hence:
$$
\sin30^\circ=\frac12,\ \cos30^\circ=\frac{\sqrt3}{2},\ \tan30^\circ=\frac{1}{\sqrt3}
$$
$$
\sin45^\circ=\frac{\sqrt2}{2},\ \cos45^\circ=\frac{\sqrt2}{2},\ \tan45^\circ=1
$$
$$
\sin60^\circ=\frac{\sqrt3}{2},\ \cos60^\circ=\frac12,\ \tan60^\circ=\sqrt3
$$

> Memory aid for sine: numerators $\sqrt1,\sqrt2,\sqrt3$ over $2$.

### 8.2 Definitions of six trigonometric functions (unit circle)

On unit circle (radius = 1), point $P(x,y)$ corresponding to angle $\theta$ (counterclockwise from positive $x$-axis):
- $\sin \theta = y$ (sine)
- $\cos \theta = x$ (cosine)
- $\tan \theta = \frac{y}{x} = \frac{\sin\theta}{\cos\theta}$ (tangent)
- $\sec \theta = \frac{1}{\cos\theta}$ (secant)
- $\csc \theta = \frac{1}{\sin\theta}$ (cosecant)
- $\cot \theta = \frac{1}{\tan\theta} = \frac{\cos\theta}{\sin\theta}$ (cotangent)

**Sign mnemonic (ASTC)**:
- Quadrant I (0°–90°): **A**ll positive
- Quadrant II (90°–180°): **S**ine positive
- Quadrant III (180°–270°): **T**angent positive
- Quadrant IV (270°–360°): **C**osine positive

**Sign table**:

| Quadrant | $\sin$ | $\cos$ | $\tan$ | $\sec$ | $\csc$ | $\cot$ |
|----------|--------|--------|--------|--------|--------|--------|
| I        | +      | +      | +      | +      | +      | +      |
| II       | +      | -      | -      | -      | +      | -      |
| III      | -      | -      | +      | -      | -      | +      |
| IV       | -      | +      | -      | +      | -      | -      |

#### 8.2.1 Sum‑to‑product formulas (extension)

$$
\sin A + \sin B = 2\sin\frac{A+B}{2}\cos\frac{A-B}{2}
$$
$$
\sin A - \sin B = 2\cos\frac{A+B}{2}\sin\frac{A-B}{2}
$$
$$
\cos A + \cos B = 2\cos\frac{A+B}{2}\cos\frac{A-B}{2}
$$
$$
\cos A - \cos B = -2\sin\frac{A+B}{2}\sin\frac{A-B}{2}
$$

**Example**: Simplify $\sin75^\circ+\sin15^\circ = 2\sin45^\circ\cos30^\circ = 2\cdot\frac{\sqrt2}{2}\cdot\frac{\sqrt3}{2} = \frac{\sqrt6}{2}$.

### 8.3 Graphs of trigonometric functions (essential!)

#### 8.3.1 $y = \sin x$
- Domain: all reals
- Range: $[-1,1]$
- Period: $2\pi$
- Odd: $\sin(-x)=-\sin x$
- Zeros: $x=n\pi$

#### 8.3.2 $y = \cos x$
- Domain: all reals
- Range: $[-1,1]$
- Period: $2\pi$
- Even: $\cos(-x)=\cos x$
- Zeros: $x=\frac{\pi}{2}+n\pi$

#### 8.3.3 $y = \tan x$
- Domain: $x \neq \frac{\pi}{2}+n\pi$ ($n$ integer)
- Range: all reals
- Period: $\pi$
- Odd
- Asymptotes: $x=\frac{\pi}{2}+n\pi$

**Sketching tips**: $\sin x$ starts at 0, goes up to 1, down to -1; $\cos x$ starts at 1, goes down to -1; $\tan x$ repeats every $\pi$, has vertical asymptotes at $\pm\pi/2$.

### 8.4 Amplitude, period, and graph transformations

For $y = A\sin(Bx + C) + D$ (similarly for cosine):
- $|A|$ = amplitude (vertical stretch)
- $\frac{2\pi}{|B|}$ = period (horizontal stretch)
- $-\frac{C}{B}$ = phase shift (horizontal translation)
- $D$ = vertical shift

**Example**: $y = 3\sin(2x + \frac{\pi}{3})$  
- Amplitude = 3
- Period = $2\pi/2 = \pi$
- Phase shift = $-\frac{\pi/3}{2} = -\frac{\pi}{6}$ (shift left by $\pi/6$)

**Order of transformations**: horizontal stretch → horizontal shift → vertical stretch → vertical shift.

### 8.5 Basic trigonometric identities

**Core identities (must memorise)**:
$$
\sin^2\theta + \cos^2\theta = 1
$$
$$
\sec^2\theta = 1 + \tan^2\theta
$$
$$
\csc^2\theta = 1 + \cot^2\theta
$$

**Derivation**: first from unit circle; second divide by $\cos^2\theta$; third divide by $\sin^2\theta$.

**Double‑angle formulas (commonly used extensions)**:
$$
\sin(2\theta) = 2\sin\theta\cos\theta
$$
$$
\cos(2\theta) = \cos^2\theta - \sin^2\theta = 2\cos^2\theta - 1 = 1 - 2\sin^2\theta
$$
$$
\tan(2\theta) = \frac{2\tan\theta}{1-\tan^2\theta}
$$

### 8.6 Proving trigonometric identities

**Strategy**: Start from the more complicated side, use basic identities to simplify until you reach the other side.  
**Technique**: Convert everything to $\sin$ and $\cos$, then combine fractions.

**Example 1**: Prove $\tan x + \cot x = \sec x \csc x$.

Left side:
$$
\frac{\sin x}{\cos x} + \frac{\cos x}{\sin x} = \frac{\sin^2 x + \cos^2 x}{\sin x \cos x} = \frac{1}{\sin x \cos x}
$$
Right side:
$$
\sec x \csc x = \frac{1}{\cos x}\cdot\frac{1}{\sin x} = \frac{1}{\sin x \cos x}
$$
Equal.

**Example 2**: Prove $\frac{\sin\theta}{1+\cos\theta} + \frac{1+\cos\theta}{\sin\theta} = 2\csc\theta$.

Common denominator:
$$
\frac{\sin^2\theta + (1+\cos\theta)^2}{\sin\theta(1+\cos\theta)} = \frac{\sin^2\theta + 1 + 2\cos\theta + \cos^2\theta}{\sin\theta(1+\cos\theta)} = \frac{2 + 2\cos\theta}{\sin\theta(1+\cos\theta)} = \frac{2(1+\cos\theta)}{\sin\theta(1+\cos\theta)} = \frac{2}{\sin\theta} = 2\csc\theta
$$

**Proof techniques summary**:
- Convert to $\sin$ and $\cos$
- Get common denominator
- Use $\sin^2+\cos^2=1$
- Factorise
- Use double‑angle formulas when needed

> **Common mistakes**:  
> - Don’t write $\sin^2\theta$ as $\sin\theta^2$ (different meaning).  
> - Don’t forget domain restrictions (denominators ≠ 0).

### 8.7 Solving trigonometric equations

#### 8.7.1 Basic form $\sin x = k$

**Steps (reference angle method)**:
1. Compute reference angle $\alpha = \arcsin(|k|)$ (acute, $0 \le \alpha \le \pi/2$).
2. Determine quadrants based on sign of $k$:
   - $k \ge 0$: solutions in QI and QII: $x = \alpha$ and $x = \pi - \alpha$.
   - $k < 0$: solutions in QIII and QIV: $x = \pi + \alpha$ and $x = 2\pi - \alpha$.
3. List all solutions in the given interval (e.g. $[0,2\pi)$).
4. General solution: add $2n\pi$ ($n$ integer).

**Example**: $\sin x = \frac12$, $0 \le x < 2\pi$.  
$\alpha = \arcsin(0.5) = \frac{\pi}{6}$. Solutions: $x = \frac{\pi}{6}$ and $x = \pi - \frac{\pi}{6} = \frac{5\pi}{6}$.

**Example**: $\sin x = -\frac12$, $0 \le x < 2\pi$.  
$\alpha = \frac{\pi}{6}$, $k<0$ → QIII and QIV: $x = \pi + \frac{\pi}{6} = \frac{7\pi}{6}$ and $x = 2\pi - \frac{\pi}{6} = \frac{11\pi}{6}$.

#### 8.7.2 Basic form $\cos x = k$

1. Reference $\alpha = \arccos(|k|) \in [0,\pi]$.
2. Sign of $k$:
   - $k \ge 0$: QI and QIV: $x = \alpha$ and $x = 2\pi - \alpha$.
   - $k < 0$: QII and QIII: $x = \pi - \alpha$ and $x = \pi + \alpha$.
3. General solution: $x = \pm \alpha + 2n\pi$ (with $\alpha \ge 0$).

**Example**: $\cos x = -\frac12$.  
$\alpha = \arccos(0.5)=\frac{\pi}{3}$, $k<0$ → $x = \pi - \frac{\pi}{3} = \frac{2\pi}{3}$ and $x = \pi + \frac{\pi}{3} = \frac{4\pi}{3}$.

#### 8.7.3 Basic form $\tan x = k$

1. Reference $\alpha = \arctan(|k|) \in (0,\frac{\pi}{2})$.
2. Solutions: $x = \alpha$ (QI) and $x = \alpha + \pi$ (QIII), etc.
3. General solution: $x = \alpha + n\pi$ (where $\alpha = \arctan k$ can be negative, principal value $(-\frac{\pi}{2},\frac{\pi}{2})$).

**Example**: $\tan x = \sqrt3$, $\alpha = \frac{\pi}{3}$, in $[0,2\pi)$: $\frac{\pi}{3}$ and $\frac{\pi}{3}+\pi = \frac{4\pi}{3}$.

**Example**: $\tan x = -1$, $\alpha = -\frac{\pi}{4}$, in $[0,2\pi)$: $-\frac{\pi}{4}+\pi = \frac{3\pi}{4}$ and $-\frac{\pi}{4}+2\pi = \frac{7\pi}{4}$.

#### 8.7.4 Equations requiring identities

**Example**: Solve $2\sec^2 x + \tan x - 3 = 0$, $0 \le x < 2\pi$.

Use $\sec^2 x = 1+\tan^2 x$:
$$
2(1+\tan^2 x) + \tan x - 3 = 0 \Rightarrow 2\tan^2 x + \tan x - 1 = 0
$$
Let $u=\tan x$: $2u^2+u-1=0$ → $u=\frac12$ or $u=-1$.

- $\tan x = 0.5$: $\alpha = \arctan(0.5) \approx 0.4636$, other solution $\alpha+\pi \approx 3.6052$.
- $\tan x = -1$: $\alpha = -\frac{\pi}{4}$, add $\pi$ → $\frac{3\pi}{4}$, add $2\pi$ → $\frac{7\pi}{4}$ (both in $[0,2\pi)$).

Solution set: $\{0.4636,\ 3.6052,\ \frac{3\pi}{4},\ \frac{7\pi}{4}\}$.

> **⚠️ Solving trig equations – must watch**:  
> - Check domain; exclude points where function undefined (e.g. $\tan x$ at $\frac{\pi}{2}+n\pi$).  
> - If approximate values, keep sufficient precision (usually 3 decimal places).  
> - Verify solutions by substituting back.

### 8.8 Topic 8 Summary

| Concept | Key points |
|---------|-------------|
| Radians | $180^\circ = \pi$ rad, calculator in Rad mode |
| Six trig functions | $\sin,\cos,\tan,\sec,\csc,\cot$, domains and ranges |
| Graphs | $\sin,\cos$ period $2\pi$, $\tan$ period $\pi$; amplitude, phase shift |
| Basic identities | $\sin^2+\cos^2=1$, $\sec^2=1+\tan^2$, $\csc^2=1+\cot^2$ |
| Proving identities | Convert to $\sin,\cos$, common denominator, use square identity |
| Solving equations | Reference angle, quadrant signs, add periods, check domain |

---

## Topic 9 – Coordinate Geometry (Lines and Circles)

**Goal**: Master equations of lines and circles, find intersections, determine line‑circle positions, and write tangent equations to circles.

> Learning path:  
> 9.1–9.2 → Line equations, slope, parallel/perpendicular  
> 9.3–9.4 → Circle equations (standard, general), centre, radius  
> 9.5 → Line‑circle intersection (discriminant)  
> 9.6 → Tangents to circles (three cases)

### 9.1 Straight line equations

#### 9.1.1 Common forms

- **Slope‑intercept**: $y = mx + c$ ($m$ = slope, $c$ = $y$-intercept)
- **Point‑slope**: $y - y_1 = m(x - x_1)$ (through $(x_1,y_1)$ with slope $m$)
- **General**: $Ax + By + C = 0$ (slope $m = -\frac{A}{B}$ if $B\neq0$)

#### 9.1.2 Slope formula

Given two points $(x_1,y_1)$ and $(x_2,y_2)$:
$$
m = \frac{y_2 - y_1}{x_2 - x_1}
$$

#### 9.1.3 Parallel and perpendicular

- **Parallel**: $m_1 = m_2$
- **Perpendicular**: $m_1 \cdot m_2 = -1$ (provided both slopes exist)

**Example**: Line $L_1: y=2x+3$ has slope $2$.  
Parallel line: slope $2$. Perpendicular line: slope $-\frac12$.

### 9.2 Distance from a point to a line

Point $P(x_0,y_0)$ to line $Ax+By+C=0$:
$$
d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2+B^2}}
$$

**Example**: Point $(1,2)$ to line $3x-4y+5=0$:
$$
d = \frac{|3-8+5|}{5} = \frac{0}{5}=0
$$
(Point lies on the line.)

### 9.3 Circle equations

#### 9.3.1 Standard form

Centre $(a,b)$, radius $r$:
$$
(x-a)^2 + (y-b)^2 = r^2
$$

**Example**: Centre $(2,-3)$, radius $4$: $(x-2)^2+(y+3)^2=16$.

#### 9.3.2 General form

$$
x^2 + y^2 + 2gx + 2fy + c = 0
$$
- Centre: $(-g, -f)$
- Radius: $\sqrt{g^2+f^2-c}$ (requires $g^2+f^2-c > 0$)

**Example**: $x^2+y^2-4x+6y+9=0$  
$2g=-4 \Rightarrow g=-2$, $2f=6 \Rightarrow f=3$, $c=9$  
Centre $(-g,-f)=(2,-3)$, radius $\sqrt{(-2)^2+3^2-9}=\sqrt{4+9-9}=2$.

> **Common trap**: Sign of centre coordinates – opposite to $g,f$.

### 9.4 Position of a line and a circle

Substitute line equation into circle equation → quadratic in $x$ (or $y$). Discriminant $\Delta$ determines:
- $\Delta > 0$: line intersects circle at two distinct points (secant)
- $\Delta = 0$: line touches circle at one point (tangent)
- $\Delta < 0$: line does not meet circle (no intersection)

**Example**: $y = x+1$ and $x^2+y^2=1$.  
Substitute: $x^2+(x+1)^2=1 \Rightarrow 2x^2+2x=0 \Rightarrow 2x(x+1)=0$ → two solutions → intersecting.

### 9.5 Tangents to a circle (three cases)

#### 9.5.1 Given point of tangency $(x_1,y_1)$ on the circle

For circle $(x-a)^2+(y-b)^2=r^2$, the tangent at $(x_1,y_1)$ is:
$$
(x_1-a)(x-a) + (y_1-b)(y-b) = r^2
$$

**Example**: Circle $x^2+y^2=5$, point $(1,2)$.  
Tangent: $1·x + 2·y = 5$ → $x+2y=5$.

#### 9.5.2 Given slope $m$

For circle centre $(a,b)$, radius $r$, tangents with slope $m$:
$$
y - b = m(x-a) \pm r\sqrt{1+m^2}
$$
(If centre at origin: $y = mx \pm r\sqrt{1+m^2}$.)

**Example**: Circle $x^2+y^2=9$, slope $2$: $y = 2x \pm 3\sqrt{1+4}=2x \pm 3\sqrt5$.

#### 9.5.3 Tangent from an external point $(x_0,y_0)$

**Procedure**: Let tangent have slope $m$: $y-y_0 = m(x-x_0)$. Write in general form, use distance from centre = radius to solve for $m$ (usually two solutions). Check vertical line separately.

**Example**: Find tangents from $(4,0)$ to $x^2+y^2=4$.  
Let $y = m(x-4)$ → $mx - y -4m = 0$.  
Distance from centre $(0,0)$ to line = $2$:
$$
\frac{|-4m|}{\sqrt{m^2+1}} = 2 \Rightarrow \frac{4|m|}{\sqrt{m^2+1}}=2 \Rightarrow 2|m|=\sqrt{m^2+1}
$$
Square: $4m^2 = m^2+1 \Rightarrow 3m^2=1 \Rightarrow m=\pm\frac{1}{\sqrt3}$.  
Tangents: $y = \frac{1}{\sqrt3}(x-4)$ and $y = -\frac{1}{\sqrt3}(x-4)$.  
Check vertical $x=4$: distance from centre to $x=4$ is $4 \neq 2$, so not tangent.

> **Trap**: Always test the vertical line possibility when the external point has $x_0$ outside the circle.

### 9.6 Worked examples

**Example 1**: Find circle with centre on $y=2x$ passing through $(1,1)$ and $(2,3)$.  
Let centre $(a,2a)$. Distances squared equal:  
$(1-a)^2+(1-2a)^2 = (2-a)^2+(3-2a)^2$  
Expand: $(1-2a+a^2)+(1-4a+4a^2) = (4-4a+a^2)+(9-12a+4a^2)$  
$(2-6a+5a^2) = (13-16a+5a^2) \Rightarrow -6a+2 = -16a+13 \Rightarrow 10a=11 \Rightarrow a=1.1$  
Centre $(1.1,2.2)$, radius$^2 = (1-1.1)^2+(1-2.2)^2 = 0.01+1.44=1.45$  
Equation: $(x-1.1)^2+(y-2.2)^2=1.45$.

**Example 2**: Find $k$ such that $y=x+k$ is tangent to $x^2+y^2=4$.  
Substitute: $x^2+(x+k)^2=4 \Rightarrow 2x^2+2kx+k^2-4=0$  
Tangent → discriminant $=0$: $(2k)^2 - 4·2·(k^2-4)=0 \Rightarrow 4k^2-8k^2+32=0 \Rightarrow -4k^2+32=0 \Rightarrow k^2=8 \Rightarrow k=\pm2\sqrt2$.

### 9.7 Topic 9 Summary

| Concept | Key points |
|---------|-------------|
| Line equations | slope‑intercept, point‑slope, general |
| Parallel/perpendicular | $m_1=m_2$ or $m_1m_2=-1$ |
| Point‑line distance | $d = \frac{|Ax_0+By_0+C|}{\sqrt{A^2+B^2}}$ |
| Circle standard | $(x-a)^2+(y-b)^2=r^2$, centre $(a,b)$, radius $r$ |
| Circle general | $x^2+y^2+2gx+2fy+c=0$, centre $(-g,-f)$, radius $\sqrt{g^2+f^2-c}$ |
| Line‑circle intersection | Substitute, discriminant $\Delta$: >0 secant, =0 tangent, <0 none |
| Tangent to circle | Three cases: at point on circle; given slope; from external point |

---

## Topic 10 – Mixed Applications

**Goal**: Combine knowledge from previous chapters to solve typical problems involving multiple topics. Develop cross‑topic mathematical thinking.

> Topics covered: functions, quadratics, polynomials, equations/inequalities, exponentials/logarithms, lines and circles, radians, trigonometry, permutations/combinations, binomial theorem, vectors, calculus (differentiation & integration).

### 10.1 Functions and quadratics

**Example**: $f(x)=x^2-4x+3$.  
1. Vertex and range: complete square $(x-2)^2-1$, vertex $(2,-1)$, range $[-1,\infty)$.  
2. Max/min on $[0,3]$: vertex inside → min $-1$; endpoints $f(0)=3$, $f(3)=0$ → max $3$.  
3. Solve $f(x)>0$: $(x-1)(x-3)>0$ → $x<1$ or $x>3$.

> **Trap**: When finding range on an interval, check if vertex lies inside.

### 10.2 Functions with exponentials and logarithms

**Example**: $f(x)=e^{2x}$, $g(x)=\ln x$.  
1. $h(x)=f(g(x)) = e^{2\ln x}=e^{\ln(x^2)}=x^2$, domain $x>0$.  
2. Solve $h(x)=e^4$: $x^2=e^4 \Rightarrow x=e^2$ (positive root only).  
3. $h'(x)=2x$.

> **Trap**: Don’t forget domain of $\ln x$ ($x>0$); discard negative roots.

### 10.3 Trigonometric equations with identities, radians

**Example**: Solve $2\sin^2 x + \cos x = 1$, $0\le x<2\pi$.  
Use $\sin^2 x = 1-\cos^2 x$: $2(1-\cos^2 x)+\cos x=1 \Rightarrow 2-2\cos^2 x+\cos x-1=0 \Rightarrow -2\cos^2 x+\cos x+1=0$  
Multiply by $-1$: $2\cos^2 x-\cos x-1=0$. Let $u=\cos x$: $2u^2-u-1=0 \Rightarrow u=1$ or $u=-\frac12$.  
- $\cos x=1 \Rightarrow x=0$  
- $\cos x=-\frac12 \Rightarrow x=\frac{2\pi}{3},\ \frac{4\pi}{3}$  
Solution set: $\{0,\frac{2\pi}{3},\frac{4\pi}{3}\}$.

### 10.4 Lines, circles, vectors

**Example**: Circle $(x-1)^2+(y-2)^2=5$, line $y=x+k$.  
1. When $k=1$, find intersections: substitute $y=x+1$: $(x-1)^2+(x-1)^2=5 \Rightarrow 2(x-1)^2=5 \Rightarrow (x-1)^2=2.5 \Rightarrow x=1\pm\sqrt{2.5}$, $y=x+1$.  
2. Tangency condition: distance from centre $(1,2)$ to line $x-y+k=0$ equals $\sqrt5$: $\frac{|1-2+k|}{\sqrt2}=\sqrt5 \Rightarrow |k-1|=\sqrt{10} \Rightarrow k=1\pm\sqrt{10}$.

### 10.5 Calculus with kinematics and optimisation

**Example**: $s(t)=t^3-6t^2+9t+2$, $t\ge0$.  
1. $v(t)=3t^2-12t+9$, $a(t)=6t-12$.  
2. Direction change when $v=0$ and sign changes: $v=3(t-1)(t-3)=0$ at $t=1,3$. Test signs: $t<1$: $v>0$; $1<t<3$: $v<0$; $t>3$: $v>0$ → changes at both.  
3. $v(2)=3·4-24+9=-3$, $a(2)=12-12=0$.  
4. Displacement $s(4)-s(0)= (64-96+36+2)-2 = 6-2=4$.

### 10.6 Permutations, combinations, binomial theorem

**Example**:  
1. From 5 boys, 3 girls, choose 4 with at least 2 girls. Total $C(8,4)=70$. Subtract cases with 0 girls ($C(5,4)=5$) or 1 girl ($C(3,1)C(5,3)=3·10=30$) → $70-35=35$.  
2. Constant term in $(x+\frac{2}{x})^6$: general term $\binom{6}{r}x^{6-r}(2x^{-1})^r = \binom{6}{r}2^r x^{6-2r}$. Set $6-2r=0 \Rightarrow r=3$, term $=\binom{6}{3}2^3=20·8=160$.

### 10.7 Vectors and geometry

**Example**: $\vec{a}=(1,2)$, $\vec{b}=(3,-1)$.  
1. $\vec{a}+\vec{b}=(4,1)$, $|\vec{a}+\vec{b}|=\sqrt{17}$.  
2. Unit vector perpendicular to $\vec{a}$: any $(x,y)$ with $x+2y=0$, e.g. $(2,-1)$, unit $=\frac{1}{\sqrt5}(2,-1)$.  
3. $\vec{a}+t\vec{b}=(1+3t,2-t)$ parallel to $\vec{a}$ ⇒ $(1+3t)/1 = (2-t)/2$ ⇒ $2+6t=2-t$ ⇒ $7t=0$ ⇒ $t=0$.

### 10.8 Calculus – area between curve and tangent

**Example**: $y=x^2$ at $(1,1)$, tangent $y=2x-1$. Area between curve and tangent from $x=0$ to $1$:  
$$
\int_0^1 [x^2-(2x-1)]\,dx = \int_0^1 (x^2-2x+1)\,dx = \int_0^1 (x-1)^2\,dx = \left[\frac{(x-1)^3}{3}\right]_0^1 = 0 - \frac{(-1)^3}{3} = \frac13.
$$

### 10.9 Exponential, logarithm and calculus (product rule)

**Example**: $f(x)=e^{2x}\ln x$.  
$f'(x)= (e^{2x})'\ln x + e^{2x}(\ln x)' = 2e^{2x}\ln x + e^{2x}\cdot\frac1x = e^{2x}\left(2\ln x + \frac1x\right)$.

### 10.10 Trigonometry and calculus

**Example**: $y=\sin(2x)$, tangent at $x=\frac{\pi}{4}$.  
$y' = 2\cos(2x)$. At $x=\frac{\pi}{4}$, $y=\sin(\frac{\pi}{2})=1$, $y' = 2\cos(\frac{\pi}{2})=0$. Tangent: $y=1$ (horizontal).

### 10.11 Topic 10 Summary

Mixed problems often combine:
- Function properties + inequalities
- Exponentials/logarithms + composite functions + derivatives
- Trig identities + solving equations
- Lines and circles + discriminant + distance
- Kinematics + derivatives + displacement/velocity/acceleration
- Permutations/combinations + binomial theorem
- Vectors + geometry
- Calculus + area/tangents

**Revision advice**:
- Master basic formulas from each chapter (derivatives, integrals, trig identities, combinatorics).
- Practice cross‑topic problems to build multi‑angle thinking.
- Watch for common traps: domain, sign, radian/degree, classification, checking validity of solutions.

---
