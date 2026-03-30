# Topic 6: Straight‑line Graphs

## 6.1 Length of a Segment and Midpoint

- **Length formula**: Given two points A(x1, y1) and B(x2, y2), the length of AB is sqrt[(x2−x1)² + (y2−y1)²].
- **Midpoint formula**: The midpoint M has coordinates ((x1+x2)/2, (y1+y2)/2).
- **Pitfall**: The order of points does not matter; take the positive square root.

---

## 6.2 Parallel and Perpendicular Lines

- **Parallel**: If both slopes exist, m1 = m2; a horizontal line (m=0) is parallel to another horizontal line.
- **Perpendicular**: If both slopes exist, m1·m2 = −1; special case: a horizontal line (m=0) and a vertical line (slope undefined) are perpendicular.
- **Geometric intuition**: Parallel → same direction; perpendicular → slopes multiply to −1 or one horizontal and one vertical.

### Finding the slope of two segments
For three points A, B, C with segments AB and BC having different slopes:

(a_y − b_y)/(a_x − b_x) = (b_y − c_y)/(b_x − c_x)  — used for collinearity.

---

## 6.3 Equation of a Straight Line

- **Common forms**  
  - Slope‑intercept: y = mx + c (m slope, c y‑intercept)  
  - Point‑slope: y − y1 = m(x − x1)  
  - Two‑point: first find m = (y2−y1)/(x2−x1), then use point‑slope form.  
  - General form: Ax + By + C = 0 (slope = −A/B, intercept = −C/B)
- **Steps**:  
  1. Determine what is given (point + slope, two points, slope and intercept, etc.).  
  2. Choose the appropriate form.  
  3. Convert to the required form (e.g., y = mx + c or Ax + By + C = 0).
- **Pitfall**: Vertical lines have no slope; their equation is x = a.

---

## 6.4 Area of Rectilinear Figures (Coordinate Geometry)

- **Area of a triangle (given three points)**:  
  For A(x1,y1), B(x2,y2), C(x3,y3),  
  S = ½·|x1(y2−y3) + x2(y3−y1) + x3(y1−y2)|.  
  (Determinant form also works.)
- **Steps**: Substitute coordinates, take absolute value, divide by 2.
- **Example**: A(1,2), B(4,5), C(6,1)  
  S = ½·|1·(5−1) + 4·(1−2) + 6·(2−5)| = ½·|4 −4 −18| = 9.
- **Pitfall**: Collinear points give area 0 (can be used to test collinearity).
- **Area of a polygon (shoelace formula)**:  
  For vertices listed in order, S = ½·| Σ (xi·y(i+1) − x(i+1)·yi) |, where (x(n+1),y(n+1)) = (x1,y1).

---

## 6.5 Converting a Non‑linear Equation to Linear Form

- **Common models**:  
  - y = k·xⁿ → take common log (lg): set Y = lg y, X = lg x → Y = n·X + lg k.  
  - y = k·bˣ → take lg: Y = lg y, X = x → Y = (lg b)·X + lg k.  
  - y = e^(px+q) → take natural log (ln): Y = ln y → Y = p·x + q.  
  - y = a/x + b → set X = 1/x, Y = y → Y = a·X + b.  
  - y = a·√x + b → set X = √x, Y = y → Y = a·X + b.
- **Steps**:  
  1. Identify the model and corresponding transformation.  
  2. Compute the new variables.  
  3. Plot (or compute) to get the slope and intercept of the line.  
  4. Back‑substitute to find the original parameters.
- **Pitfall**: Logarithms require positive data; the slope and intercept correspond to the parameters after transformation.

---

## 6.6 Converting from Linear Form back to a Non‑linear Equation

Given X, Y satisfy Y = m·X + c, with known relationships to original variables:

- Y = lg y, X = lg x → y = 10^c · x^m (power function)
- Y = lg y, X = x → y = 10^c · (10^m)^x (exponential function)

The fundamental difference between power and exponential models lies in the position of the variable x:

- **Power function y = k·xⁿ**: x is in the base → taking logs gives lg y = n·lg x + lg k → plot lg y vs lg x.
- **Exponential function y = k·bˣ**: x is in the exponent → taking logs gives lg y = x·lg b + lg k → plot lg y vs x.

