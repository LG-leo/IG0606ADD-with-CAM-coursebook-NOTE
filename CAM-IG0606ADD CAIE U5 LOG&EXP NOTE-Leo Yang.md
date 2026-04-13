# U5 – Logarithmic and Exponential Functions[not classify with course book]
##This chapter purely tests comprehensive application. You must ensure that you master all the methods (adding steps, increasing complexity, adding conditions, and solving application problems (plus other units)). Application problems will be presented in a separate chapter


## 5.1 Definitions & Basic Properties

### Logarithms

For \(a > 0,\ a \neq 1\) and \(x > 0\):
\[
y = \log_a x \quad\Longleftrightarrow\quad a^y = x
\]

- \(\log_a x\) is the **power** you raise \(a\) to get \(x\).  
- In IGCSE 0606, \(\log_{10}x\) is often written as \(\lg x\).  
- Natural logarithm: \(\ln x = \log_e x\), where \(e \approx 2.718\).

**Common values**:  
\(\lg 10 = 1,\quad \lg 100 = 2,\quad \ln e = 1,\quad \ln 1 = 0\)

---

### Exponential Functions

For \(a > 0,\ a \neq 1\):
\[
y = a^x
\]

---

## 5.2 Laws of Logarithms

| Rule (in symbols) | Example |
|------------------|---------|
| \(\log_a (MN) = \log_a M + \log_a N\) | \(\lg(2\times5) = \lg2 + \lg5\) |
| \(\log_a \frac{M}{N} = \log_a M - \log_a N\) | \(\lg\frac{100}{10} = \lg100 - \lg10 = 2 - 1 = 1\) |
| \(\log_a (M^k) = k \log_a M\) | \(\lg(10^3) = 3\lg10 = 3\) |
| \(\log_a a = 1\) | \(\lg10 = 1\) |
| \(\log_a 1 = 0\) | \(\lg1 = 0\) |

> **Note**: These rules work for any base \(a\) (\(a>0,\ a\neq1\)).  
> “Addition” outside the log becomes multiplication inside; “subtraction” becomes division; multiplication outside becomes power inside.

---

## 5.3 Graphs – Exponential vs Logarithmic

### Exponential \(y = a^x\)

| \(a > 1\) | \(0 < a < 1\) |
|----------|--------------|
| Passes through \((0,1)\) | Passes through \((0,1)\) |
| Increasing | Decreasing |
| \(x\)-axis (\(y=0\)) is a **horizontal asymptote** | \(x\)-axis (\(y=0\)) is a **horizontal asymptote** |
| As \(x \to -\infty,\ y \to 0^+\) | As \(x \to +\infty,\ y \to 0^+\) |
| As \(x \to +\infty,\ y \to +\infty\) | As \(x \to -\infty,\ y \to +\infty\) |

### Logarithmic \(y = \log_a x\)

| \(a > 1\) | \(0 < a < 1\) |
|----------|--------------|
| Passes through \((1,0)\) | Passes through \((1,0)\) |
| Increasing | Decreasing |
| \(y\)-axis (\(x=0\)) is a **vertical asymptote** | \(y\)-axis (\(x=0\)) is a **vertical asymptote** |
| As \(x \to 0^+,\ y \to -\infty\) | As \(x \to 0^+,\ y \to +\infty\) |
| As \(x \to +\infty,\ y \to +\infty\) | As \(x \to +\infty,\ y \to -\infty\) |

**Key symmetry**:  
\(y = \log_a x\) and \(y = a^x\) are **inverse functions**. Their graphs are reflections of each other in the line \(y = x\).

---

## 5.4 Domain and Range

| Function | Domain | Range |
|----------|--------|-------|
| \(y = a^x\) (\(a>0,\ a\neq1\)) | \(\mathbb{R}\) (all real numbers) | \(y > 0\) |
| \(y = \log_a x\) (\(a>0,\ a\neq1\)) | \(x > 0\) | \(\mathbb{R}\) |

**Important for composite functions**:
- For \(y = \ln(ax+b)\): **inside must be positive**, i.e. \(ax+b > 0\).  
- Example: \(f(x) = \ln(3-x)\) has domain \(3-x > 0 \Rightarrow x < 3\).

---

## 5.5 Solving Equations with Logs and Exponentials

### 5.5.1 Exponential Equations

**Method**: Take logs of both sides (usually \(\lg\) or \(\ln\)), then use the power rule.

**Example**: Solve \(5^x = 65\).

\[
\begin{aligned}
5^x &= 65 \\
\lg(5^x) &= \lg 65 \\
x \lg 5 &= \lg 65 \\
x &= \frac{\lg 65}{\lg 5} \approx 2.593
\end{aligned}
\]

### 5.5.2 Logarithmic Equations

**Method**: Combine logs using the laws, then convert to exponential form. **Always check the domain** (arguments of logs must be positive).

**Example**: Solve \(2\lg(4+x) = \lg(8+2x)\).

\[
\begin{aligned}
\lg(4+x)^2 &= \lg(8+2x) \\
(4+x)^2 &= 8+2x \\
x^2 + 8x + 16 &= 8 + 2x \\
x^2 + 6x + 8 &= 0 \\
(x+2)(x+4) &= 0 \\
x &= -2 \quad\text{or}\quad x = -4
\end{aligned}
\]

