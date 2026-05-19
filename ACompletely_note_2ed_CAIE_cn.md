# IGCSE 0606 附加数学综合笔记第二版本

本笔记严格按照 **剑桥 IGCSE 附加数学（0606）2028–2030 考纲** 编写。附加数学课程位于 IGCSE 普通数学之上，旨在拓展代数、函数、几何、三角与微积分的深度，为 AS/A Level 数学打下坚实基础。

每一章的编排遵循"概念定义 → 公式推导 → 典型例题"的结构。例题选自历年真题风格，难度对标考试要求。
// 里面部分题型是有真题。引用源https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-mathematics-additional-0606/past-papers/

> **说明**：考卷的公式列表中会给出部分公式（如等差/等比数列的求和公式、二项式展开公式），但本笔记仍完整推导，以帮助理解而非机械记忆。考试中，**理解何时使用哪个公式**比背公式更重要。
---
> 本笔记基于剑桥 IGCSE 附加数学（0606）2025-2027 考纲编写，按照认知顺序排列，涵盖所有主题。包含推导过程、典型例题和常见易错点。适合自学。
- 这份笔记由 LG-leo 整理和维护。如果你觉得这份笔记对你有帮助，欢迎在 GitHub 上关注我或给我一个 ⭐，这能帮助我持续产出更多免费的学习资源。
- 我的其他课程笔记：https://github.com/LG-leo?tab=repositories

- This note is maintained by LG-leo. If you find it helpful, feel free to follow me or leave a ⭐ on GitHub. It helps me keep producing more free study resources. Check out my other notes: https://github.com/LG-leo?tab=repositories
---
---

## 目录

