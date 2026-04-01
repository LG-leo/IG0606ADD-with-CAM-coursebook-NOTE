# Topic 9 & 10: Circular Measure & Trigonometry

---

## 9.1 Circular Measure (Radian Measure)

### 9.1.1 Basic Formulas
\[
s = r\theta, \quad A = \frac{1}{2}r^2\theta
\]
where \(\theta\) must be in radians, \(s\) is arc length, \(A\) is sector area.

**Conversion between degrees and radians**:
\[
180^\circ = \pi\ \text{rad} \quad\Rightarrow\quad 1^\circ = \frac{\pi}{180}\ \text{rad},\quad 1\ \text{rad} = \frac{180}{\pi}^\circ
\]

---

### 9.1.2 Basic Problems: Given radius and angle, find arc length or sector area

**Steps**:
1. If the angle is given in degrees, convert to radians: \(\theta_{\text{rad}} = \theta_{\text{deg}} \times \frac{\pi}{180}\).
2. Substitute into \(s = r\theta\) or \(A = \frac{1}{2}r^2\theta\).

**Example**: Radius 5 cm, central angle \(60^\circ\). Find arc length and sector area.
- Convert: \(60 \times \frac{\pi}{180} = \frac{\pi}{3}\) rad.
- Arc length: \(s = 5 \times \frac{\pi}{3} = \frac{5\pi}{3}\) cm.
- Sector area: \(A = \frac12 \times 25 \times \frac{\pi}{3} = \frac{25\pi}{6}\) cm².

**Pitfall**: Do not use degrees in the formulas; they require radians.

---

### 9.1.3 Composite Shapes (Sectors with Triangles or Polygons)

**Type**: Find the perimeter or area of a shape made of a sector and other polygons.

**Steps**:
1. Break the shape into basic parts (sector, triangle, rectangle, etc.).
2. Compute each part’s arc length, side lengths, area. Watch for overlapping edges.
3. Add or subtract as required.

**Example**: A shape consists of a sector of radius \(r\) and central angle \(\theta\) together with the triangle formed by the two radii. Find total area and perimeter.
- Sector area: \(A_{\text{sector}} = \frac12 r^2\theta\).
- Triangle area: \(A_{\triangle} = \frac12 r^2\sin\theta\) (if the included angle is \(\theta\)).
- Total area: \(A_{\text{total}} = \frac12 r^2\theta + \frac12 r^2\sin\theta\).
- Perimeter: two radii \(2r\) + arc length \(r\theta\) + chord length \(= 2r\sin\frac{\theta}{2}\) (if the third side is the chord).

> **Note**: If the shape is a segment (sector minus triangle), subtract the triangle area.

---

## 10.1 Trigonometric Functions – Basics

### 10.1.1 Six Functions (Unit Circle Definition)
For an angle \(\theta\) (in radians), let \(P(x,y)\) be the point on the unit circle. Then:
\[
\sin\theta = y,\quad \cos\theta = x,\quad \tan\theta = \frac{y}{x}\ (x\neq 0)
\]
\[
\csc\theta = \frac{1}{y}\ (y\neq 0),\quad \sec\theta = \frac{1}{x}\ (x\neq 0),\quad \cot\theta = \frac{x}{y}\ (y\neq 0)
\]

---

### 10.1.2 Special Angle Values (Must Memorise)

| Degrees | 0° | 30° | 45° | 60° | 90° | 180° | 270° | 360° |
|---------|----|----|----|----|----|----|----|----|
| Radians | 0 | \(\pi/6\) | \(\pi/4\) | \(\pi/3\) | \(\pi/2\) | \(\pi\) | \(3\pi/2\) | \(2\pi\) |
| \(\sin\) | 0 | 1/2 | \(\sqrt{2}/2\) | \(\sqrt{3}/2\) | 1 | 0 | -1 | 0 |
| \(\cos\) | 1 | \(\sqrt{3}/2\) | \(\sqrt{2}/2\) | 1/2 | 0 | -1 | 0 | 1 |
| \(\tan\) | 0 | \(1/\sqrt{3}\) | 1 | \(\sqrt{3}\) | undefined | 0 | undefined | 0 |

---

### 10.1.3 Given One Trig Value, Find Others

**Steps**:
1. Use \(\sin^2\theta + \cos^2\theta = 1\) to find the other sine/cosine.
2. Use \(\tan\theta = \frac{\sin\theta}{\cos\theta}\) to find tangent.
3. Reciprocal functions: \(\sec\theta = 1/\cos\theta\), etc.
4. **Determine sign using the quadrant**.

