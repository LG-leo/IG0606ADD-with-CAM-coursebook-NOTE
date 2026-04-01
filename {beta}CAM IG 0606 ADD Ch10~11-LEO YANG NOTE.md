# U10 Permutations and Combinations

---

## 10.1 Basic Concepts and Notation

### 10.1.1 Factorial
\[
n! = n \times (n-1) \times \cdots \times 2 \times 1, \quad 0! = 1
\]

### 10.1.2 Permutations
The number of ways to arrange \(r\) distinct items chosen from \(n\) distinct items (order matters) is:
\[
^nP_r = \frac{n!}{(n-r)!}
\]

**When to use**: Order is important (e.g., lining up, passwords, ranking).

### 10.1.3 Combinations
The number of ways to choose \(r\) items from \(n\) distinct items (order does not matter) is:
\[
^nC_r = \binom{n}{r} = \frac{n!}{r!\,(n-r)!}
\]

**When to use**: Order is irrelevant (e.g., selecting a committee, choosing members, lottery).

---

## 10.2 Types of Problems and Step‑by‑Step Methods

### 10.2.1 Direct Substitution

**Steps**:
1. Decide whether the problem is about permutations or combinations.
2. Identify \(n\) and \(r\).
3. Substitute into the formula and simplify.

**Example**: In how many ways can 3 people be chosen from 8 to form a committee?
- Combination: \(\binom{8}{3} = \frac{8\times7\times6}{3\times2\times1} = 56\).

**Example**: In how many ways can 3 people be selected from 8 to be president, secretary and treasurer?
- Permutation: \(^8P_3 = 8\times7\times6 = 336\).

---

### 10.2.2 Permutations with Restrictions

Common restrictions: certain items must be together, must not be together, fixed positions, etc.

#### (1) Items that must be together (Bundling method)
**Steps**:
1. Treat the items that must be together as a single block.
2. Arrange the blocks together with the remaining items.
3. Multiply by the number of ways to arrange the items inside the block.

**Example**: 5 people stand in a row. If A and B must stand next to each other, how many arrangements?
- Treat A and B as one block → 4 objects → \(4!\) arrangements.
- Inside the block, A and B can be ordered in \(2!\) ways.
- Total: \(4! \times 2! = 48\).

#### (2) Items that must not be together (Gap method)
**Steps**:
1. Arrange the other items first.
2. Insert the restricted items into the gaps (including ends) created by those arrangements.

**Example**: 5 people stand in a row. If A and B must not stand next to each other, how many arrangements?
- First arrange the other 3 people: \(3! = 6\) ways, creating 4 gaps (including ends).
- Choose 2 gaps out of 4 and order A and B: \(^4P_2 = 4\times3 = 12\).
- Total: \(6\times12 = 72\). Alternatively, total arrangements minus arrangements with them together: \(5! - 48 = 120-48=72\).

#### (3) Fixed positions
**Steps**: Place the fixed items first, then arrange the rest.

**Example**: 5 people stand in a row. If A must be first, how many arrangements?
- A fixed, arrange the other 4: \(4! = 24\).

---

### 10.2.3 Combinations with Restrictions

Common restrictions: must include certain members, must exclude certain members, grouping, etc.

#### (1) “At least” / “At most” problems
**Steps**: Break into cases (addition principle) or use complement (total minus undesirable).

**Example**: From 10 people (4 women, 6 men), choose 5. How many ways if at least 2 women are chosen?
- Cases:
  - 2 women, 3 men: \(\binom{4}{2}\binom{6}{3}\)
  - 3 women, 2 men: \(\binom{4}{3}\binom{6}{2}\)
  - 4 women, 1 man: \(\binom{4}{4}\binom{6}{1}\)
  Sum them.
- Or complement: total ways minus ways with 0 or 1 woman:
  \[
  \binom{10}{5} - \binom{4}{0}\binom{6}{5} - \binom{4}{1}\binom{6}{4}
  \]

#### (2) Grouping and distributing
**Steps**: When dividing into unlabeled groups of equal size, divide by the factorial of the number of groups to avoid overcounting. Then, if the groups are to be assigned to different tasks, multiply by the number of ways to assign them.

**Example**: Split 6 people into 3 pairs. How many ways?
- Number of ways to choose pairs: \(\frac{\binom{6}{2}\binom{4}{2}\binom{2}{2}}{3!} = 15\).
- If the three pairs are then assigned to three different tasks, multiply by \(3!\).

---

## 10.3 Common Mistakes

| Pitfall | Correct Approach |
|---------|------------------|
| Mixing up permutations and combinations | Ask: Does order matter? |
| Forgetting internal arrangements in bundling | Multiply by the factorial of the number of items inside the block. |
| Using wrong number of gaps for insertion | After arranging the other items, count all gaps (including ends). |
| Missing cases in “at least/at most” problems | Use casework or complement; ensure all possibilities are covered. |
| Overcounting unlabeled equal‑size groups | Divide by the factorial of the number of groups. |
| Misunderstanding \(0!\) | \(0! = 1\). |

---

## 10.4 Key Formulas

| Concept | Formula |
|---------|---------|
| Factorial | \(n! = n(n-1)\cdots1\), \(0! = 1\) |
| Permutations | \(^nP_r = \frac{n!}{(n-r)!}\) |
| Combinations | \(^nC_r = \frac{n!}{r!(n-r)!}\) |
| Bundling method | Treat required items as one object, then multiply by internal arrangements. |
| Gap method | Arrange others, then insert restricted items into gaps. |
| Complement principle | Total − undesirable = desirable. |

---

# U11 Series

---