If you mix them up, you won’t obtain a straight line.

- Y = ln y, X = x → y = e^c · e^(m·x) (exponential, base e)
- Y = y, X = 1/x → y = m/x + c (inverse proportion)
- Y = y, X = √x → y = m·√x + c (square‑root type)

**Note**: The slope m and intercept c are read from the straight line; when back‑substituting, pay attention to the base (10 or e) and domain.

---

## Supplement: Key Points for Non‑linear to Linear Transformations

### 1. Choose the correct logarithm base
- Models y = kxⁿ or y = kbˣ: use **common logarithm (lg)**, base 10.  
  \[
  \lg y = n \lg x + \lg k
  \]
- Model y = e^(px+q): use **natural logarithm (ln)**, base e.  
  \[
  \ln y = p x + q
  \]
> **Note**: If a problem uses “log” without a base, it usually means base 10; if the equation contains e, use ln.

### 2. Carefully recover parameters from intercept

| Original model | Transformation | Slope | Intercept | Back‑substitution |
|----------------|----------------|-------|-----------|-------------------|
| y = kxⁿ | Y = nX + lg k | n | lg k | k = 10^(intercept) |
| y = k bˣ | Y = (lg b)X + lg k | lg b | lg k | b = 10^(slope), k = 10^(intercept) |
| y = e^(px+q) | Y = p x + q | p | q | directly p, q |

> **Pitfall**: Using ln with y = kxⁿ is possible, but if the problem’s data table uses lg, you must stay consistent; otherwise the base when recovering k will be wrong.

### 3. Procedure for exam questions
These questions often have several parts:
1. Write expressions for the transformed variables Y and X.
2. Compute missing Y or X values in a table.
3. Plot the points and draw the best‑fit line.
4. Read the slope and intercept from the graph (keep sufficient precision, typically 0.01 or 0.1).
5. Find the original parameters.

> **Note**: When reading values from the graph, use two points on the drawn line (not the original data points) to calculate slope.

### 4. Data must be positive
Taking logarithms requires all data > 0. If a table contains zero or negative values, that model is not applicable – sometimes designed as a trap.

---

## 6.7 Finding Relationships from Data

- **Method**:  
  1. Plot the original data; observe the trend (linear, curved, exponential, power).  
  2. Guess a model (e.g., y = k·xⁿ, y = k·bˣ, y = a/x + b, etc.).  
  3. Transform accordingly to get new variables X, Y.  
  4. Plot the transformed points; check if they lie approximately on a straight line.  
  5. If they do, find slope m and intercept c using two points on the line (or regression).  
  6. Back‑transform to obtain the original constants.
- **Example**: Data suspected to follow y = k·xⁿ → compute X = lg x, Y = lg y; if the plot is approximately linear, the slope gives n, the intercept gives lg k.
- **Pitfall**: Measurement errors may cause points not to lie exactly on a line; draw a best‑fit line. Also, be careful with zero or negative values when taking logs.

**General procedure with a data set (x, y)**:  

1. **Guess the model** based on the shape of the scatter plot:  
   - Increasing faster and faster → try y = k bˣ or y = e^(px+q)  
   - Power‑law (e.g., parabola, inverse) → try y = k xⁿ  
   - Relationship with 1/x → try y = a/x + b  
   - Relationship with √x → try y = a√x + b  

2. **Compute new variables** for each candidate model, and check which gives a straight line.

3. **Find slope and intercept** of that line:  
   \[
   \text{slope} = \frac{Y_2 - Y_1}{X_2 - X_1}, \quad \text{intercept} = Y - \text{slope}\cdot X
   \]

4. **Recover original parameters** according to the transformation table.

**Example (short)**: Data:

| x | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| y | 2.5 | 6.3 | 15.8 | 39.7 |

Plotting lg y against x shows a straight line → model y = k bˣ.  
Slope ≈ 0.477 → b = 10^0.477 ≈ 3.0; intercept ≈ 0.398 → k = 10^0.398 ≈ 2.5.  
Thus y = 2.5·3ˣ.

---

# Topic 6.8: Vectors – Foundation and Geometric Applications (Plain Text)