**Check domain**:  
\(4+x > 0 \Rightarrow x > -4\)  
\(8+2x > 0 \Rightarrow x > -4\)  

- \(x = -2\) is valid (\(-2 > -4\)) ✅  
- \(x = -4\) is **not** valid (\(4+(-4)=0\), log undefined) ❌  

**Solution**: \(x = -2\).

---

## 5.6 Change of Base Formula

\[
\log_a b = \frac{\log_c b}{\log_c a} \qquad (c > 0,\ c \neq 1)
\]

Commonly we use \(c = 10\) or \(c = e\):

\[
\log_a b = \frac{\lg b}{\lg a} \quad\text{or}\quad \log_a b = \frac{\ln b}{\ln a}
\]

**Special case**: \(\log_a b = \dfrac{1}{\log_b a}\) (when the two bases are swapped).

---

## 5.7 Transformations (Shifts)

### Exponential: \(y = a^{x} + c\)  
- Horizontal asymptote moves from \(y=0\) to \(y=c\).  
- Example: \(y = 2^x + 3\) has asymptote \(y=3\).

### Logarithmic: \(y = \log_a (x - h)\)  
- Vertical asymptote moves from \(x=0\) to \(x=h\).  
- Example: \(y = \ln(x-2)\) has asymptote \(x=2\).

---

## 5.8 A Typical “Mixed” Log Equation (from past papers)

**Problem**: Solve \(\displaystyle \frac{\ln(2x+3)}{\ln 5} = 2\).

**Solution**:

\[
\begin{aligned}
\frac{\ln(2x+3)}{\ln 5} &= 2 \\
\ln(2x+3) &= 2\ln 5 \\
\ln(2x+3) &= \ln(5^2) \\
2x+3 &= 25 \\
2x &= 22 \\
x &= 11
\end{aligned}
\]

**Check domain**: \(2x+3 > 0 \Rightarrow 11 > -1.5\) ✅.

---

## 5.9 Inverse Functions

For \(y = a^x\): swap \(x\) and \(y\) → \(x = a^y\) → \(y = \log_a x\).  
So \(f(x) = a^x\) and \(f^{-1}(x) = \log_a x\) are inverses.

**Example**: Find the inverse of \(f(x) = e^{2x}\).

\[
\begin{aligned}
y &= e^{2x} \\
x &= e^{2y} \quad\text{(swap)}\\
\ln x &= 2y \\
y &= \frac{1}{2}\ln x
\end{aligned}
\]
Thus \(f^{-1}(x) = \frac12 \ln x\).

---

## 5.10 Summary – Key Points to Remember

- \(\log_a x\) is defined only for \(x>0\).  
- \(\log_a 1 = 0\), \(\log_a a = 1\).  
- Laws: \(\log(MN)=\log M+\log N\), \(\log(M/N)=\log M-\log N\), \(\log(M^k)=k\log M\).  
- Exponential \(y=a^x\) has horizontal asymptote \(y=0\); logarithmic \(y=\log_a x\) has vertical asymptote \(x=0\).  
- Transformations shift asymptotes: \(y=a^x+c\) shifts asymptote to \(y=c\); \(y=\log_a(x-h)\) shifts asymptote to \(x=h\).  
- When solving logarithmic equations, **always check domain** (arguments > 0).

---
---
# IGCSE 0606 Exponential and Logarithmic Functions (Chapter 5) – Problem-Solving Guide (Revised Edition)
-我真的服了，教辅书的编辑真的不知道真题考啥，怎么考吗？真的不知道这些东西怎么做才是对的吗，这个章节怎么只教释义啊！
---

## Step 1: Exponential Equations

**Core Goal**: Either make the bases the same, or take logarithms to bring the exponent down.

### 1. Same Base Method

- **When to use**: Both sides can be written as powers of the same number (e.g., 2, 3, e, 10).
- **Method**: If \(a^m = a^n\) (with \(a > 0\) and \(a \neq 1\)), then \(m = n\).
- **Tip**: When you see numbers like 2, 4, 8 or 3, 9, 27, rewrite them as powers of the same base (e.g., \(8 = 2^3\), \(27 = 3^3\)).
- **Example**: \(2^{x+1} = 8\) → \(2^{x+1} = 2^3\) → \(x+1 = 3\) → \(x = 2\).

### 2. Taking Logarithms Method

- **When to use**: Bases cannot be made the same (e.g., \(2^x = 5\), \(e^{2x} = 10\)).
- **Method**: Take \(\ln\) (natural log) or \(\lg\) (common log) of both sides. Then use the power rule: \(\ln(a^b) = b \ln a\).
- **Tip**: If the equation contains \(e\) (the natural exponential), use \(\ln\) because \(\ln e = 1\) simplifies the working.
- **Important**: You must take logs of **both sides** together. You cannot take logs of only one side.
  - ✅ Correct: \(2^x = 5\) → \(\lg(2^x) = \lg 5\) → \(x \lg 2 = \lg 5\) → \(x = \frac{\lg 5}{\lg 2}\)
  - ❌ Wrong: \(2^x = 5\) → \(x = \lg 5\) (this loses the factor \(\lg 2\))