**Example**: \(\sin\theta = \frac{3}{5}\) and \(\theta\) is in quadrant II. Find \(\cos\theta\) and \(\tan\theta\).
- \(\cos^2\theta = 1 - \frac{9}{25} = \frac{16}{25}\) → \(\cos\theta = \pm\frac{4}{5}\).
- In quadrant II, cosine is negative → \(\cos\theta = -\frac{4}{5}\).
- \(\tan\theta = \frac{3/5}{-4/5} = -\frac{3}{4}\).

**Pitfall**: Forgetting the quadrant leads to wrong sign.

---

## 10.2 Graphs and Properties

### 10.2.1 Basic Graphs

| Function | Period | Parity | Zeros | Asymptotes | Range |
|----------|--------|--------|-------|------------|-------|
| \(\sin x\) | \(2\pi\) | odd | \(k\pi\) | none | \([-1,1]\) |
| \(\cos x\) | \(2\pi\) | even | \(\frac{\pi}{2}+k\pi\) | none | \([-1,1]\) |
| \(\tan x\) | \(\pi\) | odd | \(k\pi\) | \(x=\frac{\pi}{2}+k\pi\) | \(\mathbb{R}\) |

---

### 10.2.2 General Form: \(y = a\sin(bx+c)+d\) (and similarly for cosine, tangent)

**Steps to analyse**:
1. Amplitude: \(|a|\) (for sine/cosine).
2. Period: \(T = \frac{2\pi}{|b|}\) (for sine/cosine), \(T = \frac{\pi}{|b|}\) (for tangent).
3. Phase shift: \(-\frac{c}{b}\) (right if positive, left if negative).
4. Vertical shift: \(d\).

**Example**: \(y = 2\sin(3x-\frac{\pi}{2}) + 1\)
- Amplitude = 2
- Period = \(2\pi/3\)
- Phase shift: set \(3x-\frac{\pi}{2}=0\) → \(x=\frac{\pi}{6}\) → shift right by \(\frac{\pi}{6}\)
- Vertical shift = +1

**Pitfall**: Phase shift formula is \(-\frac{c}{b}\); be careful with sign.

---

### 10.2.3 Determine Equation from Graph

**Example**: Graph has maximum (0,3) and minimum (π, -1). Find the equation.

**Steps**:
- Amplitude \(a = \frac{3-(-1)}{2} = 2\).
- Vertical shift \(d = \frac{3+(-1)}{2} = 1\).
- From max to min is half period: \(\frac{T}{2} = \pi\) → \(T=2\pi\) → \(b=1\).
- Assume \(y = 2\sin(x+c)+1\). Plug (0,3): \(3=2\sin c+1\) → \(\sin c=1\) → \(c=\frac{\pi}{2}\).
- Equation: \(y = 2\sin(x+\frac{\pi}{2})+1 = 2\cos x+1\).

**Pitfall**: Decide whether to use sine or cosine; both work with different phase shifts.

---

## 10.3 Trigonometric Identities

### 10.3.1 Core Identities (given in formula sheet)
\[
\sin^2\theta + \cos^2\theta = 1
\]
\[
\sec^2\theta = 1 + \tan^2\theta,\qquad \csc^2\theta = 1 + \cot^2\theta
\]
\[
\tan\theta = \frac{\sin\theta}{\cos\theta},\quad \cot\theta = \frac{\cos\theta}{\sin\theta}
\]

---

### 10.3.2 Simplifying Expressions

**Example**: Simplify \(\frac{\sin x}{1+\cos x} + \frac{1+\cos x}{\sin x}\).

**Steps**:
1. Common denominator: \(\frac{\sin^2 x + (1+\cos x)^2}{\sin x(1+\cos x)}\)
2. Expand numerator: \(\sin^2 x + 1 + 2\cos x + \cos^2 x = (\sin^2 x+\cos^2 x) + 1 + 2\cos x = 2 + 2\cos x\)
3. Factor: \(\frac{2(1+\cos x)}{\sin x(1+\cos x)} = \frac{2}{\sin x} = 2\csc x\).

---

### 10.3.3 Proving Identities

**Steps**:
1. Start with the more complicated side.
2. Convert all functions to \(\sin\) and \(\cos\).
3. Use \(\sin^2+\cos^2=1\) and algebraic manipulation to reach the other side.