## 1. Representation of Vectors

### 1.1 Two common forms
- Column vector: e.g., (3,4) written vertically.
- Unit vector combination: a i + b j, where i = (1,0), j = (0,1).

Both forms are acceptable; use the one required.

### 1.2 Directed line segment
\(\overrightarrow{AB}\) denotes the vector from A to B: coordinates (xB−xA, yB−yA) = OB − OA.  
Note: \(\overrightarrow{BA} = OA - OB\) (opposite direction).

---

## 2. Position Vectors and Unit Vectors

### 2.1 Position vector
The position vector of point P(x,y) is \(\overrightarrow{OP} = (x, y)\).  
For any two points, \(\overrightarrow{AB} = \overrightarrow{OB} - \overrightarrow{OA}\).

### 2.2 Unit vector
A unit vector in the direction of a is â = a / |a|, where |a| = sqrt(a₁² + a₂²).  
The opposite unit vector is −a / |a|.  
Example: a = (3,4), |a| = 5, unit vector = (3/5, 4/5).

---

## 3. Basic Vector Operations

### 3.1 Addition
Algebraic: (a,b) + (c,d) = (a+c, b+d)  
Geometric: triangle rule (head‑to‑tail) or parallelogram rule.

### 3.2 Subtraction
a − b = a + (−b)  
Geometric: from the tip of b to the tip of a (when both start at the same point).  
In coordinates: \(\overrightarrow{AB} = OB − OA\) is an example of subtraction.

### 3.3 Scalar multiplication
k·(a,b) = (k·a, k·b)  
- k > 0: same direction, length multiplied by |k|.  
- k < 0: opposite direction, length multiplied by |k|.  
- k = 0: zero vector.

### 3.4 Magnitude
|a| = sqrt(a² + b²)

### 3.5 Midpoint formula
If M is the midpoint of AB, then \(\overrightarrow{OM} = (\overrightarrow{OA} + \overrightarrow{OB})/2\)  
Coordinates: M((xA+xB)/2, (yA+yB)/2)

---

## 4. Parallelism, Collinearity, Perpendicularity

### 4.1 Parallel
a ∥ b iff a = k·b (k ≠ 0).  
In coordinates: a₁/b₁ = a₂/b₂ (provided denominators ≠ 0).

### 4.2 Collinear points
A, B, C are collinear iff \(\overrightarrow{AB} = λ·\overrightarrow{AC}\) (or AB ∥ BC). λ can be any non‑zero real number (including negative).  
Example: A(1,2), B(3,5), C(5,8): AB = (2,3), AC = (4,6) = 2·(2,3) → collinear.

### 4.3 Perpendicular (dot product)
In IGCSE 0606, perpendicularity is tested using the dot product:  
a·b = a₁b₁ + a₂b₂ = 0.  
Geometric meaning: |a||b| cos θ = 0 → θ = 90°.  
Example: a=(2,3), b=(3,−2): 2·3 + 3·(−2) = 0 → perpendicular.

---

## 5. Kinematics Applications (Velocity and Resultant)

### 5.1 Position vector for uniform motion
r(t) = r₀ + t·v, where r₀ is the initial position and v the velocity vector.

### 5.2 Relative velocity
Velocity of A relative to B: v_A/B = v_A − v_B.

### 5.3 Meeting condition
There exists a time t ≥ 0 such that r_A(t) = r_B(t) (both coordinates equal).  
Classic example: Boat A starts at (0,0) with velocity (2,3), boat B starts at (10,0) with velocity (1,4). Do they meet?  
r_A(t) = (2t, 3t), r_B(t) = (10+t, 4t).  
Setting 2t = 10+t gives t = 10; then y_A = 30, y_B = 40 → not equal → they do not meet.

### 5.4 Closest distance problem (advanced)
If they do not meet, find when they are closest.  
Let r_AB(t) = r_A(t) − r_B(t). The squared distance is a quadratic in t; find its minimum.

---

## 6. Vectors with Lines and Circles

### 6.1 Direction vector of a line
- For y = mx + c: a direction vector is (1, m).  
- For Ax + By + C = 0: a direction vector is (B, −A) (since it is perpendicular to the normal).