---

## Step 2: Logarithmic Equations

**Core Goal**: Use logarithm laws to combine or split terms. **Always check the domain** – the argument of every logarithm must be positive.

### 1. Change of Base

- **Formula**: \(\displaystyle \log_a b = \frac{\log_c b}{\log_c a}\) (usually choose \(c = 10\) or \(c = e\)).
- **Useful form**: \(\displaystyle \log_a b = \frac{1}{\log_b a}\).
- **Example**: Simplify \(\log_5 10\) → \(\frac{\lg 10}{\lg 5} = \frac{1}{\lg 5}\).

### 2. Laws of Logarithms

| Law | Formula | Example |
|-----|---------|---------|
| Addition | \(\log_a M + \log_a N = \log_a (MN)\) | \(\lg 2 + \lg 5 = \lg(2\times5) = \lg 10 = 1\) |
| Subtraction | \(\log_a M - \log_a N = \log_a \left(\frac{M}{N}\right)\) | \(\lg 100 - \lg 10 = \lg(100/10) = \lg 10 = 1\) |
| Power rule | \(\log_a (M^k) = k \log_a M\) | \(\lg(10^3) = 3\lg 10 = 3\) |

- **Exam focus**: Many questions ask you to simplify an expression into the form \(c + d\log y\). To do this, you split products and quotients using addition/subtraction rules, then use the power rule to move coefficients.

### 3. ⚠️ Critical Warning: Extraneous Solutions

- After solving a logarithmic equation, **substitute your solutions back into the original equation**.
- Any solution that makes any logarithm’s argument ≤ 0 must be rejected.
- **Example**: Solve \(\lg(x-1) + \lg(x+1) = 0\)  
  → \(\lg[(x-1)(x+1)] = 0\) → \((x-1)(x+1) = 1\) → \(x^2 - 1 = 1\) → \(x^2 = 2\) → \(x = \sqrt{2}\) or \(x = -\sqrt{2}\).
  - \(x = \sqrt{2} \approx 1.41\) → \(x-1 > 0\), \(x+1 > 0\) ✅
  - \(x = -\sqrt{2} \approx -1.41\) → \(x-1 < 0\) ❌ (argument of first log is negative) → reject.

---

## Step 3: Quadratic-Type Exponential/Logarithmic Equations

**Core Goal**: Use substitution to turn the equation into a quadratic.

### Substitution Method

- **When to use**: The equation contains a term and its square, e.g., \(5^x\) and \(5^{2x} = (5^x)^2\), or \(\ln x\) and \((\ln x)^2\).
- **Method**:
  1. Let \(y = 5^x\) (or \(y = \ln x\), etc.).
  2. The equation becomes a quadratic in \(y\): \(ay^2 + by + c = 0\).
  3. Solve for \(y\).
  4. **Replace \(y\) back**: solve \(5^x = y\) (or \(e^x = y\), etc.) for \(x\).
- **Important**: If \(y = 5^x\), then \(y\) must be **positive** (exponential functions only give positive outputs). If you get a negative \(y\), discard it.
- **Example**: \(3^{2x} - 4\cdot3^x + 3 = 0\)  
  Let \(y = 3^x\). Then \(y^2 - 4y + 3 = 0\) → \((y-1)(y-3)=0\) → \(y = 1\) or \(y = 3\).  
  - \(3^x = 1\) → \(x = 0\)  
  - \(3^x = 3\) → \(x = 1\)  
  Both solutions are valid (no negative \(y\)).

---

## Step 4: Simultaneous Exponential Equations

**Core Goal**: Reduce to a system of linear equations by expressing everything with the same prime base.

### Method: Prime Base Reduction

- **When to use**: Equations like \(8^q = 2^{p+1}\) and \(4^p = 2^{q}\).
- **Steps**:
  1. Write each number as a power of a prime (2, 3, 5, etc.).
  2. Use the power rule: \((a^m)^n = a^{mn}\).
  3. Equate exponents to form linear equations.
  4. Solve the linear system.
- **Example**: \(8^q = 2^{p+1}\) and \(4^p = 2^{q}\).
  - \(8^q = (2^3)^q = 2^{3q}\) → so \(3q = p+1\)
  - \(4^p = (2^2)^p = 2^{2p}\) → so \(2p = q\)
  - Solve: \(q = 2p\) → substitute into \(3(2p) = p+1\) → \(6p = p+1\) → \(5p = 1\) → \(p = 0.2\), \(q = 0.4\).

---

## Step 5: Domain, Graphs and Transformations

**Core Goal**: Understand the restrictions on \(x\) and how shifting changes the graph.

### 1. Domain Restrictions for Logarithms

- For \(\log_b(f(x))\), we require \(f(x) > 0\).
- If there are multiple logarithms, **take the intersection** of all their domain conditions.
- **Example**: \(\ln(x-2) + \ln(5-x)\) requires \(x-2 > 0\) AND \(5-x > 0\) → \(x > 2\) and \(x < 5\) → domain \(2 < x < 5\).