**Example**: Prove \(\tan x + \cot x = \sec x \csc x\).

**Proof**:
- Left: \(\frac{\sin x}{\cos x} + \frac{\cos x}{\sin x} = \frac{\sin^2 x + \cos^2 x}{\sin x \cos x} = \frac{1}{\sin x \cos x}\).
- Right: \(\frac{1}{\cos x} \cdot \frac{1}{\sin x} = \frac{1}{\sin x \cos x}\). Hence LHS = RHS.

---

## 10.4 Solving Trigonometric Equations

### 10.4.1 Basic Forms

#### (i) \(\sin x = a\)
**Steps**:
- Find principal value \(x_0 = \arcsin a\) (usually acute).
- In \([0,2\pi)\): solutions are \(x_0\) and \(\pi - x_0\).
- General: \(x = x_0 + 2k\pi\) or \(x = \pi - x_0 + 2k\pi\).
- If \(a<0\), find principal value for \(|a|\) and adjust signs using symmetry.

**Example**: \(\sin x = \frac12\), \(0\le x<2\pi\) → \(x = \frac{\pi}{6}, \frac{5\pi}{6}\).

#### (ii) \(\cos x = a\)
**Steps**:
- Principal value \(x_0 = \arccos a\) (in \([0,\pi]\)).
- In \([0,2\pi)\): solutions are \(x_0\) and \(2\pi - x_0\).
- General: \(x = \pm x_0 + 2k\pi\).

**Example**: \(\cos x = -\frac12\), \(0\le x<2\pi\) → \(x = \frac{2\pi}{3}, \frac{4\pi}{3}\).

#### (iii) \(\tan x = a\)
**Steps**:
- Principal value \(x_0 = \arctan a\) (in \((-\pi/2,\pi/2)\)).
- Period \(\pi\): all solutions \(x = x_0 + k\pi\).

**Example**: \(\tan x = \sqrt{3}\), \(0\le x<2\pi\) → \(x = \frac{\pi}{3}, \frac{4\pi}{3}\).

---

### 10.4.2 Reducible to Quadratic Form

**Steps**:
1. Let \(t = \sin x\) (or \(\cos x\), \(\tan x\)).
2. Solve quadratic \(at^2+bt+c=0\).
3. For each solution \(t\), solve \(\sin x = t\) (check \(t\) in \([-1,1]\) for sine/cosine).
4. Find all solutions in the given interval.

**Example**: \(2\sin^2 x + \sin x - 1 = 0\), \(0\le x<2\pi\).
- Let \(t=\sin x\): \(2t^2+t-1=0\) → \((2t-1)(t+1)=0\) → \(t=\frac12\) or \(t=-1\).
- \(\sin x = \frac12\) → \(x=\frac{\pi}{6}, \frac{5\pi}{6}\).
- \(\sin x = -1\) → \(x=\frac{3\pi}{2}\).
- Solutions: \(\frac{\pi}{6}, \frac{5\pi}{6}, \frac{3\pi}{2}\).

---

### 10.4.3 Using Identities to Convert to One Function

**Example**: \(2\sec^2 x + \tan x - 3 = 0\).
- Use \(\sec^2 x = 1+\tan^2 x\): \(2(1+\tan^2 x) + \tan x - 3 = 0\) → \(2\tan^2 x + \tan x - 1 = 0\).
- Let \(t=\tan x\): \(2t^2+t-1=0\) → \((2t-1)(t+1)=0\) → \(t=\frac12\) or \(t=-1\).
- \(\tan x = \frac12\) → \(x = \arctan\frac12 + k\pi\) (use calculator for decimal).
- \(\tan x = -1\) → \(x = \frac{3\pi}{4} + k\pi\).
- Then pick solutions in the required interval.

---

### 10.4.4 Graphical Method

**When to use**: Equations like \(\sin x = x/2\) or when asked to “use a graphical method”.

**Steps**:
1. Rewrite as \(f(x)=g(x)\).
2. Sketch \(y=f(x)\) and \(y=g(x)\) on the same axes.
3. Intersection points give solutions (approximate or count).
4. If exact values are not required, read approximate values from the graph.