- [第 1 章：数列、排列、组合与二项式定理](#第-1-章数列排列组合与二项式定理)
- [第 2 章：向量与变化率](#第-2-章向量与变化率)
- [第 3 章：二次函数（含多项式因式）](#第-3-章二次函数含多项式因式)
- [第 4 章：函数（线性、三次、指数、对数）](#第-4-章函数线性三次指数对数)
- [第 5 章：微分（导数）](#第-5-章微分导数)
- [第 6 章：方程与不等式（图形法）](#第-6-章方程与不等式图形法)
- [第 7 章：积分（不定积分与定积分）](#第-7-章积分不定积分与定积分)
- [第 8 章：三角学（含弧度法）](#第-8-章三角学含弧度法)
- [第 9 章：几何（直线与圆）](#第-9-章几何直线与圆)
- [第 10 章：综合应用](#第-10-章综合应用)

---

# 第 1 章：数列、排列、组合与二项式定理

本章将三个看似不同但内核相通的主题放在一起。**数列**训练你发现规律和求和的能力；**排列与组合**训练你系统化计数的逻辑；**二项式定理**则是排列组合在代数展开中的直接应用。

---

## 考纲对照表（Syllabus Mapping）

| 考纲编号 | 英文原文（Syllabus 2028–2030） | 中文说明 | 覆盖章节 |
|:-------:|------|---------|:-------:|
| **11.1** | *Recognise the difference between permutations and combinations and know when each should be used.* | 识别排列与组合的区别，知道何时使用哪个 | §1.2.4 |
| **11.2** | *Know and use the notation $n!$ and the expressions for permutations and combinations of $n$ items taken $r$ at a time. Includes $0! = 1$.* | 掌握 $n!$、$^nP_r$、$^nC_r$ 的记号与表达式 | §1.2.2, §1.2.3 |
| **11.3** | *Solve problems on arrangement and selection using permutations or combinations. Problems will be either in an everyday context or based on an algebraic problem. Problems involving: repetition of objects; objects arranged in a circle; both permutations and combinations, are **not** included.* | 用排列或组合解决排列与选择问题（日常生活或代数背景）。不考重复元素、圆排列、排列组合混合。 | §1.2.5 |
| **12.1** | *Use the binomial theorem for expansion of $(a+b)^n$ for positive integer $n$. Includes simplification of coefficients.* | 使用二项式定理展开 $(a+b)^n$（$n$ 为正整数），包含系数的化简 | §1.3.1 |
| **12.2** | *Use the general term $\displaystyle\binom{n}{r}a^{n-r}b^r$, $0 \le r \le n$. For example: Find the term independent of $x$ in the expansion of $\left(x^2 + \frac{1}{x}\right)^{\!10}$. Knowledge of the greatest term and properties of the coefficients is **not** required.* | 使用通项公式求特定项（如常数项）。不考最大项和系数性质。 | §1.3.2, §1.3.3 |
| **12.3** | *Recognise arithmetic and geometric progressions and understand the difference between them.* | 识别等差数列与等比数列，理解它们之间的区别 | §1.1.4 |
| **12.4** | *Use the formulas for the $n$th term and for the sum of the first $n$ terms to solve problems involving arithmetic or geometric progressions. Problems may be in context.* | 使用第 $n$ 项和前 $n$ 项和公式解决等差/等比数列问题（可能含实际情境） | §1.1.2, §1.1.3 |
| **12.5** | *Use the condition for the convergence of a geometric progression, and the formula for the sum to infinity of a convergent geometric progression. Includes explaining why a particular geometric progression has or does not have a sum to infinity.* | 使用等比数列的收敛条件及无穷和公式，**包含解释为什么某个等比级数有/无无穷和** | §1.1.3 |

---

## 1.1 数列（等差与等比）

数列是按顺序排列的一列数。附加数学中重点考察两种最基本的数列：**等差数列**（相邻两项的差固定）和**等比数列**（相邻两项的比固定）。

### 1.1.1 求和符号 $\sum$

在深入讨论数列之前，我们需要掌握求和符号 $\sum$（希腊字母 Sigma）。它表示将一系列数相加：

$$
\sum_{k=1}^{n} a_k = a_1 + a_2 + a_3 + \cdots + a_n
$$

求和运算满足三条基本法则：

**法则 1——常数因子提取**：

$$
\sum_{k=1}^{n} (c \cdot a_k) = c \cdot \sum_{k=1}^{n} a_k
$$

**法则 2——和的拆分**：

$$
\sum_{k=1}^{n} (a_k \pm b_k) = \sum_{k=1}^{n} a_k \pm \sum_{k=1}^{n} b_k
$$

**法则 3——常数的和**：

$$
\sum_{k=1}^{n} c = n c
$$

**示例**：计算 $\displaystyle\sum_{k=1}^{5} (3k - 2)$。

$$
\sum_{k=1}^{5} (3k - 2) = 3\sum_{k=1}^{5} k - \sum_{k=1}^{5} 2 = 3 \times (1+2+3+4+5) - 5 \times 2 = 3 \times 15 - 10 = 45 - 10 = 35
$$

---

### 1.1.2 等差数列（Arithmetic Progression）

#### 定义

一个数列如果从第二项起，每一项与它的前一项的差等于**同一个常数**，则称为**等差数列**。这个常数叫做**公差**，记作 $d$：

$$
a_{n+1} - a_n = d \quad (\text{对所有 } n \ge 1\text{ 成立})
$$

**示例**：$5, 9, 13, 17, 21$ 是等差数列，$d=4$，$a=5$。

#### 第 $n$ 项公式（推导）

设首项 $a_1 = a$，则：

$$
\begin{aligned}
a_2 &= a + d \\
a_3 &= a_2 + d = a + 2d \\
a_4 &= a_3 + d = a + 3d
\end{aligned}
$$

规律：第 $n$ 项是在首项的基础上加了 $(n-1)$ 次公差。

$$
\boxed{a_n = a + (n-1)d}
$$

**验证**：$n=1$ 时 $a_1 = a$；$n=2$ 时 $a_2 = a + d$。正确。

#### 前 $n$ 项和公式（推导——倒序相加法）

$$
\begin{aligned}
S_n &= a + (a+d) + (a+2d) + \cdots + [a+(n-1)d] \\
S_n &= [a+(n-1)d] + [a+(n-2)d] + \cdots + a
\end{aligned}
$$

两式相加，每一对的和均为 $2a + (n-1)d$，共 $n$ 对：

$$
2S_n = n[2a + (n-1)d]
$$

$$
\boxed{S_n = \frac{n}{2}[2a + (n-1)d]}
$$

若末项 $l = a_n = a + (n-1)d$，则：

$$
\boxed{S_n = \frac{n}{2}(a + l)}
$$

#### 例题

**例题 1**：首项 $7$，公差 $3$，求第 $15$ 项。

$$
a_{15} = 7 + 14 \times 3 = 7 + 42 = 49
$$

---

**例题 2**：首项 $2$，公差 $5$，前 $n$ 项和 $156$，求 $n$。

$$
\frac{n}{2}[4 + (n-1) \times 5] = 156 \quad\Rightarrow\quad \frac{n}{2}(5n - 1) = 156
$$

$$
5n^2 - n - 312 = 0 \quad\Rightarrow\quad n = \frac{1 \pm \sqrt{1 + 6240}}{10} = \frac{1 \pm 79}{10}
$$

$n$ 为正整数，$n = \frac{80}{10} = 8$。

---

**例题 3**（实际情境）：第一年存 $500$ 元，之后每年多存 $50$ 元。$10$ 年共存多少钱？

$$
S_{10} = \frac{10}{2}[2 \times 500 + 9 \times 50] = 5 \times (1000 + 450) = 7250
$$

答：$7250$ 元。

---

### 1.1.3 等比数列（Geometric Progression）

#### 定义

一个数列如果从第二项起，每一项与它的前一项的比值等于**同一个常数**，则称为**等比数列**。这个常数叫做**公比**，记作 $r$：

$$
\frac{a_{n+1}}{a_n} = r \quad (\text{对所有 } n \ge 1\text{ 成立})
$$

**示例**：$2, 6, 18, 54, 162$ 是等比数列，$r=3$，$a=2$。

#### 第 $n$ 项公式

$$
\begin{aligned}
a_2 &= a r \\
a_3 &= a_2 \cdot r = a r^2 \\
a_4 &= a_3 \cdot r = a r^3
\end{aligned}
$$

$$
\boxed{a_n = a r^{\,n-1}}
$$

#### 前 $n$ 项和公式（推导——错位相减法）

$$
S_n = a + a r + a r^2 + \cdots + a r^{\,n-1}
$$

$$
r S_n = a r + a r^2 + a r^3 + \cdots + a r^{\,n}
$$

相减：

$$
S_n - r S_n = a - a r^{\,n}
$$

$$
S_n(1 - r) = a(1 - r^{\,n})
$$

若 $r = 1$：$S_n = n a$。

若 $r \neq 1$：

$$
\boxed{S_n = a \cdot \frac{1 - r^{\,n}}{1 - r}} \quad \text{或等价地} \quad \boxed{S_n = a \cdot \frac{r^{\,n} - 1}{r - 1}}
$$

#### 无穷等比级数的收敛条件与和（**考纲 12.5 重点**）

$$
S_\infty = \lim_{n \to \infty} S_n = \lim_{n \to \infty} a \cdot \frac{1 - r^{\,n}}{1 - r}
$$

$r^{\,n}$ 在 $n \to \infty$ 时的行为决定了级数是否收敛：

| $r$ 的取值范围 | $n \to \infty$ 时 $r^{\,n}$ 的行为 | 级数是否收敛 | 无穷和 |
|:-------------:|----------------------------------|:-----------:|:------:|
| $\|r\| < 1$ | $r^{\,n} \to 0$ | ✅ **收敛** | $\displaystyle S_\infty = \frac{a}{1-r}$ |
| $\|r\| > 1$ | $\|r^{\,n}\| \to \infty$ | ❌ **发散** | 无有限和 |
| $r = 1$ | $r^{\,n} = 1$（恒定） | ❌ **发散** | $S_n = n a \to \infty$ |
| $r = -1$ | 在 $1$ 和 $-1$ 之间振荡 | ❌ **发散** | 和不确定 |

因此，**等比级数收敛的充要条件是 $|r| < 1$**。

考试中如果被要求"解释为什么某个等比级数有/没有无穷和"，你需要说明：当 $|r| < 1$ 时，$n \to \infty$ 使 $r^{\,n} \to 0$，因此 $S_n \to \dfrac{a}{1-r}$；当 $|r| \ge 1$ 时，$r^{\,n}$ 不趋近于 $0$，$S_n$ 不趋近于有限值。

#### 例题

**例题 1**：首项 $3$，公比 $2$，求第 $6$ 项。

$$
a_6 = 3 \times 2^5 = 3 \times 32 = 96
$$

---

**例题 2**（收敛判断 + 无穷和）：$12 + 6 + 3 + \dfrac{3}{2} + \cdots$

首项 $a = 12$，公比 $r = \dfrac{6}{12} = \dfrac{1}{2}$。

因为 $|r| = \dfrac{1}{2} < 1$，当 $n \to \infty$ 时 $\left(\dfrac{1}{2}\right)^{\!n} \to 0$，所以级数收敛。

$$
S_\infty = \frac{12}{1 - \frac{1}{2}} = \frac{12}{\frac{1}{2}} = 24
$$

---

**例题 3**（已知 $S_\infty$ 求 $r$）：无穷等比级数收敛，和为 $8$，首项为 $4$，求公比 $r$。

$$
8 = \frac{4}{1 - r} \quad\Rightarrow\quad 8(1 - r) = 4 \quad\Rightarrow\quad 1 - r = \frac{1}{2} \quad\Rightarrow\quad r = \frac{1}{2}
$$

验证：$|r| = \dfrac{1}{2} < 1$，满足收敛条件。

---

### 1.1.4 对照：等差数列 vs 等比数列（**考纲 12.3 重点**）

| 特征 | 等差数列 (AP) | 等比数列 (GP) |
|:----|:-------------|:-------------|
| **定义性质** | $a_{n+1} - a_n = d$（差恒定） | $\dfrac{a_{n+1}}{a_n} = r$（比恒定） |
| **检查方法** | 相邻项相减，看是否恒等 | 相邻项相除，看是否恒等 |
| **第 $n$ 项** | $a_n = a + (n-1)d$ | $a_n = a r^{\,n-1}$ |
| **前 $n$ 项和** | $S_n = \dfrac{n}{2}[2a + (n-1)d]$ | $S_n = a\dfrac{1-r^n}{1-r}$（$r \neq 1$） |
| **增长模式** | **线性增长**（每次加固定值） | **指数增长/衰减**（每次乘固定值） |
| **无穷和** | 不存在（除 $d=0$ 常数数列） | $|r| < 1$ 时收敛于 $\dfrac{a}{1-r}$ |

**判断练习**：

1. $5, 8, 11, 14, 17, \ldots$ → 差恒为 $3$ → **AP** ✓
2. $5, 10, 20, 40, 80, \ldots$ → 比恒为 $2$ → **GP** ✓
3. $1, 4, 9, 16, 25, \ldots$ → 差为 $3,5,7,9$（不恒定），比为 $4, 2.25, 1.78,\ldots$（不恒定）→ **两者都不是** ✗
4. $100, 50, 25, 12.5, \ldots$ → 比恒为 $\dfrac{1}{2}$ → **GP**（收敛）✓

---

## 1.2 排列与组合

排列与组合回答同一个基本问题："有多少种不同的方式？"二者的核心区别在于 **顺序是否重要**。

### 1.2.1 乘法原理

如果一项任务可以分解为 $k$ 个依次进行的步骤，第 $i$ 步有 $m_i$ 种方法，则总方法数为：

$$
\boxed{m_1 \times m_2 \times \cdots \times m_k}
$$

**示例**：A→B 有 $3$ 条路，B→C 有 $4$ 条路，A→B→C 共有 $3 \times 4 = 12$ 条路线。

### 1.2.2 排列——顺序重要（Permutations）

**定义**：从 $n$ 个不同元素中取出 $r$ 个（$r \le n$），按一定顺序排成一列。顺序不同算不同排列。记作 $^nP_r$ 或 $P(n,r)$。

**推导**：

$$
^nP_r = n(n-1)(n-2)\cdots(n-r+1)
$$

用阶乘表示：

$$
\boxed{^nP_r = \frac{n!}{(n-r)!}}
$$

**特殊值**：$^nP_n = n!$，$^nP_0 = 1$，$0! = 1$。

### 1.2.3 组合——顺序不重要（Combinations）

**定义**：从 $n$ 个不同元素中取出 $r$ 个（$r \le n$），不考虑顺序。记作 $^nC_r$、$C(n,r)$ 或 $\binom{n}{r}$。

**推导**：排列数除以内部排列数：

$$
\boxed{^nC_r = \binom{n}{r} = \frac{^nP_r}{r!} = \frac{n!}{r!\,(n-r)!}}
$$

**性质**：

- 对称性：$\displaystyle\binom{n}{r} = \binom{n}{n-r}$
- 边界值：$\displaystyle\binom{n}{0} = \binom{n}{n} = 1$，$\displaystyle\binom{n}{1} = \binom{n}{n-1} = n$

### 1.2.4 如何选择？（**考纲 11.1 重点**）

问自己：**交换任意两个已选元素，结果是否不同？**

| 情境 | 顺序重要？ | 使用 | 示例 |
|:----|:---------:|:----|:-----|
| 排队、名次、密码、排名 | ✅ 是 | **排列** $^nP_r$ | 6 人选 3 人站一排 |
| 委员会、选科、抽奖、组队 | ❌ 否 | **组合** $^nC_r$ | 6 人选 3 人组委员会 |

### 1.2.5 应用题例题

**例题 1**（排列——日常生活）：6 本不同的书选 4 本排上书架（从左到右），多少种摆法？

$$
^6P_4 = \frac{6!}{(6-4)!} = \frac{6!}{2!} = 6 \times 5 \times 4 \times 3 = 360
$$

答：$360$ 种。

---

**例题 2**（组合——日常生活）：7 男 5 女中选 4 人组委员会，要求至少 2 名女生，多少种选法？

- $2$ 女 $2$ 男：$\displaystyle\binom{5}{2} \times \binom{7}{2} = 10 \times 21 = 210$
- $3$ 女 $1$ 男：$\displaystyle\binom{5}{3} \times \binom{7}{1} = 10 \times 7 = 70$
- $4$ 女 $0$ 男：$\displaystyle\binom{5}{4} \times \binom{7}{0} = 5 \times 1 = 5$

总方法数：$210 + 70 + 5 = 285$。

> **补集法验证**：总数 $\displaystyle\binom{12}{4}=495$，减去"至多 1 名女生"（$0$ 女 $4$ 男 $= \binom{5}{0}\binom{7}{4}=35$，$1$ 女 $3$ 男 $= \binom{5}{1}\binom{7}{3}=5\times35=175$，共 $210$），$495 - 210 = 285$ ✓

---

**例题 3**（代数背景——组合恒等式）：证明 $\displaystyle\binom{n}{r} + \binom{n}{r-1} = \binom{n+1}{r}$，并用此计算 $\displaystyle\binom{8}{3} + \binom{8}{2}$。

**证明**：

$$
\begin{aligned}
\binom{n}{r} + \binom{n}{r-1}
&= \frac{n!}{r!(n-r)!} + \frac{n!}{(r-1)!(n-r+1)!} \\[4pt]
&= \frac{n!}{r!(n-r+1)!}\Big[(n-r+1) + r\Big] \\[4pt]
&= \frac{n! \cdot (n+1)}{r!(n-r+1)!}
= \frac{(n+1)!}{r!(n+1-r)!}
= \binom{n+1}{r}
\end{aligned}
$$

**应用**：

$$
\binom{8}{3} + \binom{8}{2} = \binom{9}{3} = \frac{9 \times 8 \times 7}{3 \times 2 \times 1} = 84
$$

### 1.2.6 ⚠️ 考试不考的内容

根据考纲，以下类型**不会出现**：

| 不考内容 | 英文原文 |
|---------|---------|
| ❌ 重复元素的排列 | *repetition of objects* |
| ❌ 圆排列 | *objects arranged in a circle* |
| ❌ 排列与组合在同一题中混合使用 | *both permutations and combinations* |

考试中每道题要么是纯排列，要么是纯组合。

---

## 1.3 二项式定理（Binomial Theorem）

### 1.3.1 二项式展开（**考纲 12.1**）

$(a+b)^n$ 可看作 $n$ 个 $(a+b)$ 相乘。展开时，每一项是分别从每个因子选 $a$ 或 $b$ 的乘积。要得到 $a^{\,n-r}b^{\,r}$，需从 $r$ 个因子中选 $b$，从 $n-r$ 个因子中选 $a$。选择方式数为 $\binom{n}{r}$。

对 $r = 0, 1, \ldots, n$ 求和：

$$
\boxed{(a+b)^n = \sum_{r=0}^{n} \binom{n}{r} a^{\,n-r} b^{\,r}}
$$

**示例**：展开 $(x+3)^4$。

$$
\begin{aligned}
(x+3)^4 &= \binom{4}{0}x^4(3)^0 + \binom{4}{1}x^3(3)^1 + \binom{4}{2}x^2(3)^2 + \binom{4}{3}x^1(3)^3 + \binom{4}{4}x^0(3)^4 \\
&= 1 \cdot x^4 + 4 \cdot 3x^3 + 6 \cdot 9x^2 + 4 \cdot 27x + 1 \cdot 81 \\
&= x^4 + 12x^3 + 54x^2 + 108x + 81
\end{aligned}
$$

注意：每一项的系数都经过了**化简**（如 $4 \times 3 = 12$，$6 \times 9 = 54$），这是考纲明确要求的。

### 1.3.2 通项公式与特定项（**考纲 12.2**）

展开式中的第 $(r+1)$ 项（从 $r=0$ 开始计数）：

$$
\boxed{T_{r+1} = \binom{n}{r} a^{\,n-r} b^{\,r}}
$$

常见题型：

| 题型 | 方法 |
|:----|:----|
| 求 $x^k$ 的系数 | 设通项中 $x$ 的指数 $= k$，解出 $r$ |
| 求常数项（不含 $x$） | 设 $x$ 的指数 $= 0$，解出 $r$ |
| 求 $x^p y^q$ 的系数 | 分别设 $x$ 和 $y$ 的指数匹配 |

> **⚠️ 重要区分**：
> - **二项式系数** = $\binom{n}{r}$（只与 $n,r$ 有关）
> - **完整系数** = $\binom{n}{r}$ × $a$ 和 $b$ 中的常数因子及符号
>
> 例如 $(2x-3)^5$ 中 $r=2$：二项式系数 $\binom{5}{2}=10$，完整系数 $= 10 \cdot (2)^3 \cdot (-3)^2 = 720$

### 1.3.3 例题

**例题 1**（求指定幂次的系数）：求 $\left(2x + \dfrac{1}{x}\right)^7$ 展开式中 $x$ 的系数。

**解**：

$$
T_{r+1} = \binom{7}{r} (2x)^{7-r} \left(\frac{1}{x}\right)^{\!r}
= \binom{7}{r} 2^{7-r} x^{7-r} \cdot x^{-r}
= \binom{7}{r} 2^{7-r} x^{7-2r}
$$

令 $7-2r = 1$，得 $r = 3$。

$$
T_4 = \binom{7}{3} 2^{4} x = 35 \times 16 \times x = 560x
$$

所以 $x$ 的系数为 $560$。

---

**例题 2**（求常数项——考纲典型）：求 $\left(x^2 - \dfrac{2}{x}\right)^6$ 展开式中的常数项。

**解**：

$$
\begin{aligned}
T_{r+1} &= \binom{6}{r} (x^2)^{6-r} \left(-\frac{2}{x}\right)^{\!r} \\
&= \binom{6}{r} (-2)^r x^{12-2r} \cdot x^{-r} \\
&= \binom{6}{r} (-2)^r x^{12-3r}
\end{aligned}
$$

令 $12 - 3r = 0$，得 $r = 4$。

$$
T_5 = \binom{6}{4} (-2)^4 = 15 \times 16 = 240
$$

所以常数项为 $240$。

---

**例题 3**（两个二项式乘积的系数）：求 $(1+x)^5 (2-x)^4$ 展开式中 $x^2$ 的系数。

**解**：

$(1+x)^5$ 通项：$\displaystyle\binom{5}{r} x^r$
$(2-x)^4$ 通项：$\displaystyle\binom{4}{k} 2^{4-k} (-1)^k x^k$

需要 $r + k = 2$：

| $r$ | $k$ | 计算 | 贡献 |
|:--:|:--:|:----|:----:|
| $0$ | $2$ | $\binom{5}{0} \cdot \binom{4}{2} 2^{2} (-1)^2 = 1 \times 6 \times 4 \times 1$ | $24$ |
| $1$ | $1$ | $\binom{5}{1} \cdot \binom{4}{1} 2^{3} (-1)^1 = 5 \times 4 \times 8 \times (-1)$ | $-160$ |
| $2$ | $0$ | $\binom{5}{2} \cdot \binom{4}{0} 2^{4} (-1)^0 = 10 \times 1 \times 16 \times 1$ | $160$ |

总和：$24 + (-160) + 160 = 24$。

答：$x^2$ 的系数为 $24$。

---

### 1.3.4 二项式系数的性质（杨辉三角）

**对称性**：

$$
\boxed{\binom{n}{r} = \binom{n}{n-r}}
$$

**杨辉法则**（递推关系）：

$$
\boxed{\binom{n}{r} + \binom{n}{r-1} = \binom{n+1}{r}}
$$

**杨辉三角**：

```
n=0:        1
n=1:       1 1
n=2:      1 2 1
n=3:     1 3 3 1
n=4:    1 4 6 4 1
n=5:   1 5 10 10 5 1
```

> **考试提示**：$n \le 5$ 时可用杨辉三角直接写系数，$n \ge 6$ 时用组合数公式 $\binom{n}{r}$。

> **不考内容**（考纲明确说明）：最大项（greatest term）和系数的性质（properties of the coefficients）不考。

---

## 本章公式速查表

| 主题 | 公式 | 条件 |
|:----|:----|:----|
| AP 第 $n$ 项 | $a_n = a + (n-1)d$ | — |
| AP 前 $n$ 项和 | $S_n = \dfrac{n}{2}[2a + (n-1)d]$ | — |
| GP 第 $n$ 项 | $a_n = a r^{\,n-1}$ | — |
| GP 前 $n$ 项和 | $S_n = a\dfrac{1-r^n}{1-r}$ | $r \neq 1$ |
| GP 无穷和 | $S_\infty = \dfrac{a}{1-r}$ | $\|r\| < 1$ |
| 排列数 | $^nP_r = \dfrac{n!}{(n-r)!}$ | 顺序重要 |
| 组合数 | $\displaystyle\binom{n}{r} = \dfrac{n!}{r!(n-r)!}$ | 顺序不重要 |
| 二项式定理 | $(a+b)^n = \displaystyle\sum_{r=0}^{n}\binom{n}{r}a^{n-r}b^{r}$ | $n \in \mathbb{Z}^+$ |
| 通项 | $T_{r+1} = \displaystyle\binom{n}{r}a^{n-r}b^{r}$ | 用于求特定项 |

---
---

# 第 2 章：向量与变化率

## 考纲对照

本章对应剑桥 IGCSE 附加数学（0606）2028–2030 考纲的以下内容：

| 考纲编号 | 内容 | 说明 |
|---------|------|------|
| **13.1** | 理解并使用向量记号 | 列向量、$\mathbf{i}$-$\mathbf{j}$ 形式、$\overrightarrow{AB}$、$p$ 等形式 |
| **13.2** | 位置向量与单位向量 | 求单位向量 $\hat{\mathbf{a}} = \frac{\mathbf{a}}{|\mathbf{a}|}$ |
| **13.3** | 向量的模、加法、减法与数乘 | 含向量相等、向量几何问题（给定图形） |
| **13.4** | 速度的合成与分解 | 求合向量、利用速度向量求位置、相撞问题 |
| **14.1** | 导函数的思想（变化率入门） | 极限的直观理解，不要求从第一原理求导 |

---

## 引言

在现实世界中，许多量不仅有大小，还有方向。从飞机航行时的风速修正，到两艘船在海上是否可能相撞，再到抛体运动的轨迹分析——这些问题的数学语言都是**向量**。

本章将从零开始构建二维向量的完整知识体系。我们先学习向量的基本表示方法和运算规则（含垂直向量的判定），然后把这些工具应用于几何问题和运动学问题（速度合成、相撞检测）。最后，我们将视角从"静态的向量"转向"动态的变化率"——当位置向量随时间变化时，它的变化率就是速度，而速度的变化率就是加速度。反过来，已知加速度，我们可通过积分求出速度和位置。这个思想将直接通向第 5 章的微分学与第 7 章的积分学。

---

## 2.1 二维向量基础

### 2.1.1 什么是向量？

向量（vector）是一个既有**大小**又有**方向**的量。与它相对的是标量（scalar），标量只有大小没有方向。例如：

- **向量**：位移、速度、力
- **标量**：距离、速率、质量、温度

在二维平面中，向量有多种等价的表示方式。

#### 表示法 1：列向量

$$
\mathbf{v} = \begin{pmatrix} x \\ y \end{pmatrix}
$$

其中 $x$ 是水平分量，$y$ 是垂直分量。这种表示法在解方程组时非常方便，因为我们可以直接对分量进行操作。

#### 表示法 2：$\mathbf{i}$-$\mathbf{j}$ 形式

定义两个基本单位向量：

$$
\mathbf{i} = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad \mathbf{j} = \begin{pmatrix} 0 \\ 1 \end{pmatrix}
$$

$\mathbf{i}$ 指向正 $x$ 轴方向（向右），$\mathbf{j}$ 指向正 $y$ 轴方向（向上）。那么任意向量可以写为：

$$
\mathbf{v} = x\mathbf{i} + y\mathbf{j}
$$

**两种表示法的等价性**：

$$
x\mathbf{i} + y\mathbf{j} = \begin{pmatrix} x \\ y \end{pmatrix}
$$

例如，向量 $3\mathbf{i} - 2\mathbf{j}$ 与列向量 $\begin{pmatrix} 3 \\ -2 \end{pmatrix}$ 是同一个向量。

#### 表示法 3：有向线段

从点 $A$ 到点 $B$ 的向量记作 $\overrightarrow{AB}$。它等于终点位置减去起点位置：

$$
\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A
$$

> **为什么是"终点减起点"？** 假设你想从家 $A$ 走到学校 $B$。你的位移（从 $A$ 到 $B$）就是你最终到达的位置（学校的位置）减去你出发时的位置（家的位置）。如果 $A$ 在 $(1,1)$，$B$ 在 $(4,5)$，那么你需要向右走 $3$ 个单位、向上走 $4$ 个单位，即 $\overrightarrow{AB} = (3,4)$。

---

### 2.1.2 位置向量

设 $O$ 为原点。任意点 $P(x, y)$ 的**位置向量**是：

$$
\mathbf{r} = \overrightarrow{OP} = \begin{pmatrix} x \\ y \end{pmatrix} = x\mathbf{i} + y\mathbf{j}
$$

位置向量告诉我们点 $P$ 相对于原点的位置。这里的关键区分是：**点** $P(x, y)$ 是空间中的一个位置，而**向量** $\mathbf{r} = (x, y)$ 是从原点到该点的有向线段——它包含了位移的信息。

> **点和向量的区别**：点是一个位置，像地图上的一个坐标。向量是一个位移，像"向右 3 步，向上 2 步"。同一个向量可以从任何起点出发，但同一个点只能在一个位置。

---

### 2.1.3 向量的模（大小）

向量 $\mathbf{v} = x\mathbf{i} + y\mathbf{j}$ 的模（或称长度、大小）由勾股定理给出：

$$
|\mathbf{v}| = \sqrt{x^2 + y^2}
$$

模一定是非负实数。当且仅当向量是零向量 $\mathbf{0} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$ 时，模为零。

> **为什么是 $\sqrt{x^2 + y^2}$？** 把向量 $\mathbf{v}$ 看作从原点 $(0,0)$ 到点 $(x,y)$ 的线段。这条线段就是直角三角形的斜边，两条直角边的长度分别是 $|x|$ 和 $|y|$。根据勾股定理，斜边长度 $= \sqrt{x^2 + y^2}$。

---

### 2.1.4 单位向量

**单位向量**是模为 1 的向量。给定任意非零向量 $\mathbf{v}$，我们可以构造与它同方向的单位向量 $\hat{\mathbf{v}}$：

$$
\hat{\mathbf{v}} = \frac{\mathbf{v}}{|\mathbf{v}|}
$$

也就是说，将原向量除以它自己的模。这个操作称为**归一化**。

> **为什么这样定义？** 设 $\hat{\mathbf{v}} = \frac{\mathbf{v}}{|\mathbf{v}|}$，那么
> $$
> |\hat{\mathbf{v}}| = \frac{|\mathbf{v}|}{|\mathbf{v}|} = 1
> $$
> 方向保持不变，因为我们在用正标量除以原向量。
>
> **类比**：就像把一段绳子切成单位长度的小段。如果你有一根 5 米长的绳子，把它切成 5 等份，每份就是 1 米，方向与原来相同。

---

### 2.1.5 向量的加法与减法

两个向量的加法，就是将它们的对应分量分别相加：

$$
\begin{pmatrix} x_1 \\ y_1 \end{pmatrix} + \begin{pmatrix} x_2 \\ y_2 \end{pmatrix} = \begin{pmatrix} x_1 + x_2 \\ y_1 + y_2 \end{pmatrix}
$$

减法同理：

$$
\begin{pmatrix} x_1 \\ y_1 \end{pmatrix} - \begin{pmatrix} x_2 \\ y_2 \end{pmatrix} = \begin{pmatrix} x_1 - x_2 \\ y_1 - y_2 \end{pmatrix}
$$

**几何意义——为什么是"平行四边形法则"？**

想象两个人同时拉一个箱子。一个人用力 $\mathbf{a}$ 向东拉，另一个人用力 $\mathbf{b}$ 向北拉。箱子实际受到的合力就是 $\mathbf{a} + \mathbf{b}$。

- **加法——平行四边形法则**：以两个向量为邻边作平行四边形，从起点出发的对角线即为它们的和。
- **减法——三角形法则**：$\mathbf{a} - \mathbf{b}$ 等于从 $\mathbf{b}$ 的终点指向 $\mathbf{a}$ 的终点的向量。

**实用的口诀**：
- 对于位移向量：**终点减起点**。从 $A$ 到 $B$ 的向量 $\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A$
- 对于加法：首尾相连，从第一个起点指向最后一个终点

---

### 2.1.6 向量的数乘

向量乘以一个标量 $c$，相当于每个分量都乘以 $c$：

$$
c \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} cx \\ cy \end{pmatrix}
$$

数乘的几何效果：
- 如果 $c > 0$，向量沿原方向拉伸（$c > 1$）或压缩（$0 < c < 1$）
- 如果 $c < 0$，向量反向

数乘后的模：

$$
|c\mathbf{v}| = |c| \cdot |\mathbf{v}|
$$

> **为什么模会乘以 $|c|$ 而不是 $c$？** 因为如果 $c = -2$，向量的长度变为原来的 2 倍，方向反转。长度是正数，所以取 $|c| = 2$。

---

### 2.1.7 向量相等

两个向量相等当且仅当它们的对应分量分别相等。即：

$$
\begin{pmatrix} x_1 \\ y_1 \end{pmatrix} = \begin{pmatrix} x_2 \\ y_2 \end{pmatrix} \iff x_1 = x_2 \quad \text{且} \quad y_1 = y_2
$$

这称为**向量相等原理**（equating like vectors）——它是解向量方程的核心工具。

> **为什么这个原理如此有用？** 一个向量方程实际上包含了两个独立的标量方程（一个对应 $x$ 分量，一个对应 $y$ 分量）。这让我们能从两个方向分别求解未知数。

---

### 2.1.8 垂直向量（正交向量）

#### 什么是垂直？

两个非零向量 $\mathbf{u}$ 和 $\mathbf{v}$ 垂直（或称正交）当且仅当它们之间的夹角是 $90^\circ$。

#### 如何判断垂直？——点积

两个向量的**点积（内积，dot product）**定义为：

$$
\mathbf{u} \cdot \mathbf{v} = u_x v_x + u_y v_y
$$

点积的结果是一个**标量**（不是向量），因此也称为"标量积"。

**垂直的判定条件**：

$$
\mathbf{u} \perp \mathbf{v} \iff \mathbf{u} \cdot \mathbf{v} = 0
$$

> **为什么点积为零代表垂直？**
>
> 从几何角度理解，点积还有另一个等价的定义：
> $$
> \mathbf{u} \cdot \mathbf{v} = |\mathbf{u}| |\mathbf{v}| \cos\theta
> $$
> 其中 $\theta$ 是两个向量之间的夹角。
>
> 推导这个等价关系：利用余弦定理。设 $\mathbf{u}$ 和 $\mathbf{v}$ 的夹角为 $\theta$，则向量 $\mathbf{u} - \mathbf{v}$ 的模满足：
> $$
> |\mathbf{u} - \mathbf{v}|^2 = |\mathbf{u}|^2 + |\mathbf{v}|^2 - 2|\mathbf{u}||\mathbf{v}|\cos\theta
> $$
> 同时展开左边：
> $$
> |\mathbf{u} - \mathbf{v}|^2 = (u_x - v_x)^2 + (u_y - v_y)^2 = (u_x^2 + u_y^2) + (v_x^2 + v_y^2) - 2(u_x v_x + u_y v_y)
> $$
> 比较两式，得：
> $$
> |\mathbf{u}|^2 + |\mathbf{v}|^2 - 2|\mathbf{u}||\mathbf{v}|\cos\theta = |\mathbf{u}|^2 + |\mathbf{v}|^2 - 2(u_x v_x + u_y v_y)
> $$
> 因此 $u_x v_x + u_y v_y = |\mathbf{u}||\mathbf{v}|\cos\theta$。
>
> 当 $\theta = 90^\circ$ 时，$\cos 90^\circ = 0$，所以点积为零。

#### 水平向量与垂直向量

一个特殊的例子：**水平向量**的 $y$ 分量为零，即 $\mathbf{h} = (h_x, 0)$（$h_x \neq 0$），它的方向平行于 $x$ 轴。**垂直向量**的 $x$ 分量为零，即 $\mathbf{v} = (0, v_y)$（$v_y \neq 0$），它的方向平行于 $y$ 轴。

水平向量总是垂直于垂直向量。用点积验证：

$$
(h_x, 0) \cdot (0, v_y) = h_x \cdot 0 + 0 \cdot v_y = 0
$$

#### 通过斜率判断垂直

如果两个非零向量都不与坐标轴平行（即 $x$ 和 $y$ 分量均不为零），我们也可以用斜率来判断垂直。设向量 $\mathbf{u}$ 的斜率为 $k_1 = \frac{u_y}{u_x}$，向量 $\mathbf{v}$ 的斜率为 $k_2 = \frac{v_y}{v_x}$，那么：

$$
\mathbf{u} \perp \mathbf{v} \iff k_1 \cdot k_2 = -1
$$

> **推导**：由点积为零的条件：
> $$
> u_x v_x + u_y v_y = 0 \implies u_x v_x = -u_y v_y \implies \frac{u_y}{u_x} \cdot \frac{v_y}{v_x} = -1
> $$
> 即 $k_1 \cdot k_2 = -1$。

> **关于零向量的说明**：零向量 $\mathbf{0} = (0, 0)$ 没有固定方向。按照惯例，在技术讨论中它被视为与所有向量既平行又垂直，但在实际解题中我们通常排除它。

---

### 📌 例题 2.1：向量基础运算

**例题 1**（向量表示、模与单位向量）

已知两点 $A(1, 2)$ 和 $B(5, -1)$。

（a）求向量 $\overrightarrow{AB}$ 用 $\mathbf{i}$-$\mathbf{j}$ 形式表示。
（b）求 $|\overrightarrow{AB}|$。
（c）求与 $\overrightarrow{AB}$ 同方向的单位向量。

**思路分析**：
- 从 $A$ 到 $B$ 的向量 = $B$ 的位置减 $A$ 的位置
- 模 = 各分量平方和的平方根
- 单位向量 = 原向量除以模

**解**：

（a）

$$
\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A = (5\mathbf{i} - \mathbf{j}) - (\mathbf{i} + 2\mathbf{j}) = (5-1)\mathbf{i} + (-1-2)\mathbf{j} = 4\mathbf{i} - 3\mathbf{j}
$$

（b）

$$
|\overrightarrow{AB}| = \sqrt{4^2 + (-3)^2} = \sqrt{16 + 9} = \sqrt{25} = 5
$$

（c）同方向的单位向量为：

$$
\hat{\mathbf{v}} = \frac{4\mathbf{i} - 3\mathbf{j}}{5} = \frac{4}{5}\mathbf{i} - \frac{3}{5}\mathbf{j}
$$

验证模长：$\sqrt{(4/5)^2 + (-3/5)^2} = \sqrt{16/25 + 9/25} = \sqrt{25/25} = 1$。✓

---

**例题 2**（向量加法、数乘与向量相等——解方程组）

已知 $\mathbf{a} = 2\mathbf{i} + 3\mathbf{j}$，$\mathbf{b} = -\mathbf{i} + 2\mathbf{j}$。求：

（a）$\mathbf{a} + \mathbf{b}$
（b）$2\mathbf{a} - 3\mathbf{b}$
（c）实数 $p$ 和 $q$ 使得 $p\mathbf{a} + q\mathbf{b} = 7\mathbf{i} + 8\mathbf{j}$

**思路分析**：
- 加法和数乘都是对分量分别操作
- 对于第（c）问，先展开左侧，利用向量相等原理（$\mathbf{i}$ 和 $\mathbf{j}$ 的系数分别相等）建立方程组

**解**：

（a）

$$
\mathbf{a} + \mathbf{b} = (2\mathbf{i} + 3\mathbf{j}) + (-\mathbf{i} + 2\mathbf{j}) = (2-1)\mathbf{i} + (3+2)\mathbf{j} = \mathbf{i} + 5\mathbf{j}
$$

（b）

$$
2\mathbf{a} - 3\mathbf{b} = 2(2\mathbf{i} + 3\mathbf{j}) - 3(-\mathbf{i} + 2\mathbf{j}) = (4\mathbf{i} + 6\mathbf{j}) + (3\mathbf{i} - 6\mathbf{j}) = 7\mathbf{i} + 0\mathbf{j} = 7\mathbf{i}
$$

（c）设 $p\mathbf{a} + q\mathbf{b} = 7\mathbf{i} + 8\mathbf{j}$，即：

$$
p(2\mathbf{i} + 3\mathbf{j}) + q(-\mathbf{i} + 2\mathbf{j}) = 7\mathbf{i} + 8\mathbf{j}
$$

先展开括号：

$$
2p\mathbf{i} + 3p\mathbf{j} - q\mathbf{i} + 2q\mathbf{j} = 7\mathbf{i} + 8\mathbf{j}
$$

合并 $\mathbf{i}$ 和 $\mathbf{j}$ 的系数：

$$
(2p - q)\mathbf{i} + (3p + 2q)\mathbf{j} = 7\mathbf{i} + 8\mathbf{j}
$$

利用向量相等原理，$\mathbf{i}$ 的系数必须相等，$\mathbf{j}$ 的系数也必须相等：

$$
\begin{cases}
2p - q = 7 \quad \text{（① $\mathbf{i}$ 系数相等）} \\[4pt]
3p + 2q = 8 \quad \text{（② $\mathbf{j}$ 系数相等）}
\end{cases}
$$

解这个方程组。从①式得 $q = 2p - 7$，代入②式：

$$
3p + 2(2p - 7) = 8 \implies 3p + 4p - 14 = 8 \implies 7p = 22 \implies p = \frac{22}{7}
$$

于是 $q = 2 \times \frac{22}{7} - 7 = \frac{44}{7} - \frac{49}{7} = -\frac{5}{7}$。

因此 $p = \frac{22}{7}$，$q = -\frac{5}{7}$。✓

---

**例题 3**（位置向量、位移与垂直向量判定）

三点 $P$、$Q$、$R$ 的位置向量分别为 $\mathbf{p} = 3\mathbf{i} + \mathbf{j}$，$\mathbf{q} = 5\mathbf{i} - 2\mathbf{j}$，$\mathbf{r} = -2\mathbf{i} + 4\mathbf{j}$。

（a）求 $\overrightarrow{PQ}$ 和 $\overrightarrow{PR}$。
（b）已知 $\overrightarrow{PS} = 2\overrightarrow{PQ}$，求 $S$ 的位置向量。
（c）判断 $\overrightarrow{PQ}$ 与 $\overrightarrow{PR}$ 是否垂直。

**思路分析**：
- $\overrightarrow{PQ} = \mathbf{q} - \mathbf{p}$（终点减起点）
- $\overrightarrow{PS} = \mathbf{s} - \mathbf{p}$，代入已知条件解出 $\mathbf{s}$
- 垂直判定：计算点积，若为零则垂直

**解**：

（a）

$$
\overrightarrow{PQ} = \mathbf{q} - \mathbf{p} = (5\mathbf{i} - 2\mathbf{j}) - (3\mathbf{i} + \mathbf{j}) = 2\mathbf{i} - 3\mathbf{j}
$$

$$
\overrightarrow{PR} = \mathbf{r} - \mathbf{p} = (-2\mathbf{i} + 4\mathbf{j}) - (3\mathbf{i} + \mathbf{j}) = -5\mathbf{i} + 3\mathbf{j}
$$

（b）设 $S$ 的位置向量为 $\mathbf{s}$。由 $\overrightarrow{PS} = \mathbf{s} - \mathbf{p}$ 且 $\overrightarrow{PS} = 2\overrightarrow{PQ}$，得：

$$
\mathbf{s} - \mathbf{p} = 2(2\mathbf{i} - 3\mathbf{j}) = 4\mathbf{i} - 6\mathbf{j}
$$

所以：

$$
\mathbf{s} = \mathbf{p} + (4\mathbf{i} - 6\mathbf{j}) = (3\mathbf{i} + \mathbf{j}) + (4\mathbf{i} - 6\mathbf{j}) = 7\mathbf{i} - 5\mathbf{j}
$$

因此 $S$ 的坐标为 $(7, -5)$。

（c）计算点积：

$$
\overrightarrow{PQ} \cdot \overrightarrow{PR} = (2)(-5) + (-3)(3) = -10 - 9 = -19 \neq 0
$$

因为点积不为零，所以 $\overrightarrow{PQ}$ 与 $\overrightarrow{PR}$ **不垂直**。

> **如果用斜率法验证**：
> $k_{PQ} = \dfrac{-3}{2} = -1.5$
> $k_{PR} = \dfrac{3}{-5} = -0.6$
> $k_{PQ} \cdot k_{PR} = (-1.5)(-0.6) = 0.9 \neq -1$
> 同样得出不垂直。✓

---

## 2.2 向量的实际运用

### 2.2.1 向量几何——深度解析

向量是解决平面几何问题的强大工具。通过将几何关系转化为向量方程，我们可以用代数方法精确求解，避免画图的不精确性。

#### 核心思想

**向量几何的本质**：用向量运算（加减、数乘）来表示几何关系。

| 几何关系 | 向量表达 |
|:---|:---|
| 从 $A$ 到 $B$ 的线段 | $\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A$ |
| $A$ 和 $B$ 的中点 $M$ | $\mathbf{r}_M = \dfrac{\mathbf{r}_A + \mathbf{r}_B}{2}$ |
| $P$ 分 $AB$ 为 $m:n$ | $\mathbf{r}_P = \dfrac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n}$ |
| $AB \parallel CD$ | $\overrightarrow{AB} = k \cdot \overrightarrow{CD}$ |
| $AB \perp CD$ | $\overrightarrow{AB} \cdot \overrightarrow{CD} = 0$ |
| $A,B,C$ 共线 | $\overrightarrow{AB} = k \cdot \overrightarrow{BC}$（存在 $k$） |

#### 中点公式——为什么是这样？

设 $M$ 是 $AB$ 的中点。从 $A$ 到 $M$ 的位移是 $\overrightarrow{AB}$ 的一半：

$$
\mathbf{r}_M = \mathbf{r}_A + \frac{1}{2}\overrightarrow{AB} = \mathbf{r}_A + \frac{1}{2}(\mathbf{r}_B - \mathbf{r}_A) = \frac{2\mathbf{r}_A + \mathbf{r}_B - \mathbf{r}_A}{2} = \frac{\mathbf{r}_A + \mathbf{r}_B}{2}
$$

#### 分点公式——详细推导

设点 $P$ 分线段 $AB$ 为 $AP:PB = m:n$（即 $P$ 靠近 $A$ 的方向上，$AP$ 占 $m$ 份，$PB$ 占 $n$ 份）。

这意味着 $P$ 位于从 $A$ 到 $B$ 的 $\dfrac{m}{m+n}$ 处（从 $A$ 算起）。所以：

$$
\begin{aligned}
\mathbf{r}_P &= \mathbf{r}_A + \frac{m}{m+n}\overrightarrow{AB} \\
&= \mathbf{r}_A + \frac{m}{m+n}(\mathbf{r}_B - \mathbf{r}_A) \\
&= \frac{(m+n)\mathbf{r}_A + m\mathbf{r}_B - m\mathbf{r}_A}{m+n} \\
&= \frac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n}
\end{aligned}
$$

> **记忆技巧**：分点公式中，$A$ 的系数是 $n$（对面那段的比例），$B$ 的系数是 $m$（对面那段的比例）。交叉相乘！
>
> 例如 $AP:PB = 2:3$（$m=2, n=3$），则：
> $$\mathbf{r}_P = \frac{3\mathbf{r}_A + 2\mathbf{r}_B}{5}$$
> $A$ 的系数是 $3$（对面的 $PB$ 是 $3$ 份），$B$ 的系数是 $2$（对面的 $AP$ 是 $2$ 份）。

#### 平行向量

两个非零向量 $\mathbf{a}$ 和 $\mathbf{b}$ 平行（即方向相同或相反）当且仅当存在一个实数 $k$ 使得：

$$
\mathbf{a} = k\mathbf{b}
$$

即一个向量是另一个向量的标量倍。

> **如何判断平行？** 检查两个向量的对应分量是否成比例：
> 若 $\mathbf{a} = (a_x, a_y)$，$\mathbf{b} = (b_x, b_y)$，且 $\frac{a_x}{b_x} = \frac{a_y}{b_y}$（分母不为零），则它们平行。
> 注意这个比例可以是负数（方向相反）。

#### 三点共线的判定

三点 $A$、$B$、$C$ 共线当且仅当 $\overrightarrow{AB}$ 与 $\overrightarrow{AC}$ 平行（或 $\overrightarrow{AB}$ 与 $\overrightarrow{BC}$ 平行）。

**为什么？** 如果三点共线，那么从 $A$ 到 $B$ 和从 $A$ 到 $C$ 的位移方向相同或相反，即存在标量 $k$ 使 $\overrightarrow{AC} = k \cdot \overrightarrow{AB}$。

---

### 📌 例题 2.2：向量几何应用

**例题 1**（平行四边形与中点——配图说明）

在平行四边形 $ABCD$ 中，$A$、$B$、$C$ 的位置向量分别为 $\mathbf{a} = \mathbf{i} + 2\mathbf{j}$，$\mathbf{b} = 4\mathbf{i} + 3\mathbf{j}$，$\mathbf{c} = 6\mathbf{i} + \mathbf{j}$。求：

（a）$D$ 的位置向量
（b）对角线 $AC$ 与 $BD$ 的交点 $M$ 的位置向量

**思路分析**：

> 先理解平行四边形的结构。顶点按 $A \to B \to C \to D \to A$ 的顺序排列。
>
> **平行四边形的关键性质**：对边平行且相等。
> - $AB \parallel DC$ 且 $AB = DC$
> - $AD \parallel BC$ 且 $AD = BC$
>
> 这意味着 $\overrightarrow{AD} = \overrightarrow{BC}$ 或 $\overrightarrow{AB} = \overrightarrow{DC}$。
>
> 另外，平行四边形的对角线**互相平分**，即 $AC$ 的中点 = $BD$ 的中点。

**解**：

（a）在平行四边形 $ABCD$ 中，对边 $AD$ 和 $BC$ 平行且相等，所以 $\overrightarrow{AD} = \overrightarrow{BC}$。

先求 $\overrightarrow{BC} = \mathbf{c} - \mathbf{b}$：

$$
\overrightarrow{BC} = (6\mathbf{i} + \mathbf{j}) - (4\mathbf{i} + 3\mathbf{j}) = 2\mathbf{i} - 2\mathbf{j}
$$

因为 $\overrightarrow{AD} = \overrightarrow{BC} = 2\mathbf{i} - 2\mathbf{j}$，而 $\overrightarrow{AD} = \mathbf{d} - \mathbf{a}$，所以：

$$
\mathbf{d} = \mathbf{a} + \overrightarrow{AD} = (\mathbf{i} + 2\mathbf{j}) + (2\mathbf{i} - 2\mathbf{j}) = 3\mathbf{i}
$$

所以 $D$ 的坐标为 $(3, 0)$。

**验证**：也可用 $\overrightarrow{AB} = \overrightarrow{DC}$ 来求。
$\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (4\mathbf{i} + 3\mathbf{j}) - (\mathbf{i} + 2\mathbf{j}) = 3\mathbf{i} + \mathbf{j}$
$\overrightarrow{DC} = \mathbf{c} - \mathbf{d}$，所以 $\mathbf{c} - \mathbf{d} = 3\mathbf{i} + \mathbf{j}$，解得 $\mathbf{d} = \mathbf{c} - (3\mathbf{i} + \mathbf{j}) = (6\mathbf{i} + \mathbf{j}) - (3\mathbf{i} + \mathbf{j}) = 3\mathbf{i}$，一致。✓

（b）平行四边形的对角线互相平分。因此 $M$ 既是 $AC$ 的中点，也是 $BD$ 的中点。

用 $AC$ 的中点计算：

$$
\mathbf{m} = \frac{\mathbf{a} + \mathbf{c}}{2} = \frac{(\mathbf{i} + 2\mathbf{j}) + (6\mathbf{i} + \mathbf{j})}{2} = \frac{7\mathbf{i} + 3\mathbf{j}}{2} = 3.5\mathbf{i} + 1.5\mathbf{j}
$$

验证用 $BD$ 的中点：$\frac{\mathbf{b} + \mathbf{d}}{2} = \frac{(4\mathbf{i} + 3\mathbf{j}) + 3\mathbf{i}}{2} = \frac{7\mathbf{i} + 3\mathbf{j}}{2}$，一致。✓

---

**例题 2**（共线判定与比值——如何证明三点共线）

三点 $A$、$B$、$C$ 的位置向量分别为 $\mathbf{a} = 2\mathbf{i} + \mathbf{j}$，$\mathbf{b} = 5\mathbf{i} + 4\mathbf{j}$，$\mathbf{c} = 8\mathbf{i} + 7\mathbf{j}$。

（a）证明 $A$、$B$、$C$ 三点共线。
（b）求 $AB:BC$ 的比值。

**思路分析**：

> 证明三点共线的标准方法：
> 1. 计算 $\overrightarrow{AB}$ 和 $\overrightarrow{BC}$（或 $\overrightarrow{AB}$ 和 $\overrightarrow{AC}$）
> 2. 判断它们是否平行（即是否存在标量 $k$ 使得一个等于另一个乘以 $k$）
> 3. 如果平行且有一个公共点（$B$ 是 $\overrightarrow{AB}$ 和 $\overrightarrow{BC}$ 的公共点），则三点共线

**解**：

（a）计算向量：

$$
\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (5\mathbf{i} + 4\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = 3\mathbf{i} + 3\mathbf{j}
$$

$$
\overrightarrow{BC} = \mathbf{c} - \mathbf{b} = (8\mathbf{i} + 7\mathbf{j}) - (5\mathbf{i} + 4\mathbf{j}) = 3\mathbf{i} + 3\mathbf{j}
$$

观察发现 $\overrightarrow{BC} = \overrightarrow{AB}$，即 $\overrightarrow{BC} = 1 \cdot \overrightarrow{AB}$。存在标量 $k = 1$ 使得 $\overrightarrow{BC} = k\overrightarrow{AB}$，所以 $\overrightarrow{AB} \parallel \overrightarrow{BC}$。又因为这两个向量都通过点 $B$，故 $A$、$B$、$C$ 共线。

> **注意**：也可以验证 $\overrightarrow{AC}$ 与 $\overrightarrow{AB}$ 的关系。
> $\overrightarrow{AC} = \mathbf{c} - \mathbf{a} = (8\mathbf{i} + 7\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = 6\mathbf{i} + 6\mathbf{j} = 2(3\mathbf{i} + 3\mathbf{j}) = 2\overrightarrow{AB}$
> 同样得出共线结论。

（b）因为 $\overrightarrow{BC} = \overrightarrow{AB}$，且方向相同，所以 $\overrightarrow{AB}$ 和 $\overrightarrow{BC}$ 的长度相等。即 $AB = BC$，因此 $AB:BC = 1:1$。

换句话说，$B$ 是线段 $AC$ 的中点。

---

**例题 3**（分点公式 + 垂直验证——综合应用）

在 $\triangle OAB$ 中，$C$ 在 $OA$ 上且 $OC:CA = 2:1$，$D$ 在 $AB$ 上且 $AD:DB = 3:1$。设 $\overrightarrow{OA} = \mathbf{a}$，$\overrightarrow{OB} = \mathbf{b}$。

（a）用 $\mathbf{a}$ 和 $\mathbf{b}$ 表示 $\overrightarrow{OD}$。
（b）用 $\mathbf{a}$ 和 $\mathbf{b}$ 表示 $\overrightarrow{CD}$。
（c）已知 $\mathbf{a} = 3\mathbf{i} + 2\mathbf{j}$，$\mathbf{b} = \mathbf{i} + 6\mathbf{j}$，判断 $\overrightarrow{OC}$ 与 $\overrightarrow{OD}$ 是否垂直。

**思路分析**：

> 这是一个"用基底表示向量"的典型问题。$\mathbf{a}$ 和 $\mathbf{b}$ 是基底，所有其他向量都要用它们表示。
>
> 关键步骤：
> 1. 确定分点 $C$ 在 $OA$ 上的位置：$OC:CA = 2:1$ 意味着 $OC = \frac{2}{3}OA$
> 2. 确定分点 $D$ 在 $AB$ 上的位置：$AD:DB = 3:1$ 意味着 $AD = \frac{3}{4}AB$
> 3. 用分点公式或直接加减法表示向量
> 4. 垂直判定：代入具体数值后计算点积

**解**：

（a）先表示 $D$ 的位置。

方法一（分点公式）：$D$ 分 $AB$ 为 $AD:DB = 3:1$，即从 $A$ 到 $B$ 的方向上，$D$ 位于 $\frac{3}{4}$ 处。

由分点公式（$m=3, n=1$）：

$$
\mathbf{r}_D = \frac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n} = \frac{1 \cdot \mathbf{a} + 3 \cdot \mathbf{b}}{3+1} = \frac{\mathbf{a} + 3\mathbf{b}}{4}
$$

方法二（直接法）：从 $A$ 出发走到 $B$ 的 $\frac{3}{4}$ 处。

$$
\overrightarrow{OD} = \overrightarrow{OA} + \frac{3}{4}\overrightarrow{AB}
$$

而 $\overrightarrow{AB} = \overrightarrow{OB} - \overrightarrow{OA} = \mathbf{b} - \mathbf{a}$，所以：

$$
\overrightarrow{OD} = \mathbf{a} + \frac{3}{4}(\mathbf{b} - \mathbf{a}) = \mathbf{a} + \frac{3}{4}\mathbf{b} - \frac{3}{4}\mathbf{a} = \frac{1}{4}\mathbf{a} + \frac{3}{4}\mathbf{b}
$$

注意 $\frac{\mathbf{a} + 3\mathbf{b}}{4} = \frac{1}{4}\mathbf{a} + \frac{3}{4}\mathbf{b}$，两种方法结果一致。✓

（b）$C$ 在 $OA$ 上且 $OC:CA = 2:1$，所以 $C$ 分 $\overrightarrow{OA}$ 为 $2:1$（从 $O$ 算起）。因此：

$$
\overrightarrow{OC} = \frac{2}{3}\overrightarrow{OA} = \frac{2}{3}\mathbf{a}
$$

于是：

$$
\overrightarrow{CD} = \overrightarrow{OD} - \overrightarrow{OC} = \left(\frac{1}{4}\mathbf{a} + \frac{3}{4}\mathbf{b}\right) - \frac{2}{3}\mathbf{a}
$$

通分计算 $\mathbf{a}$ 的系数：$\frac{1}{4} - \frac{2}{3} = \frac{3}{12} - \frac{8}{12} = -\frac{5}{12}$。

所以：

$$
\overrightarrow{CD} = -\frac{5}{12}\mathbf{a} + \frac{3}{4}\mathbf{b}
$$

（c）代入 $\mathbf{a} = 3\mathbf{i} + 2\mathbf{j}$，$\mathbf{b} = \mathbf{i} + 6\mathbf{j}$：

先求 $\overrightarrow{OC}$：

$$
\overrightarrow{OC} = \frac{2}{3}(3\mathbf{i} + 2\mathbf{j}) = 2\mathbf{i} + \frac{4}{3}\mathbf{j}
$$

再求 $\overrightarrow{OD}$：

$$
\begin{aligned}
\overrightarrow{OD} &= \frac{1}{4}(3\mathbf{i} + 2\mathbf{j}) + \frac{3}{4}(\mathbf{i} + 6\mathbf{j}) \\
&= \left(\frac{3}{4} + \frac{3}{4}\right)\mathbf{i} + \left(\frac{1}{2} + \frac{9}{2}\right)\mathbf{j} \\
&= \frac{6}{4}\mathbf{i} + \frac{10}{2}\mathbf{j} \\
&= \frac{3}{2}\mathbf{i} + 5\mathbf{j}
\end{aligned}
$$

计算点积：

$$
\overrightarrow{OC} \cdot \overrightarrow{OD} = \left(2\right)\left(\frac{3}{2}\right) + \left(\frac{4}{3}\right)(5) = 3 + \frac{20}{3} = \frac{9}{3} + \frac{20}{3} = \frac{29}{3} \neq 0
$$

点积不为零，所以 $\overrightarrow{OC}$ 与 $\overrightarrow{OD}$ **不垂直**。

---

### 2.2.2 速度的合成与分解

速度是一个向量。当一个物体同时参与两个或更多运动时，它的合速度是这些速度的向量和。

#### 相对速度公式

设物体 $A$ 相对于参考系 $C$ 的速度为 $\mathbf{v}_{A/C}$，物体 $A$ 相对于物体 $B$ 的速度为 $\mathbf{v}_{A/B}$，物体 $B$ 相对于参考系 $C$ 的速度为 $\mathbf{v}_{B/C}$，则：

$$
\mathbf{v}_{A/C} = \mathbf{v}_{A/B} + \mathbf{v}_{B/C}
$$

> **直观理解**：
> - 你在火车上行走，速度为 $\mathbf{v}_{A/B}$（你相对于火车）
> - 火车相对于地面行驶，速度为 $\mathbf{v}_{B/C}$（火车相对于地面）
> - 你相对于地面的速度 $\mathbf{v}_{A/C}$ 就是两者之和
>
> **另一个例子**：一艘船在河中行驶。
> - 船在静水中的速度 = $\mathbf{v}_{B/W}$（船相对于水）
> - 水流速度 = $\mathbf{v}_{W/G}$（水相对于地面）
> - 船相对于地面的实际速度 = $\mathbf{v}_{B/W} + \mathbf{v}_{W/G}$

#### 速度的分解

与合成相反，将一个速度向量分解为两个互相垂直的分量（通常沿水平方向和垂直方向）称为**速度的分解**。

设速度 $\mathbf{v}$ 的大小为 $v$（速率），与水平方向的夹角为 $\theta$，则：

$$
\mathbf{v} = (v\cos\theta)\mathbf{i} + (v\sin\theta)\mathbf{j}
$$

其中 $v_x = v\cos\theta$ 是水平分量，$v_y = v\sin\theta$ 是垂直分量。

> **推导**：将速度向量投影到 $x$ 轴和 $y$ 轴上。在直角三角形中，邻边 $=$ 斜边 $\times \cos\theta$，对边 $=$ 斜边 $\times \sin\theta$。

---

#### 相撞问题

两个运动物体相撞的条件是：在**同一时刻**，它们的位置向量**相等**。即：

$$
\mathbf{r}_1(t) = \mathbf{r}_2(t)
$$

对于匀速直线运动，位置向量满足：

$$
\mathbf{r}(t) = \mathbf{r}_0 + \mathbf{v}t
$$

其中 $\mathbf{r}_0$ 是初始位置向量，$\mathbf{v}$ 是速度向量。因此相撞条件可以展开为：

$$
\mathbf{r}_{01} + \mathbf{v}_1 t = \mathbf{r}_{02} + \mathbf{v}_2 t
$$

这是一个关于时间 $t$ 的向量方程。它等价于两个分量方程分别相等，从而可以解出 $t$ 并验证是否一致。

**解题步骤**：
1. 写出两物体的位置向量 $\mathbf{r}_1(t)$ 和 $\mathbf{r}_2(t)$。
2. 令 $\mathbf{r}_1(t) = \mathbf{r}_2(t)$，得到两个分量方程。
3. 分别解出 $t$。如果两个 $t$ 值相等且 $\geq 0$，则相撞；否则不相撞。

> **注意**："相撞"要求同时在同一位置。如果两船在不同时间到达同一点，那只叫"相遇"而非"相撞"。

---

### 📌 例题 2.3：速度合成与相撞问题

**例题 1**（速度合成——船与水流）

一艘船在静水中的速度是 $6\,\text{m/s}$ 向东。水流以 $4\,\text{m/s}$ 的速度向北流动。求船相对于地面的速度的大小和方向。

**思路分析**：
- 船相对于水的速度 $\mathbf{v}_{B/W}$ = 向东 $6$ m/s
- 水相对于地面的速度 $\mathbf{v}_{W/G}$ = 向北 $4$ m/s
- 船相对于地面的速度 $\mathbf{v}_{B/G} = \mathbf{v}_{B/W} + \mathbf{v}_{W/G}$

**解**：

设正东方向为 $+x$ 轴，正北方向为 $+y$ 轴。

船相对于水的速度：$\mathbf{v}_{B/W} = 6\mathbf{i}$
水流相对于地面的速度：$\mathbf{v}_{W/G} = 4\mathbf{j}$

由速度合成公式：

$$
\mathbf{v}_{B/G} = \mathbf{v}_{B/W} + \mathbf{v}_{W/G} = 6\mathbf{i} + 4\mathbf{j}
$$

合速度的大小（速率）：

$$
|\mathbf{v}_{B/G}| = \sqrt{6^2 + 4^2} = \sqrt{36 + 16} = \sqrt{52} = 2\sqrt{13} \approx 7.21\,\text{m/s}
$$

合速度的方向：设 $\theta$ 为与正东方向的夹角（逆时针为正）。

$$
\tan\theta = \frac{4}{6} = \frac{2}{3} \implies \theta = \arctan\left(\frac{2}{3}\right) \approx 33.69^\circ
$$

因此船相对于地面的速度大小为 $2\sqrt{13}\,\text{m/s}$，方向为北偏东 $33.69^\circ$（即从正东方向逆时针旋转 $33.69^\circ$）。

> **生活实例**：这就是为什么船过河时，如果直接朝对岸开，会被水流冲偏。要想直接到达正对岸，船头必须朝上游方向倾斜。

---

**例题 2**（速度分解——斜抛的初速度）

一个球以初速度 $20\,\text{m/s}$、与水平方向成 $30^\circ$ 角斜向上抛出。

（a）求初速度的水平分量和垂直分量。
（b）写出初速度的向量形式。

**思路分析**：
- 速度的大小是 $20$，方向是 $30^\circ$ 仰角
- 水平分量 $v_x = v\cos\theta$，垂直分量 $v_y = v\sin\theta$

**解**：

（a）设水平向右为 $+x$ 轴，竖直向上为 $+y$ 轴。

水平分量：

$$
v_x = v\cos\theta = 20 \times \cos 30^\circ = 20 \times \frac{\sqrt{3}}{2} = 10\sqrt{3} \approx 17.32\,\text{m/s}
$$

垂直分量：

$$
v_y = v\sin\theta = 20 \times \sin 30^\circ = 20 \times \frac{1}{2} = 10\,\text{m/s}
$$

（b）初速度的向量形式：

$$
\mathbf{v}_0 = 10\sqrt{3}\,\mathbf{i} + 10\,\mathbf{j}\,\text{m/s}
$$

> **物理意义**：
> - 如果没有空气阻力，水平分量 $v_x$ 在整个运动过程中保持不变（因为水平方向不受力）
> - 而垂直分量 $v_y$ 受重力影响以 $-g$ 的加速度变化（$g \approx 9.8\,\text{m/s}^2$）
> - 所以任意时刻的速度为 $\mathbf{v}(t) = 10\sqrt{3}\,\mathbf{i} + (10 - gt)\,\mathbf{j}$
> - 这为第 10 章的运动学问题奠定了基础

---

**例题 3**（相撞问题——两船是否会相撞）

船 $P$ 从点 $(0, 0)$ 出发，以速度 $\mathbf{v}_P = (3\mathbf{i} + 4\mathbf{j})\,\text{km/h}$ 航行。船 $Q$ 从点 $(10, 5)\,\text{km}$ 出发，以速度 $\mathbf{v}_Q = (-2\mathbf{i} + \mathbf{j})\,\text{km/h}$ 航行。两船同时出发，判断它们是否会相撞。

**思路分析**：
1. 写出两船的位置向量（都是 $\mathbf{r}_0 + \mathbf{v}t$ 的形式）
2. 令 $\mathbf{r}_P(t) = \mathbf{r}_Q(t)$
3. 得到两个分量方程，分别解 $t$
4. 如果 $t$ 值一致且 $\geq 0$，相撞；否则不相撞

**解**：

设 $t$ 为出发后的时间（小时）。

$P$ 的位置向量（从原点出发）：

$$
\mathbf{r}_P(t) = \begin{pmatrix} 0 \\ 0 \end{pmatrix} + \begin{pmatrix} 3 \\ 4 \end{pmatrix} t = \begin{pmatrix} 3t \\ 4t \end{pmatrix}
$$

$Q$ 的位置向量（从 $(10,5)$ 出发）：

$$
\mathbf{r}_Q(t) = \begin{pmatrix} 10 \\ 5 \end{pmatrix} + \begin{pmatrix} -2 \\ 1 \end{pmatrix} t = \begin{pmatrix} 10 - 2t \\ 5 + t \end{pmatrix}
$$

如果两船相撞，则存在某个 $t \geq 0$ 使得 $\mathbf{r}_P(t) = \mathbf{r}_Q(t)$，即：

$$
\begin{pmatrix} 3t \\ 4t \end{pmatrix} = \begin{pmatrix} 10 - 2t \\ 5 + t \end{pmatrix}
$$

这给出两个分量方程：

$$
\begin{cases}
x\text{分量：} & 3t = 10 - 2t \implies 5t = 10 \implies t = 2 \\[4pt]
y\text{分量：} & 4t = 5 + t \implies 3t = 5 \implies t = \dfrac{5}{3}
\end{cases}
$$

两个 $t$ 值不相等（$2 \neq \frac{5}{3}$），因此不存在同时满足两个分量方程的时刻。两船不会相撞。

> **为什么不相撞？** 即使 $x$ 坐标在 $t=2$ 时相等，$y$ 坐标在 $t=2$ 时分别为 $4\times 2 = 8$ 和 $5+2=7$，不相等。所以两船永远不会在同一时刻到达同一点。

---

## 2.3 变化率入门（微积分铺垫）

### 2.3.1 为何研究变化率？

在物理世界中，很少有事物是静止的。一辆行驶的汽车，它的位置在变化；一个充气的气球，它的体积在变化；一个加热的金属棒，它的温度在变化。**变化率**就是描述"一个量随另一个量变化得有多快"的数学工具。

在 2.1 和 2.2 节中，我们用向量描述了位置、速度和加速度。现在我们要问一个更深入的问题：**如何精确地定义"瞬时"变化率？**

---

### 2.3.2 从平均变化率到瞬时变化率

让我们从一个具体的运动学例子开始。

一个质点沿直线运动，它的位移 $s$（单位：米）与时间 $t$（单位：秒）的关系为：

$$
s(t) = t^2
$$

我们想知道 $t = 1$ 秒这一**瞬间**的速度。

#### 第一步：平均速度

如果取一个时间区间 $[1, 1 + \Delta t]$，质点在区间内的平均速度是：

$$
\text{平均速度} = \frac{s(1 + \Delta t) - s(1)}{\Delta t}
$$

代入 $s(t) = t^2$：

$$
\frac{(1 + \Delta t)^2 - 1^2}{\Delta t} = \frac{1 + 2\Delta t + (\Delta t)^2 - 1}{\Delta t} = \frac{2\Delta t + (\Delta t)^2}{\Delta t} = 2 + \Delta t
$$

#### 第二步：让 $\Delta t$ 越来越小

我们让 $\Delta t$ 逐渐趋近于 0，观察平均速度的变化：

| $\Delta t$（秒） | 平均速度（m/s） |
|:---:|:---:|
| 0.1 | $2 + 0.1 = 2.1$ |
| 0.01 | $2 + 0.01 = 2.01$ |
| 0.001 | $2 + 0.001 = 2.001$ |
| 0.0001 | $2 + 0.0001 = 2.0001$ |
| $\to 0$ | $\to 2$ |

随着 $\Delta t$ 越来越接近 0，平均速度越来越接近 **2**。

#### 第三步：极限

当 $\Delta t$ 趋近于 0 时，平均速度 $2 + \Delta t$ 趋近于 2。我们记：

$$
v(1) = \lim_{\Delta t \to 0} \frac{s(1 + \Delta t) - s(1)}{\Delta t} = \lim_{\Delta t \to 0} (2 + \Delta t) = 2
$$

这个极限值就是质点在 $t = 1$ 时的**瞬时速度**。

> **重要理解**：我们从不令 $\Delta t = 0$（那样会得到 $0/0$，没有意义）。我们让 $\Delta t$ 无限趋近于 0，观察比值趋近于哪个固定值。这个"趋近的目标"就是导数。
>
> 用极限的语言说：**当 $\Delta t$ 趋近于 0 时，平均速度的极限就是瞬时速度。**

---

### 2.3.3 导数的一般定义

一般地，对于函数 $y = f(x)$，它在 $x = a$ 处的**导数**（即瞬时变化率）定义为：

$$
f'(a) = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h}
$$

其中 $h$ 就是前面例子中的 $\Delta x$ 或 $\Delta t$。

如果这个极限存在，我们就说 $f$ 在 $x = a$ 处**可导**。

**导数的记号**：
- 莱布尼茨记号：$\dfrac{dy}{dx}$ 或 $\dfrac{d}{dx}f(x)$
- 拉格朗日记号：$f'(x)$
- 牛顿记号（常用于物理）：$\dot{y}$

> 在考纲 14.1 中，只要求对极限有直观理解，不要求从第一原理求导。但我们这里仍会展示几个基本推导，帮助你建立直觉。

---

### 2.3.4 用定义求导——基础推导

让我们用极限定义推导几个基本函数的导数。

#### 推导 1：$f(x) = x^2$

$$
\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{(x + h)^2 - x^2}{h} \\
&= \lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h} \\
&= \lim_{h \to 0} \frac{2xh + h^2}{h} \\
&= \lim_{h \to 0} (2x + h) \\
&= 2x
\end{aligned}
$$

因此 $\dfrac{d}{dx}(x^2) = 2x$。

**几何意义**：函数 $y = x^2$ 在任意点 $x$ 处的切线斜率为 $2x$。在 $x = 1$ 处斜率为 $2$，在 $x = 3$ 处斜率为 $6$。

#### 推导 2：$f(x) = x^3$

$$
\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{(x + h)^3 - x^3}{h}
\end{aligned}
$$

展开 $(x + h)^3 = x^3 + 3x^2h + 3xh^2 + h^3$：

$$
\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{x^3 + 3x^2h + 3xh^2 + h^3 - x^3}{h} \\
&= \lim_{h \to 0} \frac{3x^2h + 3xh^2 + h^3}{h} \\
&= \lim_{h \to 0} (3x^2 + 3xh + h^2) \\
&= 3x^2
\end{aligned}
$$

因此 $\dfrac{d}{dx}(x^3) = 3x^2$。

#### 推导 3：$f(x) = \dfrac{1}{x}$（$x \neq 0$）

$$
\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{\frac{1}{x + h} - \frac{1}{x}}{h}
\end{aligned}
$$

先通分分子：

$$
\frac{1}{x + h} - \frac{1}{x} = \frac{x - (x + h)}{x(x + h)} = \frac{-h}{x(x + h)}
$$

所以：

$$
\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{-h}{x(x + h)} \cdot \frac{1}{h} \\
&= \lim_{h \to 0} \frac{-1}{x(x + h)} \\
&= -\frac{1}{x^2}
\end{aligned}
$$

因此 $\dfrac{d}{dx}\left(\dfrac{1}{x}\right) = -\dfrac{1}{x^2}$。

---

### 2.3.5 幂法则

从上面的推导中，我们可以观察出一个模式：

| $f(x)$ | $f'(x)$ |
|:---:|:---:|
| $x^2$ | $2x$ |
| $x^3$ | $3x^2$ |
| $x^1$ | $1$（即 $1 \cdot x^0$） |
| $\dfrac{1}{x} = x^{-1}$ | $-\dfrac{1}{x^2} = -x^{-2}$ |

这个模式就是**幂法则**：对任意实数 $n$，

$$
\boxed{\frac{d}{dx}(x^n) = n x^{n-1}}
$$

> **幂法则的完整推导**（利用二项式定理，仅对正整数 $n$）：
>
> 考虑 $f(x) = x^n$，其中 $n$ 为正整数。利用二项式定理展开 $(x + h)^n$：
> $$
> (x + h)^n = x^n + n x^{n-1}h + \binom{n}{2}x^{n-2}h^2 + \binom{n}{3}x^{n-3}h^3 + \dots + h^n
> $$
> 因此：
> $$
> \begin{aligned}
> f'(x) &= \lim_{h \to 0} \frac{x^n + n x^{n-1}h + \binom{n}{2}x^{n-2}h^2 + \dots + h^n - x^n}{h} \\
> &= \lim_{h \to 0} \left( n x^{n-1} + \binom{n}{2}x^{n-2}h + \binom{n}{3}x^{n-3}h^2 + \dots + h^{n-1} \right) \\
> &= n x^{n-1}
> \end{aligned}
> $$
> 因为所有含 $h$ 的项在 $h \to 0$ 时都趋于 0。

---

### 2.3.6 变化率在向量中的应用：运动学

现在回到向量的语境中。如果质点的位置向量 $\mathbf{r}(t)$ 随时间变化，那么它的速度向量和加速度向量就是位置向量对时间的变化率。

设 $\mathbf{r}(t) = x(t)\mathbf{i} + y(t)\mathbf{j}$，则：

$$
\mathbf{v}(t) = \frac{d\mathbf{r}}{dt} = \frac{dx}{dt}\mathbf{i} + \frac{dy}{dt}\mathbf{j}
$$

$$
\mathbf{a}(t) = \frac{d\mathbf{v}}{dt} = \frac{d^2\mathbf{r}}{dt^2} = \frac{d^2x}{dt^2}\mathbf{i} + \frac{d^2y}{dt^2}\mathbf{j}
$$

也就是说，对向量函数求导，就是对它的各个分量分别求导。

---

### 2.3.7 从加速度到速度和位置（积分铺垫）

在物理中，加速度 $\mathbf{a}(t)$ 是速度 $\mathbf{v}(t)$ 的变化率。如果我们知道加速度并想恢复出速度，需要做微分的逆运算——这称为**积分**（将在第 7 章详细学习）。

基本关系是：

- 速度 $\mathbf{v}(t) = \int \mathbf{a}(t) \, dt + \mathbf{v}_0$（其中 $\mathbf{v}_0$ 是初始速度）
- 位置 $\mathbf{r}(t) = \int \mathbf{v}(t) \, dt + \mathbf{r}_0$（其中 $\mathbf{r}_0$ 是初始位置）

或者用定积分的形式（更适合已知确定时间段的问题）：

$$
\mathbf{v}(t) = \mathbf{v}_0 + \int_0^t \mathbf{a}(u) \, du,
\quad
\mathbf{r}(t) = \mathbf{r}_0 + \int_0^t \mathbf{v}(u) \, du
$$

这里先建立直观理解：**微分**是求变化率（位置 → 速度 → 加速度），**积分**是求累积量（加速度 → 速度 → 位置），两者互为逆运算。

---

### 📌 例题 2.4：变化率入门

**例题 1**（用极限定义求瞬时速度）

一个质点的位移（单位：米）与时间（单位：秒）的关系为 $s(t) = 3t^2 - 2t + 1$。

（a）求从 $t = 2$ 到 $t = 2 + h$ 的平均速度。
（b）利用极限求 $t = 2$ 时的瞬时速度。

**思路分析**：
- 平均速度 = $\dfrac{s(2+h) - s(2)}{h}$
- 瞬时速度 = $\displaystyle\lim_{h \to 0}$ 平均速度

**解**：

（a）

$$
\begin{aligned}
\text{平均速度} &= \frac{s(2 + h) - s(2)}{h} \\
&= \frac{[3(2+h)^2 - 2(2+h) + 1] - [3(4) - 4 + 1]}{h} \\
&= \frac{[3(4 + 4h + h^2) - 4 - 2h + 1] - [12 - 4 + 1]}{h} \\
&= \frac{[12 + 12h + 3h^2 - 4 - 2h + 1] - 9}{h} \\
&= \frac{[9 + 10h + 3h^2] - 9}{h} \\
&= \frac{10h + 3h^2}{h} = 10 + 3h
\end{aligned}
$$

（b）瞬时速度是 $h \to 0$ 时平均速度的极限：

$$
v(2) = \lim_{h \to 0} (10 + 3h) = 10\,\text{m/s}
$$

因此质点在 $t = 2$ 秒时的瞬时速度为 $10\,\text{m/s}$。

> **验证**：用幂法则直接求导：$s'(t) = 6t - 2$，$s'(2) = 12 - 2 = 10$，一致。✓

---

**例题 2**（用极限定义求一般导数 + 幂法则验证）

用导数的极限定义求 $f(x) = 4x - x^2$ 的导数 $f'(x)$。

**解**：

$$
\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{f(x + h) - f(x)}{h} \\
&= \lim_{h \to 0} \frac{[4(x + h) - (x + h)^2] - [4x - x^2]}{h} \\
&= \lim_{h \to 0} \frac{4x + 4h - (x^2 + 2xh + h^2) - 4x + x^2}{h} \\
&= \lim_{h \to 0} \frac{4h - 2xh - h^2}{h} \\
&= \lim_{h \to 0} (4 - 2x - h) \\
&= 4 - 2x
\end{aligned}
$$

因此 $f'(x) = 4 - 2x$。

**验证**：使用幂法则对 $f(x) = 4x - x^2$ 逐项求导：
- $\dfrac{d}{dx}(4x) = 4 \cdot 1 \cdot x^{0} = 4$
- $\dfrac{d}{dx}(-x^2) = -2x^{1} = -2x$
- 相加得 $f'(x) = 4 - 2x$，与极限结果一致。✓

---

**例题 3**（向量的变化率 + 积分逆运算）

一个质点在平面内运动，它的位置向量为：

$$
\mathbf{r}(t) = (t^3 - 3t)\mathbf{i} + (t^2 - 2t)\mathbf{j}
$$

其中 $t$ 以秒为单位，位置以米为单位。

（a）求速度向量 $\mathbf{v}(t)$。
（b）求加速度向量 $\mathbf{a}(t)$。
（c）求 $t = 2$ 秒时的速度和加速度向量。
（d）已知该质点的加速度恒为 $\mathbf{a}(t) = 6t\mathbf{i} + 2\mathbf{j}$，初速度 $\mathbf{v}_0 = -3\mathbf{i} - 2\mathbf{j}$，初始位置 $\mathbf{r}_0 = \mathbf{0}$。用积分求 $\mathbf{v}(t)$ 和 $\mathbf{r}(t)$，验证与（a）（b）一致。

**思路分析**：
- 速度 = 位置的导数（分量分别求导）
- 加速度 = 速度的导数（分量分别求导）
- 积分是微分的逆运算：已知加速度，积分一次得速度（加常数），再积分一次得位置（加常数）
- 常数由初始条件确定

**解**：

（a）速度是位置对时间的导数，对各分量分别求导：

$$
\mathbf{v}(t) = \frac{d\mathbf{r}}{dt} = \frac{d}{dt}(t^3 - 3t)\,\mathbf{i} + \frac{d}{dt}(t^2 - 2t)\,\mathbf{j}
$$

使用幂法则：
- $\dfrac{d}{dt}(t^3) = 3t^2$
- $\dfrac{d}{dt}(-3t) = -3$
- $\dfrac{d}{dt}(t^2) = 2t$
- $\dfrac{d}{dt}(-2t) = -2$

因此：

$$
\mathbf{v}(t) = (3t^2 - 3)\mathbf{i} + (2t - 2)\mathbf{j}
$$

（b）加速度是速度对时间的导数：

$$
\mathbf{a}(t) = \frac{d\mathbf{v}}{dt} = \frac{d}{dt}(3t^2 - 3)\,\mathbf{i} + \frac{d}{dt}(2t - 2)\,\mathbf{j}
$$

$$
\mathbf{a}(t) = (6t)\mathbf{i} + 2\mathbf{j}
$$

（c）代入 $t = 2$：

$$
\mathbf{v}(2) = (3 \times 4 - 3)\mathbf{i} + (4 - 2)\mathbf{j} = 9\mathbf{i} + 2\mathbf{j}\,\text{m/s}
$$

速度的大小：$|\mathbf{v}(2)| = \sqrt{9^2 + 2^2} = \sqrt{81 + 4} = \sqrt{85} \approx 9.22\,\text{m/s}$

$$
\mathbf{a}(2) = (6 \times 2)\mathbf{i} + 2\mathbf{j} = 12\mathbf{i} + 2\mathbf{j}\,\text{m/s}^2
$$

加速度的大小：$|\mathbf{a}(2)| = \sqrt{12^2 + 2^2} = \sqrt{144 + 4} = \sqrt{148} = 2\sqrt{37} \approx 12.17\,\text{m/s}^2$

（d）已知 $\mathbf{a}(t) = (6t)\mathbf{i} + 2\mathbf{j}$，对加速度积分求速度：

$$
\mathbf{v}(t) = \int \mathbf{a}(t) \, dt = \left(\int 6t \, dt\right)\mathbf{i} + \left(\int 2 \, dt\right)\mathbf{j}
$$

$$
= (3t^2 + C_1)\mathbf{i} + (2t + C_2)\mathbf{j}
$$

由 $\mathbf{v}_0 = \mathbf{v}(0) = -3\mathbf{i} - 2\mathbf{j}$，代入 $t = 0$ 得 $C_1 = -3$，$C_2 = -2$。所以：

$$
\mathbf{v}(t) = (3t^2 - 3)\mathbf{i} + (2t - 2)\mathbf{j}
$$

与（a）一致。✓

再对速度积分求位置：

$$
\mathbf{r}(t) = \int \mathbf{v}(t) \, dt = \left(\int (3t^2 - 3) \, dt\right)\mathbf{i} + \left(\int (2t - 2) \, dt\right)\mathbf{j}
$$

$$
= (t^3 - 3t + D_1)\mathbf{i} + (t^2 - 2t + D_2)\mathbf{j}
$$

由 $\mathbf{r}_0 = \mathbf{r}(0) = \mathbf{0}$，代入 $t = 0$ 得 $D_1 = 0$，$D_2 = 0$。所以：

$$
\mathbf{r}(t) = (t^3 - 3t)\mathbf{i} + (t^2 - 2t)\mathbf{j}
$$

与原始位置函数一致。✓

---

## 2.4 本章练习题

以下练习题按考试难度编写，涵盖本章所有知识点，题号前面标注了对应的考纲编号。

---

**13.1–13.3 题组：向量基础与几何**

**1.** 已知 $\mathbf{a} = 2\mathbf{i} - \mathbf{j}$，$\mathbf{b} = \mathbf{i} + 3\mathbf{j}$。

（a）求 $\mathbf{a} + 2\mathbf{b}$。
（b）求 $|2\mathbf{a} - \mathbf{b}|$。
（c）求与 $3\mathbf{a} + \mathbf{b}$ 同方向的单位向量。

---

**2.** 在 $\triangle ABC$ 中，$P$ 是 $BC$ 的中点，$Q$ 是 $CA$ 的中点。设 $\overrightarrow{AB} = \mathbf{p}$，$\overrightarrow{AC} = \mathbf{q}$。

（a）用 $\mathbf{p}$ 和 $\mathbf{q}$ 表示 $\overrightarrow{BC}$。
（b）用 $\mathbf{p}$ 和 $\mathbf{q}$ 表示 $\overrightarrow{PQ}$。
（c）证明 $PQ \parallel AB$ 且 $PQ = \frac{1}{2} AB$。

---

**3.** 三点 $A$、$B$、$C$ 的位置向量分别为 $\mathbf{a} = 3\mathbf{i} + 2\mathbf{j}$，$\mathbf{b} = 5\mathbf{i} + 6\mathbf{j}$，$\mathbf{c} = 9\mathbf{i} + 14\mathbf{j}$。

（a）证明 $A$、$B$、$C$ 三点共线。
（b）求 $AB:BC$ 的比值。

---

**13.3–13.4 题组：向量几何与运动**

**4.** 在 $\triangle OAB$ 中，$P$ 在 $OA$ 上且 $OP:PA = 1:2$，$Q$ 在 $AB$ 上且 $AQ:QB = 2:3$。设 $\overrightarrow{OA} = \mathbf{a}$，$\overrightarrow{OB} = \mathbf{b}$。

（a）用 $\mathbf{a}$ 和 $\mathbf{b}$ 表示 $\overrightarrow{OP}$。
（b）用 $\mathbf{a}$ 和 $\mathbf{b}$ 表示 $\overrightarrow{OQ}$。
（c）用 $\mathbf{a}$ 和 $\mathbf{b}$ 表示 $\overrightarrow{PQ}$。

---

**5.** 船 $A$ 从点 $(0, 5)$ 出发，以速度 $\mathbf{v}_A = (2\mathbf{i} + 3\mathbf{j})\,\text{km/h}$ 航行。船 $B$ 从点 $(10, 0)$ 出发，以速度 $\mathbf{v}_B = (-3\mathbf{i} + 4\mathbf{j})\,\text{km/h}$ 航行。两船同时出发。

（a）写出两船的位置向量 $\mathbf{r}_A(t)$ 和 $\mathbf{r}_B(t)$。
（b）判断两船是否会相撞。

---

**6.** 一艘船在静水中的速度为 $10\,\text{m/s}$，船头指向正北方向。水流的速度为 $6\,\text{m/s}$ 流向正东方向。

（a）求船相对于地面的合速度向量。
（b）求合速度的大小和方向（与正北方向的夹角）。

---

**14.1 题组：变化率入门**

**7.** 一个质点的位移 $s$（米）与时间 $t$（秒）的关系为 $s(t) = 4t^2 + 3t$。

（a）求从 $t = 1$ 到 $t = 1 + h$ 的平均速度。
（b）利用极限求 $t = 1$ 时的瞬时速度。

---

**8.** 一个质点在平面内运动，它的位置向量为：

$$
\mathbf{r}(t) = (2t^2 + t)\mathbf{i} + (3t - 1)\mathbf{j}
$$

（a）求速度向量 $\mathbf{v}(t)$。
（b）求加速度向量 $\mathbf{a}(t)$。
（c）求 $t = 2$ 时速度的大小。

---

**综合题**

**9.** 在平行四边形 $ABCD$ 中，$A$、$B$、$C$ 的位置向量分别为 $\mathbf{a} = 2\mathbf{i} + \mathbf{j}$，$\mathbf{b} = 5\mathbf{i} + 3\mathbf{j}$，$\mathbf{c} = 4\mathbf{i} + 6\mathbf{j}$。

（a）求 $D$ 的位置向量。
（b）判断 $\overrightarrow{AB}$ 与 $\overrightarrow{AD}$ 是否垂直。
（c）求平行四边形 $ABCD$ 的面积。

> 提示：平行四边形的面积 $= |\overrightarrow{AB}| \times |\overrightarrow{AD}| \times \sin\theta$，其中 $\theta$ 是两边的夹角。或者用行列式公式：面积 $= |x_1 y_2 - x_2 y_1|$，其中 $\overrightarrow{AB} = (x_1, y_1)$，$\overrightarrow{AD} = (x_2, y_2)$。

---

## 练习题答案

**1.**

（a）$\mathbf{a} + 2\mathbf{b} = (2\mathbf{i} - \mathbf{j}) + 2(\mathbf{i} + 3\mathbf{j}) = (2\mathbf{i} - \mathbf{j}) + (2\mathbf{i} + 6\mathbf{j}) = 4\mathbf{i} + 5\mathbf{j}$

（b）$2\mathbf{a} - \mathbf{b} = 2(2\mathbf{i} - \mathbf{j}) - (\mathbf{i} + 3\mathbf{j}) = (4\mathbf{i} - 2\mathbf{j}) - (\mathbf{i} + 3\mathbf{j}) = 3\mathbf{i} - 5\mathbf{j}$

$|2\mathbf{a} - \mathbf{b}| = \sqrt{3^2 + (-5)^2} = \sqrt{9 + 25} = \sqrt{34}$

（c）$3\mathbf{a} + \mathbf{b} = 3(2\mathbf{i} - \mathbf{j}) + (\mathbf{i} + 3\mathbf{j}) = (6\mathbf{i} - 3\mathbf{j}) + (\mathbf{i} + 3\mathbf{j}) = 7\mathbf{i}$

$|7\mathbf{i}| = 7$，所以单位向量 $= \frac{7\mathbf{i}}{7} = \mathbf{i}$

---

**2.**

（a）$\overrightarrow{BC} = \overrightarrow{BA} + \overrightarrow{AC} = -\overrightarrow{AB} + \overrightarrow{AC} = -\mathbf{p} + \mathbf{q}$

（b）$P$ 是 $BC$ 的中点，所以 $\mathbf{r}_P = \frac{\mathbf{r}_B + \mathbf{r}_C}{2}$。$Q$ 是 $CA$ 的中点，所以 $\mathbf{r}_Q = \frac{\mathbf{r}_C + \mathbf{r}_A}{2}$。

$$
\begin{aligned}
\overrightarrow{PQ} &= \mathbf{r}_Q - \mathbf{r}_P \\
&= \frac{\mathbf{r}_C + \mathbf{r}_A}{2} - \frac{\mathbf{r}_B + \mathbf{r}_C}{2} \\
&= \frac{\mathbf{r}_A - \mathbf{r}_B}{2} \\
&= \frac{1}{2}\overrightarrow{BA} = -\frac{1}{2}\overrightarrow{AB} = -\frac{1}{2}\mathbf{p}
\end{aligned}
$$

（c）由（b）得 $\overrightarrow{PQ} = -\frac{1}{2}\mathbf{p} = -\frac{1}{2}\overrightarrow{AB}$，所以 $\overrightarrow{PQ} \parallel \overrightarrow{AB}$ 且 $|\overrightarrow{PQ}| = \frac{1}{2}|\overrightarrow{AB}|$，即 $PQ = \frac{1}{2}AB$。✓

> 这条性质叫做**三角形中位线定理**：三角形两边中点的连线平行于第三边且等于第三边的一半。

---

**3.**

（a）

$$
\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (5\mathbf{i} + 6\mathbf{j}) - (3\mathbf{i} + 2\mathbf{j}) = 2\mathbf{i} + 4\mathbf{j}
$$

$$
\overrightarrow{BC} = \mathbf{c} - \mathbf{b} = (9\mathbf{i} + 14\mathbf{j}) - (5\mathbf{i} + 6\mathbf{j}) = 4\mathbf{i} + 8\mathbf{j}
$$

$\overrightarrow{BC} = 2(2\mathbf{i} + 4\mathbf{j}) = 2\overrightarrow{AB}$，存在 $k = 2$ 使得 $\overrightarrow{BC} = k\overrightarrow{AB}$，所以 $A$、$B$、$C$ 共线。

（b）$|\overrightarrow{AB}| = \sqrt{2^2 + 4^2} = \sqrt{4 + 16} = \sqrt{20} = 2\sqrt{5}$

$|\overrightarrow{BC}| = \sqrt{4^2 + 8^2} = \sqrt{16 + 64} = \sqrt{80} = 4\sqrt{5}$

所以 $AB:BC = 2\sqrt{5}:4\sqrt{5} = 1:2$

---

**4.**

（a）$OP:PA = 1:2$，所以 $OP:OA = 1:3$，即 $\overrightarrow{OP} = \frac{1}{3}\mathbf{a}$

（b）$AQ:QB = 2:3$，所以 $AQ:AB = 2:5$，$Q$ 从 $A$ 到 $B$ 的 $\frac{2}{5}$ 处。

$$
\begin{aligned}
\overrightarrow{OQ} &= \overrightarrow{OA} + \frac{2}{5}\overrightarrow{AB} \\
&= \mathbf{a} + \frac{2}{5}(\mathbf{b} - \mathbf{a}) \\
&= \mathbf{a} + \frac{2}{5}\mathbf{b} - \frac{2}{5}\mathbf{a} \\
&= \frac{3}{5}\mathbf{a} + \frac{2}{5}\mathbf{b}
\end{aligned}
$$

（c）

$$
\overrightarrow{PQ} = \overrightarrow{OQ} - \overrightarrow{OP} = \left(\frac{3}{5}\mathbf{a} + \frac{2}{5}\mathbf{b}\right) - \frac{1}{3}\mathbf{a} = \left(\frac{3}{5} - \frac{1}{3}\right)\mathbf{a} + \frac{2}{5}\mathbf{b}
$$

通分：$\frac{3}{5} - \frac{1}{3} = \frac{9}{15} - \frac{5}{15} = \frac{4}{15}$

所以 $\overrightarrow{PQ} = \frac{4}{15}\mathbf{a} + \frac{2}{5}\mathbf{b}$

---

**5.**

（a）

$$
\mathbf{r}_A(t) = \begin{pmatrix} 0 \\ 5 \end{pmatrix} + \begin{pmatrix} 2 \\ 3 \end{pmatrix} t = \begin{pmatrix} 2t \\ 5 + 3t \end{pmatrix}
$$

$$
\mathbf{r}_B(t) = \begin{pmatrix} 10 \\ 0 \end{pmatrix} + \begin{pmatrix} -3 \\ 4 \end{pmatrix} t = \begin{pmatrix} 10 - 3t \\ 4t \end{pmatrix}
$$

（b）令 $\mathbf{r}_A(t) = \mathbf{r}_B(t)$：

$$
\begin{cases}
2t = 10 - 3t \implies 5t = 10 \implies t = 2 \\[4pt]
5 + 3t = 4t \implies 5 = t \implies t = 5
\end{cases}
$$

两个 $t$ 值不相等（$2 \neq 5$），所以两船不会相撞。

---

**6.**

（a）设正北为 $+y$ 轴，正东为 $+x$ 轴。

船相对于水的速度：$\mathbf{v}_{B/W} = 10\mathbf{j}$
水相对于地面的速度：$\mathbf{v}_{W/G} = 6\mathbf{i}$

合速度：$\mathbf{v}_{B/G} = 6\mathbf{i} + 10\mathbf{j}$

（b）大小：$|\mathbf{v}_{B/G}| = \sqrt{6^2 + 10^2} = \sqrt{36 + 100} = \sqrt{136} = 2\sqrt{34} \approx 11.66\,\text{m/s}$

方向：设 $\theta$ 为与正北方向的夹角。

$$
\tan\theta = \frac{6}{10} = 0.6 \implies \theta = \arctan(0.6) \approx 30.96^\circ
$$

所以方向为东偏北 $30.96^\circ$（或北偏东 $59.04^\circ$）。

---

**7.**

（a）

$$
\begin{aligned}
\frac{s(1+h) - s(1)}{h} &= \frac{[4(1+h)^2 + 3(1+h)] - [4 + 3]}{h} \\
&= \frac{[4(1 + 2h + h^2) + 3 + 3h] - 7}{h} \\
&= \frac{4 + 8h + 4h^2 + 3 + 3h - 7}{h} \\
&= \frac{11h + 4h^2}{h} = 11 + 4h
\end{aligned}
$$

（b）$v(1) = \displaystyle\lim_{h \to 0} (11 + 4h) = 11\,\text{m/s}$

验证：$s'(t) = 8t + 3$，$s'(1) = 8 + 3 = 11$ ✓

---

**8.**

（a）$\mathbf{v}(t) = \dfrac{d\mathbf{r}}{dt} = (4t + 1)\mathbf{i} + 3\mathbf{j}$

（b）$\mathbf{a}(t) = \dfrac{d\mathbf{v}}{dt} = 4\mathbf{i}$

（c）$\mathbf{v}(2) = (4 \times 2 + 1)\mathbf{i} + 3\mathbf{j} = 9\mathbf{i} + 3\mathbf{j}$

$|\mathbf{v}(2)| = \sqrt{9^2 + 3^2} = \sqrt{81 + 9} = \sqrt{90} = 3\sqrt{10} \approx 9.49\,\text{m/s}$

---

**9.**

（a）平行四边形 $ABCD$ 中，$\overrightarrow{AD} = \overrightarrow{BC}$。

$$
\overrightarrow{BC} = \mathbf{c} - \mathbf{b} = (4\mathbf{i} + 6\mathbf{j}) - (5\mathbf{i} + 3\mathbf{j}) = -\mathbf{i} + 3\mathbf{j}
$$

所以 $\mathbf{d} = \mathbf{a} + \overrightarrow{BC} = (2\mathbf{i} + \mathbf{j}) + (-\mathbf{i} + 3\mathbf{j}) = \mathbf{i} + 4\mathbf{j}$

（b）$\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (5\mathbf{i} + 3\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = 3\mathbf{i} + 2\mathbf{j}$

$\overrightarrow{AD} = \mathbf{d} - \mathbf{a} = (\mathbf{i} + 4\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = -\mathbf{i} + 3\mathbf{j}$

点积：$\overrightarrow{AB} \cdot \overrightarrow{AD} = (3)(-1) + (2)(3) = -3 + 6 = 3 \neq 0$

所以 $\overrightarrow{AB}$ 与 $\overrightarrow{AD}$ **不垂直**。

（c）方法一（用叉积的行列式公式）：

$$
\text{面积} = |x_1 y_2 - x_2 y_1|
$$

其中 $\overrightarrow{AB} = (3, 2)$，$\overrightarrow{AD} = (-1, 3)$。

$$
\text{面积} = |3 \times 3 - 2 \times (-1)| = |9 + 2| = 11
$$

方法二（用 $|\overrightarrow{AB}| \cdot |\overrightarrow{AD}| \cdot \sin\theta$）：

$$
|\overrightarrow{AB}| = \sqrt{3^2 + 2^2} = \sqrt{13}, \quad |\overrightarrow{AD}| = \sqrt{(-1)^2 + 3^2} = \sqrt{10}
$$

由点积 $\overrightarrow{AB} \cdot \overrightarrow{AD} = |\overrightarrow{AB}||\overrightarrow{AD}|\cos\theta$：

$$
3 = \sqrt{13} \cdot \sqrt{10} \cdot \cos\theta \implies \cos\theta = \frac{3}{\sqrt{130}}
$$

$$
\sin\theta = \sqrt{1 - \cos^2\theta} = \sqrt{1 - \frac{9}{130}} = \sqrt{\frac{121}{130}} = \frac{11}{\sqrt{130}}
$$

$$
\text{面积} = \sqrt{13} \cdot \sqrt{10} \cdot \frac{11}{\sqrt{130}} = \sqrt{130} \cdot \frac{11}{\sqrt{130}} = 11
$$

平行四边形的面积为 $11$ 平方单位。✓

---

## 本章总结

### 考纲覆盖核对

| 考纲编号 | 内容 | 对应节次 | 例题 | 练习题 |
|:---:|------|:---:|:---:|:---:|
| 13.1 | 向量记号 | 2.1.1 | 2.1(1) | 1 |
| 13.2 | 位置向量与单位向量 | 2.1.2, 2.1.4 | 2.1(1) | 1(c) |
| 13.3 | 模、加减、数乘、向量几何 | 2.1.3, 2.1.5–2.1.8, 2.2.1 | 2.1, 2.2 | 1–4, 9 |
| 13.4 | 速度合成与分解、相撞问题 | 2.2.2 | 2.3 | 5, 6 |
| 14.1 | 变化率与极限思想 | 2.3 | 2.4 | 7, 8 |

### 核心公式速查表

**向量部分**：

| 概念 | 公式 |
|:---|:---|
| 向量表示 | $\mathbf{v} = x\mathbf{i} + y\mathbf{j} = \begin{pmatrix} x \\ y \end{pmatrix}$ |
| 模 | $|\mathbf{v}| = \sqrt{x^2 + y^2}$ |
| 单位向量 | $\hat{\mathbf{v}} = \dfrac{\mathbf{v}}{|\mathbf{v}|}$ |
| 位移 | $\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A$ |
| 中点 | $\mathbf{r}_M = \dfrac{\mathbf{r}_A + \mathbf{r}_B}{2}$ |
| 分点（$AP:PB = m:n$） | $\mathbf{r}_P = \dfrac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n}$ |
| 平行条件 | $\mathbf{a} = k\mathbf{b}$（存在标量 $k$） |
| 垂直条件（点积） | $\mathbf{u} \cdot \mathbf{v} = u_x v_x + u_y v_y = 0$ |
| 斜率法判垂直 | $k_1 \cdot k_2 = -1$ |
| 速度合成 | $\mathbf{v}_{A/C} = \mathbf{v}_{A/B} + \mathbf{v}_{B/C}$ |
| 速度分解 | $\mathbf{v} = (v\cos\theta)\mathbf{i} + (v\sin\theta)\mathbf{j}$ |
| 匀速直线运动 | $\mathbf{r}(t) = \mathbf{r}_0 + \mathbf{v}t$ |
| 相撞条件 | $\mathbf{r}_1(t) = \mathbf{r}_2(t)$ |

**变化率部分**：

| 概念 | 公式 |
|:---|:---|
| 导数定义 | $f'(a) = \displaystyle\lim_{h \to 0} \dfrac{f(a + h) - f(a)}{h}$ |
| 幂法则 | $\dfrac{d}{dx}(x^n) = n x^{n-1}$ |
| 速度（向量） | $\mathbf{v}(t) = \dfrac{d\mathbf{r}}{dt} = \dfrac{dx}{dt}\mathbf{i} + \dfrac{dy}{dt}\mathbf{j}$ |
| 加速度（向量） | $\mathbf{a}(t) = \dfrac{d\mathbf{v}}{dt} = \dfrac{d^2x}{dt^2}\mathbf{i} + \dfrac{d^2y}{dt^2}\mathbf{j}$ |
| 积分求速度 | $\mathbf{v}(t) = \int \mathbf{a}(t) \, dt + \mathbf{v}_0$ |
| 积分求位置 | $\mathbf{r}(t) = \int \mathbf{v}(t) \, dt + \mathbf{r}_0$ |

### 学习路线图

从本章出发，后续章节将这样深化你的理解：

- **第 5 章（微分）**：系统学习求导法则（链式法则、积法则、商法则），以及用导数求切线、法线和极值
- **第 7 章（积分）**：学习微分的逆运算——积分，掌握从加速度求速度和位置的完整方法
- **第 10 章（综合应用）**：将向量和微积分结合，解决完整的运动学问题

---
---

# 第 3 章：二次函数（含多项式因式）

## 本章引言

二次函数是 IGCSE 附加数学（0606）中贯穿始终的核心工具。从解方程到求极值，从不等式到曲线分析，二次函数的知识无处不在。本章将二次函数的概念体系与多项式因式有机结合，形成从"因式"到"函数"再到"图像"的完整逻辑链条。

**考纲对照表**：

| 考纲编号 | 内容 | 对应小节 |
|:---:|:---|:---:|
| **3.1** | 余数定理与因式定理 | §3.1.1, §3.1.2 |
| **3.2** | 分解多项式（三次 → 线性×二次） | §3.1.3 |
| **3.3** | 解三次方程 | §3.1.4 |
| **2.1** | 配方法或微分求二次函数极值 | §3.4, §3.7 |
| **2.2** | 利用最值画草图或求值域 | §3.4 |
| **2.3** | 判别式与根的条件、直线与曲线位置关系 | §3.2 |
| **2.4** | 解二次方程（因式分解、公式法、配方法） | §3.3 |
| **2.5** | 二次不等式（代数法或图像法） | §3.5 |
| **4.4** | 三个线性因式乘积的图像与绝对值图像 | §3.6.1, §3.6.2 |
| **4.5** | 三次不等式的图像解法 | §3.6.3 |

---

## 3.1 多项式的因式

### 3.1.1 余数定理

**定理陈述**：当多项式 $f(x)$ 除以线性因式 $(x - a)$ 时，余数等于 $f(a)$。

**完整推导**：

设 $f(x)$ 除以 $(x - a)$，得到商式 $q(x)$ 和余数 $R$。由于除式 $(x - a)$ 是一次式，余数 $R$ 的次数必须低于除式的次数，所以 $R$ 只能是一个常数。因此有恒等式：

$$
f(x) = (x - a) \cdot q(x) + R
$$

这个等式对**所有** $x$ 的值都成立——这是多项式恒等式的基本性质。

现在，我们巧妙地选择 $x = a$ 代入。之所以选 $x = a$，是因为这样可以使 $(x - a)$ 这一项变为零，从而消去包含 $q(x)$ 的项：

$$
f(a) = (a - a) \cdot q(a) + R = 0 \cdot q(a) + R = R
$$

因此 $R = f(a)$。这就是余数定理的全部内容。

**为什么这个定理如此有用？**

要得到余数，不需要做完整的长除法，只需要把 $x = a$ 代入原多项式计算即可。这大大简化了计算，尤其是当多项式次数较高时。

**推广形式**：

如果除式是 $(ax + b)$，则令 $ax + b = 0$ 解出 $x = -\frac{b}{a}$，余数为：

$$
R = f\!\left(-\frac{b}{a}\right)
$$

思路完全相同——找到使除式为零的 $x$ 值后代入。

---

**例题 1**：多项式 $f(x) = 2x^3 - 3x^2 + 4x - 5$ 除以 $x - 2$，求余数。

**详解**：

除式为 $x - 2$，令 $x - 2 = 0$ 得 $x = 2$。由余数定理，余数 $R = f(2)$。

代入计算，逐项进行：

$$
\begin{aligned}
f(2) &= 2(2)^3 - 3(2)^2 + 4(2) - 5 \\
&\text{（先算乘方：$2^3 = 8$，$2^2 = 4$）} \\
&= 2 \times 8 - 3 \times 4 + 8 - 5 \\
&\text{（再算乘法：$2 \times 8 = 16$，$3 \times 4 = 12$）} \\
&= 16 - 12 + 8 - 5 \\
&= 7
\end{aligned}
$$

所以余数为 $7$。

---

**例题 2**：多项式 $f(x) = x^3 + kx^2 - 2x + 3$ 除以 $x + 1$ 余数为 $5$，求常数 $k$ 的值。

**详解**：

除式为 $x + 1$，令 $x + 1 = 0$ 得 $x = -1$。注意这里的符号：$x + 1 = 0$ 的解是 $x = -1$，不是 $x = 1$。这是一个常见的易错点。

由余数定理，余数等于 $f(-1)$，题目已知余数为 5，所以 $f(-1) = 5$。

代入计算：

$$
\begin{aligned}
f(-1) &= (-1)^3 + k(-1)^2 - 2(-1) + 3 = 5 \\
&\text{（逐项计算：$(-1)^3 = -1$，$(-1)^2 = 1$，$-2(-1) = 2$）} \\
-1 + k + 2 + 3 &= 5 \\
k + 4 &= 5 \\
k &= 1
\end{aligned}
$$

所以 $k = 1$。

---

**例题 3**：多项式 $f(x) = 6x^3 + x^2 - 8x + 2$ 除以 $2x - 1$，求余数。

**详解**：

除式是 $2x - 1$，不是简单的 $(x - a)$ 形式。令 $2x - 1 = 0$，解得 $x = \frac{1}{2}$。

代入 $x = \frac{1}{2}$ 时，注意分数运算的准确性：

$$
\begin{aligned}
f\!\left(\frac{1}{2}\right) &= 6\left(\frac{1}{2}\right)^3 + \left(\frac{1}{2}\right)^2 - 8\left(\frac{1}{2}\right) + 2 \\
&= 6 \times \frac{1}{8} + \frac{1}{4} - 4 + 2 \\
&= \frac{6}{8} + \frac{1}{4} - 2 \\
&= \frac{3}{4} + \frac{1}{4} - 2 \\
&= 1 - 2 = -1
\end{aligned}
$$

所以余数为 $-1$。

---

**例题 4**：多项式 $f(x) = 4x^4 - 3x^3 + 2x^2 - x + 5$ 除以 $x - 1$，求余数。

**详解**：

令 $x - 1 = 0$ 得 $x = 1$。余数 $R = f(1)$。

$$
\begin{aligned}
f(1) &= 4(1)^4 - 3(1)^3 + 2(1)^2 - 1 + 5 \\
&= 4 - 3 + 2 - 1 + 5 \\
&= 7
\end{aligned}
$$

余数为 $7$。即使多项式次数更高，余数定理仍然适用。

---

**例题 5**：多项式 $f(x) = x^4 - 2x^3 + 3x^2 - 4x + 2$ 除以 $x + 2$，求余数。

**详解**：

令 $x + 2 = 0$ 得 $x = -2$。

$$
\begin{aligned}
f(-2) &= (-2)^4 - 2(-2)^3 + 3(-2)^2 - 4(-2) + 2 \\
&= 16 - 2(-8) + 3(4) + 8 + 2 \\
&= 16 + 16 + 12 + 8 + 2 \\
&= 54
\end{aligned}
$$

余数为 $54$。

---

**例题 6**：多项式 $f(x) = 8x^3 - 4x^2 + 2x - 1$ 除以 $2x + 3$，求余数。

**详解**：

令 $2x + 3 = 0$ 得 $x = -\frac{3}{2}$。余数 $R = f\!\left(-\frac{3}{2}\right)$。

$$
\begin{aligned}
f\!\left(-\frac{3}{2}\right) &= 8\left(-\frac{3}{2}\right)^3 - 4\left(-\frac{3}{2}\right)^2 + 2\left(-\frac{3}{2}\right) - 1 \\
&= 8\left(-\frac{27}{8}\right) - 4\left(\frac{9}{4}\right) - 3 - 1 \\
&= -27 - 9 - 3 - 1 = -40
\end{aligned}
$$

余数为 $-40$。

---

### 3.1.2 因式定理

**定理陈述**：如果 $f(a) = 0$，那么 $(x - a)$ 是 $f(x)$ 的一个因式。反之，如果 $(x - a)$ 是 $f(x)$ 的一个因式，那么 $f(a) = 0$。

**推导**：

因式定理是余数定理的直接推论。由余数定理，$f(x)$ 除以 $(x - a)$ 的余数等于 $f(a)$。如果 $f(a) = 0$，意味着余数为零——也就是说 $(x - a)$ **完全整除** $f(x)$，没有余数，所以 $(x - a)$ 是 $f(x)$ 的一个因式。

反过来，如果 $(x - a)$ 是 $f(x)$ 的因式，那么 $f(x) = (x - a) \cdot q(x)$，代入 $x = a$ 得 $f(a) = 0$。

**实际意义**：

要判断 $(x - a)$ 是不是 $f(x)$ 的因式，只需要看 $f(a)$ 是否等于 0。这比做长除法快得多。同时，因式定理是**分解三次多项式的起点**——通过试根找到一个零点，就等于找到了一个线性因式。

**试根策略**：

对于整系数多项式，可能的有理根为 $\pm \frac{\text{常数项的因数}}{\text{首项系数的因数}}$。对于三次多项式，通常从最简单的 $\pm 1, \pm 2, \pm 3$ 开始试。

---

**例题 1**：证明 $(x - 2)$ 是 $f(x) = x^3 - 3x^2 - 4x + 12$ 的一个因式。

**详解**：

要证明 $(x - 2)$ 是因式，由因式定理，只需证明 $f(2) = 0$。

$$
\begin{aligned}
f(2) &= 2^3 - 3(2)^2 - 4(2) + 12 \\
&= 8 - 12 - 8 + 12 = 0
\end{aligned}
$$

因为 $f(2) = 0$，所以 $(x - 2)$ 是 $f(x)$ 的一个因式。✓

---

**例题 2**：多项式 $f(x) = 2x^3 + ax^2 + bx - 6$ 有因式 $(x - 1)$ 和 $(x + 2)$，求 $a$ 和 $b$ 的值。

**详解**：

由因式定理：
- $(x - 1)$ 是因式 $\Rightarrow$ $f(1) = 0$
- $(x + 2)$ 是因式 $\Rightarrow$ $f(-2) = 0$

由 $f(1) = 0$：

$$
2 + a + b - 6 = 0 \;\Rightarrow\; a + b = 4 \tag{1}
$$

由 $f(-2) = 0$：

$$
-16 + 4a - 2b - 6 = 0 \;\Rightarrow\; 4a - 2b = 22 \tag{2}
$$

联立 (1)(2)：由 (1) 得 $b = 4 - a$，代入 (2)：

$$
4a - 2(4 - a) = 22 \;\Rightarrow\; 4a - 8 + 2a = 22 \;\Rightarrow\; 6a = 30 \;\Rightarrow\; a = 5
$$

所以 $b = 4 - 5 = -1$。

---

**例题 3**：已知 $x - 2$ 是 $f(x) = x^3 - px^2 + 5x - 2$ 的一个因式，求 $p$ 的值并将 $f(x)$ 完全因式分解。

**详解**：

由因式定理，$f(2) = 0$：

$$
8 - 4p + 10 - 2 = 16 - 4p = 0 \;\Rightarrow\; p = 4
$$

所以 $f(x) = x^3 - 4x^2 + 5x - 2$。

用综合除法除以 $(x - 2)$：

$$
\begin{array}{r|rrrr}
2 & 1 & -4 & 5 & -2 \\
  &   & 2  & -4 & 2 \\
\hline
  & 1 & -2 & 1 & 0
\end{array}
$$

商式为 $x^2 - 2x + 1 = (x - 1)^2$。

因此：

$$
\boxed{f(x) = (x - 2)(x - 1)^2}
$$

---

**例题 4**：已知 $x - 3$ 是 $f(x) = 2x^3 - 7x^2 + 2x + 3$ 的一个因式，将 $f(x)$ 分解。

**详解**：

综合除法：

$$
\begin{array}{r|rrrr}
3 & 2 & -7 & 2 & 3 \\
  &   & 6  & -3 & -3 \\
\hline
  & 2 & -1 & -1 & 0
\end{array}
$$

商式为 $2x^2 - x - 1$。

分解二次式：$2x^2 - x - 1 = 2x^2 - 2x + x - 1 = 2x(x - 1) + 1(x - 1) = (2x + 1)(x - 1)$。

因此：

$$
\boxed{f(x) = (x - 3)(2x + 1)(x - 1)}
$$

---

**例题 5**：多项式 $f(x) = 3x^3 + kx^2 - 4x + 4$ 有因式 $(x + 1)$，求 $k$ 的值。

**详解**：

$(x + 1)$ 是因式 $\Rightarrow$ $f(-1) = 0$。

$$
f(-1) = -3 + k + 4 + 4 = k + 5 = 0 \;\Rightarrow\; k = -5
$$

---

**例题 6**：已知 $x - 1$ 和 $x - 2$ 都是 $f(x) = x^3 + ax^2 + bx + c$ 的因式，且 $f(x)$ 除以 $x + 1$ 余数为 $-12$，求 $a, b, c$ 的值并写出 $f(x)$ 的完整因式分解。

**详解**：

由已知条件：

$$
\begin{aligned}
f(1) &= 1 + a + b + c = 0 &\Rightarrow\quad a + b + c = -1 \tag{1}\\
f(2) &= 8 + 4a + 2b + c = 0 &\Rightarrow\quad 4a + 2b + c = -8 \tag{2}\\
f(-1) &= -1 + a - b + c = -12 &\Rightarrow\quad a - b + c = -11 \tag{3}
\end{aligned}
$$

(2) - (1)：$3a + b = -7 \tag{4}$
(1) - (3)：$2b = 10 \Rightarrow b = 5$

代入 (4)：$3a + 5 = -7 \Rightarrow 3a = -12 \Rightarrow a = -4$

代入 (1)：$-4 + 5 + c = -1 \Rightarrow c = -2$

所以 $f(x) = x^3 - 4x^2 + 5x - 2$。

验证：
- $f(1) = 1 - 4 + 5 - 2 = 0$ ✓
- $f(2) = 8 - 16 + 10 - 2 = 0$ ✓
- $f(-1) = -1 - 4 - 5 - 2 = -12$ ✓

用综合除法除以 $(x - 1)$：

$$
\begin{array}{r|rrrr}
1 & 1 & -4 & 5 & -2 \\
  &   & 1  & -3 & 2 \\
\hline
  & 1 & -3 & 2 & 0
\end{array}
$$

商式为 $x^2 - 3x + 2 = (x - 1)(x - 2)$。

所以 $f(x) = (x - 1)^2(x - 2)$。

---

### 3.1.3 分解三次多项式

分解三次多项式 $f(x) = ax^3 + bx^2 + cx + d$ 就像解一个"三层锁"：先找到一把钥匙（一个线性因式），打开第一层锁后露出一个二次锁，再用熟悉的二次分解方法打开它。

**标准流程**：

**Step 1：试根——用因式定理找线性因式**

试 $x = \pm 1, \pm 2, \pm 3, \dots$ 以及分数 $\pm \frac{\text{常数项的因数}}{\text{首项系数的因数}}$。找到 $p$ 使得 $f(p) = 0$，则 $(x - p)$ 是一个因式。

**Step 2：综合除法——求二次商式**

将 $f(x)$ 除以 $(x - p)$，得到二次式 $Ax^2 + Bx + C$。

**Step 3：分解二次式**

用因式分解、求根公式或配方法分解 $Ax^2 + Bx + C$。

**Step 4：完整因式分解**

写出 $f(x) = (x - p) \times (\text{二次因式的分解})$。

---

#### 综合除法详解

综合除法是一种简洁的多项式除法格式，只处理系数，不写变量。

**步骤**（以 $f(x) = a_3 x^3 + a_2 x^2 + a_1 x + a_0$ 除以 $(x - p)$ 为例）：

```
p |  a₃   a₂   a₁   a₀
  |      p·b₂ p·b₁ p·b₀
  ------------------------
     b₂   b₁   b₀   R
```

其中：
- $b_2 = a_3$（下拉首项系数）
- $b_1 = a_2 + p \cdot b_2$
- $b_0 = a_1 + p \cdot b_1$
- $R = a_0 + p \cdot b_0$（余数）

商式为 $b_2 x^2 + b_1 x + b_0$，余数为 $R$。

---

**例题 1**：分解 $f(x) = x^3 - 6x^2 + 11x - 6$。

**详解**：

**Step 1：试根**。从最简单的 $x = 1$ 开始试：

$$
f(1) = 1 - 6 + 11 - 6 = 0
$$

所以 $(x - 1)$ 是一个因式。

**Step 2：综合除法**。

```
    1 |  1   -6   11   -6
      |      1   -5    6
      -------------------
         1   -5    6    0
```

**详细过程说明**：
- 将系数 $1, -6, 11, -6$ 依次排开。
- 最左边的数字 $1$ 来自 $(x - 1)$ 的根 $x = 1$。
- **下拉**：首项系数 $1$ 直接写到下面。
- **第 1 步**：$1 \times 1 = 1$，写到第二行第二个位置。$-6 + 1 = -5$ 写到下面。
- **第 2 步**：$(-5) \times 1 = -5$，写到第二行第三个位置。$11 + (-5) = 6$ 写到下面。
- **第 3 步**：$6 \times 1 = 6$，写到第二行第四个位置。$-6 + 6 = 0$ 写到下面。

下面第三行的数字 $1, -5, 6, 0$ 的含义：
- $1, -5, 6$ 是商式的系数：$1x^2 - 5x + 6$
- 最后的 $0$ 是余数——为 0 说明整除，验证了 $(x - 1)$ 确实为因式。

**Step 3：分解二次式**。

$$
x^2 - 5x + 6 = (x - 2)(x - 3)
$$

找到两个数乘积为 $6$、和为 $-5$：$-2$ 和 $-3$。

**Step 4：完整分解**。

$$
\boxed{f(x) = (x - 1)(x - 2)(x - 3)}
$$

---

**例题 2**：分解 $f(x) = 2x^3 - 3x^2 - 11x + 6$。

**详解**：

**Step 1：试根**。

首项系数为 2，常数项为 6，可能的有理根为 $\pm 1, \pm 2, \pm 3, \pm 6, \pm \frac{1}{2}, \pm \frac{3}{2}$。

试 $x = 2$：$f(2) = 16 - 12 - 22 + 6 = -12 \neq 0$。
试 $x = -2$：

$$
f(-2) = -16 - 12 + 22 + 6 = 0
$$

所以 $(x + 2)$ 是一个因式（注意 $x = -2$ 对应 $x + 2 = 0$）。

**Step 2：综合除法**。

```
    -2 |  2   -3   -11    6
       |     -4    14    -6
       --------------------
          2   -7     3    0
```

**过程说明**：
- 最左边是 $-2$（根的值）。
- 下拉 $2$。
- $2 \times (-2) = -4$，$-3 + (-4) = -7$。
- $(-7) \times (-2) = 14$，$-11 + 14 = 3$。
- $3 \times (-2) = -6$，$6 + (-6) = 0$。

商式为 $2x^2 - 7x + 3$。

**Step 3：分解二次式 $2x^2 - 7x + 3$**。

$a \times c = 2 \times 3 = 6$。找两个数乘积为 $6$、和为 $-7$：$(-1) \times (-6) = 6$，$(-1) + (-6) = -7$。

拆分并分组：

$$
\begin{aligned}
2x^2 - 7x + 3 &= 2x^2 - x - 6x + 3 \\
&= x(2x - 1) - 3(2x - 1) \\
&= (2x - 1)(x - 3)
\end{aligned}
$$

**Step 4：完整分解**。

$$
\boxed{f(x) = (x + 2)(2x - 1)(x - 3)}
$$

---

**例题 3**：分解 $f(x) = 3x^3 + 6x^2 - 3x - 6$。

**详解**：

**Step 0 观察**：所有系数都能被 3 整除，先提取公因式 3：

$$
f(x) = 3(x^3 + 2x^2 - x - 2)
$$

令 $g(x) = x^3 + 2x^2 - x - 2$。

**Step 1：试根**。试 $x = 1$：$g(1) = 1 + 2 - 1 - 2 = 0$。所以 $(x - 1)$ 是 $g(x)$ 的因式。

**Step 2：综合除法**。

```
    1 |  1    2   -1   -2
      |       1    3    2
      --------------------
         1    3    2    0
```

商式为 $x^2 + 3x + 2$。

**Step 3：分解二次式**。

$$
x^2 + 3x + 2 = (x + 1)(x + 2)
$$

**Step 4：完整分解**。

$$
\boxed{f(x) = 3(x - 1)(x + 1)(x + 2)}
$$

---

**例题 4**：分解 $f(x) = 2x^3 - 9x^2 + 7x + 6$。

**详解**：

**Step 1：试根**。

试 $x = 1$：$f(1) = 2 - 9 + 7 + 6 = 6 \neq 0$。
试 $x = -1$：$f(-1) = -2 - 9 - 7 + 6 = -12 \neq 0$。
试 $x = 2$：$f(2) = 16 - 36 + 14 + 6 = 0$。✓

所以 $(x - 2)$ 是一个因式。

**Step 2：综合除法**。

```
    2 |  2   -9    7    6
      |       4  -10   -6
      --------------------
         2   -5   -3    0
```

商式为 $2x^2 - 5x - 3$。

**Step 3：分解二次式 $2x^2 - 5x - 3$**。

$a \times c = 2 \times (-3) = -6$。找两个数乘积为 $-6$、和为 $-5$：$(-6) \times 1 = -6$，$(-6) + 1 = -5$。

$$
2x^2 - 6x + x - 3 = 2x(x - 3) + 1(x - 3) = (2x + 1)(x - 3)
$$

**Step 4：完整分解**。

$$
\boxed{f(x) = (x - 2)(2x + 1)(x - 3)}
$$

---

**例题 5**：分解 $f(x) = 6x^3 - 7x^2 - 7x + 6$。

**详解**：

**Step 1：试根**。

试 $x = 1$：$f(1) = 6 - 7 - 7 + 6 = -2 \neq 0$。
试 $x = -1$：$f(-1) = -6 - 7 + 7 + 6 = 0$。✓

所以 $(x + 1)$ 是一个因式。

**Step 2：综合除法**。

```
    -1 |  6   -7   -7    6
       |     -6   13   -6
       --------------------
          6  -13    6    0
```

商式为 $6x^2 - 13x + 6$。

**Step 3：分解二次式 $6x^2 - 13x + 6$**。

$a \times c = 6 \times 6 = 36$。找两个数乘积为 $36$、和为 $-13$：$(-9) \times (-4) = 36$，$(-9) + (-4) = -13$。

$$
6x^2 - 9x - 4x + 6 = 3x(2x - 3) - 2(2x - 3) = (3x - 2)(2x - 3)
$$

**Step 4：完整分解**。

$$
\boxed{f(x) = (x + 1)(3x - 2)(2x - 3)}
$$

---

**例题 6**：分解 $f(x) = x^3 + 2x^2 - 5x - 6$。

**详解**：

**Step 1：试根**。

试 $x = 1$：$f(1) = 1 + 2 - 5 - 6 = -8 \neq 0$。
试 $x = -1$：$f(-1) = -1 + 2 + 5 - 6 = 0$。✓

所以 $(x + 1)$ 是一个因式。

**Step 2：综合除法**。

```
    -1 |  1    2   -5   -6
       |     -1   -1    6
       --------------------
          1    1   -6    0
```

商式为 $x^2 + x - 6$。

**Step 3：分解二次式**。

$$
x^2 + x - 6 = (x + 3)(x - 2)
$$

**Step 4：完整分解**。

$$
\boxed{f(x) = (x + 1)(x + 3)(x - 2)}
$$

---

### 3.1.4 解三次方程

解三次方程 $ax^3 + bx^2 + cx + d = 0$ 的流程就是**将三次多项式分解因式，然后令每个因式等于零**。因为如果几个因式的乘积为零，则至少其中一个因式为零。

---

**例题 1**：解 $x^3 - 4x^2 + x + 6 = 0$。

**详解**：

试根：$f(2) = 8 - 16 + 2 + 6 = 0$，所以 $(x - 2)$ 是因式。

综合除法：

```
    2 |  1   -4    1    6
      |       2   -4   -6
      --------------------
         1   -2   -3    0
```

商式 $x^2 - 2x - 3 = (x - 3)(x + 1)$。

所以 $(x - 2)(x - 3)(x + 1) = 0$。

解得：

$$
\boxed{x = 2,\quad x = 3,\quad x = -1}
$$

---

**例题 2**：解 $x^3 - 5x^2 + 8x - 4 = 0$。

**详解**：

试 $x = 1$：$f(1) = 1 - 5 + 8 - 4 = 0$。

综合除法：

```
    1 |  1   -5    8   -4
      |       1   -4    4
      --------------------
         1   -4    4    0
```

商式 $x^2 - 4x + 4 = (x - 2)^2$。

所以 $(x - 1)(x - 2)^2 = 0$。

解得：

$$
\boxed{x = 1 \quad\text{或}\quad x = 2\ (\text{二重根})}
$$

---

**例题 3**：已知 $x = 2$ 是 $2x^3 - 3x^2 - 18x + k = 0$ 的一个根，求 $k$ 并解此方程。

**详解**：

代入 $x = 2$：$16 - 12 - 36 + k = -32 + k = 0 \Rightarrow k = 32$。

方程为 $2x^3 - 3x^2 - 18x + 32 = 0$。已知 $(x - 2)$ 是因式。

综合除法：

```
    2 |  2   -3   -18   32
      |       4     2   -32
      ----------------------
         2    1   -16    0
```

商式 $2x^2 + x - 16$。用求根公式：

$$
x = \frac{-1 \pm \sqrt{1 + 128}}{4} = \frac{-1 \pm \sqrt{129}}{4}
$$

所以解为：

$$
\boxed{x = 2,\quad x = \frac{-1 + \sqrt{129}}{4},\quad x = \frac{-1 - \sqrt{129}}{4}}
$$

---

**例题 4**：解 $x^3 - 2x^2 - 5x + 6 = 0$。

**详解**：

试 $x = 1$：$f(1) = 1 - 2 - 5 + 6 = 0$。✓

综合除法：

```
    1 |  1   -2   -5    6
      |       1   -1   -6
      --------------------
         1   -1   -6    0
```

商式 $x^2 - x - 6 = (x - 3)(x + 2)$。

所以 $(x - 1)(x - 3)(x + 2) = 0$。

解得：

$$
\boxed{x = 1,\quad x = 3,\quad x = -2}
$$

---

**例题 5**：解 $2x^3 - x^2 - 13x - 6 = 0$。

**详解**：

试 $x = -1$：$f(-1) = -2 - 1 + 13 - 6 = 4 \neq 0$。
试 $x = -2$：$f(-2) = -16 - 4 + 26 - 6 = 0$。✓

综合除法：

```
    -2 |  2   -1   -13   -6
       |     -4    10    6
       ---------------------
          2   -5    -3    0
```

商式 $2x^2 - 5x - 3 = (2x + 1)(x - 3)$。

所以 $(x + 2)(2x + 1)(x - 3) = 0$。

解得：

$$
\boxed{x = -2,\quad x = -\frac{1}{2},\quad x = 3}
$$

---

**例题 6**：已知 $x = 3$ 是 $x^3 + 4x^2 - 11x + k = 0$ 的一个根，求 $k$ 并解此方程。

**详解**：

代入 $x = 3$：$27 + 36 - 33 + k = 30 + k = 0 \Rightarrow k = -30$。

方程为 $x^3 + 4x^2 - 11x - 30 = 0$。已知 $(x - 3)$ 是因式。

综合除法：

```
    3 |  1    4   -11   -30
      |       3    21    30
      ---------------------
         1    7    10     0
```

商式 $x^2 + 7x + 10 = (x + 2)(x + 5)$。

所以 $(x - 3)(x + 2)(x + 5) = 0$。

解得：

$$
\boxed{x = 3,\quad x = -2,\quad x = -5}
$$

---

## 3.2 判别式 $\Delta$

### 3.2.1 判别式的定义与三种情况

对于一元二次方程 $ax^2 + bx + c = 0$（$a \neq 0$），求根公式为：

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

根号内的表达式 $b^2 - 4ac$ 决定了根的性质。我们定义**判别式**：

$$
\boxed{\Delta = b^2 - 4ac}
$$

**为什么 $\Delta$ 能决定根的情况？**

| $\Delta$ 的值 | $\sqrt{\Delta}$ 的情况 | 根的情况 |
|:---:|:---|:---|
| $\Delta > 0$ | $\sqrt{\Delta}$ 是正实数 | $\frac{-b \pm \text{正数}}{2a}$，两个不同的根 |
| $\Delta = 0$ | $\sqrt{\Delta} = 0$ | $\frac{-b \pm 0}{2a} = -\frac{b}{2a}$，一个重根 |
| $\Delta < 0$ | $\sqrt{\Delta}$ 在实数范围内无意义 | 无实数根 |

---

**例题 1**：判断下列方程的根的情况：
(a) $2x^2 - 3x + 1 = 0$
(b) $4x^2 - 4x + 1 = 0$
(c) $3x^2 + 2x + 5 = 0$

**详解**：

(a) $\Delta = (-3)^2 - 4(2)(1) = 9 - 8 = 1 > 0$，两个不等实根。

(b) $\Delta = (-4)^2 - 4(4)(1) = 16 - 16 = 0$，重根。

(c) $\Delta = 2^2 - 4(3)(5) = 4 - 60 = -56 < 0$，无实根。

---

**例题 2**：方程 $x^2 + kx + 4 = 0$ 有重根，求 $k$。

**详解**：

$\Delta = k^2 - 16 = 0 \Rightarrow k = \pm 4$。

---

**例题 3**：方程 $2x^2 - 3x + k = 0$ 有两个不等实根，求 $k$ 的范围。

**详解**：

$\Delta = 9 - 8k > 0 \Rightarrow k < \frac{9}{8}$。

---

**例题 4**：方程 $x^2 - 2x + (k - 3) = 0$ 无实根，求 $k$ 的范围。

**详解**：

$\Delta = (-2)^2 - 4(1)(k - 3) = 4 - 4k + 12 = 16 - 4k < 0 \Rightarrow 4k > 16 \Rightarrow k > 4$。

---

**例题 5**：方程 $kx^2 + 3x + 2 = 0$ 有重根，求 $k$ 的值。

**详解**：

注意 $k$ 是二次项系数，$k \neq 0$。

$\Delta = 9 - 8k = 0 \Rightarrow k = \frac{9}{8}$。

---

**例题 6**：方程 $3x^2 - 4x + k = 0$ 有两个不等实根，求 $k$ 的范围。

**详解**：

$\Delta = 16 - 12k > 0 \Rightarrow k < \frac{4}{3}$。

---

### 3.2.2 直线与曲线的位置关系

将直线 $y = mx + c$ 代入曲线消去 $y$，得到关于 $x$ 的二次方程：

| $\Delta$ 的值 | 交点个数 | 位置关系 |
|:---:|:---:|:---|
| $\Delta > 0$ | 2 个 | 相交于两点 |
| $\Delta = 0$ | 1 个 | 相切 |
| $\Delta < 0$ | 0 个 | 不相交 |

---

**例题 1**：判断 $y = 2x + 1$ 与 $y = x^2 - 3x + 4$ 的位置关系。

代入得 $x^2 - 5x + 3 = 0$，$\Delta = 25 - 12 = 13 > 0$，相交于两点。

---

**例题 2**：求 $k$ 使 $y = 3x + k$ 与 $y = x^2 - x + 2$ 相切。

代入得 $x^2 - 4x + (2 - k) = 0$，$\Delta = 16 - 4(2 - k) = 8 + 4k = 0 \Rightarrow k = -2$。

---

**例题 3**：求 $c$ 使 $y = x + c$ 与 $y = 2x^2 - 3x + 1$ 不相交。

代入得 $2x^2 - 4x + (1 - c) = 0$，$\Delta = 16 - 8(1 - c) = 8 + 8c < 0 \Rightarrow c < -1$。

---

**例题 4**：求 $k$ 使直线 $y = 2x + k$ 与曲线 $y = x^2 - 2x + 3$ 相交于两点。

代入得 $x^2 - 4x + (3 - k) = 0$，$\Delta = 16 - 4(3 - k) = 4 + 4k > 0 \Rightarrow k > -1$。

---

**例题 5**：直线 $y = mx + 1$ 与曲线 $y = x^2 - 3x + 5$ 相切，求 $m$。

代入得 $x^2 - (m + 3)x + 4 = 0$。

$\Delta = (m + 3)^2 - 16 = 0 \Rightarrow (m + 3)^2 = 16 \Rightarrow m + 3 = \pm 4 \Rightarrow m = 1$ 或 $m = -7$。

---

**例题 6**：求 $c$ 使直线 $y = 5x + c$ 与曲线 $y = x^2 + x + 2$ 相切。

代入得 $x^2 + x + 2 = 5x + c \Rightarrow x^2 - 4x + (2 - c) = 0$。

$\Delta = 16 - 4(2 - c) = 8 + 4c = 0 \Rightarrow c = -2$。

---

## 3.3 解二次方程

解二次方程 $ax^2 + bx + c = 0$ 有三种核心方法：

| 方法 | 适用场景 | 优点 | 缺点 |
|:---|:---|:---|:---|
| **因式分解法** | 表达式容易分解 | 最快，答案精确 | 并非所有二次式都可分解 |
| **公式法** | 任何情况 | 万能，按部就班 | 计算稍繁，可能含根号 |
| **配方法** | 需要顶点形式时 | 同时得到极值信息 | 步骤稍多 |

---

### 3.3.1 因式分解法

**核心原理**：若 $A \times B = 0$，则 $A = 0$ 或 $B = 0$。

**对于 $x^2 + bx + c = 0$（首项系数为 1）**：

找 $p, q$ 满足 $p + q = b$ 且 $pq = c$，则 $x^2 + bx + c = (x + p)(x + q)$。

因为 $(x + p)(x + q) = x^2 + (p + q)x + pq$。

**对于 $ax^2 + bx + c = 0$（首项系数不为 1）**：

找 $p, q$ 满足 $pq = ac$ 且 $p + q = b$，拆分中间项后分组提取公因式。

---

**例题 1**：解 $x^2 - 5x + 6 = 0$。

找 $p+q=-5$，$pq=6$：$(-2)+(-3)=-5$，$(-2)\times(-3)=6$。

$(x-2)(x-3)=0 \Rightarrow x=2$ 或 $x=3$。

---

**例题 2**：解 $2x^2 - 5x - 3 = 0$。

$ac = 2\times(-3)=-6$，找 $p+q=-5$，$pq=-6$：$(-6)+1=-5$，$(-6)\times1=-6$。

拆分：$2x^2-6x+x-3 = 2x(x-3)+1(x-3) = (2x+1)(x-3)$。

$x=-\frac{1}{2}$ 或 $x=3$。

---

**例题 3**：解 $3x^2 + 2 = 7x$。

移项：$3x^2 - 7x + 2 = 0$。$ac=6$，$(-6)+(-1)=-7$，$(-6)\times(-1)=6$。

$3x^2-6x-x+2 = 3x(x-2)-1(x-2) = (3x-1)(x-2)$。

$x=\frac{1}{3}$ 或 $x=2$。

---

**例题 4**：解 $x^2 + x - 12 = 0$。

找 $p+q=1$，$pq=-12$：$4+(-3)=1$，$4\times(-3)=-12$。

$(x+4)(x-3)=0 \Rightarrow x=-4$ 或 $x=3$。

---

**例题 5**：解 $6x^2 - 5x - 6 = 0$。

$ac = 6\times(-6)=-36$，找 $p+q=-5$，$pq=-36$：$(-9)+4=-5$，$(-9)\times4=-36$。

$6x^2-9x+4x-6 = 3x(2x-3)+2(2x-3) = (3x+2)(2x-3)$。

$x=-\frac{2}{3}$ 或 $x=\frac{3}{2}$。

---

**例题 6**：解 $4x^2 + 4x = 3$。

移项：$4x^2 + 4x - 3 = 0$。$ac = 4\times(-3)=-12$，找 $p+q=4$，$pq=-12$：$6+(-2)=4$，$6\times(-2)=-12$。

$4x^2+6x-2x-3 = 2x(2x+3)-1(2x+3) = (2x-1)(2x+3)$。

$x=\frac{1}{2}$ 或 $x=-\frac{3}{2}$。

---

### 3.3.2 公式法

**求根公式**：

$$
\boxed{x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}}
$$

**完整推导**（配方法）：

$$
\begin{aligned}
ax^2 + bx + c &= 0 \\
x^2 + \frac{b}{a}x + \frac{c}{a} &= 0 \quad (\text{两边除以 } a) \\
x^2 + \frac{b}{a}x &= -\frac{c}{a} \quad (\text{移项}) \\
x^2 + \frac{b}{a}x + \left(\frac{b}{2a}\right)^2 &= \left(\frac{b}{2a}\right)^2 - \frac{c}{a} \quad (\text{配方}) \\
\left(x + \frac{b}{2a}\right)^2 &= \frac{b^2 - 4ac}{4a^2} \\
x + \frac{b}{2a} &= \pm \frac{\sqrt{b^2 - 4ac}}{2a} \\
x &= \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\end{aligned}
$$

---

**例题 1**：解 $2x^2 - 3x - 4 = 0$。

$a=2, b=-3, c=-4$。

$$
x = \frac{3 \pm \sqrt{9 + 32}}{4} = \frac{3 \pm \sqrt{41}}{4}
$$

---

**例题 2**：解 $x^2 - 2x - 3 = 0$。

$$
x = \frac{2 \pm \sqrt{4 + 12}}{2} = \frac{2 \pm 4}{2}
$$

$x=3$ 或 $x=-1$。

---

**例题 3**：解 $4x^2 - 12x + 9 = 0$。

$$
x = \frac{12 \pm \sqrt{144 - 144}}{8} = \frac{12}{8} = \frac{3}{2}\ (\text{重根})
$$

---

**例题 4**：解 $x^2 - 3x - 5 = 0$。

$$
x = \frac{3 \pm \sqrt{9 + 20}}{2} = \frac{3 \pm \sqrt{29}}{2}
$$

---

**例题 5**：解 $3x^2 + 2x - 4 = 0$。

$$
x = \frac{-2 \pm \sqrt{4 + 48}}{6} = \frac{-2 \pm \sqrt{52}}{6} = \frac{-2 \pm 2\sqrt{13}}{6} = \frac{-1 \pm \sqrt{13}}{3}
$$

---

**例题 6**：解 $5x^2 + 2x - 1 = 0$。

$$
x = \frac{-2 \pm \sqrt{4 + 20}}{10} = \frac{-2 \pm \sqrt{24}}{10} = \frac{-2 \pm 2\sqrt{6}}{10} = \frac{-1 \pm \sqrt{6}}{5}
$$

---

### 3.3.3 配方法

配方法将 $ax^2 + bx + c$ 写成 $a(x + p)^2 + q$ 的形式。

**完整推导**：

$$
\begin{aligned}
ax^2 + bx + c &= a\left(x^2 + \frac{b}{a}x\right) + c \\
&= a\left[x^2 + \frac{b}{a}x + \left(\frac{b}{2a}\right)^2 - \left(\frac{b}{2a}\right)^2\right] + c \\
&= a\left[\left(x + \frac{b}{2a}\right)^2 - \frac{b^2}{4a^2}\right] + c \\
&= a\left(x + \frac{b}{2a}\right)^2 + \left(c - \frac{b^2}{4a}\right)
\end{aligned}
$$

**最终形式**：

$$
\boxed{ax^2 + bx + c = a\left(x + \frac{b}{2a}\right)^2 + \frac{4ac - b^2}{4a}}
$$

---

**例题 1**：用配方法解 $x^2 - 6x + 5 = 0$。

$$
\begin{aligned}
x^2 - 6x + 5 &= 0 \\
x^2 - 6x &= -5 \\
x^2 - 6x + 9 &= -5 + 9 \quad (\text{加 } (\frac{6}{2})^2=9) \\
(x - 3)^2 &= 4 \\
x - 3 &= \pm 2 \\
x &= 5 \text{ 或 } x = 1
\end{aligned}
$$

---

**例题 2**：用配方法解 $2x^2 - 8x + 3 = 0$。

$$
\begin{aligned}
2x^2 - 8x + 3 &= 0 \\
2(x^2 - 4x) &= -3 \\
2[(x^2 - 4x + 4) - 4] &= -3 \\
2(x - 2)^2 - 8 &= -3 \\
2(x - 2)^2 &= 5 \\
(x - 2)^2 &= \frac{5}{2} \\
x &= 2 \pm \frac{\sqrt{10}}{2}
\end{aligned}
$$

---

**例题 3**：将 $f(x) = 3x^2 + 12x + 5$ 写成 $a(x + p)^2 + q$ 的形式。

$$
\begin{aligned}
f(x) &= 3x^2 + 12x + 5 \\
&= 3(x^2 + 4x) + 5 \\
&= 3[(x + 2)^2 - 4] + 5 \\
&= 3(x + 2)^2 - 12 + 5 \\
&= 3(x + 2)^2 - 7
\end{aligned}
$$

顶点为 $(-2, -7)$，$a=3>0$ 开口向上。

---

**例题 4**：用配方法解 $x^2 - 8x + 13 = 0$。

$$
\begin{aligned}
x^2 - 8x + 13 &= 0 \\
x^2 - 8x &= -13 \\
x^2 - 8x + 16 &= -13 + 16 \quad (\text{加 } (\frac{8}{2})^2=16) \\
(x - 4)^2 &= 3 \\
x - 4 &= \pm \sqrt{3} \\
x &= 4 \pm \sqrt{3}
\end{aligned}
$$

---

**例题 5**：用配方法解 $2x^2 - 8x + 5 = 0$。

$$
\begin{aligned}
2x^2 - 8x + 5 &= 0 \\
2(x^2 - 4x) &= -5 \\
2[(x - 2)^2 - 4] &= -5 \\
2(x - 2)^2 - 8 &= -5 \\
2(x - 2)^2 &= 3 \\
(x - 2)^2 &= \frac{3}{2} \\
x &= 2 \pm \frac{\sqrt{6}}{2}
\end{aligned}
$$

---

**例题 6**：将 $f(x) = -2x^2 + 8x - 5$ 写成 $a(x + p)^2 + q$ 的形式。

$$
\begin{aligned}
f(x) &= -2x^2 + 8x - 5 \\
&= -2(x^2 - 4x) - 5 \\
&= -2[(x - 2)^2 - 4] - 5 \\
&= -2(x - 2)^2 + 8 - 5 \\
&= -2(x - 2)^2 + 3
\end{aligned}
$$

顶点为 $(2, 3)$，$a=-2<0$ 开口向下。

---

### 三法对比——同一个方程用三种方法解

解 $x^2 - 4x - 5 = 0$：

**因式分解法**（最快）：
$(x - 5)(x + 1) = 0$，$x = 5$ 或 $x = -1$。

**公式法**：
$x = \frac{4 \pm \sqrt{16 + 20}}{2} = \frac{4 \pm 6}{2}$，$x = 5$ 或 $x = -1$。

**配方法**：
$(x - 2)^2 = 9$，$x - 2 = \pm 3$，$x = 5$ 或 $x = -1$。

三法结果相同，但因式分解法最快捷——**能用分解法时优先用分解法**。

---

## 3.4 配方法与最值

### 3.4.1 用配方法求最值

$f(x) = a(x + p)^2 + q$ 中，由于 $(x + p)^2 \geq 0$：
- $a > 0$：$f(x) \geq q$，最小值 $q$ 在 $x = -p$ 处。
- $a < 0$：$f(x) \leq q$，最大值 $q$ 在 $x = -p$ 处。

**为什么？** 因为 $(x + p)^2$ 的最小值是 0（当 $x = -p$ 时），此时 $f(x) = q$。

---

**例题 1**：求 $f(x) = x^2 - 4x + 7$ 的最小值。

$f(x) = (x - 2)^2 + 3$。$a=1>0$，当 $x=2$ 时取最小值 $3$。

---

**例题 2**：求 $f(x) = -2x^2 + 12x - 10$ 的最大值。

$f(x) = -2(x - 3)^2 + 8$。$a=-2<0$，当 $x=3$ 时取最大值 $8$。

---

**例题 3**：求 $f(x) = x^2 - 2x - 3$ 在 $[0, 4]$ 上的最值。

$f(x) = (x - 1)^2 - 4$。顶点 $(1, -4)$ 在区间内，最小值 $-4$。
$f(0) = -3$，$f(4) = 5$。最大值 $5$。

---

**例题 4**：求 $f(x) = x^2 + 6x + 11$ 的最小值。

$f(x) = (x + 3)^2 + 2$。最小值 $2$ 在 $x = -3$ 处。

---

**例题 5**：求 $f(x) = -x^2 + 4x + 1$ 的最大值。

$f(x) = -(x - 2)^2 + 5$。最大值 $5$ 在 $x = 2$ 处。

---

**例题 6**：求 $f(x) = x^2 - 4x + 5$ 在 $[1, 5]$ 上的值域。

$f(x) = (x - 2)^2 + 1$，顶点 $(2, 1)$ 在区间内。$f(1)=2$，$f(5)=10$。值域 $[1, 10]$。

---

### 3.4.2 画草图

四个关键要素：开口方向、顶点、$x$ 轴交点、$y$ 轴交点。

---

**例题 1**：$f(x) = x^2 - 2x - 3$。
开口向上，顶点 $(1, -4)$，$x$ 轴交点 $(-1,0)$ 和 $(3,0)$，$y$ 轴交点 $(0,-3)$。

**例题 2**：$f(x) = -x^2 + 4x$。
开口向下，顶点 $(2, 4)$，$x$ 轴交点 $(0,0)$ 和 $(4,0)$。

**例题 3**：$f(x) = x^2 + 2x + 3$。
开口向上，顶点 $(-1, 2)$，$\Delta < 0$ 无 $x$ 轴交点，$y$ 轴交点 $(0,3)$。完全在 $x$ 轴上方。

**例题 4**：$f(x) = -2x^2 + 4x + 6$。
开口向下，顶点 $(1, 8)$，$x$ 轴交点 $(-1,0)$ 和 $(3,0)$，$y$ 轴交点 $(0,6)$。

---

### 3.4.3 求值域

步骤：配方→判断顶点是否在定义域内→算端点→比较。

**例题 1**：$f(x) = 2x^2 - 8x + 3$ 在 $\mathbb{R}$ 上。
$f(x)=2(x-2)^2-5$，值域 $[-5,\infty)$。

**例题 2**：$f(x) = x^2 - 2x + 3$ 在 $[-1,3]$ 上。
$f(x)=(x-1)^2+2$，顶点在区间内，$f(1)=2$，$f(-1)=6$，$f(3)=6$，值域 $[2,6]$。

**例题 3**：$f(x) = x^2 - 4x + 5$ 在 $[3,5]$ 上。
$f(x)=(x-2)^2+1$，顶点 $x=2$ 不在区间内，函数单调递增，$f(3)=2$，$f(5)=10$，值域 $[2,10]$。

**例题 4**：$f(x) = -x^2 + 2x + 3$ 在 $[-1,4]$ 上。
$f(x)=-(x-1)^2+4$，顶点 $(1,4)$ 在区间内。$f(-1)=0$，$f(4)=-5$。值域 $[-5,4]$。

---

## 3.5 二次不等式

### 3.5.1 代数法（符号表法）

**完整步骤**：

**第 1 步**：整理为 $ax^2 + bx + c \;(>/</\geq/\leq)\;0$。若 $a < 0$，两边乘 $-1$ 并反转不等号。

**第 2 步**：解对应方程 $ax^2 + bx + c = 0$，得根 $x_1 \leq x_2$。

**第 3 步**：写出解集。

**符号法则**（$a > 0$ 时）：

```
符号：   +      -      +
       ———|—————|—————>
          x₁    x₂
```

- **大于取两边**：$ax^2 + bx + c > 0 \Rightarrow x < x_1$ 或 $x > x_2$
- **小于取中间**：$ax^2 + bx + c < 0 \Rightarrow x_1 < x < x_2$

**为什么这个符号法则成立？**

因为 $a > 0$ 时抛物线开口向上。在两根之间，抛物线在 $x$ 轴下方（负值）；在两根之外，抛物线在 $x$ 轴上方（正值）。

**特殊情况**：

| $\Delta$ 的情况 | $>0$ | $<0$ |
|:---|:---|:---|
| $\Delta = 0$（$a>0$） | $x \neq x_1$ | 无解 |
| $\Delta < 0$（$a>0$） | $\mathbb{R}$（全体实数） | 无解 |

---

**例题 1**：解 $x^2 - 5x + 6 > 0$。

$(x - 2)(x - 3) > 0$。根为 $x = 2$ 和 $x = 3$。$a = 1 > 0$。

"大于取两边"：$x < 2$ 或 $x > 3$。

验证：取 $x=0$：$0-0+6=6 > 0$ ✓；取 $x=2.5$：$6.25-12.5+6=-0.25 < 0$ ✓。

---

**例题 2**：解 $2x^2 - 5x - 3 \leq 0$。

$(2x + 1)(x - 3) \leq 0$。根为 $x = -\frac{1}{2}$ 和 $x = 3$。$a = 2 > 0$。

"小于取中间"（含端点）：$-\frac{1}{2} \leq x \leq 3$。

---

**例题 3**：解 $x^2 + 2x + 3 > 0$。

$\Delta = 4 - 12 = -8 < 0$，$a = 1 > 0$。恒正。解集为 $\mathbb{R}$。

---

**例题 4**：解 $-x^2 + 3x + 4 > 0$。

$a = -1 < 0$，两边乘 $-1$：$x^2 - 3x - 4 < 0$。

$(x - 4)(x + 1) < 0$。根为 $x = -1$ 和 $x = 4$。

"小于取中间"：$-1 < x < 4$。

---

**例题 5**：解 $x^2 - 4x + 4 \geq 0$。

$(x - 2)^2 \geq 0$。平方数恒 $\geq 0$，解集为 $\mathbb{R}$。

---

**例题 6**：解 $x^2 - 4x + 4 < 0$。

$(x - 2)^2 < 0$。平方数不可能小于零，**无解**。

---

### 3.5.2 图像法

画出 $y = ax^2 + bx + c$ 的草图，查看抛物线在 $x$ 轴上方的部分（$> 0$）或下方的部分（$< 0$）。

---

**例题 1**：用图像法解 $x^2 - x - 2 < 0$。

$y = x^2 - x - 2$，$a=1>0$，开口向上。$x$ 轴交点 $(-1,0)$ 和 $(2,0)$。

图像在 $-1 < x < 2$ 之间位于 $x$ 轴下方。解集：$-1 < x < 2$。

---

**例题 2**：已知 $x^2 - 2kx + 4 > 0$ 对所有实数 $x$ 恒成立，求 $k$。

$a=1>0$，需 $\Delta < 0$：$4k^2 - 16 < 0 \Rightarrow k^2 < 4 \Rightarrow -2 < k < 2$。

---

**例题 3**：解 $x^2 - 4 \geq 3x$。

移项：$x^2 - 3x - 4 \geq 0$。$(x - 4)(x + 1) \geq 0$。

"大于取两边"（含端点）：$x \leq -1$ 或 $x \geq 4$。

---

**例题 4**：解 $x^2 - 3x - 10 > 0$。

$(x - 5)(x + 2) > 0$。$x < -2$ 或 $x > 5$。

---

**例题 5**：解 $2x^2 + 5x - 3 \leq 0$。

$(2x - 1)(x + 3) \leq 0$。$-3 \leq x \leq \frac{1}{2}$。

---

**例题 6**：解 $x^2 - 6x + 9 \geq 0$。

$(x - 3)^2 \geq 0$，解集 $\mathbb{R}$。

---

### 3.5.3 含参数的不等式问题

**例题 1**：求 $k$ 使 $x^2 + kx + 9 \geq 0$ 对一切 $x$ 恒成立。

$a=1>0$，需 $\Delta \leq 0$：$k^2 - 36 \leq 0 \Rightarrow -6 \leq k \leq 6$。

---

**例题 2**：求 $k$ 使 $kx^2 + 2x + 3 > 0$ 对一切 $x$ 恒成立。

若 $k = 0$：$2x+3>0$ 不是恒成立，排除。
若 $k \neq 0$：需 $k > 0$ 且 $\Delta = 4 - 12k < 0 \Rightarrow k > \frac{1}{3}$。

所以 $k > \frac{1}{3}$。

---

**例题 3**：求 $k$ 使 $x^2 - 2kx + 4 > 0$ 对所有实数 $x$ 恒成立。

$\Delta = 4k^2 - 16 < 0 \Rightarrow k^2 < 4 \Rightarrow -2 < k < 2$。

---

**例题 4**：求 $k$ 使 $(k-1)x^2 + 2x + 1 > 0$ 对一切 $x$ 恒成立。

若 $k-1 = 0$，即 $k=1$：$2x+1 > 0$，不是恒成立。
若 $k-1 \neq 0$：需 $k-1 > 0$ 且 $\Delta = 4 - 4(k-1) = 8 - 4k < 0 \Rightarrow k > 2$。

所以 $k > 2$。

---

## 3.6 三次多项式的图像与不等式

### 3.6.1 三个线性因式乘积的图像

$f(x) = a(x - p)(x - q)(x - r)$ 的图像特征：

**（1）$x$ 轴截距**：$x = p, q, r$（三个零点）。

**（2）$y$ 轴截距**：$f(0) = a(-p)(-q)(-r) = -a \cdot pqr$。

**（3）端点行为**——取决于最高次项 $ax^3$：

当 $|x|$ 很大时，最高次项 $ax^3$ 起主导作用：

| $a$ 的符号 | $x \to -\infty$ | $x \to +\infty$ |
|:---:|:---:|:---:|
| $a > 0$ | $f(x) \to -\infty$（左下） | $f(x) \to +\infty$（右上） |
| $a < 0$ | $f(x) \to +\infty$（左上） | $f(x) \to -\infty$（右下） |

**（4）零点处的行为**：
- **单根**（因式次数为 1）：图像**穿过** $x$ 轴。
- **二重根**（因式次数为 2）：图像**触及并反弹**（相切于 $x$ 轴）。

**画草图步骤**：
1. 标出 $x$ 轴截距 $p, q, r$。
2. 标出 $y$ 轴截距。
3. 根据 $a$ 的符号确定两端走向。
4. 用平滑的 S 形曲线连接各点，在单根处穿过，在二重根处反弹。

---

**例题 1**：画出 $f(x) = (x + 1)(x - 1)(x - 3)$ 的草图。

$x$ 截距：$x = -1,\;1,\;3$（三个单根，全部穿过）。
$y$ 截距：$f(0) = (1)(-1)(-3) = 3$，过 $(0, 3)$。
$a = 1 > 0$：左端向下，右端向上。

走向：从第三象限 → 在 $x = -1$ 从下到上穿过 → 局部极大值 → 到 $x = 1$ 从上到下穿过 → 局部极小值 → 到 $x = 3$ 从下到上穿过 → 向右上延伸。

---

**例题 2**：画出 $f(x) = -(x + 2)(x - 1)(x - 4)$ 的草图。

$x$ 截距：$x = -2,\;1,\;4$。
$y$ 截距：$f(0) = -(2)(-1)(-4) = -8$，过 $(0, -8)$。
$a = -1 < 0$：左端向上，右端向下。

走向：从第二象限 → 在 $x = -2$ 从上到下穿过 → 局部极小值 → 到 $x = 1$ 从下到上穿过 → 局部极大值 → 到 $x = 4$ 从上到下穿过 → 向右下延伸。

---

**例题 3**：画出 $f(x) = (x - 1)^2(x + 2)$ 的草图。

$x$ 截距：$x = -2$（单根，穿过），$x = 1$（二重根，触及反弹）。
$y$ 截距：$f(0) = (1)^2(2) = 2$，过 $(0, 2)$。
$a = 1 > 0$：左端向下，右端向上。

走向：从第三象限 → 在 $x = -2$ 从下到上穿过 → 局部极大值 → 下降到 $x = 1$ 处触及 $x$ 轴并反弹 → 向右上延伸。

---

**例题 4**：画出 $f(x) = -(x + 1)(x - 2)^2$ 的草图。

$x$ 截距：$x = -1$（单根，穿过），$x = 2$（二重根，触及反弹）。
$y$ 截距：$f(0) = -(1)(4) = -4$，过 $(0, -4)$。
$a = -1 < 0$：左端向上，右端向下。

走向：从第二象限 → 在 $x = -1$ 从上到下穿过 → 局部极小值 → 上升到 $x = 2$ 处触及 $x$ 轴并反弹 → 向右下延伸。

---

**例题 5**：画出 $f(x) = (x + 3)(x + 1)(x - 2)$ 的草图。

$x$ 截距：$x = -3,\;-1,\;2$（三个单根）。
$y$ 截距：$f(0) = (3)(1)(-2) = -6$，过 $(0, -6)$。
$a = 1 > 0$：左端向下，右端向上。

---

**例题 6**：画出 $f(x) = -2(x + 1)(x - 1)(x - 3)$ 的草图。

$x$ 截距：$x = -1,\;1,\;3$。
$y$ 截距：$f(0) = -2(1)(-1)(-3) = -6$，过 $(0, -6)$。
$a = -2 < 0$：左端向上，右端向下。

---

### 3.6.2 绝对值图像

**核心规则**（必须牢记）：

$$
y = |f(x)|
$$

- **保留** $f(x) \geq 0$ 的部分（$x$ 轴上方的部分**不变**）
- **翻折** $f(x) < 0$ 的部分（将 $x$ 轴下方的部分**沿 $x$ 轴向上对称翻转**）

即：**负数部分翻折到正半轴**。

因此在 $y = |f(x)|$ 的图像中：
1. 图像永远在 $x$ 轴**上方**（或轴上），不可能有负值。
2. 在 $f(x) = 0$ 的零点处，绝对值图像会出现**尖点**（因为从正变负或从负变正时，斜率突然反转方向）。
3. 原函数在 $x$ 轴上方的部分保持不变，下方的部分被"折叠"上来。

---

**例题 1**：画出 $y = |(x + 1)(x - 1)(x - 3)|$ 的草图。

先分析 $f(x) = (x + 1)(x - 1)(x - 3)$ 的符号：

| 区间 | $x<-1$ | $-1<x<1$ | $1<x<3$ | $x>3$ |
|:---:|:---:|:---:|:---:|:---:|
| $f(x)$ | $-$ | $+$ | $-$ | $+$ |

将负的部分（$x < -1$ 和 $1 < x < 3$）沿 $x$ 轴向上翻折。

最终图像在 $x = -1, 1, 3$ 处与 $x$ 轴相交（尖点），其余部分全部在 $x$ 轴上方。

---

**例题 2**：画出 $y = |(x - 1)(x - 2)(x - 4)|$ 的草图。

分析 $f(x) = (x - 1)(x - 2)(x - 4)$ 的符号：

$f(0) = (-1)(-2)(-4) = -8$，说明 $x=0$ 时 $f(x) < 0$。

| 区间 | $x<1$ | $1<x<2$ | $2<x<4$ | $x>4$ |
|:---:|:---:|:---:|:---:|:---:|
| $f(x)$ | $-$ | $+$ | $-$ | $+$ |

将负的区域（$x<1$ 和 $2<x<4$）沿 $x$ 轴向上翻折。尖点在 $x=1,2,4$。

---

**例题 3**：求 $|(x + 1)(x - 1)(x - 2)| = 2$ 的实根个数。

符号分析：$x<-1$（$-$），$-1<x<1$（$+$），$1<x<2$（$-$），$x>2$（$+$）。

做绝对值变换后，$|f(0)| = |(1)(-1)(-2)| = 2$，$(0,2)$ 是一个交点。

水平线 $y=2$ 与图像相交：
- $x<-1$：1 个交点
- $-1<x<1$：2 个交点
- $1<x<2$：2 个交点
- $x>2$：1 个交点

总共 **5 个交点**，即方程有 5 个实根。

---

**例题 4**：画出 $y = |(x + 2)(x - 1)^2|$ 的草图。

$f(x) = (x + 2)(x - 1)^2$。

符号：$x<-2$（$-$），$-2<x<1$（$+$），$x>1$（$+$）。

将 $x<-2$ 的部分沿 $x$ 轴向上翻折。在 $x=-2$ 处有尖点；在 $x=1$ 处是平滑触及（二重根，原函数在此不改变符号，不需要翻折）。

---

**例题 5**：画出 $y = |(x+1)(x-2)(x-5)|$ 的草图。

符号：$x<-1$（$-$），$-1<x<2$（$+$），$2<x<5$（$-$），$x>5$（$+$）。

翻折 $x<-1$ 和 $2<x<5$ 部分。尖点在 $x=-1,2,5$。

---

**例题 6**：求 $|(x+2)(x-1)(x-4)|=3$ 的实根个数（估算）。

图像在 $x<-2$ 和 $1<x<4$ 部分被翻折上来。水平线 $y=3$ 与图像大约有 5 个交点，即约 5 个实根。

---

### 3.6.3 三次不等式的图像解法（考纲 4.5）

对于 $f(x) \geq d$（$>$, $\leq$, $<$ 同理），其中 $f(x) = a(x-p)(x-q)(x-r)$：

1. 画出 $y = f(x)$ 的草图。
2. 画水平线 $y = d$。
3. 找出交点横坐标（解 $f(x) = d$）。
4. 读取满足不等式的 $x$ 区间。

**当 $d = 0$ 时**，水平线就是 $x$ 轴，问题简化为分析 $f(x)$ 的符号。

---

**例题 1**：$f(x) = (x+1)(x-1)(x-3)$，解 $f(x) \leq 0$。

符号表：

| 区间 | $x<-1$ | $-1<x<1$ | $1<x<3$ | $x>3$ |
|:---:|:---:|:---:|:---:|:---:|
| $f(x)$ | $-$ | $+$ | $-$ | $+$ |

$f(x) \leq 0$ 对应负或零的区间（含端点）：

$$
\boxed{x \leq -1 \quad \text{或} \quad 1 \leq x \leq 3}
$$

---

**例题 2**：$f(x) = -(x+1)(x-2)(x-5)$，解 $f(x) > 0$。

先考虑 $g(x) = (x+1)(x-2)(x-5)$，$a_g = 1 > 0$。

$g(x)$ 符号：$x<-1$（$-$），$-1<x<2$（$+$），$2<x<5$（$-$），$x>5$（$+$）。

$f(x) = -g(x)$，符号与 $g(x)$ 相反：

| 区间 | $x<-1$ | $-1<x<2$ | $2<x<5$ | $x>5$ |
|:---:|:---:|:---:|:---:|:---:|
| $f(x)$ | $+$ | $-$ | $+$ | $-$ |

$f(x) > 0$ 对应正区间（不含端点）：

$$
\boxed{x < -1 \quad \text{或} \quad 2 < x < 5}
$$

---

**例题 3**：$f(x) = (x+2)(x-1)(x-4)$，解 $f(x) \geq 8$。

展开：$f(x) = x^3 - 3x^2 - 6x + 8$。

解 $f(x) = 8$：

$$
x^3 - 3x^2 - 6x + 8 = 8 \Rightarrow x^3 - 3x^2 - 6x = 0 \Rightarrow x(x^2 - 3x - 6) = 0
$$

$x = 0$ 或 $x = \frac{3 \pm \sqrt{33}}{2}$。$\frac{3 - \sqrt{33}}{2} \approx -1.372$，$\frac{3 + \sqrt{33}}{2} \approx 4.372$。

$a = 1 > 0$，左端向下，右端向上。$f(x) \geq 8$ 的解集为：

$$
\boxed{\frac{3 - \sqrt{33}}{2} \leq x \leq 0 \quad \text{或} \quad x \geq \frac{3 + \sqrt{33}}{2}}
$$

---

**例题 4**：$f(x) = (x+1)(x-2)(x-4)$，解 $f(x) \leq 0$。

符号：$x<-1$（$-$），$-1<x<2$（$+$），$2<x<4$（$-$），$x>4$（$+$）。

$\leq 0$：$x \leq -1$ 或 $2 \leq x \leq 4$。

---

**例题 5**：$f(x) = -(x+2)(x-1)(x-5)$，解 $f(x) \geq 0$。

$f(x) \geq 0 \iff -(x+2)(x-1)(x-5) \geq 0 \iff (x+2)(x-1)(x-5) \leq 0$。

符号：$x<-2$（$-$），$-2<x<1$（$+$），$1<x<5$（$-$），$x>5$（$+$）。

$(x+2)(x-1)(x-5) \leq 0$：$x \leq -2$ 或 $1 \leq x \leq 5$。

---

**例题 6**：解 $(x+1)(x-1)(x-3) \geq 4$。

$f(x) = (x+1)(x-1)(x-3) = x^3 - 3x^2 - x + 3$。

$f(x) = 4 \Rightarrow x^3 - 3x^2 - x - 1 = 0$。此三次方程不易因式分解，在实际考试中通常会给出交点坐标或可通过计算器求解。

---

## 3.7 用微分求二次函数的极值

### 3.7.1 微分法的引入

在学习微分之前，我们用配方法求极值。有了微分这个工具后，我们可以用导数来求极值，这为后续学习更复杂函数（三次函数、指数函数、三角函数等）的极值问题打下基础。

**核心思想**：函数在极值点处的切线是水平的，即斜率为零，即**导数为零**。

对于二次函数 $f(x) = ax^2 + bx + c$：

**第 1 步：求导**。

由幂法则 $(x^n)' = nx^{n-1}$：

$$
f'(x) = \frac{d}{dx}(ax^2 + bx + c) = 2ax + b
$$

**推导过程**：
- $\frac{d}{dx}(ax^2) = a \cdot 2x = 2ax$
- $\frac{d}{dx}(bx) = b \cdot 1 = b$
- $\frac{d}{dx}(c) = 0$（常数的导数为零）

**第 2 步：令导数为零，找到驻点**。

$$
2ax + b = 0 \;\Rightarrow\; x = -\frac{b}{2a}
$$

这正是我们用配方法得到的顶点横坐标！

**第 3 步：代入原函数求极值**。

$$
\begin{aligned}
f\!\left(-\frac{b}{2a}\right) &= a\left(-\frac{b}{2a}\right)^2 + b\left(-\frac{b}{2a}\right) + c \\
&= a \cdot \frac{b^2}{4a^2} - \frac{b^2}{2a} + c \\
&= -\frac{b^2}{4a} + c = \frac{4ac - b^2}{4a}
\end{aligned}
$$

**第 4 步：用二阶导数判断极值类型**。

二阶导数是一阶导数的导数：

$$
f''(x) = \frac{d}{dx}(2ax + b) = 2a
$$

- $f''(x) = 2a > 0$（即 $a > 0$）：**最小值**。因为 $f'' > 0$ 意味着 $f'$ 在增加，$f'$ 从负到正经过零，函数先减后增。
- $f''(x) = 2a < 0$（即 $a < 0$）：**最大值**。因为 $f'' < 0$ 意味着 $f'$ 在减少，$f'$ 从正到负经过零，函数先增后减。

**对照配方法**：

微分法得到 $x = -\frac{b}{2a}$，配方法得到 $f(x) = a(x + \frac{b}{2a})^2 + \frac{4ac-b^2}{4a}$，顶点横坐标都是 $-\frac{b}{2a}$。两种方法完全等价。

---

**例题 1**：用微分法求 $f(x) = 2x^2 - 8x + 5$ 的极值。

$f'(x) = 4x - 8$。令 $f'(x) = 0$：$4x = 8 \Rightarrow x = 2$。

$f''(x) = 4 > 0$，最小值。

$f(2) = 8 - 16 + 5 = -3$。

**验证**（配方法）：$f(x) = 2(x - 2)^2 - 3$，最小值 $-3$。✓

---

**例题 2**：用微分法求 $f(x) = -3x^2 + 12x - 7$ 的极值。

$f'(x) = -6x + 12$。令 $f'(x) = 0$：$x = 2$。

$f''(x) = -6 < 0$，最大值。

$f(2) = -12 + 24 - 7 = 5$。

**验证**（配方法）：$f(x) = -3(x - 2)^2 + 5$，最大值 $5$。✓

---

**例题 3**：已知 $f(x) = x^2 + kx + 4$ 在 $x = 3$ 处取极值，求 $k$ 并判断。

$f'(x) = 2x + k$。$f'(3) = 6 + k = 0 \Rightarrow k = -6$。

$f''(x) = 2 > 0$，极小值。

$f(3) = 9 - 18 + 4 = -5$。

---

**例题 4**：用微分法求 $f(x) = 5x^2 - 20x + 3$ 的极值，与配方法对比。

**微分法**：$f'(x) = 10x - 20 = 0 \Rightarrow x = 2$。$f''(x) = 10 > 0$，最小值 $f(2) = 20 - 40 + 3 = -17$。

**配方法**：$f(x) = 5(x-2)^2 - 17$，最小值 $-17$。两种方法结果一致。✓

**对比**：微分法步骤更直接，不需要配方运算。

---

**例题 5**：用微分法求 $f(x) = -4x^2 + 24x - 31$ 的极值。

$f'(x) = -8x + 24 = 0 \Rightarrow x = 3$。$f''(x) = -8 < 0$，最大值 $f(3) = -36 + 72 - 31 = 5$。

---

**例题 6**：已知 $f(x) = 3x^2 + 2mx + 5$ 在 $x = -2$ 处取极值，求 $m$ 和极值。

$f'(x) = 6x + 2m$。$f'(-2) = -12 + 2m = 0 \Rightarrow m = 6$。

$f''(x) = 6 > 0$，极小值。$f(-2) = 12 - 24 + 5 = -7$。

---

**例题 7**：用微分法证明 $f(x) = x^2 + 4x + 7$ 的最小值为 $3$。

$f'(x) = 2x + 4 = 0 \Rightarrow x = -2$。$f''(x) = 2 > 0$，最小值 $f(-2) = 4 - 8 + 7 = 3$。证毕。✓

---

**例题 8**：某矩形花园的周长为 $40$ 米，求面积的最大值。

设长为 $x$ 米，则宽为 $20 - x$ 米。

面积 $A(x) = x(20 - x) = 20x - x^2 = -x^2 + 20x$。

$A'(x) = -2x + 20 = 0 \Rightarrow x = 10$。$A''(x) = -2 < 0$，最大值。

最大面积 $A(10) = 100$ 平方米。

---

**例题 9**：求 $f(x) = 2x^2 - 12x + 5$ 的极值，并用配方法验证。

**微分法**：$f'(x) = 4x - 12 = 0 \Rightarrow x = 3$。$f''(x) = 4 > 0$，最小值 $f(3) = 18 - 36 + 5 = -13$。

**配方法验证**：$f(x) = 2(x-3)^2 - 13$，最小值 $-13$。✓

---

**例题 10**：已知 $f(x) = ax^2 + 6x + 2$ 在 $x = -1$ 处取极值，求 $a$ 和极值。

$f'(x) = 2ax + 6$。$f'(-1) = -2a + 6 = 0 \Rightarrow a = 3$。

$f''(x) = 2a = 6 > 0$，极小值。$f(-1) = 3 - 6 + 2 = -1$。

---

**例题 11**：用微分法求 $f(x) = 4x^2 - 16x + 7$ 的极值。

$f'(x) = 8x - 16 = 0 \Rightarrow x = 2$。$f''(x) = 8 > 0$，最小值 $f(2) = 16 - 32 + 7 = -9$。

---

**例题 12**：用微分法求 $f(x) = -5x^2 + 30x - 41$ 的极值。

$f'(x) = -10x + 30 = 0 \Rightarrow x = 3$。$f''(x) = -10 < 0$，最大值 $f(3) = -45 + 90 - 41 = 4$。

---

**例题 13**：已知 $f(x) = 2x^2 + kx + 3$ 在 $x = -2$ 处取极值，求 $k$ 和极值。

$f'(x) = 4x + k$。$f'(-2) = -8 + k = 0 \Rightarrow k = 8$。

$f''(x) = 4 > 0$，极小值。$f(-2) = 8 - 16 + 3 = -5$。

---

**例题 14**：已知 $f(x) = -3x^2 + mx + 1$ 在 $x = 1$ 处取极值，求 $m$ 和极值。

$f'(x) = -6x + m$。$f'(1) = -6 + m = 0 \Rightarrow m = 6$。

$f''(x) = -6 < 0$，最大值。$f(1) = -3 + 6 + 1 = 4$。

---

**例题 15**：用微分法和配方法分别求 $f(x) = 3x^2 - 18x + 25$ 的极值，对比两种方法。

**微分法**：$f'(x) = 6x - 18 = 0 \Rightarrow x = 3$。$f''(x) = 6 > 0$，最小值 $f(3) = 27 - 54 + 25 = -2$。

**配方法**：$f(x) = 3(x^2 - 6x) + 25 = 3[(x-3)^2 - 9] + 25 = 3(x-3)^2 - 27 + 25 = 3(x-3)^2 - 2$。最小值 $-2$ 在 $x=3$ 处。✓

**对比**：微分法只需三步（求导→令零→二阶导），配方法需要配方运算。对于二次函数两者难度相当，但对于更复杂的函数微分法更具优势。

---

## 本章总结

| 知识点 | 核心内容 |
|:---|:---|
| **余数定理** | $f(x) \div (x-a)$ 余数为 $f(a)$；$f(x) \div (ax+b)$ 余数为 $f(-b/a)$ |
| **因式定理** | $f(a)=0 \iff (x-a)$ 是因式 |
| **三次式分解流程** | 试根 → 综合除法 → 分解二次式 |
| **综合除法** | 只处理系数的除法格式，比长除法更简洁 |
| **判别式 $\Delta$** | $\Delta = b^2-4ac$；$\Delta>0$ 两不等根，$\Delta=0$ 重根，$\Delta<0$ 无实根 |
| **直线与曲线** | 代入消 $y$ → 二次方程 → $\Delta$ 判相交/相切/不相交 |
| **解二次方程三法** | 因式分解（最快）、公式法（万能）、配方法（顶点形式） |
| **最值** | $a(x+p)^2+q$，$a>0$ 最小 $q$，$a<0$ 最大 $q$ |
| **二次不等式** | $a>0$ 时"大于取两边，小于取中间" |
| **三次图像** | $a>0$ 左下到右上，$a<0$ 左上到右下；单根穿过，二重根反弹 |
| **绝对值图像** | 负的部分向上翻折到正半轴，零点处有尖点 |
| **三次不等式** | 画图 → 画水平线 $y=d$ → 读区间 |
| **微分求极值** | $f'(x)=0$ 得驻点，$f''(x)$ 判最大/最小 |

---

## 综合练习题

**1. 余数定理**：
(a) 求 $f(x) = 5x^3 - 4x^2 + 3x - 2$ 除以 $x - 2$ 的余数。
(b) 多项式 $f(x) = 2x^3 + kx^2 - 3x + 1$ 除以 $x + 2$ 余数为 $15$，求 $k$。
(c) 求 $f(x) = 8x^3 - 6x^2 + 4x - 1$ 除以 $2x - 3$ 的余数。

**2. 因式定理**：
(a) 证明 $(x + 2)$ 是 $f(x) = x^3 + 3x^2 - 4x - 12$ 的一个因式。
(b) 多项式 $f(x) = 3x^3 + ax^2 + bx - 10$ 有因式 $(x - 2)$ 和 $(x + 1)$，求 $a$ 和 $b$。
(c) 已知 $x - 3$ 是 $f(x) = 2x^3 - 5x^2 + kx - 6$ 的一个因式，求 $k$。

**3. 分解三次多项式**：
(a) $x^3 - 3x^2 - 10x + 24$
(b) $3x^3 + 2x^2 - 7x + 2$
(c) $4x^3 - 12x^2 - x + 3$

**4. 解三次方程**：
(a) $x^3 - 2x^2 - 5x + 6 = 0$
(b) $2x^3 - 3x^2 - 3x + 2 = 0$
(c) 已知 $x = -3$ 是 $x^3 + 3x^2 - 4x + k = 0$ 的一个根，求 $k$ 并解此方程。

**5. 判别式**：
(a) 判断 $2x^2 - 5x + 4 = 0$ 的根的情况。
(b) 方程 $x^2 - 6x + k = 0$ 有重根，求 $k$。
(c) 方程 $3x^2 + kx + 3 = 0$ 无实根，求 $k$ 的范围。

**6. 直线与曲线**：
(a) 判断 $y = 4x - 3$ 与 $y = x^2 - x + 2$ 的位置关系。
(b) 求 $k$ 使 $y = 2x + k$ 与 $y = x^2 - 4x + 7$ 相切。
(c) 求 $m$ 使 $y = mx - 1$ 与 $y = x^2 - 2x + 4$ 相交于两点。

**7. 解二次方程**：
(a) $x^2 - 7x + 12 = 0$（因式分解法）
(b) $3x^2 + 5x - 2 = 0$（因式分解法）
(c) $2x^2 - 4x - 3 = 0$（公式法）
(d) $x^2 - 8x + 13 = 0$（配方法）
(e) $5x^2 + 2x - 1 = 0$（公式法）
(f) $2x^2 - 8x + 5 = 0$（配方法）

**8. 最值与值域**：
(a) 求 $f(x) = x^2 + 8x + 19$ 的最小值。
(b) 求 $f(x) = -2x^2 + 8x - 3$ 的最大值。
(c) 求 $f(x) = x^2 - 6x + 10$ 在 $[1, 5]$ 上的值域。
(d) 求 $f(x) = -x^2 + 2x + 3$ 在 $[-1, 4]$ 上的值域。

**9. 二次不等式**：
(a) $x^2 - 3x - 10 > 0$
(b) $2x^2 - 7x + 3 \leq 0$
(c) $-x^2 + 5x - 6 \geq 0$
(d) 求 $k$ 使 $x^2 + kx + 16 > 0$ 对一切实数 $x$ 恒成立。

**10. 三次图像**：
(a) 画出 $f(x) = (x - 1)(x - 3)(x - 5)$ 的草图，标出截距。
(b) 画出 $f(x) = -(x + 2)(x - 1)(x - 3)$ 的草图，标出截距。
(c) 画出 $f(x) = (x + 1)^2(x - 4)$ 的草图，标出截距和反弹点。
(d) 画出 $y = |(x + 1)(x - 1)(x - 5)|$ 的草图。
(e) 求方程 $|(x + 2)(x - 1)(x - 4)| = 3$ 的实根个数（估算）。

**11. 三次不等式**：
(a) 解 $(x + 1)(x - 2)(x - 4) \leq 0$。
(b) 解 $-(x + 2)(x - 1)(x - 5) > 0$。
(c) 解 $(x + 1)(x - 1)(x - 3) \geq 4$。

**12. 微分求极值**：
(a) 用微分法求 $f(x) = 4x^2 - 16x + 7$ 的极值。
(b) 用微分法求 $f(x) = -5x^2 + 30x - 41$ 的极值。
(c) 已知 $f(x) = 2x^2 + kx + 3$ 在 $x = -2$ 处取极值，求 $k$ 和极值。
(d) 已知 $f(x) = -3x^2 + mx + 1$ 在 $x = 1$ 处取极值，求 $m$ 和极值。
(e) 用微分法证明 $f(x) = x^2 - 10x + 28$ 的最小值为 $3$。
(f) 用微分法和配方法分别求 $f(x) = 3x^2 - 18x + 25$ 的极值，对比两种方法。

---

<details>
<summary><strong>点击查看全部答案</strong></summary>

**1. 余数定理**：
(a) $f(2) = 5(8) - 4(4) + 3(2) - 2 = 40 - 16 + 6 - 2 = 28$。
(b) $f(-2) = 2(-8) + k(4) - 3(-2) + 1 = -16 + 4k + 6 + 1 = 4k - 9 = 15 \Rightarrow k = 6$。
(c) $x = \frac{3}{2}$：$f(\frac{3}{2}) = 8(\frac{27}{8}) - 6(\frac{9}{4}) + 4(\frac{3}{2}) - 1 = 27 - \frac{27}{2} + 6 - 1 = \frac{54 - 27 + 12 - 2}{2} = \frac{37}{2}$。

**2. 因式定理**：
(a) $f(-2) = -8 + 12 + 8 - 12 = 0$，所以 $(x+2)$ 是 $f(x)$ 的因式。✓
(b) $f(2) = 24 + 4a + 2b - 10 = 14 + 4a + 2b = 0 \Rightarrow 2a + b = -7$；$f(-1) = -3 + a - b - 10 = -13 + a - b = 0 \Rightarrow a - b = 13$。解得 $a = 2$，$b = -11$。
(c) $f(3) = 54 - 45 + 3k - 6 = 3 + 3k = 0 \Rightarrow k = -1$。

**3. 分解三次多项式**：
(a) $f(2) = 8 - 12 - 20 + 24 = 0$。综合除法得 $x^2 - x - 12 = (x - 4)(x + 3)$。$f(x) = (x - 2)(x - 4)(x + 3)$。
(b) $f(1) = 3 + 2 - 7 + 2 = 0$。综合除法得 $3x^2 + 5x - 2 = (3x - 1)(x + 2)$。$f(x) = (x - 1)(3x - 1)(x + 2)$。
(c) $f(3) = 108 - 108 - 3 + 3 = 0$。综合除法得 $4x^2 - 1 = (2x + 1)(2x - 1)$。$f(x) = (x - 3)(2x + 1)(2x - 1)$。

**4. 解三次方程**：
(a) $f(1) = 0$，分解得 $(x - 1)(x + 2)(x - 3) = 0$，解为 $x = 1, -2, 3$。
(b) $f(-1) = 0$，分解得 $(x + 1)(2x - 1)(x - 2) = 0$，解为 $x = -1, \frac{1}{2}, 2$。
(c) $f(-3) = -27 + 27 + 12 + k = 12 + k = 0 \Rightarrow k = -12$。方程为 $x^3 + 3x^2 - 4x - 12 = 0$，分解得 $(x + 3)(x + 2)(x - 2) = 0$，解为 $x = -3, -2, 2$。

**5. 判别式**：
(a) $\Delta = 25 - 32 = -7 < 0$，无实根。
(b) $\Delta = 36 - 4k = 0 \Rightarrow k = 9$。
(c) $\Delta = k^2 - 36 < 0 \Rightarrow -6 < k < 6$。

**6. 直线与曲线**：
(a) 代入得 $x^2 - 5x + 5 = 0$，$\Delta = 25 - 20 = 5 > 0$，相交于两点。
(b) 代入得 $x^2 - 6x + (7 - k) = 0$，$\Delta = 36 - 4(7 - k) = 8 + 4k = 0 \Rightarrow k = -2$。
(c) 代入得 $x^2 - (m + 2)x + 5 = 0$，$\Delta = (m+2)^2 - 20 > 0 \Rightarrow m < -2 - 2\sqrt{5}$ 或 $m > -2 + 2\sqrt{5}$。

**7. 解二次方程**：
(a) $(x - 3)(x - 4) = 0$，$x = 3$ 或 $x = 4$。
(b) $(3x - 1)(x + 2) = 0$，$x = \frac{1}{3}$ 或 $x = -2$。
(c) $x = \frac{4 \pm \sqrt{16 + 24}}{4} = \frac{4 \pm \sqrt{40}}{4} = \frac{4 \pm 2\sqrt{10}}{4} = \frac{2 \pm \sqrt{10}}{2}$。
(d) $(x - 4)^2 = 3$，$x = 4 \pm \sqrt{3}$。
(e) $x = \frac{-2 \pm \sqrt{4 + 20}}{10} = \frac{-2 \pm \sqrt{24}}{10} = \frac{-2 \pm 2\sqrt{6}}{10} = \frac{-1 \pm \sqrt{6}}{5}$。
(f) $2(x - 2)^2 = 3$，$(x - 2)^2 = \frac{3}{2}$，$x = 2 \pm \frac{\sqrt{6}}{2}$。

**8. 最值与值域**：
(a) $f(x) = (x + 4)^2 + 3$，最小值 $3$。
(b) $f(x) = -2(x - 2)^2 + 5$，最大值 $5$。
(c) $f(x) = (x - 3)^2 + 1$，顶点 $x=3$ 在 $[1,5]$ 内，$f(3)=1$，$f(1)=5$，$f(5)=5$，值域 $[1,5]$。
(d) $f(x) = -(x - 1)^2 + 4$，顶点 $x=1$ 在 $[-1,4]$ 内，$f(1)=4$，$f(-1)=0$，$f(4)=-5$，值域 $[-5,4]$。

**9. 二次不等式**：
(a) $(x - 5)(x + 2) > 0$，$x < -2$ 或 $x > 5$。
(b) $(2x - 1)(x - 3) \leq 0$，$\frac{1}{2} \leq x \leq 3$。
(c) 乘 $-1$ 得 $x^2 - 5x + 6 \leq 0$，$(x - 2)(x - 3) \leq 0$，$2 \leq x \leq 3$。
(d) $\Delta = k^2 - 64 < 0 \Rightarrow -8 < k < 8$。

**10. 三次图像**：
(a) $x$ 截距 $1,3,5$，$y$ 截距 $(-1)(-3)(-5) = -15$，$a>0$ 左下到右上。
(b) $x$ 截距 $-2,1,3$，$y$ 截距 $-(2)(-1)(-3) = 6$，$a<0$ 左上到右下。
(c) $x$ 截距 $-1$（二重根，反弹）、$4$（单根，穿过），$y$ 截距 $(1)^2(-4) = -4$，$a>0$ 左下到右上。
(d) $f(x)$ 在 $x<-1$ 负，$-1<x<1$ 正，$1<x<5$ 负，$x>5$ 正。翻折 $x<-1$ 和 $1<x<5$ 部分。
(e) 约 5 个实根。

**11. 三次不等式**：
(a) 符号：$x<-1$（$-$），$-1<x<2$（$+$），$2<x<4$（$-$），$x>4$（$+$）。$\leq 0$：$x \leq -1$ 或 $2 \leq x \leq 4$。
(b) $f(x) > 0$：$x<-2$ 或 $1<x<5$。
(c) 需解 $x^3 - 3x^2 - x - 1 = 0$，非整数根，考试中会给出交点或用计算器求解。

**12. 微分求极值**：
(a) $f'(x) = 8x - 16 = 0 \Rightarrow x = 2$，$f''(x) = 8 > 0$，最小值 $f(2) = 16 - 32 + 7 = -9$。
(b) $f'(x) = -10x + 30 = 0 \Rightarrow x = 3$，$f''(x) = -10 < 0$，最大值 $f(3) = -45 + 90 - 41 = 4$。
(c) $f'(x) = 4x + k$，$f'(-2) = -8 + k = 0 \Rightarrow k = 8$。$f''(x) = 4 > 0$，极小值 $f(-2) = 8 - 16 + 3 = -5$。
(d) $f'(x) = -6x + m$，$f'(1) = -6 + m = 0 \Rightarrow m = 6$。$f''(x) = -6 < 0$，最大值 $f(1) = -3 + 6 + 1 = 4$。
(e) $f'(x) = 2x - 10 = 0 \Rightarrow x = 5$，$f''(x) = 2 > 0$，最小值 $f(5) = 25 - 50 + 28 = 3$。证毕。✓
(f) **微分法**：$f'(x) = 6x - 18 = 0 \Rightarrow x = 3$，$f''(x) = 6 > 0$，最小值 $f(3) = 27 - 54 + 25 = -2$。
**配方法**：$f(x) = 3(x^2 - 6x) + 25 = 3[(x - 3)^2 - 9] + 25 = 3(x - 3)^2 - 27 + 25 = 3(x - 3)^2 - 2$。最小值 $-2$ 在 $x=3$ 处。✓
**对比**：微分法只需三步（求导→令零→二阶导），配方法需要配方运算。对于二次函数两者难度相当，但对于更复杂的函数微分法更具优势。

</details>

---
---