### 2. Finding Intersections Graphically

- If you see a problem like \(a^x = kx + b\), it often asks for the number of solutions.
- Sketch \(y = a^x\) and \(y = kx + b\) (a line). Count their intersection points.
- For exact intersection (e.g., \(\log_a x = c\)), convert to exponential form: \(x = a^c\).

### 3. Transformations (Shifting Asymptotes)

- **Exponential**: \(y = a^x + c\)  
  - Horizontal asymptote moves from \(y = 0\) to \(y = c\).  
  - Example: \(y = 2^x + 3\) has asymptote \(y = 3\).
- **Logarithmic**: \(y = \ln(x - h)\)  
  - Vertical asymptote moves from \(x = 0\) to \(x = h\).  
  - Example: \(y = \ln(x-2)\) has asymptote \(x = 2\), domain \(x > 2\).

---

## Step 6: Solving Quadratic Forms (Again, but with Logs)

**Core Goal**: Recognize when a substitution turns a logarithmic equation into a quadratic.

### Factoring After Substitution

- **When to use**: The equation contains \(\ln(5x)\) and \((\ln(5x))^2\).
- **Method**: Let \(u = \ln(5x)\). Solve \(au^2 + bu + c = 0\) by factoring or the quadratic formula.
- **Important trap**: \(\ln(5x)\) is **not** equal to \(\ln 5 \cdot \ln x\). The power rule only applies when the **argument** is raised to a power, not when the whole logarithm is multiplied.

- **Example**: \(3(\ln 5x)^2 + 2\ln 5x - 1 = 0\)  
  Let \(u = \ln 5x\). Then \(3u^2 + 2u - 1 = 0\) → \((3u - 1)(u + 1) = 0\) → \(u = \frac{1}{3}\) or \(u = -1\).  
  - \(\ln 5x = \frac13\) → \(5x = e^{1/3}\) → \(x = \frac{1}{5}e^{1/3}\)  
  - \(\ln 5x = -1\) → \(5x = e^{-1}\) → \(x = \frac{1}{5e}\)

---

## Additional Topics

### Parameter Problems (Equations with Unknown Constants)

- **When to use**: The problem says “the equation has exactly one solution”, “no real solution”, etc.
- **Strategy**:
  - For equations like \(2^x = k - x\), think about the graphs: \(y = 2^x\) (exponential) and \(y = k - x\) (a straight line with slope -1). The number of solutions is the number of intersection points.
  - For quadratic forms after substitution, use the discriminant: \(\Delta = 0\) gives one solution, \(\Delta > 0\) gives two, etc., **but** remember to check domain restrictions on the substituted variable (e.g., \(y = 5^x > 0\)).

### Applications: Exponential Growth/Decay

- **Standard forms**:  
  - \(N = N_0 e^{kt}\) (continuous growth, e.g., bacteria, radioactive decay)  
  - \(N = N_0 a^t\) (discrete growth, e.g., compound interest)
- **How to solve**:
  1. Identify \(N_0\) (initial value) from the context.
  2. Use one data point to find the growth factor \(k\) or \(a\).
  3. Answer the question (find a value, find time, etc.).
- **Example**: A population starts at 100 and triples every 2 hours. Find a formula and the population after 5 hours.  
  - \(P = 100 \cdot 3^{t/2}\) (because after 2 hours, multiply by 3)  
  - After 5 hours: \(P = 100 \cdot 3^{2.5} = 100 \cdot 3^{5/2} = 100 \cdot 3^2 \cdot \sqrt{3} = 900\sqrt{3}\)
-# Supplement: Exponential/Logarithmic Equations with Parameters

**Core idea**: Number of solutions → convert to number of intersection points of graphs, or to root distribution of a quadratic equation.

────────────────────────────────
# Supplement: Exponential/Logarithmic Equations with Parameters

**Core idea**: Reduce the problem of counting solutions to either the number of intersection points of two graphs, or to the distribution of roots of a quadratic equation after substitution.

---

## Method 1: Graphical Method

**When to use**: The two sides of the equation have very different forms (e.g., exponential vs. line, logarithmic vs. line).

**Steps**:
1. Rewrite the equation as \( f(x) = g(x) \), placing the parameter in one of the functions.
2. Sketch the graph of the function that does not contain the parameter.
3. Sketch the graph of the line (or curve) that contains the parameter; observe how the number of intersection points changes as the parameter varies.
4. Find the **tangency** condition (the critical case for a unique solution):
   - Let the tangency point be \((x_0, y_0)\).
   - Equal slopes: \( f'(x_0) = g'(x_0) \).
   - Equal function values: \( f(x_0) = g(x_0) \).
5. Solve for the critical parameter value(s).
6. Use the sketch to determine the parameter range that gives the required number of solutions.

**Example**: \( e^x = kx \) has exactly one solution. Find \( k \).

- Tangency condition: let the point of tangency be \((t, e^t)\).
  \[
  e^t = kt, \quad e^t = k
  \]
  Substituting \( e^t = k \) into the first equation gives \( k = kt \Rightarrow t = 1 \), hence \( k = e \).