**Example**: \(\sin x = \frac{x}{2}\) on \([-π, π]\). How many solutions?
- Sketch \(y=\sin x\) and the line \(y=x/2\).
- Intersection at \(x=0\) (since both 0). On the positive side, the line is below the sine curve for small \(x\), then crosses again near \(x≈1.9\). Negative side symmetric. Total 3 solutions.

**Pitfall**: Graphs must be accurate; mark key points (zeros, peaks, intercepts).

---

### 10.4.5 Using a Calculator (Paper 2)

**When**: No exact angle, calculator allowed.

**Steps**:
1. Isolate the trigonometric function (e.g., \(\sin x = 0.3\)).
2. Find the principal value using calculator:
   - \(\sin^{-1}(a)\) → value in \([-π/2, π/2]\)
   - \(\cos^{-1}(a)\) → value in \([0,π]\)
   - \(\tan^{-1}(a)\) → value in \((-π/2, π/2)\)
3. Use symmetry to find all solutions in the required interval.
4. Add multiples of the period as needed.

**Example**: \(\sin x = 0.3\), \(0\le x<2\pi\).
- Principal: \(x_1 = \sin^{-1}(0.3) \approx 0.3047\) (rad).
- Second solution: \(x_2 = \pi - 0.3047 \approx 2.8369\).
- Answers: \(x \approx 0.3047, 2.8369\).

**Pitfall**: Ensure calculator is in **radian mode** unless the problem uses degrees.

---

## 10.5 Common Problem Types & Solutions

| Type | Key Method |
|------|------------|
| **Angle–radian conversion** | Multiply/divide by \(\pi/180\) |
| **Arc length / sector area** | Use \(s=r\theta,\ A=\frac12 r^2\theta\) with radians |
| **Composite shapes** | Break into parts, compute separately |
| **Find trig values from one given** | Use \(\sin^2+\cos^2=1\) and quadrant signs |
| **Sketch trig graphs** | Determine amplitude, period, phase shift, vertical shift |
| **Solve trig equations** | 1. Basic: use reference angle and symmetry 2. Quadratic: substitute 3. Use identities to reduce to one function 4. Graphical/calculator methods |
| **Prove identities** | Start from complex side, convert to sine/cosine, use \(\sin^2+\cos^2=1\) |
| **Max/min of trig functions** | Use range of sine/cosine, or express in form \(R\sin(x+\phi)\) |

---

## 10.6 Common Pitfalls

| Pitfall | Correct Practice |
|---------|------------------|
| Using degrees in radian formulas | Convert to radians first |
| Solving \(\sin x = a\) with only one solution | Two solutions in \([0,2\pi)\) unless \(a=\pm1\) |
| Forgetting \(\tan x\) period is \(\pi\) | Add \(k\pi\), not \(2k\pi\) |
| Substitution quadratic: ignoring range of \(\sin x\) | Discard \(t\) outside \([-1,1]\) |
| Proving identities by moving terms prematurely | Keep side‑by‑side manipulation |
| Phase shift sign confusion | Solve \(bx+c=0\) to find shift direction |
| Calculator mode mismatch | Use radian mode unless problem explicitly uses degrees |
| Composite shape perimeter: double‑counting boundaries | Draw and label each edge |

---

## Key Formula Summary

| Item | Formula |
|------|---------|
| Radian definition | \(\theta = s/r\) |
| Arc length | \(s = r\theta\) |
| Sector area | \(A = \frac12 r^2\theta\) |
| Segment area | \(\frac12 r^2(\theta - \sin\theta)\) |
| Pythagorean identity | \(\sin^2\theta+\cos^2\theta=1\) |
| Derived identities | \(\sec^2\theta=1+\tan^2\theta,\ \csc^2\theta=1+\cot^2\theta\) |
| Period of sine/cosine | \(2\pi\) |
| Period of tangent | \(\pi\) |
| General sine/cosine | \(y=a\sin(bx+c)+d\): amplitude \(|a|\), period \(2\pi/|b|\), phase shift \(-c/b\), vertical shift \(d\) |
| General tangent | \(y=a\tan(bx+c)+d\): period \(\pi/|b|\), asymptotes \(bx+c=\frac{\pi}{2}+k\pi\) |
| Solutions for \(\sin x = a\) | \(x = \arcsin a + 2k\pi\) or \(x = \pi - \arcsin a + 2k\pi\) |
| Solutions for \(\cos x = a\) | \(x = \pm\arccos a + 2k\pi\) |
| Solutions for \(\tan x = a\) | \(x = \arctan a + k\pi\) |