### 6.2 Normal vector of a line
The line Ax + By + C = 0 has a normal vector n = (A, B), perpendicular to the line.

### 6.3 Circles and tangents
- Centre C, point of tangency T: the radius CT is perpendicular to the tangent.  
- If the direction vector of the tangent is d, then CT·d = 0.  
Example: Circle x²+y²=25, point P(3,4) on the circle, centre O(0,0), radius vector (3,4). A perpendicular direction is (4,−3); the tangent passes through P with that direction.

---

## 7. Common Problem Types and Methods

| Type | Key Method |
|------|------------|
| Geometric proofs (parallelogram, collinearity) | Use vector equality, scalar multiples, midpoint formula. |
| Coordinate operations (vectors, magnitude, unit vectors, parameters) | Direct definitions, solve equations. |
| Kinematics (meeting, closest distance) | Set up position vector equations, solve for time, use quadratic minima. |
| Lines and circles (tangents, perpendicularity) | Use dot product = 0 for perpendicular conditions. |

---

## 8. Quick Reference – Common Pitfalls

| Pitfall | Correct Approach |
|---------|------------------|
| Writing \(\overrightarrow{AB}\) incorrectly | \(\overrightarrow{AB} = OB - OA\) (tip minus tail). |
| Collinearity ignoring negative λ | Parallel vectors can be in opposite directions. |
| Mixing up perpendicular and parallel conditions | Perpendicular → dot product = 0; parallel → scalar multiple. |
| Meeting condition using only one coordinate | Both coordinates must match at the same time t. |
| Forgetting to divide by magnitude for unit vector | â = a / |a|. |

---

# Topic 7: Coordinate Geometry of the Circle

---

## 7.1 Equation of a Circle

### 7.1.1 Standard form
Centre (a, b), radius r:
$$
(x - a)^2 + (y - b)^2 = r^2
$$

### 7.1.2 General form
$$
x^2 + y^2 + 2gx + 2fy + c = 0
$$
- Centre: \((-g, -f)\)
- Radius: \(r = \sqrt{g^2 + f^2 - c}\) (requires \(g^2 + f^2 - c > 0\))

> **Note**: If the general form is written as \(x^2 + y^2 + Dx + Ey + F = 0\), then centre = \((-D/2, -E/2)\), radius = \(\sqrt{(D/2)^2 + (E/2)^2 - F}\).

### 7.1.3 Completing the square
Convert general form to standard form by completing the square.

**Example**: \(x^2 + y^2 - 4x + 6y - 3 = 0\)
$$
(x^2 - 4x) + (y^2 + 6y) = 3
$$
$$
(x-2)^2 - 4 + (y+3)^2 - 9 = 3
$$
$$
(x-2)^2 + (y+3)^2 = 16
$$
Centre (2, -3), radius 4.

> **Pitfall**: Maintain balance on both sides when adding terms to complete the square.

---

## 7.2 Intersection of a Line and a Circle

### 7.2.1 Solving by substitution
Substitute the line equation (e.g., \(y = mx + c\)) into the circle equation, eliminate y, obtain a quadratic in x:
$$
Ax^2 + Bx + C = 0
$$
The discriminant \(\Delta = B^2 - 4AC\) determines the relationship:
- \(\Delta > 0\): two distinct intersections (secant)
- \(\Delta = 0\): one intersection (tangent)
- \(\Delta < 0\): no intersection (line misses the circle)

If the line is vertical (\(x = k\)), substitute into the circle to get a quadratic in y.

### 7.2.2 Tangent equations

#### (1) Given point of tangency \((x_0, y_0)\) on the circle
Method 1 (slope): radius is perpendicular to tangent, slope \(m = -\dfrac{x_0 - a}{y_0 - b}\) (centre (a,b)), then \(y - y_0 = m(x - x_0)\).

Method 2 (quick formula):
$$
(x_0 - a)(x - a) + (y_0 - b)(y - b) = r^2
$$
or equivalently
$$
(x_0 - a)(x - x_0) + (y_0 - b)(y - y_0) = 0
$$