- Graphical analysis:
  - \( k > e \): no intersection.
  - \( k = e \): one intersection (tangent).
  - \( 0 < k < e \): two intersections.
- **Answer**: \( k = e \).

---

## Method 2: Discriminant Method (Substitution)

**When to use**: The equation can be transformed into a quadratic by a substitution, e.g., \( a^{2x} \) and \( a^x \), or \( (\log x)^2 \) and \( \log x \).

**Steps**:
1. Substitute: let \( t = a^x \) (with \( t > 0 \)) or \( t = \log_a x \).
2. Obtain a quadratic equation in \( t \): \( A t^2 + B t + C = 0 \).
3. Translate the condition on the original equation (“has solution”, “has no solution”, “has a unique solution”) into conditions on the roots of this quadratic:
   - Has solution → the quadratic has a real root that lies in the allowed domain of \( t \).
   - No solution → no real root, or all real roots are outside the domain.
   - Unique solution → a double root that lies inside the domain, or exactly one of the two real roots lies inside the domain.
4. Use the discriminant \( \Delta \) and Vieta’s formulas (sum and product of roots) together with domain restrictions.
5. Solve for the parameter range and verify boundary cases (endpoints, domain conditions).

**Example**: \( 4^x - k \cdot 2^x + 1 = 0 \) has a solution. Find \( k \).

- Substitute \( t = 2^x > 0 \). Then \( 4^x = t^2 \), so the equation becomes \( t^2 - k t + 1 = 0 \).
- We need this quadratic to have a real root with \( t > 0 \).
- Discriminant: \( \Delta = k^2 - 4 \ge 0 \) → \( k \ge 2 \) or \( k \le -2 \).
- Vieta’s formulas: \( t_1 + t_2 = k \), \( t_1 t_2 = 1 > 0 \). The product is positive, so the two roots have the same sign.
- For a root to be positive, the sum must be positive (because both roots share the same sign). Hence \( k > 0 \).
- Combine with the discriminant condition: \( k \ge 2 \).
- Check boundary \( k = 2 \): \( t^2 - 2t + 1 = (t-1)^2 = 0 \), \( t = 1 > 0 \), valid.
- **Answer**: \( k \ge 2 \).

---

**Note**: After solving, always verify boundary cases and domain restrictions (e.g., the argument of a logarithm must be positive, exponential functions are positive).

---

## Vieta’s Formulas (韦达定理)

For a quadratic equation \( A t^2 + B t + C = 0 \) (\( A \neq 0 \)), let its two roots be \( t_1 \) and \( t_2 \). Then:

\[
t_1 + t_2 = -\frac{B}{A}, \qquad t_1 t_2 = \frac{C}{A}.
\]

---

### Application in Parameter Problems

After substitution, Vieta’s formulas help determine the sign or range of the roots, which translates into conditions on the parameter.

| Condition | Translated into Vieta |
|-----------|------------------------|
| Both roots have the same sign | \( t_1 t_2 > 0 \) |
| Roots have opposite signs | \( t_1 t_2 < 0 \) |
| Both roots are positive | \( t_1 + t_2 > 0 \) and \( t_1 t_2 > 0 \) |
| Both roots are negative | \( t_1 + t_2 < 0 \) and \( t_1 t_2 > 0 \) |
| At least one root is positive | Combine discriminant, sum/product, or use graph |
| One root lies in an interval, the other outside | Use \( f(m)f(n) < 0 \) (intermediate value property) |

---

### Example (continuing the previous one)

Equation \( 4^x - k \cdot 2^x + 1 = 0 \) has a solution. Find \( k \).

Substitute \( t = 2^x > 0 \), get \( t^2 - k t + 1 = 0 \).

From Vieta:
\[
t_1 + t_2 = k,\quad t_1 t_2 = 1.
\]

- Product \( = 1 > 0 \) → both roots have the same sign.
- Sum \( = k \): if \( k > 0 \) then both roots are positive; if \( k < 0 \) then both are negative.
- Since we need at least one root positive (because \( t > 0 \)), we require \( k > 0 \).
- Combined with discriminant \( \Delta = k^2 - 4 \ge 0 \) → \( k \ge 2 \) or \( k \le -2 \).
- Intersection: \( k \ge 2 \).

## 3. Equations Reducible to Quadratic Form (Examples)

### Example 1 (Exponential type)
Solve \(4^x - 6 \cdot 2^x + 8 = 0\).

- Let \(t = 2^x\) (note \(t > 0\)), then \(4^x = t^2\).
- The equation becomes \(t^2 - 6t + 8 = 0\).
- Factor: \((t-2)(t-4)=0\) → \(t = 2\) or \(t = 4\).
- Substitute back:
  - \(2^x = 2 \Rightarrow x = 1\)
  - \(2^x = 4 \Rightarrow x = 2\)
- Answer: \(x = 1,\;2\).

### Example 2 (Logarithmic type)
Solve \((\lg x)^2 - 3\lg x + 2 = 0\).