## 11.1 Binomial Theorem

### 11.1.1 Theorem
\[
(a+b)^n = \sum_{r=0}^{n} \binom{n}{r} a^{n-r} b^r
\]
where \(\binom{n}{r}\) are the binomial coefficients. The formula is given in the examination paper.

### 11.1.2 Finding a Specific Term

**Steps**:
1. Write the general term: \(T_{r+1} = \binom{n}{r} a^{n-r} b^r\).
2. Set up an equation for the exponent of \(x\) (or for the constant term) to find \(r\).
3. Substitute \(r\) back and compute the coefficient.

**Example**: Find the constant term in \((2x - \frac{1}{x})^{10}\).
- General term: \(T_{r+1} = \binom{10}{r} (2x)^{10-r} (-\frac{1}{x})^r = \binom{10}{r} 2^{10-r} (-1)^r x^{10-2r}\).
- Set exponent \(10-2r = 0\) → \(r = 5\).
- Constant term: \(\binom{10}{5} 2^{5} (-1)^5 = -252 \times 32 = -8064\).

---

## 11.2 Arithmetic Progression (AP)

### 11.2.1 Basic Formulas
- First term \(a\), common difference \(d\).
- \(n\)th term: \(u_n = a + (n-1)d\).
- Sum of first \(n\) terms: \(S_n = \frac{n}{2}(a + u_n) = \frac{n}{2}[2a + (n-1)d]\).

These formulas are given in the examination paper.

### 11.2.2 Typical Problems

#### (1) Given terms, find \(a\) and \(d\)
**Steps**: Form equations using \(u_n = a + (n-1)d\) and solve.

**Example**: In an AP, \(u_3 = 10\) and \(u_7 = 22\). Find \(a\), \(d\) and \(S_{10}\).
- \(a + 2d = 10\), \(a + 6d = 22\) → subtract: \(4d = 12\) → \(d = 3\), \(a = 4\).
- \(S_{10} = \frac{10}{2}[2\times4 + 9\times3] = 5\times(8+27)=175\).

#### (2) Given \(S_n\), find \(u_n\) or other terms
**Example**: If \(S_n = 3n^2 + 2n\), find \(u_n\).
- \(u_n = S_n - S_{n-1} = (3n^2+2n) - [3(n-1)^2+2(n-1)] = 6n-1\).
- Check \(u_1 = S_1 = 5\) → \(6\cdot1-1 = 5\) correct.

---

## 11.3 Geometric Progression (GP)

### 11.3.1 Basic Formulas
- First term \(a\), common ratio \(r\).
- \(n\)th term: \(u_n = a r^{n-1}\).
- Sum of first \(n\) terms: \(S_n = \frac{a(1-r^n)}{1-r}\) for \(r \neq 1\).
- Sum to infinity (convergent series): \(S_\infty = \frac{a}{1-r}\) for \(|r| < 1\).

These formulas are given in the examination paper.

### 11.3.2 Typical Problems

#### (1) Given terms, find \(a\) and \(r\)
**Example**: In a GP, \(u_2 = 6\), \(u_5 = 48\). Find \(a\), \(r\) and \(S_4\).
- \(a r = 6\), \(a r^4 = 48\) → divide: \(r^3 = 8\) → \(r = 2\), \(a = 3\).
- \(S_4 = \frac{3(1-2^4)}{1-2} = 3\times15 = 45\).

#### (2) Sum to infinity
**Example**: GP with \(a = 4\), \(r = 0.5\): \(S_\infty = \frac{4}{1-0.5} = 8\).

#### (3) Convergence condition
- A GP has an infinite sum only if \(|r| < 1\); otherwise it diverges.

---

## 11.4 Mixed AP/GP Problems

Sometimes numbers are given in AP or GP, and we need to find them.

**Example**: Three numbers are in AP; their sum is 12 and product is 48. Find the numbers.
- Let the numbers be \(a-d, a, a+d\).
- Sum: \(3a = 12\) → \(a = 4\).
- Product: \((4-d)\cdot4\cdot(4+d)=48\) → \(16 - d^2 = 12\) → \(d^2 = 4\) → \(d = \pm 2\).
- Numbers: 2, 4, 6 or 6, 4, 2.

---

## 11.5 Common Mistakes

| Pitfall | Correct Approach |
|---------|------------------|
| Exponent error in binomial term | Ensure the sum of exponents of \(a\) and \(b\) equals \(n\). |
| Confusing AP and GP formulas | AP uses addition (common difference), GP uses multiplication (common ratio). |
| Using infinite sum formula without checking | Only valid when \(|r| < 1\). |
| Applying sum formula to \(r=1\) | For \(r=1\), the sum is \(na\). |
| Sign error in GP sum denominator | Denominator is \(1-r\), not \(r-1\). |
| In mixed AP/GP, forgetting the possibility of two solutions | Often both positive and negative differences/ratios exist. |

---

## Key Formula Summary

| Topic | Formula |
|-------|---------|
| Binomial theorem | \((a+b)^n = \sum_{r=0}^n \binom{n}{r} a^{n-r} b^r\) |
| Binomial coefficient | \(\binom{n}{r} = \frac{n!}{r!(n-r)!}\) |
| AP nth term | \(u_n = a + (n-1)d\) |
| AP sum | \(S_n = \frac{n}{2}(2a+(n-1)d)\) |
| GP nth term | \(u_n = a r^{n-1}\) |
| GP sum | \(S_n = \frac{a(1-r^n)}{1-r}\) (\(r\neq1\)) |
| Infinite GP sum | \(S_\infty = \frac{a}{1-r}\) (\(|r|<1\)) |

---