**Example**: Circle \((x-2)^2 + (y+3)^2 = 16\), point (2,1):
$$
(2-2)(x-2) + (1+3)(y+3) = 16 \implies 4(y+3) = 16 \implies y = 1
$$

#### (2) Given slope k
Let the tangent be \(y = kx + c\), substitute into the circle, set \(\Delta = 0\) to solve for c (two parallel tangents).

#### (3) From an external point \(P(x_1, y_1)\)
Let the tangent have slope k, equation \(y - y_1 = k(x - x_1)\), substitute into the circle, set \(\Delta = 0\) to solve for k. Check the case of a vertical tangent (x = x₁) separately.

> **Pitfall**: If only one k is found, the other tangent is vertical.

---

## 7.3 Perpendicular from Centre to a Chord (Chord Properties)

### 7.3.1 Theorem
The perpendicular from the centre of a circle to a chord bisects the chord.  
If O is the centre, M is the midpoint of chord AB, then \(OM \perp AB\).

### 7.3.2 Chord length formula
Given radius r and the distance d from the centre to the chord (the perpendicular distance), the chord length is:
$$
\text{Chord length} = 2\sqrt{r^2 - d^2}
$$

### 7.3.3 Applications
- Given chord length and radius, find the distance from centre to chord.
- Used in problems involving chord lengths and midpoints.

---

## 7.4 Triangles and Angle Relationships in a Circle

### 7.4.1 Central angle and inscribed angle
- **Central angle**: vertex at the centre, measure equals the measure of its intercepted arc.
- **Inscribed angle**: vertex on the circle, measure equals half the measure of its intercepted arc.

**Theorem**: Inscribed angles that intercept the same arc are equal; an inscribed angle is half the corresponding central angle.

### 7.4.2 Angle in a semicircle
If AB is a diameter and C is any point on the circle (C ≠ A, B), then \(\angle ACB = 90^\circ\).

**Application**: In coordinate geometry, if three points are given, we can use the right‑angle property to find the centre or radius.

### 7.4.3 Cyclic triangle
- The circumcentre of a triangle is the intersection of the perpendicular bisectors of its sides; it is the centre of the circumscribed circle.
- The circumcentre is equidistant from the three vertices (all equal to the radius).

**Common uses in coordinate geometry**:
- Find the circle through three given points → set up general form and solve, or find two perpendicular bisectors to locate the centre.
- Given two points on a circle and an angle condition, apply the inscribed angle theorem.

### 7.4.4 Cyclic quadrilateral (supplementary)
- Opposite angles are supplementary: \(\angle A + \angle C = 180^\circ\), \(\angle B + \angle D = 180^\circ\).
- An exterior angle equals the interior opposite angle.

### 7.4.5 Example

**Problem**: Circle \(x^2 + y^2 = 25\), points A(3,4), B(−4,3) on the circle. Find \(\angle AOB\) and \(\angle ACB\) (C another point on the circle).

**Solution**:
- Centre O(0,0). \(\overrightarrow{OA} = (3,4)\), \(\overrightarrow{OB} = (-4,3)\). Dot product: \(3×(-4)+4×3 = -12+12=0\), so \(OA \perp OB\). Hence \(\angle AOB = 90^\circ\).
- By the inscribed angle theorem, \(\angle ACB = \frac12 \angle AOB = 45^\circ\) (if C lies on the major arc AB) or \(135^\circ\) (if on the minor arc AB).

---

## 7.5 Position of Two Circles

Let the distance between centres be d, radii \(r_1, r_2\) (assume \(r_1 \ge r_2\)):

| Condition | Position |
|-----------|----------|
| \(d > r_1 + r_2\) | Separate (no intersection) |
| \(d = r_1 + r_2\) | Externally tangent |
| \(|r_1 - r_2| < d < r_1 + r_2\) | Intersect at two points |
| \(d = |r_1 - r_2|\) | Internally tangent |
| \(d < |r_1 - r_2|\) | One circle lies inside the other (no intersection) |

---

## 7.6 Equation of the Common Chord

If two circles intersect, subtract one equation from the other (eliminating \(x^2\) and \(y^2\) terms) to obtain the linear equation of the common chord.

---

## 7.7 Key Formulas