- Let \(t = \lg x\) (no restriction on \(t\)), then \(t^2 - 3t + 2 = 0\).
- Factor: \((t-1)(t-2)=0\) → \(t = 1\) or \(t = 2\).
- Substitute back:
  - \(\lg x = 1 \Rightarrow x = 10\)
  - \(\lg x = 2 \Rightarrow x = 100\)
- Answer: \(x = 10,\;100\) (domain automatically satisfied).
---

**Note**: Vieta gives only the sum and product, not the roots themselves. It must be used together with the discriminant and domain conditions.
---
---
────────────────────────────────
**Note**: Always verify boundary cases (endpoints, domain restrictions) after solving.
## exponengtial&logarium function with f(x)=x

### type of question
方程 \(a^x = kx\) 或 \(\log_a x = kx\) 有唯一解，求参数 \(k\) 的值或范围。

### formula

| type of function | point of tangence \(t\) | gradient \(k\) |
|----------|----------------|----------------|
| \(y = \log_a x\) 与 \(y = kx\) | \(t = e\) | \(k = \dfrac{1}{e \ln a}\) |
| \(y = a^x\) 与 \(y = kx\) | \(t = \dfrac{1}{\ln a}\) | \(k = e \ln a\) |

"So \(5^{2x+1}\) can be split as \(5^{x+1} \times 5^x\)"—actually captures the core insight of this type of substitution problem: **write the exponent as a sum, then factor out the common part \(5^x\)**.
For the equation \(\ln(3x) = 4 + \ln 2\), you want to “wrap” the constant \(4\) inside a logarithm so that you can combine the right‑hand side.

**Method**:  
Since \(4 = \ln(e^4)\), the right‑hand side becomes
\[
4 + \ln 2 = \ln(e^4) + \ln 2 = \ln(2e^4)
\]
Thus the equation is
\[
\ln(3x) = \ln(2e^4)
\]
Because the natural logarithm is one‑to‑one, we can drop the logs:
\[
3x = 2e^4 \quad\Longrightarrow\quad x = \frac{2e^4}{3}
\]

**General approach**: For any equation of the form \(\ln(\text{expression}) = k + \ln(\text{constant})\), write \(k = \ln(e^k)\), then use \(\ln A + \ln B = \ln(AB)\) to combine the right‑hand side into a single logarithm. Finally, equate the arguments and solve.
\[
5^{2x+1} = 5^{(x+1)+x} = 5^{x+1} \cdot 5^x
\]
Then with \(y = 5^x\) and \(5^{x+1} = 5y\), we get \(5y \cdot y = 5y^2\).

Of course, a more direct way is:
\[
5^{2x+1} = 5 \cdot 5^{2x} = 5 \cdot (5^x)^2 = 5y^2
\]
Both ways are essentially the same, just different perspectives—you split by adding exponents, I split by extracting the constant factor. The fact that you found this relationship shows you already have a solid grasp of exponential operations.
---

## Exam Checklist

Before you start, ask yourself:

1. **Bases**: Are the bases the same? If yes, equate exponents. If not, take logs.
2. **Structure**: Do you see \(a^x\) and \(a^{2x}\)? Use substitution to form a quadratic.
3. **Operations**: Are you adding/subtracting logs? Combine them into a single log.
4. **Domain**: If it’s a logarithmic equation, **always check** that solutions make all arguments positive.
5. **Coefficients**: In simultaneous equations, write everything with prime bases, then compare exponents.
6. **Graphs**: If the question asks for number of solutions or parameter ranges, sketch the two graphs.
7. **Applications**: For growth/decay, identify the initial value and use one data point to find the growth constant.

---
In calculus, the derivative formulas for the natural logarithm \(\ln x\) and the general logarithm \(\log_a x\) are:

\[
\frac{d}{dx}(\ln x) = \frac{1}{x} \quad (x>0)
\]

\[
\frac{d}{dx}(\log_a x) = \frac{1}{x \ln a} \quad (a>0, a\neq 1, x>0)
\]

When using the graphical method, if we set the point of tangency as \((t, \ln t)\), the slope of the curve \(y = \ln x\) at \(x = t\) is \(\frac{1}{t}\). This is why we have \(k = \frac{1}{t}\).

> Note: Differentiation belongs to Topic 14 (Calculus) in the syllabus, but these formulas can be used directly when applying the graphical method; derivation is not required.

## Exponential Equation (taking logs)

**Example**: Solve \(5^{2x} = 7^{x-1}\), giving the exact value.

**Solution**  
1. Take natural logs: \(\ln(5^{2x}) = \ln(7^{x-1})\)  
2. Use the power rule: \(2x\ln 5 = (x-1)\ln 7\)  
3. Expand: \(2x\ln 5 = x\ln 7 - \ln 7\)  
4. Bring terms together: \(2x\ln 5 - x\ln 7 = -\ln 7\)  
5. Factor \(x\): \(x(2\ln 5 - \ln 7) = -\ln 7\)  
6. Solve: \(\displaystyle x = \frac{-\ln 7}{2\ln 5 - \ln 7} = \frac{\ln 7}{\ln 7 - 2\ln 5}\)

---

## Change of Base

**Example**: Given \(\log_2 5 = a\), express \(\log_4 20\) in terms of \(a\).

**Solution**  
\[
\log_4 20 = \frac{\log_2 20}{\log_2 4} = \frac{\log_2(4\times5)}{2} = \frac{\log_2 4 + \log_2 5}{2} = \frac{2 + a}{2}
\]

---

## Exponential Equation Reducible to Quadratic

**Example** (2023 June 0606/21 Q5): Solve \(3^{2x} - 10\cdot 3^{x} + 9 = 0\).

**Solution**  
Let \(t = 3^{x}\;(t>0)\). Then \(t^2 - 10t + 9 = 0\).  
Factor: \((t-1)(t-9)=0\) → \(t = 1\) or \(t = 9\).  
Back‑substitute:
- \(3^{x} = 1\) → \(x = 0\)
- \(3^{x} = 9\) → \(x = 2\)

Thus \(x = 0\) or \(x = 2\).

\[
\log_{27} x = \frac{\log_3 x}{\log_3 27} = \frac{\log_3 x}{3} = \frac{1}{3} \log_3 x
\]

\[
\lg\left(\frac{1}{10^n}\right) = \lg(10^{-n}) = -n \cdot \lg 10 = -n
\]

\[
5e^{3x+4}=14 \implies e^{3x+4}=\frac{14}{5}
\]  

Take natural logarithms:  
\[
3x+4=\ln\left(\frac{14}{5}\right) \implies 3x=\ln\left(\frac{14}{5}\right)-4
\]  
\[
x=\frac{\ln\left(\frac{14}{5}\right)-4}{3}
\]  
For a numerical value, \(\ln(2.8)\approx 1.0296\), so \(x\approx \frac{1.0296-4}{3}=\frac{-2.9704}{3}\approx -0.9901\).

\[
\log_a(\sqrt{2}) + \log_a 8 + \log_a\left(\frac{1}{2}\right) = \frac{1}{2}\log_a 2 + 3\log_a 2 - \log_a 2 = \left(\frac{1}{2}+3-1\right)\log_a 2 = \frac{5}{2}\log_a 2
\]

Convert each term to base 2:

\[
8^{q-1} = (2^3)^{q-1} = 2^{3(q-1)}
\]
\[
2^{2p+1} \text{ remains as is}
\]
Right-hand side:
\[
4^7 = (2^2)^7 = 2^{14}
\]

Add the exponents on the left:
\[
3(q-1) + (2p+1) = 3q - 3 + 2p + 1 = 2p + 3q - 2
\]

Thus:
\[
2p + 3q - 2 = 14 \implies 2p + 3q = 16
\]

So the equation is \(2p + 3q = 16\). 

\[
(\log_2 r)(\log_r 2) = 1
\]

\[
2e^{1-2y} = 3e^{3y+2}
\]  
Take natural logarithms on both sides:  
\[
\ln 2 + (1-2y) = \ln 3 + (3y+2)
\]  
Rearrange:  
\[
\ln 2 - \ln 3 + 1 - 2 = 3y + 2y
\]  
\[
\ln\left(\frac{2}{3}\right) - 1 = 5y
\]  
\[
y = \frac{\ln\left(\frac{2}{3}\right) - 1}{5}
\]  
Alternatively, \(y = -\frac{1 + \ln\frac{3}{2}}{5}\).

---Mindlessly choose In if there is/are e.

The equation must be in the form \(e^{\text{expression}} = \text{constant}\) (e.g., \(5e^{3x+4}=14\)) before taking \(\ln\) on both sides.

If you have \(e^{A} = e^{B}\), simply set \(A = B\); you don't even need to take \(\ln\).

For equations like \(a^{x} = b\) where the base is not \(e\), you can take either \(\lg\) or \(\ln\). Taking \(\ln\) works just as well, but you don’t get the convenience of “canceling” the base.

### Equations reducible to quadratics (substitution method)

When the equation contains terms like \(a^{2x}\) and \(a^x\), or \((\log x)^2\) and \(\log x\), let \(t = a^x\) or \(t = \log x\) to obtain a quadratic.

**Example** (Cambridge IGCSE 0606 2014 Nov P1 Q4):  
Solve \(5^{2x+1} - 5^{x+1} + 2 = 2\cdot5^x\).

Let \(y = 5^x\). Then  
\(5^{2x+1} = 5 \cdot 5^{2x} = 5y^2\),  
\(5^{x+1} = 5y\), and the right side is \(2y\).

The equation becomes \(5y^2 - 5y + 2 = 2y\) → \(5y^2 - 7y + 2 = 0\).  
Factor: \((5y-2)(y-1)=0\) → \(y = \frac{2}{5}\) or \(y = 1\).  
Back‑substitute:
- \(5^x = 1\) → \(x = 0\)
- \(5^x = \frac{2}{5}\) → \(x = \log_5\frac{2}{5} = \frac{\ln\frac{2}{5}}{\ln5}\) (exact form)