| Item | Formula |
|------|---------|
| Slope | \(m = \dfrac{y_2 - y_1}{x_2 - x_1}\) |
| Midpoint | \(\left( \dfrac{x_1+x_2}{2}, \dfrac{y_1+y_2}{2} \right)\) |
| Distance between two points | \(\sqrt{(x_2-x_1)^2 + (y_2-y_1)^2}\) |
| Distance from point to line | \(d = \dfrac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}\) |
| Triangle area (coordinate) | \(S = \dfrac12 \left| x_1(y_2-y_3) + x_2(y_3-y_1) + x_3(y_1-y_2) \right|\) |
| Circle standard form | \((x-a)^2 + (y-b)^2 = r^2\) |
| Centre from general form | \((-g, -f)\) |
| Radius from general form | \(\sqrt{g^2 + f^2 - c}\) |
| Chord length (perpendicular distance) | \(2\sqrt{r^2 - d^2}\) (d = distance from centre to chord) |
| Tangent length from external point | \(\sqrt{OP^2 - r^2}\) |
| Distance between centres | \(\sqrt{(a_1-a_2)^2 + (b_1-b_2)^2}\) |

---

## 7.8 Common Problem Types and Methods

| Type | Method Summary |
|------|----------------|
| **Find circle equation** (centre, radius) | Write standard form directly. |
| **Find circle equation** (through three points) | Use general form, substitute points to solve for coefficients; or find two perpendicular bisectors to get centre. |
| **Line–circle position** | Solve simultaneous equations → discriminant; or compare centre‑to‑line distance with radius. |
| **Tangent at a point on circle** | Use perpendicular radius (slope method) or the quick formula. |
| **Tangent of given slope** | Let \(y = mx + c\), substitute, set \(\Delta = 0\), solve for c. |
| **Tangents from an external point** | Let \(y - y_1 = k(x - x_1)\), substitute, set \(\Delta = 0\) for k; check vertical case. |
| **Chord length** | Use perpendicular distance from centre to chord and formula \(2\sqrt{r^2-d^2}\). |
| **Two‑circle position** | Compare centre distance with sum/difference of radii. |
| **Common chord** | Subtract circle equations. |

---

## 7.9 Common Mistakes

| Mistake | Correct Approach |
|---------|------------------|
| Sign of centre in general form | Centre is \((-g, -f)\), not \((g, f)\). |
| Forgetting to add the same value on both sides when completing the square | Keep the equation balanced. |
| Omitting the vertical tangent when using slope method from external point | Check the line \(x = x_1\) separately. |
| Using chord length formula as \(2\sqrt{r^2 + d^2}\) | Correct is \(2\sqrt{r^2 - d^2}\). |
| Forgetting the internally tangent case | Both \(d = r_1+r_2\) and \(d = |r_1-r_2|\) give tangency. |
| Subtracting circle equations without first ensuring both are in general form | Write both as \(x^2+y^2+...=0\) before subtracting. |

---

## Supplement: Additional Circle Properties (Often Omitted but Useful)

### Perpendicular from centre to a chord (already covered)
- Proved using vectors: \(\overrightarrow{OM} = (\overrightarrow{OA}+\overrightarrow{OB})/2\), \(\overrightarrow{AB} = \overrightarrow{OB}-\overrightarrow{OA}\), then \(\overrightarrow{OM}\cdot\overrightarrow{AB}=0\).

### Position of two circles (already covered)

### Common chord (already covered)

---

## Summary: Key Formula Table

- Slope: \(m = (y_2-y_1)/(x_2-x_1)\)
- Midpoint: \(((x_1+x_2)/2, (y_1+y_2)/2)\)
- Distance: \(\sqrt{(x_2-x_1)^2 + (y_2-y_1)^2}\)
- Triangle area (coordinates): \(\frac12 |x_1(y_2-y_3)+x_2(y_3-y_1)+x_3(y_1-y_2)|\)
- Circle standard: \((x-a)^2+(y-b)^2=r^2\)
- Centre from general form: \((-g,-f)\)
- Radius from general form: \(\sqrt{g^2+f^2-c}\)
- Line‑circle relationship: substitute → discriminant
- Chord length: \(2\sqrt{r^2-d^2}\)