**Note**: The resulting quadratic can be solved by factorisation (if possible) or the quadratic formula. In U2, we talk about this before.
---
Given
\[
\frac{\ln 8}{\ln(y-1)} = 3
\]
Multiply both sides by \(\ln(y-1)\) (noting \(y-1>0\) and \(y-1\neq1\) so that the logarithm is defined and the denominator is non‑zero):
\[
\ln 8 = 3\ln(y-1) = \ln\big((y-1)^3\big)
\]
Hence
\[
8 = (y-1)^3 \quad\Rightarrow\quad y-1 = 2 \quad\Rightarrow\quad y = 3
\]
Check the domain: \(y-1>0 \Rightarrow y>1\), and \(y-1\neq1 \Rightarrow y\neq2\).  
\(y=3\) satisfies both, so it is the only solution.
**Note**:To calculate by sequence, first find a quantity (for example, log_√b 9a), and then combine the pairs.
---
### Problem
Simplify  
\[
\log_a 4 + (\log_a \sqrt{b})\,(\log_{\sqrt{b}} 8a)
\]  
and express the result in the form \(c + d\log_a 4\).

---

### Step‑by‑step

**Step 1 – Simplify \(\log_a \sqrt{b}\)**  
\[
\log_a \sqrt{b} = \log_a b^{1/2} = \frac12 \log_a b
\]

**Step 2 – Change the base of \(\log_{\sqrt{b}} (8a)\) to base \(a\)**  
\[
\log_{\sqrt{b}} (8a) = \frac{\log_a (8a)}{\log_a \sqrt{b}}
\]  
Numerator: \(\log_a (8a) = \log_a 8 + \log_a a = \log_a 8 + 1\)  
Denominator (from Step 1): \(\log_a \sqrt{b} = \frac12 \log_a b\)  
Thus  
\[
\log_{\sqrt{b}} (8a) = \frac{\log_a 8 + 1}{\frac12 \log_a b} = \frac{2(\log_a 8 + 1)}{\log_a b}
\]

**Step 3 – Multiply the two logarithmic terms**  
\[
(\log_a \sqrt{b})(\log_{\sqrt{b}} 8a) = \left(\frac12 \log_a b\right)\cdot \left(\frac{2(\log_a 8 + 1)}{\log_a b}\right)
\]  
Cancel \(\log_a b\) and the factor \(2\):  
\[
= 1 \cdot (\log_a 8 + 1) = \log_a 8 + 1
\]

**Step 4 – Add the remaining \(\log_a 4\)**  
\[
\log_a 4 + (\log_a \sqrt{b})(\log_{\sqrt{b}} 8a) = \log_a 4 + \log_a 8 + 1
\]

**Step 5 – Combine \(\log_a 4 + \log_a 8\)**  
\[
\log_a 4 + \log_a 8 = \log_a (4 \times 8) = \log_a 32
\]

**Step 6 – Express \(\log_a 32\) in terms of \(\log_a 4\)**  
Notice \(32 = 4^{5/2}\) because \(4^{5/2} = (2^2)^{5/2} = 2^5 = 32\).  
Hence  
\[
\log_a 32 = \log_a (4^{5/2}) = \frac{5}{2}\log_a 4
\]

**Step 7 – Write the final expression**  
\[
\log_a 4 + (\log_a \sqrt{b})(\log_{\sqrt{b}} 8a) = \frac{5}{2}\log_a 4 + 1
\]  
So in the form \(c + d\log_a 4\) we have  
\[
c = 1,\qquad d = \frac{5}{2}
\]

---

**Final answer**  
\[
\boxed{1 + \frac{5}{2}\log_a 4}
\]

## Strategy for “Long Train” Logarithm Problems

When you see a complicated expression involving nested logarithms (e.g., \(\log_{\sqrt{b}} 9a\) inside a product), **split it into steps**:

1. **Isolate the most complex part** – treat it as a separate sub‑problem.  
2. **Simplify that part** using change of base or power rules.  
3. **Plug the simplified result back** and combine with the remaining terms.  

**Example** (as seen earlier):  
To simplify \(\log_a 9 + (\log_a b)(\log_{\sqrt{b}} 9a)\), first work on \(\log_{\sqrt{b}} 9a\):

\[
\log_{\sqrt{b}} 9a = \frac{\log_a (9a)}{\log_a \sqrt{b}} = \frac{\log_a 9 + 1}{\frac12 \log_a b} = \frac{2(1+\log_a 9)}{\log_a b}.
\]

Then multiply by \(\log_a b\) and add the remaining term.

This “divide and conquer” approach turns a long train into short, manageable carriages.
---

## One‑Line Summary

> **Exponentials take logs, logarithms need domain checks, change of base simplifies, graphs focus on asymptotes, substitution solves quadratics, and simultaneous equations reduce to prime bases.**

<!-- 
感谢使用这份笔记！如果你觉得它对你有帮助，请回到 GitHub 仓库页面点一个 ⭐，
这能帮助更多同学发现这个项目。仓库地址：https://github.com/LG-leo/IG0606ADD-with-CAM-coursebook-NOTE
-->
<!-- 
Thanks for using this note! If you find it helpful, please go back to the GitHub repository page and leave a ⭐.
It helps other students discover this project. Repository link: https://github.com/LG-leo/IG0606ADD-with-CAM-coursebook-NOTE
-->
