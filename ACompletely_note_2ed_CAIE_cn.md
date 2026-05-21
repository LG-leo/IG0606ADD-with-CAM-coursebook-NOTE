# IGCSE 0606 附加数学综合笔记第二版本

本笔记严格按照 **剑桥 IGCSE 附加数学（0606）2028–2030 考纲** 编写。附加数学课程位于 IGCSE 普通数学之上，旨在拓展代数、函数、几何、三角与微积分的深度，为 AS/A Level Further Math, AP calculus BC, IB AA HL 数学打下坚实基础。

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
| **11.2** | *Know and use the notation $`n!`$ and the expressions for permutations and combinations of $`n`$ items taken $`r`$ at a time. Includes $`0! = 1`$.* | 掌握 $`n!`$、$`^nP_r`$、$`^nC_r`$ 的记号与表达式 | §1.2.2, §1.2.3 |
| **11.3** | *Solve problems on arrangement and selection using permutations or combinations. Problems will be either in an everyday context or based on an algebraic problem. Problems involving: repetition of objects; objects arranged in a circle; both permutations and combinations, are **not** included.* | 用排列或组合解决排列与选择问题（日常生活或代数背景）。不考重复元素、圆排列、排列组合混合。 | §1.2.5 |
| **12.1** | *Use the binomial theorem for expansion of $`(a+b)^n`$ for positive integer $`n`$. Includes simplification of coefficients.* | 使用二项式定理展开 $`(a+b)^n`$（$`n`$ 为正整数），包含系数的化简 | §1.3.1 |
| **12.2** | *Use the general term $`^nC_r a^{n-r} b^r`$, $`0 ≤ r ≤ n`$. For example: Find the term independent of $`x`$ in the expansion of $`(x^2 + 1/x)^{10}`$. Knowledge of the greatest term and properties of the coefficients is **not** required.* | 使用通项公式求特定项（如常数项）。不考最大项和系数性质。 | §1.3.2, §1.3.3 |
| **12.3** | *Recognise arithmetic and geometric progressions and understand the difference between them.* | 识别等差数列与等比数列，理解它们之间的区别 | §1.1.4 |
| **12.4** | *Use the formulas for the $`n`$th term and for the sum of the first $`n`$ terms to solve problems involving arithmetic or geometric progressions. Problems may be in context.* | 使用第 $`n`$ 项和前 $`n`$ 项和公式解决等差/等比数列问题（可能含实际情境） | §1.1.2, §1.1.3 |
| **12.5** | *Use the condition for the convergence of a geometric progression, and the formula for the sum to infinity of a convergent geometric progression. Includes explaining why a particular geometric progression has or does not have a sum to infinity.* | 使用等比数列的收敛条件及无穷和公式，**包含解释为什么某个等比级数有/无无穷和** | §1.1.3 |

---

## 1.1 数列（等差与等比）

数列是按顺序排列的一列数。附加数学中重点考察两种最基本的数列：**等差数列**（相邻两项的差固定）和**等比数列**（相邻两项的比固定）。

### 1.1.1 求和符号 Σ

在深入讨论数列之前，我们需要掌握求和符号 Σ（希腊字母 Sigma）。它表示将一系列数相加：

$$`
Σ_{k=1}^{n} a_k = a_1 + a_2 + a_3 + … + a_n
`$$

求和运算满足三条基本法则：

**法则 1——常数因子提取**：

$$`
Σ_{k=1}^{n} (c · a_k) = c · Σ_{k=1}^{n} a_k
`$$

**法则 2——和的拆分**：

$$`
Σ_{k=1}^{n} (a_k ± b_k) = Σ_{k=1}^{n} a_k ± Σ_{k=1}^{n} b_k
`$$

**法则 3——常数的和**：

$$`
Σ_{k=1}^{n} c = n c
`$$

**示例**：计算 $`Σ_{k=1}^{5} (3k - 2)`$。

$$`
Σ_{k=1}^{5} (3k - 2) = 3 Σ_{k=1}^{5} k - Σ_{k=1}^{5} 2 = 3 × (1+2+3+4+5) - 5 × 2 = 3 × 15 - 10 = 45 - 10 = 35
`$$

---

### 1.1.2 等差数列（Arithmetic Progression）

#### 定义

一个数列如果从第二项起，每一项与它的前一项的差等于**同一个常数**，则称为**等差数列**。这个常数叫做**公差**，记作 $`d`$：

$$`
a_{n+1} - a_n = d  (对所有 n ≥ 1 成立)
`$$

**示例**：$`5, 9, 13, 17, 21`$ 是等差数列，$`d=4`$，$`a=5`$。

#### 第 $`n`$ 项公式（推导）

设首项 $`a_1 = a`$，则：

$$`
a_2 = a + d
`$$

$$`
a_3 = a_2 + d = a + 2d
`$$

$$`
a_4 = a_3 + d = a + 3d
`$$

规律：第 $`n`$ 项是在首项的基础上加了 $`(n-1)`$ 次公差。

$$`
a_n = a + (n-1)d
`$$

**验证**：$`n=1`$ 时 $`a_1 = a`$；$`n=2`$ 时 $`a_2 = a + d`$。正确。

#### 前 $`n`$ 项和公式（推导——倒序相加法）

$$`
S_n = a + (a+d) + (a+2d) + … + [a+(n-1)d]
`$$

$$`
S_n = [a+(n-1)d] + [a+(n-2)d] + … + a
`$$

两式相加，每一对的和均为 $`2a + (n-1)d`$，共 $`n`$ 对：

$$`
2S_n = n[2a + (n-1)d]
`$$

$$`
S_n = n/2 · [2a + (n-1)d]
`$$

若末项 $`l = a_n = a + (n-1)d`$，则：

$$`
S_n = n/2 · (a + l)
`$$

#### 例题

**例题 1**：首项 $`7`$，公差 $`3`$，求第 $`15`$ 项。

$$`
a_{15} = 7 + 14 × 3 = 7 + 42 = 49
`$$

---

**例题 2**：首项 $`2`$，公差 $`5`$，前 $`n`$ 项和 $`156`$，求 $`n`$。

$$`
n/2 · [4 + (n-1) × 5] = 156  ⇒  n/2 · (5n - 1) = 156
`$$

$$`
5n^2 - n - 312 = 0  ⇒  n = (1 ± √(1 + 6240))/10 = (1 ± 79)/10
`$$

$`n`$ 为正整数，$`n = 80/10 = 8`$。

---

**例题 3**（实际情境）：第一年存 $`500`$ 元，之后每年多存 $`50`$ 元。$`10`$ 年共存多少钱？

$$`
S_{10} = 10/2 · [2 × 500 + 9 × 50] = 5 × (1000 + 450) = 7250
`$$

答：$`7250`$ 元。

---

### 1.1.3 等比数列（Geometric Progression）

#### 定义

一个数列如果从第二项起，每一项与它的前一项的比值等于**同一个常数**，则称为**等比数列**。这个常数叫做**公比**，记作 $`r`$：

$$`
a_{n+1} / a_n = r  (对所有 n ≥ 1 成立)
`$$

**示例**：$`2, 6, 18, 54, 162`$ 是等比数列，$`r=3`$，$`a=2`$。

#### 第 $`n`$ 项公式

$$`
a_2 = a r
`$$

$$`
a_3 = a_2 · r = a r^2
`$$

$$`
a_4 = a_3 · r = a r^3
`$$

$$`
a_n = a r^{n-1}
`$$

#### 前 $`n`$ 项和公式（推导——错位相减法）

$$`
S_n = a + a r + a r^2 + … + a r^{n-1}
`$$

$$`
r S_n = a r + a r^2 + a r^3 + … + a r^{n}
`$$

相减：

$$`
S_n - r S_n = a - a r^{n}
`$$

$$`
S_n(1 - r) = a(1 - r^{n})
`$$

若 $`r = 1`$：$`S_n = n a`$。

若 $`r ≠ 1`$：

$$`
S_n = a · (1 - r^{n})/(1 - r) 或等价地  S_n = a · (r^{n} - 1)/(r - 1)
`$$

#### 无穷等比级数的收敛条件与和（**考纲 12.5 重点**）

$$`
S_∞ = \lim_{n → ∞} S_n = \lim_{n → ∞} a · (1 - r^{n})/(1 - r)
`$$

$`r^{n}`$ 在 $`n → ∞`$ 时的行为决定了级数是否收敛：

| $`r`$ 的取值范围 | $`n → ∞`$ 时 $`r^{n}`$ 的行为 | 级数是否收敛 | 无穷和 |
|:-------------:|----------------------------------|:-----------:|:------:|
| $`|r| < 1`$ | $`r^{n} → 0`$ | ✅ **收敛** | $`S_∞ = a/(1-r)`$ |
| $`|r| > 1`$ | $`|r^{n}| → ∞`$ | ❌ **发散** | 无有限和 |
| $`r = 1`$ | $`r^{n} = 1`$（恒定） | ❌ **发散** | $`S_n = n a → ∞`$ |
| $`r = -1`$ | 在 $`1`$ 和 $`-1`$ 之间振荡 | ❌ **发散** | 和不确定 |

因此，**等比级数收敛的充要条件是 $`|r| < 1`$**。

考试中如果被要求"解释为什么某个等比级数有/没有无穷和"，你需要说明：当 $`|r| < 1`$ 时，$`n → ∞`$ 使 $`r^{n} → 0`$，因此 $`S_n → a/(1-r)`$；当 $`|r| ≥ 1`$ 时，$`r^{n}`$ 不趋近于 $`0`$，$`S_n`$ 不趋近于有限值。

#### 例题

**例题 1**：首项 $`3`$，公比 $`2`$，求第 $`6`$ 项。

$$`
a_6 = 3 × 2^5 = 3 × 32 = 96
`$$

---

**例题 2**（收敛判断 + 无穷和）：$`12 + 6 + 3 + 3/2 + …`$

首项 $`a = 12`$，公比 $`r = 6/12 = 1/2`$。

因为 $`|r| = 1/2 < 1`$，当 $`n → ∞`$ 时 $`(1/2)^{n} → 0`$，所以级数收敛。

$$`
S_∞ = 12/(1 - 1/2) = 12/(1/2) = 24
`$$

---

**例题 3**（已知 $`S_∞`$ 求 $`r`$）：无穷等比级数收敛，和为 $`8`$，首项为 $`4`$，求公比 $`r`$。

$$`
8 = 4/(1 - r)  ⇒  8(1 - r) = 4  ⇒  1 - r = 1/2  ⇒  r = 1/2
`$$

验证：$`|r| = 1/2 < 1`$，满足收敛条件。

---

### 1.1.4 对照：等差数列 vs 等比数列（**考纲 12.3 重点**）

| 特征 | 等差数列 (AP) | 等比数列 (GP) |
|:----|:-------------|:-------------|
| **定义性质** | $`a_{n+1} - a_n = d`$（差恒定） | $`a_{n+1} / a_n = r`$（比恒定） |
| **检查方法** | 相邻项相减，看是否恒等 | 相邻项相除，看是否恒等 |
| **第 $`n`$ 项** | $`a_n = a + (n-1)d`$ | $`a_n = a r^{n-1}`$ |
| **前 $`n`$ 项和** | $`S_n = n/2 · [2a + (n-1)d]`$ | $`S_n = a(1-r^n)/(1-r)`$（$`r ≠ 1`$） |
| **增长模式** | **线性增长**（每次加固定值） | **指数增长/衰减**（每次乘固定值） |
| **无穷和** | 不存在（除 $`d=0`$ 常数数列） | $`|r| < 1`$ 时收敛于 $`a/(1-r)`$ |

**判断练习**：

1. $`5, 8, 11, 14, 17, …`$ → 差恒为 $`3`$ → **AP** ✓
2. $`5, 10, 20, 40, 80, …`$ → 比恒为 $`2`$ → **GP** ✓
3. $`1, 4, 9, 16, 25, …`$ → 差为 $`3,5,7,9`$（不恒定），比为 $`4, 2.25, 1.78, …`$（不恒定）→ **两者都不是** ✗
4. $`100, 50, 25, 12.5, …`$ → 比恒为 $`1/2`$ → **GP**（收敛）✓

---

## 1.2 排列与组合

排列与组合回答同一个基本问题："有多少种不同的方式？"二者的核心区别在于 **顺序是否重要**。

### 1.2.1 乘法原理

如果一项任务可以分解为 $`k`$ 个依次进行的步骤，第 $`i`$ 步有 $`m_i`$ 种方法，则总方法数为：

$$`
m_1 × m_2 × … × m_k
`$$

**示例**：A→B 有 $`3`$ 条路，B→C 有 $`4`$ 条路，A→B→C 共有 $`3 × 4 = 12`$ 条路线。

### 1.2.2 排列——顺序重要（Permutations）

**定义**：从 $`n`$ 个不同元素中取出 $`r`$ 个（$`r ≤ n`$），按一定顺序排成一列。顺序不同算不同排列。记作 $`^nP_r`$ 或 $`P(n,r)`$。

**推导**：

$$`
^nP_r = n(n-1)(n-2)…(n-r+1)
`$$

用阶乘表示：

$$`
^nP_r = n!/(n-r)!
`$$

**特殊值**：$`^nP_n = n!`$，$`^nP_0 = 1`$，$`0! = 1`$。

### 1.2.3 组合——顺序不重要（Combinations）

**定义**：从 $`n`$ 个不同元素中取出 $`r`$ 个（$`r ≤ n`$），不考虑顺序。记作 $`^nC_r`$、$`C(n,r)`$ 或 $`^nC_r`$。

**推导**：排列数除以内部排列数：

$$`
^nC_r = ^nP_r / r! = n!/(r! (n-r)!)
`$$

**性质**：

- 对称性：$`^nC_r = ^nC_{n-r}`$
- 边界值：$`^nC_0 = ^nC_n = 1`$，$`^nC_1 = ^nC_{n-1} = n`$

### 1.2.4 如何选择？（**考纲 11.1 重点**）

问自己：**交换任意两个已选元素，结果是否不同？**

| 情境 | 顺序重要？ | 使用 | 示例 |
|:----|:---------:|:----|:-----|
| 排队、名次、密码、排名 | ✅ 是 | **排列** $`^nP_r`$ | 6 人选 3 人站一排 |
| 委员会、选科、抽奖、组队 | ❌ 否 | **组合** $`^nC_r`$ | 6 人选 3 人组委员会 |

### 1.2.5 应用题例题

**例题 1**（排列——日常生活）：6 本不同的书选 4 本排上书架（从左到右），多少种摆法？

$$`
^6P_4 = 6!/(6-4)! = 6!/2! = 6 × 5 × 4 × 3 = 360
`$$

答：$`360`$ 种。

---

**例题 2**（组合——日常生活）：7 男 5 女中选 4 人组委员会，要求至少 2 名女生，多少种选法？

- $`2`$ 女 $`2`$ 男：$`^5C_2 × ^7C_2 = 10 × 21 = 210`$
- $`3`$ 女 $`1`$ 男：$`^5C_3 × ^7C_1 = 10 × 7 = 70`$
- $`4`$ 女 $`0`$ 男：$`^5C_4 × ^7C_0 = 5 × 1 = 5`$

总方法数：$`210 + 70 + 5 = 285`$。

> **补集法验证**：总数 $`^{12}C_4 = 495`$，减去"至多 1 名女生"（$`0`$ 女 $`4`$ 男 $`= ^5C_0 · ^7C_4 = 35`$，$`1`$ 女 $`3`$ 男 $`= ^5C_1 · ^7C_3 = 5×35 = 175`$，共 $`210`$），$`495 - 210 = 285`$ ✓

---

**例题 3**（代数背景——组合恒等式）：证明 $`^nC_r + ^nC_{r-1} = ^{n+1}C_r`$，并用此计算 $`^8C_3 + ^8C_2`$。

**证明**：

$$`
^nC_r + ^nC_{r-1}
= n!/(r!(n-r)!) + n!/((r-1)!(n-r+1)!)
`$$

$$`
= n!/(r!(n-r+1)!) · [(n-r+1) + r]
`$$

$$`
= (n! · (n+1))/(r!(n-r+1)!)
= (n+1)!/(r!(n+1-r)!)
= ^{n+1}C_r
`$$

**应用**：

$$`
^8C_3 + ^8C_2 = ^9C_3 = (9 × 8 × 7)/(3 × 2 × 1) = 84
`$$

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

$`(a+b)^n`$ 可看作 $`n`$ 个 $`(a+b)`$ 相乘。展开时，每一项是分别从每个因子选 $`a`$ 或 $`b`$ 的乘积。要得到 $`a^{n-r} b^{r}`$，需从 $`r`$ 个因子中选 $`b`$，从 $`n-r`$ 个因子中选 $`a`$。选择方式数为 $`^nC_r`$。

对 $`r = 0, 1, …, n`$ 求和：

$$`
(a+b)^n = Σ_{r=0}^{n} ^nC_r a^{n-r} b^{r}
`$$

**示例**：展开 $`(x+3)^4`$。

$$`
(x+3)^4 = ^4C_0 x^4 (3)^0 + ^4C_1 x^3 (3)^1 + ^4C_2 x^2 (3)^2 + ^4C_3 x^1 (3)^3 + ^4C_4 x^0 (3)^4
`$$

$$`
= 1 · x^4 + 4 · 3x^3 + 6 · 9x^2 + 4 · 27x + 1 · 81
`$$

$$`
= x^4 + 12x^3 + 54x^2 + 108x + 81
`$$

注意：每一项的系数都经过了**化简**（如 $`4 × 3 = 12`$，$`6 × 9 = 54`$），这是考纲明确要求的。

### 1.3.2 通项公式与特定项（**考纲 12.2**）

展开式中的第 $`(r+1)`$ 项（从 $`r=0`$ 开始计数）：

$$`
T_{r+1} = ^nC_r a^{n-r} b^{r}
`$$

常见题型：

| 题型 | 方法 |
|:----|:----|
| 求 $`x^k`$ 的系数 | 设通项中 $`x`$ 的指数 $`= k`$，解出 $`r`$ |
| 求常数项（不含 $`x`$） | 设 $`x`$ 的指数 $`= 0`$，解出 $`r`$ |
| 求 $`x^p y^q`$ 的系数 | 分别设 $`x`$ 和 $`y`$ 的指数匹配 |

> **⚠️ 重要区分**：
> - **二项式系数** = $`^nC_r`$（只与 $`n, r`$ 有关）
> - **完整系数** = $`^nC_r`$ × $`a`$ 和 $`b`$ 中的常数因子及符号
>
> 例如 $`(2x-3)^5`$ 中 $`r=2`$：二项式系数 $`^5C_2 = 10`$，完整系数 $`= 10 · (2)^3 · (-3)^2 = 720`$

### 1.3.3 例题

**例题 1**（求指定幂次的系数）：求 $`(2x + 1/x)^7`$ 展开式中 $`x`$ 的系数。

**解**：

$$`
T_{r+1} = ^7C_r (2x)^{7-r} (1/x)^{r}
= ^7C_r 2^{7-r} x^{7-r} · x^{-r}
= ^7C_r 2^{7-r} x^{7-2r}
`$$

令 $`7-2r = 1`$，得 $`r = 3`$。

$$`
T_4 = ^7C_3 2^{4} x = 35 × 16 × x = 560x
`$$

所以 $`x`$ 的系数为 $`560`$。

---

**例题 2**（求常数项——考纲典型）：求 $`(x^2 - 2/x)^6`$ 展开式中的常数项。

**解**：

$$`
T_{r+1} = ^6C_r (x^2)^{6-r} (-2/x)^{r}
= ^6C_r (-2)^r x^{12-2r} · x^{-r}
= ^6C_r (-2)^r x^{12-3r}
`$$

令 $`12 - 3r = 0`$，得 $`r = 4`$。

$$`
T_5 = ^6C_4 (-2)^4 = 15 × 16 = 240
`$$

所以常数项为 $`240`$。

---

**例题 3**（两个二项式乘积的系数）：求 $`(1+x)^5 (2-x)^4`$ 展开式中 $`x^2`$ 的系数。

**解**：

$`(1+x)^5`$ 通项：$`^5C_r x^r`$
$`(2-x)^4`$ 通项：$`^4C_k 2^{4-k} (-1)^k x^k`$

需要 $`r + k = 2`$：

| $`r`$ | $`k`$ | 计算 | 贡献 |
|:--:|:--:|:----|:----:|
| $`0`$ | $`2`$ | $`^5C_0 · ^4C_2 2^{2} (-1)^2 = 1 × 6 × 4 × 1`$ | $`24`$ |
| $`1`$ | $`1`$ | $`^5C_1 · ^4C_1 2^{3} (-1)^1 = 5 × 4 × 8 × (-1)`$ | $`-160`$ |
| $`2`$ | $`0`$ | $`^5C_2 · ^4C_0 2^{4} (-1)^0 = 10 × 1 × 16 × 1`$ | $`160`$ |

总和：$`24 + (-160) + 160 = 24`$。

答：$`x^2`$ 的系数为 $`24`$。

---

### 1.3.4 二项式系数的性质（杨辉三角）

**对称性**：

$$`
^nC_r = ^nC_{n-r}
`$$

**杨辉法则**（递推关系）：

$$`
^nC_r + ^nC_{r-1} = ^{n+1}C_r
`$$

**杨辉三角**：

`
n=0: 1
n=1: 1 1
n=2: 1 2 1
n=3: 1 3 3 1
n=4: 1 4 6 4 1
n=5: 1 5 10 10 5 1
`


> **考试提示**：$`n ≤ 5`$ 时可用杨辉三角直接写系数，$`n ≥ 6`$ 时用组合数公式 $`^nC_r`$。

> **不考内容**（考纲明确说明）：最大项（greatest term）和系数的性质（properties of the coefficients）不考。

---

## 本章公式速查表

| 主题 | 公式 | 条件 |
|:----|:----|:----|
| AP 第 $`n`$ 项 | $`a_n = a + (n-1)d`$ | — |
| AP 前 $`n`$ 项和 | $`S_n = n/2 · [2a + (n-1)d]`$ | — |
| GP 第 $`n`$ 项 | $`a_n = a r^{n-1}`$ | — |
| GP 前 $`n`$ 项和 | $`S_n = a(1-r^n)/(1-r)`$ | $`r ≠ 1`$ |
| GP 无穷和 | $`S_∞ = a/(1-r)`$ | $`|r| < 1`$ |
| 排列数 | $`^nP_r = n!/(n-r)!`$ | 顺序重要 |
| 组合数 | $`^nC_r = n!/(r!(n-r)!)`$ | 顺序不重要 |
| 二项式定理 | $`(a+b)^n = Σ_{r=0}^{n} ^nC_r a^{n-r} b^{r}`$ | $`n ∈ ℤ⁺`$ |
| 通项 | $`T_{r+1} = ^nC_r a^{n-r} b^{r}`$ | 用于求特定项 |

---
---








# 第 2 章：向量与变化率

## 考纲对照

本章对应剑桥 IGCSE 附加数学（0606）2028–2030 考纲的以下内容：

| 考纲编号 | 内容 | 说明 |
|---------|------|------|
| **13.1** | 理解并使用向量记号 | 列向量、**i**–**j** 形式、$`\overrightarrow{AB}`$、**p** 等形式 |
| **13.2** | 位置向量与单位向量 | 求单位向量 $`\hat{\mathbf{a}} = \frac{\mathbf{a}}{|\mathbf{a}|}`$ |
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
`\mathbf{v} = \begin{pmatrix} x \\ y \end{pmatrix}`
$$

其中 $`x`$ 是水平分量，$`y`$ 是垂直分量。这种表示法在解方程组时非常方便，因为我们可以直接对分量进行操作。

#### 表示法 2：**i**–**j** 形式

定义两个基本单位向量：

$$
`\mathbf{i} = (1, 0)^\mathrm{T},\quad \mathbf{j} = (0, 1)^\mathrm{T}`
$$

**i** 指向正 $`x`$ 轴方向（向右），**j** 指向正 $`y`$ 轴方向（向上）。那么任意向量可以写为：

$$
`\mathbf{v} = x\mathbf{i} + y\mathbf{j}`
$$

**两种表示法的等价性**：

$$
`x\mathbf{i} + y\mathbf{j} = (x, y)^\mathrm{T}`
$$

例如，向量 $`3\mathbf{i} - 2\mathbf{j}`$ 与列向量 $`(3, -2)^\mathrm{T}`$ 是同一个向量。

#### 表示法 3：有向线段

从点 $`A`$ 到点 $`B`$ 的向量记作 $`\overrightarrow{AB}`$。它等于终点位置减去起点位置：

$$
`\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A`
$$

> **为什么是"终点减起点"？** 假设你想从家 $`A`$ 走到学校 $`B`$。你的位移（从 $`A`$ 到 $`B`$）就是你最终到达的位置（学校的位置）减去你出发时的位置（家的位置）。如果 $`A`$ 在 $`(1,1)`$，$`B`$ 在 $`(4,5)`$，那么你需要向右走 3 个单位、向上走 4 个单位，即 $`\overrightarrow{AB} = (3,4)`$。

---

### 2.1.2 位置向量

设 $`O`$ 为原点。任意点 $`P(x, y)`$ 的**位置向量**是：

$$
`\mathbf{r} = \overrightarrow{OP} = (x, y)^\mathrm{T} = x\mathbf{i} + y\mathbf{j}`
$$

位置向量告诉我们点 $`P`$ 相对于原点的位置。这里的关键区分是：**点** $`P(x, y)`$ 是空间中的一个位置，而**向量** $`\mathbf{r} = (x, y)`$ 是从原点到该点的有向线段——它包含了位移的信息。

> **点和向量的区别**：点是一个位置，像地图上的一个坐标。向量是一个位移，像"向右 3 步，向上 2 步"。同一个向量可以从任何起点出发，但同一个点只能在一个位置。

---

### 2.1.3 向量的模（大小）

向量 $`\mathbf{v} = x\mathbf{i} + y\mathbf{j}`$ 的模（或称长度、大小）由勾股定理给出：

$$
`|\mathbf{v}| = \sqrt{x^2 + y^2}`
$$

模一定是非负实数。当且仅当向量是零向量 $`\mathbf{0} = (0, 0)^\mathrm{T}`$ 时，模为零。

> **为什么是 $`\sqrt{x^2 + y^2}`$？** 把向量 $`\mathbf{v}`$ 看作从原点 $`(0,0)`$ 到点 $`(x,y)`$ 的线段。这条线段就是直角三角形的斜边，两条直角边的长度分别是 $`|x|`$ 和 $`|y|`$。根据勾股定理，斜边长度 $`= \sqrt{x^2 + y^2}`$。

---

### 2.1.4 单位向量

**单位向量**是模为 1 的向量。给定任意非零向量 $`\mathbf{v}`$，我们可以构造与它同方向的单位向量 $`\hat{\mathbf{v}}`$：

$$
`\hat{\mathbf{v}} = \frac{\mathbf{v}}{|\mathbf{v}|}`
$$

也就是说，将原向量除以它自己的模。这个操作称为**归一化**。

> **为什么这样定义？** 设 $`\hat{\mathbf{v}} = \frac{\mathbf{v}}{|\mathbf{v}|}`$，那么
> $$
`|\hat{\mathbf{v}}| = \frac{|\mathbf{v}|}{|\mathbf{v}|} = 1`$$
> 方向保持不变，因为我们在用正标量除以原向量。
>
> **类比**：就像把一段绳子切成单位长度的小段。如果你有一根 5 米长的绳子，把它切成 5 等份，每份就是 1 米，方向与原来相同。

---

### 2.1.5 向量的加法与减法

两个向量的加法，就是将它们的对应分量分别相加：

$$
`(x_1, y_1)^\mathrm{T} + (x_2, y_2)^\mathrm{T} = (x_1 + x_2,\; y_1 + y_2)^\mathrm{T}`
$$

减法同理：

$$
`(x_1, y_1)^\mathrm{T} - (x_2, y_2)^\mathrm{T} = (x_1 - x_2,\; y_1 - y_2)^\mathrm{T}`
$$

**几何意义——为什么是"平行四边形法则"？**

想象两个人同时拉一个箱子。一个人用力 $`\mathbf{a}`$ 向东拉，另一个人用力 $`\mathbf{b}`$ 向北拉。箱子实际受到的合力就是 $`\mathbf{a} + \mathbf{b}`$。

- **加法——平行四边形法则**：以两个向量为邻边作平行四边形，从起点出发的对角线即为它们的和。
- **减法——三角形法则**：$`\mathbf{a} - \mathbf{b}`$ 等于从 $`\mathbf{b}`$ 的终点指向 $`\mathbf{a}`$ 的终点的向量。

**实用的口诀**：
- 对于位移向量：**终点减起点**。从 $`A`$ 到 $`B`$ 的向量 $`\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A`$
- 对于加法：首尾相连，从第一个起点指向最后一个终点

---

### 2.1.6 向量的数乘

向量乘以一个标量 $`c`$，相当于每个分量都乘以 $`c`$：

$$
`c\,(x, y)^\mathrm{T} = (cx,\; cy)^\mathrm{T}`
$$

数乘的几何效果：
- 如果 $`c > 0`$，向量沿原方向拉伸（$`c > 1`$）或压缩（$`0 < c < 1`$）
- 如果 $`c < 0`$，向量反向

数乘后的模：

$$
`|c\mathbf{v}| = |c| \cdot |\mathbf{v}|`
$$

> **为什么模会乘以 $`|c|`$ 而不是 $`c`$？** 因为如果 $`c = -2`$，向量的长度变为原来的 2 倍，方向反转。长度是正数，所以取 $`|c| = 2`$。

---

### 2.1.7 向量相等

两个向量相等当且仅当它们的对应分量分别相等。即：

$$
`(x_1, y_1)^\mathrm{T} = (x_2, y_2)^\mathrm{T} \iff x_1 = x_2 \;\text{且}\; y_1 = y_2`
$$

这称为**向量相等原理**（equating like vectors）——它是解向量方程的核心工具。

> **为什么这个原理如此有用？** 一个向量方程实际上包含了两个独立的标量方程（一个对应 $`x`$ 分量，一个对应 $`y`$ 分量）。这让我们能从两个方向分别求解未知数。

---

### 2.1.8 垂直向量（正交向量）

#### 什么是垂直？

两个非零向量 $`\mathbf{u}`$ 和 $`\mathbf{v}`$ 垂直（或称正交）当且仅当它们之间的夹角是 $`90^\circ`$。

#### 如何判断垂直？——点积

两个向量的**点积（内积，dot product）**定义为：

$$
`\mathbf{u} \cdot \mathbf{v} = u_x v_x + u_y v_y`
$$

点积的结果是一个**标量**（不是向量），因此也称为"标量积"。

**垂直的判定条件**：

$$
`\mathbf{u} \perp \mathbf{v} \iff \mathbf{u} \cdot \mathbf{v} = 0`
$$

> **为什么点积为零代表垂直？**
>
> 从几何角度理解，点积还有另一个等价的定义：
> $$
`\mathbf{u} \cdot \mathbf{v} = |\mathbf{u}|\,|\mathbf{v}|\,\cos\theta`$$
> 其中 $`\theta`$ 是两个向量之间的夹角。
>
> 推导这个等价关系：利用余弦定理。设 $`\mathbf{u}`$ 和 $`\mathbf{v}`$ 的夹角为 $`\theta`$，则向量 $`\mathbf{u} - \mathbf{v}`$ 的模满足：
> $$
`|\mathbf{u} - \mathbf{v}|^2 = |\mathbf{u}|^2 + |\mathbf{v}|^2 - 2|\mathbf{u}||\mathbf{v}|\cos\theta`$$
> 同时展开左边：
> $$
`|\mathbf{u} - \mathbf{v}|^2 = (u_x - v_x)^2 + (u_y - v_y)^2 = (u_x^2 + u_y^2) + (v_x^2 + v_y^2) - 2(u_x v_x + u_y v_y)`$$
> 比较两式，得：
> $$
`|\mathbf{u}|^2 + |\mathbf{v}|^2 - 2|\mathbf{u}||\mathbf{v}|\cos\theta = |\mathbf{u}|^2 + |\mathbf{v}|^2 - 2(u_x v_x + u_y v_y)`$$
> 因此 $`u_x v_x + u_y v_y = |\mathbf{u}||\mathbf{v}|\cos\theta`$。
>
> 当 $`\theta = 90^\circ`$ 时，$`\cos 90^\circ = 0`$，所以点积为零。

#### 水平向量与垂直向量

一个特殊的例子：**水平向量**的 $`y`$ 分量为零，即 $`\mathbf{h} = (h_x, 0)`$（$`h_x \neq 0`$），它的方向平行于 $`x`$ 轴。**垂直向量**的 $`x`$ 分量为零，即 $`\mathbf{v} = (0, v_y)`$（$`v_y \neq 0`$），它的方向平行于 $`y`$ 轴。

水平向量总是垂直于垂直向量。用点积验证：

$$
`(h_x, 0) \cdot (0, v_y) = h_x \cdot 0 + 0 \cdot v_y = 0`
$$

#### 通过斜率判断垂直

如果两个非零向量都不与坐标轴平行（即 $`x`$ 和 $`y`$ 分量均不为零），我们也可以用斜率来判断垂直。设向量 $`\mathbf{u}`$ 的斜率为 $`k_1 = \frac{u_y}{u_x}`$，向量 $`\mathbf{v}`$ 的斜率为 $`k_2 = \frac{v_y}{v_x}`$，那么：

$$
`\mathbf{u} \perp \mathbf{v} \iff k_1 \cdot k_2 = -1`
$$

> **推导**：由点积为零的条件：
> $$
`u_x v_x + u_y v_y = 0 \;\Longrightarrow\; u_x v_x = -u_y v_y \;\Longrightarrow\; \frac{u_y}{u_x} \cdot \frac{v_y}{v_x} = -1`$$
> 即 $`k_1 \cdot k_2 = -1`$。

> **关于零向量的说明**：零向量 $`\mathbf{0} = (0, 0)`$ 没有固定方向。按照惯例，在技术讨论中它被视为与所有向量既平行又垂直，但在实际解题中我们通常排除它。

---

### 📌 例题 2.1：向量基础运算

**例题 1**（向量表示、模与单位向量）

已知两点 $`A(1, 2)`$ 和 $`B(5, -1)`$。

（a）求向量 $`\overrightarrow{AB}`$ 用 **i**–**j** 形式表示。
（b）求 $`|\overrightarrow{AB}|`$。
（c）求与 $`\overrightarrow{AB}`$ 同方向的单位向量。

**思路分析**：
- 从 $`A`$ 到 $`B`$ 的向量 = $`B`$ 的位置减 $`A`$ 的位置
- 模 = 各分量平方和的平方根
- 单位向量 = 原向量除以模

**解**：

（a）

$$
`\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A = (5\mathbf{i} - \mathbf{j}) - (\mathbf{i} + 2\mathbf{j}) = (5-1)\mathbf{i} + (-1-2)\mathbf{j} = 4\mathbf{i} - 3\mathbf{j}`
$$

（b）

$$
`|\overrightarrow{AB}| = \sqrt{4^2 + (-3)^2} = \sqrt{16 + 9} = \sqrt{25} = 5`
$$

（c）同方向的单位向量为：

$$
`\hat{\mathbf{v}} = \frac{4\mathbf{i} - 3\mathbf{j}}{5} = \frac{4}{5}\mathbf{i} - \frac{3}{5}\mathbf{j}`
$$

验证模长：$`\sqrt{(4/5)^2 + (-3/5)^2} = \sqrt{16/25 + 9/25} = \sqrt{25/25} = 1`$。✓

---

**例题 2**（向量加法、数乘与向量相等——解方程组）

已知 $`\mathbf{a} = 2\mathbf{i} + 3\mathbf{j}`$，$`\mathbf{b} = -\mathbf{i} + 2\mathbf{j}`$。求：

（a）$`\mathbf{a} + \mathbf{b}`$
（b）$`2\mathbf{a} - 3\mathbf{b}`$
（c）实数 $`p`$ 和 $`q`$ 使得 $`p\mathbf{a} + q\mathbf{b} = 7\mathbf{i} + 8\mathbf{j}`$

**思路分析**：
- 加法和数乘都是对分量分别操作
- 对于第（c）问，先展开左侧，利用向量相等原理（**i** 和 **j** 的系数分别相等）建立方程组

**解**：

（a）

$$
`\mathbf{a} + \mathbf{b} = (2\mathbf{i} + 3\mathbf{j}) + (-\mathbf{i} + 2\mathbf{j}) = (2-1)\mathbf{i} + (3+2)\mathbf{j} = \mathbf{i} + 5\mathbf{j}`
$$

（b）

$$
`2\mathbf{a} - 3\mathbf{b} = 2(2\mathbf{i} + 3\mathbf{j}) - 3(-\mathbf{i} + 2\mathbf{j}) = (4\mathbf{i} + 6\mathbf{j}) + (3\mathbf{i} - 6\mathbf{j}) = 7\mathbf{i} + 0\mathbf{j} = 7\mathbf{i}`
$$

（c）设 $`p\mathbf{a} + q\mathbf{b} = 7\mathbf{i} + 8\mathbf{j}`$，即：

$$
`p(2\mathbf{i} + 3\mathbf{j}) + q(-\mathbf{i} + 2\mathbf{j}) = 7\mathbf{i} + 8\mathbf{j}`
$$

先展开括号：

$$
`2p\mathbf{i} + 3p\mathbf{j} - q\mathbf{i} + 2q\mathbf{j} = 7\mathbf{i} + 8\mathbf{j}`
$$

合并 **i** 和 **j** 的系数：

$$
`(2p - q)\mathbf{i} + (3p + 2q)\mathbf{j} = 7\mathbf{i} + 8\mathbf{j}`
$$

利用向量相等原理，**i** 的系数必须相等，**j** 的系数也必须相等：

$$
`\begin{cases}
2p - q = 7 \quad (\text{① } \mathbf{i} \text{ 系数相等}) \\[4pt]
3p + 2q = 8 \quad (\text{② } \mathbf{j} \text{ 系数相等})
\end{cases}`
$$

解这个方程组。从①式得 $`q = 2p - 7`$，代入②式：

$$
`3p + 2(2p - 7) = 8 \;\Longrightarrow\; 3p + 4p - 14 = 8 \;\Longrightarrow\; 7p = 22 \;\Longrightarrow\; p = \frac{22}{7}`
$$

于是 $`q = 2 \times \frac{22}{7} - 7 = \frac{44}{7} - \frac{49}{7} = -\frac{5}{7}`$。

因此 $`p = \frac{22}{7}`$，$`q = -\frac{5}{7}`$。✓

---

**例题 3**（位置向量、位移与垂直向量判定）

三点 $`P`$、$`Q`$、$`R`$ 的位置向量分别为 $`\mathbf{p} = 3\mathbf{i} + \mathbf{j}`$，$`\mathbf{q} = 5\mathbf{i} - 2\mathbf{j}`$，$`\mathbf{r} = -2\mathbf{i} + 4\mathbf{j}`$。

（a）求 $`\overrightarrow{PQ}`$ 和 $`\overrightarrow{PR}`$。
（b）已知 $`\overrightarrow{PS} = 2\overrightarrow{PQ}`$，求 $`S`$ 的位置向量。
（c）判断 $`\overrightarrow{PQ}`$ 与 $`\overrightarrow{PR}`$ 是否垂直。

**思路分析**：
- $`\overrightarrow{PQ} = \mathbf{q} - \mathbf{p}`$（终点减起点）
- $`\overrightarrow{PS} = \mathbf{s} - \mathbf{p}`$，代入已知条件解出 $`\mathbf{s}`$
- 垂直判定：计算点积，若为零则垂直

**解**：

（a）

$$
`\overrightarrow{PQ} = \mathbf{q} - \mathbf{p} = (5\mathbf{i} - 2\mathbf{j}) - (3\mathbf{i} + \mathbf{j}) = 2\mathbf{i} - 3\mathbf{j}`
$$

$$
`\overrightarrow{PR} = \mathbf{r} - \mathbf{p} = (-2\mathbf{i} + 4\mathbf{j}) - (3\mathbf{i} + \mathbf{j}) = -5\mathbf{i} + 3\mathbf{j}`
$$

（b）设 $`S`$ 的位置向量为 $`\mathbf{s}`$。由 $`\overrightarrow{PS} = \mathbf{s} - \mathbf{p}`$ 且 $`\overrightarrow{PS} = 2\overrightarrow{PQ}`$，得：

$$
`\mathbf{s} - \mathbf{p} = 2(2\mathbf{i} - 3\mathbf{j}) = 4\mathbf{i} - 6\mathbf{j}`
$$

所以：

$$
`\mathbf{s} = \mathbf{p} + (4\mathbf{i} - 6\mathbf{j}) = (3\mathbf{i} + \mathbf{j}) + (4\mathbf{i} - 6\mathbf{j}) = 7\mathbf{i} - 5\mathbf{j}`
$$

因此 $`S`$ 的坐标为 $`(7, -5)`$。

（c）计算点积：

$$
`\overrightarrow{PQ} \cdot \overrightarrow{PR} = (2)(-5) + (-3)(3) = -10 - 9 = -19 \neq 0`
$$

因为点积不为零，所以 $`\overrightarrow{PQ}`$ 与 $`\overrightarrow{PR}`$ **不垂直**。

> **如果用斜率法验证**：
> $`k_{PQ} = \dfrac{-3}{2} = -1.5`$
> $`k_{PR} = \dfrac{3}{-5} = -0.6`$
> $`k_{PQ} \cdot k_{PR} = (-1.5)(-0.6) = 0.9 \neq -1`$
> 同样得出不垂直。✓

---

## 2.2 向量的实际运用

### 2.2.1 向量几何——深度解析

向量是解决平面几何问题的强大工具。通过将几何关系转化为向量方程，我们可以用代数方法精确求解，避免画图的不精确性。

#### 核心思想

**向量几何的本质**：用向量运算（加减、数乘）来表示几何关系。

| 几何关系 | 向量表达 |
|:---|:---|
| 从 $`A`$ 到 $`B`$ 的线段 | $`\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A`$ |
| $`A`$ 和 $`B`$ 的中点 $`M`$ | $`\mathbf{r}_M = \dfrac{\mathbf{r}_A + \mathbf{r}_B}{2}`$ |
| $`P`$ 分 $`AB`$ 为 $`m:n`$ | $`\mathbf{r}_P = \dfrac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n}`$ |
| $`AB \parallel CD`$ | $`\overrightarrow{AB} = k \cdot \overrightarrow{CD}`$ |
| $`AB \perp CD`$ | $`\overrightarrow{AB} \cdot \overrightarrow{CD} = 0`$ |
| $`A,B,C`$ 共线 | $`\overrightarrow{AB} = k \cdot \overrightarrow{BC}`$（存在 $`k`$） |

#### 中点公式——为什么是这样？

设 $`M`$ 是 $`AB`$ 的中点。从 $`A`$ 到 $`M`$ 的位移是 $`\overrightarrow{AB}`$ 的一半：

$$
`\mathbf{r}_M = \mathbf{r}_A + \frac{1}{2}\overrightarrow{AB} = \mathbf{r}_A + \frac{1}{2}(\mathbf{r}_B - \mathbf{r}_A) = \frac{2\mathbf{r}_A + \mathbf{r}_B - \mathbf{r}_A}{2} = \frac{\mathbf{r}_A + \mathbf{r}_B}{2}`
$$

#### 分点公式——详细推导

设点 $`P`$ 分线段 $`AB`$ 为 $`AP:PB = m:n`$（即 $`P`$ 靠近 $`A`$ 的方向上，$`AP`$ 占 $`m`$ 份，$`PB`$ 占 $`n`$ 份）。

这意味着 $`P`$ 位于从 $`A`$ 到 $`B`$ 的 $`\dfrac{m}{m+n}`$ 处（从 $`A`$ 算起）。所以：

$$
`\begin{aligned}
\mathbf{r}_P &= \mathbf{r}_A + \frac{m}{m+n}\overrightarrow{AB} \\
&= \mathbf{r}_A + \frac{m}{m+n}(\mathbf{r}_B - \mathbf{r}_A) \\
&= \frac{(m+n)\mathbf{r}_A + m\mathbf{r}_B - m\mathbf{r}_A}{m+n} \\
&= \frac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n}
\end{aligned}`
$$

> **记忆技巧**：分点公式中，$`A`$ 的系数是 $`n`$（对面那段的比例），$`B`$ 的系数是 $`m`$（对面那段的比例）。交叉相乘！
>
> 例如 $`AP:PB = 2:3`$（$`m=2, n=3`$），则：
> $$`\mathbf{r}_P = \frac{3\mathbf{r}_A + 2\mathbf{r}_B}{5}`$$
> $`A`$ 的系数是 3（对面的 $`PB`$ 是 3 份），$`B`$ 的系数是 2（对面的 $`AP`$ 是 2 份）。

#### 平行向量

两个非零向量 $`\mathbf{a}`$ 和 $`\mathbf{b}`$ 平行（即方向相同或相反）当且仅当存在一个实数 $`k`$ 使得：

$$
`\mathbf{a} = k\mathbf{b}`
$$

即一个向量是另一个向量的标量倍。

> **如何判断平行？** 检查两个向量的对应分量是否成比例：
> 若 $`\mathbf{a} = (a_x, a_y)`$，$`\mathbf{b} = (b_x, b_y)`$，且 $`\frac{a_x}{b_x} = \frac{a_y}{b_y}`$（分母不为零），则它们平行。
> 注意这个比例可以是负数（方向相反）。

#### 三点共线的判定

三点 $`A`$、$`B`$、$`C`$ 共线当且仅当 $`\overrightarrow{AB}`$ 与 $`\overrightarrow{AC}`$ 平行（或 $`\overrightarrow{AB}`$ 与 $`\overrightarrow{BC}`$ 平行）。

**为什么？** 如果三点共线，那么从 $`A`$ 到 $`B`$ 和从 $`A`$ 到 $`C`$ 的位移方向相同或相反，即存在标量 $`k`$ 使 $`\overrightarrow{AC} = k \cdot \overrightarrow{AB}`$。

---

### 📌 例题 2.2：向量几何应用

**例题 1**（平行四边形与中点——配图说明）

在平行四边形 $`ABCD`$ 中，$`A`$、$`B`$、$`C`$ 的位置向量分别为 $`\mathbf{a} = \mathbf{i} + 2\mathbf{j}`$，$`\mathbf{b} = 4\mathbf{i} + 3\mathbf{j}`$，$`\mathbf{c} = 6\mathbf{i} + \mathbf{j}`$。求：

（a）$`D`$ 的位置向量
（b）对角线 $`AC`$ 与 $`BD`$ 的交点 $`M`$ 的位置向量

**思路分析**：

> 先理解平行四边形的结构。顶点按 $`A \to B \to C \to D \to A`$ 的顺序排列。
>
> **平行四边形的关键性质**：对边平行且相等。
> - $`AB \parallel DC`$ 且 $`AB = DC`$
> - $`AD \parallel BC`$ 且 $`AD = BC`$
>
> 这意味着 $`\overrightarrow{AD} = \overrightarrow{BC}`$ 或 $`\overrightarrow{AB} = \overrightarrow{DC}`$。
>
> 另外，平行四边形的对角线**互相平分**，即 $`AC`$ 的中点 = $`BD`$ 的中点。

**解**：

（a）在平行四边形 $`ABCD`$ 中，对边 $`AD`$ 和 $`BC`$ 平行且相等，所以 $`\overrightarrow{AD} = \overrightarrow{BC}`$。

先求 $`\overrightarrow{BC} = \mathbf{c} - \mathbf{b}`$：

$$
`\overrightarrow{BC} = (6\mathbf{i} + \mathbf{j}) - (4\mathbf{i} + 3\mathbf{j}) = 2\mathbf{i} - 2\mathbf{j}`
$$

因为 $`\overrightarrow{AD} = \overrightarrow{BC} = 2\mathbf{i} - 2\mathbf{j}`$，而 $`\overrightarrow{AD} = \mathbf{d} - \mathbf{a}`$，所以：

$$
`\mathbf{d} = \mathbf{a} + \overrightarrow{AD} = (\mathbf{i} + 2\mathbf{j}) + (2\mathbf{i} - 2\mathbf{j}) = 3\mathbf{i}`
$$

所以 $`D`$ 的坐标为 $`(3, 0)`$。

**验证**：也可用 $`\overrightarrow{AB} = \overrightarrow{DC}`$ 来求。
$`\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (4\mathbf{i} + 3\mathbf{j}) - (\mathbf{i} + 2\mathbf{j}) = 3\mathbf{i} + \mathbf{j}`$
$`\overrightarrow{DC} = \mathbf{c} - \mathbf{d}`$，所以 $`\mathbf{c} - \mathbf{d} = 3\mathbf{i} + \mathbf{j}`$，解得 $`\mathbf{d} = \mathbf{c} - (3\mathbf{i} + \mathbf{j}) = (6\mathbf{i} + \mathbf{j}) - (3\mathbf{i} + \mathbf{j}) = 3\mathbf{i}`$，一致。✓

（b）平行四边形的对角线互相平分。因此 $`M`$ 既是 $`AC`$ 的中点，也是 $`BD`$ 的中点。

用 $`AC`$ 的中点计算：

$$
`\mathbf{m} = \frac{\mathbf{a} + \mathbf{c}}{2} = \frac{(\mathbf{i} + 2\mathbf{j}) + (6\mathbf{i} + \mathbf{j})}{2} = \frac{7\mathbf{i} + 3\mathbf{j}}{2} = 3.5\mathbf{i} + 1.5\mathbf{j}`
$$

验证用 $`BD`$ 的中点：$`\frac{\mathbf{b} + \mathbf{d}}{2} = \frac{(4\mathbf{i} + 3\mathbf{j}) + 3\mathbf{i}}{2} = \frac{7\mathbf{i} + 3\mathbf{j}}{2}`$，一致。✓

---

**例题 2**（共线判定与比值——如何证明三点共线）

三点 $`A`$、$`B`$、$`C`$ 的位置向量分别为 $`\mathbf{a} = 2\mathbf{i} + \mathbf{j}`$，$`\mathbf{b} = 5\mathbf{i} + 4\mathbf{j}`$，$`\mathbf{c} = 8\mathbf{i} + 7\mathbf{j}`$。

（a）证明 $`A`$、$`B`$、$`C`$ 三点共线。
（b）求 $`AB:BC`$ 的比值。

**思路分析**：

> 证明三点共线的标准方法：
> 1. 计算 $`\overrightarrow{AB}`$ 和 $`\overrightarrow{BC}`$（或 $`\overrightarrow{AB}`$ 和 $`\overrightarrow{AC}`$）
> 2. 判断它们是否平行（即是否存在标量 $`k`$ 使得一个等于另一个乘以 $`k`$）
> 3. 如果平行且有一个公共点（$`B`$ 是 $`\overrightarrow{AB}`$ 和 $`\overrightarrow{BC}`$ 的公共点），则三点共线

**解**：

（a）计算向量：

$$
`\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (5\mathbf{i} + 4\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = 3\mathbf{i} + 3\mathbf{j}`
$$

$$
`\overrightarrow{BC} = \mathbf{c} - \mathbf{b} = (8\mathbf{i} + 7\mathbf{j}) - (5\mathbf{i} + 4\mathbf{j}) = 3\mathbf{i} + 3\mathbf{j}`
$$

观察发现 $`\overrightarrow{BC} = \overrightarrow{AB}`$，即 $`\overrightarrow{BC} = 1 \cdot \overrightarrow{AB}`$。存在标量 $`k = 1`$ 使得 $`\overrightarrow{BC} = k\overrightarrow{AB}`$，所以 $`\overrightarrow{AB} \parallel \overrightarrow{BC}`$。又因为这两个向量都通过点 $`B`$，故 $`A`$、$`B`$、$`C`$ 共线。

> **注意**：也可以验证 $`\overrightarrow{AC}`$ 与 $`\overrightarrow{AB}`$ 的关系。
> $`\overrightarrow{AC} = \mathbf{c} - \mathbf{a} = (8\mathbf{i} + 7\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = 6\mathbf{i} + 6\mathbf{j} = 2(3\mathbf{i} + 3\mathbf{j}) = 2\overrightarrow{AB}`$
> 同样得出共线结论。

（b）因为 $`\overrightarrow{BC} = \overrightarrow{AB}`$，且方向相同，所以 $`\overrightarrow{AB}`$ 和 $`\overrightarrow{BC}`$ 的长度相等。即 $`AB = BC`$，因此 $`AB:BC = 1:1`$。

换句话说，$`B`$ 是线段 $`AC`$ 的中点。

---

**例题 3**（分点公式 + 垂直验证——综合应用）

在 $`\triangle OAB`$ 中，$`C`$ 在 $`OA`$ 上且 $`OC:CA = 2:1`$，$`D`$ 在 $`AB`$ 上且 $`AD:DB = 3:1`$。设 $`\overrightarrow{OA} = \mathbf{a}`$，$`\overrightarrow{OB} = \mathbf{b}`$。

（a）用 $`\mathbf{a}`$ 和 $`\mathbf{b}`$ 表示 $`\overrightarrow{OD}`$。
（b）用 $`\mathbf{a}`$ 和 $`\mathbf{b}`$ 表示 $`\overrightarrow{CD}`$。
（c）已知 $`\mathbf{a} = 3\mathbf{i} + 2\mathbf{j}`$，$`\mathbf{b} = \mathbf{i} + 6\mathbf{j}`$，判断 $`\overrightarrow{OC}`$ 与 $`\overrightarrow{OD}`$ 是否垂直。

**思路分析**：

> 这是一个"用基底表示向量"的典型问题。$`\mathbf{a}`$ 和 $`\mathbf{b}`$ 是基底，所有其他向量都要用它们表示。
>
> 关键步骤：
> 1. 确定分点 $`C`$ 在 $`OA`$ 上的位置：$`OC:CA = 2:1`$ 意味着 $`OC = \frac{2}{3}OA`$
> 2. 确定分点 $`D`$ 在 $`AB`$ 上的位置：$`AD:DB = 3:1`$ 意味着 $`AD = \frac{3}{4}AB`$
> 3. 用分点公式或直接加减法表示向量
> 4. 垂直判定：代入具体数值后计算点积

**解**：

（a）先表示 $`D`$ 的位置。

方法一（分点公式）：$`D`$ 分 $`AB`$ 为 $`AD:DB = 3:1`$，即从 $`A`$ 到 $`B`$ 的方向上，$`D`$ 位于 $`\frac{3}{4}`$ 处。

由分点公式（$`m=3, n=1`$）：

$$
`\mathbf{r}_D = \frac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n} = \frac{1 \cdot \mathbf{a} + 3 \cdot \mathbf{b}}{3+1} = \frac{\mathbf{a} + 3\mathbf{b}}{4}`
$$

方法二（直接法）：从 $`A`$ 出发走到 $`B`$ 的 $`\frac{3}{4}`$ 处。

$$
`\overrightarrow{OD} = \overrightarrow{OA} + \frac{3}{4}\overrightarrow{AB}`
$$

而 $`\overrightarrow{AB} = \overrightarrow{OB} - \overrightarrow{OA} = \mathbf{b} - \mathbf{a}`$，所以：

$$
`\overrightarrow{OD} = \mathbf{a} + \frac{3}{4}(\mathbf{b} - \mathbf{a}) = \mathbf{a} + \frac{3}{4}\mathbf{b} - \frac{3}{4}\mathbf{a} = \frac{1}{4}\mathbf{a} + \frac{3}{4}\mathbf{b}`
$$

注意 $`\frac{\mathbf{a} + 3\mathbf{b}}{4} = \frac{1}{4}\mathbf{a} + \frac{3}{4}\mathbf{b}`$，两种方法结果一致。✓

（b）$`C`$ 在 $`OA`$ 上且 $`OC:CA = 2:1`$，所以 $`C`$ 分 $`\overrightarrow{OA}`$ 为 $`2:1`$（从 $`O`$ 算起）。因此：

$$
`\overrightarrow{OC} = \frac{2}{3}\overrightarrow{OA} = \frac{2}{3}\mathbf{a}`
$$

于是：

$$
`\overrightarrow{CD} = \overrightarrow{OD} - \overrightarrow{OC} = \left(\frac{1}{4}\mathbf{a} + \frac{3}{4}\mathbf{b}\right) - \frac{2}{3}\mathbf{a}`
$$

通分计算 $`\mathbf{a}`$ 的系数：$`\frac{1}{4} - \frac{2}{3} = \frac{3}{12} - \frac{8}{12} = -\frac{5}{12}`$。

所以：

$$
`\overrightarrow{CD} = -\frac{5}{12}\mathbf{a} + \frac{3}{4}\mathbf{b}`
$$

（c）代入 $`\mathbf{a} = 3\mathbf{i} + 2\mathbf{j}`$，$`\mathbf{b} = \mathbf{i} + 6\mathbf{j}`$：

先求 $`\overrightarrow{OC}`$：

$$
`\overrightarrow{OC} = \frac{2}{3}(3\mathbf{i} + 2\mathbf{j}) = 2\mathbf{i} + \frac{4}{3}\mathbf{j}`
$$

再求 $`\overrightarrow{OD}`$：

$$
`\begin{aligned}
\overrightarrow{OD} &= \frac{1}{4}(3\mathbf{i} + 2\mathbf{j}) + \frac{3}{4}(\mathbf{i} + 6\mathbf{j}) \\
&= \left(\frac{3}{4} + \frac{3}{4}\right)\mathbf{i} + \left(\frac{1}{2} + \frac{9}{2}\right)\mathbf{j} \\
&= \frac{6}{4}\mathbf{i} + \frac{10}{2}\mathbf{j} \\
&= \frac{3}{2}\mathbf{i} + 5\mathbf{j}
\end{aligned}`
$$

计算点积：

$$
`\overrightarrow{OC} \cdot \overrightarrow{OD} = (2)\left(\frac{3}{2}\right) + \left(\frac{4}{3}\right)(5) = 3 + \frac{20}{3} = \frac{9}{3} + \frac{20}{3} = \frac{29}{3} \neq 0`
$$

点积不为零，所以 $`\overrightarrow{OC}`$ 与 $`\overrightarrow{OD}`$ **不垂直**。

---

### 2.2.2 速度的合成与分解

速度是一个向量。当一个物体同时参与两个或更多运动时，它的合速度是这些速度的向量和。

#### 相对速度公式

设物体 $`A`$ 相对于参考系 $`C`$ 的速度为 $`\mathbf{v}_{A/C}`$，物体 $`A`$ 相对于物体 $`B`$ 的速度为 $`\mathbf{v}_{A/B}`$，物体 $`B`$ 相对于参考系 $`C`$ 的速度为 $`\mathbf{v}_{B/C}`$，则：

$$
`\mathbf{v}_{A/C} = \mathbf{v}_{A/B} + \mathbf{v}_{B/C}`
$$

> **直观理解**：
> - 你在火车上行走，速度为 $`\mathbf{v}_{A/B}`$（你相对于火车）
> - 火车相对于地面行驶，速度为 $`\mathbf{v}_{B/C}`$（火车相对于地面）
> - 你相对于地面的速度 $`\mathbf{v}_{A/C}`$ 就是两者之和
>
> **另一个例子**：一艘船在河中行驶。
> - 船在静水中的速度 = $`\mathbf{v}_{B/W}`$（船相对于水）
> - 水流速度 = $`\mathbf{v}_{W/G}`$（水相对于地面）
> - 船相对于地面的实际速度 = $`\mathbf{v}_{B/W} + \mathbf{v}_{W/G}`$

#### 速度的分解

与合成相反，将一个速度向量分解为两个互相垂直的分量（通常沿水平方向和垂直方向）称为**速度的分解**。

设速度 $`\mathbf{v}`$ 的大小为 $`v`$（速率），与水平方向的夹角为 $`\theta`$，则：

$$
`\mathbf{v} = (v\cos\theta)\,\mathbf{i} + (v\sin\theta)\,\mathbf{j}`
$$

其中 $`v_x = v\cos\theta`$ 是水平分量，$`v_y = v\sin\theta`$ 是垂直分量。

> **推导**：将速度向量投影到 $`x`$ 轴和 $`y`$ 轴上。在直角三角形中，邻边 $=$ 斜边 $`\times \cos\theta`$，对边 $=$ 斜边 $`\times \sin\theta`$。

---

#### 相撞问题

两个运动物体相撞的条件是：在**同一时刻**，它们的位置向量**相等**。即：

$$
`\mathbf{r}_1(t) = \mathbf{r}_2(t)`
$$

对于匀速直线运动，位置向量满足：

$$
`\mathbf{r}(t) = \mathbf{r}_0 + \mathbf{v}t`
$$

其中 $`\mathbf{r}_0`$ 是初始位置向量，$`\mathbf{v}`$ 是速度向量。因此相撞条件可以展开为：

$$
`\mathbf{r}_{01} + \mathbf{v}_1 t = \mathbf{r}_{02} + \mathbf{v}_2 t`
$$

这是一个关于时间 $`t`$ 的向量方程。它等价于两个分量方程分别相等，从而可以解出 $`t`$ 并验证是否一致。

**解题步骤**：
1. 写出两物体的位置向量 $`\mathbf{r}_1(t)`$ 和 $`\mathbf{r}_2(t)`$。
2. 令 $`\mathbf{r}_1(t) = \mathbf{r}_2(t)`$，得到两个分量方程。
3. 分别解出 $`t`$。如果两个 $`t`$ 值相等且 $`\geq 0`$，则相撞；否则不相撞。

> **注意**："相撞"要求同时在同一位置。如果两船在不同时间到达同一点，那只叫"相遇"而非"相撞"。

---

### 📌 例题 2.3：速度合成与相撞问题

**例题 1**（速度合成——船与水流）

一艘船在静水中的速度是 $`6\ \text{m/s}`$ 向东。水流以 $`4\ \text{m/s}`$ 的速度向北流动。求船相对于地面的速度的大小和方向。

**思路分析**：
- 船相对于水的速度 $`\mathbf{v}_{B/W}`$ = 向东 6 m/s
- 水相对于地面的速度 $`\mathbf{v}_{W/G}`$ = 向北 4 m/s
- 船相对于地面的速度 $`\mathbf{v}_{B/G} = \mathbf{v}_{B/W} + \mathbf{v}_{W/G}`$

**解**：

设正东方向为 $`+x`$ 轴，正北方向为 $`+y`$ 轴。

船相对于水的速度：$`\mathbf{v}_{B/W} = 6\mathbf{i}`$
水流相对于地面的速度：$`\mathbf{v}_{W/G} = 4\mathbf{j}`$

由速度合成公式：

$$
`\mathbf{v}_{B/G} = \mathbf{v}_{B/W} + \mathbf{v}_{W/G} = 6\mathbf{i} + 4\mathbf{j}`
$$

合速度的大小（速率）：

$$
`|\mathbf{v}_{B/G}| = \sqrt{6^2 + 4^2} = \sqrt{36 + 16} = \sqrt{52} = 2\sqrt{13} \approx 7.21\ \text{m/s}`
$$

合速度的方向：设 $`\theta`$ 为与正东方向的夹角（逆时针为正）。

$$
`\tan\theta = \frac{4}{6} = \frac{2}{3} \;\Longrightarrow\; \theta = \arctan\!\left(\frac{2}{3}\right) \approx 33.69^\circ`
$$

因此船相对于地面的速度大小为 $`2\sqrt{13}\ \text{m/s}`$，方向为北偏东 $`33.69^\circ`$（即从正东方向逆时针旋转 $`33.69^\circ`$）。

> **生活实例**：这就是为什么船过河时，如果直接朝对岸开，会被水流冲偏。要想直接到达正对岸，船头必须朝上游方向倾斜。

---

**例题 2**（速度分解——斜抛的初速度）

一个球以初速度 $`20\ \text{m/s}`$、与水平方向成 $`30^\circ`$ 角斜向上抛出。

（a）求初速度的水平分量和垂直分量。
（b）写出初速度的向量形式。

**思路分析**：
- 速度的大小是 20，方向是 $`30^\circ`$ 仰角
- 水平分量 $`v_x = v\cos\theta`$，垂直分量 $`v_y = v\sin\theta`$

**解**：

（a）设水平向右为 $`+x`$ 轴，竖直向上为 $`+y`$ 轴。

水平分量：

$$
`v_x = v\cos\theta = 20 \times \cos 30^\circ = 20 \times \frac{\sqrt{3}}{2} = 10\sqrt{3} \approx 17.32\ \text{m/s}`
$$

垂直分量：

$$
`v_y = v\sin\theta = 20 \times \sin 30^\circ = 20 \times \frac{1}{2} = 10\ \text{m/s}`
$$

（b）初速度的向量形式：

$$
`\mathbf{v}_0 = 10\sqrt{3}\ \mathbf{i} + 10\ \mathbf{j}\ \text{m/s}`
$$

> **物理意义**：
> - 如果没有空气阻力，水平分量 $`v_x`$ 在整个运动过程中保持不变（因为水平方向不受力）
> - 而垂直分量 $`v_y`$ 受重力影响以 $`-g`$ 的加速度变化（$`g \approx 9.8\ \text{m/s}^2`$）
> - 所以任意时刻的速度为 $`\mathbf{v}(t) = 10\sqrt{3}\ \mathbf{i} + (10 - gt)\ \mathbf{j}`$
> - 这为第 10 章的运动学问题奠定了基础

---

**例题 3**（相撞问题——两船是否会相撞）

船 $`P`$ 从点 $`(0, 0)`$ 出发，以速度 $`\mathbf{v}_P = (3\mathbf{i} + 4\mathbf{j})\ \text{km/h}`$ 航行。船 $`Q`$ 从点 $`(10, 5)\ \text{km}`$ 出发，以速度 $`\mathbf{v}_Q = (-2\mathbf{i} + \mathbf{j})\ \text{km/h}`$ 航行。两船同时出发，判断它们是否会相撞。

**思路分析**：
1. 写出两船的位置向量（都是 $`\mathbf{r}_0 + \mathbf{v}t`$ 的形式）
2. 令 $`\mathbf{r}_P(t) = \mathbf{r}_Q(t)`$
3. 得到两个分量方程，分别解 $`t`$
4. 如果 $`t`$ 值一致且 $`\geq 0`$，相撞；否则不相撞

**解**：

设 $`t`$ 为出发后的时间（小时）。

$`P`$ 的位置向量（从原点出发）：

$$
`\mathbf{r}_P(t) = (0, 0)^\mathrm{T} + (3, 4)^\mathrm{T}\,t = (3t,\; 4t)^\mathrm{T}`
$$

$`Q`$ 的位置向量（从 $`(10,5)`$ 出发）：

$$
`\mathbf{r}_Q(t) = (10, 5)^\mathrm{T} + (-2, 1)^\mathrm{T}\,t = (10 - 2t,\; 5 + t)^\mathrm{T}`
$$

如果两船相撞，则存在某个 $`t \geq 0`$ 使得 $`\mathbf{r}_P(t) = \mathbf{r}_Q(t)`$，即：

$$
`(3t,\; 4t)^\mathrm{T} = (10 - 2t,\; 5 + t)^\mathrm{T}`
$$

这给出两个分量方程：

$$
`\begin{cases}
x\text{分量：} & 3t = 10 - 2t \;\Longrightarrow\; 5t = 10 \;\Longrightarrow\; t = 2 \\[4pt]
y\text{分量：} & 4t = 5 + t \;\Longrightarrow\; 3t = 5 \;\Longrightarrow\; t = \dfrac{5}{3}
\end{cases}`
$$

两个 $`t`$ 值不相等（$`2 \neq \frac{5}{3}`$），因此不存在同时满足两个分量方程的时刻。两船不会相撞。

> **为什么不相撞？** 即使 $`x`$ 坐标在 $`t=2`$ 时相等，$`y`$ 坐标在 $`t=2`$ 时分别为 $`4\times 2 = 8`$ 和 $`5+2=7`$，不相等。所以两船永远不会在同一时刻到达同一点。

---

## 2.3 变化率入门（微积分铺垫）

### 2.3.1 为何研究变化率？

在物理世界中，很少有事物是静止的。一辆行驶的汽车，它的位置在变化；一个充气的气球，它的体积在变化；一个加热的金属棒，它的温度在变化。**变化率**就是描述"一个量随另一个量变化得有多快"的数学工具。

在 2.1 和 2.2 节中，我们用向量描述了位置、速度和加速度。现在我们要问一个更深入的问题：**如何精确地定义"瞬时"变化率？**

---

### 2.3.2 从平均变化率到瞬时变化率

让我们从一个具体的运动学例子开始。

一个质点沿直线运动，它的位移 $`s`$（单位：米）与时间 $`t`$（单位：秒）的关系为：

$$
`s(t) = t^2`
$$

我们想知道 $`t = 1`$ 秒这一**瞬间**的速度。

#### 第一步：平均速度

如果取一个时间区间 $`[1, 1 + \Delta t]`$，质点在区间内的平均速度是：

$$
`\text{平均速度} = \frac{s(1 + \Delta t) - s(1)}{\Delta t}`
$$

代入 $`s(t) = t^2`$：

$$
`\frac{(1 + \Delta t)^2 - 1^2}{\Delta t} = \frac{1 + 2\Delta t + (\Delta t)^2 - 1}{\Delta t} = \frac{2\Delta t + (\Delta t)^2}{\Delta t} = 2 + \Delta t`
$$

#### 第二步：让 $`\Delta t`$ 越来越小

我们让 $`\Delta t`$ 逐渐趋近于 0，观察平均速度的变化：

| $`\Delta t`$（秒） | 平均速度（m/s） |
|:---:|:---:|
| 0.1 | $`2 + 0.1 = 2.1`$ |
| 0.01 | $`2 + 0.01 = 2.01`$ |
| 0.001 | $`2 + 0.001 = 2.001`$ |
| 0.0001 | $`2 + 0.0001 = 2.0001`$ |
| $`\to 0`$ | $`\to 2`$ |

随着 $`\Delta t`$ 越来越接近 0，平均速度越来越接近 **2**。

#### 第三步：极限

当 $`\Delta t`$ 趋近于 0 时，平均速度 $`2 + \Delta t`$ 趋近于 2。我们记：

$$
`v(1) = \lim_{\Delta t \to 0} \frac{s(1 + \Delta t) - s(1)}{\Delta t} = \lim_{\Delta t \to 0} (2 + \Delta t) = 2`
$$

这个极限值就是质点在 $`t = 1`$ 时的**瞬时速度**。

> **重要理解**：我们从不令 $`\Delta t = 0`$（那样会得到 $`0/0`$，没有意义）。我们让 $`\Delta t`$ 无限趋近于 0，观察比值趋近于哪个固定值。这个"趋近的目标"就是导数。
>
> 用极限的语言说：**当 $`\Delta t`$ 趋近于 0 时，平均速度的极限就是瞬时速度。**

---

### 2.3.3 导数的一般定义

一般地，对于函数 $`y = f(x)`$，它在 $`x = a`$ 处的**导数**（即瞬时变化率）定义为：

$$
`f'(a) = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h}`
$$

其中 $`h`$ 就是前面例子中的 $`\Delta x`$ 或 $`\Delta t`$。

如果这个极限存在，我们就说 $`f`$ 在 $`x = a`$ 处**可导**。

**导数的记号**：
- 莱布尼茨记号：$`\dfrac{dy}{dx}`$ 或 $`\dfrac{d}{dx}f(x)`$
- 拉格朗日记号：$`f'(x)`$
- 牛顿记号（常用于物理）：$`\dot{y}`$

> 在考纲 14.1 中，只要求对极限有直观理解，不要求从第一原理求导。但我们这里仍会展示几个基本推导，帮助你建立直觉。

---

### 2.3.4 用定义求导——基础推导

让我们用极限定义推导几个基本函数的导数。

#### 推导 1：$`f(x) = x^2`$

$$
`\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{(x + h)^2 - x^2}{h} \\
&= \lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h} \\
&= \lim_{h \to 0} \frac{2xh + h^2}{h} \\
&= \lim_{h \to 0} (2x + h) \\
&= 2x
\end{aligned}`
$$

因此 $`\dfrac{d}{dx}(x^2) = 2x`$。

**几何意义**：函数 $`y = x^2`$ 在任意点 $`x`$ 处的切线斜率为 $`2x`$。在 $`x = 1`$ 处斜率为 2，在 $`x = 3`$ 处斜率为 6。

#### 推导 2：$`f(x) = x^3`$

$$
`\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{(x + h)^3 - x^3}{h}
\end{aligned}`
$$

展开 $`(x + h)^3 = x^3 + 3x^2h + 3xh^2 + h^3`$：

$$
`\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{x^3 + 3x^2h + 3xh^2 + h^3 - x^3}{h} \\
&= \lim_{h \to 0} \frac{3x^2h + 3xh^2 + h^3}{h} \\
&= \lim_{h \to 0} (3x^2 + 3xh + h^2) \\
&= 3x^2
\end{aligned}`
$$

因此 $`\dfrac{d}{dx}(x^3) = 3x^2`$。

#### 推导 3：$`f(x) = \dfrac{1}{x}`$（$`x \neq 0`$）

$$
`\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{\frac{1}{x + h} - \frac{1}{x}}{h}
\end{aligned}`
$$

先通分分子：

$$
`\frac{1}{x + h} - \frac{1}{x} = \frac{x - (x + h)}{x(x + h)} = \frac{-h}{x(x + h)}`
$$

所以：

$$
`\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{-h}{x(x + h)} \cdot \frac{1}{h} \\
&= \lim_{h \to 0} \frac{-1}{x(x + h)} \\
&= -\frac{1}{x^2}
\end{aligned}`
$$

因此 $`\dfrac{d}{dx}\!\left(\dfrac{1}{x}\right) = -\dfrac{1}{x^2}`$。

---


继续！以下接续第 2 章 2.3.5 节之后的内容：

---

### 2.3.5 幂法则

从上面的推导中，我们可以观察出一个模式：

| $`f(x)`$ | $`f'(x)`$ |
|:---:|:---:|
| $`x^2`$ | $`2x`$ |
| $`x^3`$ | $`3x^2`$ |
| $`x^1`$ | $`1`$（即 $`1 \cdot x^0`$） |
| $`1/x = x^{-1}`$ | $`-1/x^2 = -x^{-2}`$ |

这个模式就是**幂法则**：对任意实数 $`n`$，

$$
\boxed{`\dfrac{d}{dx}(x^n) = n x^{n-1}`}
$$

> **幂法则的完整推导**（利用二项式定理展开，仅对正整数 $`n`$）：
>
> 考虑 $`f(x) = x^n`$，其中 $`n`$ 为正整数。展开 $`(x + h)^n`$：
> $$
`(x + h)^n = x^n + n x^{n-1}h + \dfrac{n(n-1)}{2}x^{n-2}h^2 + \dfrac{n(n-1)(n-2)}{6}x^{n-3}h^3 + \dots + h^n`$$
> 因此：
> $$
`\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{x^n + n x^{n-1}h + \frac{n(n-1)}{2}x^{n-2}h^2 + \dots + h^n - x^n}{h} \\
&= \lim_{h \to 0} \left( n x^{n-1} + \frac{n(n-1)}{2}x^{n-2}h + \dots + h^{n-1} \right) \\
&= n x^{n-1}
\end{aligned}`$$
> 因为所有含 $`h`$ 的项在 $`h \to 0`$ 时都趋于 0。

---

### 2.3.6 变化率在向量中的应用：运动学

现在回到向量的语境中。如果质点的位置向量 $`\mathbf{r}(t)`$ 随时间变化，那么它的速度向量和加速度向量就是位置向量对时间的变化率。

设 $`\mathbf{r}(t) = x(t)\mathbf{i} + y(t)\mathbf{j}`$，则：

$$
`\mathbf{v}(t) = \frac{d\mathbf{r}}{dt} = \frac{dx}{dt}\mathbf{i} + \frac{dy}{dt}\mathbf{j}`
$$

$$
`\mathbf{a}(t) = \frac{d\mathbf{v}}{dt} = \frac{d^2\mathbf{r}}{dt^2} = \frac{d^2x}{dt^2}\mathbf{i} + \frac{d^2y}{dt^2}\mathbf{j}`
$$

也就是说，对向量函数求导，就是对它的各个分量分别求导。

---

### 2.3.7 从加速度到速度和位置（积分铺垫）

在物理中，加速度 $`\mathbf{a}(t)`$ 是速度 $`\mathbf{v}(t)`$ 的变化率。如果我们知道加速度并想恢复出速度，需要做微分的逆运算——这称为**积分**（将在第 7 章详细学习）。

基本关系是：

- 速度 $`\mathbf{v}(t) = \int \mathbf{a}(t) \, dt + \mathbf{v}_0`$（其中 $`\mathbf{v}_0`$ 是初始速度）
- 位置 $`\mathbf{r}(t) = \int \mathbf{v}(t) \, dt + \mathbf{r}_0`$（其中 $`\mathbf{r}_0`$ 是初始位置）

或者用定积分的形式（更适合已知确定时间段的问题）：

$$
`\mathbf{v}(t) = \mathbf{v}_0 + \int_0^t \mathbf{a}(u) \, du,\quad \mathbf{r}(t) = \mathbf{r}_0 + \int_0^t \mathbf{v}(u) \, du`
$$

这里先建立直观理解：**微分**是求变化率（位置 → 速度 → 加速度），**积分**是求累积量（加速度 → 速度 → 位置），两者互为逆运算。

---

### 📌 例题 2.4：变化率入门

**例题 1**（用极限定义求瞬时速度）

一个质点的位移（单位：米）与时间（单位：秒）的关系为 $`s(t) = 3t^2 - 2t + 1`$。

（a）求从 $`t = 2`$ 到 $`t = 2 + h`$ 的平均速度。
（b）利用极限求 $`t = 2`$ 时的瞬时速度。

**思路分析**：
- 平均速度 = $`\dfrac{s(2+h) - s(2)}{h}`$
- 瞬时速度 = $`\displaystyle\lim_{h \to 0}`$ 平均速度

**解**：

（a）

$$
`\begin{aligned}
\text{平均速度} &= \frac{s(2 + h) - s(2)}{h} \\
&= \frac{[3(2+h)^2 - 2(2+h) + 1] - [3(4) - 4 + 1]}{h} \\
&= \frac{[3(4 + 4h + h^2) - 4 - 2h + 1] - [12 - 4 + 1]}{h} \\
&= \frac{[12 + 12h + 3h^2 - 4 - 2h + 1] - 9}{h} \\
&= \frac{[9 + 10h + 3h^2] - 9}{h} \\
&= \frac{10h + 3h^2}{h} = 10 + 3h
\end{aligned}`
$$

（b）瞬时速度是 $`h \to 0`$ 时平均速度的极限：

$$
`v(2) = \lim_{h \to 0} (10 + 3h) = 10\ \text{m/s}`
$$

因此质点在 $`t = 2`$ 秒时的瞬时速度为 $`10\ \text{m/s}`$。

> **验证**：用幂法则直接求导：$`s'(t) = 6t - 2`$，$`s'(2) = 12 - 2 = 10`$，一致。✓

---

**例题 2**（用极限定义求一般导数 + 幂法则验证）

用导数的极限定义求 $`f(x) = 4x - x^2`$ 的导数 $`f'(x)`$。

**解**：

$$
`\begin{aligned}
f'(x) &= \lim_{h \to 0} \frac{f(x + h) - f(x)}{h} \\
&= \lim_{h \to 0} \frac{[4(x + h) - (x + h)^2] - [4x - x^2]}{h} \\
&= \lim_{h \to 0} \frac{4x + 4h - (x^2 + 2xh + h^2) - 4x + x^2}{h} \\
&= \lim_{h \to 0} \frac{4h - 2xh - h^2}{h} \\
&= \lim_{h \to 0} (4 - 2x - h) \\
&= 4 - 2x
\end{aligned}`
$$

因此 $`f'(x) = 4 - 2x`$。

**验证**：使用幂法则对 $`f(x) = 4x - x^2`$ 逐项求导：
- $`\dfrac{d}{dx}(4x) = 4 \cdot 1 \cdot x^{0} = 4`$
- $`\dfrac{d}{dx}(-x^2) = -2x^{1} = -2x`$
- 相加得 $`f'(x) = 4 - 2x`$，与极限结果一致。✓

---

**例题 3**（向量的变化率 + 积分逆运算）

一个质点在平面内运动，它的位置向量为：

$$
`\mathbf{r}(t) = (t^3 - 3t)\mathbf{i} + (t^2 - 2t)\mathbf{j}`
$$

其中 $`t`$ 以秒为单位，位置以米为单位。

（a）求速度向量 $`\mathbf{v}(t)`$。
（b）求加速度向量 $`\mathbf{a}(t)`$。
（c）求 $`t = 2`$ 秒时的速度和加速度向量。
（d）已知该质点的加速度恒为 $`\mathbf{a}(t) = 6t\mathbf{i} + 2\mathbf{j}`$，初速度 $`\mathbf{v}_0 = -3\mathbf{i} - 2\mathbf{j}`$，初始位置 $`\mathbf{r}_0 = \mathbf{0}`$。用积分求 $`\mathbf{v}(t)`$ 和 $`\mathbf{r}(t)`$，验证与（a）（b）一致。

**思路分析**：
- 速度 = 位置的导数（分量分别求导）
- 加速度 = 速度的导数（分量分别求导）
- 积分是微分的逆运算：已知加速度，积分一次得速度（加常数），再积分一次得位置（加常数）
- 常数由初始条件确定

**解**：

（a）速度是位置对时间的导数，对各分量分别求导：

$$
`\mathbf{v}(t) = \frac{d\mathbf{r}}{dt} = \frac{d}{dt}(t^3 - 3t)\,\mathbf{i} + \frac{d}{dt}(t^2 - 2t)\,\mathbf{j}`
$$

使用幂法则：
- $`\dfrac{d}{dt}(t^3) = 3t^2`$
- $`\dfrac{d}{dt}(-3t) = -3`$
- $`\dfrac{d}{dt}(t^2) = 2t`$
- $`\dfrac{d}{dt}(-2t) = -2`$

因此：

$$
`\mathbf{v}(t) = (3t^2 - 3)\mathbf{i} + (2t - 2)\mathbf{j}`
$$

（b）加速度是速度对时间的导数：

$$
`\mathbf{a}(t) = \frac{d\mathbf{v}}{dt} = \frac{d}{dt}(3t^2 - 3)\,\mathbf{i} + \frac{d}{dt}(2t - 2)\,\mathbf{j}`
$$

$$
`\mathbf{a}(t) = (6t)\mathbf{i} + 2\mathbf{j}`
$$

（c）代入 $`t = 2`$：

$$
`\mathbf{v}(2) = (3 \times 4 - 3)\mathbf{i} + (4 - 2)\mathbf{j} = 9\mathbf{i} + 2\mathbf{j}\ \text{m/s}`
$$

速度的大小：$`|\mathbf{v}(2)| = \sqrt{9^2 + 2^2} = \sqrt{81 + 4} = \sqrt{85} \approx 9.22\ \text{m/s}`$

$$
`\mathbf{a}(2) = (6 \times 2)\mathbf{i} + 2\mathbf{j} = 12\mathbf{i} + 2\mathbf{j}\ \text{m/s}^2`
$$

加速度的大小：$`|\mathbf{a}(2)| = \sqrt{12^2 + 2^2} = \sqrt{144 + 4} = \sqrt{148} = 2\sqrt{37} \approx 12.17\ \text{m/s}^2`$

（d）已知 $`\mathbf{a}(t) = (6t)\mathbf{i} + 2\mathbf{j}`$，对加速度积分求速度：

$$
`\mathbf{v}(t) = \int \mathbf{a}(t) \, dt = \left(\int 6t \, dt\right)\mathbf{i} + \left(\int 2 \, dt\right)\mathbf{j}`
$$

$$
`= (3t^2 + C_1)\mathbf{i} + (2t + C_2)\mathbf{j}`
$$

由 $`\mathbf{v}_0 = \mathbf{v}(0) = -3\mathbf{i} - 2\mathbf{j}`$，代入 $`t = 0`$ 得 $`C_1 = -3`$，$`C_2 = -2`$。所以：

$$
`\mathbf{v}(t) = (3t^2 - 3)\mathbf{i} + (2t - 2)\mathbf{j}`
$$

与（a）一致。✓

再对速度积分求位置：

$$
`\mathbf{r}(t) = \int \mathbf{v}(t) \, dt = \left(\int (3t^2 - 3) \, dt\right)\mathbf{i} + \left(\int (2t - 2) \, dt\right)\mathbf{j}`
$$

$$
`= (t^3 - 3t + D_1)\mathbf{i} + (t^2 - 2t + D_2)\mathbf{j}`
$$

由 $`\mathbf{r}_0 = \mathbf{r}(0) = \mathbf{0}`$，代入 $`t = 0`$ 得 $`D_1 = 0`$，$`D_2 = 0`$。所以：

$$
`\mathbf{r}(t) = (t^3 - 3t)\mathbf{i} + (t^2 - 2t)\mathbf{j}`
$$

与原始位置函数一致。✓

---

## 2.4 本章练习题

以下练习题按考试难度编写，涵盖本章所有知识点，题号前面标注了对应的考纲编号。

---

**13.1–13.3 题组：向量基础与几何**

**1.** 已知 $`\mathbf{a} = 2\mathbf{i} - \mathbf{j}`$，$`\mathbf{b} = \mathbf{i} + 3\mathbf{j}`$。

（a）求 $`\mathbf{a} + 2\mathbf{b}`$。
（b）求 $`|2\mathbf{a} - \mathbf{b}|`$。
（c）求与 $`3\mathbf{a} + \mathbf{b}`$ 同方向的单位向量。

---

**2.** 在 $`\triangle ABC`$ 中，$`P`$ 是 $`BC`$ 的中点，$`Q`$ 是 $`CA`$ 的中点。设 $`\overrightarrow{AB} = \mathbf{p}`$，$`\overrightarrow{AC} = \mathbf{q}`$。

（a）用 $`\mathbf{p}`$ 和 $`\mathbf{q}`$ 表示 $`\overrightarrow{BC}`$。
（b）用 $`\mathbf{p}`$ 和 $`\mathbf{q}`$ 表示 $`\overrightarrow{PQ}`$。
（c）证明 $`PQ \parallel AB`$ 且 $`PQ = \frac{1}{2} AB`$。

---

**3.** 三点 $`A`$、$`B`$、$`C`$ 的位置向量分别为 $`\mathbf{a} = 3\mathbf{i} + 2\mathbf{j}`$，$`\mathbf{b} = 5\mathbf{i} + 6\mathbf{j}`$，$`\mathbf{c} = 9\mathbf{i} + 14\mathbf{j}`$。

（a）证明 $`A`$、$`B`$、$`C`$ 三点共线。
（b）求 $`AB:BC`$ 的比值。

---

**13.3–13.4 题组：向量几何与运动**

**4.** 在 $`\triangle OAB`$ 中，$`P`$ 在 $`OA`$ 上且 $`OP:PA = 1:2`$，$`Q`$ 在 $`AB`$ 上且 $`AQ:QB = 2:3`$。设 $`\overrightarrow{OA} = \mathbf{a}`$，$`\overrightarrow{OB} = \mathbf{b}`$。

（a）用 $`\mathbf{a}`$ 和 $`\mathbf{b}`$ 表示 $`\overrightarrow{OP}`$。
（b）用 $`\mathbf{a}`$ 和 $`\mathbf{b}`$ 表示 $`\overrightarrow{OQ}`$。
（c）用 $`\mathbf{a}`$ 和 $`\mathbf{b}`$ 表示 $`\overrightarrow{PQ}`$。

---

**5.** 船 $`A`$ 从点 $`(0, 5)`$ 出发，以速度 $`\mathbf{v}_A = (2\mathbf{i} + 3\mathbf{j})\ \text{km/h}`$ 航行。船 $`B`$ 从点 $`(10, 0)`$ 出发，以速度 $`\mathbf{v}_B = (-3\mathbf{i} + 4\mathbf{j})\ \text{km/h}`$ 航行。两船同时出发。

（a）写出两船的位置向量 $`\mathbf{r}_A(t)`$ 和 $`\mathbf{r}_B(t)`$。
（b）判断两船是否会相撞。

---

**6.** 一艘船在静水中的速度为 $`10\ \text{m/s}`$，船头指向正北方向。水流的速度为 $`6\ \text{m/s}`$ 流向正东方向。

（a）求船相对于地面的合速度向量。
（b）求合速度的大小和方向（与正北方向的夹角）。

---

**14.1 题组：变化率入门**

**7.** 一个质点的位移 $`s`$（米）与时间 $`t`$（秒）的关系为 $`s(t) = 4t^2 + 3t`$。

（a）求从 $`t = 1`$ 到 $`t = 1 + h`$ 的平均速度。
（b）利用极限求 $`t = 1`$ 时的瞬时速度。

---

**8.** 一个质点在平面内运动，它的位置向量为：

$$
`\mathbf{r}(t) = (2t^2 + t)\mathbf{i} + (3t - 1)\mathbf{j}`
$$

（a）求速度向量 $`\mathbf{v}(t)`$。
（b）求加速度向量 $`\mathbf{a}(t)`$。
（c）求 $`t = 2`$ 时速度的大小。

---

**综合题**

**9.** 在平行四边形 $`ABCD`$ 中，$`A`$、$`B`$、$`C`$ 的位置向量分别为 $`\mathbf{a} = 2\mathbf{i} + \mathbf{j}`$，$`\mathbf{b} = 5\mathbf{i} + 3\mathbf{j}`$，$`\mathbf{c} = 4\mathbf{i} + 6\mathbf{j}`$。

（a）求 $`D`$ 的位置向量。
（b）判断 $`\overrightarrow{AB}`$ 与 $`\overrightarrow{AD}`$ 是否垂直。
（c）求平行四边形 $`ABCD`$ 的面积。

> 提示：平行四边形的面积 $`= |\overrightarrow{AB}| \times |\overrightarrow{AD}| \times \sin\theta`$，其中 $`\theta`$ 是两边的夹角。或者用行列式公式：面积 $`= |x_1 y_2 - x_2 y_1|`$，其中 $`\overrightarrow{AB} = (x_1, y_1)`$，$`\overrightarrow{AD} = (x_2, y_2)`$。

---

## 练习题答案

**1.**

（a）$`\mathbf{a} + 2\mathbf{b} = (2\mathbf{i} - \mathbf{j}) + 2(\mathbf{i} + 3\mathbf{j}) = (2\mathbf{i} - \mathbf{j}) + (2\mathbf{i} + 6\mathbf{j}) = 4\mathbf{i} + 5\mathbf{j}`$

（b）$`2\mathbf{a} - \mathbf{b} = 2(2\mathbf{i} - \mathbf{j}) - (\mathbf{i} + 3\mathbf{j}) = (4\mathbf{i} - 2\mathbf{j}) - (\mathbf{i} + 3\mathbf{j}) = 3\mathbf{i} - 5\mathbf{j}`$

$`|2\mathbf{a} - \mathbf{b}| = \sqrt{3^2 + (-5)^2} = \sqrt{9 + 25} = \sqrt{34}`$

（c）$`3\mathbf{a} + \mathbf{b} = 3(2\mathbf{i} - \mathbf{j}) + (\mathbf{i} + 3\mathbf{j}) = (6\mathbf{i} - 3\mathbf{j}) + (\mathbf{i} + 3\mathbf{j}) = 7\mathbf{i}`$

$`|7\mathbf{i}| = 7`$，所以单位向量 $`= \dfrac{7\mathbf{i}}{7} = \mathbf{i}`$

---

**2.**

（a）$`\overrightarrow{BC} = \overrightarrow{BA} + \overrightarrow{AC} = -\overrightarrow{AB} + \overrightarrow{AC} = -\mathbf{p} + \mathbf{q}`$

（b）$`P`$ 是 $`BC`$ 的中点，所以 $`\mathbf{r}_P = \dfrac{\mathbf{r}_B + \mathbf{r}_C}{2}`$。$`Q`$ 是 $`CA`$ 的中点，所以 $`\mathbf{r}_Q = \dfrac{\mathbf{r}_C + \mathbf{r}_A}{2}`$。

$$
`\begin{aligned}
\overrightarrow{PQ} &= \mathbf{r}_Q - \mathbf{r}_P \\
&= \frac{\mathbf{r}_C + \mathbf{r}_A}{2} - \frac{\mathbf{r}_B + \mathbf{r}_C}{2} \\
&= \frac{\mathbf{r}_A - \mathbf{r}_B}{2} \\
&= \frac{1}{2}\overrightarrow{BA} = -\frac{1}{2}\overrightarrow{AB} = -\frac{1}{2}\mathbf{p}
\end{aligned}`
$$

（c）由（b）得 $`\overrightarrow{PQ} = -\dfrac{1}{2}\mathbf{p} = -\dfrac{1}{2}\overrightarrow{AB}`$，所以 $`\overrightarrow{PQ} \parallel \overrightarrow{AB}`$ 且 $`|\overrightarrow{PQ}| = \dfrac{1}{2}|\overrightarrow{AB}|`$，即 $`PQ = \dfrac{1}{2}AB`$。✓

> 这条性质叫做**三角形中位线定理**：三角形两边中点的连线平行于第三边且等于第三边的一半。

---

**3.**

（a）

$$
`\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (5\mathbf{i} + 6\mathbf{j}) - (3\mathbf{i} + 2\mathbf{j}) = 2\mathbf{i} + 4\mathbf{j}`
$$

$$
`\overrightarrow{BC} = \mathbf{c} - \mathbf{b} = (9\mathbf{i} + 14\mathbf{j}) - (5\mathbf{i} + 6\mathbf{j}) = 4\mathbf{i} + 8\mathbf{j}`
$$

$`\overrightarrow{BC} = 2(2\mathbf{i} + 4\mathbf{j}) = 2\overrightarrow{AB}`$，存在 $`k = 2`$ 使得 $`\overrightarrow{BC} = k\overrightarrow{AB}`$，所以 $`A`$、$`B`$、$`C`$ 共线。

（b）$`|\overrightarrow{AB}| = \sqrt{2^2 + 4^2} = \sqrt{4 + 16} = \sqrt{20} = 2\sqrt{5}`$

$`|\overrightarrow{BC}| = \sqrt{4^2 + 8^2} = \sqrt{16 + 64} = \sqrt{80} = 4\sqrt{5}`$

所以 $`AB:BC = 2\sqrt{5}:4\sqrt{5} = 1:2`$

---

**4.**

（a）$`OP:PA = 1:2`$，所以 $`OP:OA = 1:3`$，即 $`\overrightarrow{OP} = \dfrac{1}{3}\mathbf{a}`$

（b）$`AQ:QB = 2:3`$，所以 $`AQ:AB = 2:5`$，$`Q`$ 从 $`A`$ 到 $`B`$ 的 $`\dfrac{2}{5}`$ 处。

$$
`\begin{aligned}
\overrightarrow{OQ} &= \overrightarrow{OA} + \frac{2}{5}\overrightarrow{AB} \\
&= \mathbf{a} + \frac{2}{5}(\mathbf{b} - \mathbf{a}) \\
&= \mathbf{a} + \frac{2}{5}\mathbf{b} - \frac{2}{5}\mathbf{a} \\
&= \frac{3}{5}\mathbf{a} + \frac{2}{5}\mathbf{b}
\end{aligned}`
$$

（c）

$$
`\overrightarrow{PQ} = \overrightarrow{OQ} - \overrightarrow{OP} = \left(\frac{3}{5}\mathbf{a} + \frac{2}{5}\mathbf{b}\right) - \frac{1}{3}\mathbf{a} = \left(\frac{3}{5} - \frac{1}{3}\right)\mathbf{a} + \frac{2}{5}\mathbf{b}`
$$

通分：$`\dfrac{3}{5} - \dfrac{1}{3} = \dfrac{9}{15} - \dfrac{5}{15} = \dfrac{4}{15}`$

所以 $`\overrightarrow{PQ} = \dfrac{4}{15}\mathbf{a} + \dfrac{2}{5}\mathbf{b}`$

---

**5.**

（a）

$$
`\mathbf{r}_A(t) = (0, 5)^\mathrm{T} + (2, 3)^\mathrm{T}\,t = (2t,\; 5 + 3t)^\mathrm{T}`
$$

$$
`\mathbf{r}_B(t) = (10, 0)^\mathrm{T} + (-3, 4)^\mathrm{T}\,t = (10 - 3t,\; 4t)^\mathrm{T}`
$$

（b）令 $`\mathbf{r}_A(t) = \mathbf{r}_B(t)`$：

$$
`\begin{cases}
2t = 10 - 3t \;\Longrightarrow\; 5t = 10 \;\Longrightarrow\; t = 2 \\[4pt]
5 + 3t = 4t \;\Longrightarrow\; 5 = t \;\Longrightarrow\; t = 5
\end{cases}`
$$

两个 $`t`$ 值不相等（$`2 \neq 5`$），所以两船不会相撞。

---

**6.**

（a）设正北为 $`+y`$ 轴，正东为 $`+x`$ 轴。

船相对于水的速度：$`\mathbf{v}_{B/W} = 10\mathbf{j}`$
水相对于地面的速度：$`\mathbf{v}_{W/G} = 6\mathbf{i}`$

合速度：$`\mathbf{v}_{B/G} = 6\mathbf{i} + 10\mathbf{j}`$

（b）大小：$`|\mathbf{v}_{B/G}| = \sqrt{6^2 + 10^2} = \sqrt{36 + 100} = \sqrt{136} = 2\sqrt{34} \approx 11.66\ \text{m/s}`$

方向：设 $`\theta`$ 为与正北方向的夹角。

$$
`\tan\theta = \frac{6}{10} = 0.6 \;\Longrightarrow\; \theta = \arctan(0.6) \approx 30.96^\circ`
$$

所以方向为东偏北 $`30.96^\circ`$（或北偏东 $`59.04^\circ`$）。

---

**7.**

（a）

$$
`\begin{aligned}
\frac{s(1+h) - s(1)}{h} &= \frac{[4(1+h)^2 + 3(1+h)] - [4 + 3]}{h} \\
&= \frac{[4(1 + 2h + h^2) + 3 + 3h] - 7}{h} \\
&= \frac{4 + 8h + 4h^2 + 3 + 3h - 7}{h} \\
&= \frac{11h + 4h^2}{h} = 11 + 4h
\end{aligned}`
$$

（b）$`v(1) = \displaystyle\lim_{h \to 0} (11 + 4h) = 11\ \text{m/s}`$

验证：$`s'(t) = 8t + 3`$，$`s'(1) = 8 + 3 = 11`$ ✓

---

**8.**

（a）$`\mathbf{v}(t) = \dfrac{d\mathbf{r}}{dt} = (4t + 1)\mathbf{i} + 3\mathbf{j}`$

（b）$`\mathbf{a}(t) = \dfrac{d\mathbf{v}}{dt} = 4\mathbf{i}`$

（c）$`\mathbf{v}(2) = (4 \times 2 + 1)\mathbf{i} + 3\mathbf{j} = 9\mathbf{i} + 3\mathbf{j}`$

$`|\mathbf{v}(2)| = \sqrt{9^2 + 3^2} = \sqrt{81 + 9} = \sqrt{90} = 3\sqrt{10} \approx 9.49\ \text{m/s}`$

---

**9.**

（a）平行四边形 $`ABCD`$ 中，$`\overrightarrow{AD} = \overrightarrow{BC}`$。

$$
`\overrightarrow{BC} = \mathbf{c} - \mathbf{b} = (4\mathbf{i} + 6\mathbf{j}) - (5\mathbf{i} + 3\mathbf{j}) = -\mathbf{i} + 3\mathbf{j}`
$$

所以 $`\mathbf{d} = \mathbf{a} + \overrightarrow{BC} = (2\mathbf{i} + \mathbf{j}) + (-\mathbf{i} + 3\mathbf{j}) = \mathbf{i} + 4\mathbf{j}`$

（b）$`\overrightarrow{AB} = \mathbf{b} - \mathbf{a} = (5\mathbf{i} + 3\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = 3\mathbf{i} + 2\mathbf{j}`$

$`\overrightarrow{AD} = \mathbf{d} - \mathbf{a} = (\mathbf{i} + 4\mathbf{j}) - (2\mathbf{i} + \mathbf{j}) = -\mathbf{i} + 3\mathbf{j}`$

点积：$`\overrightarrow{AB} \cdot \overrightarrow{AD} = (3)(-1) + (2)(3) = -3 + 6 = 3 \neq 0`$

所以 $`\overrightarrow{AB}`$ 与 $`\overrightarrow{AD}`$ **不垂直**。

（c）方法一（用叉积的行列式公式）：

$$
`\text{面积} = |x_1 y_2 - x_2 y_1|`
$$

其中 $`\overrightarrow{AB} = (3, 2)`$，$`\overrightarrow{AD} = (-1, 3)`$。

$$
`\text{面积} = |3 \times 3 - 2 \times (-1)| = |9 + 2| = 11`
$$

方法二（用 $`|\overrightarrow{AB}| \cdot |\overrightarrow{AD}| \cdot \sin\theta`$）：

$$
`|\overrightarrow{AB}| = \sqrt{3^2 + 2^2} = \sqrt{13},\quad |\overrightarrow{AD}| = \sqrt{(-1)^2 + 3^2} = \sqrt{10}`
$$

由点积 $`\overrightarrow{AB} \cdot \overrightarrow{AD} = |\overrightarrow{AB}||\overrightarrow{AD}|\cos\theta`$：

$$
`3 = \sqrt{13} \cdot \sqrt{10} \cdot \cos\theta \;\Longrightarrow\; \cos\theta = \frac{3}{\sqrt{130}}`
$$

$$
`\sin\theta = \sqrt{1 - \cos^2\theta} = \sqrt{1 - \frac{9}{130}} = \sqrt{\frac{121}{130}} = \frac{11}{\sqrt{130}}`
$$

$$
`\text{面积} = \sqrt{13} \cdot \sqrt{10} \cdot \frac{11}{\sqrt{130}} = \sqrt{130} \cdot \frac{11}{\sqrt{130}} = 11`
$$

平行四边形的面积为 11 平方单位。✓

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
| 向量表示 | $`\mathbf{v} = x\mathbf{i} + y\mathbf{j} = (x, y)^\mathrm{T}`$ |
| 模 | $`|\mathbf{v}| = \sqrt{x^2 + y^2}`$ |
| 单位向量 | $`\hat{\mathbf{v}} = \dfrac{\mathbf{v}}{|\mathbf{v}|}`$ |
| 位移 | $`\overrightarrow{AB} = \mathbf{r}_B - \mathbf{r}_A`$ |
| 中点 | $`\mathbf{r}_M = \dfrac{\mathbf{r}_A + \mathbf{r}_B}{2}`$ |
| 分点（$`AP:PB = m:n`$） | $`\mathbf{r}_P = \dfrac{n\mathbf{r}_A + m\mathbf{r}_B}{m+n}`$ |
| 平行条件 | $`\mathbf{a} = k\mathbf{b}`$（存在标量 $`k`$） |
| 垂直条件（点积） | $`\mathbf{u} \cdot \mathbf{v} = u_x v_x + u_y v_y = 0`$ |
| 斜率法判垂直 | $`k_1 \cdot k_2 = -1`$ |
| 速度合成 | $`\mathbf{v}_{A/C} = \mathbf{v}_{A/B} + \mathbf{v}_{B/C}`$ |
| 速度分解 | $`\mathbf{v} = (v\cos\theta)\,\mathbf{i} + (v\sin\theta)\,\mathbf{j}`$ |
| 匀速直线运动 | $`\mathbf{r}(t) = \mathbf{r}_0 + \mathbf{v}t`$ |
| 相撞条件 | $`\mathbf{r}_1(t) = \mathbf{r}_2(t)`$ |

**变化率部分**：

| 概念 | 公式 |
|:---|:---|
| 导数定义 | $`f'(a) = \displaystyle\lim_{h \to 0} \dfrac{f(a + h) - f(a)}{h}`$ |
| 幂法则 | $`\dfrac{d}{dx}(x^n) = n x^{n-1}`$ |
| 速度（向量） | $`\mathbf{v}(t) = \dfrac{d\mathbf{r}}{dt} = \dfrac{dx}{dt}\mathbf{i} + \dfrac{dy}{dt}\mathbf{j}`$ |
| 加速度（向量） | $`\mathbf{a}(t) = \dfrac{d\mathbf{v}}{dt} = \dfrac{d^2x}{dt^2}\mathbf{i} + \dfrac{d^2y}{dt^2}\mathbf{j}`$ |
| 积分求速度 | $`\mathbf{v}(t) = \int \mathbf{a}(t) \, dt + \mathbf{v}_0`$ |
| 积分求位置 | $`\mathbf{r}(t) = \int \mathbf{v}(t) \, dt + \mathbf{r}_0`$ |

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
|---------|------|---------|
| 3.1 | 余数定理与因式定理 | 3.1.1, 3.1.2 |
| 3.2 | 分解多项式（三次 → 线性×二次） | 3.1.3 |
| 3.3 | 解三次方程 | 3.1.4 |
| 2.1 | 配方法或微分求二次函数极值 | 3.4, 3.7 |
| 2.2 | 利用最值画草图或求值域 | 3.4 |
| 2.3 | 判别式与根的条件、直线与曲线位置关系 | 3.2 |
| 2.4 | 解二次方程（因式分解、公式法、配方法） | 3.3 |
| 2.5 | 二次不等式（代数法或图像法） | 3.5 |
| 4.4 | 三个线性因式乘积的图像与绝对值图像 | 3.6.1, 3.6.2 |
| 4.5 | 三次不等式的图像解法 | 3.6.3 |

---

## 3.1 多项式的因式

### 3.1.1 余数定理

**定理陈述**：当多项式 f(x) 除以线性因式 (x - a) 时，余数等于 f(a)。

**完整推导**：

设 f(x) 除以 (x - a)，得到商式 q(x) 和余数 R。由于除式 (x - a) 是一次式，余数 R 的次数必须低于除式的次数，所以 R 只能是一个常数。因此有恒等式：

f(x) = (x - a) * q(x) + R

这个等式对所有 x 的值都成立——这是多项式恒等式的基本性质。

现在，我们选择 x = a 代入：

f(a) = (a - a) * q(a) + R = 0 * q(a) + R = R

因此 R = f(a)。这就是余数定理。

**推广形式**：

如果除式是 (ax + b)，则令 ax + b = 0 解出 x = -b/a，余数为：

R = f(-b/a)

---

**例题 1**：多项式 f(x) = 2x³ - 3x² + 4x - 5 除以 x - 2，求余数。

**解**：

除式为 x - 2，令 x - 2 = 0 得 x = 2。由余数定理，余数 R = f(2)。

f(2) = 2(2)³ - 3(2)² + 4(2) - 5
= 2 × 8 - 3 × 4 + 8 - 5
= 16 - 12 + 8 - 5
= 7

余数为 7。

---

**例题 2**：多项式 f(x) = x³ + kx² - 2x + 3 除以 x + 1 余数为 5，求常数 k 的值。

**解**：

除式为 x + 1，令 x + 1 = 0 得 x = -1。由余数定理，余数等于 f(-1)，已知余数为 5，所以 f(-1) = 5。

f(-1) = (-1)³ + k(-1)² - 2(-1) + 3
= -1 + k + 2 + 3
= k + 4 = 5

k = 1

---

**例题 3**：多项式 f(x) = 6x³ + x² - 8x + 2 除以 2x - 1，求余数。

**解**：

令 2x - 1 = 0，解得 x = 1/2。

f(1/2) = 6(1/2)³ + (1/2)² - 8(1/2) + 2
= 6 × (1/8) + 1/4 - 4 + 2
= 3/4 + 1/4 - 2
= 1 - 2 = -1

余数为 -1。

---

**例题 4**：多项式 f(x) = 4x⁴ - 3x³ + 2x² - x + 5 除以 x - 1，求余数。

**解**：

令 x - 1 = 0 得 x = 1。余数 R = f(1)。

f(1) = 4(1)⁴ - 3(1)³ + 2(1)² - 1 + 5
= 4 - 3 + 2 - 1 + 5
= 7

余数为 7。

---

**例题 5**：多项式 f(x) = x⁴ - 2x³ + 3x² - 4x + 2 除以 x + 2，求余数。

**解**：

令 x + 2 = 0 得 x = -2。

f(-2) = (-2)⁴ - 2(-2)³ + 3(-2)² - 4(-2) + 2
= 16 - 2(-8) + 3(4) + 8 + 2
= 16 + 16 + 12 + 8 + 2
= 54

余数为 54。

---

**例题 6**：多项式 f(x) = 8x³ - 4x² + 2x - 1 除以 2x + 3，求余数。

**解**：

令 2x + 3 = 0 得 x = -3/2。

f(-3/2) = 8(-3/2)³ - 4(-3/2)² + 2(-3/2) - 1
= 8(-27/8) - 4(9/4) - 3 - 1
= -27 - 9 - 3 - 1
= -40

余数为 -40。

---

### 3.1.2 因式定理

**定理陈述**：如果 f(a) = 0，那么 (x - a) 是 f(x) 的一个因式。反之，如果 (x - a) 是 f(x) 的一个因式，那么 f(a) = 0。

**推导**：

因式定理是余数定理的直接推论。由余数定理，f(x) 除以 (x - a) 的余数等于 f(a)。如果 f(a) = 0，意味着余数为零——也就是说 (x - a) 完全整除 f(x)，没有余数，所以 (x - a) 是 f(x) 的一个因式。

反过来，如果 (x - a) 是 f(x) 的因式，那么 f(x) = (x - a) * q(x)，代入 x = a 得 f(a) = 0。

**实际意义**：

要判断 (x - a) 是不是 f(x) 的因式，只需要看 f(a) 是否等于 0。这比做长除法快得多。同时，因式定理是分解三次多项式的起点——通过试根找到一个零点，就等于找到了一个线性因式。

---

**例题 1**：证明 (x - 2) 是 f(x) = x³ - 3x² - 4x + 12 的一个因式。

**解**：

f(2) = 2³ - 3(2)² - 4(2) + 12
= 8 - 12 - 8 + 12
= 0

因为 f(2) = 0，所以 (x - 2) 是 f(x) 的一个因式。

---

**例题 2**：多项式 f(x) = 2x³ + ax² + bx - 6 有因式 (x - 1) 和 (x + 2)，求 a 和 b 的值。

**解**：

由因式定理：
- (x - 1) 是因式 ⇒ f(1) = 0
- (x + 2) 是因式 ⇒ f(-2) = 0

由 f(1) = 0：2 + a + b - 6 = 0 ⇒ a + b = 4 ... (1)

由 f(-2) = 0：-16 + 4a - 2b - 6 = 0 ⇒ 4a - 2b = 22 ... (2)

联立 (1)(2)：由 (1) 得 b = 4 - a，代入 (2)：
4a - 2(4 - a) = 22 ⇒ 4a - 8 + 2a = 22 ⇒ 6a = 30 ⇒ a = 5

b = 4 - 5 = -1

---

**例题 3**：已知 x - 2 是 f(x) = x³ - px² + 5x - 2 的一个因式，求 p 的值并将 f(x) 完全因式分解。

**解**：

由因式定理，f(2) = 0：
8 - 4p + 10 - 2 = 16 - 4p = 0 ⇒ p = 4

所以 f(x) = x³ - 4x² + 5x - 2。

用综合除法除以 (x - 2)：
```
    2 |  1   -4    5   -2
      |      2   -4    2
      -------------------
         1   -2    1    0
```

商式为 x² - 2x + 1 = (x - 1)²。

因此：f(x) = (x - 2)(x - 1)²

---

**例题 4**：已知 x - 3 是 f(x) = 2x³ - 7x² + 2x + 3 的一个因式，将 f(x) 分解。

**解**：

综合除法：
```
    3 |  2   -7    2    3
      |      6   -3   -3
      -------------------
         2   -1   -1    0
```

商式为 2x² - x - 1。

分解二次式：2x² - x - 1 = 2x² - 2x + x - 1 = 2x(x - 1) + 1(x - 1) = (2x + 1)(x - 1)

因此：f(x) = (x - 3)(2x + 1)(x - 1)

---

**例题 5**：多项式 f(x) = 3x³ + kx² - 4x + 4 有因式 (x + 1)，求 k 的值。

**解**：

(x + 1) 是因式 ⇒ f(-1) = 0。

f(-1) = -3 + k + 4 + 4 = k + 5 = 0 ⇒ k = -5

---

**例题 6**：已知 x - 1 和 x - 2 都是 f(x) = x³ + ax² + bx + c 的因式，且 f(x) 除以 x + 1 余数为 -12，求 a, b, c 的值并写出 f(x) 的完整因式分解。

**解**：

由已知条件：

f(1) = 1 + a + b + c = 0 ⇒ a + b + c = -1 ... (1)
f(2) = 8 + 4a + 2b + c = 0 ⇒ 4a + 2b + c = -8 ... (2)
f(-1) = -1 + a - b + c = -12 ⇒ a - b + c = -11 ... (3)

(2) - (1)：3a + b = -7 ... (4)
(1) - (3)：2b = 10 ⇒ b = 5

代入 (4)：3a + 5 = -7 ⇒ 3a = -12 ⇒ a = -4

代入 (1)：-4 + 5 + c = -1 ⇒ c = -2

所以 f(x) = x³ - 4x² + 5x - 2。

验证：
- f(1) = 1 - 4 + 5 - 2 = 0 ✓
- f(2) = 8 - 16 + 10 - 2 = 0 ✓
- f(-1) = -1 - 4 - 5 - 2 = -12 ✓

用综合除法除以 (x - 1)：
```
    1 |  1   -4    5   -2
      |      1   -3    2
      -------------------
         1   -3    2    0
```

商式为 x² - 3x + 2 = (x - 1)(x - 2)。

所以 f(x) = (x - 1)²(x - 2)。

---

### 3.1.3 分解三次多项式

分解三次多项式 f(x) = ax³ + bx² + cx + d 的标准流程：

**Step 1：试根**——用因式定理找线性因式
试 x = ±1, ±2, ±3 等，以及分数 ±(常数项的因数)/(首项系数的因数)。找到 p 使得 f(p) = 0，则 (x - p) 是一个因式。

**Step 2：综合除法**——求二次商式
将 f(x) 除以 (x - p)，得到二次式 Ax² + Bx + C。

**Step 3：分解二次式**
用因式分解、求根公式或配方法分解 Ax² + Bx + C。

**Step 4：完整因式分解**
写出 f(x) = (x - p) × (二次因式的分解)。

---

**例题 1**：分解 f(x) = x³ - 6x² + 11x - 6。

**解**：

试 x = 1：f(1) = 1 - 6 + 11 - 6 = 0，所以 (x - 1) 是一个因式。

综合除法：
```
    1 |  1   -6   11   -6
      |      1   -5    6
      -------------------
         1   -5    6    0
```

商式为 x² - 5x + 6。

分解二次式：x² - 5x + 6 = (x - 2)(x - 3)。

完整分解：f(x) = (x - 1)(x - 2)(x - 3)

---

**例题 2**：分解 f(x) = 2x³ - 3x² - 11x + 6。

**解**：

试 x = 1：f(1) = 2 - 3 - 11 + 6 = -6 ≠ 0。
试 x = -2：f(-2) = -16 - 12 + 22 + 6 = 0，所以 (x + 2) 是一个因式。

综合除法：
```
    -2 |  2   -3   -11    6
       |     -4    14   -6
       --------------------
          2   -7     3    0
```

商式为 2x² - 7x + 3。

分解二次式 2x² - 7x + 3：
2x² - 7x + 3 = 2x² - x - 6x + 3 = x(2x - 1) - 3(2x - 1) = (2x - 1)(x - 3)

完整分解：f(x) = (x + 2)(2x - 1)(x - 3)

---

**例题 3**：分解 f(x) = 3x³ + 6x² - 3x - 6。

**解**：

提取公因式 3：f(x) = 3(x³ + 2x² - x - 2)

令 g(x) = x³ + 2x² - x - 2。

试 x = 1：g(1) = 1 + 2 - 1 - 2 = 0，所以 (x - 1) 是 g(x) 的因式。

综合除法：
```
    1 |  1    2   -1   -2
      |       1    3    2
      --------------------
         1    3    2    0
```

商式为 x² + 3x + 2 = (x + 1)(x + 2)。

完整分解：f(x) = 3(x - 1)(x + 1)(x + 2)

---

**例题 4**：分解 f(x) = 2x³ - 9x² + 7x + 6。

**解**：

试 x = 1：f(1) = 2 - 9 + 7 + 6 = 6 ≠ 0。
试 x = -1：f(-1) = -2 - 9 - 7 + 6 = -12 ≠ 0。
试 x = 2：f(2) = 16 - 36 + 14 + 6 = 0，所以 (x - 2) 是一个因式。

综合除法：
```
    2 |  2   -9    7    6
      |       4  -10   -6
      --------------------
         2   -5   -3    0
```

商式为 2x² - 5x - 3。

分解二次式 2x² - 5x - 3：
2x² - 5x - 3 = 2x² - 6x + x - 3 = 2x(x - 3) + 1(x - 3) = (2x + 1)(x - 3)

完整分解：f(x) = (x - 2)(2x + 1)(x - 3)

---

**例题 5**：分解 f(x) = 6x³ - 7x² - 7x + 6。

**解**：

试 x = 1：f(1) = 6 - 7 - 7 + 6 = -2 ≠ 0。
试 x = -1：f(-1) = -6 - 7 + 7 + 6 = 0，所以 (x + 1) 是一个因式。

综合除法：
```
    -1 |  6   -7   -7    6
       |     -6   13   -6
       --------------------
          6  -13    6    0
```

商式为 6x² - 13x + 6。

分解二次式 6x² - 13x + 6：
6x² - 13x + 6 = 6x² - 9x - 4x + 6 = 3x(2x - 3) - 2(2x - 3) = (3x - 2)(2x - 3)

完整分解：f(x) = (x + 1)(3x - 2)(2x - 3)

---

**例题 6**：分解 f(x) = x³ + 2x² - 5x - 6。

**解**：

试 x = 1：f(1) = 1 + 2 - 5 - 6 = -8 ≠ 0。
试 x = -1：f(-1) = -1 + 2 + 5 - 6 = 0，所以 (x + 1) 是一个因式。

综合除法：
```
    -1 |  1    2   -5   -6
       |     -1   -1    6
       --------------------
          1    1   -6    0
```

商式为 x² + x - 6 = (x + 3)(x - 2)。

完整分解：f(x) = (x + 1)(x + 3)(x - 2)

---

### 3.1.4 解三次方程

解三次方程 ax³ + bx² + cx + d = 0 的流程就是将三次多项式分解因式，然后令每个因式等于零。因为如果几个因式的乘积为零，则至少其中一个因式为零。

---

**例题 1**：解 x³ - 4x² + x + 6 = 0。

**解**：

试根：f(2) = 8 - 16 + 2 + 6 = 0，所以 (x - 2) 是因式。

综合除法：
```
    2 |  1   -4    1    6
      |       2   -4   -6
      -------------------
         1   -2   -3    0
```

商式 x² - 2x - 3 = (x - 3)(x + 1)。

所以 (x - 2)(x - 3)(x + 1) = 0。

解得：x = 2, x = 3, x = -1

---

**例题 2**：解 x³ - 5x² + 8x - 4 = 0。

**解**：

试 x = 1：f(1) = 1 - 5 + 8 - 4 = 0。

综合除法：
```
    1 |  1   -5    8   -4
      |       1   -4    4
      -------------------
         1   -4    4    0
```

商式 x² - 4x + 4 = (x - 2)²。

所以 (x - 1)(x - 2)² = 0。

解得：x = 1 或 x = 2（二重根）

---

**例题 3**：已知 x = 2 是 2x³ - 3x² - 18x + k = 0 的一个根，求 k 并解此方程。

**解**：

代入 x = 2：16 - 12 - 36 + k = -32 + k = 0 ⇒ k = 32。

方程为 2x³ - 3x² - 18x + 32 = 0。已知 (x - 2) 是因式。

综合除法：
```
    2 |  2   -3   -18   32
      |       4     2   -32
      ----------------------
         2    1   -16    0
```

商式 2x² + x - 16。用求根公式：

x = (-1 ± √(1 + 128)) / 4 = (-1 ± √129) / 4

所以解为：x = 2, x = (-1 + √129)/4, x = (-1 - √129)/4

---

**例题 4**：解 x³ - 2x² - 5x + 6 = 0。

**解**：

试 x = 1：f(1) = 1 - 2 - 5 + 6 = 0。

综合除法：
```
    1 |  1   -2   -5    6
      |       1   -1   -6
      -------------------
         1   -1   -6    0
```

商式 x² - x - 6 = (x - 3)(x + 2)。

所以 (x - 1)(x - 3)(x + 2) = 0。

解得：x = 1, x = 3, x = -2

---

**例题 5**：解 2x³ - x² - 13x - 6 = 0。

**解**：

试 x = -1：f(-1) = -2 - 1 + 13 - 6 = 4 ≠ 0。
试 x = -2：f(-2) = -16 - 4 + 26 - 6 = 0。

综合除法：
```
    -2 |  2   -1   -13   -6
       |     -4    10    6
       ---------------------
          2   -5    -3    0
```

商式 2x² - 5x - 3 = (2x + 1)(x - 3)。

所以 (x + 2)(2x + 1)(x - 3) = 0。

解得：x = -2, x = -1/2, x = 3

---

**例题 6**：已知 x = 3 是 x³ + 4x² - 11x + k = 0 的一个根，求 k 并解此方程。

**解**：

代入 x = 3：27 + 36 - 33 + k = 30 + k = 0 ⇒ k = -30。

方程为 x³ + 4x² - 11x - 30 = 0。已知 (x - 3) 是因式。

综合除法：
```
    3 |  1    4   -11   -30
      |       3    21    30
      ---------------------
         1    7    10     0
```

商式 x² + 7x + 10 = (x + 2)(x + 5)。

所以 (x - 3)(x + 2)(x + 5) = 0。

解得：x = 3, x = -2, x = -5

---

## 3.2 判别式 Δ

### 3.2.1 判别式的定义与三种情况

对于一元二次方程 ax² + bx + c = 0（a ≠ 0），求根公式为：

x = (-b ± √(b² - 4ac)) / (2a)

根号内的表达式 b² - 4ac 决定了根的性质。定义判别式：

Δ = b² - 4ac

| Δ 的值 | 根的情况 |
|--------|---------|
| Δ > 0 | 两个不同的实根 |
| Δ = 0 | 一个重根 |
| Δ < 0 | 无实数根 |

---

**例题 1**：判断下列方程的根的情况：
(a) 2x² - 3x + 1 = 0
(b) 4x² - 4x + 1 = 0
(c) 3x² + 2x + 5 = 0

**解**：

(a) Δ = (-3)² - 4(2)(1) = 9 - 8 = 1 > 0，两个不等实根。

(b) Δ = (-4)² - 4(4)(1) = 16 - 16 = 0，重根。

(c) Δ = 2² - 4(3)(5) = 4 - 60 = -56 < 0，无实根。

---

**例题 2**：方程 x² + kx + 4 = 0 有重根，求 k。

**解**：

Δ = k² - 16 = 0 ⇒ k = ±4。

---

**例题 3**：方程 2x² - 3x + k = 0 有两个不等实根，求 k 的范围。

**解**：

Δ = 9 - 8k > 0 ⇒ k < 9/8。

---

**例题 4**：方程 x² - 2x + (k - 3) = 0 无实根，求 k 的范围。

**解**：

Δ = (-2)² - 4(1)(k - 3) = 4 - 4k + 12 = 16 - 4k < 0 ⇒ 4k > 16 ⇒ k > 4。

---

**例题 5**：方程 kx² + 3x + 2 = 0 有重根，求 k 的值。

**解**：

注意 k 是二次项系数，k ≠ 0。

Δ = 9 - 8k = 0 ⇒ k = 9/8。

---

**例题 6**：方程 3x² - 4x + k = 0 有两个不等实根，求 k 的范围。

**解**：

Δ = 16 - 12k > 0 ⇒ k < 4/3。

---

### 3.2.2 直线与曲线的位置关系

将直线 y = mx + c 代入曲线消去 y，得到关于 x 的二次方程：

| Δ 的值 | 交点个数 | 位置关系 |
|--------|---------|---------|
| Δ > 0 | 2 个 | 相交于两点 |
| Δ = 0 | 1 个 | 相切 |
| Δ < 0 | 0 个 | 不相交 |

---

**例题 1**：判断 y = 2x + 1 与 y = x² - 3x + 4 的位置关系。

代入得 x² - 5x + 3 = 0，Δ = 25 - 12 = 13 > 0，相交于两点。

---

**例题 2**：求 k 使 y = 3x + k 与 y = x² - x + 2 相切。

代入得 x² - 4x + (2 - k) = 0，Δ = 16 - 4(2 - k) = 8 + 4k = 0 ⇒ k = -2。

---

**例题 3**：求 c 使 y = x + c 与 y = 2x² - 3x + 1 不相交。

代入得 2x² - 4x + (1 - c) = 0，Δ = 16 - 8(1 - c) = 8 + 8c < 0 ⇒ c < -1。

---

**例题 4**：求 k 使直线 y = 2x + k 与曲线 y = x² - 2x + 3 相交于两点。

代入得 x² - 4x + (3 - k) = 0，Δ = 16 - 4(3 - k) = 4 + 4k > 0 ⇒ k > -1。

---

**例题 5**：直线 y = mx + 1 与曲线 y = x² - 3x + 5 相切，求 m。

代入得 x² - (m + 3)x + 4 = 0。

Δ = (m + 3)² - 16 = 0 ⇒ (m + 3)² = 16 ⇒ m + 3 = ±4 ⇒ m = 1 或 m = -7。

---

**例题 6**：求 c 使直线 y = 5x + c 与曲线 y = x² + x + 2 相切。

代入得 x² + x + 2 = 5x + c ⇒ x² - 4x + (2 - c) = 0。

Δ = 16 - 4(2 - c) = 8 + 4c = 0 ⇒ c = -2。

---

## 3.3 解二次方程

解二次方程 ax² + bx + c = 0 有三种核心方法：

| 方法 | 适用场景 | 优点 | 缺点 |
|------|---------|------|------|
| 因式分解法 | 表达式容易分解 | 最快，答案精确 | 并非所有二次式都可分解 |
| 公式法 | 任何情况 | 万能，按部就班 | 计算稍繁，可能含根号 |
| 配方法 | 需要顶点形式时 | 同时得到极值信息 | 步骤稍多 |

### 3.3.1 因式分解法

**核心原理**：若 A × B = 0，则 A = 0 或 B = 0。

**对于 x² + bx + c = 0（首项系数为 1）**：

找 p, q 满足 p + q = b 且 pq = c，则 x² + bx + c = (x + p)(x + q)。

**对于 ax² + bx + c = 0（首项系数不为 1）**：

找 p, q 满足 pq = ac 且 p + q = b，拆分中间项后分组提取公因式。

---

**例题 1**：解 x² - 5x + 6 = 0。

找 p+q=-5，pq=6：(-2)+(-3)=-5，(-2)×(-3)=6。

(x-2)(x-3)=0 ⇒ x=2 或 x=3。

---

**例题 2**：解 2x² - 5x - 3 = 0。

ac = 2×(-3) = -6，找 p+q=-5，pq=-6：(-6)+1=-5，(-6)×1=-6。

拆分：2x²-6x+x-3 = 2x(x-3)+1(x-3) = (2x+1)(x-3)。

x=-1/2 或 x=3。

---

**例题 3**：解 3x² + 2 = 7x。

移项：3x² - 7x + 2 = 0。ac=6，(-6)+(-1)=-7，(-6)×(-1)=6。

3x²-6x-x+2 = 3x(x-2)-1(x-2) = (3x-1)(x-2)。

x=1/3 或 x=2。

---

**例题 4**：解 x² + x - 12 = 0。

找 p+q=1，pq=-12：4+(-3)=1，4×(-3)=-12。

(x+4)(x-3)=0 ⇒ x=-4 或 x=3。

---

**例题 5**：解 6x² - 5x - 6 = 0。

ac = 6×(-6) = -36，找 p+q=-5，pq=-36：(-9)+4=-5，(-9)×4=-36。

6x²-9x+4x-6 = 3x(2x-3)+2(2x-3) = (3x+2)(2x-3)。

x=-2/3 或 x=3/2。

---

**例题 6**：解 4x² + 4x = 3。

移项：4x² + 4x - 3 = 0。ac = 4×(-3) = -12，找 p+q=4，pq=-12：6+(-2)=4，6×(-2)=-12。

4x²+6x-2x-3 = 2x(2x+3)-1(2x+3) = (2x-1)(2x+3)。

x=1/2 或 x=-3/2。

---

### 3.3.2 公式法

求根公式：

x = (-b ± √(b² - 4ac)) / (2a)

---

**例题 1**：解 2x² - 3x - 4 = 0。

a=2, b=-3, c=-4。

x = (3 ± √(9 + 32)) / 4 = (3 ± √41) / 4

---

**例题 2**：解 x² - 2x - 3 = 0。

x = (2 ± √(4 + 12)) / 2 = (2 ± 4) / 2

x=3 或 x=-1。

---

**例题 3**：解 4x² - 12x + 9 = 0。

x = (12 ± √(144 - 144)) / 8 = 12/8 = 3/2（重根）

---

**例题 4**：解 x² - 3x - 5 = 0。

x = (3 ± √(9 + 20)) / 2 = (3 ± √29) / 2

---

**例题 5**：解 3x² + 2x - 4 = 0。

x = (-2 ± √(4 + 48)) / 6 = (-2 ± √52) / 6 = (-2 ± 2√13) / 6 = (-1 ± √13) / 3

---

**例题 6**：解 5x² + 2x - 1 = 0。

x = (-2 ± √(4 + 20)) / 10 = (-2 ± √24) / 10 = (-2 ± 2√6) / 10 = (-1 ± √6) / 5

---

### 3.3.3 配方法

配方法将 ax² + bx + c 写成 a(x + p)² + q 的形式。

**最终形式**：

ax² + bx + c = a(x + b/(2a))² + (4ac - b²)/(4a)

---

**例题 1**：用配方法解 x² - 6x + 5 = 0。

x² - 6x + 5 = 0
x² - 6x = -5
x² - 6x + 9 = -5 + 9  （加 (6/2)² = 9）
(x - 3)² = 4
x - 3 = ±2
x = 5 或 x = 1

---

**例题 2**：用配方法解 2x² - 8x + 3 = 0。

2x² - 8x + 3 = 0
2(x² - 4x) = -3
2[(x² - 4x + 4) - 4] = -3
2(x - 2)² - 8 = -3
2(x - 2)² = 5
(x - 2)² = 5/2
x = 2 ± √10/2

---

**例题 3**：将 f(x) = 3x² + 12x + 5 写成 a(x + p)² + q 的形式。

f(x) = 3x² + 12x + 5
= 3(x² + 4x) + 5
= 3[(x + 2)² - 4] + 5
= 3(x + 2)² - 12 + 5
= 3(x + 2)² - 7

顶点为 (-2, -7)，a=3>0 开口向上。

---

**例题 4**：用配方法解 x² - 8x + 13 = 0。

x² - 8x + 13 = 0
x² - 8x = -13
x² - 8x + 16 = -13 + 16
(x - 4)² = 3
x - 4 = ±√3
x = 4 ± √3

---

**例题 5**：用配方法解 2x² - 8x + 5 = 0。

2x² - 8x + 5 = 0
2(x² - 4x) = -5
2[(x - 2)² - 4] = -5
2(x - 2)² - 8 = -5
2(x - 2)² = 3
(x - 2)² = 3/2
x = 2 ± √6/2

---

**例题 6**：将 f(x) = -2x² + 8x - 5 写成 a(x + p)² + q 的形式。

f(x) = -2x² + 8x - 5
= -2(x² - 4x) - 5
= -2[(x - 2)² - 4] - 5
= -2(x - 2)² + 8 - 5
= -2(x - 2)² + 3

顶点为 (2, 3)，a=-2<0 开口向下。

---

## 3.4 配方法与最值

### 3.4.1 用配方法求最值

f(x) = a(x + p)² + q 中，由于 (x + p)² ≥ 0：
- a > 0：f(x) ≥ q，最小值 q 在 x = -p 处。
- a < 0：f(x) ≤ q，最大值 q 在 x = -p 处。

---

**例题 1**：求 f(x) = x² - 4x + 7 的最小值。

f(x) = (x - 2)² + 3。a=1>0，当 x=2 时取最小值 3。

---

**例题 2**：求 f(x) = -2x² + 12x - 10 的最大值。

f(x) = -2(x - 3)² + 8。a=-2<0，当 x=3 时取最大值 8。

---

**例题 3**：求 f(x) = x² - 2x - 3 在 [0, 4] 上的最值。

f(x) = (x - 1)² - 4。顶点 (1, -4) 在区间内，最小值 -4。
f(0) = -3，f(4) = 5。最大值 5。

---

**例题 4**：求 f(x) = x² + 6x + 11 的最小值。

f(x) = (x + 3)² + 2。最小值 2 在 x = -3 处。

---

**例题 5**：求 f(x) = -x² + 4x + 1 的最大值。

f(x) = -(x - 2)² + 5。最大值 5 在 x = 2 处。

---

**例题 6**：求 f(x) = x² - 4x + 5 在 [1, 5] 上的值域。

f(x) = (x - 2)² + 1，顶点 (2, 1) 在区间内。f(1)=2，f(5)=10。值域 [1, 10]。

---

### 3.4.2 画草图

四个关键要素：开口方向、顶点、x 轴交点、y 轴交点。

---

**例题 1**：f(x) = x² - 2x - 3。
开口向上，顶点 (1, -4)，x 轴交点 (-1,0) 和 (3,0)，y 轴交点 (0,-3)。

**例题 2**：f(x) = -x² + 4x。
开口向下，顶点 (2, 4)，x 轴交点 (0,0) 和 (4,0)。

**例题 3**：f(x) = x² + 2x + 3。
开口向上，顶点 (-1, 2)，Δ < 0 无 x 轴交点，y 轴交点 (0,3)。完全在 x 轴上方。

**例题 4**：f(x) = -2x² + 4x + 6。
开口向下，顶点 (1, 8)，x 轴交点 (-1,0) 和 (3,0)，y 轴交点 (0,6)。

---

### 3.4.3 求值域

步骤：配方 → 判断顶点是否在定义域内 → 算端点 → 比较。

---

**例题 1**：f(x) = 2x² - 8x + 3 在 R 上。
f(x)=2(x-2)²-5，值域 [-5, ∞)。

**例题 2**：f(x) = x² - 2x + 3 在 [-1,3] 上。
f(x)=(x-1)²+2，顶点在区间内，f(1)=2，f(-1)=6，f(3)=6，值域 [2,6]。

**例题 3**：f(x) = x² - 4x + 5 在 [3,5] 上。
f(x)=(x-2)²+1，顶点 x=2 不在区间内，函数单调递增，f(3)=2，f(5)=10，值域 [2,10]。

**例题 4**：f(x) = -x² + 2x + 3 在 [-1,4] 上。
f(x)=-(x-1)²+4，顶点 (1,4) 在区间内。f(-1)=0，f(4)=-5。值域 [-5,4]。

---

## 3.5 二次不等式

### 3.5.1 代数法（符号表法）

**完整步骤**：

**第 1 步**：整理为 ax² + bx + c > 0（或 <, ≥, ≤）。若 a < 0，两边乘 -1 并反转不等号。

**第 2 步**：解对应方程 ax² + bx + c = 0，得根 x₁ ≤ x₂。

**第 3 步**：写出解集。

**符号法则**（a > 0 时）：

- 大于取两边：ax² + bx + c > 0 ⇒ x < x₁ 或 x > x₂
- 小于取中间：ax² + bx + c < 0 ⇒ x₁ < x < x₂

---

**例题 1**：解 x² - 5x + 6 > 0。

(x - 2)(x - 3) > 0。根为 x = 2 和 x = 3。a = 1 > 0。

"大于取两边"：x < 2 或 x > 3。

---

**例题 2**：解 2x² - 5x - 3 ≤ 0。

(2x + 1)(x - 3) ≤ 0。根为 x = -1/2 和 x = 3。a = 2 > 0。

"小于取中间"（含端点）：-1/2 ≤ x ≤ 3。

---

**例题 3**：解 x² + 2x + 3 > 0。

Δ = 4 - 12 = -8 < 0，a = 1 > 0。恒正。解集为 R。

---

**例题 4**：解 -x² + 3x + 4 > 0。

a = -1 < 0，两边乘 -1：x² - 3x - 4 < 0。

(x - 4)(x + 1) < 0。根为 x = -1 和 x = 4。

"小于取中间"：-1 < x < 4。

---

**例题 5**：解 x² - 4x + 4 ≥ 0。

(x - 2)² ≥ 0。平方数恒 ≥ 0，解集为 R。

---

**例题 6**：解 x² - 4x + 4 < 0。

(x - 2)² < 0。平方数不可能小于零，无解。

---

### 3.5.2 图像法

画出 y = ax² + bx + c 的草图，查看抛物线在 x 轴上方的部分（> 0）或下方的部分（< 0）。

---

**例题 1**：用图像法解 x² - x - 2 < 0。

y = x² - x - 2，a=1>0，开口向上。x 轴交点 (-1,0) 和 (2,0)。

图像在 -1 < x < 2 之间位于 x 轴下方。解集：-1 < x < 2。

---

**例题 2**：已知 x² - 2kx + 4 > 0 对所有实数 x 恒成立，求 k。

a=1>0，需 Δ < 0：4k² - 16 < 0 ⇒ k² < 4 ⇒ -2 < k < 2。

---

**例题 3**：解 x² - 4 ≥ 3x。

移项：x² - 3x - 4 ≥ 0。(x - 4)(x + 1) ≥ 0。

"大于取两边"（含端点）：x ≤ -1 或 x ≥ 4。

---

**例题 4**：解 x² - 3x - 10 > 0。

(x - 5)(x + 2) > 0。x < -2 或 x > 5。

---

**例题 5**：解 2x² + 5x - 3 ≤ 0。

(2x - 1)(x + 3) ≤ 0。-3 ≤ x ≤ 1/2。

---

**例题 6**：解 x² - 6x + 9 ≥ 0。

(x - 3)² ≥ 0，解集 R。

---

### 3.5.3 含参数的不等式问题

**例题 1**：求 k 使 x² + kx + 9 ≥ 0 对一切 x 恒成立。

a=1>0，需 Δ ≤ 0：k² - 36 ≤ 0 ⇒ -6 ≤ k ≤ 6。

---

**例题 2**：求 k 使 kx² + 2x + 3 > 0 对一切 x 恒成立。

若 k = 0：2x+3>0 不是恒成立，排除。
若 k ≠ 0：需 k > 0 且 Δ = 4 - 12k < 0 ⇒ k > 1/3。

所以 k > 1/3。

---

**例题 3**：求 k 使 x² - 2kx + 4 > 0 对所有实数 x 恒成立。

Δ = 4k² - 16 < 0 ⇒ k² < 4 ⇒ -2 < k < 2。

---

**例题 4**：求 k 使 (k-1)x² + 2x + 1 > 0 对一切 x 恒成立。

若 k-1 = 0，即 k=1：2x+1 > 0，不是恒成立。
若 k-1 ≠ 0：需 k-1 > 0 且 Δ = 4 - 4(k-1) = 8 - 4k < 0 ⇒ k > 2。

所以 k > 2。

---

## 3.6 三次多项式的图像与不等式

### 3.6.1 三个线性因式乘积的图像

f(x) = a(x - p)(x - q)(x - r) 的图像特征：

**（1）x 轴截距**：x = p, q, r（三个零点）。

**（2）y 轴截距**：f(0) = a(-p)(-q)(-r) = -a * pqr。

**（3）端点行为**——取决于最高次项 ax³：

| a 的符号 | x → -∞ | x → +∞ |
|---------|--------|--------|
| a > 0 | f(x) → -∞（左下） | f(x) → +∞（右上） |
| a < 0 | f(x) → +∞（左上） | f(x) → -∞（右下） |

**（4）零点处的行为**：
- 单根（因式次数为 1）：图像穿过 x 轴。
- 二重根（因式次数为 2）：图像触及并反弹。

---

**例题 1**：画出 f(x) = (x + 1)(x - 1)(x - 3) 的草图。

x 截距：x = -1, 1, 3（三个单根，全部穿过）。
y 截距：f(0) = (1)(-1)(-3) = 3，过 (0, 3)。
a = 1 > 0：左端向下，右端向上。

---

**例题 2**：画出 f(x) = -(x + 2)(x - 1)(x - 4) 的草图。

x 截距：x = -2, 1, 4。
y 截距：f(0) = -(2)(-1)(-4) = -8，过 (0, -8)。
a = -1 < 0：左端向上，右端向下。

---

**例题 3**：画出 f(x) = (x - 1)²(x + 2) 的草图。

x 截距：x = -2（单根，穿过），x = 1（二重根，触及反弹）。
y 截距：f(0) = (1)²(2) = 2，过 (0, 2)。
a = 1 > 0：左端向下，右端向上。

---

**例题 4**：画出 f(x) = -(x + 1)(x - 2)² 的草图。

x 截距：x = -1（单根，穿过），x = 2（二重根，触及反弹）。
y 截距：f(0) = -(1)(4) = -4，过 (0, -4)。
a = -1 < 0：左端向上，右端向下。

---

**例题 5**：画出 f(x) = (x + 3)(x + 1)(x - 2) 的草图。

x 截距：x = -3, -1, 2（三个单根）。
y 截距：f(0) = (3)(1)(-2) = -6，过 (0, -6)。
a = 1 > 0：左端向下，右端向上。

---

**例题 6**：画出 f(x) = -2(x + 1)(x - 1)(x - 3) 的草图。

x 截距：x = -1, 1, 3。
y 截距：f(0) = -2(1)(-1)(-3) = -6，过 (0, -6)。
a = -2 < 0：左端向上，右端向下。

---

### 3.6.2 绝对值图像

核心规则：

y = |f(x)|

- 保留 f(x) ≥ 0 的部分（x 轴上方的部分不变）
- 翻折 f(x) < 0 的部分（将 x 轴下方的部分沿 x 轴向上对称翻转）

---

**例题 1**：画出 y = |(x + 1)(x - 1)(x - 3)| 的草图。

先分析 f(x) = (x + 1)(x - 1)(x - 3) 的符号：

| 区间 | x<-1 | -1<x<1 | 1<x<3 | x>3 |
|------|------|--------|-------|-----|
| f(x) | - | + | - | + |

将负的部分（x < -1 和 1 < x < 3）沿 x 轴向上翻折。

---

**例题 2**：画出 y = |(x - 1)(x - 2)(x - 4)| 的草图。

分析 f(x) = (x - 1)(x - 2)(x - 4) 的符号：

| 区间 | x<1 | 1<x<2 | 2<x<4 | x>4 |
|------|-----|-------|-------|-----|
| f(x) | - | + | - | + |

将负的区域（x<1 和 2<x<4）沿 x 轴向上翻折。

---

**例题 3**：求 |(x + 1)(x - 1)(x - 2)| = 2 的实根个数。

符号分析：x<-1（-），-1<x<1（+），1<x<2（-），x>2（+）。

做绝对值变换后，|f(0)| = |(1)(-1)(-2)| = 2，(0,2) 是一个交点。

水平线 y=2 与图像相交：
- x<-1：1 个交点
- -1<x<1：2 个交点
- 1<x<2：2 个交点
- x>2：1 个交点

总共 5 个交点，即方程有 5 个实根。

---

**例题 4**：画出 y = |(x + 2)(x - 1)²| 的草图。

f(x) = (x + 2)(x - 1)²。

符号：x<-2（-），-2<x<1（+），x>1（+）。

将 x<-2 的部分沿 x 轴向上翻折。在 x=-2 处有尖点；在 x=1 处是平滑触及。

---

### 3.6.3 三次不等式的图像解法

对于 f(x) ≥ d（>，≤，< 同理），其中 f(x) = a(x-p)(x-q)(x-r)：

1. 画出 y = f(x) 的草图。
2. 画水平线 y = d。
3. 找出交点横坐标（解 f(x) = d）。
4. 读取满足不等式的 x 区间。

---

**例题 1**：f(x) = (x+1)(x-1)(x-3)，解 f(x) ≤ 0。

符号表：

| 区间 | x<-1 | -1<x<1 | 1<x<3 | x>3 |
|------|------|--------|-------|-----|
| f(x) | - | + | - | + |

f(x) ≤ 0 对应负或零的区间（含端点）：

x ≤ -1 或 1 ≤ x ≤ 3

---

**例题 2**：f(x) = -(x+1)(x-2)(x-5)，解 f(x) > 0。

先考虑 g(x) = (x+1)(x-2)(x-5)，a_g = 1 > 0。

g(x) 符号：x<-1（-），-1<x<2（+），2<x<5（-），x>5（+）。

f(x) = -g(x)，符号与 g(x) 相反：

| 区间 | x<-1 | -1<x<2 | 2<x<5 | x>5 |
|------|------|--------|-------|-----|
| f(x) | + | - | + | - |

f(x) > 0 对应正区间（不含端点）：

x < -1 或 2 < x < 5

---

**例题 3**：f(x) = (x+2)(x-1)(x-4)，解 f(x) ≥ 8。

展开：f(x) = x³ - 3x² - 6x + 8。

解 f(x) = 8：
x³ - 3x² - 6x + 8 = 8 ⇒ x³ - 3x² - 6x = 0 ⇒ x(x² - 3x - 6) = 0

x = 0 或 x = (3 ± √33)/2。(3 - √33)/2 ≈ -1.372，(3 + √33)/2 ≈ 4.372。

a = 1 > 0，左端向下，右端向上。f(x) ≥ 8 的解集为：

(3 - √33)/2 ≤ x ≤ 0 或 x ≥ (3 + √33)/2

---

## 3.7 用微分求二次函数的极值

### 3.7.1 微分法的引入

对于二次函数 f(x) = ax² + bx + c：

**第 1 步：求导**。

由幂法则 (xⁿ)' = nxⁿ⁻¹：

f'(x) = d/dx(ax² + bx + c) = 2ax + b

**第 2 步：令导数为零，找到驻点**。

2ax + b = 0 ⇒ x = -b/(2a)

**第 3 步：代入原函数求极值**。

f(-b/(2a)) = a(-b/(2a))² + b(-b/(2a)) + c
= a * (b²/(4a²)) - b²/(2a) + c
= -b²/(4a) + c = (4ac - b²)/(4a)

**第 4 步：用二阶导数判断极值类型**。

f''(x) = d/dx(2ax + b) = 2a

- f''(x) = 2a > 0（即 a > 0）：最小值
- f''(x) = 2a < 0（即 a < 0）：最大值

---

**例题 1**：用微分法求 f(x) = 2x² - 8x + 5 的极值。

f'(x) = 4x - 8。令 f'(x) = 0：4x = 8 ⇒ x = 2。

f''(x) = 4 > 0，最小值。

f(2) = 8 - 16 + 5 = -3。

---

**例题 2**：用微分法求 f(x) = -3x² + 12x - 7 的极值。

f'(x) = -6x + 12。令 f'(x) = 0：x = 2。

f''(x) = -6 < 0，最大值。

f(2) = -12 + 24 - 7 = 5。

---

**例题 3**：已知 f(x) = x² + kx + 4 在 x = 3 处取极值，求 k 并判断。

f'(x) = 2x + k。f'(3) = 6 + k = 0 ⇒ k = -6。

f''(x) = 2 > 0，极小值。

f(3) = 9 - 18 + 4 = -5。

---

**例题 4**：用微分法求 f(x) = 5x² - 20x + 3 的极值。

f'(x) = 10x - 20 = 0 ⇒ x = 2。f''(x) = 10 > 0，最小值 f(2) = 20 - 40 + 3 = -17。

---

**例题 5**：用微分法求 f(x) = -4x² + 24x - 31 的极值。

f'(x) = -8x + 24 = 0 ⇒ x = 3。f''(x) = -8 < 0，最大值 f(3) = -36 + 72 - 31 = 5。

---

**例题 6**：已知 f(x) = 3x² + 2mx + 5 在 x = -2 处取极值，求 m 和极值。

f'(x) = 6x + 2m。f'(-2) = -12 + 2m = 0 ⇒ m = 6。

f''(x) = 6 > 0，极小值。f(-2) = 12 - 24 + 5 = -7。

---

**例题 7**：用微分法证明 f(x) = x² + 4x + 7 的最小值为 3。

f'(x) = 2x + 4 = 0 ⇒ x = -2。f''(x) = 2 > 0，最小值 f(-2) = 4 - 8 + 7 = 3。证毕。

---

**例题 8**：某矩形花园的周长为 40 米，求面积的最大值。

设长为 x 米，则宽为 20 - x 米。

面积 A(x) = x(20 - x) = 20x - x² = -x² + 20x。

A'(x) = -2x + 20 = 0 ⇒ x = 10。A''(x) = -2 < 0，最大值。

最大面积 A(10) = 100 平方米。

---

**例题 9**：求 f(x) = 2x² - 12x + 5 的极值，并用配方法验证。

微分法：f'(x) = 4x - 12 = 0 ⇒ x = 3。f''(x) = 4 > 0，最小值 f(3) = 18 - 36 + 5 = -13。

配方法验证：f(x) = 2(x-3)² - 13，最小值 -13。✓

---

**例题 10**：已知 f(x) = ax² + 6x + 2 在 x = -1 处取极值，求 a 和极值。

f'(x) = 2ax + 6。f'(-1) = -2a + 6 = 0 ⇒ a = 3。

f''(x) = 2a = 6 > 0，极小值。f(-1) = 3 - 6 + 2 = -1。

---

**例题 11**：用微分法求 f(x) = 4x² - 16x + 7 的极值。

f'(x) = 8x - 16 = 0 ⇒ x = 2。f''(x) = 8 > 0，最小值 f(2) = 16 - 32 + 7 = -9。

---

**例题 12**：用微分法求 f(x) = -5x² + 30x - 41 的极值。

f'(x) = -10x + 30 = 0 ⇒ x = 3。f''(x) = -10 < 0，最大值 f(3) = -45 + 90 - 41 = 4。

---

## 本章总结

| 知识点 | 核心内容 |
|--------|---------|
| 余数定理 | f(x) ÷ (x-a) 余数为 f(a)；f(x) ÷ (ax+b) 余数为 f(-b/a) |
| 因式定理 | f(a)=0 ⇔ (x-a) 是因式 |
| 三次式分解流程 | 试根 → 综合除法 → 分解二次式 |
| 判别式 Δ | Δ = b²-4ac；Δ>0 两不等根，Δ=0 重根，Δ<0 无实根 |
| 直线与曲线 | 代入消 y → 二次方程 → Δ 判相交/相切/不相交 |
| 解二次方程三法 | 因式分解（最快）、公式法（万能）、配方法（顶点形式） |
| 最值 | a(x+p)²+q，a>0 最小 q，a<0 最大 q |
| 二次不等式 | a>0 时"大于取两边，小于取中间" |
| 三次图像 | a>0 左下到右上，a<0 左上到右下；单根穿过，二重根反弹 |
| 绝对值图像 | 负的部分向上翻折到正半轴，零点处有尖点 |
| 三次不等式 | 画图 → 画水平线 y=d → 读区间 |
| 微分求极值 | f'(x)=0 得驻点，f''(x) 判最大/最小 |

---
---
根据您的要求，我已将第4章“函数（线性、三次、指数、对数）”的内容重新编译，只使用Unicode字符和必要的LaTeX（仅用于积分、求导、函数专用符号），同时避免使用 `\binom`、`\frac` 以及 `\mathbf{i}`+`pmatrix` 等格式。所有向量改用 `(1,0)` 等表示，分数用斜线，组合数用 `C(n,r)` 或类似记号。以下为完整输出。

---

# 第 4 章：函数（线性、三次、指数、对数）

## 考纲对照

本章覆盖 IGCSE 0606 附加数学（2028–2030）考纲中 **Topic 1: Functions** 与 **Topic 6: Logarithmic and exponential functions** 的全部内容。

| 考纲条目 | 对应本节 |
|---------|---------|
| **1.1** 理解函数（含垂直检验线）、定义域、值域、单射（水平检验线）、多对一、反函数、复合函数；解释一个关系式是否为函数 | §4.1, §4.4 |
| **1.2** 求函数的定义域和值域（含反函数和复合函数）；理解定义域限制使反函数/复合函数存在；理解 Domain(gf) ⊆ Domain(f)，Range(gf) ⊆ Range(g) | §4.1, §4.4 |
| **1.3** 识别并使用函数记号：f(x)、f:x↦、f⁻¹(x)、fg(x)、f²(x)（f² 不用于三角函数） | §4.1 |
| **1.4** 理解 y=f(x) 与 y=|f(x)| 的关系，其中 f(x) 可以是线性、二次、三次或三角（a sin(bx)+c、a cos(bx)+c、a tan(bx)+c 形式） | §4.5 |
| **1.5** 用文字解释给定函数为什么没有反函数 | §4.4 |
| **1.6** 求单射函数的反函数（如 f(x)=e^(2x) 的反函数为 (1/2)ln x） | §4.4 |
| **1.7** 构造并使用复合函数，理解 fg 一般不等于 gf | §4.4 |
| **1.8** 用草图表示函数与其反函数关于 y=x 对称的关系 | §4.4 |
| **6.1** 了解并使用对数与指数函数的性质与图形（含 ln x 和 e^x、渐近线） | §4.3 |
| **6.2** 了解并使用对数运算法则（含换底公式） | §4.3 |
| **6.3** 解 a^x = b 形式的方程 | §4.3 |

> 学习路径：§4.1（概念基础）→ §4.2（线性与三次）→ §4.3（指数与对数）→ §4.4（反函数与复合）→ §4.5（绝对值图形）→ 练习题

---

## 4.1 函数的基础概念

### 4.1.1 什么是函数？

函数是一种特殊的对应关系：它将**定义域**中的每一个输入值 x，对应到**恰好一个**输出值 y = f(x)。我们称 y 是 x 的**像**。

f: D → R,  x ↦ f(x)

其中 D 是定义域，**值域**是所有可能的输出值 f(x) 的集合。

**函数必须满足的条件**：对于定义域中的每个 x，必须有且仅有一个 y 与之对应。这是函数的**垂直检验线法则**——任何竖直线与函数图形最多相交一次。

**如何解释一个关系式是否为函数**（考纲 1.1）：

对于定义域中的每一个 x 值，关系式只给出唯一的一个 y 值。

- y = x² **是**函数：每个 x 对应唯一一个 y。
- x = y² **不是**函数：例如 x=4 时，y 可以是 2 或 -2，一个 x 对应两个 y。
- y = ±√x **不是**函数：每个正 x 对应两个 y 值。

### 4.1.2 单射（一对一）与多对一

- **单射（one–one function / injective）**：定义域中不同的 x 对应不同的 y。即：若 x₁ ≠ x₂，则 f(x₁) ≠ f(x₂)。检验方法——**水平检验线法则**：任何水平线与图形最多相交一次。

- **多对一（many–one function）**：不同的 x 可以对应同一个 y。例如 f(x) = x²，f(2) = f(-2) = 4。水平检验线 y=4 与图形相交于两点。

> ⚠️ **只有单射函数才有反函数**。这是因为反函数需要将每个输出值唯一地映射回输入值——如果原函数是多对一的，那么反函数将是一对多，不满足函数的定义。

### 4.1.3 函数记号

IGCSE 0606 中使用的函数记号包括：

- **f(x)**：最常见的记号，如 f(x) = 2e^x
- **f: x ↦**：映射记号，如 f: x ↦ lg x，表示“f 将 x 映射到 lg x”
- **f⁻¹(x)**：反函数记号
- **fg(x)**：复合函数记号，fg(x) = f(g(x))
- **f²(x)**：表示 f(f(x))，即 f 复合自身

> ⚠️ **重要**：记号 f²(x) **不适用于三角函数**。例如 sin²x 表示 (sin x)²，而不是 sin(sin x)。

### 4.1.4 定义域与值域的求法

求定义域时需要考虑的限制因素：

1. **分母不为零**：f(x) = 1 / g(x) ⇒ g(x) ≠ 0
2. **偶次根号内非负**：f(x) = √g(x) ⇒ g(x) ≥ 0
3. **对数的真数为正**：f(x) = log_a(g(x)) ⇒ g(x) > 0

**值域的求法**：

**方法一——配方法**（适用于二次函数）：
将 f(x) = ax² + bx + c 写成 a(x-h)² + k 的形式。
- 若 a > 0，最小值为 k，值域为 [k, ∞)
- 若 a < 0，最大值为 k，值域为 (-∞, k]

**方法二——观察法**（适用于单调函数）：
如果函数在定义域上单调递增或递减，值域就是两端函数值的区间。

**方法三——反函数法**：
若函数有反函数，原函数的值域等于反函数的定义域。

---

### 例题 4.1（定义域与值域）

**例 1**（基础型——根号与分母）：求 f(x) = √(x-2) + 1/(x-3) 的定义域。

**解**：

**第一步**（根号条件）：x-2 ≥ 0 ⇒ x ≥ 2。

**第二步**（分母条件）：x-3 ≠ 0 ⇒ x ≠ 3。

**第三步**（取交集）：定义域为 [2, 3) ∪ (3, ∞)。

---

**例 2**（复合型——分离常数求值域）：函数 f(x) = (2x+1)/(x-1)，x ≠ 1。

（i）求值域；
（ii）判断 f 是否为单射。

**解**：

（i）**分离常数**：将分子改写成与分母相关的形式。

f(x) = (2x+1)/(x-1) = [2(x-1) + 3]/(x-1)

这一步的思路：分母是 x-1，我们希望分子中也出现 x-1 以便约分。将 2x 写成 2(x-1) + 2，再加上原分子中的 1，得到 2(x-1) + 3。

继续化简：

f(x) = 2(x-1)/(x-1) + 3/(x-1) = 2 + 3/(x-1)

因为 3/(x-1) ≠ 0 对一切 x ≠ 1 成立，所以 f(x) 永远取不到 2。

**值域为 R \ {2}**。

（ii）判断单射：设 f(a) = f(b)，则：

2 + 3/(a-1) = 2 + 3/(b-1)

两边减去 2：

3/(a-1) = 3/(b-1)

两边取倒数再乘以 3：

a-1 = b-1 ⇒ a = b

因此 f 是单射。从图形上看，y = 2 + 3/(x-1) 是反比例函数经过平移后的结果，每条水平线（除 y=2 外）恰好相交一次。

---

**例 3**（半圆型值域）：已知 f(x) = √(4 - x²)。

（i）求定义域和值域；
（ii）判断 f 是否有反函数。

**解**：

（i）**定义域**：4 - x² ≥ 0 ⇒ x² ≤ 4 ⇒ -2 ≤ x ≤ 2。定义域为 [-2, 2]。

**值域**：令 y = √(4 - x²)，则 y ≥ 0 且 y² = 4 - x²，即 x² + y² = 4（y ≥ 0）。

这是一个圆心在原点、半径为 2 的**上半圆**。y 的最小值出现在 x = ±2 时，y = 0；最大值出现在 x = 0 时，y = 2。因此值域为 [0, 2]。

（ii）f 不是单射，因为例如 f(-1) = f(1) = √3。水平检验线 y = √3 与上半圆相交于 (±1, √3) 两点。因此 f 没有反函数。

> 但如果将定义域限制为 x ∈ [0, 2]，则 f 变为单射，此时反函数为 f⁻¹(x) = √(4 - x²)（定义域 [0, 2]）。

---

**例 4**（对数与分式复合型定义域）：求 f(x) = ln(3x - 6) + 1/√(8 - 2x) 的定义域。

**解**：

**条件 1**（对数真数大于零）：3x - 6 > 0 ⇒ x > 2。

**条件 2**（分母根号内大于零——因为分母不能为零且根号在分母中）：8 - 2x > 0 ⇒ x < 4。

**取交集**：x > 2 且 x < 4，即 (2, 4)。

---

**例 5**（判断关系式是否为函数——考纲 1.1 要求）：判断下列关系式是否为函数，并解释原因。

（i）y = ±√x，x ≥ 0
（ii）y = x³ - 2x + 1
（iii）x² + y² = 25

**解**：

（i）**不是函数**。对于同一个 x（例如 x=4），关系式给出两个 y 值：y = 2 和 y = -2。这违反了函数**每个输入对应唯一输出**的定义。垂直检验线 x=4 与图形相交于两点。

（ii）**是函数**。对于每一个实数 x，x³ - 2x + 1 恰好计算出一个实数 y。垂直检验线在任何 x 处都只与图形相交一次。

（iii）**不是函数**。例如 x=0 时，y² = 25 ⇒ y = ±5，一个 x 对应两个 y。垂直检验线 x=0 与圆相交于 (0,5) 和 (0,-5) 两点。

---

## 4.2 线性函数与三次函数

### 4.2.1 线性函数 f(x) = mx + c

线性函数是最简单的函数类型。它的图形是一条直线。

**斜率 m 的几何意义**：x 每增加 1 个单位，y 增加 m 个单位。如果 m > 0，直线向右上方倾斜；m < 0，向右下方倾斜；m = 0，水平直线。

**截距 c**：直线与 y 轴的交点纵坐标，即 f(0) 的值。

**变化率特征**：线性函数的变化率是**常数**——无论在哪一点上，瞬时变化率都等于 m。这是线性函数区别于其他函数的最重要特性。

由两点 (x₁, y₁) 和 (x₂, y₂) 求斜率：

m = (y₂ - y₁) / (x₂ - x₁)

这个公式的推导思路：两点之间的垂直变化是 y₂ - y₁，水平变化是 x₂ - x₁，斜率就是“升程除以行程”。

**点斜式方程**：过点 (x₀, y₀) 且斜率为 m 的直线方程为：

y - y₀ = m(x - x₀)

### 4.2.2 三次函数 f(x) = ax³ + bx² + cx + d（a ≠ 0）

三次函数的图形呈 S 形（或反 S 形）。它的导数 f'(x) = 3ax² + 2bx + c 是一个二次函数，可能有两个零点（对应局部极值点），也可能只有一个或没有实数零点。

**三次函数的两种基本形态**：

1. **三个线性因式乘积形式**：f(x) = a(x - p)(x - q)(x - r)，与 x 轴交于 x = p, q, r。
2. **一个线性因式与一个二次因式的乘积**：f(x) = (x - p)(Ax² + Bx + C)，可能只有一个实根。

**端部行为（leading term test）**：
- 若 a > 0：当 x → -∞ 时 f(x) → -∞；当 x → ∞ 时 f(x) → ∞。
- 若 a < 0：当 x → -∞ 时 f(x) → ∞；当 x → ∞ 时 f(x) → -∞。

---

### 例题 4.2（线性与三次函数）

**例 1**（线性函数参数求解）：已知直线 L 经过点 A(2, 5) 和 B(4, 11)。

（i）求 L 的方程；
（ii）求 L 与 x 轴和 y 轴的交点。

**解**：

（i）**求斜率**：

m = (11 - 5) / (4 - 2) = 6/2 = 3

**写方程**：使用点斜式，取 A(2, 5) 作为已知点：

y - 5 = 3(x - 2)

化简：

y - 5 = 3x - 6 ⇒ y = 3x - 1

（ii）**y 截距**：令 x = 0，得 y = 3(0) - 1 = -1，即 (0, -1)。

**x 截距**：令 y = 0，得 0 = 3x - 1 ⇒ x = 1/3，即 (1/3, 0)。

---

**例 2**（三次函数图形与极值）：已知 f(x) = x³ - 3x² + 2。

（i）求 f'(x) 并解 f'(x) = 0；
（ii）判断驻点的类型；
（iii）求 f 与坐标轴的交点。

**解**：

（i）**求导**：

f'(x) = d/dx(x³) - d/dx(3x²) + d/dx(2) = 3x² - 6x

因式分解：f'(x) = 3x(x - 2)。

令 f'(x) = 0，得 3x(x-2) = 0，即 x = 0 或 x = 2。

（ii）用一阶导数符号检验每个驻点附近的单调性变化：

**在 x = 0 处**：
- 取 x = -1（左侧）：f'(-1) = 3(-1)(-3) = 9 > 0，递增
- 取 x = 1（右侧）：f'(1) = 3(1)(-1) = -3 < 0，递减
- 从左到右：递增 → 递减 → **局部最大值**。f(0) = 2。

**在 x = 2 处**：
- 取 x = 1（左侧）：f'(1) = -3 < 0，递减
- 取 x = 3（右侧）：f'(3) = 3(3)(1) = 9 > 0，递增
- 从左到右：递减 → 递增 → **局部最小值**。f(2) = 8 - 12 + 2 = -2。

（iii）**y 截距**：f(0) = 2，即 (0, 2)。

**x 截距**：解 x³ - 3x² + 2 = 0。

尝试有理根。检验 x = 1：f(1) = 1 - 3 + 2 = 0，所以 x-1 是因子。

用综合除法分解：

```
    1 |  1   -3    0    2
      |       1   -2   -2
      --------------------
         1   -2   -2    0
```

商为 x² - 2x - 2。用二次公式求根：

x = [2 ± √(4 - 4(1)(-2))] / (2(1)) = [2 ± √(4 + 8)] / 2 = (2 ± √12)/2 = (2 ± 2√3)/2 = 1 ± √3

三个 x 截距：x = 1，x = 1 + √3，x = 1 - √3。

---

**例 3**（三次函数的符号分析与不等式）：已知 f(x) = (x+2)(x-1)(x-3)。

（i）求 f(x) = 0 的解；
（ii）解 f(x) > 0；
（iii）画出 y = f(x) 的草图。

**解**：

（i）三个线性因子分别等于零：x = -2，x = 1，x = 3。

（ii）将实轴按三个零点分为四个区间。在每个区间内取一个测试点，判断每个因子的符号，三个因子符号的乘积即为 f(x) 的符号：

| 区间 | 测试点 | (x+2) | (x-1) | (x-3) | 乘积符号 |
|------|--------|-------|-------|-------|---------|
| x < -2 | x = -3 | -1（负） | -4（负） | -6（负） | 负×负×负 = **负** |
| -2 < x < 1 | x = 0 | 2（正） | -1（负） | -3（负） | 正×负×负 = **正** |
| 1 < x < 3 | x = 2 | 4（正） | 1（正） | -1（负） | 正×正×负 = **负** |
| x > 3 | x = 4 | 6（正） | 3（正） | 1（正） | 正×正×正 = **正** |

因此 f(x) > 0 的解为 -2 < x < 1 或 x > 3。

（iii）草图要点：
- x 截距：(-2, 0)，(1, 0)，(3, 0)
- y 截距：f(0) = (2)(-1)(-3) = 6
- 端部行为：a = 1 > 0，所以 x → -∞ 时 f → -∞，x → ∞ 时 f → ∞
- 图形在三个零点之间依次穿越 x 轴

---

**例 4**（因式定理与三次函数分解）：已知 f(x) = x³ + kx² - 4x - 4 能被 x+1 整除，求 k 的值，并完全因式分解 f(x)。

**解**：

**第一步**（应用因式定理）：如果 x+1 是因子，则 f(-1) = 0。

f(-1) = (-1)³ + k(-1)² - 4(-1) - 4 = -1 + k + 4 - 4 = k - 1

令 f(-1) = 0，得 k - 1 = 0 ⇒ k = 1。

**第二步**（综合除法分解）：f(x) = x³ + x² - 4x - 4。

除以 (x+1)：

```
    -1 |  1    1   -4   -4
       |     -1    0    4
       -------------------
          1    0   -4    0
```

商为 x² - 4 = (x-2)(x+2)。

**第三步**（写出完全因式分解）：

f(x) = (x+1)(x-2)(x+2)

---

## 4.3 指数函数与对数函数

### 4.3.1 指数函数 f(x) = a^x（a > 0，a ≠ 1）

指数函数的核心特征是：函数值的增长（或衰减）速度与函数本身的大小成正比。

**图形性质**（以 a > 1 为例）：
- 定义域：R（全体实数）
- 值域：(0, ∞)（永远取正值）
- 恒过点 (0, 1)，因为 a⁰ = 1
- 当 a > 1 时，函数严格递增；当 0 < a < 1 时，函数严格递减
- **水平渐近线**：y = 0（x 轴）。当 a > 1 时，x → -∞ 时趋近于 y=0；当 0 < a < 1 时，x → ∞ 时趋近于 y=0。

**更一般的形式**：y = k e^(nx) + a
- 水平渐近线为 y = a
- k 控制垂直拉伸和方向（k > 0 时图形在渐近线上方，k < 0 时在下方）

**为什么 e 如此重要？**

d/dx(e^x) = e^x

e^x 是唯一**导数等于自身**的函数。如果用一般底数 a：

d/dx(a^x) = a^x ln a

当 a = e 时，ln e = 1，导数简化为 e^x 自身。

### 4.3.2 自然指数函数 e^x 的详细推导

**问题**：是否存在一个数 e，使得 e^x 的导数等于 e^x？

从一般指数函数 f(x) = a^x 出发。根据导数定义：

f'(x) = lim_{h→0} (a^(x+h) - a^x)/h

**第一步**：提取公因子 a^x：

f'(x) = lim_{h→0} a^x(a^h - 1)/h = a^x · lim_{h→0} (a^h - 1)/h

**第二步**：记 L(a) = lim_{h→0} (a^h - 1)/h。这个极限依赖于 a。于是：

f'(x) = a^x · L(a) = f(x) · L(a)

**第三步**：我们希望 L(a) = 1，这样 f'(x) = f(x)。数值求解 L(a) = 1：

| a | L(a) ≈ (a^0.001 - 1)/0.001 |
|---|---------------------------|
| 2 | ≈ 0.693 |
| 2.7 | ≈ 0.993 |
| 2.71 | ≈ 0.996 |
| 2.718 | ≈ 0.999 |
| 2.71828 | ≈ 1.000 |

这个特殊的数就是 e ≈ 2.71828，它也可以定义为极限：

e = lim_{n→∞} (1 + 1/n)^n

**数值验证**：
- n = 1：(1+1)¹ = 2
- n = 10：(1.1)^10 ≈ 2.594
- n = 100：(1.01)^100 ≈ 2.705
- n = 10000：(1.0001)^10000 ≈ 2.718

### 4.3.3 对数函数 f(x) = log_a x（a > 0，a ≠ 1）

对数函数是指数函数的**反函数**：

y = log_a x ⇔ a^y = x  (x > 0)

**图形性质**（以 a > 1 为例）：
- 定义域：(0, ∞)（真数必须为正）
- 值域：R
- 恒过点 (1, 0)，因为 log_a 1 = 0
- 当 a > 1 时，函数严格递增；当 0 < a < 1 时，函数严格递减
- **垂直渐近线**：x = 0（y 轴）。当 a > 1 时，x → 0⁺ 时 log_a x → -∞

**更一般的形式**：y = k ln(ax + b)
- 垂直渐近线在 ax + b = 0 处，即 x = -b/a
- 定义域为 x > -b/a

**两个重要的特殊底数**：
- **常用对数**（以 10 为底）：log_10 x，有时记作 lg x
- **自然对数**（以 e 为底）：log_e x，记作 ln x

**指数函数与对数函数互为反函数**：

y = a^x  ⟷  y = log_a x

**对称性推导**：
假设点 (p, q) 在 y = a^x 上，则 q = a^p。
由对数定义，p = log_a q，所以点 (q, p) 在 y = log_a x 上。
点 (p, q) 关于直线 y = x 的对称点正是 (q, p)（因为交换坐标）。
因此两个函数的图形关于 y = x 对称。

### 4.3.4 对数运算法则的详细推导

对数法则的本质：将对数运算**降级**——乘法变为加法，除法变为减法，指数变为系数。

**法则 1——积的对数**：log_a (MN) = log_a M + log_a N

*推导*：
设 log_a M = x，log_a N = y。
由对数定义：a^x = M，a^y = N。
那么 MN = a^x · a^y = a^(x+y)。
再由对数定义：log_a (MN) = x + y = log_a M + log_a N。□

**法则 2——商的对数**：log_a (M/N) = log_a M - log_a N

*推导*：
设 log_a M = x，log_a N = y。
则 M/N = a^x / a^y = a^(x-y)。
因此 log_a (M/N) = x - y = log_a M - log_a N。□

**法则 3——幂的对数**：log_a (M^k) = k log_a M

*推导*：
设 log_a M = x，则 a^x = M。
于是 M^k = (a^x)^k = a^(kx)。
由定义：log_a (M^k) = kx = k log_a M。□

**法则 4——换底公式**：log_a M = (log_b M) / (log_b a)

*推导*：
设 y = log_a M，则 a^y = M。
两边取以 b 为底的对数：
log_b (a^y) = log_b M
y log_b a = log_b M
y = (log_b M) / (log_b a)
因此 log_a M = (log_b M) / (log_b a)。□

换底公式最常见的两种应用形式：

log_a M = (log M) / (log a)   （换为常用对数），
log_a M = (ln M) / (ln a)   （换为自然对数）

**逆恒等式**（直接来自反函数定义）：

a^(log_a x) = x  (x > 0)， log_a (a^x) = x  (x ∈ R)

### 4.3.5 解指数方程 a^x = b

**基本方法**：两边取对数，利用幂法则将对数中的指数“降”为系数。

a^x = b  ⇒  ln(a^x) = ln b  ⇒  x ln a = ln b  ⇒  x = (ln b) / (ln a)

也可以用常用对数：x = (log b) / (log a)。

> ⚠️ **注意**：只有当 b > 0 时方程才有实数解。若 b ≤ 0，方程 a^x = b 无实数解（因为指数函数的值域为 (0, ∞)）。

---

### 例题 4.3（指数与对数函数）

**例 1**（对数化简与求值）：化简 log_2 24 - log_2 3 + log_2 (1/2)。

**解**：

**第一步**（用商法则合并前两项）：

log_2 24 - log_2 3 = log_2 (24/3) = log_2 8

**第二步**（用积法则继续合并）：

log_2 8 + log_2 (1/2) = log_2 (8 × 1/2) = log_2 4

**第三步**（求值）：log_2 4 = 2，因为 2² = 4。

所以表达式的值为 2。

---

**例 2**（换底公式与对数方程）：

（i）用自然对数表示 log_5 20 并化简；
（ii）解方程 log_2 (x+1) + log_2 (x-1) = 3。

**解**：

（i）用换底公式：

log_5 20 = (ln 20) / (ln 5)

分解 20 = 4 × 5，所以 ln 20 = ln(4 × 5) = ln 4 + ln 5 = ln(2²) + ln 5 = 2 ln 2 + ln 5。

因此：

log_5 20 = (2 ln 2 + ln 5) / (ln 5) = 2 (ln 2)/(ln 5) + 1

（ii）**第一步**（合并对数）：

log_2[(x+1)(x-1)] = 3 ⇒ log_2(x² - 1) = 3

**第二步**（去对数）：两边取以 2 为底的指数：

x² - 1 = 2³ = 8

**第三步**（解二次方程）：

x² = 9 ⇒ x = ±3

**第四步**（检查定义域）：对数的真数必须为正。

x+1 > 0 ⇒ x > -1，x-1 > 0 ⇒ x > 1。取交集得 x > 1。

x = 3 > 1，有效。x = -3 不满足 x > 1，舍去。

因此 x = 3。

---

**例 3**（解指数方程与指数—对数复合）：

（i）解 3^(2x-1) = 7，结果用自然对数表示；
（ii）已知 f(x) = ln(e^(2x) + 1)，求 f(0)。

**解**：

（i）两边取自然对数：

ln(3^(2x-1)) = ln 7

用幂法则将对数中的指数“降”下来：

(2x - 1) ln 3 = ln 7

解出 x：

2x - 1 = (ln 7) / (ln 3) ⇒ 2x = 1 + (ln 7)/(ln 3) ⇒ x = (1/2)(1 + (ln 7)/(ln 3))

（ii）代入 x = 0：

f(0) = ln(e⁰ + 1) = ln(1 + 1) = ln 2

---

**例 4**（指数方程——代换法）：解方程 4^x - 5 · 2^x + 4 = 0。

**解**：

**第一步**（识别结构）：注意到 4^x = (2²)^x = 2^(2x) = (2^x)²。

**第二步**（换元）：令 u = 2^x，注意 u > 0（因为指数函数的值域为正）。

方程化为：

u² - 5u + 4 = 0

**第三步**（解二次方程）：

(u-1)(u-4) = 0 ⇒ u = 1 或 u = 4

**第四步**（回代）：

- 2^x = 1 ⇒ x = log_2 1 = 0
- 2^x = 4 ⇒ x = log_2 4 = 2

两个解都满足定义域，所以 x = 0 或 x = 2。

---

**例 5**（对数方程——换底后化为一元二次）：解方程 log_3 x + log_x 3 = 2。

**解**：

**第一步**（换底）：用换底公式将 log_x 3 转换为以 3 为底：

log_x 3 = (log_3 3) / (log_3 x) = 1 / (log_3 x)

**第二步**（换元）：设 u = log_3 x（注意 x > 0 且 x ≠ 1，否则 log_x 3 无定义）。

方程化为：

u + 1/u = 2

**第三步**（去分母）：两边乘以 u（u ≠ 0）：

u² + 1 = 2u ⇒ u² - 2u + 1 = 0 ⇒ (u-1)² = 0

**第四步**（回代）：u = 1 ⇒ log_3 x = 1 ⇒ x = 3¹ = 3。

**验证**：log_3 3 = 1，log_3 3 = 1，1 + 1 = 2。✓

---

**例 6**（指数不等式——两边取对数）：解不等式 2^x < 5。

**解**：

两边取自然对数。因为 ln 是递增函数，不等号方向**不变**：

ln(2^x) < ln 5

用幂法则：

x ln 2 < ln 5

因为 ln 2 > 0，两边除以 ln 2 不等号方向不变：

x < (ln 5) / (ln 2)

所以解为 x < (ln 5)/(ln 2)（约为 x < 2.322）。

> ⚠️ **注意**：如果底数 a 满足 0 < a < 1，取对数时不等号会反转（因为 ln a < 0）。例如解 (1/2)^x < 3 时：
> x ln(1/2) < ln 3，因为 ln(1/2) < 0，两边除以它得到 x > (ln 3) / ln(1/2)。

---

**例 7**（用已知对数表示未知对数）：已知 log_a 2 = p，log_a 5 = q。用 p 和 q 表示：

（i）log_a 20；
（ii）log_a 0.4。

**解**：

（i）20 = 2² × 5，所以：

log_a 20 = log_a (2² × 5) = log_a 2² + log_a 5 = 2 log_a 2 + log_a 5 = 2p + q

（ii）0.4 = 2/5，所以：

log_a 0.4 = log_a (2/5) = log_a 2 - log_a 5 = p - q

---

**例 8**（指数函数图形的渐近线与变换——考纲 6.1）：函数 f(x) = 3e^(2x) - 4。

（i）求 f(x) 的水平渐近线；
（ii）求 f(x) 与坐标轴的交点；
（iii）描述 f 的定义域和值域。

**解**：

（i）当 x → -∞ 时，e^(2x) → 0，所以 3e^(2x) - 4 → -4。

因此水平渐近线为 y = -4。

（ii）**y 截距**：令 x = 0，f(0) = 3e⁰ - 4 = 3 - 4 = -1，即 (0, -1)。

**x 截距**：令 f(x) = 0：

3e^(2x) - 4 = 0 ⇒ e^(2x) = 4/3

两边取自然对数：2x = ln(4/3) ⇒ x = (1/2) ln(4/3)。

x 截距为 ((1/2) ln(4/3), 0)。

（iii）**定义域**：R（全体实数）。

**值域**：因为 e^(2x) > 0 对所有实数 x 成立，所以 3e^(2x) > 0，3e^(2x) - 4 > -4。值域为 (-4, ∞)。

---

**例 9**（对数函数图形的渐近线——考纲 6.1）：函数 g(x) = 2 ln(x-1) + 3。

（i）求 g(x) 的定义域和垂直渐近线；
（ii）求 g(x) 与坐标轴的交点。

**解**：

（i）**定义域**：真数必须为正，x-1 > 0 ⇒ x > 1。定义域为 (1, ∞)。

**垂直渐近线**：真数为零处 x-1 = 0 ⇒ x = 1。当 x → 1⁺ 时，ln(x-1) → -∞，g(x) → -∞。

因此垂直渐近线方程为 x = 1。

（ii）**y 截距**：x = 0 不在定义域内，所以没有 y 截距。

**x 截距**：令 g(x) = 0：

2 ln(x-1) + 3 = 0 ⇒ ln(x-1) = -3/2

两边取指数：x - 1 = e^(-3/2) ⇒ x = 1 + e^(-3/2)。

x 截距为 (1 + e^(-3/2), 0)（约为 (1.223, 0)）。

---

## 4.4 反函数与复合函数

### 4.4.1 反函数

**定义**：若函数 f 是单射（一一对应），则存在反函数 f⁻¹，满足：

f⁻¹(y) = x ⇔ f(x) = y

**核心性质**：

f⁻¹(f(x)) = x， f(f⁻¹(x)) = x

**几何意义**：y = f(x) 与 y = f⁻¹(x) 的图形关于直线 y = x 对称。

**对称性的详细推导**：

设点 (a, b) 在 y = f(x) 上，即 b = f(a)。
由反函数定义，a = f⁻¹(b)，所以点 (b, a) 在 y = f⁻¹(x) 上。
点 (a, b) 关于直线 y = x 的对称点正是 (b, a)（因为交换坐标）。
因此 f 和 f⁻¹ 的图形互为关于 y = x 的镜像。

**举例**：对于 f(x) = 2^x 和 f⁻¹(x) = log_2 x：
- f 过 (0, 1)，(1, 2)，(2, 4)
- f⁻¹ 过 (1, 0)，(2, 1)，(4, 2)
- 每一对点关于 y = x 对称

**为什么只有单射函数才有反函数？**

如果 f 不是单射（即存在 x₁ ≠ x₂ 使得 f(x₁) = f(x₂) = y₀），那么反函数 f⁻¹ 在 x = y₀ 处需要返回两个不同的值——x₁ 和 x₂——这违反了函数的定义。因此非单射函数没有反函数。

**如何用文字解释函数没有反函数**（考纲 1.5 标准表述）：

“函数 f 不是单射（one–one），因为存在不同的 x 值对应同一个 y 值。例如 f(a) = f(b) 但 a ≠ b。水平检验线 y = f(a) 与 y = f(x) 的图形相交于多于一个点。因此 f 没有反函数。”

**求反函数的步骤**：
1. 将 y = f(x) 写成等式。
2. 解出 x，用 y 表示。
3. 交换 x 和 y 的角色，得到 y = f⁻¹(x) 的表达式。
4. 注明反函数的定义域（即原函数的值域）。

**原函数与反函数定义域和值域的关系**：
- f 的定义域 = f⁻¹ 的值域
- f 的值域 = f⁻¹ 的定义域

> ⚠️ **关键**：有时原函数的定义域需要被限制（restrict）才能使 f 成为单射，从而存在反函数。例如 f(x) = x² 在整个 R 上不是单射，但限制为 x ≥ 0 后，变为单射，反函数为 √x。

### 4.4.2 复合函数

**定义**：(f ∘ g)(x) = f(g(x))，读作“f 复合 g”，也写作 fg(x)。

**复合顺序**：先应用 g，再将 f 应用于结果。顺序通常不可交换——一般 f(g(x)) ≠ g(f(x))。

**复合函数的定义域**：需要满足两个条件：
1. x 在 g 的定义域内
2. g(x) 在 f 的定义域内

**重要关系**（考纲 1.2）：

Domain(gf) ⊆ Domain(f)， Range(gf) ⊆ Range(g)

> 解释：要计算 gf(x) = g(f(x))，首先 x 必须在 f 的定义域内，且 f(x) 必须在 g 的定义域内。因此 gf 的定义域是 f 的定义域的子集。gf 的输出来自 g，所以其值域是 g 的值域的子集。

**定义域限制使复合函数存在**的进一步说明：

有时 f 的定义域需要被限制，才能使 gf 存在。这是因为 f(x) 必须落在 g 的定义域内。

*示例*：已知 f(x) = x²（定义域 R），g(x) = √(1 - x²)（定义域 |x| ≤ 1）。

gf(x) = g(f(x)) = √(1 - (x²)²) = √(1 - x⁴)。

gf 的定义域要求 1 - x⁴ ≥ 0 ⇒ |x| ≤ 1。

所以 Domain(gf) = [-1, 1] ⊂ R = Domain(f)。

---

### 例题 4.4（反函数与复合函数）

**例 1**（求反函数——线性函数）：求 f(x) = (2x - 3)/5 的反函数。

**解**：

**第一步**（写等式）：y = (2x - 3)/5

**第二步**（解出 x）：

5y = 2x - 3 ⇒ 2x = 5y + 3 ⇒ x = (5y + 3)/2

**第三步**（交换 x 和 y）：

f⁻¹(x) = (5x + 3)/2

**第四步**（定义域）：反函数的定义域为 R（原函数的值域为 R）。

**验证**：

f(f⁻¹(x)) = f((5x+3)/2) = [2·(5x+3)/2 - 3]/5 = (5x+3-3)/5 = x

---

**例 2**（求反函数——含定义域限制）：已知 f(x) = x² - 4x + 3，x ≥ 2。求 f⁻¹(x) 及其定义域。

**解**：

**第一步**（配方法找顶点和值域）：

f(x) = x² - 4x + 3 = (x² - 4x + 4) - 4 + 3 = (x-2)² - 1

顶点在 (2, -1)。因为 a = 1 > 0，且定义域为 x ≥ 2（在顶点右侧），函数单调递增。值域为 [-1, ∞)。

**第二步**（解出 x）：令 y = (x-2)² - 1。

y + 1 = (x-2)² ⇒ x - 2 = ±√(y+1)

因为 x ≥ 2，取正号：x = 2 + √(y+1)。

**第三步**（交换 x 和 y）：

f⁻¹(x) = 2 + √(x+1)

**第四步**（定义域）：反函数的定义域是原函数的值域，即 [-1, ∞)。

**验证**：

f(f⁻¹(x)) = f(2 + √(x+1)) = (2+√(x+1) - 2)² - 1 = (x+1) - 1 = x

---

**例 3**（复合函数及其定义域——详细推导）：已知 f(x) = √(x-1)，g(x) = 1/(x-2)。

（i）求 fg(x) 及其定义域；
（ii）求 gf(x) 及其定义域。

**解**：

（i）fg(x) = f(g(x)) = √( 1/(x-2) - 1 )

**定义域分析**：

**条件 1**：g(x) 有定义。分母不为零：x ≠ 2。

**条件 2**：g(x) 必须落在 f 的定义域内。f 的定义域为 √内 ≥ 0，即：

1/(x-2) - 1 ≥ 0

解这个不等式。这是关键步骤，分情况讨论：

*情况 A*：x > 2。两边乘以正数 (x-2)，不等号不变：

1 ≥ x - 2 ⇒ x ≤ 3

结合 x > 2，得 2 < x ≤ 3。

*情况 B*：x < 2。两边乘以负数 (x-2)，不等号反转：

1 ≤ x - 2 ⇒ x ≥ 3

结合 x < 2，无解。

因此条件 2 给出 2 < x ≤ 3。

**取交集**：x ≠ 2 且 2 < x ≤ 3，定义域为 (2, 3]。

**化简表达式**：

1/(x-2) - 1 = [1 - (x-2)]/(x-2) = (3 - x)/(x-2)

因此：

fg(x) = √( (3 - x)/(x - 2) ),  x ∈ (2, 3]

（ii）gf(x) = g(f(x)) = 1 / ( √(x-1) - 2 )

**定义域分析**：

**条件 1**：f(x) 有定义。根号内非负：x - 1 ≥ 0 ⇒ x ≥ 1。

**条件 2**：f(x) 必须落在 g 的定义域内。g 的分母不能为零：√(x-1) - 2 ≠ 0。

√(x-1) ≠ 2 ⇒ x-1 ≠ 4 ⇒ x ≠ 5

**取交集**：x ≥ 1 且 x ≠ 5，定义域为 [1, 5) ∪ (5, ∞)。

---

**例 4**（复合函数的值域与 fg ≠ gf）：f(x) = 2^x，g(x) = x²。求 fg(x) 和 gf(x) 的表达式，并求 fg(x) 的值域。

**解**：

**fg(x)**：fg(x) = f(g(x)) = 2^(x²)

**gf(x)**：gf(x) = g(f(x)) = (2^x)² = 2^(2x) = 4^x

注意 fg(x) = 2^(x²) ≠ 4^x = gf(x)，说明复合顺序重要。

**求 fg(x) 的值域**：
- g(x) = x² 的值域为 [0, ∞)
- f(u) = 2^u 在 [0, ∞) 上单调递增
- 最小值：u = 0 时 2⁰ = 1
- 上界：u → ∞ 时 2^u → ∞

因此 fg(x) 的值域为 [1, ∞)。

---

**例 5**（用文字解释函数为何没有反函数——考纲 1.5）：

（i）f(x) = x²，定义域 R。
（ii）f(x) = cos x，定义域 [0, 2π]。

**解**：

（i）f(x) = x² **不是单射**，因为存在不同的 x 值对应同一个 y 值。例如 f(2) = 4 且 f(-2) = 4，即 2 ≠ -2 但 f(2) = f(-2)。水平检验线 y = 4 与 y = x² 的图形相交于 (2, 4) 和 (-2, 4) 两点。因此 f 没有反函数。

> 但若将定义域限制为 x ≥ 0，则 f 变为单射，反函数为 f⁻¹(x) = √x。

（ii）f(x) = cos x 在 [0, 2π] 上**不是单射**。例如 cos(π/3) = 1/2 且 cos(5π/3) = 1/2，但 π/3 ≠ 5π/3。水平检验线 y = 1/2 与图形相交于两点。因此 f 没有反函数。

> 但若将定义域限制为 [0, π]，cos x 严格递减，此时反函数为 arccos x。

---

**例 6**（草图表示函数与其反函数关于 y=x 对称——考纲 1.8）：已知 f(x) = e^x。

（i）求 f⁻¹(x)；
（ii）描述 y = f(x)，y = f⁻¹(x) 和 y = x 在同一坐标系中的关系。

**解**：

（i）y = e^x ⇒ x = ln y ⇒ f⁻¹(x) = ln x（定义域 x > 0）。

（ii）**对称关系**：y = e^x 和 y = ln x 的图形关于直线 y = x 对称。

具体对应点：
- e^x 过 (0, 1) → ln x 过 (1, 0)
- e^x 过 (1, e) → ln x 过 (e, 1)
- e^x 过 (-1, e⁻¹) → ln x 过 (e⁻¹, -1)

每条曲线都是另一条在 y = x 中的镜像。

**渐近线关系**：
- y = e^x 有水平渐近线 y = 0（x 轴）
- y = ln x 有垂直渐近线 x = 0（y 轴）
- 这一对渐近线也关于 y = x 对称

---

**例 7**（复合函数的顺序重要性 fg ≠ gf——考纲 1.7）：f(x) = 3x + 1，g(x) = x²。求 fg(x) 和 gf(x)，并比较。

**解**：

fg(x) = f(g(x)) = f(x²) = 3x² + 1

gf(x) = g(f(x)) = g(3x+1) = (3x+1)² = 9x² + 6x + 1

显然 fg(x) ≠ gf(x)，因此复合函数的顺序至关重要。

---

**例 8**（反函数与复合的综合应用）：已知 f(x) = 2x + 3，g(x) = 1/(x-1)，x ≠ 1。

（i）求 f⁻¹(x)；
（ii）求 gf⁻¹(x) 及其定义域。

**解**：

（i）y = 2x + 3 ⇒ 2x = y - 3 ⇒ x = (y-3)/2
交换得 f⁻¹(x) = (x-3)/2，定义域 R。

（ii）gf⁻¹(x) = g((x-3)/2) = 1 / [ (x-3)/2 - 1 ]

化简分母：(x-3)/2 - 1 = (x-3 - 2)/2 = (x-5)/2

因此：

gf⁻¹(x) = 1 / ((x-5)/2) = 2/(x-5)

**定义域**：
- f⁻¹(x) 的定义域为 R（无限制）
- g 的定义域要求分母不为零：(x-3)/2 - 1 ≠ 0 ⇒ (x-5)/2 ≠ 0 ⇒ x ≠ 5

因此定义域为 R \ {5}。

---

**例 9**（考纲 1.6 指定示例——指数函数的反函数）：已知 f(x) = e^(2x)，求 f⁻¹(x)。

**解**：

令 y = e^(2x)。两边取自然对数：

ln y = ln(e^(2x)) = 2x · ln e = 2x

因为 ln e = 1，所以 2x = ln y ⇒ x = (1/2) ln y。

交换 x 和 y：

f⁻¹(x) = (1/2) ln x

**定义域**：原函数 f(x) = e^(2x) 的值域为 (0, ∞)，所以 f⁻¹ 的定义域为 (0, ∞)。

**验证**：

f(f⁻¹(x)) = e^(2 · (1/2) ln x) = e^(ln x) = x  (x > 0)

---

**例 10**（验证 Domain(gf) ⊆ Domain(f)——考纲 1.2）：f(x) = √x，g(x) = 1/(x-3)。求 gf(x) 的定义域，并验证 Domain(gf) ⊆ Domain(f)。

**解**：

gf(x) = g(f(x)) = 1 / (√x - 3)

**条件 1**：f 的定义域：x ≥ 0。
**条件 2**：f(x) 在 g 的定义域内：√x - 3 ≠ 0 ⇒ √x ≠ 3 ⇒ x ≠ 9。

取交集：x ≥ 0 且 x ≠ 9，即 [0, 9) ∪ (9, ∞)。

验证 Domain(gf) ⊆ Domain(f)：
Domain(f) = [0, ∞)，Domain(gf) = [0, 9) ∪ (9, ∞) ⊂ [0, ∞)。✓

---

## 4.5 绝对值函数 y = |f(x)| 的图像

### 4.5.1 基本原理

|f(x)| 的定义为：

|f(x)| = { f(x), f(x) ≥ 0;  -f(x), f(x) < 0 }

**图形变换规则**：取 y = f(x) 的图形，将 x 轴下方的部分沿 x 轴向上**反射**（即取 y 坐标的绝对值），x 轴上方和轴上的部分保持不变。

**关键观察**：
- 反射后，图形的所有 y 值都非负（|f(x)| ≥ 0）。
- 在 f(x) = 0 的点（即 x 截距处），绝对值图形会形成**尖点**——这是因为左右两侧的斜率突然改变了符号。
- |f(x)| 的值域是 [0, ∞)（如果原函数能取到任意大的正值）或 [0, 有限最大值]。

### 4.5.2 各类函数的绝对值图形特征

| 原函数类型 | |f(x)| 的特征 |
|-----------|----------------|
| **线性** |mx+c| | V 形，尖点在 x = -c/m |
| **二次** |ax²+bx+c| | 在 x 截距处有尖点，抛物线在 x 轴下方的部分翻折到上方 |
| **三次** |(x-p)(x-q)(x-r)| | 在三个 x 截距处都有尖点 |
| **三角** |a sin(bx)+c| | 周期减半，波谷翻为波峰 |
| **三角** |a cos(bx)+c| | 周期减半，波谷翻为波峰 |
| **三角** |a tan(bx)+c| | 垂直渐近线位置不变，图像翻折使 y ≥ 0 |

### 4.5.3 绝对值方程与不等式的解法

**方程 |f(x)| = k（k > 0）**：等价于 f(x) = k 或 f(x) = -k。

**不等式 |f(x)| < k（k > 0）**：等价于 -k < f(x) < k。

**不等式 |f(x)| > k（k > 0）**：等价于 f(x) > k 或 f(x) < -k。

---

### 例题 4.5（绝对值函数）

**例 1**（线性函数的绝对值——V 形）：画出 y = |2x - 3| 的草图，并求 x 为何值时 y = 5。

**解**：

**画图**：

f(x) = 2x - 3，f(x) = 0 时 x = 1.5。

当 x ≥ 1.5 时，2x - 3 ≥ 0，所以 |2x-3| = 2x-3（直线，斜率 2）。
当 x < 1.5 时，2x - 3 < 0，所以 |2x-3| = -(2x-3) = -2x+3（直线，斜率 -2）。

图形是 V 形，尖点在 (1.5, 0)。

**解方程 |2x-3| = 5**：

情况 1：2x-3 = 5 ⇒ 2x = 8 ⇒ x = 4
情况 2：2x-3 = -5 ⇒ 2x = -2 ⇒ x = -1

解为 x = 4 或 x = -1。

---

**例 2**（二次函数的绝对值）：画出 y = |x² - 4x + 3| 的草图。

**解**：

**第一步**（画原函数）：y = x² - 4x + 3 = (x-1)(x-3)。

- x 截距：x = 1 和 x = 3
- 顶点：x = 2，y = 4 - 8 + 3 = -1，即 (2, -1)
- 开口向上（a = 1 > 0）

**第二步**（取绝对值）：[1, 3] 区间内原函数 f(x) ≤ 0，这部分翻折到上方。
x < 1 和 x > 3 部分 f(x) > 0，保持不变。

**第三步**（标出关键点）：尖点在 x = 1 和 x = 3 处。翻折后原顶点 (2, -1) 变为 (2, 1)。

值域为 [0, ∞)。

---

**例 3**（三次函数的绝对值图像与符号分析）：已知 f(x) = (x+1)(x-1)(x-2)。

（i）画出 y = |f(x)| 的草图；
（ii）讨论 |f(x)| 与 y = 2 的交点情况。

**解**：

（i）**符号分析**：

| 区间 | 测试点 | (x+1) | (x-1) | (x-2) | f(x) 符号 | |f(x)| |
|------|--------|-------|-------|-------|------------|----------|
| x < -1 | x=-2 | 负 | 负 | 负 | **负** | 翻折到正 |
| -1 < x < 1 | x=0 | 正 | 负 | 负 | **正** | 保持不变 |
| 1 < x < 2 | x=1.5 | 正 | 正 | 负 | **负** | 翻折到正 |
| x > 2 | x=3 | 正 | 正 | 正 | **正** | 保持不变 |

x 截距：x = -1, 1, 2（均为尖点）。
y 截距：f(0) = (1)(-1)(-2) = 2。

（ii）y = 2 与 |f(x)| 的交点：
- 在 (-1, 1) 区间上，f(0) = 2，有一个交点。
- 在 x < -1 翻折区域，|f(x)| = -f(x)，f(-2) = (-1)(-3)(-4) = -12，|f(-2)| = 12，f(-1) = 0。由连续性，y = 2 在此区间上相交一次。
- 在 (1, 2) 翻折区域，同理相交一次。

因此共有 **3 个交点**。

---

**例 4**（|a sin(bx)+c| 形式——考纲 1.4 指定）：画出 y = |sin x| 在 [0, 2π] 上的草图。

**解**：

先画 y = sin x：
- [0, π] 上 sin x ≥ 0（x 轴及上方）
- [π, 2π] 上 sin x ≤ 0（x 轴下方）

取绝对值：
- [0, π]：保持不变
- [π, 2π]：向上反射（|sin x| = -sin x）

图形特征：
- 两个相同的“拱形”：(0,0)→(π/2,1)→(π,0) 和 (π,0)→(3π/2,1)→(2π,0)
- **周期**：π（原 sin x 周期为 2π，反射后每 π 重复一次）
- **值域**：[0, 1]
- **尖点**：x = 0, π, 2π 等处

---

**例 5**（|a cos(bx)+c| 形式——考纲 1.4 指定）：画出 y = |3 cos 2x - 1| 在 [0, π] 上的草图。

**解**：

**第一步**（画原函数 y = 3 cos 2x - 1）：
- 振幅为 3，周期为 π，垂直下移 1 个单位
- 最大值：3(1) - 1 = 2，最小值：3(-1) - 1 = -4
- 零点：3 cos 2x - 1 = 0 ⇒ cos 2x = 1/3
  2x = arccos(1/3) 或 2x = 2π - arccos(1/3)
  即 x = (1/2) arccos(1/3) 或 x = π - (1/2) arccos(1/3)
  记 α = (1/2) arccos(1/3) ≈ 0.615 弧度

**第二步**（取绝对值）：
- 在两个零点之间的区间（α < x < π - α），3 cos 2x - 1 ≤ 0，这部分翻折到上方
- 其余部分保持不变

**第三步**（标出关键点）：
- 尖点：x = α 和 x = π - α 处
- 翻折后的“波峰”：原最小值 x = π/2 处 3 cos π - 1 = -4 翻折为 4
- 原最大值 x = 0 处 2 和 x = π 处 2 保持不变

**最终图形特征**：
- 值域：[0, 4]
- 尖点数量（一个周期内）：2 个
- 渐近线：无

---

**例 6**（|a tan(bx)+c| 形式——考纲 1.4 指定）：画出 y = |tan x - 1| 在 (-π/2, π/2) 上的草图。

**解**：

**第一步**（画原函数 y = tan x - 1）：
- tan x 的周期为 π，垂直下移 1 个单位
- 垂直渐近线：x = -π/2 和 x = π/2
- 零点：tan x - 1 = 0 ⇒ tan x = 1 ⇒ x = π/4（在区间 (-π/2, π/2) 内）
- 当 x → π/2⁻ 时，tan x → ∞，tan x - 1 → ∞
- 当 x → -π/2⁺ 时，tan x → -∞，tan x - 1 → -∞

**第二步**（取绝对值）：
- 当 x < π/4 时，tan x - 1 < 0，翻折到上方
- 当 x > π/4 时，tan x - 1 > 0，保持不变
- 当 x = π/4 时，tan(π/4) - 1 = 0，为尖点

**第三步**（分析翻折后的行为）：
- 在 x < π/4 区域，|tan x - 1| = -(tan x - 1) = 1 - tan x
  当 x → -π/2⁺ 时，tan x → -∞，1 - tan x → ∞
- 在 x > π/4 区域，|tan x - 1| = tan x - 1
  当 x → π/2⁻ 时，tan x → ∞，tan x - 1 → ∞

**最终图形特征**：
- 垂直渐近线仍然在 x = -π/2 和 x = π/2 处（绝对值不改变渐近线的位置）
- 尖点在 x = π/4 处
- 图形在尖点两侧都趋向无穷大
- 值域：[0, ∞)（最小值 0 在 x = π/4 处）

---

**例 7**（绝对值方程——二次型）：解方程 |x² - 3x + 2| = 2。

**解**：

原二次式 x² - 3x + 2 = (x-1)(x-2)，根为 x = 1, 2。

**情况 1**：x² - 3x + 2 = 2

x² - 3x = 0 ⇒ x(x-3) = 0 ⇒ x = 0 或 x = 3

检查：x = 0 时 0 - 0 + 2 = 2 > 0（在非负区域），有效。x = 3 时 9 - 9 + 2 = 2 > 0，有效。

**情况 2**：x² - 3x + 2 = -2

x² - 3x + 4 = 0

判别式 Δ = 9 - 16 = -7 < 0，无实数解。

因此解为 x = 0 或 x = 3。

---

**例 8**（绝对值不等式——两边平方技巧）：解 |x-1| > |2x+3|。

**解**：

两边都非负，可以平方，不等号方向不变：

(x-1)² > (2x+3)²

展开：

x² - 2x + 1 > 4x² + 12x + 9

移项：

0 > 3x² + 14x + 8 ⇒ 3x² + 14x + 8 < 0

求根：

x = [ -14 ± √(196 - 96) ] / 6 = [ -14 ± 10 ] / 6

x = (-14 + 10)/6 = -4/6 = -2/3， x = (-14 - 10)/6 = -24/6 = -4

因为二次项系数 3 > 0，抛物线开口向上，不等式在两根之间成立：

-4 < x < -2/3

---

**例 9**（绝对值函数的最值——几何意义法）：函数 f(x) = |x-1| + |x-3|，求 f(x) 的最小值。

**解**：

**几何解释**：|x-1| 是数轴上 x 到 1 的距离，|x-3| 是 x 到 3 的距离。f(x) 是这两个距离之和。

当 x 在 [1, 3] 之间时，两距离之和恒等于线段长度 2。
当 x < 1 或 x > 3 时，和大于 2。

因此 f(x) 的最小值为 2，在 x ∈ [1, 3] 时取到。

**代数验证**——分段讨论：

f(x) = {
  -(x-1) - (x-3) = -2x + 4,  x < 1
  (x-1) - (x-3) = 2,         1 ≤ x ≤ 3
  (x-1) + (x-3) = 2x - 4,     x > 3
}

当 x < 1 时，f(x) = -2x + 4 > 2（因为 -2x > -2）。
当 1 ≤ x ≤ 3 时，f(x) = 2。
当 x > 3 时，f(x) = 2x - 4 > 2。

最小值为 2。

---

## 本章综合练习题

### 一、定义域与值域（6 题）

1. 求 f(x) = √(x+3) / (x-5) 的定义域。

2. 已知 f(x) = x² - 6x + 10，x ∈ R。求 f(x) 的最小值及值域。

3. 求 f(x) = ln(4 - x²) 的定义域和值域。

4. 求 f(x) = 1/√(2x-1) + ln(5-x) 的定义域。

5. 判断 y = ±√(9 - x²)（|x| ≤ 3）是否为函数，并解释原因。

6. 已知 f(x) = (3x-1)/(x+2)，求 f 的值域，并判断 f 是否为单射。

### 二、线性与三次函数（5 题）

7. 直线 L 经过点 (2, -1) 且与直线 y = 3x + 2 平行，求 L 的方程。

8. 已知 f(x) = x³ - 2x² - 5x + 6。
   （i）验证 x = 1 是 f(x) 的一个根，并完全因式分解 f(x)；
   （ii）求 f(x) = 0 的所有解。

9. 已知三次函数 f(x) = x³ - 3x² - 9x + 11，求 f'(x) 并解 f'(x) = 0，判断驻点的类型。

10. 解三次不等式 (x+1)(x-2)(x-4) > 0。

11. 已知 f(x) = x³ + kx² - 5x - 6 能被 x+2 整除，求 k 的值，并完全因式分解 f(x)。

### 三、指数与对数（9 题）

12. 化简：log_3 54 - log_3 2 + log_3 (1/3)。

13. 解方程 2^(x+1) = 5，结果用自然对数表示。

14. 解方程 log_3 (x+2) + log_3 (x-4) = 2。

15. 解方程 3^(2x) - 10 · 3^x + 9 = 0。

16. 计算：log_2 3 · log_3 4 · log_4 5 · log_5 2。

17. 函数 f(x) = 2e^x - 3。求 f(x) 的水平渐近线、y 截距和 x 截距。

18. 解不等式 3^x < 7。

19. 已知 log_a 3 = p，log_a 7 = q。用 p, q 表示 log_a 21 和 log_a (7/3)。

20. 解方程 log_2 x + log_4 x = 3。（提示：用换底公式将 log_4 x 换为以 2 为底）

### 四、反函数与复合函数（8 题）

21. 求 f(x) = (3x - 2)/4 的反函数 f⁻¹(x)。

22. 已知 f(x) = x² + 2x，x ≥ -1。求 f⁻¹(x) 及其定义域。

23. 已知 f(x) = 2x + 1，g(x) = 1/x。求 fg(x) 和 gf(x)，并求 gf(x) 的定义域。

24. 已知 f(x) = e^(3x)，求 f⁻¹(x)。

25. 已知 f(x) = ln(x+2)，x > -2。求 f⁻¹(x)。

26. 用文字解释为什么 f(x) = x⁴（定义域 R）没有反函数。

27. f(x) = √(x+1)，g(x) = x² - 4。求 fg(x) 及其定义域。

28. 已知 f(x) = x²，x ≥ 0，g(x) = 2x + 1。验证 Domain(gf) ⊆ Domain(f)。

### 五、绝对值函数（6 题）

29. 画出 y = |x-2| 的草图，并解 |x-2| = 3。

30. 解不等式 |2x+1| < 5。

31. 画出 y = |cos x| 在 [0, 2π] 上的草图，并指出其周期。

32. 解方程 |x² - 5x + 6| = 2。

33. 解不等式 |x+2| ≥ 3。

34. 函数 f(x) = |x-2| + |x+1|，求 f(x) 的最小值。

### 六、三角函数绝对值（新增 3 题——考纲 1.4 指定）

35. 画出 y = |2 cos x + 1| 在 [0, 2π] 上的草图要点，标出关键点和尖点位置。

36. 画出 y = |tan x| 在 (-π/2, π/2) 上的草图，说明渐近线位置。

37. 已知 f(x) = |3 sin 2x - 2|，求 f(x) 在 [0, π] 上的最大值和最小值。

### 七、定义域限制与复合函数存在（新增 1 题——考纲 1.2）

38. 已知 f(x) = √(x-2)，g(x) = 1/√(5-x)。求 gf(x) 及其定义域，并验证 Domain(gf) ⊆ Domain(f)。

---

## 综合练习题答案与详细解析

### 一、定义域与值域

**1.**
条件 1（根号）：x+3 ≥ 0 ⇒ x ≥ -3。
条件 2（分母不为零）：x-5 ≠ 0 ⇒ x ≠ 5。
取交集：[-3, 5) ∪ (5, ∞)。

**2.**
配方法：

f(x) = (x² - 6x + 9) + 1 = (x-3)² + 1

因为 (x-3)² ≥ 0，所以 f(x) ≥ 1。
最小值在 x = 3 处，f(3) = 1。
值域为 [1, ∞)。

**3.**
定义域：4 - x² > 0 ⇒ x² < 4 ⇒ -2 < x < 2，即 (-2, 2)。

值域：令 u = 4 - x²，x ∈ (-2, 2)，则 u ∈ (0, 4]。
f(x) = ln u，u ∈ (0, 4]。
ln u 在 (0, 4] 上递增，最小趋近于 -∞（u → 0⁺），最大为 ln 4（u = 4）。
值域为 (-∞, ln 4]。

**4.**
条件 1（分母根号内）：2x-1 > 0 ⇒ x > 1/2。
条件 2（对数真数）：5 - x > 0 ⇒ x < 5。
取交集：(1/2, 5)。

**5.**
**不是函数**。例如 x = 0 时，y = ±√(9 - 0) = ±3，一个 x 对应两个 y 值。垂直检验线 x = 0 与图形相交于 (0, 3) 和 (0, -3) 两点。

**6.**
分离常数：

f(x) = (3x-1)/(x+2) = [3(x+2) - 7]/(x+2) = 3 - 7/(x+2)

因为 7/(x+2) ≠ 0，所以 f(x) ≠ 3。值域为 R \ {3}。

判断单射：设 f(a) = f(b)：

3 - 7/(a+2) = 3 - 7/(b+2) ⇒ 7/(a+2) = 7/(b+2) ⇒ a+2 = b+2 ⇒ a = b

因此 f 是单射。

### 二、线性与三次函数

**7.**
平行直线斜率相同，m = 3。
点斜式：y - (-1) = 3(x - 2) ⇒ y + 1 = 3x - 6 ⇒ y = 3x - 7。

**8.**
（i）f(1) = 1 - 2 - 5 + 6 = 0，所以 x-1 是因子。

综合除法：

```
    1 |  1   -2   -5    6
      |       1   -1   -6
      --------------------
         1   -1   -6    0
```

商为 x² - x - 6 = (x-3)(x+2)。

因此 f(x) = (x-1)(x-3)(x+2)。

（ii）f(x) = 0 的解为 x = 1, 3, -2。

**9.**
f'(x) = 3x² - 6x - 9 = 3(x² - 2x - 3) = 3(x-3)(x+1)。

令 f'(x) = 0，得 x = -1 或 x = 3。

符号检验：
- x < -1（取 x = -2）：f'(-2) = 3(-5)(-1) = 15 > 0，递增
- -1 < x < 3（取 x = 0）：f'(0) = 3(-3)(1) = -9 < 0，递减
- x > 3（取 x = 4）：f'(4) = 3(1)(5) = 15 > 0，递增

x = -1：递增→递减 → **局部最大值**，f(-1) = -1 - 3 + 9 + 11 = 16。
x = 3：递减→递增 → **局部最小值**，f(3) = 27 - 27 - 27 + 11 = -16。

**10.**
三个根：x = -1, 2, 4。最高次项系数 a = 1 > 0。

符号分析：

| 区间 | x+1 | x-2 | x-4 | 乘积 |
|------|-----|-----|-----|------|
| x < -1 | 负 | 负 | 负 | **负** |
| -1 < x < 2 | 正 | 负 | 负 | **正** |
| 2 < x < 4 | 正 | 正 | 负 | **负** |
| x > 4 | 正 | 正 | 正 | **正** |

f(x) > 0 的解为 -1 < x < 2 或 x > 4。

**11.**
由因式定理，f(-2) = 0：

f(-2) = (-2)³ + k(4) - 5(-2) - 6 = -8 + 4k + 10 - 6 = 4k - 4 = 0

k = 1。

综合除法除以 (x+2)：

```
    -2 |  1    1   -5   -6
       |     -2    2    6
       -------------------
          1   -1   -3    0
```

商为 x² - x - 3。

因此 f(x) = (x+2)(x² - x - 3)。二次式不可进一步有理分解。

### 三、指数与对数

**12.**

log_3 54 - log_3 2 = log_3 (54/2) = log_3 27 = 3

3 + log_3 (1/3) = log_3 (27 × 1/3) = log_3 9 = 2

值为 2。

**13.**

2^(x+1) = 5 ⇒ ln(2^(x+1)) = ln 5 ⇒ (x+1) ln 2 = ln 5

x+1 = (ln 5)/(ln 2) ⇒ x = (ln 5)/(ln 2) - 1

**14.**

log_3[(x+2)(x-4)] = 2 ⇒ (x+2)(x-4) = 3² = 9

x² - 2x - 8 = 9 ⇒ x² - 2x - 17 = 0

x = [2 ± √(4 + 68)] / 2 = (2 ± √72)/2 = (2 ± 6√2)/2 = 1 ± 3√2

检查定义域：x+2 > 0 且 x-4 > 0 ⇒ x > 4。

1 + 3√2 ≈ 5.24 > 4，有效。
1 - 3√2 ≈ -3.24 < 4，舍去。

因此 x = 1 + 3√2。

**15.**
令 u = 3^x > 0，则 3^(2x) = (3^x)² = u²。

u² - 10u + 9 = 0 ⇒ (u-1)(u-9) = 0 ⇒ u = 1 或 u = 9

3^x = 1 ⇒ x = 0。
3^x = 9 ⇒ x = 2。

解为 x = 0 或 x = 2。

**16.**
使用换底公式，全部换为自然对数：

log_2 3 = ln 3 / ln 2， log_3 4 = ln 4 / ln 3， log_4 5 = ln 5 / ln 4， log_5 2 = ln 2 / ln 5

乘积为：

(ln 3 / ln 2) × (ln 4 / ln 3) × (ln 5 / ln 4) × (ln 2 / ln 5) = 1

值为 1（所有项抵消）。

**17.**
水平渐近线：x → -∞ 时 e^x → 0，2e^x - 3 → -3，渐近线为 y = -3。

y 截距：f(0) = 2e⁰ - 3 = 2 - 3 = -1，即 (0, -1)。

x 截距：2e^x - 3 = 0 ⇒ e^x = 3/2 ⇒ x = ln(3/2)，即 (ln(3/2), 0)。

**18.**
3^x < 7 ⇒ ln(3^x) < ln 7 ⇒ x ln 3 < ln 7 ⇒ x < (ln 7)/(ln 3)。

**19.**
log_a 21 = log_a (3 × 7) = log_a 3 + log_a 7 = p + q。

log_a (7/3) = log_a 7 - log_a 3 = q - p。

**20.**
用换底公式将 log_4 x 换为以 2 为底：

log_4 x = (log_2 x) / (log_2 4) = (log_2 x)/2

设 u = log_2 x，则原方程化为：

u + u/2 = 3 ⇒ (3u)/2 = 3 ⇒ u = 2

log_2 x = 2 ⇒ x = 2² = 4。

### 四、反函数与复合函数

**21.**
y = (3x-2)/4 ⇒ 4y = 3x - 2 ⇒ 3x = 4y + 2 ⇒ x = (4y+2)/3。

交换得 f⁻¹(x) = (4x+2)/3。

**22.**
配方法：f(x) = (x+1)² - 1，x ≥ -1。值域为 [-1, ∞)。

令 y = (x+1)² - 1 ⇒ y+1 = (x+1)² ⇒ x+1 = √(y+1)（因 x ≥ -1，取正根）。

x = √(y+1) - 1。

交换得 f⁻¹(x) = √(x+1) - 1，定义域为 [-1, ∞)。

**23.**
fg(x) = f(g(x)) = f(1/x) = 2(1/x) + 1 = 2/x + 1，x ≠ 0。

gf(x) = g(f(x)) = g(2x+1) = 1/(2x+1)。

gf(x) 的定义域：2x+1 ≠ 0 ⇒ x ≠ -1/2，即 R \ {-1/2}。

**24.**
y = e^(3x) ⇒ ln y = 3x ⇒ x = (1/3) ln y。

交换得 f⁻¹(x) = (1/3) ln x，定义域 x > 0。

**25.**
y = ln(x+2) ⇒ e^y = x+2 ⇒ x = e^y - 2。

交换得 f⁻¹(x) = e^x - 2。

原函数值域为 R，所以 f⁻¹ 的定义域为 R。

验证：f(f⁻¹(x)) = ln(e^x - 2 + 2) = ln(e^x) = x。✓

**26.**
f(x) = x⁴ **不是单射**，因为存在不同的 x 值对应同一个 y 值。例如 f(2) = 16 且 f(-2) = 16，即 2 ≠ -2 但 f(2) = f(-2)。水平检验线 y = 16 与 y = x⁴ 的图形相交于 (2, 16) 和 (-2, 16) 两点。因此 f 没有反函数。

> 若将定义域限制为 x ≥ 0，则反函数为 f⁻¹(x) = ∜x。

**27.**
fg(x) = f(g(x)) = √((x² - 4) + 1) = √(x² - 3)。

定义域：f(x) = √(x+1) 的定义域为 x+1 ≥ 0 ⇒ x ≥ -1。

所以 g(x) ≥ -1 ⇒ x² - 4 ≥ -1 ⇒ x² ≥ 3 ⇒ |x| ≥ √3。

定义域为 (-∞, -√3] ∪ [√3, ∞)。

**28.**
f(x) = x²，x ≥ 0，定义域 [0, ∞)。
g(x) = 2x + 1，定义域 R。

gf(x) = g(f(x)) = 2x² + 1。

gf 的定义域：x 必须在 f 的定义域内（x ≥ 0），且 f(x) 必须在 g 的定义域内（R，无限制）。

因此 Domain(gf) = [0, ∞)。

Domain(f) = [0, ∞)，所以 Domain(gf) ⊆ Domain(f) 成立（实际上两者相等）。✓

### 五、绝对值函数

**29.**
V 形，尖点在 (2, 0)。
x ≥ 2 时 y = x-2；x < 2 时 y = 2-x。

解 |x-2| = 3：
情况 1：x-2 = 3 ⇒ x = 5
情况 2：x-2 = -3 ⇒ x = -1

解为 x = 5 或 x = -1。

**30.**
|2x+1| < 5 ⇒ -5 < 2x+1 < 5。

左边：-5 < 2x+1 ⇒ -6 < 2x ⇒ -3 < x。
右边：2x+1 < 5 ⇒ 2x < 4 ⇒ x < 2。

取交集：-3 < x < 2。

**31.**
y = |cos x| 在 [0, 2π] 上：
- [0, π/2]：cos x ≥ 0，从 (0,1) 下降到 (π/2, 0)
- [π/2, 3π/2]：cos x ≤ 0，翻折到上方：从 (π/2, 0) 上升到 (π, 1) 再下降到 (3π/2, 0)
- [3π/2, 2π]：cos x ≥ 0，从 (3π/2, 0) 上升到 (2π, 1)

周期为 π。尖点在 x = π/2, 3π/2 等处。

**32.**
x² - 5x + 6 = (x-2)(x-3)。

情况 1：x² - 5x + 6 = 2 ⇒ x² - 5x + 4 = 0 ⇒ (x-1)(x-4) = 0 ⇒ x = 1 或 x = 4。
检查：x=1 时 1-5+6=2>0，有效。x=4 时 16-20+6=2>0，有效。

情况 2：x² - 5x + 6 = -2 ⇒ x² - 5x + 8 = 0。
Δ = 25 - 32 = -7 < 0，无实数解。

解为 x = 1 或 x = 4。

**33.**
|x+2| ≥ 3 ⇒ x+2 ≤ -3 或 x+2 ≥ 3。

x+2 ≤ -3 ⇒ x ≤ -5。
x+2 ≥ 3 ⇒ x ≥ 1。

解为 x ≤ -5 或 x ≥ 1。

**34.**
几何解释：|x-2| 是 x 到 2 的距离，|x+1| = |x-(-1)| 是 x 到 -1 的距离。f(x) 是这两段距离之和。

数轴上点 -1 到 2 的距离为 3。当 x 在 [-1, 2] 之间时，两距离之和恒等于 3。当 x < -1 或 x > 2 时，和大于 3。

因此最小值为 3，在 x ∈ [-1, 2] 时取到。

代数验证：

f(x) = {
  -(x-2) - (x+1) = -2x + 1,  x < -1
  -(x-2) + (x+1) = 3,        -1 ≤ x ≤ 2
  (x-2) + (x+1) = 2x - 1,     x > 2
}

当 x < -1 时，f(x) = -2x + 1 > 3。
当 -1 ≤ x ≤ 2 时，f(x) = 3。
当 x > 2 时，f(x) = 2x - 1 > 3。

最小值为 3。

### 六、三角函数绝对值

**35.**
y = 2 cos x + 1 在 [0, 2π] 上：
- 最大值：2(1) + 1 = 3（x = 0, 2π）
- 最小值：2(-1) + 1 = -1（x = π）
- 零点：2 cos x + 1 = 0 ⇒ cos x = -1/2 ⇒ x = 2π/3, 4π/3

取绝对值后：
- [2π/3, 4π/3] 区间内 2 cos x + 1 ≤ 0，翻折到上方
- 其余部分保持不变
- 尖点：x = 2π/3 和 x = 4π/3
- 翻折后最大值出现在 x = π 处，|2 cos π + 1| = |-2+1| = 1
- 原最大值 x = 0 处 3 和 x = 2π 处 3 保持不变

值域：[0, 3]。

**36.**
y = |tan x| 在 (-π/2, π/2) 上：

- (-π/2, 0)：tan x < 0，绝对值后翻折到上方，|tan x| = -tan x
- (0, π/2)：tan x > 0，保持不变，|tan x| = tan x
- x = 0：tan 0 = 0，为尖点

**渐近线**：x = -π/2 和 x = π/2 仍然是垂直渐近线（绝对值不改变渐近线位置）。

图形特征：
- 在 x = 0 处有尖点
- 在 x → ±π/2 时，|tan x| → ∞
- 值域：[0, ∞)
- 图形关于 x = 0 对称（偶函数），因为 |tan(-x)| = |-tan x| = |tan x|

**37.**
f(x) = |3 sin 2x - 2|，x ∈ [0, π]。

先分析 y = 3 sin 2x - 2：
- 振幅 3，周期 π，垂直下移 2
- 最大值：3(1) - 2 = 1，最小值：3(-1) - 2 = -5
- 零点：3 sin 2x - 2 = 0 ⇒ sin 2x = 2/3
  2x = arcsin(2/3) 或 2x = π - arcsin(2/3)
  记 α = (1/2) arcsin(2/3) ≈ 0.364 弧度
  则 x = α 或 x = π/2 - α

在 [0, π] 上，3 sin 2x - 2 在 [α, π/2 - α] 区间为负，翻折到上方。

最大值：翻折后，原最小值 -5（x = 3π/4）变为 5。所以 f(x) 的最大值为 5。
最小值：0（在零点 x = α 和 x = π/2 - α 处）。

因此 f(x) 在 [0, π] 上的最大值为 5，最小值为 0。

### 七、定义域限制与复合函数存在

**38.**
f(x) = √(x-2)，定义域 [2, ∞)。
g(x) = 1/√(5-x)，定义域 x < 5。

gf(x) = g(f(x)) = 1 / √(5 - √(x-2))。

定义域条件：
1. f 的定义域：x ≥ 2
2. f(x) 在 g 的定义域内：
   - 5 - √(x-2) > 0（分母根号内为正）
   - √(x-2) < 5 ⇒ x-2 < 25 ⇒ x < 27
   - 5 - √(x-2) ≠ 0 已由 >0 保证

取交集：2 ≤ x < 27。

验证 Domain(gf) ⊆ Domain(f)：
Domain(f) = [2, ∞)，Domain(gf) = [2, 27) ⊂ [2, ∞)。✓

---

> **复习建议**：函数是 IGCSE 0606 附加数学的基石——微分、积分、曲线草图、运动学都建立在函数概念之上。本章的重点是：
>
> 1. 熟练掌握定义域和值域的计算（尤其是根号、分母、对数同时出现时）
> 2. 深刻理解指数与对数的互逆关系（a^(log_a x) = x，log_a(a^x) = x）
> 3. 掌握对数运算法则的灵活运用（特别是换底公式 log_a M = (log_b M)/(log_b a)）
> 4. 熟练求反函数和复合函数，注意定义域的变化
> 5. 能够画出 |f(x)| 的变换图形（线性、二次、三次、三角 a sin(bx)+c、a cos(bx)+c、a tan(bx)+c）
> 6. 能用文字准确解释函数没有反函数的原因（考纲 1.5）
> 7. 理解 Domain(gf) ⊆ Domain(f) 和 Range(gf) ⊆ Range(g)（考纲 1.2）

---
---

根据您的要求，我已将第 5 章（微分）的原始内容重新编译为纯文本 + Unicode 格式。保留所有文字、例题、公式和答案，仅将 LaTeX 指令替换为 Unicode 字符或简单文本，不使用 `\binom`、`\frac`、`\mathbf{i} = \begin{pmatrix} ... \end{pmatrix}` 等不符合要求的语法。积分、导数、函数专用符号（如 `∫`, `d/dx`, `lim`, `∑`, `√`, `sin`, `cos`, `tan` 等）使用 Unicode 或标准文字表示。

输出如下：

---

# 第 5 章：微分（导数）

## 考纲对照

本章内容覆盖 Cambridge IGCSE Additional Mathematics (0606) 2028–2030 考纲 第 14 单元 Calculus 中的以下条目：

| 考纲条目 | 内容 | 本节对应 |
|---------|------|---------|
| 14.1 | 理解导函数的概念（非正式极限理解，不考第一原理） | 5.1 |
| 14.2 | 使用记号 f'(x), f''(x), dy/dx, d²y/dx², δx, δx → 0 | 5.1 |
| 14.3 | 已知并使用标准函数的导数：xⁿ（任意有理数 n）、sin x、cos x、tan x、eˣ、ln x（含常数倍、和差、复合函数） | 5.2, 5.3 |
| 14.4 | 积法则与商法则 | 5.4 |
| 14.5 | 求切线（tangent）与法线（normal） | 5.5 |
| 14.6 | 求驻点（stationary points），不含拐点 | 5.6 |
| 14.7 | 相关变化率（connected rates of change）、微小增量与近似（small increments and approximations） | 5.7 |
| 14.8 | 实际最值问题 | 5.8 |
| 14.9 | 用一阶和二阶导数判别法区分极大值与极小值 | 5.6 |

核心要求：三角函数的角度始终使用弧度制。不考从第一原理（first principles）求导。不考拐点（points of inflexion）。二阶导数判别法要求能完整证明结论。

---

## 引言

微分（differentiation）是微积分的两大核心运算之一。它的任务是量化变化——具体来说，是量化函数在任意一点上的瞬时变化率。

想象你正开车行驶在一条蜿蜒的公路上。速度表上显示的数值就是瞬时速度——它告诉你在这一刹那车子变化得有多快。微分所做的，正是为任何函数计算出这种"瞬时速度"。在几何上，导数给出的是曲线在某一点的切线斜率，也就是曲线在该点"有多陡"。

为什么要学微分？因为自然界中几乎一切都在变化：物体的运动、人口的增减、温度的升降、利润的涨落。微分给了我们一把精确描述这些变化的数学工具。掌握了微分，后续的积分（求累积量）、最优化（求最佳方案）、运动学分析等问题都将迎刃而解。

本章将从导数的基本概念出发，依次学习基本求导公式、链式法则、积法则与商法则，然后将这些工具应用于切线与法线、极值判断、相关变化率以及实际最值问题。每个知识点配有丰富的例题和练习题，帮助你完全掌握。

---

## 5.1 导数概念与记号

### 5.1.1 从平均变化率到瞬时变化率

变化率是一个我们非常熟悉的概念。例如，一辆汽车在 2 小时内行驶了 120 公里，那么它的平均速度就是：

平均速度 = 120/2 = 60 km/h

但这个平均速度掩盖了细节——汽车可能在有些时刻开得快，有些时刻开得慢。如果我们想知道在某个精确时刻的速度，就需要瞬时变化率。

设函数 y = f(x)。考虑从 x 到 x + δx 的一个小区间（其中 δx 读作 "delta x"，表示 x 的一个微小变化量）。在这个区间上，函数的平均变化率为：

(函数值的变化量)/(自变量的变化量) = (f(x + δx) - f(x))/(δx)

当 δx 趋近于 0 时，这个平均变化率就会趋近于一个极限值——这就是函数在点 x 处的导数：

f'(x) = lim_{δx→0} [f(x + δx) - f(x)] / δx

这里 lim_{δx→0} 表示"当 δx 无限趋近于 0 时"。这个极限的存在性（即导数是否存在）取决于函数在该点是否"光滑"。

### 5.1.2 导数的几何意义

从几何角度看，导数 f'(a) 就是曲线 y = f(x) 在点 (a, f(a)) 处切线的斜率。

- 如果 f'(a) > 0，曲线在该点上升（切线向右上方倾斜）。
- 如果 f'(a) < 0，曲线在该点下降（切线向右下方倾斜）。
- 如果 f'(a) = 0，曲线在该点水平（可能是极大值、极小值或鞍点）。

### 5.1.3 记号

导数的记号有多种，考试中常见的有：

| 记号 | 名称 | 示例 |
|------|------|------|
| f'(x) | 拉格朗日记法 | f'(x) = 2x |
| dy/dx | 莱布尼茨记法 | dy/dx = 2x |
| (d/dx) f(x) | 算子记法 | (d/dx)(x²) = 2x |
| f''(x), d²y/dx² | 二阶导数 | 导数的导数 |

⚠️ 重要理解：记号 dy/dx 并不是一个分数，而是一个整体符号——它表示"对 x 求导"这个运算的结果。但在微小增量近似中，我们可以把它当作一个"比值"来使用（δy ≈ (dy/dx)·δx），这在线性近似中非常有效。

### 5.1.4 极限的直观理解

在求导过程中，我们经常碰到 0/0 型的不定式。处理方法通常是因式分解后约分再代入。

示例：求 lim_{x→2} (x² - 4)/(x - 2)。

当 x = 2 时，分子分母都是 0，但我们可以这样做：

lim_{x→2} (x² - 4)/(x - 2) = lim_{x→2} [(x-2)(x+2)]/(x-2) = lim_{x→2} (x+2) = 4

注意：x 趋近于 2，但从不等于 2，所以约分 x-2 是合法的。

---

### 例题 5.1A（导数概念的直观理解）

已知 f(x) = x²，用极限定义求 f'(2)。

解：

f'(2) = lim_{δx→0} [f(2 + δx) - f(2)] / δx = lim_{δx→0} [(2 + δx)² - 4] / δx

展开 (2 + δx)² = 4 + 4δx + (δx)²，代入：

f'(2) = lim_{δx→0} (4 + 4δx + (δx)² - 4) / δx = lim_{δx→0} (4δx + (δx)²) / δx = lim_{δx→0} (4 + δx)

当 δx → 0 时，4 + δx → 4，所以 f'(2) = 4。

几何意义：抛物线 y = x² 在点 (2, 4) 处的切线斜率为 4。

---

### 例题 5.1B（平均变化率与瞬时变化率的对比）

物体自由落体的位移函数为 s(t) = 5t²（s 以米为单位，t 以秒为单位）。
(a) 求 t = 2 到 t = 2.1 之间的平均速度。
(b) 求 t = 2 时的瞬时速度。

解：

(a) 平均速度 = [s(2.1) - s(2)] / 0.1 = [5×4.41 - 5×4] / 0.1 = (22.05 - 20)/0.1 = 20.5 m/s

(b) 瞬时速度。先求导数的一般形式：

s'(t) = lim_{δt→0} [5(t + δt)² - 5t²] / δt = lim_{δt→0} [5(t² + 2tδt + (δt)²) - 5t²] / δt
= lim_{δt→0} (10tδt + 5(δt)²) / δt = lim_{δt→0} (10t + 5δt) = 10t

代入 t = 2：s'(2) = 10×2 = 20 m/s。

注意：平均速度 20.5 m/s 非常接近瞬时速度 20 m/s——区间越小，两者越接近。

---

### 例题 5.1C（导数值与切线斜率的关系）

曲线 y = 1/x 在点 (2, 1/2) 处的切线斜率是多少？曲线在该点是上升还是下降？

解：

f'(x) = lim_{δx→0} [1/(x+δx) - 1/x] / δx = lim_{δx→0} [(x - (x+δx))/(x(x+δx))] / δx
= lim_{δx→0} (-δx) / (x(x+δx)δx) = lim_{δx→0} (-1)/(x(x+δx)) = -1/x²

代入 x = 2：f'(2) = -1/4。

斜率为负，说明曲线在 x = 2 处下降（随着 x 增大，y 减小）。

---

### 例题 5.1D（极限计算——约分法）

求 lim_{x→3} (x² - 2x - 3)/(x - 3)。

解：

当 x = 3 时，分子 3² - 2(3) - 3 = 9 - 6 - 3 = 0，分母也为 0。因式分解分子：

x² - 2x - 3 = (x - 3)(x + 1)

所以：

lim_{x→3} (x² - 2x - 3)/(x - 3) = lim_{x→3} [(x - 3)(x + 1)]/(x - 3) = lim_{x→3} (x + 1) = 4

---

### 练习题 5.1

1. 用极限定义求 f(x) = x² + 2x 在 x = 1 处的导数。

2. 物体位移 s(t) = 2t² + 3t（t ≥ 0），求 t = 3 时的瞬时速度。

3. 求 lim_{x→4} (x² - 16)/(x - 4)。

---

## 5.2 基本求导公式

有了导数的概念，我们现在需要一套高效的求导工具，而不是每次都用极限定义来计算。以下是最基本的求导公式，必须熟练掌握。

### 5.2.1 幂函数求导公式的推导

对于 f(x) = xⁿ，其中 n 为正整数，我们先用二项式定理来推导。

由导数定义：

f'(x) = lim_{δx→0} [(x + δx)ⁿ - xⁿ] / δx

根据二项式定理：

(x + δx)ⁿ = xⁿ + n xⁿ⁻¹ δx + [n(n-1)/2] xⁿ⁻² (δx)² + ... + (δx)ⁿ

代入：

f'(x) = lim_{δx→0} [n xⁿ⁻¹ δx + (n(n-1)/2) xⁿ⁻² (δx)² + ... + (δx)ⁿ] / δx
= lim_{δx→0} [n xⁿ⁻¹ + (n(n-1)/2) xⁿ⁻² δx + ... + (δx)ⁿ⁻¹]

当 δx → 0 时，除第一项外所有项都趋于 0，因此：

(d/dx)(xⁿ) = n xⁿ⁻¹

这个公式不仅对正整数成立，对任意有理数 n 都成立。这是考纲明确要求的。

下表展示了常见情形：

| f(x) | 改写为 xⁿ 形式 | f'(x) | 说明 |
|------|---------------|-------|------|
| x² | x² | 2x | n=2 |
| x³ | x³ | 3x² | n=3 |
| x | x¹ | 1 | n=1 |
| 1 | x⁰ | 0 | n=0 |
| √x | x^(1/2) | (1/2)x^(-1/2) = 1/(2√x) | n = 1/2 |
| 1/x | x⁻¹ | -x⁻² = -1/x² | n = -1 |
| 1/x² | x⁻² | -2x⁻³ = -2/x³ | n = -2 |
| ∛x | x^(1/3) | (1/3)x^(-2/3) = 1/(3∛(x²)) | n = 1/3 |

### 5.2.2 常数倍与和/差法则

函数的线性组合求导非常简单：

- 常数倍法则： (d/dx)[c·f(x)] = c·f'(x)
  推导：lim_{δx→0} [c f(x+δx) - c f(x)] / δx = c·lim_{δx→0} [f(x+δx)-f(x)]/δx = c f'(x)

- 和法则： (d/dx)[f(x) + g(x)] = f'(x) + g'(x)
  推导：lim_{δx→0} [(f(x+δx)+g(x+δx)) - (f(x)+g(x))] / δx = f'(x) + g'(x)

- 差法则： (d/dx)[f(x) - g(x)] = f'(x) - g'(x)

示例：f(x) = 3x² - 4x + 5

f'(x) = 3·(2x) - 4·(1) + 0 = 6x - 4

### 5.2.3 三角函数的导数

核心条件：所有三角函数的角度必须使用弧度制。

为什么必须用弧度？因为在弧度制下，lim_{θ→0} (sin θ)/θ = 1。这个极限是三角函数求导的基础。如果使用角度制，这个极限会多出一个因子 π/180，导数公式就不再简洁了。

sin x 导数的推导：

(d/dx)(sin x) = lim_{δx→0} [sin(x+δx) - sin x] / δx

使用三角恒等式 sin(A+B) = sin A cos B + cos A sin B：

= lim_{δx→0} [sin x cos(δx) + cos x sin(δx) - sin x] / δx
= lim_{δx→0} [ sin x·(cos(δx)-1)/δx + cos x·(sin(δx))/δx ]

利用两个重要极限：lim_{θ→0} (sin θ)/θ = 1 和 lim_{θ→0} (cos θ - 1)/θ = 0，得到：

(d/dx)(sin x) = sin x·0 + cos x·1 = cos x

类似地可以推导 (d/dx)(cos x) = -sin x。

对于 tan x，我们利用 tan x = sin x / cos x 和商法则推导（见 5.4 节）。

标准公式汇总：

(d/dx)(sin x) = cos x
(d/dx)(cos x) = -sin x
(d/dx)(tan x) = sec² x

### 5.2.4 指数函数与对数函数的导数

(d/dx)(eˣ) = eˣ

这是微积分中最优美的公式之一——eˣ 的导数就是它本身。从几何上看，这意味着曲线 y = eˣ 在任意一点处的切线斜率都等于该点的函数值。

对于一般的指数函数 aˣ（a>0, a≠1）：

(d/dx)(aˣ) = aˣ ln a

推导过程：将 aˣ 写成 e^(ln(aˣ)) = e^(x ln a)，然后使用链式法则：

(d/dx)(aˣ) = (d/dx)(e^(x ln a)) = e^(x ln a)·ln a = aˣ ln a

对于自然对数：

(d/dx)(ln x) = 1/x

对于一般底数的对数：

(d/dx)(log_a x) = 1/(x ln a)

ln x 导数的推导：

设 y = ln x，则 e^y = x。两边对 x 求导（隐函数微分）：

e^y·(dy/dx) = 1  ⇒  dy/dx = 1/e^y = 1/x

---

### 例题 5.2A（多项式求导）

求下列函数的导数：
(a) f(x) = 2x⁵ - 3x³ + 7x - 10
(b) g(x) = (1/3)x⁶ + 4/x² - √x
(c) h(x) = (x+1)(x-2)（先展开再求导）
(d) p(x) = 5x⁴ + 2x⁻³ - 3x^(1/2) + 8

解：

(a) 逐项求导：
f'(x) = 2·5x⁴ - 3·3x² + 7 - 0 = 10x⁴ - 9x² + 7

(b) 先写成幂的形式：4/x² = 4x⁻²，√x = x^(1/2)。

g(x) = (1/3)x⁶ + 4x⁻² - x^(1/2)

g'(x) = (1/3)·6x⁵ + 4·(-2)x⁻³ - (1/2)x^(-1/2)
= 2x⁵ - 8x⁻³ - (1/2)x^(-1/2)

化为分数形式：
g'(x) = 2x⁵ - 8/x³ - 1/(2√x)

(c) 先展开：(x+1)(x-2) = x² - x - 2，然后求导：
h'(x) = 2x - 1

(d)
p'(x) = 5·4x³ + 2·(-3)x⁻⁴ - 3·(1/2)x^(-1/2) + 0
= 20x³ - 6x⁻⁴ - (3/2)x^(-1/2)

---

### 例题 5.2B（三角函数求导）

求下列函数的导数：
(a) f(x) = 3 sin x - 2 cos x
(b) g(x) = tan x + 5
(c) 求 f'(0)，其中 f(x) = sin x - cos x
(d) h(x) = 4 sin x + (1/2) cos x

解：

(a) f'(x) = 3 cos x - 2(-sin x) = 3 cos x + 2 sin x

(b) g'(x) = sec² x + 0 = sec² x

(c) 先求导：f'(x) = cos x + sin x
代入 x = 0：f'(0) = cos 0 + sin 0 = 1 + 0 = 1

(d) h'(x) = 4 cos x + (1/2)(-sin x) = 4 cos x - (1/2) sin x

---

### 例题 5.2C（指数与对数求导）

求下列函数的导数：
(a) f(x) = 4 eˣ - (1/2) ln x
(b) g(x) = 3ˣ + log₂ x
(c) 已知 h(x) = eˣ + ln x，求 h'(1)
(d) p(x) = 5ˣ - 2 eˣ + 3 ln x

解：

(a) f'(x) = 4 eˣ - (1/2)·(1/x) = 4 eˣ - 1/(2x)

(b) 使用公式：(d/dx)(3ˣ) = 3ˣ ln 3，(d/dx)(log₂ x) = 1/(x ln 2)
g'(x) = 3ˣ ln 3 + 1/(x ln 2)

(c) 先求导：h'(x) = eˣ + 1/x
代入 x = 1：h'(1) = e¹ + 1 = e + 1

(d) p'(x) = 5ˣ ln 5 - 2 eˣ + 3·(1/x) = 5ˣ ln 5 - 2 eˣ + 3/x

---

### 例题 5.2D（综合求导——重新表达后再求导）

求下列函数的导数：
(a) f(x) = 2/∛x
(b) g(x) = (2x)³（注意与 2x³ 的区别）

解：

(a) 先改写：2/∛x = 2 x^(-1/3)
f'(x) = 2·(-1/3)x^(-4/3) = -(2/3)x^(-4/3) = -2/(3∛(x⁴))

(b) (2x)³ = 8 x³，所以 g'(x) = 8·3x² = 24x²
注意：如果是 2x³，导数为 6x²，两者不同。

---

### 练习题 5.2

1. 求 f(x) = 4x³ - 2x² + 5x - 7 的导数。

2. 求 g(x) = 3/x² - 1/(2√x) + 6 x^(1/3) 的导数。

3. 求 h(x) = 5 sin x - 3 cos x + 2 tan x 的导数。

4. 求 p(x) = 2 eˣ + 4ˣ - (1/3) ln x 的导数。

---

## 5.3 链式法则（Chain Rule）

### 5.3.1 链式法则的原理

当想要求解复合函数的导数时——比如 y = (2x+1)³ 或 y = sin(3x)——就需要用到链式法则。

链式法则的核心思想是"层层求导，逐层相乘"。设 y 是 u 的函数，而 u 又是 x 的函数，即 y = f(u) 且 u = g(x)，则：

dy/dx = (dy/du)·(du/dx)

用另一种形式写出：如果 y = f(g(x))，那么：

dy/dx = f'(g(x))·g'(x)

即：外层函数对中间变量的导数，乘以中间变量对自变量的导数。

### 5.3.2 链式法则的直观理解

为什么链式法则成立？考虑微小变化量：

- 当 x 变化 δx 时，u = g(x) 变化 δu ≈ g'(x) δx
- 当 u 变化 δu 时，y = f(u) 变化 δy ≈ f'(u) δu

因此：
δy/δx ≈ f'(u)·(δu/δx) ≈ f'(u)·g'(x)

当 δx → 0 时，近似变成精确等式。

### 5.3.3 链式法则的常见应用模式

模式一：y = (ax+b)ⁿ
设 u = ax + b，则 y = uⁿ，dy/du = n uⁿ⁻¹，du/dx = a，所以：
dy/dx = n(ax+b)ⁿ⁻¹·a = a n (ax+b)ⁿ⁻¹

模式二：y = sin(ax+b)
设 u = ax+b，则 y = sin u，dy/du = cos u，du/dx = a，所以：
dy/dx = cos(ax+b)·a = a cos(ax+b)

模式三：y = cos(ax+b)
dy/dx = -sin(ax+b)·a = -a sin(ax+b)

模式四：y = e^(ax+b)
设 u = ax+b，则 y = e^u，dy/du = e^u，du/dx = a，所以：
dy/dx = e^(ax+b)·a = a e^(ax+b)

模式五：y = ln(ax+b)
设 u = ax+b，则 y = ln u，dy/du = 1/u，du/dx = a，所以：
dy/dx = a/(ax+b)

模式六：y = tan(ax+b)
dy/dx = sec²(ax+b)·a = a sec²(ax+b)

### 5.3.4 多层链式法则

当函数有三层甚至更多层复合时，链式法则可以连续使用多次。例如 y = f(g(h(x)))：

dy/dx = f'(g(h(x)))·g'(h(x))·h'(x)

从最外层开始，逐层向内求导，每层相乘。

---

### 例题 5.3A（多项式复合函数）

求下列函数的导数：
(a) y = (3x - 2)⁵
(b) y = 1/(2x+1)³
(c) y = √(4x - 1)
(d) y = (5 - 2x)⁻⁴

解：

(a) 令 u = 3x - 2，则 y = u⁵。
dy/dx = 5u⁴·3 = 5(3x-2)⁴·3 = 15(3x-2)⁴

(b) 写成 y = (2x+1)⁻³，令 u = 2x+1。
dy/dx = (-3)u⁻⁴·2 = -6(2x+1)⁻⁴ = -6/(2x+1)⁴

(c) 写成 y = (4x-1)^(1/2)，令 u = 4x-1。
dy/dx = (1/2)u^(-1/2)·4 = 2/√(4x-1)

(d) 令 u = 5 - 2x，则 y = u⁻⁴。
dy/dx = (-4)u⁻⁵·(-2) = 8(5-2x)⁻⁵ = 8/(5-2x)⁵

---

### 例题 5.3B（三角与指数复合函数）

求下列函数的导数：
(a) y = sin(2x + π/3)
(b) y = e^(-3x + 1)
(c) y = tan(5x)
(d) y = cos(x/2)

解：

(a) 令 u = 2x + π/3，则 y = sin u。
dy/dx = cos u·2 = 2 cos(2x + π/3)

(b) 令 u = -3x + 1，则 y = e^u。
dy/dx = e^u·(-3) = -3 e^(-3x+1)

(c) 令 u = 5x，则 y = tan u。
dy/dx = sec² u·5 = 5 sec²(5x)

(d) 令 u = x/2，则 y = cos u。
dy/dx = -sin u·(1/2) = -(1/2) sin(x/2)

---

### 例题 5.3C（对数复合与多层链式）

求下列函数的导数：
(a) y = ln(3x² + 1)
(b) y = e^(sin x)
(c) y = sin³ x（即 (sin x)³）
(d) y = √(cos x)

解：

(a) 令 u = 3x² + 1，则 y = ln u。
dy/dx = (1/u)·6x = 6x/(3x²+1)

(b) 令 u = sin x，则 y = e^u。
dy/dx = e^u·cos x = e^(sin x)·cos x

(c) 这里有两层复合：令 u = sin x，y = u³，则：
dy/dx = 3u²·cos x = 3 sin² x·cos x

(d) 写成 y = (cos x)^(1/2)，令 u = cos x，y = u^(1/2)。
dy/dx = (1/2)u^(-1/2)·(-sin x) = -sin x / (2√(cos x))

---

### 例题 5.3D（三层链式法则）

求 y = sin²(3x) 的导数。

解：

这里有三层复合：y = (sin(3x))²

令 v = 3x，u = sin v，y = u²。

dy/dx = (dy/du)·(du/dv)·(dv/dx) = (2u)·(cos v)·(3)
= 2 sin(3x)·cos(3x)·3 = 6 sin(3x) cos(3x) = 3 sin(6x)

（最后一步使用了倍角公式 sin 2θ = 2 sin θ cos θ）

---

### 练习题 5.3

1. 求 y = (5x + 2)⁴ 的导数。

2. 求 y = 1/√(3x - 1) 的导数。

3. 求 y = e^(2x-3) 的导数。

4. 求 y = ln(x² + 4) 的导数。

5. 求 y = cos³(2x) 的导数。

---

## 5.4 积法则与商法则

当两个函数相乘或相除时，它们的导数不能简单地对每个部分分别求导再相乘或相除。这时需要专门的法则。

### 5.4.1 积法则（Product Rule）

设 y = u·v，其中 u 和 v 都是 x 的函数，则：

dy/dx = u·(dv/dx) + v·(du/dx)

或简记为：(uv)' = uv' + vu'

记忆口诀："前导后不导 + 后导前不导"——第一个函数求导乘以第二个函数不动，加上第二个函数求导乘以第一个函数不动。

积法则的详细推导：

从导数的极限定义出发：

(uv)' = lim_{δx→0} [u(x+δx)v(x+δx) - u(x)v(x)] / δx

在分子中巧妙地加减 u(x+δx)v(x)：

= lim_{δx→0} [u(x+δx)v(x+δx) - u(x+δx)v(x) + u(x+δx)v(x) - u(x)v(x)] / δx
= lim_{δx→0} [ u(x+δx)·(v(x+δx)-v(x))/δx + v(x)·(u(x+δx)-u(x))/δx ]

当 δx → 0 时，u(x+δx) → u(x)，于是：
(uv)' = u(x)·v'(x) + v(x)·u'(x) = uv' + vu'

### 5.4.2 商法则（Quotient Rule）

设 y = u/v，其中 u 和 v 都是 x 的函数，且 v ≠ 0，则：

dy/dx = [v·(du/dx) - u·(dv/dx)] / v²

或简记为：(u/v)' = (vu' - uv') / v²

记忆口诀："上导下不导减下导上不导，除以分母的平方"。

商法则的推导（从积法则导出）：

将 u/v 写成 u·v⁻¹，然后用积法则和链式法则：

(d/dx)(u/v) = (d/dx)(u·v⁻¹) = u·(d/dx)(v⁻¹) + v⁻¹·(du/dx)
= u·(-1)v⁻²·(dv/dx) + (1/v)·(du/dx)
= -(u/v²)(dv/dx) + (1/v)(du/dx)

通分：
= [v(du/dx) - u(dv/dx)] / v²

---

### 例题 5.4A（积法则基础）

求下列函数的导数：
(a) y = (x² + 1)(x³ - 2x)
(b) y = x sin x
(c) y = eˣ cos x
(d) y = x² ln x

解：

(a) 设 u = x² + 1，v = x³ - 2x。
则 u' = 2x，v' = 3x² - 2。

y' = uv' + vu' = (x²+1)(3x²-2) + (x³-2x)(2x)
展开：
= 3x⁴ - 2x² + 3x² - 2 + 2x⁴ - 4x² = 5x⁴ - 3x² - 2

（也可先展开原式再求导来验证）

(b) 设 u = x，v = sin x，则 u' = 1，v' = cos x。
y' = x cos x + sin x·1 = x cos x + sin x

(c) 设 u = eˣ，v = cos x，则 u' = eˣ，v' = -sin x。
y' = eˣ·(-sin x) + cos x·eˣ = eˣ(cos x - sin x)

(d) 设 u = x²，v = ln x，则 u' = 2x，v' = 1/x。
y' = x²·(1/x) + ln x·2x = x + 2x ln x

---

### 例题 5.4B（商法则基础）

求下列函数的导数：
(a) y = x/(x+1)
(b) y = x²/sin x
(c) y = eˣ/(x²+1)
(d) y = (ln x)/x

解：

(a) 设 u = x，v = x+1，则 u' = 1，v' = 1。
y' = (vu' - uv')/v² = ((x+1)·1 - x·1)/(x+1)² = (x+1-x)/(x+1)² = 1/(x+1)²

(b) 设 u = x²，v = sin x，则 u' = 2x，v' = cos x。
y' = (sin x·2x - x²·cos x) / sin² x = (2x sin x - x² cos x) / sin² x

(c) 设 u = eˣ，v = x²+1，则 u' = eˣ，v' = 2x。
y' = ((x²+1)eˣ - eˣ·2x) / (x²+1)² = eˣ(x²+1-2x) / (x²+1)² = eˣ(x-1)² / (x²+1)²

(d) 设 u = ln x，v = x，则 u' = 1/x，v' = 1。
y' = (x·(1/x) - ln x·1) / x² = (1 - ln x) / x²

---

### 例题 5.4C（积法则与商法则综合）

(a) 已知 y = (x²+1) ln x，求 dy/dx。
(b) 已知 y = (sin x)/eˣ，求 dy/dx。
(c) 已知 y = tan x，用 tan x = sin x/cos x 及商法则验证 (d/dx)(tan x) = sec² x。
(d) 求 y = (2x-1)/(x²+3) 的导数。

解：

(a) 积法则。设 u = x²+1，v = ln x，则 u' = 2x，v' = 1/x。
dy/dx = (x²+1)·(1/x) + ln x·2x = (x²+1)/x + 2x ln x = x + 1/x + 2x ln x

(b) 商法则。设 u = sin x，v = eˣ，则 u' = cos x，v' = eˣ。
dy/dx = (eˣ cos x - sin x·eˣ) / (eˣ)² = eˣ(cos x - sin x) / e^(2x) = (cos x - sin x)/eˣ

(c) 设 u = sin x，v = cos x，则 u' = cos x，v' = -sin x。
(d/dx)(sin x/cos x) = (cos x·cos x - sin x·(-sin x)) / cos² x
= (cos² x + sin² x) / cos² x

由三角恒等式 sin² x + cos² x = 1：
(d/dx)(tan x) = 1/cos² x = sec² x
验证完毕。

(d) 设 u = 2x-1，v = x²+3，则 u' = 2，v' = 2x。
y' = [(x²+3)·2 - (2x-1)·2x] / (x²+3)²
= (2x²+6 - 4x² + 2x) / (x²+3)²
= (-2x² + 2x + 6) / (x²+3)²
= -2(x² - x - 3) / (x²+3)²

---

### 练习题 5.4

1. 求 y = x² eˣ 的导数。

2. 求 y = 3x/(x-2) 的导数。

3. 求 y = x cos x 的导数。

4. 求 y = (x+1)/(x²+1) 的导数。

5. 求 y = eˣ sin x 的导数。

---

## 5.5 切线与法线

### 5.5.1 基础知识

给定一条光滑曲线 y = f(x) 及其上一点 P(a, f(a))：

- 切线（Tangent）：过点 P 且斜率为 f'(a) 的直线。切线是曲线在该点处的最佳线性逼近。
- 法线（Normal）：过点 P 且与切线垂直的直线。

### 5.5.2 标准三步法（已知切点）

当题目明确说"在点 P 处的切线"时，P 就是切点。求解步骤如下：

1. 求切点坐标：确定 a，计算 f(a)，得到 (a, f(a))。
2. 求切线斜率：m = f'(a)。
3. 写切线方程：使用点斜式 y - y₀ = m(x - x₀)：

y - f(a) = f'(a)(x - a)

法线的斜率 m⊥ 满足 m·m⊥ = -1（当 m ≠ 0 时），即 m⊥ = -1/f'(a)。法线方程为：

y - f(a) = (-1/f'(a))(x - a)

特殊情况：
- 若 f'(a) = 0（切线水平），则法线为竖直线 x = a。
- 若 f'(a) 不存在（如尖点），则切线竖直，法线水平。

### 5.5.3 为什么切线斜率等于导数？

从几何上看，曲线上两点 (a, f(a)) 和 (a+δx, f(a+δx)) 的连线斜率为 [f(a+δx)-f(a)]/δx。当 δx 趋近于 0 时，这条连线趋近于切线，其斜率趋近于导数 f'(a)。

从代数上看，切线方程 y = f(a) + f'(a)(x-a) 在 x=a 处与曲线有相同的函数值和相同的一阶导数，因此是"最佳线性逼近"。

### 5.5.4 重要陷阱：切点未知的情形

如果题目说"经过点 P 的切线"（而非"在点 P 处"），那么 P 可能不是切点。此时需要：

1. 设切点为 (a, f(a))，a 为未知数。
2. 写出切线方程：y - f(a) = f'(a)(x - a)。
3. 将 P 的坐标代入，得到关于 a 的方程，解出所有可能的 a。
4. 每个 a 对应一条切线。

---

### 例题 5.5A（已知切点求切线与法线）

曲线 y = x² - 3x + 2 在点 (2, 0) 处的切线和法线方程各是什么？

解：

切点：(2, 0)，即 a = 2，f(2) = 0。

求导：f'(x) = 2x - 3，f'(2) = 2(2) - 3 = 1。

切线方程：
y - 0 = 1(x - 2)  ⇒  y = x - 2

法线斜率 m⊥ = -1/1 = -1，法线方程：
y - 0 = -1(x - 2)  ⇒  y = -x + 2

---

### 例题 5.5B（已知切点，含三角函数）

求曲线 y = sin x 在点 (π/6, 1/2) 处的切线和法线方程。

解：

切点：(π/6, 1/2)。

求导：f'(x) = cos x，f'(π/6) = cos(π/6) = √3/2。

切线方程：
y - 1/2 = (√3/2)(x - π/6)
化简：
y = (√3/2)x - (√3 π)/12 + 1/2

法线斜率 m⊥ = -1/(√3/2) = -2/√3，法线方程：
y - 1/2 = (-2/√3)(x - π/6)

---

### 例题 5.5C（"经过点"的切线——切点未知）

求曲线 y = x² 经过点 P(2, 3) 的切线方程。

解：

注意 P(2, 3) 并不在曲线 y = x² 上（因为 2² = 4 ≠ 3），所以 P 不是切点。设切点为 (a, a²)。

f(x) = x²，f'(x) = 2x，所以 f'(a) = 2a。

切线方程：
y - a² = 2a(x - a)

将 P(2, 3) 代入：
3 - a² = 2a(2 - a)

展开：
3 - a² = 4a - 2a²

整理：
a² - 4a + 3 = 0

因式分解：
(a - 1)(a - 3) = 0

解得 a = 1 或 a = 3。

- 当 a = 1 时，切点为 (1, 1)，斜率 m = 2，切线方程为 y - 1 = 2(x - 1)，即 y = 2x - 1。
- 当 a = 3 时，切点为 (3, 9)，斜率 m = 6，切线方程为 y - 9 = 6(x - 3)，即 y = 6x - 9。

点 P(2, 3) 可以引出两条不同的切线。

---

### 例题 5.5D（切线与坐标轴的交点）

求曲线 y = ln x 在点 (1, 0) 处的切线与 x 轴和 y 轴的交点。

解：

f(x) = ln x，f'(x) = 1/x，f'(1) = 1。

切线方程：y - 0 = 1(x - 1)，即 y = x - 1。

与 x 轴的交点：令 y = 0，0 = x - 1，x = 1，即 (1, 0)（就是切点本身）。

与 y 轴的交点：令 x = 0，y = 0 - 1 = -1，即 (0, -1)。

---

### 练习题 5.5

1. 求曲线 y = x³ 在点 (2, 8) 处的切线和法线方程。

2. 求曲线 y = eˣ 在点 (0, 1) 处的切线方程。

3. 求曲线 y = √x 在点 (4, 2) 处的切线和法线方程。

4. 求曲线 y = x² - 2x 经过点 (1, -4) 的切线方程。

---

## 5.6 驻点（极大值与极小值）

### 5.6.1 什么是驻点？

驻点（stationary point）是函数图像上切线水平（斜率为零）的点。在驻点处，函数的值可能达到局部最大、局部最小，或者既不是最大也不是最小（后一种情况在 IGCSE 中不考）。

求驻点的步骤：
1. 求 f'(x)。
2. 解方程 f'(x) = 0。
3. 得到的每个解 x = a 对应一个驻点 (a, f(a))。

### 5.6.2 判别极大值与极小值

有两种方法可以区分极大值和极小值。

方法一：一阶导数判别法（符号变化法）

观察驻点 x = a 左右两侧 f'(x) 的符号：

| x 略小于 a（左） | x = a | x 略大于 a（右） | 结论 |
|:---:|:---:|:---:|:---:|
| f' > 0（上升） | f' = 0 | f' < 0（下降） | 局部最大值 |
| f' < 0（下降） | f' = 0 | f' > 0（上升） | 局部最小值 |
| f' > 0（上升） | f' = 0 | f' > 0（上升） | 非极值（不考） |
| f' < 0（下降） | f' = 0 | f' < 0（下降） | 非极值（不考） |

为什么符号变化能判断极值？想象你爬山：
- 如果你先上坡（f'>0），到达山顶（f'=0），然后下坡（f'<0），那么山顶就是局部最大值。
- 如果你先下坡（f'<0），到达谷底（f'=0），然后上坡（f'>0），那么谷底就是局部最小值。

方法二：二阶导数判别法

二阶导数 f''(x) 是一阶导数的导数，它告诉我们 f'(x) 的变化率。

- 如果 f'(a) = 0 且 f''(a) > 0 → 局部最小值（曲线在该点"向上凹"，像碗底）。
- 如果 f'(a) = 0 且 f''(a) < 0 → 局部最大值（曲线在该点"向下凹"，像倒扣的碗）。
- 如果 f''(a) = 0，判别法失效，需要用一阶导数法。

为什么二阶导数能判断？
- f''(a) > 0 意味着 f'(x) 在 x=a 处递增。由于 f'(a)=0，那么 f' 从负变为正→最小值。
- f''(a) < 0 意味着 f'(x) 在 x=a 处递减。由于 f'(a)=0，那么 f' 从正变为负→最大值。

### 5.6.3 二阶导数的求法

二阶导数就是一阶导数的导数。用记号表示：

f''(x) = (d/dx)(f'(x))  或  d²y/dx² = (d/dx)(dy/dx)

示例：f(x) = x³ - 3x² + 2
- 一阶导数：f'(x) = 3x² - 6x
- 二阶导数：f''(x) = 6x - 6

---

### 例题 5.6A（多项式函数的驻点）

求 f(x) = 2x³ - 9x² + 12x - 3 的驻点，并判别它们是极大值还是极小值。

解：

第一步：求 f'(x) 并令其为零。

f'(x) = 6x² - 18x + 12 = 6(x² - 3x + 2) = 6(x-1)(x-2)

令 f'(x) = 0，得 x = 1 或 x = 2。

f(1) = 2 - 9 + 12 - 3 = 2，驻点 (1, 2)
f(2) = 16 - 36 + 24 - 3 = 1，驻点 (2, 1)

第二步：用二阶导数判别。

f''(x) = 12x - 18

- f''(1) = 12(1) - 18 = -6 < 0 → (1, 2) 是局部最大值。
- f''(2) = 12(2) - 18 = 6 > 0 → (2, 1) 是局部最小值。

一阶导数法验证：在 x=1 左侧取 x=0，f'(0) = 12 > 0；在 x=1 右侧取 x=1.5，f'(1.5) = 6(0.5)(-0.5) = -1.5 < 0。符号从正变负，确认是最大值。

---

### 例题 5.6B（含三角函数的驻点）

求 f(x) = sin x + cos x 在区间 [0, 2π] 上的驻点，并判别类型。

解：

f'(x) = cos x - sin x

令 f'(x) = 0：
cos x - sin x = 0  ⇒  cos x = sin x  ⇒  tan x = 1

在 [0, 2π] 上，tan x = 1 的解为 x = π/4 和 x = 5π/4。

f(π/4) = √2/2 + √2/2 = √2
f(5π/4) = -√2/2 - √2/2 = -√2

求二阶导数：f''(x) = -sin x - cos x

- f''(π/4) = -√2/2 - √2/2 = -√2 < 0 → (π/4, √2) 是局部最大值。
- f''(5π/4) = √2/2 + √2/2 = √2 > 0 → (5π/4, -√2) 是局部最小值。

---

### 例题 5.6C（含指数函数的驻点）

求 f(x) = x e⁻ˣ 的驻点，并判别类型。求该函数的最大值。

解：

使用积法则：设 u = x，v = e⁻ˣ，则 u' = 1，v' = -e⁻ˣ。

f'(x) = x·(-e⁻ˣ) + e⁻ˣ·1 = e⁻ˣ(1 - x)

令 f'(x) = 0。由于 e⁻ˣ > 0 对所有 x 成立，所以 1 - x = 0，即 x = 1。

f(1) = 1·e⁻¹ = 1/e

驻点为 (1, 1/e)。

用一阶导数法判别：在 x=1 左侧取 x=0，f'(0) = e⁰(1-0) = 1 > 0；在 x=1 右侧取 x=2，f'(2) = e⁻²(1-2) = -e⁻² < 0。符号从正变负，所以 (1, 1/e) 是局部最大值。

由于当 x → ∞ 时 x e⁻ˣ → 0，当 x → -∞ 时 x e⁻ˣ → -∞，这个最大值也是全局最大值，最大值为 1/e。

---

### 例题 5.6D（驻点求参数）

已知 f(x) = x³ + a x² + b 在 x = 2 处有驻点，且该驻点的函数值为 5，求常数 a 和 b。

解：

f'(x) = 3x² + 2a x

在 x=2 处有驻点，所以 f'(2) = 0：
3(2)² + 2a(2) = 0  ⇒  12 + 4a = 0  ⇒  a = -3

驻点函数值 f(2) = 5：
f(2) = 2³ + (-3)(2)² + b = 8 - 12 + b = b - 4 = 5  ⇒  b = 9

所以 a = -3，b = 9。f(x) = x³ - 3x² + 9。

---

### 练习题 5.6

1. 求 f(x) = x³ - 6x² + 9x + 1 的驻点，并判别类型。

2. 求 f(x) = x² eˣ 的驻点，并判别类型。

3. 已知 f(x) = x³ + a x + b 在 x = 1 处有驻点 f(1) = 4，求 a 和 b。

4. 求 f(x) = 2x³ - 3x² - 12x + 5 的极值。

---

## 5.7 相关变化率与微小增量近似

### 5.7.1 相关变化率（Connected Rates of Change）

相关变化率问题处理的是多个相互关联的量的变化速度。核心思路是：如果 y 通过某个关系依赖于 u，而 u 又依赖于 x，那么我们可以通过链式法则将 dy/dx 与 dy/du 和 du/dx 联系起来。

dy/dx = (dy/du)·(du/dx)

更一般地，如果问题涉及时间 t，我们经常使用：

dy/dt = (dy/dx)·(dx/dt)

解题步骤：
1. 找出所有相关变量，确定已知变化率和需求的变化率。
2. 建立变量之间的函数关系（几何公式、物理关系等）。
3. 对关系式两边关于时间 t 求导（隐式微分）。
4. 代入已知数值，解出未知变化率。

### 5.7.2 微小增量与近似（Small Increments and Approximations）

导数的另一个重要应用是：用切线来近似函数在某个点附近的变化。

回忆导数的定义：

f'(a) ≈ [f(a + δx) - f(a)] / δx  （当 δx 很小时）

整理得到：

f(a + δx) ≈ f(a) + f'(a)·δx

这就是线性近似公式。它告诉我们：对于微小的变化 δx，函数的改变量大约等于导数乘以自变量的改变量。

用莱布尼茨记号表示：

δy ≈ (dy/dx)·δx

其中 δy = f(x + δx) - f(x) 是函数值的实际变化量，而 (dy/dx)·δx 是切线上的变化量（近似值）。

为什么这成立？从几何上看，切线是曲线在该点附近的最佳近似。当 δx 很小时，曲线上的点 (a+δx, f(a+δx)) 非常接近切线上的点 (a+δx, f(a) + f'(a)δx)，所以可以用切线上的变化来近似曲线上的变化。

---

### 例题 5.7A（相关变化率——圆面积）

一个圆的半径以 2 cm/s 的速率增加。求当半径为 5 cm 时，圆面积的增加速率。

解：

设半径为 r，面积为 A。已知 dr/dt = 2，求当 r = 5 时的 dA/dt。

圆面积公式：A = π r²

对时间 t 求导（使用链式法则）：

dA/dt = (dA/dr)·(dr/dt) = 2π r·(dr/dt)

代入已知值：r = 5，dr/dt = 2。

dA/dt = 2π·5·2 = 20π cm²/s

所以当半径为 5 cm 时，圆面积以 20π cm²/s 的速率增加。

---

### 例题 5.7B（相关变化率——运动学中的关联）

一个倒圆锥形容器，顶部半径为 4 m，高为 8 m，以 2 m³/min 的速率注水。求当水深为 3 m 时，水面上升的速率。

解：

设水深为 h，水面半径为 r，水的体积为 V。已知 dV/dt = 2，求当 h = 3 时的 dh/dt。

由相似三角形：r/h = 4/8 = 1/2，所以 r = h/2。

圆锥体积公式：
V = (1/3)π r² h = (1/3)π (h/2)² h = (1/3)π·(h²/4)·h = (π/12) h³

对时间求导：
dV/dt = (dV/dh)·(dh/dt) = (π/12)·3h²·(dh/dt) = (π/4) h²·(dh/dt)

代入 dV/dt = 2 和 h = 3：
2 = (π/4)·3²·(dh/dt) = (9π/4)·(dh/dt)

解得：
dh/dt = (2·4)/(9π) = 8/(9π) m/min

所以水深为 3 m 时，水面以 8/(9π) m/min 的速率上升。

---

### 例题 5.7C（微小增量近似）

用微分近似计算 √4.02 的值。

解：

设 f(x) = √x，取 a = 4（4 是一个容易计算平方根的数），δx = 0.02。

f(x) = x^(1/2)，f'(x) = (1/2)x^(-1/2) = 1/(2√x)

f(4) = √4 = 2，f'(4) = 1/(2√4) = 1/4

线性近似公式：
f(4 + 0.02) ≈ f(4) + f'(4)·0.02

√4.02 ≈ 2 + (1/4)×0.02 = 2 + 0.005 = 2.005

与精确值 2.004993... 相比，近似值 2.005 的误差非常小（约 7×10⁻⁶）。

---

### 例题 5.7D（微小增量近似——已知误差求最大误差）

球的体积公式为 V = (4/3)π r³。如果测量半径时的最大误差为 0.1 cm，当测量半径为 5 cm 时，求计算体积时的最大近似误差。

解：

已知 r = 5，|δr| ≤ 0.1。

dV/dr = 4π r²

δV ≈ (dV/dr)·δr = 4π r²·δr

最大误差（取绝对值）：
|δV|max ≈ 4π·5²·0.1 = 4π·25·0.1 = 10π cm³

所以体积的最大近似误差约为 10π ≈ 31.4 cm³。

---

### 练习题 5.7

1. 正方形的边长以 3 cm/s 的速率增加。求当边长为 10 cm 时，面积增加的速率。

2. 用微分近似计算 ∛8.03 的值。（提示：令 f(x) = ∛x）

3. 气体在球形容器中膨胀，当半径为 2 m 时，体积以 16π m³/s 的速率增加。求此时半径增加的速率。

---

## 5.8 实际最值问题

### 5.8.1 解题思路

实际最值问题（Practical Maxima and Minima）将微积分应用于现实世界中的优化问题——例如，如何用最少的材料制作一个容器、如何在给定成本下最大化利润、如何确定最快的路径等。

标准解题步骤：

1. 理解问题：明确需要最大化或最小化的量是什么（目标函数）。
2. 建立变量：引入变量，用变量表示所有相关量。
3. 建立关系：利用题目条件（几何关系、物理约束等），将目标函数表示为一个变量的函数。
4. 求导找驻点：对目标函数求导，令导数为零，解出驻点。
5. 判别类型：用一阶或二阶导数法确认是最大值还是最小值。
6. 检验合理性：验证驻点是否在定义域内，并回答原问题。

⚠️ 关键点：实际问题通常有约束条件（如固定总长度、固定面积等），需要用约束条件消去多余变量，将目标函数化为单变量函数。

---

### 例题 5.8A（面积最大化）

用一段长 100 m 的篱笆围成一个矩形花园，一边靠墙（墙足够长），求花园的最大面积及此时的尺寸。

解：

设垂直于墙的两边长为 x m，平行于墙的一边长为 y m。

篱笆总长为 100 m，约束条件：2x + y = 100，即 y = 100 - 2x。

花园面积 A = x·y = x(100 - 2x) = 100x - 2x²

注意定义域：x > 0 且 y > 0，即 100 - 2x > 0，x < 50，所以 0 < x < 50。

求导：
A'(x) = 100 - 4x

令 A'(x) = 0：100 - 4x = 0，解得 x = 25。

二阶导数：A''(x) = -4 < 0，确认 x = 25 处为最大值。

此时 y = 100 - 2(25) = 50。

最大面积：A = 25 × 50 = 1250 m²。

答案：当垂直于墙的边长为 25 m，平行于墙的边长为 50 m 时，最大面积为 1250 m²。

---

### 例题 5.8B（体积最大化——无盖盒子）

从一张 30 cm × 20 cm 的矩形纸板的四个角各剪去一个边长为 x cm 的小正方形，然后折起四周做成一个无盖盒子。求 x 为多少时盒子的体积最大，并求最大体积。

解：

剪去边长为 x 的正方形后，盒子的底面尺寸为 (30 - 2x) × (20 - 2x)，高为 x。

盒子体积：
V(x) = x(30 - 2x)(20 - 2x) = x(600 - 60x - 40x + 4x²) = x(600 - 100x + 4x²)
V(x) = 4x³ - 100x² + 600x

定义域：x > 0，30 - 2x > 0 ⇒ x < 15，20 - 2x > 0 ⇒ x < 10，所以 0 < x < 10。

求导：
V'(x) = 12x² - 200x + 600

令 V'(x) = 0：
12x² - 200x + 600 = 0
两边除以 4：3x² - 50x + 150 = 0

用求根公式：
x = [50 ± √(2500 - 1800)] / 6 = [50 ± √700] / 6 = [50 ± 10√7] / 6

两个解：x₁ = (50 + 10√7)/6 ≈ (50 + 26.46)/6 ≈ 12.74（超出定义域 x < 10，舍去）
x₂ = (50 - 10√7)/6 ≈ (50 - 26.46)/6 ≈ 3.92

所以 x = (50 - 10√7)/6 ≈ 3.92 cm。

用二阶导数验证：V''(x) = 24x - 200
V''(3.92) = 24(3.92) - 200 ≈ 94.08 - 200 = -105.92 < 0，确认是最大值。

最大体积：
V = 3.92 × (30 - 7.84) × (20 - 7.84) = 3.92 × 22.16 × 12.16 ≈ 1056.3 cm³

答案：当剪去的小正方形边长约为 3.92 cm 时，盒子体积最大，约为 1056 cm³。

---

### 例题 5.8C（成本最小化）

某公司需要制造一个开口圆柱形水桶，容积固定为 V = 1000π cm³。桶底材料价格为 2 元/cm²，侧面材料价格为 1 元/cm²。求水桶的底面半径 r 和高 h 为何值时，总成本最小？最小成本是多少？

解：

设底面半径为 r cm，高为 h cm。

容积约束：V = π r² h = 1000π，所以 h = 1000/r²。

成本：底面积 π r²，价格 2 元/cm²；侧面积 2π r h，价格 1 元/cm²。

C = 2·π r² + 1·2π r h = 2π r² + 2π r·(1000/r²) = 2π r² + 2000π/r

定义域：r > 0。

求导：
C'(r) = 4π r - 2000π/r²

令 C'(r) = 0：
4π r - 2000π/r² = 0  ⇒  4π r = 2000π/r²
两边除以 π（π > 0）：
4r = 2000/r²  ⇒  4r³ = 2000  ⇒  r³ = 500

解得：r = ∛500 = ∛(5×100) = 5∛4 cm。

此时 h = 1000/r² = 1000/500^(2/3) = 2·500^(1/3) = 2r。

所以 h = 2r，即高等于底面直径时成本最小。

用二阶导数验证：
C''(r) = 4π + 4000π/r³
代入 r³ = 500：C''(r) = 4π + 4000π/500 = 4π + 8π = 12π > 0，确认是最小值。

最小成本：
C_min = 6π·500^(2/3) 元

近似计算：500^(2/3) = (500^(1/3))² ≈ (7.937)² ≈ 63，所以 C_min ≈ 6π×63 ≈ 1188 元。

答案：当底面半径 r = ∛500 cm（约 7.94 cm），高 h = 2r（约 15.88 cm）时，最小成本约为 1188 元。

---

### 例题 5.8D（利润最大化）

某工厂生产一种产品，每天生产 x 件的成本为 C(x) = 200 + 10x + 0.01x² 元，售价为每件 30 元。求每天生产多少件时利润最大，最大利润是多少？

解：

收入：R(x) = 30x

利润：P(x) = R(x) - C(x) = 30x - (200 + 10x + 0.01x²) = -0.01x² + 20x - 200

定义域：x ≥ 0 且为整数（实际中为正整数，但我们可以用连续函数近似求最大值，再取整）。

求导：
P'(x) = -0.02x + 20

令 P'(x) = 0：-0.02x + 20 = 0，解得 x = 1000。

二阶导数：P''(x) = -0.02 < 0，确认是最大值。

最大利润：
P(1000) = -0.01(1000)² + 20(1000) - 200 = -10000 + 20000 - 200 = 9800 元

答案：每天生产 1000 件时利润最大，最大利润为 9800 元。

---

### 练习题 5.8

1. 用一段长 120 m 的篱笆围成一个矩形花园（不靠墙），求最大面积及此时的尺寸。

2. 求曲线 y = x² - 4x + 5 上的点到原点 (0,0) 的最短距离。
   （提示：距离平方 d² = x² + y²，将 y 代入后求最小值）

3. 一个圆柱体无盖罐头的容积固定为 V（常数）。求底面半径 r 与高 h 的比值，使得表面积最小。

---

## 本章总结（速查表）

| 知识点 | 公式/方法 | 章节 |
|--------|-----------|:----:|
| 导数的极限定义 | f'(x) = lim_{δx→0} [f(x+δx)-f(x)]/δx | 5.1 |
| 幂函数求导 | (d/dx)(xⁿ) = n xⁿ⁻¹（n 为任意有理数） | 5.2 |
| 三角函数求导 | (d/dx)(sin x) = cos x，(d/dx)(cos x) = -sin x，(d/dx)(tan x) = sec² x | 5.2 |
| 指数对数求导 | (d/dx)(eˣ) = eˣ，(d/dx)(ln x) = 1/x，(d/dx)(aˣ) = aˣ ln a | 5.2 |
| 链式法则 | dy/dx = (dy/du)·(du/dx) | 5.3 |
| 积法则 | (uv)' = u v' + v u' | 5.4 |
| 商法则 | (u/v)' = (v u' - u v')/v² | 5.4 |
| 切线方程 | y - f(a) = f'(a)(x - a) | 5.5 |
| 法线方程 | y - f(a) = (-1/f'(a))(x - a)（f'(a) ≠ 0） | 5.5 |
| 驻点 | 解 f'(x) = 0 | 5.6 |
| 二阶导数判别 | f''(a) > 0 为极小，f''(a) < 0 为极大 | 5.6 |
| 相关变化率 | dy/dt = (dy/dx)·(dx/dt) | 5.7 |
| 微小增量近似 | f(a + δx) ≈ f(a) + f'(a)δx，δy ≈ (dy/dx)δx | 5.7 |
| 实际最值 | 建立单变量函数 → 求导找驻点 → 判别类型 → 回答原问题 | 5.8 |

---

## 练习题答案

### 5.1 导数概念与记号

1. f'(1) = 4
   - f(1+δx) = (1+δx)² + 2(1+δx) = 1 + 2δx + (δx)² + 2 + 2δx = 3 + 4δx + (δx)²
   - f(1) = 1² + 2(1) = 3
   - [f(1+δx)-f(1)]/δx = (4δx + (δx)²)/δx = 4 + δx → 4

2. s'(3) = 15 m/s
   - s'(t) = 4t + 3，s'(3) = 4(3) + 3 = 15

3. 8
   - lim_{x→4} (x²-16)/(x-4) = lim_{x→4} [(x-4)(x+4)]/(x-4) = lim_{x→4} (x+4) = 8

### 5.2 基本求导公式

1. f'(x) = 12x² - 4x + 5

2. g'(x) = -6/x³ + 1/(4x√x) + 2x^(-2/3)
   - 具体：3/x² = 3x⁻² → -6x⁻³；-(1/2)x^(-1/2) → (1/4)x^(-3/2)；6x^(1/3) → 2x^(-2/3)

3. h'(x) = 5 cos x + 3 sin x + 2 sec² x

4. p'(x) = 2 eˣ + 4ˣ ln 4 - 1/(3x)

### 5.3 链式法则

1. y' = 20(5x+2)³
2. y = (3x-1)^(-1/2)，y' = -(3/2)(3x-1)^(-3/2) = -3/(2√((3x-1)³))
3. y' = 2 e^(2x-3)
4. y' = 2x/(x²+4)
5. y' = 3 cos²(2x)·(-sin(2x))·2 = -6 cos²(2x) sin(2x) = -3 cos(2x) sin(4x)

### 5.4 积法则与商法则

1. y' = 2x eˣ + x² eˣ = x eˣ(2 + x)
2. y' = [3(x-2) - 3x(1)]/(x-2)² = (3x-6-3x)/(x-2)² = -6/(x-2)²
3. y' = cos x - x sin x
4. y' = [(1)(x²+1) - (x+1)(2x)]/(x²+1)² = (x²+1 - 2x² - 2x)/(x²+1)² = (-x² - 2x + 1)/(x²+1)²
5. y' = eˣ sin x + eˣ cos x = eˣ(sin x + cos x)

### 5.5 切线与法线

1. f(x) = x³，f'(x) = 3x²，f'(2) = 12
   - 切线：y - 8 = 12(x - 2)，即 y = 12x - 16
   - 法线：y - 8 = -(1/12)(x - 2)，即 y = -(1/12)x + 49/6

2. f(x) = eˣ，f'(x) = eˣ，f'(0) = 1
   - 切线：y - 1 = 1(x - 0)，即 y = x + 1

3. f(x) = √x，f'(x) = 1/(2√x)，f'(4) = 1/4
   - 切线：y - 2 = (1/4)(x - 4)，即 y = (1/4)x + 1
   - 法线：y - 2 = -4(x - 4)，即 y = -4x + 18

4. 设切点为 (a, a² - 2a)，f'(a) = 2a - 2。
   切线方程：y - (a² - 2a) = (2a - 2)(x - a)
   代入 (1, -4)：-4 - (a² - 2a) = (2a - 2)(1 - a)
   化简：-4 - a² + 2a = (2a-2)(1-a) = 2a-2 - 2a² + 2a = -2a² + 4a - 2
   整理：-4 - a² + 2a = -2a² + 4a - 2，移项：a² - 2a - 2 = 0
   解得 a = 1 ± √3
   - a = 1 + √3：斜率 m = 2√3，切线 y = 2√3 x - 2√3 - 4
   - a = 1 - √3：斜率 m = -2√3，切线 y = -2√3 x + 2√3 - 4

### 5.6 驻点

1. f'(x) = 3x² - 12x + 9 = 3(x-1)(x-3)
   x = 1：f(1) = 5，f''(1) = 6-12 = -6 < 0 → 极大值
   x = 3：f(3) = 1，f''(3) = 18-12 = 6 > 0 → 极小值

2. f'(x) = 2x eˣ + x² eˣ = x eˣ(2 + x)
   x = 0：f(0) = 0，f''(0) = 2 > 0 → 极小值
   x = -2：f(-2) = 4 e⁻²，f''(-2) = -2 e⁻² < 0 → 极大值

3. f'(x) = 3x² + a，f'(1) = 3 + a = 0 → a = -3
   f(1) = 1 + (-3)(1) + b = 4 → b = 6

4. f'(x) = 6x² - 6x - 12 = 6(x² - x - 2) = 6(x-2)(x+1)
   x = -1：f(-1) = -2 - 3 + 12 + 5 = 12，f''(-1) = -12 - 6 = -18 < 0 → 极大值 12
   x = 2：f(2) = 16 - 12 - 24 + 5 = -15，f''(2) = 24 - 6 = 18 > 0 → 极小值 -15

### 5.7 相关变化率与微小增量近似

1. A = s²，dA/dt = 2s ds/dt = 2(10)(3) = 60 cm²/s

2. f(x) = x^(1/3)，f'(x) = (1/3)x^(-2/3)，取 a = 8，δx = 0.03
   f(8) = 2，f'(8) = (1/3)(8)^(-2/3) = (1/3)·(1/4) = 1/12
   ∛8.03 ≈ 2 + (1/12)×0.03 = 2 + 0.0025 = 2.0025

3. V = (4/3)π r³，dV/dt = 4π r² dr/dt
   16π = 4π(2)² dr/dt = 16π dr/dt → dr/dt = 1 m/s

### 5.8 实际最值问题

1. 设长为 x，宽为 y，2x + 2y = 120，y = 60 - x
   A = xy = x(60-x) = 60x - x²
   A'(x) = 60 - 2x = 0 → x = 30，y = 30
   A''(x) = -2 < 0 → 最大值
   最大面积 = 30×30 = 900 m²

2. d² = x² + (x² - 4x + 5)²
   设 g(x) = d²，求导找最小值。
   或者：到原点的最短距离即原点到抛物线的最短距离，可用求导法。
   
   更简单的方法：设 h(x) = x² + (x²-4x+5)²
   h'(x) = 2x + 2(x²-4x+5)(2x-4)
   = 2x + 2(x²-4x+5)(2)(x-2)
   = 2x + 4(x²-4x+5)(x-2)
   
   令 h'(x) = 0，可解得 x = 2。
   d² = 2² + (4-8+5)² = 4 + 1 = 5，d = √5

3. 表面积 S = π r² + 2π r h，体积 V = π r² h（常数），h = V/(π r²)
   S = π r² + 2π r (V/(π r²)) = π r² + 2V/r
   S'(r) = 2π r - 2V/r² = 0 → 2π r = 2V/r² → π r³ = V → r³ = V/π
   而 V = π r² h，所以 π r³ = π r² h → r = h
   答案：r : h = 1 : 1，即底面半径等于高时表面积最小。

---
---

# 第 6 章：方程与不等式（图形法）

## 引言

在前面的章节中，我们学习了用代数方法解方程和不等式——因式分解、求根公式、配方法等。然而，许多方程和不等式在代数上难以直接处理，尤其是涉及绝对值、三次多项式以及复杂代换的情形。**图形法**提供了一种强有力的替代思路：通过函数的图像直观地理解方程的解和不等式的解集。图形法并不总是给出精确值，但它能帮助我们迅速把握解的整体结构，并为代数运算提供几何直觉。

本章我们将综合运用前几章的知识——特别是**第3章（二次函数）**中的判别式和因式分解、**第4章（函数）**中的绝对值函数图像，以及**第5章（微分）**中的导数工具——来系统地处理五类问题：绝对值方程、绝对值不等式、代换法化为一元二次方程、三次多项式图像与不等式、以及联立方程组的图形解法。

---

## 考纲对照（Cambridge IGCSE Additional Mathematics 0606, 2028–2030）

| 考纲条目 | 内容 | 对应本节 |
|---------|------|---------|
| 4.1 | 解 |ax+b| = c (c >= 0)、|ax+b| = cx+d、|ax+b| = |cx+d|、|ax^2+bx+c| = d 型方程（代数法或图形法） | 6.1 |
| 4.2 | 解 k|ax+b| > c (c>=0)、k|ax+b| <= c (c>0)、k|ax+b| <= |cx+d| (k>0)、|ax+b| <= cx+d、|ax^2+bx+c| > d、|ax^2+bx+c| <= d 型不等式 | 6.2 |
| 4.3 | 用代换法构造并求解一元二次方程 | 6.3 |
| 4.4 | 绘制三次多项式（三个线性因式乘积）及其绝对值图像 | 6.4 |
| 4.5 | 图形法解三次不等式 f(x) >= d、f(x) > d、f(x) <= d、f(x) < d | 6.4 |
| 5.1 | 用消元法或代入法解二元联立方程组 | 6.5 |

---

## 前置知识：集合与区间表示法

> 解不等式时，我们通常用**区间**或**集合**来表示解集。本节回顾集合的基本记号和区间表示法，是本章所有内容的基础。

### 集合的基本概念

**集合**（set）是由某些确定的、互不相同的对象组成的整体。集合中的对象称为**元素**。

- a ∈ A：a 属于集合 A（a 是 A 的元素）
- a ∉ A：a 不属于集合 A

**常用数集**：

- N = {1, 2, 3, 4, ...}：自然数集
- Z = {..., -2, -1, 0, 1, 2, ...}：整数集
- Q：有理数集（可以写成分数形式的数）
- R：实数集（包括有理数和无理数）
- R+：正实数集
- ∅：空集（不含任何元素的集合）

**集合的表示法**：

**列举法**：A = {1, 2, 3, 4, 5}

**描述法**：A = {x | x 是大于 0 且小于 6 的整数}，或更一般地 A = {x ∈ R | x^2 < 4}（表示所有满足 x^2 < 4 的实数 x）。

### 区间表示法

区间是实数集的子集，用数轴上的连续段来表示。

| 区间类型 | 不等式表示 | 区间记号 | 数轴表示 |
|---------|-----------|---------|---------|
| 闭区间 | a <= x <= b | [a, b] | 两端点用实心点 |
| 开区间 | a < x < b | (a, b) | 两端点用空心点 |
| 左闭右开 | a <= x < b | [a, b) | 左实心、右空心 |
| 左开右闭 | a < x <= b | (a, b] | 左空心、右实心 |
| 无限区间 | x >= a | [a, ∞) | 向右延伸 |
| 无限区间 | x > a | (a, ∞) | 向右延伸 |
| 无限区间 | x <= b | (-∞, b] | 向左延伸 |
| 无限区间 | x < b | (-∞, b) | 向左延伸 |
| 全体实数 | x ∈ R | (-∞, ∞) | 整条数轴 |

> ⚠️ **注意**：∞（无穷大）不是一个数，而是一个概念，表示"无限延伸"。因此涉及 ∞ 的一端总是用圆括号（开区间）。

### 集合的运算

**并集** A ∪ B = {x | x ∈ A 或 x ∈ B}：属于 A **或**属于 B 的所有元素。

**交集** A ∩ B = {x | x ∈ A 且 x ∈ B}：同时属于 A **和** B 的所有元素。

**示例**：设 A = {x | x < 1}，B = {x | x >= -2}。

- A ∩ B = {x | -2 <= x < 1} = [-2, 1)
- A ∪ B = R = (-∞, ∞)

**示例**：解 x^2 - 5x + 6 > 0 得 x < 2 或 x > 3，解集用区间表示为 (-∞, 2) ∪ (3, ∞)。这里 ∪ 表示两个区间的"并集"——x 只要满足其中一个即可。

---

## 6.1 绝对值方程

### 6.1.1 绝对值的定义与几何意义

绝对值 |A| 从几何上看表示数轴上点 A 到原点的**距离**。代数上定义为：

|x| = { x, x >= 0; -x, x < 0 }

绝对值的重要性质：
- |A| >= 0 对一切实数 A 成立
- |A|^2 = A^2
- |AB| = |A| · |B|
- |A/B| = |A| / |B| (B ≠ 0)

解绝对值方程的核心思想是**去掉绝对值符号**，这通常通过分类讨论或两边平方来实现。

---

### 6.1.2 类型 |ax + b| = c (c >= 0)

这是最简单的绝对值方程。根据绝对值的定义，|ax + b| = c 等价于：

ax + b = c 或 ax + b = -c

**例题 1**：解方程 |3x - 7| = 5。

**解**：

3x - 7 = 5 或 3x - 7 = -5

3x = 12 或 3x = 2

x = 4 或 x = 2/3

验证：|3(4) - 7| = |12 - 7| = 5 ✓，|3(2/3) - 7| = |2 - 7| = 5 ✓。

**例题 2**：解方程 |5 - 2x| = 9。

**解**：

5 - 2x = 9 或 5 - 2x = -9

-2x = 4 或 -2x = -14

x = -2 或 x = 7

验证：|5 - 2(-2)| = |5 + 4| = 9 ✓，|5 - 2(7)| = |5 - 14| = 9 ✓。

**例题 3**：解方程 |4x + 3| = 0。

**解**：

4x + 3 = 0

x = -3/4

注意：c = 0 时只有一个解，因为 4x + 3 既等于 0 又等于 -0（相同）。验证：|4(-3/4) + 3| = |-3 + 3| = 0 ✓。

---

### 6.1.3 类型 |ax + b| = cx + d

当等号右边也含有变量时，不能直接拆成两个方程——因为必须确保右边非负（绝对值永远非负，所以右边也必须非负）。解法一：**分类讨论**（分 ax + b 的符号）。解法二：**两边平方**后解二次方程再验根。

**例题 4**：解方程 |2x - 3| = x + 1。

**解（分类讨论法）**：

**情况 1**：2x - 3 >= 0，即 x >= 3/2。

此时 |2x - 3| = 2x - 3，方程化为：

2x - 3 = x + 1 => x = 4

检查前提：4 >= 3/2 ✓。

**情况 2**：2x - 3 < 0，即 x < 3/2。

此时 |2x - 3| = -(2x - 3) = -2x + 3，方程化为：

-2x + 3 = x + 1 => -3x = -2 => x = 2/3

检查前提：2/3 < 3/2 ✓。

因此解为 x = 4 和 x = 2/3。

**解（平方验根法）**：

两边平方：(2x - 3)^2 = (x + 1)^2

4x^2 - 12x + 9 = x^2 + 2x + 1

3x^2 - 14x + 8 = 0

(3x - 2)(x - 4) = 0

x = 2/3 或 x = 4

验证：x = 4 时右边 4 + 1 = 5 > 0 ✓；x = 2/3 时右边 2/3 + 1 = 5/3 > 0 ✓。两个解都有效。

**例题 5**：解方程 |x + 2| = 2x - 1。

**解**：

**情况 1**：x + 2 >= 0，即 x >= -2。

x + 2 = 2x - 1 => 3 = x => x = 3

检查：3 >= -2 ✓。验证右边：2(3) - 1 = 5 > 0 ✓。

**情况 2**：x + 2 < 0，即 x < -2。

-(x + 2) = 2x - 1 => -x - 2 = 2x - 1 => -1 = 3x => x = -1/3

检查前提：-1/3 < -2？不成立！-1/3 > -2，所以此解无效。

因此唯一解为 x = 3。

**例题 6**：解方程 |3x + 1| = 2 - x。

**解**：

**情况 1**：3x + 1 >= 0，即 x >= -1/3。

3x + 1 = 2 - x => 4x = 1 => x = 1/4

检查：1/4 >= -1/3 ✓。右边：2 - 1/4 = 7/4 > 0 ✓。

**情况 2**：3x + 1 < 0，即 x < -1/3。

-(3x + 1) = 2 - x => -3x - 1 = 2 - x => -2x = 3 => x = -3/2

检查：-3/2 < -1/3 ✓。右边：2 - (-3/2) = 7/2 > 0 ✓。

因此解为 x = 1/4 和 x = -3/2。

---

### 6.1.4 类型 |ax + b| = |cx + d|

两个绝对值相等，意味着两个表达式要么相等，要么互为相反数。无需分类讨论前提条件。

|ax + b| = |cx + d|  <=>  ax + b = cx + d 或 ax + b = -(cx + d)

**例题 7**：解方程 |2x + 5| = |x - 3|。

**解**：

2x + 5 = x - 3 或 2x + 5 = -(x - 3)

**方程 1**：2x + 5 = x - 3 => x = -8

**方程 2**：2x + 5 = -x + 3 => 3x = -2 => x = -2/3

因此解为 x = -8 和 x = -2/3。

验证：|2(-8) + 5| = |-11| = 11，|(-8) - 3| = |-11| = 11 ✓。
|2(-2/3) + 5| = |-4/3 + 5| = |11/3| = 11/3，|-2/3 - 3| = |-11/3| = 11/3 ✓。

**例题 8**：解方程 |5x - 2| = |3x + 4|。

**解**：

5x - 2 = 3x + 4 或 5x - 2 = -(3x + 4)

**方程 1**：5x - 2 = 3x + 4 => 2x = 6 => x = 3

**方程 2**：5x - 2 = -3x - 4 => 8x = -2 => x = -1/4

因此解为 x = 3 和 x = -1/4。

**例题 9**：解方程 |x + 1| = |2x - 5|。

**解**：

x + 1 = 2x - 5 或 x + 1 = -(2x - 5)

**方程 1**：x + 1 = 2x - 5 => 6 = x => x = 6

**方程 2**：x + 1 = -2x + 5 => 3x = 4 => x = 4/3

因此解为 x = 6 和 x = 4/3。

---

### 6.1.5 类型 |ax^2 + bx + c| = d

当绝对值内部是二次函数时，处理思路相同：去掉绝对值后得到两个二次方程。

**例题 10**：解方程 |x^2 - 4x + 3| = 3。

**解**：

x^2 - 4x + 3 = 3 或 x^2 - 4x + 3 = -3

**方程 1**：x^2 - 4x = 0 => x(x - 4) = 0 => x = 0 或 x = 4

**方程 2**：x^2 - 4x + 6 = 0

判别式 Δ = (-4)^2 - 4(1)(6) = 16 - 24 = -8 < 0，无实数解。

因此解为 x = 0 和 x = 4。

**例题 11**：解方程 |2x^2 - 5x - 3| = 2。

**解**：

2x^2 - 5x - 3 = 2 或 2x^2 - 5x - 3 = -2

**方程 1**：2x^2 - 5x - 5 = 0

x = (5 ± √(25 - 4(2)(-5))) / (2(2)) = (5 ± √(25 + 40)) / 4 = (5 ± √65) / 4

**方程 2**：2x^2 - 5x - 1 = 0

x = (5 ± √(25 - 4(2)(-1))) / 4 = (5 ± √(25 + 8)) / 4 = (5 ± √33) / 4

因此有四个解：x = (5 ± √65)/4 和 x = (5 ± √33)/4。

**例题 12**：解方程 |x^2 - 9| = 7。

**解**：

x^2 - 9 = 7 或 x^2 - 9 = -7

**方程 1**：x^2 = 16 => x = ±4

**方程 2**：x^2 = 2 => x = ±√2

因此解为 x = 4, -4, √2, -√2。

---

## 6.2 绝对值不等式

绝对值不等式的核心思想：**将绝对值不等式转化为不含绝对值的不等式组**，然后利用数轴或图像求解。

### 6.2.1 基本类型 |ax + b| > c 和 |ax + b| <= c

**核心规则**（c > 0）：

|ax + b| > c  <=>  ax + b < -c 或 ax + b > c

|ax + b| <= c  <=>  -c <= ax + b <= c

> 记忆方法："**大于取两边，小于取中间**"。

对于 k|ax + b| > c（k > 0，c >= 0），先两边除以 k 化为标准形式：|ax + b| > c/k。

**例题 1**：解不等式 |2x - 5| > 3。

**解**：

"大于取两边"：

2x - 5 < -3 或 2x - 5 > 3

2x < 2 或 2x > 8

x < 1 或 x > 4

解集为 x ∈ (-∞, 1) ∪ (4, ∞)。

**例题 2**：解不等式 3|2x + 1| <= 15。

**解**：

先除以 3：|2x + 1| <= 5

"小于取中间"：

-5 <= 2x + 1 <= 5

左边：-5 <= 2x + 1 => -6 <= 2x => x >= -3

右边：2x + 1 <= 5 => 2x <= 4 => x <= 2

因此解集为 -3 <= x <= 2，即 x ∈ [-3, 2]。

**例题 3**：解不等式 2|4 - x| > 10。

**解**：

除以 2：|4 - x| > 5

"大于取两边"：

4 - x < -5 或 4 - x > 5

-x < -9 或 -x > 1

x > 9 或 x < -1

解集为 x ∈ (-∞, -1) ∪ (9, ∞)。

---

### 6.2.2 类型 k|ax + b| <= |cx + d| (k > 0)

当两边都有绝对值时，最可靠的方法是**两边平方**，利用 |A|^2 = A^2 的性质化为不含绝对值的不等式。

**例题 4**：解不等式 |2x - 1| <= |x + 3|。

**解**：

两边平方（不等号方向保持不变，因为两边非负）：

(2x - 1)^2 <= (x + 3)^2

4x^2 - 4x + 1 <= x^2 + 6x + 9

3x^2 - 10x - 8 <= 0

解方程 3x^2 - 10x - 8 = 0：

x = (10 ± √(100 + 96)) / 6 = (10 ± √196) / 6 = (10 ± 14) / 6

x = 24/6 = 4 或 x = -4/6 = -2/3

二次项系数 3 > 0，抛物线开口向上，所以 3x^2 - 10x - 8 <= 0 的解为两根之间：

-2/3 <= x <= 4

即 x ∈ [-2/3, 4]。

**例题 5**：解不等式 2|x + 2| > |3x - 1|。

**解**：

两边平方：

4(x + 2)^2 > (3x - 1)^2

4(x^2 + 4x + 4) > 9x^2 - 6x + 1

4x^2 + 16x + 16 > 9x^2 - 6x + 1

0 > 5x^2 - 22x - 15

5x^2 - 22x - 15 < 0

解方程 5x^2 - 22x - 15 = 0：

x = (22 ± √(484 + 300)) / 10 = (22 ± √784) / 10 = (22 ± 28) / 10

x = 50/10 = 5 或 x = -6/10 = -3/5

二次项系数 5 > 0，开口向上，所以 5x^2 - 22x - 15 < 0 的解为：

-3/5 < x < 5

即 x ∈ (-3/5, 5)。

**例题 6**：解不等式 3|x - 1| <= 2|x + 2|。

**解**：

两边平方：

9(x - 1)^2 <= 4(x + 2)^2

9(x^2 - 2x + 1) <= 4(x^2 + 4x + 4)

9x^2 - 18x + 9 <= 4x^2 + 16x + 16

5x^2 - 34x - 7 <= 0

解方程 5x^2 - 34x - 7 = 0：

x = (34 ± √(1156 + 140)) / 10 = (34 ± √1296) / 10 = (34 ± 36) / 10

x = 70/10 = 7 或 x = -2/10 = -1/5

二次项系数 5 > 0，开口向上，所以 5x^2 - 34x - 7 <= 0 的解为：

-1/5 <= x <= 7

即 x ∈ [-1/5, 7]。

---

### 6.2.3 类型 |ax + b| <= cx + d

这类不等式的右边是线性表达式。解法有代数分类法和图形法两种。

**代数分类法**：根据 ax + b 的符号分情况讨论，解出后检查是否满足前提条件。

**图形法**：画出 y = |ax + b| 和 y = cx + d 的图像，找出前者在后者下方（或上方）的区间。

**例题 7**：解不等式 |x - 3| <= 2x + 1。

**解（代数分类法）**：

**情况 1**：x - 3 >= 0，即 x >= 3。

x - 3 <= 2x + 1 => -4 <= x

结合前提 x >= 3，得到 x >= 3。

**情况 2**：x - 3 < 0，即 x < 3。

-(x - 3) <= 2x + 1 => -x + 3 <= 2x + 1 => 2 <= 3x => x >= 2/3

结合前提 x < 3，得到 2/3 <= x < 3。

两种情况取并集：x >= 2/3，即 x ∈ [2/3, ∞)。

**例题 8**：解不等式 |2x + 5| > x + 4。

**解**：

**情况 1**：2x + 5 >= 0，即 x >= -5/2。

2x + 5 > x + 4 => x > -1

结合前提 x >= -5/2，得到 x > -1。

**情况 2**：2x + 5 < 0，即 x < -5/2。

-(2x + 5) > x + 4 => -2x - 5 > x + 4 => -3x > 9 => x < -3

结合前提 x < -5/2，得到 x < -3。

解集为 x ∈ (-∞, -3) ∪ (-1, ∞)。

**例题 9**：解不等式 |x + 2| <= 3x - 1。

**解**：

**情况 1**：x + 2 >= 0，即 x >= -2。

x + 2 <= 3x - 1 => 3 <= 2x => x >= 3/2

结合前提 x >= -2，得到 x >= 3/2。

**情况 2**：x + 2 < 0，即 x < -2。

-(x + 2) <= 3x - 1 => -x - 2 <= 3x - 1 => -1 <= 4x => x >= -1/4

但前提是 x < -2，而 -1/4 > -2，无有效解。

因此解集为 x >= 3/2，即 x ∈ [3/2, ∞)。

---

### 6.2.4 类型 |ax^2 + bx + c| > d 和 |ax^2 + bx + c| <= d

处理思路：去掉绝对值，转化为两个二次不等式，分别求解后取并集或交集。

**例题 10**：解不等式 |x^2 - 3x| <= 4。

**解**：

由 |f(x)| <= 4 得 -4 <= x^2 - 3x <= 4。

**左边不等式**：x^2 - 3x >= -4

x^2 - 3x + 4 >= 0

判别式 Δ = 9 - 16 = -7 < 0，二次项系数 1 > 0，所以 x^2 - 3x + 4 > 0 对所有 x 恒成立。左边不等式自动满足。

**右边不等式**：x^2 - 3x <= 4

x^2 - 3x - 4 <= 0

(x - 4)(x + 1) <= 0

解为 -1 <= x <= 4。

因此原不等式的解集为 x ∈ [-1, 4]。

**例题 11**：解不等式 |x^2 - 2x - 3| > 3。

**解**：

由 |f(x)| > 3 得 x^2 - 2x - 3 < -3 或 x^2 - 2x - 3 > 3。

**不等式 1**：x^2 - 2x - 3 < -3

x^2 - 2x < 0 => x(x - 2) < 0 => 0 < x < 2

**不等式 2**：x^2 - 2x - 3 > 3

x^2 - 2x - 6 > 0

解方程 x^2 - 2x - 6 = 0：

x = (2 ± √(4 + 24)) / 2 = (2 ± √28) / 2 = (2 ± 2√7) / 2 = 1 ± √7

二次项系数 1 > 0，开口向上，所以 x^2 - 2x - 6 > 0 的解为：

x < 1 - √7 或 x > 1 + √7

其中 1 - √7 ≈ 1 - 2.646 = -1.646，1 + √7 ≈ 3.646。

原不等式的解集为两个不等式解集的并集：

x ∈ (-∞, 1 - √7) ∪ (0, 2) ∪ (1 + √7, ∞)

**例题 12**：解不等式 |2x^2 + x - 1| <= 5。

**解**：

由 -5 <= 2x^2 + x - 1 <= 5。

**左边不等式**：2x^2 + x - 1 >= -5

2x^2 + x + 4 >= 0

判别式 Δ = 1 - 32 = -31 < 0，二次项系数 2 > 0，恒成立。

**右边不等式**：2x^2 + x - 1 <= 5

2x^2 + x - 6 <= 0

解方程 2x^2 + x - 6 = 0：

x = (-1 ± √(1 + 48)) / 4 = (-1 ± √49) / 4 = (-1 ± 7) / 4

x = 6/4 = 3/2 或 x = -8/4 = -2

二次项系数 2 > 0，开口向上，所以 2x^2 + x - 6 <= 0 的解为：

-2 <= x <= 3/2

因此解集为 x ∈ [-2, 3/2]。

---

## 6.3 代换法化为一元二次方程

有些方程乍看不是二次方程，但通过巧妙的**代换**可以转化为熟悉的一元二次方程。代换法的核心是识别出表达式中重复出现的结构，令其为 u，从而将原方程化简。

### 6.3.1 指数型代换

形如 a^(2x) + b·a^x + c = 0 的方程，令 u = a^x（u > 0），则 a^(2x) = (a^x)^2 = u^2。

对于形如 3e^x = 12 - 5e^(-x) 的方程，两边乘以 e^x 后令 u = e^x。

**例题 1**：解方程 4^x - 5·2^x + 4 = 0。

**解**：

注意 4^x = (2^2)^x = (2^x)^2。令 u = 2^x > 0，则：

u^2 - 5u + 4 = 0

(u - 1)(u - 4) = 0

u = 1 或 u = 4

回代 u = 2^x：

- 2^x = 1 => x = 0
- 2^x = 4 => x = 2

因此解为 x = 0 和 x = 2。

**例题 2**：解方程 2e^x = 7 - 3e^(-x)。

**解**：

两边乘以 e^x（e^x > 0，不会引入增根）：

2e^(2x) = 7e^x - 3

2e^(2x) - 7e^x + 3 = 0

令 u = e^x > 0，则：

2u^2 - 7u + 3 = 0

(2u - 1)(u - 3) = 0

u = 1/2 或 u = 3

回代 u = e^x：

- e^x = 1/2 => x = ln(1/2) = -ln 2
- e^x = 3 => x = ln 3

因此解为 x = -ln 2 和 x = ln 3。

**例题 3**：解方程 3^(2x+1) - 10·3^x + 3 = 0。

**解**：

注意 3^(2x+1) = 3·3^(2x) = 3(3^x)^2。令 u = 3^x > 0，则：

3u^2 - 10u + 3 = 0

(3u - 1)(u - 3) = 0

u = 1/3 或 u = 3

回代 u = 3^x：

- 3^x = 1/3 = 3^(-1) => x = -1
- 3^x = 3 => x = 1

因此解为 x = -1 和 x = 1。

---

### 6.3.2 对数型代换

形如 (ln x)^2 + a ln x + b = 0 或 2(ln 5x)^2 + ln 5x - 6 = 0 的方程，令 u = ln(g(x))。

**例题 4**：解方程 (ln x)^2 - 3 ln x + 2 = 0。

**解**：

令 u = ln x，则：

u^2 - 3u + 2 = 0

(u - 1)(u - 2) = 0

u = 1 或 u = 2

回代 u = ln x：

- ln x = 1 => x = e^1 = e
- ln x = 2 => x = e^2

因此解为 x = e 和 x = e^2。

**例题 5**：解方程 2(ln 5x)^2 + ln 5x - 6 = 0。

**解**：

令 u = ln 5x，则：

2u^2 + u - 6 = 0

因式分解：

2u^2 + 4u - 3u - 6 = 0

2u(u + 2) - 3(u + 2) = 0

(u + 2)(2u - 3) = 0

u = -2 或 u = 3/2

回代 u = ln 5x：

- ln 5x = -2 => 5x = e^(-2) => x = e^(-2)/5
- ln 5x = 3/2 => 5x = e^(3/2) => x = e^(3/2)/5

因此解为 x = e^(-2)/5 和 x = e^(3/2)/5。

**例题 6**：解方程 log_3 x + log_x 3 = 2。

**解**：

利用换底公式 log_x 3 = (log_3 3) / (log_3 x) = 1 / (log_3 x)。

令 u = log_3 x（注意 x > 0 且 x ≠ 1，所以 u ≠ 0），则：

u + 1/u = 2

u^2 + 1 = 2u

u^2 - 2u + 1 = 0

(u - 1)^2 = 0

u = 1

回代：log_3 x = 1 => x = 3^1 = 3。

验证：log_3 3 + log_3 3 = 1 + 1 = 2 ✓。

---

### 6.3.3 根式型代换

形如 x - 6√x + 8 = 0 的方程，令 u = √x（u >= 0），则 x = u^2。

更一般地，形如 x^(2/3) - 4x^(1/3) + 2 = 0 的方程，令 u = x^(1/3)，则 x^(2/3) = u^2。

**例题 7**：解方程 x - 7√x + 12 = 0。

**解**：

令 u = √x >= 0，则 x = u^2。

u^2 - 7u + 12 = 0

(u - 3)(u - 4) = 0

u = 3 或 u = 4

回代 u = √x：

- √x = 3 => x = 9
- √x = 4 => x = 16

验证：9 - 7√9 + 12 = 9 - 21 + 12 = 0 ✓，16 - 7√16 + 12 = 16 - 28 + 12 = 0 ✓。

**例题 8**：解方程 x^(2/3) - 4x^(1/3) + 3 = 0。

**解**：

令 u = x^(1/3)，则 x^(2/3) = u^2。

u^2 - 4u + 3 = 0

(u - 1)(u - 3) = 0

u = 1 或 u = 3

回代 u = x^(1/3)：

- x^(1/3) = 1 => x = 1^3 = 1
- x^(1/3) = 3 => x = 3^3 = 27

验证：1^(2/3) - 4(1)^(1/3) + 3 = 1 - 4 + 3 = 0 ✓，27^(2/3) - 4(27)^(1/3) + 3 = 9 - 12 + 3 = 0 ✓。

**例题 9**：解方程 2x + 3√x - 2 = 0。

**解**：

令 u = √x >= 0，则 x = u^2。

2u^2 + 3u - 2 = 0

(2u - 1)(u + 2) = 0

u = 1/2 或 u = -2

u = √x >= 0，所以 u = -2 无效。

回代：√x = 1/2 => x = 1/4。

验证：2(1/4) + 3√(1/4) - 2 = 1/2 + 3/2 - 2 = 0 ✓。

---

### 6.3.4 分式型代换

形如 x^2 + 1/x^2 + a(x + 1/x) + b = 0 的方程，利用 (x + 1/x)^2 = x^2 + 2 + 1/x^2 的关系，令 u = x + 1/x。

**例题 10**：解方程 x^2 + 1/x^2 - 5(x + 1/x) + 6 = 0。

**解**：

令 u = x + 1/x，则 u^2 = x^2 + 2 + 1/x^2，所以 x^2 + 1/x^2 = u^2 - 2。

原方程化为：

(u^2 - 2) - 5u + 6 = 0

u^2 - 5u + 4 = 0

(u - 1)(u - 4) = 0

u = 1 或 u = 4

**回代 u = 1**：x + 1/x = 1

两边乘以 x（x ≠ 0）：x^2 + 1 = x => x^2 - x + 1 = 0。

判别式 Δ = 1 - 4 = -3 < 0，无实数解。

**回代 u = 4**：x + 1/x = 4

x^2 + 1 = 4x => x^2 - 4x + 1 = 0

x = (4 ± √(16 - 4)) / 2 = (4 ± √12) / 2 = (4 ± 2√3) / 2 = 2 ± √3

因此解为 x = 2 + √3 和 x = 2 - √3。

---

### 6.3.5 三角型代换（使用恒等式）

形如 sin^2 x + sin x - 2 = 0 的方程，令 u = sin x，但必须注意 u ∈ [-1, 1] 的定义域限制。

**例题 11**：解方程 2cos^2 x + 3sin x - 3 = 0，x ∈ [0, 2π)。

**解**：

利用恒等式 cos^2 x = 1 - sin^2 x：

2(1 - sin^2 x) + 3sin x - 3 = 0

2 - 2sin^2 x + 3sin x - 3 = 0

-2sin^2 x + 3sin x - 1 = 0

乘以 -1：

2sin^2 x - 3sin x + 1 = 0

令 u = sin x，u ∈ [-1, 1]：

2u^2 - 3u + 1 = 0

(2u - 1)(u - 1) = 0

u = 1/2 或 u = 1

回代：

- sin x = 1/2：在 [0, 2π) 上，x = π/6 或 x = 5π/6
- sin x = 1：在 [0, 2π) 上，x = π/2

因此解为 x = π/6, π/2, 5π/6。

---

## 6.4 三次多项式图像与不等式

### 6.4.1 三个线性因式乘积的图像特征

三次多项式 f(x) = (x - a)(x - b)(x - c)（其中 a < b < c）的图像具有以下特征：

- **与 x 轴的交点**：x = a, x = b, x = c（三个实数根）
- **端部行为**：若最高次项系数为正，当 x → ∞ 时 f(x) → ∞；当 x → -∞ 时 f(x) → -∞
- **图像形状**：从第三象限进入，依次穿过 x = a, x = b, x = c，进入第一象限
- **在每个区间上的符号**：

| 区间 | (-∞, a) | (a, b) | (b, c) | (c, ∞) |
|------|--------|--------|--------|--------|
| (x-a) | − | + | + | + |
| (x-b) | − | − | + | + |
| (x-c) | − | − | − | + |
| f(x) 符号 | − | + | − | + |

**例题 1**：绘制 f(x) = (x + 2)(x - 1)(x - 3) 的草图。

**解**：

**x 截距**：f(x) = 0 => x = -2, 1, 3

**y 截距**：f(0) = (0 + 2)(0 - 1)(0 - 3) = 2 × (-1) × (-3) = 6，点 (0, 6)

**端部行为**：展开后首项为 x^3，系数为正。x → -∞ 时 f(x) → -∞；x → ∞ 时 f(x) → ∞

**符号表**：

| 区间 | (-∞, -2) | (-2, 1) | (1, 3) | (3, ∞) |
|------|---------|--------|--------|--------|
| f(x) | − | + | − | + |

图像从第三象限进入，在 x = -2 处穿过 x 轴向上，经过 (0, 6)，在 x = 1 处再次穿过 x 轴向下，到达局部低点后上升，在 x = 3 处第三次穿过 x 轴，最终向右上方延伸。

**例题 2**：绘制 f(x) = (2x - 1)(x + 1)(x - 2) 的草图。

**解**：

**x 截距**：(2x - 1)(x + 1)(x - 2) = 0 => x = 1/2, -1, 2

排序后：x = -1, 1/2, 2

**y 截距**：f(0) = (0 - 1)(0 + 1)(0 - 2) = (-1) × 1 × (-2) = 2，点 (0, 2)

**端部行为**：首项为 2x·x·x = 2x^3，系数为正（2 > 0）。

**符号表**：

| 区间 | (-∞, -1) | (-1, 1/2) | (1/2, 2) | (2, ∞) |
|------|---------|-----------|----------|--------|
| (2x-1) | − | − | + | + |
| (x+1) | − | + | + | + |
| (x-2) | − | − | − | + |
| f(x) | − | + | − | + |

**例题 3**：绘制 f(x) = -(x + 3)(x - 1)(x - 4) 的草图。

**解**：

注意首项系数为负：-(x)(x)(x) = -x^3。x 截距为 -3, 1, 4。

**端部行为**：x → -∞ 时 f(x) → ∞（因为负三次项，从第二象限进入）；x → ∞ 时 f(x) → -∞。

**y 截距**：f(0) = -(3)(-1)(-4) = -(3)(-1)(-4) = -(12) = -12，点 (0, -12)

**符号表**：

| 区间 | (-∞, -3) | (-3, 1) | (1, 4) | (4, ∞) |
|------|---------|--------|--------|--------|
| -(x+3) | +（负×负） | −（负×正） | − | − |
| (x-1) | − | − | + | + |
| (x-4) | − | − | − | + |
| f(x) | + | − | + | − |

---

### 6.4.2 绝对值三次函数 y = |f(x)| 的图像

y = |f(x)| 的图像可以通过取 y = f(x) 图像中在 x 轴以下的部分，关于 x 轴向上反射得到：

|f(x)| = { f(x), f(x) >= 0; -f(x), f(x) < 0 }

**例题 4**：绘制 y = |(x + 2)(x - 1)(x - 3)| 的草图。

**解**：

先画出 f(x) = (x + 2)(x - 1)(x - 3) 的图像。

f(x) 为负的区间：(-∞, -2) 和 (1, 3)。

将这些部分关于 x 轴反射到上方。

最终图像特征：
- x 截距保持不变：x = -2, 1, 3（在这些点处图像"触碰" x 轴但不穿过）
- 整个图像位于 x 轴上方或与 x 轴相切
- 原来 (-∞, -2) 和 (1, 3) 上的波谷变成了波峰
- 原来 (-2, 1) 上的波峰保持在上方

**例题 5**：绘制 y = |(x - 1)(x - 2)(x - 4)| 的草图，并标注坐标轴交点。

**解**：

f(x) = (x - 1)(x - 2)(x - 4) 的 x 截距为 1, 2, 4。

f(x) 的符号：

| 区间 | (-∞, 1) | (1, 2) | (2, 4) | (4, ∞) |
|------|---------|--------|--------|--------|
| f(x) | − | + | − | + |

f(x) 为负的区间：(-∞, 1) 和 (2, 4)。将这些部分向上反射。

y 截距：|f(0)| = |(-1)(-2)(-4)| = |-8| = 8，点 (0, 8)。

**例题 6**：判断方程 |(x + 1)(x - 2)(x - 5)| = k（k > 0）的解的个数如何随 k 变化。

**解**：

画出 y = |(x + 1)(x - 2)(x - 5)| 的草图。x 截距为 -1, 2, 5。

f(x) = (x + 1)(x - 2)(x - 5) 的符号：

| 区间 | (-∞, -1) | (-1, 2) | (2, 5) | (5, ∞) |
|------|---------|--------|--------|--------|
| f(x) | − | + | − | + |

负区间（向上反射）：(-∞, -1) 和 (2, 5)。

设 M1 为 (-1, 2) 区间内 f(x) 的最大值，M2 为 (2, 5) 区间内 |f(x)| 的最大值（即原 f(x) 在 (2,5) 上的最小值的绝对值）。

- 若 0 < k < min(M1, M2)：6 个解（水平线与图像的 6 个交点）
- 若 k = M1 或 k = M2：某些交点重合，解数减少
- 若 k > max(M1, M2)：2 个解

> **注**：此类问题通常出现在较难的题目中，需要结合导数求局部极值。

---

### 6.4.3 三次不等式的图形解法

对于 f(x) >= d（或 >, <=, <），其中 f(x) 是三个线性因式的乘积：

**图形解法步骤**：

1. 画出 y = f(x) 的草图（标注三个 x 截距和 y 截距）
2. 画出水平线 y = d
3. 找出 f(x) 图像在水平线上方（对 f(x) > d）或下方（对 f(x) < d）的区间
4. 必要时求交点坐标

**例题 7**：解不等式 (x + 1)(x - 2)(x - 4) >= 0。

**解**：

f(x) = (x + 1)(x - 2)(x - 4)，d = 0（即与 x 轴比较）。

三个根为 -1, 2, 4，首项系数为正。

符号表：

| 区间 | (-∞, -1) | (-1, 2) | (2, 4) | (4, ∞) |
|------|---------|--------|--------|--------|
| f(x) | − | + | − | + |

f(x) >= 0 的解为 x ∈ [-1, 2] ∪ [4, ∞)。

**例题 8**：解不等式 (x - 1)(x - 3)(x - 5) < 0。

**解**：

三个根为 1, 3, 5，首项系数为正。

符号表：

| 区间 | (-∞, 1) | (1, 3) | (3, 5) | (5, ∞) |
|------|---------|--------|--------|--------|
| f(x) | − | + | − | + |

f(x) < 0 的解为 x ∈ (-∞, 1) ∪ (3, 5)。

**例题 9**：已知 f(x) = (2x + 1)(x - 2)(x - 3)，解不等式 f(x) <= 0。

**解**：

零点：2x + 1 = 0 => x = -1/2，以及 x = 2, x = 3。

排序后：-1/2, 2, 3。

首项系数：2x·x·x = 2x^3，系数为正。

符号表：

| 区间 | (-∞, -1/2) | (-1/2, 2) | (2, 3) | (3, ∞) |
|------|------------|----------|--------|--------|
| (2x+1) | − | + | + | + |
| (x-2) | − | − | + | + |
| (x-3) | − | − | − | + |
| f(x) | − | + | − | + |

f(x) <= 0 的解为 x ∈ (-∞, -1/2] ∪ [2, 3]。

---

## 6.5 联立方程组

### 6.5.1 联立方程组的图形意义

两个联立方程 { y = f(x), y = g(x) } 的解就是两个函数图像**交点**的坐标。

### 6.5.2 直线与直线的联立

解二元一次方程组最常用的方法是**消元法**和**代入法**。

**例题 1**：解方程组 { 3x + 2y = 7, 5x - 3y = 37 }。

**解（消元法）**：

将第一个方程乘以 3，第二个方程乘以 2：

{ 9x + 6y = 21, 10x - 6y = 74 }

相加：19x = 95 => x = 5

代入第一个方程：3(5) + 2y = 7 => 15 + 2y = 7 => 2y = -8 => y = -4

因此解为 (x, y) = (5, -4)。

**例题 2**：解方程组 { 2x - 5y = 3, 4x + y = 17 }。

**解（代入法）**：

由第二个方程：y = 17 - 4x。

代入第一个方程：

2x - 5(17 - 4x) = 3

2x - 85 + 20x = 3

22x = 88

x = 4

代入 y = 17 - 4(4) = 1

因此解为 (x, y) = (4, 1)。

**例题 3**：解方程组 { x/2 + y/3 = 4, x/4 - y/2 = 0 }。

**解**：

先消去分母。第一个方程乘以 6，第二个方程乘以 4：

{ 3x + 2y = 24, x - 2y = 0 }

两式相加：4x = 24 => x = 6

代入 x - 2y = 0 => 6 - 2y = 0 => y = 3

因此解为 (x, y) = (6, 3)。

---

### 6.5.3 直线与曲线的联立

一般用**代入法**：从一次方程中解出一个变量，代入二次方程，得到一个一元二次方程。判别式 Δ 决定交点的个数：

- Δ > 0：两个不同交点（相交于两点）
- Δ = 0：一个交点（相切）
- Δ < 0：无交点（不相交）

**例题 4**：求直线 y = 2x - 1 与曲线 y = x^2 - 2x + 2 的交点。

**解**：

令 2x - 1 = x^2 - 2x + 2：

0 = x^2 - 4x + 3

(x - 1)(x - 3) = 0

x = 1 或 x = 3

代入 y = 2x - 1：

- x = 1：y = 1，交点 (1, 1)
- x = 3：y = 5，交点 (3, 5)

**例题 5**：求 k 的值，使得直线 y = 3x + k 与曲线 y = x^2 - 4x + 7 相切。

**解**：

令 3x + k = x^2 - 4x + 7：

0 = x^2 - 7x + 7 - k

相切条件：Δ = 0

Δ = (-7)^2 - 4(1)(7 - k) = 49 - 28 + 4k = 21 + 4k = 0

k = -21/4

当 k = -21/4 时，直线与曲线相切。

切点：x^2 - 7x + 7 - (-21/4) = x^2 - 7x + 7 + 21/4 = x^2 - 7x + 49/4 = (x - 7/2)^2 = 0

所以 x = 7/2，y = 3(7/2) - 21/4 = 42/4 - 21/4 = 21/4。

切点为 (7/2, 21/4)。

**例题 6**：判断直线 y = 2x + 5 与圆 x^2 + (y - 1)^2 = 5 的位置关系。

**解**：

代入 y = 2x + 5：

x^2 + (2x + 5 - 1)^2 = 5

x^2 + (2x + 4)^2 = 5

x^2 + 4x^2 + 16x + 16 = 5

5x^2 + 16x + 11 = 0

判别式 Δ = 16^2 - 4(5)(11) = 256 - 220 = 36 > 0

因此直线与圆相交于两个不同点。

解方程 5x^2 + 16x + 11 = 0：

x = (-16 ± √36) / 10 = (-16 ± 6) / 10

x = -1 或 x = -11/5

对应 y = 2(-1) + 5 = 3 和 y = 2(-11/5) + 5 = -22/5 + 5 = 3/5。

交点为 (-1, 3) 和 (-11/5, 3/5)。

---

### 6.5.4 曲线与曲线的联立

当两个方程都是二次（或更高次）时，代入后可能得到一个高次方程，但通常可以通过因式分解或巧妙的代换来简化。

**例题 7**：解方程组 { x^2 + y^2 = 10, y = 3x }。

**解**：

代入 y = 3x 到圆的方程：

x^2 + (3x)^2 = 10

x^2 + 9x^2 = 10

10x^2 = 10

x^2 = 1

x = ±1

对应 y = 3(±1) = ±3。

解为 (1, 3) 和 (-1, -3)。

**例题 8**：解方程组 { x^2 + y^2 = 41, xy = 20 }。

**解**：

由 xy = 20 得 y = 20/x（x ≠ 0）。代入第一个方程：

x^2 + (20/x)^2 = 41

x^2 + 400/x^2 = 41

乘以 x^2：

x^4 + 400 = 41x^2

x^4 - 41x^2 + 400 = 0

令 u = x^2 >= 0：

u^2 - 41u + 400 = 0

(u - 16)(u - 25) = 0

u = 16 或 u = 25

x^2 = 16 => x = ±4，对应 y = 20/(±4) = ±5

x^2 = 25 => x = ±5，对应 y = 20/(±5) = ±4

因此解为 (4, 5)、(-4, -5)、(5, 4)、(-5, -4)。

**例题 9**：解方程组 { y - x + 3 = 0, x^2 - 3xy + y^2 + 19 = 0 }。

**解**：

由第一个方程：y = x - 3。

代入第二个方程：

x^2 - 3x(x - 3) + (x - 3)^2 + 19 = 0

x^2 - 3x^2 + 9x + x^2 - 6x + 9 + 19 = 0

-x^2 + 3x + 28 = 0

乘以 -1：

x^2 - 3x - 28 = 0

(x - 7)(x + 4) = 0

x = 7 或 x = -4

对应 y = 7 - 3 = 4 和 y = -4 - 3 = -7。

解为 (7, 4) 和 (-4, -7)。

---

## 练习题

### A组：绝对值方程

**A1**：解方程 |4x - 3| = 9。

**A2**：解方程 |5 - 3x| = 7。

**A3**：解方程 |2x + 1| = x + 5。

**A4**：解方程 |x - 4| = 2x - 5。

**A5**：解方程 |3x + 2| = |x - 6|。

**A6**：解方程 |2x - 5| = |4x + 3|。

**A7**：解方程 |x^2 - 5x + 6| = 2。

**A8**：解方程 |x^2 - 2x - 3| = 3。

---

### B组：绝对值不等式

**B1**：解不等式 |3x + 1| > 7。

**B2**：解不等式 2|5 - x| <= 8。

**B3**：解不等式 |2x - 3| <= |x + 2|。

**B4**：解不等式 2|x + 1| > |3x - 2|。

**B5**：解不等式 |x + 1| <= 2x + 3。

**B6**：解不等式 |2x - 3| > x + 1。

**B7**：解不等式 |x^2 - 4| <= 5。

**B8**：解不等式 |x^2 - 3x| > 2。

---

### C组：代换法

**C1**：解方程 2^(2x) - 6·2^x + 8 = 0。

**C2**：解方程 e^(2x) - 5e^x + 6 = 0。

**C3**：解方程 5e^x = 8 - 3e^(-x)。

**C4**：解方程 (ln x)^2 + ln x - 6 = 0。

**C5**：解方程 2(log_3 x)^2 - 5log_3 x + 2 = 0。

**C6**：解方程 x - 6√x + 5 = 0。

**C7**：解方程 x^(2/3) - 2x^(1/3) - 3 = 0。

**C8**：解方程 x^2 + 1/x^2 - 3(x + 1/x) + 2 = 0。

---

### D组：三次多项式图像与不等式

**D1**：画出 f(x) = (x + 3)(x - 2)(x - 5) 的草图，标注坐标轴交点。

**D2**：画出 f(x) = (2x + 3)(x - 1)(x - 4) 的草图。

**D3**：画出 y = |(x + 3)(x - 2)(x - 5)| 的草图。

**D4**：解不等式 (x + 2)(x - 1)(x - 4) >= 0。

**D5**：解不等式 (x - 1)(x - 3)(x - 6) < 0。

**D6**：已知 f(x) = (x + 1)(x - 2)(x - 5)，解不等式 f(x) <= 0。

---

### E组：联立方程组

**E1**：解方程组 { 2x + 3y = 8, 5x - 2y = 1 }。

**E2**：解方程组 { 4x - 3y = 11, 3x + 2y = 21 }。

**E3**：求直线 y = 3x - 2 与抛物线 y = x^2 的交点。

**E4**：求直线 y = 2x + 1 与曲线 y = x^2 - 3x + 5 的交点。

**E5**：求 k 的值，使得直线 y = x + k 与曲线 y = x^2 - 5x + 7 相切。

**E6**：解方程组 { x^2 + y^2 = 13, y = 2x - 1 }。

**E7**：解方程组 { x^2 + y^2 = 25, xy = 12 }。

**E8**：解方程组 { x^2 - 2xy + y^2 = 1, x + y = 3 }。

---

## 练习题答案

### A组答案

**A1**：|4x - 3| = 9

4x - 3 = 9 或 4x - 3 = -9

4x = 12 或 4x = -6

x = 3 或 x = -3/2

**A2**：|5 - 3x| = 7

5 - 3x = 7 或 5 - 3x = -7

-3x = 2 或 -3x = -12

x = -2/3 或 x = 4

**A3**：|2x + 1| = x + 5

情况 1（x >= -1/2）：2x + 1 = x + 5 => x = 4 ✓

情况 2（x < -1/2）：-(2x + 1) = x + 5 => -2x - 1 = x + 5 => -3x = 6 => x = -2 ✓

解：x = 4 和 x = -2

**A4**：|x - 4| = 2x - 5

情况 1（x >= 4）：x - 4 = 2x - 5 => -x = -1 => x = 1，但 1 >= 4 不成立 ✗

情况 2（x < 4）：-(x - 4) = 2x - 5 => -x + 4 = 2x - 5 => 9 = 3x => x = 3，3 < 4 ✓

解：x = 3

**A5**：|3x + 2| = |x - 6|

3x + 2 = x - 6 或 3x + 2 = -(x - 6)

2x = -8 或 3x + 2 = -x + 6

x = -4 或 4x = 4

x = -4 或 x = 1

**A6**：|2x - 5| = |4x + 3|

2x - 5 = 4x + 3 或 2x - 5 = -(4x + 3)

-2x = 8 或 2x - 5 = -4x - 3

x = -4 或 6x = 2

x = -4 或 x = 1/3

**A7**：|x^2 - 5x + 6| = 2

x^2 - 5x + 6 = 2 或 x^2 - 5x + 6 = -2

x^2 - 5x + 4 = 0 或 x^2 - 5x + 8 = 0

(x - 1)(x - 4) = 0，Δ = 25 - 32 = -7 < 0，无解

x = 1 或 x = 4

**A8**：|x^2 - 2x - 3| = 3

x^2 - 2x - 3 = 3 或 x^2 - 2x - 3 = -3

x^2 - 2x - 6 = 0 或 x^2 - 2x = 0

x = (2 ± √(4 + 24)) / 2 = (2 ± √28) / 2 = 1 ± √7 或 x(x - 2) = 0 => x = 0 或 x = 2

解：x = 1 ± √7, 0, 2

---

### B组答案

**B1**：|3x + 1| > 7

3x + 1 < -7 或 3x + 1 > 7

3x < -8 或 3x > 6

x < -8/3 或 x > 2

x ∈ (-∞, -8/3) ∪ (2, ∞)

**B2**：2|5 - x| <= 8

|5 - x| <= 4

-4 <= 5 - x <= 4

左边：-4 <= 5 - x => x <= 9

右边：5 - x <= 4 => -x <= -1 => x >= 1

x ∈ [1, 9]

**B3**：|2x - 3| <= |x + 2|

(2x - 3)^2 <= (x + 2)^2

4x^2 - 12x + 9 <= x^2 + 4x + 4

3x^2 - 16x + 5 <= 0

(3x - 1)(x - 5) <= 0

x ∈ [1/3, 5]

**B4**：2|x + 1| > |3x - 2|

4(x + 1)^2 > (3x - 2)^2

4(x^2 + 2x + 1) > 9x^2 - 12x + 4

4x^2 + 8x + 4 > 9x^2 - 12x + 4

0 > 5x^2 - 20x

5x^2 - 20x < 0

5x(x - 4) < 0

0 < x < 4

x ∈ (0, 4)

**B5**：|x + 1| <= 2x + 3

情况 1（x >= -1）：x + 1 <= 2x + 3 => -2 <= x，结合 x >= -1 得 x >= -1

情况 2（x < -1）：-(x + 1) <= 2x + 3 => -x - 1 <= 2x + 3 => -4 <= 3x => x >= -4/3

结合 x < -1 得 -4/3 <= x < -1

并集：x >= -4/3，即 x ∈ [-4/3, ∞)

**B6**：|2x - 3| > x + 1

情况 1（x >= 3/2）：2x - 3 > x + 1 => x > 4，结合前提得 x > 4

情况 2（x < 3/2）：-(2x - 3) > x + 1 => -2x + 3 > x + 1 => 2 > 3x => x < 2/3，结合前提得 x < 2/3

x ∈ (-∞, 2/3) ∪ (4, ∞)

**B7**：|x^2 - 4| <= 5

-5 <= x^2 - 4 <= 5

左边：x^2 - 4 >= -5 => x^2 >= -1，恒成立

右边：x^2 - 4 <= 5 => x^2 <= 9 => -3 <= x <= 3

x ∈ [-3, 3]

**B8**：|x^2 - 3x| > 2

x^2 - 3x < -2 或 x^2 - 3x > 2

不等式 1：x^2 - 3x + 2 < 0 => (x - 1)(x - 2) < 0 => 1 < x < 2

不等式 2：x^2 - 3x - 2 > 0

x = (3 ± √(9 + 8)) / 2 = (3 ± √17) / 2

x < (3 - √17)/2 或 x > (3 + √17)/2

其中 (3 - √17)/2 ≈ (3 - 4.123)/2 ≈ -0.562，(3 + √17)/2 ≈ (3 + 4.123)/2 ≈ 3.562

解集为 x ∈ (-∞, (3 - √17)/2) ∪ (1, 2) ∪ ((3 + √17)/2, ∞)

---

### C组答案

**C1**：2^(2x) - 6·2^x + 8 = 0

令 u = 2^x > 0：u^2 - 6u + 8 = 0 => (u - 2)(u - 4) = 0

u = 2 或 u = 4

2^x = 2 => x = 1；2^x = 4 => x = 2

**C2**：e^(2x) - 5e^x + 6 = 0

令 u = e^x > 0：u^2 - 5u + 6 = 0 => (u - 2)(u - 3) = 0

u = 2 或 u = 3

e^x = 2 => x = ln 2；e^x = 3 => x = ln 3

**C3**：5e^x = 8 - 3e^(-x)

乘以 e^x：5e^(2x) = 8e^x - 3

5e^(2x) - 8e^x + 3 = 0

令 u = e^x > 0：5u^2 - 8u + 3 = 0 => (5u - 3)(u - 1) = 0

u = 3/5 或 u = 1

e^x = 3/5 => x = ln(3/5)；e^x = 1 => x = 0

**C4**：(ln x)^2 + ln x - 6 = 0

令 u = ln x：u^2 + u - 6 = 0 => (u + 3)(u - 2) = 0

u = -3 或 u = 2

ln x = -3 => x = e^(-3)；ln x = 2 => x = e^2

**C5**：2(log_3 x)^2 - 5log_3 x + 2 = 0

令 u = log_3 x：2u^2 - 5u + 2 = 0 => (2u - 1)(u - 2) = 0

u = 1/2 或 u = 2

log_3 x = 1/2 => x = 3^(1/2) = √3；log_3 x = 2 => x = 3^2 = 9

**C6**：x - 6√x + 5 = 0

令 u = √x >= 0：u^2 - 6u + 5 = 0 => (u - 1)(u - 5) = 0

u = 1 或 u = 5

√x = 1 => x = 1；√x = 5 => x = 25

**C7**：x^(2/3) - 2x^(1/3) - 3 = 0

令 u = x^(1/3)：u^2 - 2u - 3 = 0 => (u - 3)(u + 1) = 0

u = 3 或 u = -1

x^(1/3) = 3 => x = 27；x^(1/3) = -1 => x = -1

**C8**：x^2 + 1/x^2 - 3(x + 1/x) + 2 = 0

令 u = x + 1/x，则 u^2 = x^2 + 2 + 1/x^2 => x^2 + 1/x^2 = u^2 - 2

(u^2 - 2) - 3u + 2 = 0 => u^2 - 3u = 0 => u(u - 3) = 0

u = 0 或 u = 3

u = 0：x + 1/x = 0 => x^2 + 1 = 0，无实数解

u = 3：x + 1/x = 3 => x^2 - 3x + 1 = 0 => x = (3 ± √5)/2

---

### D组答案

**D1**：f(x) = (x + 3)(x - 2)(x - 5)

x 截距：-3, 2, 5

y 截距：f(0) = 3 × (-2) × (-5) = 30，点 (0, 30)

首项系数为正。当 x → -∞，f(x) → -∞；当 x → ∞，f(x) → ∞

符号：(-∞, -3)：−；(-3, 2)：+；(2, 5)：−；(5, ∞)：+

**D2**：f(x) = (2x + 3)(x - 1)(x - 4)

x 截距：-3/2, 1, 4

y 截距：f(0) = 3 × (-1) × (-4) = 12，点 (0, 12)

首项系数 2 > 0，端部行为同 D1。

符号：(-∞, -3/2)：−；(-3/2, 1)：+；(1, 4)：−；(4, ∞)：+

**D3**：y = |(x + 3)(x - 2)(x - 5)|

将 f(x) 在 (-∞, -3) 和 (2, 5) 上的负值部分向上反射。x 截距仍为 -3, 2, 5。y 截距为 |30| = 30。图像全部在 x 轴上方（含 x 轴上的点）。

**D4**：(x + 2)(x - 1)(x - 4) >= 0

根：-2, 1, 4，首项系数为正。

符号：(-∞, -2)：−；(-2, 1)：+；(1, 4)：−；(4, ∞)：+

解：x ∈ [-2, 1] ∪ [4, ∞)

**D5**：(x - 1)(x - 3)(x - 6) < 0

根：1, 3, 6，首项系数为正。

符号：(-∞, 1)：−；(1, 3)：+；(3, 6)：−；(6, ∞)：+

解：x ∈ (-∞, 1) ∪ (3, 6)

**D6**：f(x) = (x + 1)(x - 2)(x - 5) <= 0

根：-1, 2, 5，首项系数为正。

符号：(-∞, -1)：−；(-1, 2)：+；(2, 5)：−；(5, ∞)：+

解：x ∈ (-∞, -1] ∪ [2, 5]

---

### E组答案

**E1**：{ 2x + 3y = 8, 5x - 2y = 1 }

第一个方程乘以 2，第二个乘以 3：{ 4x + 6y = 16, 15x - 6y = 3 }

相加：19x = 19 => x = 1

代入：2(1) + 3y = 8 => 3y = 6 => y = 2

解：(1, 2)

**E2**：{ 4x - 3y = 11, 3x + 2y = 21 }

第一个乘以 2，第二个乘以 3：{ 8x - 6y = 22, 9x + 6y = 63 }

相加：17x = 85 => x = 5

代入：4(5) - 3y = 11 => 20 - 3y = 11 => 3y = 9 => y = 3

解：(5, 3)

**E3**：y = 3x - 2 与 y = x^2

x^2 = 3x - 2 => x^2 - 3x + 2 = 0 => (x - 1)(x - 2) = 0

x = 1 或 x = 2

交点：(1, 1) 和 (2, 4)

**E4**：y = 2x + 1 与 y = x^2 - 3x + 5

2x + 1 = x^2 - 3x + 5 => 0 = x^2 - 5x + 4 => (x - 1)(x - 4) = 0

x = 1 或 x = 4

交点：(1, 3) 和 (4, 9)

**E5**：y = x + k 与 y = x^2 - 5x + 7 相切

x + k = x^2 - 5x + 7 => 0 = x^2 - 6x + 7 - k

Δ = (-6)^2 - 4(1)(7 - k) = 36 - 28 + 4k = 8 + 4k = 0

k = -2

**E6**：{ x^2 + y^2 = 13, y = 2x - 1 }

代入：x^2 + (2x - 1)^2 = 13 => x^2 + 4x^2 - 4x + 1 = 13 => 5x^2 - 4x - 12 = 0

(5x + 6)(x - 2) = 0 => x = -6/5 或 x = 2

y = 2(-6/5) - 1 = -12/5 - 1 = -17/5；y = 2(2) - 1 = 3

解：(-6/5, -17/5) 和 (2, 3)

**E7**：{ x^2 + y^2 = 25, xy = 12 }

由 xy = 12 得 y = 12/x（x ≠ 0）

代入：x^2 + 144/x^2 = 25 => x^4 - 25x^2 + 144 = 0

令 u = x^2 >= 0：u^2 - 25u + 144 = 0 => (u - 9)(u - 16) = 0

u = 9 => x = ±3，y = 12/(±3) = ±4

u = 16 => x = ±4，y = 12/(±4) = ±3

解：(3, 4)、(-3, -4)、(4, 3)、(-4, -3)

**E8**：{ x^2 - 2xy + y^2 = 1, x + y = 3 }

注意 x^2 - 2xy + y^2 = (x - y)^2 = 1，所以 x - y = ±1

与 x + y = 3 联立：

当 x - y = 1 时：{ x + y = 3, x - y = 1 } => x = 2, y = 1

当 x - y = -1 时：{ x + y = 3, x - y = -1 } => x = 1, y = 2

解：(2, 1) 和 (1, 2)

---

## 本章总结

| 知识点 | 核心方法 | 关键要点 |
|--------|---------|---------|
| **集合与区间** | 集合描述法、区间记号 | 开区间用圆括号，闭区间用方括号；∪ 表示并集 |
| **6.1 绝对值方程** | 分类讨论或两边平方 | |A| = B 需 B >= 0；|A| = |B| <=> A = ±B |
| **6.2 绝对值不等式** | 转化为不等式组或平方 | |A| > c <=> A < -c 或 A > c；|A| <= c <=> -c <= A <= c |
| **6.3 代换法** | 识别重复结构，令 u = g(x) | 注意回代后解的存在性和定义域（如 u >= 0、u ≠ 0 等） |
| **6.4 三次多项式图像与不等式** | 找三个 x 截距，符号分析 | 首项系数决定端部行为；绝对值图像将负部翻转 |
| **6.5 联立方程组** | 代入法 + 判别式 | Δ > 0 两交点，Δ = 0 相切，Δ < 0 无交点 |

---
---

## 第 7 章：积分（不定积分与定积分）

### 7.1 不定积分（反导数）

#### 7.1.1 从微分到积分——逆运算的本质

我们从最基本的问题开始。

**问题**：已知一个函数 F(x) 的导数为 2x，即 F'(x) = 2x，求 F(x)。

**思考过程**：在第 5 章中我们学过：

d/dx (x^2) = 2x

所以 x^2 是 2x 的一个"反导数"。但问题在于——常数的导数是 0，因此 x^2 + 1、x^2 - 5、x^2 + π 的导数也全都是 2x。这意味着 2x 的原函数有**无穷多个**，它们之间只相差一个常数。我们用 C 表示这个任意常数。

用积分符号表示这一过程：

**∫ 2x dx = x^2 + C**

其中：
- ∫ 称为**积分号**
- 2x 称为**被积函数**
- dx 表示对变量 x 积分
- C 称为**积分常数**

> **严格定义**：函数 F(x) 称为 f(x) 的一个**原函数**，如果 F'(x) = f(x) 对所有 x 在定义域内成立。f(x) 的所有原函数构成的集合称为**不定积分**，记作 ∫ f(x) dx = F(x) + C。

#### 7.1.2 积分与导数的互逆关系——验证法

由于积分是微分的逆运算，每一条积分公式都可以通过求导来验证。这是检查积分结果是否正确的最可靠方法。

**验证程序**：
1. 对积分结果 F(x) + C 求导
2. 检查导数是否等于被积函数 f(x)
3. 如果相等，积分正确

**示例验证 1**：求证 ∫ 3x^2 dx = x^3 + C

d/dx (x^3 + C) = 3x^2 (正确)

**示例验证 2**：求证 ∫ cos x dx = sin x + C

d/dx (sin x + C) = cos x (正确)

**示例验证 3**：求证 ∫ e^(2x) dx = (1/2)e^(2x) + C

d/dx ((1/2)e^(2x) + C) = (1/2) * e^(2x) * 2 = e^(2x) (正确)

---

**例题 1**（理解原函数的概念）：已知 f'(x) = 6x^2，且 f(1) = 3，求 f(x)。

**解**：

先求不定积分：

f(x) = ∫ 6x^2 dx = 6 * (x^3/3) + C = 2x^3 + C

利用条件 f(1) = 3 确定 C：

f(1) = 2(1)^3 + C = 2 + C = 3 => C = 1

因此 f(x) = 2x^3 + 1。

> 这是考试中常见的题型——已知导数和初始条件，求原函数。关键在于先积分得到含 C 的表达式，再代入条件解出 C。

---

**例题 2**（通过求导验证积分）：判断 ∫ 1/x^2 dx = -1/x + C 是否正确。

**解**：

对结果求导：

d/dx (-1/x + C) = d/dx (-x^(-1) + C) = x^(-2) = 1/x^2

导数为被积函数，因此积分正确。

---

**例题 3**（通过求导发现错误）：判断 ∫ (2x+1)^2 dx = (2x+1)^3/3 + C 是否正确。

**解**：

对结果求导：

d/dx ((2x+1)^3/3 + C) = (1/3) * 3(2x+1)^2 * 2 = 2(2x+1)^2 ≠ (2x+1)^2

多了因子 2，所以积分**不正确**！正确做法是：

∫ (2x+1)^2 dx = (2x+1)^3 / (2*3) + C = (2x+1)^3 / 6 + C

验证：d/dx ((2x+1)^3/6) = 3(2x+1)^2 * 2 / 6 = (2x+1)^2 (正确)

> ⚠️ **教训**：对于 (ax+b)^n 形式的积分，别忘了多出一个因子 1/a！这是初学者最常犯的错误之一。

---

#### 7.1.3 积分的线性性质

积分运算满足**线性性**。这一性质来源于导数的线性性，是积分中最基本的运算规则：

**∫ [a f(x) + b g(x)] dx = a ∫ f(x) dx + b ∫ g(x) dx**

其中 a、b 为任意常数。

这条性质告诉我们两件事：
1. **常数因子可以提到积分号外面**：∫ c f(x) dx = c ∫ f(x) dx
2. **和的积分等于积分之和**：∫ [f(x) + g(x)] dx = ∫ f(x) dx + ∫ g(x) dx

> ⚠️ **重要警告**：积分的线性性质**不等于**"乘积的积分等于积分的乘积"！
> ∫ f(x)g(x) dx ≠ ∫ f(x) dx * ∫ g(x) dx
> 也**不等于**"商的积分等于积分的商"！
> ∫ f(x)/g(x) dx ≠ (∫ f(x) dx) / (∫ g(x) dx)
> 在 IGCSE 0606 中，遇到乘积必须先**展开**再逐项积分。

---

**例题 1**（线性性质的基础应用）：求 ∫ (3x^2 - 5x + 2) dx。

**解**：

∫ (3x^2 - 5x + 2) dx = 3 ∫ x^2 dx - 5 ∫ x dx + 2 ∫ 1 dx

= 3 * (x^3/3) - 5 * (x^2/2) + 2x + C

= x^3 - (5/2)x^2 + 2x + C

**验证**：d/dx (x^3 - (5/2)x^2 + 2x + C) = 3x^2 - 5x + 2。正确。

---

**例题 2**（展开后再积分——乘积的处理方式）：求 ∫ (x+3)(x-2) dx。

**解**：

先展开：(x+3)(x-2) = x^2 - 2x + 3x - 6 = x^2 + x - 6

再逐项积分：

∫ (x^2 + x - 6) dx = x^3/3 + x^2/2 - 6x + C

> ⚠️ **不能**这样写：∫ (x+3)(x-2) dx = ∫ (x+3) dx * ∫ (x-2) dx

---

**例题 3**（展开多项式再积分）：求 ∫ (2x-1)^3 dx。

**解**：

方法一（展开）：

(2x-1)^3 = 8x^3 - 12x^2 + 6x - 1

∫ (8x^3 - 12x^2 + 6x - 1) dx = 8 * (x^4/4) - 12 * (x^3/3) + 6 * (x^2/2) - x + C

= 2x^4 - 4x^3 + 3x^2 - x + C

方法二（直接用 (ax+b)^n 公式）：

∫ (2x-1)^3 dx = (2x-1)^4 / (2*4) + C = (2x-1)^4 / 8 + C

两种方法答案形式上不同，但实质等价（展开后相同）。

---

**例题 4**（化简分式后再积分）：求 ∫ (x^3 + 3x^2 - 2) / x^2 dx。

**解**：

先化简：(x^3 + 3x^2 - 2) / x^2 = x + 3 - 2/x^2 = x + 3 - 2x^(-2)

再逐项积分：

∫ (x + 3 - 2x^(-2)) dx = x^2/2 + 3x - 2 * (x^(-1)/(-1)) + C

= x^2/2 + 3x + 2/x + C

> ⚠️ **常见错误**：不要对分式整体积分！必须先将分式拆成单项之和再逐项积分。

---
---

## 7.2 基本积分公式（完整推导与大量例题）

本节是**本章最核心的内容**。所有公式都必须熟练记忆，因为考试中**不提供公式表**。

### 7.2.1 幂函数积分公式：∫ x^n dx (n ≠ -1)

**公式**：

**∫ x^n dx = x^(n+1) / (n+1) + C (n ≠ -1)**

**推导**：对右端求导：

d/dx ( x^(n+1) / (n+1) + C ) = (n+1)/(n+1) * x^n = x^n

导数为被积函数 x^n，公式得证。

**理解要点**：
- **指数加 1**：n → n+1
- **除以新指数**：除以 (n+1)
- 该公式对**所有有理数** n ≠ -1 都成立，包括负数和分数

**常见指数形式速查**：

| 被积函数 | 改写为幂函数 | 积分结果 |
|---------|-------------|---------|
| x^5 | x^5 | x^6 / 6 |
| 1/x^3 | x^(-3) | x^(-2)/(-2) = -1/(2x^2) |
| √x | x^(1/2) | x^(3/2) / (3/2) = (2/3)x^(3/2) |
| 1/√x | x^(-1/2) | x^(1/2) / (1/2) = 2√x |
| ∛(x^2) | x^(2/3) | x^(5/3) / (5/3) = (3/5)x^(5/3) |

---

**例题 1**（正整数指数）：求 ∫ x^8 dx。

**解**：

∫ x^8 dx = x^(8+1) / (8+1) + C = x^9 / 9 + C

**验证**：d/dx (x^9 / 9) = 9x^8 / 9 = x^8。✓

---

**例题 2**（负指数）：求 ∫ 1/x^4 dx。

**解**：

先改写：1/x^4 = x^(-4)

∫ x^(-4) dx = x^(-4+1) / (-4+1) + C = x^(-3) / (-3) + C = -1/(3x^3) + C

**验证**：d/dx (-1/3 * x^(-3)) = -1/3 * (-3)x^(-4) = x^(-4)。✓

> ⚠️ **常见错误**：n = -4 时，n+1 = -3（不是 -5！）。始终写出中间步骤可以避免这类错误。

---

**例题 3**（分数指数——平方根）：求 ∫ √x dx。

**解**：

√x = x^(1/2)

∫ x^(1/2) dx = x^(1/2+1) / (1/2+1) + C = x^(3/2) / (3/2) + C = (2/3)x^(3/2) + C

也可以写成 (2/3)√(x^3) + C 或 (2/3)x√x + C。

**验证**：d/dx ((2/3)x^(3/2)) = (2/3)*(3/2)x^(1/2) = x^(1/2) = √x。✓

---

**例题 4**（分数指数——立方根）：求 ∫ ∛x dx。

**解**：

∛x = x^(1/3)

∫ x^(1/3) dx = x^(1/3+1) / (1/3+1) + C = x^(4/3) / (4/3) + C = (3/4)x^(4/3) + C

---

**例题 5**（负分数指数）：求 ∫ 1/∛(x^2) dx。

**解**：

1/∛(x^2) = 1/x^(2/3) = x^(-2/3)

∫ x^(-2/3) dx = x^(-2/3+1) / (-2/3+1) + C = x^(1/3) / (1/3) + C = 3x^(1/3) + C = 3∛x + C

**验证**：d/dx (3x^(1/3)) = 3*(1/3)x^(-2/3) = x^(-2/3) = 1/∛(x^2)。✓

---

**例题 6**（综合——多项混合）：求 ∫ (4x^3 + 2/x^5 - 3√x + 1/√x) dx。

**解**：

先将各项改写为幂函数形式：

4x^3 + 2x^(-5) - 3x^(1/2) + x^(-1/2)

逐项积分：

∫ 4x^3 dx = 4 * (x^4/4) = x^4

∫ 2x^(-5) dx = 2 * (x^(-4)/(-4)) = -1/2 * x^(-4) = -1/(2x^4)

∫ -3x^(1/2) dx = -3 * (x^(3/2) / (3/2)) = -3 * (2/3)x^(3/2) = -2x^(3/2)

∫ x^(-1/2) dx = x^(1/2) / (1/2) = 2x^(1/2) = 2√x

合并结果：

∫ (4x^3 + 2/x^5 - 3√x + 1/√x) dx = x^4 - 1/(2x^4) - 2x^(3/2) + 2√x + C

---

### 7.2.2 特殊情形：∫ 1/x dx

**公式**：

**∫ 1/x dx = ln |x| + C**

**为什么 n = -1 是特殊情况？**

回顾幂法则：∫ x^n dx = x^(n+1)/(n+1) + C。如果 n = -1，则 n+1 = 0，分母为零，公式失效！因此 1/x 的积分需要单独处理。

**推导**：回顾 ln x 的导数。

当 x > 0 时：d/dx (ln x) = 1/x

当 x < 0 时，|x| = -x > 0，由链式法则：

d/dx [ln (-x)] = 1/(-x) * (-1) = 1/x

两种情形统一写作 d/dx (ln |x|) = 1/x，因此 ∫ 1/x dx = ln |x| + C。

> ⚠️ **绝对值符号不可省略**！它保证了 x 取负值时公式仍然成立。

---

**例题 1**（基本形式）：求 ∫ 5/x dx。

**解**：

∫ 5/x dx = 5 ∫ 1/x dx = 5 ln |x| + C

---

**例题 2**（与幂函数混合）：求 ∫ (x^3 - 2/x) dx。

**解**：

∫ (x^3 - 2/x) dx = x^4/4 - 2 ln |x| + C

---

**例题 3**（化简后再积分）：求 ∫ (x^2 + 3x - 1)/x dx。

**解**：

先化简：(x^2 + 3x - 1)/x = x + 3 - 1/x

再积分：

∫ (x + 3 - 1/x) dx = x^2/2 + 3x - ln |x| + C

> ⚠️ **常见错误**：有的学生试图对 (x^2+3x-1)/x 整体使用幂法则——这是不行的！必须先化简成单项之和。

---

**例题 4**（小心区分 1/x 和 x^(-2)）：求 ∫ (x^3 - 2x^2 + 1)/x^2 dx。

**解**：

化简：(x^3 - 2x^2 + 1)/x^2 = x - 2 + 1/x^2 = x - 2 + x^(-2)

积分：

∫ (x - 2 + x^(-2)) dx = x^2/2 - 2x + x^(-1)/(-1) + C = x^2/2 - 2x - 1/x + C

注意这里 x^(-2) 用的是幂法则（n = -2 ≠ -1），而 1/x = x^(-1) 才用 ln |x|。两者不要混淆！

---

### 7.2.3 线性复合形式的积分：∫ (ax+b)^n dx

**公式**（n ≠ -1）：

**∫ (ax+b)^n dx = (ax+b)^(n+1) / (a(n+1)) + C (n ≠ -1)**

当 n = -1 时：

**∫ 1/(ax+b) dx = (1/a) ln |ax+b| + C**

**推导**（使用变量代换的思想）：

令 u = ax+b，则 du = a dx，即 dx = du/a。

∫ (ax+b)^n dx = ∫ u^n * (du/a) = (1/a) ∫ u^n du = (1/a) * u^(n+1)/(n+1) + C = (ax+b)^(n+1) / (a(n+1)) + C

**直观理解**：对比 ∫ x^n dx = x^(n+1)/(n+1)，这里的 x 被替换为 (ax+b)，但多出因子 1/a。这个 1/a 来源于链式法则的逆向——因为 (ax+b) 的导数是 a，所以反向操作时要除以 a。

**记忆口诀**："指数加 1，除以新指数，再除以 a"。

---

**例题 1**（正整数 n）：求 ∫ (5x+2)^3 dx。

**解**：

这里 a=5，n=3。

∫ (5x+2)^3 dx = (5x+2)^4 / (5*4) + C = (5x+2)^4 / 20 + C

**验证**：d/dx [ (5x+2)^4 / 20 ] = 4(5x+2)^3 * 5 / 20 = 20(5x+2)^3 / 20 = (5x+2)^3。✓

---

**例题 2**（负整数 n）：求 ∫ 1/(3x-1)^4 dx。

**解**：

改写为 (3x-1)^(-4)，a=3，n=-4。

∫ (3x-1)^(-4) dx = (3x-1)^(-3) / (3*(-3)) + C = -1/9 * (3x-1)^(-3) + C = -1/(9(3x-1)^3) + C

---

**例题 3**（分数 n——根式形式）：求 ∫ √(4x+3) dx。

**解**：

√(4x+3) = (4x+3)^(1/2)，a=4，n=1/2。

∫ (4x+3)^(1/2) dx = (4x+3)^(3/2) / (4*(3/2)) + C = (4x+3)^(3/2) / 6 + C

即 (1/6)(4x+3)^(3/2) + C。

---

**例题 4**（n = -1 情形——对数形式）：求 ∫ 1/(2x+5) dx。

**解**：

a=2，使用 ∫ 1/(ax+b) dx = (1/a) ln |ax+b| + C。

∫ 1/(2x+5) dx = (1/2) ln |2x+5| + C

**验证**：d/dx ( (1/2) ln |2x+5| ) = (1/2) * 1/(2x+5) * 2 = 1/(2x+5)。✓

---

**例题 5**（综合——两项混合）：求 ∫ ( 1/(3x-2)^2 + 4/(x+1) ) dx。

**解**：

第一项：∫ (3x-2)^(-2) dx = (3x-2)^(-1) / (3*(-1)) + C1 = -1/(3(3x-2)) + C1

第二项：∫ 4/(x+1) dx = 4 ln |x+1| + C2

合并：

∫ ( 1/(3x-2)^2 + 4/(x+1) ) dx = -1/(3(3x-2)) + 4 ln |x+1| + C

---

### 7.2.4 指数函数积分：∫ e^(ax+b) dx

**公式**：

**∫ e^(ax+b) dx = (1/a) e^(ax+b) + C (a ≠ 0)**

**推导**：对右端求导：

d/dx ( (1/a) e^(ax+b) + C ) = (1/a) * e^(ax+b) * a = e^(ax+b)

**理解**：与 (ax+b)^n 的情形类似，除以 a 是因为链式法则中 (ax+b)' = a，逆向时产生因子 1/a。

---

**例题 1**（基础）：求 ∫ e^(4x) dx。

**解**：

∫ e^(4x) dx = (1/4) e^(4x) + C

---

**例题 2**（负系数）：求 ∫ e^(-2x) dx。

**解**：

a = -2，所以 1/a = -1/2。

∫ e^(-2x) dx = -1/2 e^(-2x) + C

---

**例题 3**（带常数项）：求 ∫ e^(3x-2) dx。

**解**：

a=3，b=-2。

∫ e^(3x-2) dx = (1/3) e^(3x-2) + C

---

**例题 4**（分数系数）：求 ∫ e^(x/3 + π) dx。

**解**：

a = 1/3，1/a = 3。

∫ e^(x/3 + π) dx = 3 e^(x/3 + π) + C

---

**例题 5**（指数与多项式混合）：求 ∫ (2x^4 - 3e^(2x) + e) dx。

**解**：

注意 e 是常数（欧拉数，e ≈ 2.718），所以 ∫ e dx = ex。

∫ 2x^4 dx = 2 * (x^5/5) = (2/5)x^5

∫ -3e^(2x) dx = -3 * (1/2) e^(2x) = -3/2 e^(2x)

∫ e dx = ex

结果：

∫ (2x^4 - 3e^(2x) + e) dx = (2/5)x^5 - (3/2)e^(2x) + ex + C

---

### 7.2.5 三角函数积分

三个基本三角函数的积分公式，全部由第 5 章学过的导数公式逆向推导而来。

**对照速查表**：

| 导数公式 | 对应积分公式 |
|---------|------------|
| d/dx (sin x) = cos x | ∫ cos x dx = sin x + C |
| d/dx (cos x) = -sin x | ∫ sin x dx = -cos x + C |
| d/dx (tan x) = sec^2 x | ∫ sec^2 x dx = tan x + C |

对于更一般的 ax+b 形式，三个公式统一为"除以 a"的模式。

---

#### (1) ∫ sin(ax+b) dx

**公式**：

**∫ sin(ax+b) dx = - (1/a) cos(ax+b) + C**

**推导**：假设原函数为 k cos(ax+b)，求导得：

d/dx [k cos(ax+b)] = k * [-sin(ax+b)] * a = -ak sin(ax+b)

我们希望 -ak = 1，即 k = -1/a。因此原函数为 -1/a cos(ax+b)。

**验证**：

d/dx ( -1/a cos(ax+b) + C ) = -1/a * [-sin(ax+b)] * a = sin(ax+b) ✓

**记忆要点**：
- sin 积分得 -cos（注意负号）
- 再除以 a

---

**例题 1**（基础）：求 ∫ sin(2x) dx。

**解**：

∫ sin(2x) dx = -1/2 cos(2x) + C

---

**例题 2**（带相位）：求 ∫ sin(3x + π) dx。

**解**：

a=3，b=π。

∫ sin(3x + π) dx = -1/3 cos(3x + π) + C

---

**例题 3**（带系数）：求 ∫ -5 sin(x/2) dx。

**解**：

a = 1/2，1/a = 2。

∫ -5 sin(x/2) dx = -5 * (-2 cos(x/2)) + C = 10 cos(x/2) + C

---

#### (2) ∫ cos(ax+b) dx

**公式**：

**∫ cos(ax+b) dx = (1/a) sin(ax+b) + C**

**推导**：假设原函数为 k sin(ax+b)，求导得：

d/dx [k sin(ax+b)] = k * cos(ax+b) * a = ak cos(ax+b)

令 ak = 1，得 k = 1/a。

**验证**：

d/dx ( (1/a) sin(ax+b) + C ) = (1/a) * cos(ax+b) * a = cos(ax+b) ✓

**记忆要点**：
- cos 积分得 sin（没有负号）
- 再除以 a

---

**例题 1**（基础）：求 ∫ cos(5x) dx。

**解**：

∫ cos(5x) dx = 1/5 sin(5x) + C

---

**例题 2**（带相位和系数）：求 ∫ 3 cos(2x-1) dx。

**解**：

∫ 3 cos(2x-1) dx = 3 * (1/2) sin(2x-1) + C = 3/2 sin(2x-1) + C

---

**例题 3**（利用偶函数性质）：求 ∫ cos(-3x) dx。

**解**：

利用 cos(-θ) = cos θ（余弦是偶函数）：

∫ cos(-3x) dx = ∫ cos(3x) dx = 1/3 sin(3x) + C

或者直接用公式，a=-3：

∫ cos(-3x) dx = 1/(-3) sin(-3x) + C = -1/3 [-sin(3x)] + C = 1/3 sin(3x) + C

两种方法结果一致。

---

#### (3) ∫ sec^2(ax+b) dx

**公式**：

**∫ sec^2(ax+b) dx = (1/a) tan(ax+b) + C**

**推导**：d/dx (tan x) = sec^2 x，因此：

d/dx ( (1/a) tan(ax+b) ) = (1/a) * sec^2(ax+b) * a = sec^2(ax+b)

**记忆要点**：
- sec^2 积分得 tan（没有负号）
- 再除以 a

---

**例题 1**（基础）：求 ∫ sec^2(3x) dx。

**解**：

∫ sec^2(3x) dx = 1/3 tan(3x) + C

---

**例题 2**（带相位）：求 ∫ sec^2(2x - π/4) dx。

**解**：

∫ sec^2(2x - π/4) dx = 1/2 tan(2x - π/4) + C

---

**例题 3**（综合）：求 ∫ (2 sec^2 x - 3 sec^2(4x)) dx。

**解**：

∫ 2 sec^2 x dx = 2 tan x

∫ -3 sec^2(4x) dx = -3 * (1/4) tan(4x) = -3/4 tan(4x)

结果：

∫ (2 sec^2 x - 3 sec^2(4x)) dx = 2 tan x - 3/4 tan(4x) + C

---

### 7.2.6 超级综合例题（完整技能检验）

**例题 1**（六项混合——全部类型）：求 ∫ (8x^7 - 3/x^4 + 5e^(2x) + 2 sin 3x - 4 cos(x/2) + 6 sec^2(5x)) dx。

**解**：

逐项处理：

8x^7 → 8 * (x^8/8) = x^8

-3/x^4 = -3x^(-4) → -3 * (x^(-3)/(-3)) = 1/x^3

5e^(2x) → 5 * (1/2)e^(2x) = 5/2 e^(2x)

2 sin 3x → 2 * ( -1/3 cos 3x ) = -2/3 cos 3x

-4 cos(x/2) → -4 * (1/(1/2)) sin(x/2) = -4 * 2 sin(x/2) = -8 sin(x/2)

6 sec^2(5x) → 6 * (1/5) tan(5x) = 6/5 tan(5x)

合并：

**x^8 + 1/x^3 + (5/2)e^(2x) - (2/3)cos 3x - 8 sin(x/2) + (6/5)tan(5x) + C**

---

**例题 2**（先展开后积分——多项式乘积）：求 ∫ (x^2 - 1)(x^2 + 2) dx。

**解**：

展开：(x^2 - 1)(x^2 + 2) = x^4 + 2x^2 - x^2 - 2 = x^4 + x^2 - 2

积分：

∫ (x^4 + x^2 - 2) dx = x^5/5 + x^3/3 - 2x + C

---

**例题 3**（先化简分式后积分）：求 ∫ (2x^4 - 3x^2 + 5x - 1)/x^2 dx。

**解**：

化简：(2x^4 - 3x^2 + 5x - 1)/x^2 = 2x^2 - 3 + 5/x - 1/x^2 = 2x^2 - 3 + 5x^(-1) - x^(-2)

积分：

∫ (2x^2 - 3 + 5x^(-1) - x^(-2)) dx = 2*(x^3/3) - 3x + 5 ln |x| - x^(-1)/(-1) + C

= (2/3)x^3 - 3x + 5 ln |x| + 1/x + C

---

**例题 4**（(ax+b)^n 与三角指数混合）：求 ∫ ( (3x+1)^4 + 2/(5x-3) - sin(4x - π/6) ) dx。

**解**：

第一项：∫ (3x+1)^4 dx = (3x+1)^5 / (3*5) + C1 = (3x+1)^5 / 15 + C1

第二项：∫ 2/(5x-3) dx = 2 * (1/5) ln |5x-3| + C2 = (2/5) ln |5x-3| + C2

第三项：∫ -sin(4x - π/6) dx = - ( -1/4 cos(4x - π/6) ) + C3 = 1/4 cos(4x - π/6) + C3

合并：

∫ ( (3x+1)^4 + 2/(5x-3) - sin(4x - π/6) ) dx = (3x+1)^5 / 15 + (2/5) ln |5x-3| + 1/4 cos(4x - π/6) + C

---
---

## 7.3 定积分

### 7.3.1 从不定积分到定积分——微积分基本定理

不定积分 ∫ f(x) dx 给出的是一个**函数族**（包含任意常数 C），而**定积分** ∫[a,b] f(x) dx 给出的是一个**数值**——它代表了函数 f(x) 在区间 [a,b] 上的"累积效应"。

连接两者的桥梁是**微积分基本定理**，也称为**牛顿-莱布尼茨公式**：

**∫[a,b] f(x) dx = F(b) - F(a)**

其中 F'(x) = f(x)，即 F(x) 是 f(x) 的任意一个原函数。

**直观推导**：

考虑函数 A(x) = ∫[a,x] f(t) dt，它表示从 a 到 x 的累积面积。当 x 增加一个微小量 h 时：

A(x+h) - A(x) ≈ f(x) * h

因此：

lim_{h→0} (A(x+h) - A(x))/h = f(x)

即 A'(x) = f(x)。所以 A(x) 是 f(x) 的一个原函数。设 F(x) 是 f(x) 的任意一个原函数，则 F(x) = A(x) + C。于是：

F(b) - F(a) = [A(b) + C] - [A(a) + C] = A(b) - A(a) = A(b) - 0 = ∫[a,b] f(x) dx

**常用记号**：

∫[a,b] f(x) dx = [F(x)]_a^b = F(b) - F(a)

> ⚠️ **关键区分**：在定积分中，**不需要加积分常数 C**，因为在计算 F(b)-F(a) 时 C 会被消去。

---

### 7.3.2 定积分的性质

**性质 1（线性性）**：

∫[a,b] [c f(x) + d g(x)] dx = c ∫[a,b] f(x) dx + d ∫[a,b] g(x) dx

**性质 2（区间可加性）**——最重要的性质之一：

∫[a,b] f(x) dx = ∫[a,c] f(x) dx + ∫[c,b] f(x) dx

这一定理对于处理函数变号的情况至关重要。当 f(x) 在 [a,b] 上变号时，我们需要在零点处分割区间，这正是性质 2 的应用。

**性质 3（反向区间）**：

∫[a,b] f(x) dx = -∫[b,a] f(x) dx

**推导**：∫[a,b] f(x) dx = F(b)-F(a) = -[F(a)-F(b)] = -∫[b,a] f(x) dx。

**性质 4（零区间）**：

∫[a,a] f(x) dx = 0

**性质 5（比较性质）**：如果在 [a,b] 上 f(x) ≥ g(x)，则：

∫[a,b] f(x) dx ≥ ∫[a,b] g(x) dx

---

### 7.3.3 定积分的计算程序

计算定积分的一般步骤：

1. **找原函数**：找到被积函数 f(x) 的一个原函数 F(x)（不加常数 C）
2. **代入上下限**：计算 F(b) - F(a)
3. **化简结果**：给出最终数值或简化表达式

---

**例题 1**（简单幂函数——几何验证）：计算 ∫[1,4] (2x+1) dx。

**解**：

先求原函数：∫ (2x+1) dx = x^2 + x + C

所以：

∫[1,4] (2x+1) dx = [ x^2 + x ]_1^4 = (16 + 4) - (1 + 1) = 20 - 2 = 18

**几何验证**：y=2x+1 是一条直线，在 x=1 处 y=3，x=4 处 y=9，区间长度 3。梯形面积 = (3+9)/2 * 3 = 18，与积分结果一致。✓

---

**例题 2**（二次函数）：计算 ∫[-1,2] (x^2 - 2x + 3) dx。

**解**：

∫[-1,2] (x^2 - 2x + 3) dx = [ x^3/3 - x^2 + 3x ]_{-1}^2

= (8/3 - 4 + 6) - (-1/3 - 1 - 3)

= (8/3 + 2) - (-1/3 - 4)

= 14/3 - (-13/3) = 27/3 = 9

---

**例题 3**（三角函数）：计算 ∫[0,π] cos x dx。

**解**：

∫[0,π] cos x dx = [ sin x ]_0^π = sin π - sin 0 = 0 - 0 = 0

**几何意义**：余弦函数在 [0,π] 上，[0,π/2] 区间为正，[π/2,π] 区间为负，正负面积恰好抵消，所以有向面积为零。

---

**例题 4**（指数与 1/x 的混合）：计算 ∫[1,2] (e^(3x) + 2/x) dx。

**解**：

∫[1,2] (e^(3x) + 2/x) dx = [ (1/3)e^(3x) + 2 ln|x| ]_1^2

= ( (1/3)e^6 + 2 ln 2 ) - ( (1/3)e^3 + 2 ln 1 )

= (1/3)(e^6 - e^3) + 2 ln 2

（注意 ln 1 = 0）

---

**例题 5**（(ax+b)^n 形式）：计算 ∫[0,1] (3x+2)^4 dx。

**解**：

方法一（直接用公式）：a=3，n=4。

∫ (3x+2)^4 dx = (3x+2)^5 / (3*5) = (3x+2)^5 / 15

∫[0,1] (3x+2)^4 dx = [ (3x+2)^5 / 15 ]_0^1 = 5^5 / 15 - 2^5 / 15 = 3125/15 - 32/15 = 3093/15 = 1031/5

方法二（展开）：(3x+2)^4 = 81x^4 + 216x^3 + 216x^2 + 96x + 16

∫[0,1] (81x^4 + 216x^3 + 216x^2 + 96x + 16) dx = [ 81x^5/5 + 54x^4 + 72x^3 + 48x^2 + 16x ]_0^1

= 81/5 + 54 + 72 + 48 + 16 = 81/5 + 190 = 81/5 + 950/5 = 1031/5

两种方法结果一致。✓

---

**例题 6**（定积分与 ln）：计算 ∫[2,4] 1/(x-1) dx。

**解**：

∫[2,4] 1/(x-1) dx = [ ln|x-1| ]_2^4 = ln 3 - ln 1 = ln 3

---

### 7.3.4 定积分与有向面积

定积分 ∫[a,b] f(x) dx 给出的是**有向面积**：

- 当 f(x) ≥ 0 时，积分值为正，等于曲线与 x 轴之间的实际面积
- 当 f(x) ≤ 0 时，积分值为负，其绝对值等于实际面积
- 当 f(x) 变号时，正负部分相互抵消

**例题 1**：计算 ∫[-2,3] (x-1) dx 并解释其几何意义。

**解**：

∫[-2,3] (x-1) dx = [ x^2/2 - x ]_{-2}^3 = (9/2 - 3) - (2 + 2) = 3/2 - 4 = -5/2

结果为 -5/2，表示在区间 [-2,3] 上，x 轴下方的面积比上方的面积多 5/2 平方单位。函数 y=x-1 在 x=1 处穿过 x 轴，[-2,1] 上曲线在下方，[1,3] 上曲线在上方。

---

**例题 2**（利用对称性简化计算）：计算 ∫[-a,a] x^3 dx。

**解**：

由于 x^3 是奇函数（(-x)^3 = -x^3），在对称区间 [-a,a] 上的积分为零：

∫[-a,a] x^3 dx = [ x^4/4 ]_{-a}^a = a^4/4 - a^4/4 = 0

> **一般规律**：奇函数在对称区间上的定积分为零；偶函数在对称区间上的定积分等于半区间积分的两倍。
> - f 为奇函数：∫[-a,a] f(x) dx = 0
> - f 为偶函数：∫[-a,a] f(x) dx = 2∫[0,a] f(x) dx

---
---

## 7.4 平面面积

本节是定积分最重要的几何应用之一。我们将系统地学习如何用积分计算各种平面图形的面积。

### 7.4.1 曲线与 x 轴之间的面积

**情形一**：f(x) ≥ 0 在 [a,b] 上恒成立

A = ∫[a,b] f(x) dx

**情形二**：f(x) ≤ 0 在 [a,b] 上恒成立

A = -∫[a,b] f(x) dx = ∫[a,b] |f(x)| dx

**情形三**：f(x) 在 [a,b] 上变号（一般情形）

A = ∫[a,b] |f(x)| dx

**标准解题程序**：
1. **解 f(x) = 0**：找出曲线与 x 轴的所有交点
2. **分割区间**：用零点将积分区间分割为若干子区间
3. **判断正负**：在每个子区间上取测试点，判断 f(x) 的正负
4. **分段积分**：正值区间直接积分，负值区间取绝对值（加负号）
5. **求和**：将所有子区间的面积相加

---

**例题 1**（全部在 x 轴上方）：求曲线 y = x^2 + 1 与 x 轴在 x=0 到 x=2 之间围成的面积。

**解**：

在 [0,2] 上，x^2 + 1 ≥ 1 > 0，所以直接积分：

A = ∫[0,2] (x^2 + 1) dx = [ x^3/3 + x ]_0^2 = (8/3 + 2) - 0 = 14/3

---

**例题 2**（全部在 x 轴下方）：求曲线 y = -e^x 与 x 轴在 x=-1 到 x=1 之间围成的面积。

**解**：

在 [-1,1] 上，-e^x < 0，所以面积为：

A = -∫[-1,1] (-e^x) dx = ∫[-1,1] e^x dx = [ e^x ]_{-1}^1 = e - e^(-1)

---

**例题 3**（变号——分段处理）：求曲线 y = x^2 - 1 与 x 轴在 [-2,2] 之间围成的总面积。

**解**：

**Step 1**：求零点。x^2 - 1 = 0 ⇒ x = ±1。

**Step 2**：区间 [-2,2] 被三个点 -2,-1,1,2 分割为三个子区间：[-2,-1]、[-1,1]、[1,2]。

**Step 3**：判断正负。
- 在 [-2,-1] 上，取 x=-1.5：f(-1.5) = 2.25-1 = 1.25 > 0，在上方
- 在 [-1,1] 上，取 x=0：f(0) = -1 < 0，在下方
- 在 [1,2] 上，取 x=1.5：f(1.5) = 2.25-1 = 1.25 > 0，在上方

**Step 4**：

A = ∫[-2,-1] (x^2-1) dx + ∫[-1,1] -(x^2-1) dx + ∫[1,2] (x^2-1) dx

= [ x^3/3 - x ]_{-2}^{-1} + [ -x^3/3 + x ]_{-1}^{1} + [ x^3/3 - x ]_1^2

第一部分：( -1/3 + 1 ) - ( -8/3 + 2 ) = 2/3 - ( -2/3 ) = 4/3

第二部分：( -1/3 + 1 ) - ( 1/3 - 1 ) = 2/3 - ( -2/3 ) = 4/3

第三部分：( 8/3 - 2 ) - ( 1/3 - 1 ) = 2/3 - ( -2/3 ) = 4/3

总面积：A = 4/3 + 4/3 + 4/3 = 4

---

**例题 4**（考试典型题——开口向下的抛物线）：求曲线 y = 9 - x^2 与 x 轴所围成的面积。

**解**：

与 x 轴的交点：9 - x^2 = 0 ⇒ x = ±3。

在 [-3,3] 上，9 - x^2 ≥ 0，所以：

A = ∫[-3,3] (9 - x^2) dx = [ 9x - x^3/3 ]_{-3}^3

= (27 - 9) - (-27 + 9) = 18 - (-18) = 36

面积为 36 平方单位。

---

**例题 5**（三次函数——三个零点两个区间）：求曲线 y = x^3 - 4x 与 x 轴在 [-2,2] 之间围成的总面积。

**解**：

**Step 1**：x^3 - 4x = x(x^2-4) = x(x-2)(x+2) = 0，零点为 x = -2, 0, 2。

**Step 2**：区间被分割为 [-2,0] 和 [0,2]。

**Step 3**：
- 在 [-2,0] 上，取 x=-1：f(-1) = -1 + 4 = 3 > 0
- 在 [0,2] 上，取 x=1：f(1) = 1 - 4 = -3 < 0

**Step 4**：

A = ∫[-2,0] (x^3 - 4x) dx + ∫[0,2] -(x^3 - 4x) dx

= [ x^4/4 - 2x^2 ]_{-2}^0 + [ -x^4/4 + 2x^2 ]_0^2

第一部分：(0) - ( 16/4 - 8 ) = -(4-8) = 4

第二部分：( -16/4 + 8 ) - 0 = (-4+8) = 4

总面积：A = 4 + 4 = 8

---

### 7.4.2 直线与曲线之间的面积

**核心方法**：如果在区间 [a,b] 上，曲线 y = f(x) 位于直线 y = g(x) 的上方（即 f(x) ≥ g(x)），则它们之间的面积为：

**A = ∫[a,b] [f(x) - g(x)] dx**

**解题程序**：
1. 求交点：解 f(x) = g(x)
2. 确定积分区间
3. 判断上、下函数关系（取区间内任一点测试）
4. 对差值积分

---

**例题 1**（曲线在上方）：求曲线 y = x^2 + 1 与直线 y = x + 3 所围成的面积。

**解**：

**Step 1**：交点：x^2 + 1 = x + 3 ⇒ x^2 - x - 2 = 0 ⇒ (x-2)(x+1) = 0，得 x = -1 或 x = 2。

**Step 2**：区间为 [-1,2]。

**Step 3**：取 x=0 测试：f(0) = 1，g(0) = 3，所以 g(x) = x+3 在上方。

**Step 4**：

A = ∫[-1,2] [(x+3) - (x^2+1)] dx

= ∫[-1,2] (2 + x - x^2) dx

= [ 2x + x^2/2 - x^3/3 ]_{-1}^2

= (4 + 2 - 8/3) - (-2 + 1/2 + 1/3)

= 10/3 - (-7/6) = 10/3 + 7/6 = 27/6 = 9/2

---

**例题 2**（直线在上方——经典题）：求直线 y = 2x 与曲线 y = x^2 所围成的面积。

**解**：

交点：x^2 = 2x ⇒ x^2 - 2x = 0 ⇒ x(x-2) = 0，得 x=0 和 x=2。

在 [0,2] 上，取 x=1：f(1)=1，g(1)=2，所以 y=2x 在上方。

A = ∫[0,2] (2x - x^2) dx = [ x^2 - x^3/3 ]_0^2 = (4 - 8/3) - 0 = 4/3

---

**例题 3**（根式函数与直线）：求曲线 y = √x 与直线 y = x/2 所围成的面积。

**解**：

交点：√x = x/2 ⇒ 2√x = x ⇒ x = 2√x ⇒ x - 2√x = 0 ⇒ √x(√x - 2) = 0，得 x=0 或 x=4。

在 [0,4] 上，取 x=1：√1=1，1/2=0.5，所以 y=√x 在上方。

A = ∫[0,4] (√x - x/2) dx = ∫[0,4] (x^(1/2) - x/2) dx

= [ (2/3)x^(3/2) - x^2/4 ]_0^4 = ( (2/3)*8 - 16/4 ) - 0 = 16/3 - 4 = 4/3

---

### 7.4.3 两条曲线之间的面积

当两条曲线 y = f(x) 和 y = g(x) 在区间上有多个交点时，需要分段处理——在每个子区间上分别判断上下关系。

---

**例题 1**（对称曲线）：求曲线 y = x^2 与 y = 4 - x^2 所围成的面积。

**解**：

交点：x^2 = 4 - x^2 ⇒ 2x^2 = 4 ⇒ x^2 = 2 ⇒ x = ±√2。

在 [-√2, √2] 上，取 x=0：f(0)=0，g(0)=4，所以 y=4-x^2 在上方。

A = ∫[-√2,√2] [(4 - x^2) - x^2] dx = ∫[-√2,√2] (4 - 2x^2) dx

= [ 4x - 2x^3/3 ]_{-√2}^{√2}

= (4√2 - 4√2/3) - (-4√2 + 4√2/3)

= 8√2/3 - (-8√2/3) = 16√2/3

---

**例题 2**（上下关系发生变化——需分段）：求曲线 y = x^3 与 y = x 所围成的总面积。

**解**：

交点：x^3 = x ⇒ x^3 - x = 0 ⇒ x(x-1)(x+1) = 0，得 x = -1, 0, 1。

区间被分割为 [-1,0] 和 [0,1]。

- 在 [-1,0] 上，取 x=-0.5：f(-0.5) = -0.125，g(-0.5) = -0.5，y=x^3 在上方
- 在 [0,1] 上，取 x=0.5：f(0.5)=0.125，g(0.5)=0.5，y=x 在上方

A = ∫[-1,0] (x^3 - x) dx + ∫[0,1] (x - x^3) dx

= [ x^4/4 - x^2/2 ]_{-1}^0 + [ x^2/2 - x^4/4 ]_0^1

= (0 - (1/4 - 1/2)) + ((1/2 - 1/4) - 0)

= 1/4 + 1/4 = 1/2

---

### 7.4.4 多个面积之和（考纲重点）

考纲明确要求"多个面积之和"。这类问题的关键步骤是**正确分割区间**。

---

**例题 1**（三次函数与 x 轴——三段面积）：求曲线 y = x^3 - x^2 - 2x 与 x 轴之间的总面积。

**解**：

因式分解：x^3 - x^2 - 2x = x(x^2 - x - 2) = x(x-2)(x+1)，零点为 x = -1, 0, 2。

- 在 [-1,0] 上，f(-0.5) = 0.625 > 0
- 在 [0,2] 上，f(1) = -2 < 0

A = ∫[-1,0] (x^3 - x^2 - 2x) dx + ∫[0,2] -(x^3 - x^2 - 2x) dx

= [ x^4/4 - x^3/3 - x^2 ]_{-1}^0 + [ -x^4/4 + x^3/3 + x^2 ]_0^2

第一部分：(0) - ( 1/4 + 1/3 - 1 ) = -(-5/12) = 5/12

第二部分：( -16/4 + 8/3 + 4 ) - 0 = ( -4 + 4 ) + 8/3 = 8/3

总面积：A = 5/12 + 8/3 = 5/12 + 32/12 = 37/12

---

**例题 2**（二次函数——三段面积）：求曲线 y = x^2 - 4x + 3 与 x 轴在 [0,4] 之间围成的总面积。

**解**：

零点：x^2 - 4x + 3 = (x-1)(x-3) = 0，得 x=1, 3。

区间 [0,4] 被分割为 [0,1]、[1,3]、[3,4]。

- [0,1]：f(0.5) = 1.25 > 0
- [1,3]：f(2) = -1 < 0
- [3,4]：f(3.5) = 1.25 > 0

A = ∫[0,1] (x^2 - 4x + 3) dx + ∫[1,3] -(x^2 - 4x + 3) dx + ∫[3,4] (x^2 - 4x + 3) dx

= [ x^3/3 - 2x^2 + 3x ]_0^1 + [ -x^3/3 + 2x^2 - 3x ]_1^3 + [ x^3/3 - 2x^2 + 3x ]_3^4

= 4/3 + 4/3 + 4/3 = 4

---

### 7.4.5 平面面积解题策略总结

| 场景 | 识别标志 | 方法 |
|------|---------|------|
| 曲线在 x 轴上方 | f(x) ≥ 0 | A = ∫[a,b] f(x) dx |
| 曲线在 x 轴下方 | f(x) ≤ 0 | A = -∫[a,b] f(x) dx |
| 曲线穿越 x 轴 | f(x) 变号 | 在零点处分段，分别取绝对值 |
| 直线与曲线 | 已知两个函数 | A = ∫[a,b] [f(x)-g(x)] dx（上减下） |
| 两曲线多个交点 | 多个交点 | 分段处理，每段上减下 |
| 多个面积之和 | 三个或以上子区间 | 分别积分后相加 |

---

## 7.5 定积分在运动学中的应用

> **对应考纲14.14**：运用微分与积分解决运动学问题（位移、速度、加速度）。

在第5章中，我们学了用**微分**从位移求速度和加速度。而**积分**则提供了反向路径：已知加速度求速度，已知速度求位移。

### 7.5.1 核心关系

设质点沿直线运动，其位移为 s(t)，速度为 v(t)，加速度为 a(t)，则：

**微分关系**（从位移到加速度）：

v(t) = s'(t) = ds/dt

a(t) = v'(t) = dv/dt = s''(t)

**积分关系**（从加速度到位移）：

v(t) = ∫ a(t) dt

s(t) = ∫ v(t) dt

**定积分形式**（已知加速度求速度变化量）：

∫[t1,t2] a(t) dt = v(t2) - v(t1)

**定积分形式**（已知速度求位移变化量）：

∫[t1,t2] v(t) dt = s(t2) - s(t1)

**位移与路程的区别**：
- 位移 = ∫[t1,t2] v(t) dt（有向面积）
- 路程 = ∫[t1,t2] |v(t)| dt（绝对值面积，需要分段处理）

---

**例题1**（已知加速度求速度和位移）：一质点沿直线运动，加速度 a(t) = 12t^2 - 6，t=0 时速度为 v=2，位移 s=1。求 v(t) 和 s(t)。

**解**：

v(t) = ∫ (12t^2 - 6) dt = 4t^3 - 6t + C

由 v(0) = 2 得 C = 2，所以 v(t) = 4t^3 - 6t + 2。

s(t) = ∫ (4t^3 - 6t + 2) dt = t^4 - 3t^2 + 2t + D

由 s(0) = 1 得 D = 1，所以 s(t) = t^4 - 3t^2 + 2t + 1。

---

**例题2**（已知速度求位移）：质点的速度 v(t) = t^2 - 5t + 6。求从 t=1 到 t=4 的净位移。

**解**：

净位移 = ∫[1,4] (t^2 - 5t + 6) dt = [ t^3/3 - 5t^2/2 + 6t ]_1^4

= (64/3 - 80/2 + 24) - (1/3 - 5/2 + 6)

= (64/3 - 40 + 24) - (1/3 + 1/2)

= (64/3 - 16) - 5/6

= 16/3 - 5/6

= 32/6 - 5/6 = 27/6 = 9/2

净位移为 9/2 单位，方向为正。

---

**例题3**（已知速度求路程——需分段处理）：质点的速度 v(t) = 3t^2 - 12t + 9，t ≥ 0。求 t=0 到 t=4 之间的路程。

**解**：

**Step 1**：求速度为零的时刻。解 v(t) = 0：

3t^2 - 12t + 9 = 0 ⇒ t^2 - 4t + 3 = 0 ⇒ (t-1)(t-3) = 0

t = 1 或 t = 3。

**Step 2**：判断速度在区间上的符号：
- t ∈ [0,1)：取 t=0.5，v(0.5) = 3(0.25) - 6 + 9 = 0.75 - 6 + 9 = 3.75 > 0
- t ∈ (1,3)：取 t=2，v(2) = 3(4) - 24 + 9 = 12 - 24 + 9 = -3 < 0
- t ∈ (3,4]：取 t=3.5，v(3.5) = 3(12.25) - 42 + 9 = 36.75 - 42 + 9 = 3.75 > 0

**Step 3**：分段积分求路程（取绝对值）：

路程 = ∫[0,1] v(t) dt + ∫[1,3] -v(t) dt + ∫[3,4] v(t) dt

先求原函数：s(t) = ∫ v(t) dt = t^3 - 6t^2 + 9t + C

第一段（t=0到t=1）：s(1) - s(0) = (1 - 6 + 9) - 0 = 4

第二段（t=1到t=3）：|s(3) - s(1)| = |(27 - 54 + 27) - 4| = |0 - 4| = 4

第三段（t=3到t=4）：s(4) - s(3) = (64 - 96 + 36) - 0 = 4

**路程** = 4 + 4 + 4 = 12

注意：净位移 = s(4) - s(0) = 4 - 0 = 4，路程比位移大，因为质点在 t=1 到 t=3 之间反向运动。

---

**例题4**（已知加速度求速度变化量——定积分应用）：质点的加速度 a(t) = 2t + 3。求 t=0 到 t=2 之间速度的变化量。

**解**：

速度变化量 = ∫[0,2] a(t) dt = ∫[0,2] (2t + 3) dt

= [ t^2 + 3t ]_0^2 = (4 + 6) - 0 = 10

所以 v(2) - v(0) = 10 m/s。

---

**例题5**（运动学综合——已知位移函数求各物理量）：质点位移 s(t) = 2t^3 - 9t^2 + 12t + 5（t ≥ 0）。

(a) 求速度函数和加速度函数。

(b) 求 t=2 时的速度和加速度。

(c) 质点何时静止？

(d) 求 t=0 到 t=3 之间的路程。

**解**：

(a)

v(t) = s'(t) = 6t^2 - 18t + 12

a(t) = v'(t) = 12t - 18

(b)

v(2) = 6(4) - 18(2) + 12 = 24 - 36 + 12 = 0

a(2) = 12(2) - 18 = 24 - 18 = 6

(c) 解 v(t) = 0：

6t^2 - 18t + 12 = 0 ⇒ t^2 - 3t + 2 = 0 ⇒ (t-1)(t-2) = 0

t = 1 或 t = 2，质点在 t=1 和 t=2 时静止。

(d) 求路程需判断速度符号。

t ∈ [0,1)：v(t) > 0（取 t=0.5，v=6(0.25)-18(0.5)+12=1.5-9+12=4.5>0）

t ∈ (1,2)：v(t) < 0（取 t=1.5，v=6(2.25)-18(1.5)+12=13.5-27+12=-1.5<0）

t ∈ (2,3]：v(t) > 0（取 t=2.5，v=6(6.25)-18(2.5)+12=37.5-45+12=4.5>0）

路程 = |s(1)-s(0)| + |s(2)-s(1)| + |s(3)-s(2)|

s(0) = 5，s(1) = 2 - 9 + 12 + 5 = 10

s(2) = 16 - 36 + 24 + 5 = 9

s(3) = 54 - 81 + 36 + 5 = 14

路程 = |10-5| + |9-10| + |14-9| = 5 + 1 + 5 = 11

### 7.5.2 运动图像分析

**s-t 图（位移-时间图）**：
- 切线的斜率 = 瞬时速度
- 曲线上凸（二阶导数为负）表示减速（速度减小）
- 曲线下凸（二阶导数为正）表示加速（速度增大）

**v-t 图（速度-时间图）**：
- 曲线下的面积（定积分）= 位移
- 切线斜率 = 加速度
- 速度为正时，质点在正方向运动；速度为负时，质点在负方向运动
- 速度从正变负（或反之）的时刻，质点改变运动方向

**a-t 图（加速度-时间图）**：
- 曲线下的面积 = 速度的变化量

---

**例题6**（v-t图分析）：某物体做直线运动，其 v-t 图像如图所示（描述如下）：
- 0 ≤ t < 2：速度从 0 线性增加到 4 m/s
- 2 ≤ t < 5：速度保持在 4 m/s 不变
- 5 ≤ t < 7：速度从 4 m/s 线性减少到 0

求：(a) 0-7秒内的位移；(b) 物体何时加速度最大？

**解**：

(a) 位移 = v-t 图下的面积（三角形 + 矩形 + 三角形）

A1 = 1/2 * 2 * 4 = 4（t=0到t=2的三角形）

A2 = 3 * 4 = 12（t=2到t=5的矩形）

A3 = 1/2 * 2 * 4 = 4（t=5到t=7的三角形）

总位移 = 4 + 12 + 4 = 20 m

(b) 加速度 = v-t 图的切线斜率。
- t ∈ (0,2)：加速度 = 4/2 = 2 m/s²（常数）
- t ∈ (2,5)：加速度 = 0
- t ∈ (5,7)：加速度 = -4/2 = -2 m/s²（常数）

加速度大小在 t ∈ (0,2) 和 t ∈ (5,7) 时均为 2 m/s²，最大加速度大小为 2 m/s²。

---

## 本章核心公式速查表

| 被积函数 | 不定积分 | 条件/备注 |
|---------|---------|---------|
| x^n | x^(n+1)/(n+1) + C | n ≠ -1 |
| 1/x | ln|x| + C | 单独记忆，幂法则失效 |
| e^(ax+b) | (1/a)e^(ax+b) + C | a ≠ 0 |
| sin(ax+b) | -(1/a)cos(ax+b) + C | a ≠ 0 |
| cos(ax+b) | (1/a)sin(ax+b) + C | a ≠ 0 |
| sec^2(ax+b) | (1/a)tan(ax+b) + C | a ≠ 0 |
| (ax+b)^n | (ax+b)^(n+1)/(a(n+1)) + C | n ≠ -1 |
| 1/(ax+b) | (1/a)ln|ax+b| + C | a ≠ 0 |
| 定积分 ∫[a,b] f(x) dx | F(b) - F(a) | F'(x) = f(x)，不加C |
| 平面面积（上-下） | ∫[a,b] [f(x)-g(x)] dx | 先确认 f(x) ≥ g(x) |
| 变号曲线与x轴面积 | 分段取绝对值 | 先找零点 |
| 位移 | ∫[t1,t2] v(t) dt | 从t1到t2的净位移 |
| 路程 | ∫[t1,t2] |v(t)| dt | 需分段处理 |
| 速度变化量 | ∫[t1,t2] a(t) dt | 等于v(t2)-v(t1) |

---

## 本章练习题（部分精选）

**1**：求 ∫ (x^6 + 2x^3 - 4x + 1) dx。

**2**：求 ∫ (3/x - 2e^(4x) + cos(x/2)) dx。

**3**：计算 ∫[0,2] (x^3 - 4x) dx。

**4**：计算 ∫[1,4] (1/√x) dx。

**5**：求曲线 y = x^2 - 4 与 x 轴在 [-3,3] 之间围成的总面积。

**6**：求曲线 y = 4x - x^2 与直线 y = x 所围成的面积。

**7**：质点的速度 v(t) = 4t - t^2（t ≥ 0）。求从 t=0 到 t=5 的净位移和路程。

**8**：质点的加速度 a(t) = 6t - 4，初始速度 v(0) = 3，初始位移 s(0) = 0。求速度函数 v(t) 和位移函数 s(t)。

---

## 练习题答案

**1**：x^7/7 + x^4/2 - 2x^2 + x + C

**2**：3 ln|x| - (1/2)e^(4x) + 2 sin(x/2) + C

**3**：∫[0,2] (x^3 - 4x) dx = [ x^4/4 - 2x^2 ]_0^2 = (4 - 8) - 0 = -4

**4**：∫[1,4] x^(-1/2) dx = [ 2√x ]_1^4 = 4 - 2 = 2

**5**：零点为 x = ±2。A = ∫[-3,-2] (x^2-4) dx + ∫[-2,2] -(x^2-4) dx + ∫[2,3] (x^2-4) dx = 7/3 + 32/3 + 7/3 = 46/3

**6**：交点：4x - x^2 = x ⇒ 3x - x^2 = 0 ⇒ x(3-x) = 0，x=0,3。A = ∫[0,3] [(4x-x^2)-x] dx = ∫[0,3] (3x-x^2) dx = [ 3x^2/2 - x^3/3 ]_0^3 = 27/2 - 9 = 9/2

**7**：净位移 = ∫[0,5] (4t-t^2) dt = [ 2t^2 - t^3/3 ]_0^5 = 50 - 125/3 = 25/3。求路程：解 v(t)=0 ⇒ 4t-t^2=0 ⇒ t=0,4。t∈[0,4]时v≥0，t∈[4,5]时v≤0。路程 = ∫[0,4] v dt + ∫[4,5] -v dt = (32 - 64/3) + (125/3 - 50) = 32/3 + (-25/3) = 7/3。总路程 = 32/3 + 25/3 = 57/3 = 19

**8**：v(t) = ∫ (6t-4) dt = 3t^2 - 4t + C，由 v(0)=3 得 C=3，v(t)=3t^2-4t+3。s(t) = ∫ (3t^2-4t+3) dt = t^3 - 2t^2 + 3t + D，由 s(0)=0 得 D=0，s(t)=t^3-2t^2+3t

---
---

# 第 8 章：三角学（含弧度法）

## 引言与考纲对照

三角学是附加数学中工具性最强、应用最广的章节之一。从几何中的角度测量，到微积分中对三角函数求导与积分，再到物理中的运动分析，三角学无处不在。本章将系统性构建你对三角函数的完整理解。

### 考纲对照（Cambridge IGCSE Additional Mathematics 0606, 2028–2030）

| 考纲条目 | 内容 | 对应本节 |
|---------|------|---------|
| 9.1 | 弧长与扇形面积（弧度制） | **8.1** |
| 10.1 | 六个任意角三角函数 | **8.2** |
| 10.2 | 三角函数的振幅与周期 | **8.3** |
| 10.3 | 绘制 y = a sin(bx) + c 等图像 | **8.3** |
| 10.4 | 使用 sin²A + cos²A = 1 等恒等式 | **8.4** |
| 10.5 | 解三角方程（含六个函数） | **8.5** |
| 10.6 | 证明三角恒等式 | **8.6** |

> **考试信息**：Paper 1（非计算器）和 Paper 2（可用计算器）均会考察三角学。弧度制在微积分部分**强制使用**。考纲提供的公式表中仅列出 sin²A + cos²A = 1、sec²A = 1 + tan²A、csc²A = 1 + cot²A 三个恒等式。**弧长与扇形面积公式不提供**，需牢记。

---

## 8.1 弧度制（弧长、扇形面积、组合图形）

### 8.1.1 为什么要使用弧度？

在初等几何中，我们习惯用**度**（degree）来度量角。但在高等数学中，**弧度**（radian）才是自然的单位。原因有两个：

**原因一**：弧度将角度与弧长直接联系起来。当角度用弧度表示时，弧长公式 s = rθ 极其简洁。如果用度，公式将变为 s = πrθ/180，多了一个不必要的系数。

**原因二**（更重要）：微积分中三角函数的导数公式只有在弧度制下才简洁优美。例如：

d/dx (sin x) = cos x （弧度制）

如果使用度，公式将变为 d/dx (sin x°) = (π/180) cos x°，多出了常数因子 π/180。因此在 IGCSE 附加数学的微积分部分，**所有角度必须使用弧度制**。

### 8.1.2 弧度的定义

**定义**：一弧度是弧长等于半径时所对应的圆心角。

设圆的半径为 r，一段弧的长度为 s，该弧所对的圆心角为 θ（弧度），则有：

θ = s / r  或等价地  s = rθ

当 s = r 时，θ = 1 弧度。

**与度的换算推导**：整圆对应的圆心角为 360°，整圆周长为 2πr。由弧长公式 s = rθ，整圆对应：

2πr = r × (整圆的弧度数)

因此整圆的弧度数为 2π，即：

360° = 2π 弧度

两边除以 2：

180° = π 弧度

由此可推导出所有换算关系：

1° = π/180 弧度，  1 弧度 = 180°/π ≈ 57.3°

**常见角的弧度值**：

| 角度 | 0° | 30° | 45° | 60° | 90° | 120° | 135° | 150° | 180° | 270° | 360° |
|------|-----|-----|-----|-----|-----|------|------|------|------|------|------|
| 弧度 | 0 | π/6 | π/4 | π/3 | π/2 | 2π/3 | 3π/4 | 5π/6 | π | 3π/2 | 2π |

**记忆技巧**：记住 π = 180°，然后按比例推算。例如 30° = 180°/6 = π/6。

### 8.1.3 弧长公式的推导

在半径为 r 的圆中，整圆周长为 2πr，对应圆心角 2π 弧度。

设圆心角为 θ 弧度，它所对的弧长为 s。由于弧长与圆心角成正比：

s / (2πr) = θ / (2π)

交叉相乘：

s = (θ / (2π)) × 2πr = rθ

因此：

s = rθ

其中 θ **必须为弧度**。

### 8.1.4 扇形面积公式的推导

方法一（比例法）：整圆面积为 πr²，对应 2π 弧度。扇形面积 A 与整圆面积之比等于圆心角 θ 与 2π 之比：

A / (πr²) = θ / (2π)

A = (θ / (2π)) × πr² = (1/2) r²θ

方法二（积分法，微积分视角）：将扇形视为由无数个细小的三角形组成。每个小三角形的面积近似为 (1/2) r · r dθ = (1/2) r² dθ。从 0 到 θ 积分：

A = ∫₀^θ (1/2) r² dθ = (1/2) r²θ

两种方法得到相同结果：

A = (1/2) r²θ

### 8.1.5 弓形面积

在扇形中，连接弧的两个端点的线段称为**弦**。弦与弧之间的区域称为**弓形**（segment）。

**弓形面积的推导**：

弓形面积 = 扇形面积 - 三角形面积

扇形面积我们已经知道为 (1/2) r²θ。三角形是由两条半径和弦围成的等腰三角形，其面积可以用“两边夹一角”公式计算：

A_△ = (1/2) · r · r · sin θ = (1/2) r² sin θ

因此：

A_弓形 = (1/2) r²θ - (1/2) r² sin θ = (1/2) r² (θ - sin θ)

> ⚠️ **注意**：此公式中的 θ 必须是弧度制，且为扇形的圆心角。

### 8.1.6 组合图形的解题策略

当遇到包含圆弧、扇形、三角形的组合图形时，通用的解题思路是：

1. **分解图形**：将复杂图形拆分为若干个扇形、三角形、矩形等基本图形
2. **确定已知量**：标出所有已知的半径、角度（注意是弧度还是度）、边长
3. **统一单位**：角度全部转换为弧度（如果不是弧度的话）
4. **分别计算**：用弧长、扇形面积、三角形面积公式分别计算各部分
5. **组合结果**：根据图形关系相加或相减

### 8.1.7 例题

---

**例题 1（角度与弧度互化）**：
(a) 将 150° 转换为弧度。
(b) 将 5π/6 弧度转换为度。

**解**：

(a) 由 1° = π/180 弧度：

150° = 150 × (π/180) = (150π)/180 = 5π/6 弧度

(b) 由 1 弧度 = 180°/π：

(5π/6) 弧度 = (5π/6) × (180°/π) = (5 × 180°)/6 = 150°

**答案**：(a) 5π/6 弧度 (b) 150°

---

**例题 2（已知半径和圆心角求弧长与扇形面积）**：一个扇形的半径为 12 cm，圆心角为 2π/3 弧度。求：
(a) 弧长
(b) 扇形面积

**解**：

(a) 代入弧长公式 s = rθ：

s = 12 × (2π/3) = 8π cm

(b) 代入扇形面积公式 A = (1/2) r²θ：

A = (1/2) × 12² × (2π/3) = (1/2) × 144 × (2π/3) = 72 × (2π/3) = 48π cm²

**答案**：(a) 8π cm  (b) 48π cm²

---

**例题 3（已知弧长求圆心角和扇形面积）**：一个扇形的半径为 10 cm，弧长为 25 cm。求：
(a) 扇形的圆心角（弧度）
(b) 扇形的面积

**解**：

(a) 由 s = rθ 解出 θ：

θ = s / r = 25 / 10 = 2.5 弧度

(b) 代入扇形面积公式：

A = (1/2) r²θ = (1/2) × 10² × 2.5 = (1/2) × 100 × 2.5 = 125 cm²

**答案**：(a) 2.5 弧度  (b) 125 cm²

---

**例题 4（已知扇形面积求圆心角和弧长）**：一个半径为 6 cm 的扇形面积为 15π cm²。求：
(a) 扇形的圆心角（弧度）
(b) 扇形的弧长

**解**：

(a) 由 A = (1/2) r²θ 解出 θ：

15π = (1/2) × 6² × θ = (1/2) × 36 × θ = 18θ

θ = 15π / 18 = 5π/6 弧度

(b) 代入弧长公式：

s = rθ = 6 × (5π/6) = 5π cm

**答案**：(a) 5π/6 弧度  (b) 5π cm

---

**例题 5（弓形面积）**：一个半径为 8 cm 的圆中，圆心角为 π/4 的扇形被截去三角形部分，求剩余弓形的面积。

**解**：

**步骤 1**：计算扇形面积。

A_扇 = (1/2) r²θ = (1/2) × 8² × (π/4) = (1/2) × 64 × (π/4) = 8π cm²

**步骤 2**：计算三角形面积（两边为半径 8 cm，夹角 π/4）。

A_△ = (1/2) r² sin θ = (1/2) × 8² × sin(π/4) = (1/2) × 64 × (√2/2) = 16√2 cm²

**步骤 3**：弓形面积 = 扇形面积 - 三角形面积。

A_弓 = 8π - 16√2 cm²

**答案**：8π - 16√2 cm²

---

**例题 6（组合图形——两个扇形）**：下图由一个半径为 5 cm 的大扇形（圆心角 π/3）和一个半径为 3 cm 的小扇形（相同的圆心角）组合而成（即一个“环形扇形”）。求阴影区域（两个扇形之间的区域）的面积。

**解**：

**思路**：阴影区域面积 = 大扇形面积 - 小扇形面积。

**步骤 1**：大扇形面积。

A_大 = (1/2) × 5² × (π/3) = (1/2) × 25 × (π/3) = 25π/6 cm²

**步骤 2**：小扇形面积。

A_小 = (1/2) × 3² × (π/3) = (1/2) × 9 × (π/3) = 3π/2 cm²

**步骤 3**：阴影面积。

A = A_大 - A_小 = 25π/6 - 3π/2 = 25π/6 - 9π/6 = 16π/6 = 8π/3 cm²

**答案**：8π/3 cm²

---

**例题 7（组合图形——扇形与三角形）**：一个扇形的半径为 10 cm，圆心角为 60°。在扇形内作一个最大的等腰三角形，其中两条边为扇形的两条半径，底边为弦。求扇形中除去三角形后的剩余面积。

**解**：

**步骤 1**：先将 60° 转换为弧度。

θ = 60° × (π/180°) = π/3

**步骤 2**：扇形面积。

A_扇 = (1/2) × 10² × (π/3) = 50 × (π/3) = 50π/3 cm²

**步骤 3**：三角形面积。等腰三角形的顶角为 π/3，腰长为 10 cm。

A_△ = (1/2) × 10 × 10 × sin(π/3) = 50 × (√3/2) = 25√3 cm²

**步骤 4**：剩余面积。

A = 50π/3 - 25√3 cm²

**答案**：50π/3 - 25√3 cm²

---

> ⚠️ **易错提醒**：
> 1. 弧长和扇形面积公式中的 θ **必须使用弧度制**，不能使用度
> 2. 弓形面积公式中 θ - sin θ 两项中的 θ 都是弧度值
> 3. 遇到混合了度和弧度的题目，先统一单位再计算

---

## 8.2 六个三角函数（任意角）

### 8.2.1 从锐角三角比到任意角三角函数

在直角三角形中，对于锐角 θ，我们最初的定义是：

sin θ = 对边/斜边， cos θ = 邻边/斜边， tan θ = 对边/邻边

但这个定义有严重的局限性——它只适用于 0° < θ < 90° 的角。如果角度大于 90° 或是负角，直角三角形就无法直接定义了。

**突破**：我们将角度放在**坐标系**中，用**单位圆**来重新定义三角函数，从而将定义域扩展到全体实数。

### 8.2.2 单位圆定义法

**单位圆**是圆心在原点、半径为 1 的圆，方程为：

x² + y² = 1

对于任意角 θ，我们按以下方式放置它：
- 角的顶点在原点
- 角的起始边沿正 x 轴方向
- 角的终边从起始边逆时针旋转 θ（若 θ 为负则顺时针旋转）

设角的终边与单位圆的交点为 P(x, y)，则定义：

sin θ = y， cos θ = x， tan θ = y/x (x ≠ 0)

**为什么这样定义是合理的？**

当 θ 为锐角时，我们在单位圆上得到的点 P 恰好构成一个直角三角形——从 P 向 x 轴作垂线，得到直角三角形的对边为 y，邻边为 x，斜边为 1。因此 sin θ = y/1 = y，cos θ = x/1 = x，与直角三角形定义完全一致。

而当 θ 为任意角时，x 和 y 坐标可以为正、零或负，三角函数的符号也随之变化——这正是我们想要的！

### 8.2.3 六个三角函数的完整定义

由 sin θ 和 cos θ 出发，可以定义另外四个函数：

**正切**：

tan θ = sin θ / cos θ = y/x， cos θ ≠ 0

**余割**（sin 的倒数）：

csc θ = 1 / sin θ = 1/y， sin θ ≠ 0

**正割**（cos 的倒数）：

sec θ = 1 / cos θ = 1/x， cos θ ≠ 0

**余切**（tan 的倒数）：

cot θ = 1 / tan θ = cos θ / sin θ = x/y， sin θ ≠ 0

**六个函数一览表**：

| 函数 | 记号 | 单位圆定义 | 定义域限制 |
|------|------|-----------|-----------|
| 正弦 | sin θ | y | 全体实数 |
| 余弦 | cos θ | x | 全体实数 |
| 正切 | tan θ | y/x | x ≠ 0，即 θ ≠ π/2 + nπ |
| 余割 | csc θ | 1/y | y ≠ 0，即 θ ≠ nπ |
| 正割 | sec θ | 1/x | x ≠ 0，即 θ ≠ π/2 + nπ |
| 余切 | cot θ | x/y | y ≠ 0，即 θ ≠ nπ |

### 8.2.4 特殊角的三角函数值推导

**特殊三角形法**：

**(a) 45°（π/4）角的推导**

考虑一个等腰直角三角形，两直角边均为 1，斜边为 √2。

sin(π/4) = 对边/斜边 = 1/√2 = √2/2

cos(π/4) = 邻边/斜边 = 1/√2 = √2/2

tan(π/4) = 对边/邻边 = 1/1 = 1

**(b) 30°（π/6）和 60°（π/3）角的推导**

考虑一个 30°-60°-90° 的直角三角形，三边比例为 1 : √3 : 2（30° 对边为 1，60° 对边为 √3，斜边为 2）。

对于 30°：

sin(π/6) = 1/2， cos(π/6) = √3/2， tan(π/6) = 1/√3

对于 60°：

sin(π/3) = √3/2， cos(π/3) = 1/2， tan(π/3) = √3

**(c) 0° 和 90° 的推导**

在单位圆上，θ = 0 时终边与正 x 轴重合，交点为 (1, 0)，所以 sin 0 = 0，cos 0 = 1，tan 0 = 0/1 = 0。

θ = π/2 时终边与正 y 轴重合，交点为 (0, 1)，所以 sin(π/2) = 1，cos(π/2) = 0，tan(π/2) 无定义（分母为零）。

**完整特殊角值表**：

| θ | 0 | π/6 | π/4 | π/3 | π/2 | π | 3π/2 |
|----|----|------|------|------|------|-----|-------|
| sin θ | 0 | 1/2 | √2/2 | √3/2 | 1 | 0 | -1 |
| cos θ | 1 | √3/2 | √2/2 | 1/2 | 0 | -1 | 0 |
| tan θ | 0 | 1/√3 | 1 | √3 | 无定义 | 0 | 无定义 |

### 8.2.5 符号法则——ASTC

三角函数在四个象限中的符号由单位圆上 x、y 坐标的符号决定。

| 象限 | 角度范围 | x = cos θ | y = sin θ | tan θ = y/x | 正值函数 |
|------|---------|-----------|-----------|-------------|---------|
| I | 0 < θ < π/2 | + | + | + | **A**ll（全部） |
| II | π/2 < θ < π | - | + | - | **S**in（及 csc） |
| III | π < θ < 3π/2 | - | - | + | **T**an（及 cot） |
| IV | 3π/2 < θ < 2π | + | - | - | **C**os（及 sec） |

**记忆口诀**：逆时针从第一象限开始，ASTC —— “All Students Take Calculus”（所有学生学微积分）。

完整的六个函数符号表：

| 象限 | sin | cos | tan | sec | csc | cot |
|------|-----|-----|-----|-----|-----|-----|
| I | + | + | + | + | + | + |
| II | + | - | - | - | + | - |
| III | - | - | + | - | - | + |
| IV | - | + | - | + | - | - |

### 8.2.6 参考角法

**参考角**（reference angle）是指角的终边与 x 轴之间的最小夹角，通常记为 α，且 0 ≤ α ≤ π/2。

对于任意角 θ，其在 [0, 2π) 内的参考角 α 为：

| θ 所在象限 | 参考角 α |
|-----------|---------|
| I | α = θ |
| II | α = π - θ |
| III | α = θ - π |
| IV | α = 2π - θ |

> **核心性质**：任意角的三角函数值等于其参考角的三角函数值的绝对值，再根据象限确定正负号。即：
> sin θ = ± sin α， cos θ = ± cos α， tan θ = ± tan α
> 其中正负号由 θ 所在象限决定。

### 8.2.7 例题

---

**例题 1（已知 sin 求其他函数——锐角情况）**：已知 sin θ = 4/5 且 0 < θ < π/2，求 cos θ、tan θ、sec θ、csc θ、cot θ 的值。

**解**：

**步骤 1**：利用 sin²θ + cos²θ = 1 求 cos²θ。

cos²θ = 1 - sin²θ = 1 - (4/5)² = 1 - 16/25 = 9/25

**步骤 2**：确定 cos θ 的符号。θ 在第一象限，cos θ > 0，所以：

cos θ = √(9/25) = 3/5

**步骤 3**：依次求其他函数。

tan θ = sin θ / cos θ = (4/5) / (3/5) = 4/3

sec θ = 1 / cos θ = 1 / (3/5) = 5/3

csc θ = 1 / sin θ = 1 / (4/5) = 5/4

cot θ = 1 / tan θ = 1 / (4/3) = 3/4

**答案**：cos θ = 3/5，tan θ = 4/3，sec θ = 5/3，csc θ = 5/4，cot θ = 3/4

---

**例题 2（已知 sin 求其他函数——任意角情况）**：已知 sin θ = 3/5 且 θ 在第二象限，求 cos θ、tan θ、sec θ、csc θ、cot θ 的值。

**解**：

**步骤 1**：利用 sin²θ + cos²θ = 1 求 cos²θ。

cos²θ = 1 - sin²θ = 1 - (3/5)² = 1 - 9/25 = 16/25

**步骤 2**：确定 cos θ 的符号。θ 在第二象限，cos θ < 0，所以：

cos θ = -√(16/25) = -4/5

**步骤 3**：依次求其他函数。

tan θ = sin θ / cos θ = (3/5) / (-4/5) = -3/4

sec θ = 1 / cos θ = 1 / (-4/5) = -5/4

csc θ = 1 / sin θ = 1 / (3/5) = 5/3

cot θ = 1 / tan θ = 1 / (-3/4) = -4/3

**答案**：cos θ = -4/5，tan θ = -3/4，sec θ = -5/4，csc θ = 5/3，cot θ = -4/3

> **对比**：与例题 1 相比，θ 从第一象限变为第二象限，cos 和 tan 的符号发生了变化（由正变负），但绝对值相同。这正是参考角法的体现。

---

**例题 3（参考角法求任意角三角函数值）**：求 sin(5π/6)、cos(5π/6)、tan(5π/6) 的精确值。

**解**：

**步骤 1**：确定 θ = 5π/6 所在的象限。

5π/6 对应 150°，在第二象限（介于 π/2 和 π 之间）。

**步骤 2**：求参考角。

第二象限的参考角为 α = π - θ = π - 5π/6 = π/6。

**步骤 3**：确定各函数的符号。

在第二象限，sin 为正，cos 为负，tan 为负。

**步骤 4**：写出答案。

sin(5π/6) = + sin(π/6) = 1/2

cos(5π/6) = - cos(π/6) = -√3/2

tan(5π/6) = - tan(π/6) = -1/√3

---

**例题 4（参考角法——第四象限角）**：求 sin(7π/4)、cos(7π/4)、tan(7π/4) 的精确值。

**解**：

**步骤 1**：确定象限。7π/4 对应 315°，在第四象限。

**步骤 2**：求参考角。第四象限的参考角为 α = 2π - θ = 2π - 7π/4 = π/4。

**步骤 3**：确定符号。第四象限中，sin 为负，cos 为正，tan 为负。

**步骤 4**：写出答案。

sin(7π/4) = - sin(π/4) = -√2/2

cos(7π/4) = + cos(π/4) = √2/2

tan(7π/4) = - tan(π/4) = -1

---

**例题 5（已知 tan 求其他函数）**：已知 tan θ = 2 且 π < θ < 3π/2，求 sin θ 和 cos θ 的值。

**解**：

**步骤 1**：确定 θ 在第三象限（π 到 3π/2）。在第三象限，sin 和 cos 均为负值。

**步骤 2**：由 tan θ = sin θ / cos θ = 2，可知 sin θ = 2 cos θ。

**步骤 3**：代入 sin²θ + cos²θ = 1。

(2 cos θ)² + cos²θ = 1

4 cos²θ + cos²θ = 1

5 cos²θ = 1

cos²θ = 1/5

**步骤 4**：确定符号。θ 在第三象限，cos θ < 0，所以：

cos θ = -√(1/5) = -1/√5

**步骤 5**：求 sin θ。

sin θ = 2 cos θ = 2 × (-1/√5) = -2/√5

**答案**：sin θ = -2/√5，cos θ = -1/√5

---

**例题 6（已知 sec 求其他函数）**：已知 sec θ = 3 且 3π/2 < θ < 2π，求 sin θ、cos θ、tan θ。

**解**：

**步骤 1**：由 sec θ = 1 / cos θ = 3 得 cos θ = 1/3。θ 在第四象限，cos θ > 0，符号一致。

**步骤 2**：由 sin²θ + cos²θ = 1：

sin²θ = 1 - cos²θ = 1 - 1/9 = 8/9

**步骤 3**：确定符号。θ 在第四象限，sin θ < 0，所以：

sin θ = -√(8/9) = -2√2/3

**步骤 4**：求 tan θ。

tan θ = sin θ / cos θ = (-2√2/3) / (1/3) = -2√2

**答案**：sin θ = -2√2/3，cos θ = 1/3，tan θ = -2√2

---

**例题 7（已知 cot 求角度）**：已知 cot θ = √3 且 π < θ < 2π，求 θ 的可能值（弧度）。

**解**：

**步骤 1**：cot θ = √3 意味着 tan θ = 1/√3 = √3/3。

**步骤 2**：求参考角。tan α = √3/3 时，α = π/6。

**步骤 3**：确定 tan θ > 0 的象限。正切为正发生在第一和第三象限。

**步骤 4**：给定范围 π < θ < 2π（第三和第四象限），结合 tan θ > 0，θ 只能在第三象限：

θ = π + α = π + π/6 = 7π/6

**答案**：θ = 7π/6

---

## 8.3 三角函数的图像（振幅、周期、渐近线）

### 8.3.1 基本三角函数的图像

#### y = sin x

先列出 [0, 2π] 区间内的关键点：

| x | 0 | π/2 | π | 3π/2 | 2π |
|---|----|------|----|------|----|
| sin x | 0 | 1 | 0 | -1 | 0 |

**性质总结**：

- **定义域**：R（全体实数）
- **值域**：[-1, 1]
- **周期性**：周期为 2π，即 sin(x + 2π) = sin x
- **奇偶性**：奇函数，sin(-x) = -sin x，图像关于原点对称
- **零点**：x = nπ（n ∈ Z）
- **最大值**：在 x = π/2 + 2nπ 处取 1
- **最小值**：在 x = 3π/2 + 2nπ 处取 -1

图像形态：从 0 开始上升，像波浪般周期性振荡。

#### y = cos x

关键点：

| x | 0 | π/2 | π | 3π/2 | 2π |
|---|----|------|----|------|----|
| cos x | 1 | 0 | -1 | 0 | 1 |

**性质总结**：

- **定义域**：R
- **值域**：[-1, 1]
- **周期性**：周期 2π
- **奇偶性**：偶函数，cos(-x) = cos x，图像关于 y 轴对称
- **零点**：x = π/2 + nπ
- **最大值**：在 x = 2nπ 处取 1
- **最小值**：在 x = π + 2nπ 处取 -1

**正弦与余弦的关系**：

cos x = sin(x + π/2)， sin x = cos(x - π/2)

即余弦曲线是正弦曲线向左平移 π/2 的结果。

#### y = tan x

关键点和渐近线：

| x | -π/2 | 0 | π/2 | π | 3π/2 |
|----|------|----|------|----|------|
| tan x | 无定义 | 0 | 无定义 | 0 | 无定义 |

**性质总结**：

- **定义域**：x ≠ π/2 + nπ（在这些点 cos x = 0，正切无定义）
- **值域**：R（全体实数）
- **周期性**：周期 π，即 tan(x + π) = tan x
- **奇偶性**：奇函数，tan(-x) = -tan x，关于原点对称
- **零点**：x = nπ
- **渐近线**：x = π/2 + nπ（垂直渐近线）

图像形态：在每个周期 (-π/2, π/2) 内，从负无穷经过 0 上升到正无穷。

#### y = sec x、y = csc x、y = cot x 的图像概要

- y = sec x = 1 / cos x：在 cos x = 0（x = π/2 + nπ）处有垂直渐近线，值域 (-∞, -1] ∪ [1, ∞)，周期 2π，偶函数
- y = csc x = 1 / sin x：在 sin x = 0（x = nπ）处有垂直渐近线，值域 (-∞, -1] ∪ [1, ∞)，周期 2π，奇函数
- y = cot x = cos x / sin x：在 sin x = 0（x = nπ）处有垂直渐近线，值域 R，周期 π，奇函数

### 8.3.2 三角函数的变换

考虑一般形式 y = a sin(bx + c) + d（对 cos 和 tan 也适用，虽然 tan 没有振幅的概念）。

#### 振幅（Amplitude）

参数 a 控制垂直方向的拉伸或压缩。对于正弦和余弦，|a| 是波形偏离中心线的最大距离。

**推导**：sin x 的值域为 [-1, 1]，乘以 a 后值域变为 [-|a|, |a|]（若 a > 0）或 [|a|, -|a|]（若 a < 0）。因此振幅为 |a|。

**示例**：y = 3 sin x 的振幅为 3，最大值 3，最小值 -3。

#### 周期（Period）

参数 b 控制水平方向的拉伸或压缩。

**推导**：sin x 的周期为 2π，即 sin(x + 2π) = sin x。对于 y = sin(bx)，我们希望找到最小的正数 T 使得 sin(b(x + T)) = sin(bx)。由于 sin 的周期为 2π，我们需要 bT = 2π，即：

T = 2π / |b|

对 tan(bx)，由于 tan x 的周期为 π，所以：

T = π / |b|

**示例**：y = sin(2x) 的周期为 T = 2π/2 = π。y = tan(x/2) 的周期为 T = π / (1/2) = 2π。

#### 相移（Phase Shift）

参数 c 引起水平平移。

**推导**：

y = sin(bx + c) = sin[b(x + c/b)]

这相当于将 y = sin(bx) 的图像向左平移 c/b 个单位。若 c/b > 0 则左移，c/b < 0 则右移。**相移量**通常定义为 -c/b（正数表示右移）。

#### 垂直平移（Vertical Shift）

参数 d 将整个图像向上（d > 0）或向下（d < 0）平移 |d| 个单位。d 也是新图像的中心线（中轴线）的纵坐标。

**综合公式**：对于 y = a sin(bx + c) + d：

| 参数 | 名称 | 计算公式 |
|------|------|---------|
| |a| | 振幅 | 最大值 = d + |a|，最小值 = d - |a| |
| T = 2π/|b| | 周期 | 对 tan 为 π/|b| |
| -c/b | 相移 | >0 右移，<0 左移 |
| d | 垂直平移 | 新中心线为 y = d |

### 8.3.3 图像绘制方法

**绘制 y = a sin(bx + c) + d 的步骤**：

1. 确定振幅 |a|、周期 T = 2π/|b|、相移 -c/b、垂直平移 d
2. 找出一个完整周期内的关键点（通常取 5 个点：起点、峰点、中点、谷点、终点）
3. 标出中心线 y = d，标出最大值 d + |a| 和最小值 d - |a|
4. 从相移后的起点开始，每隔 T/4 取一个关键点
5. 用平滑曲线连接各点

### 8.3.4 例题

---

**例题 1（确定变换参数）**：对于函数 y = 4 cos(3x + π/2) - 2，求振幅、周期、相移和垂直平移，并写出其最大值和最小值。

**解**：

与标准形式 y = a cos(bx + c) + d 对比：

a = 4, b = 3, c = π/2, d = -2

**振幅**：|a| = |4| = 4

**周期**：T = 2π/|b| = 2π/3

**相移**：-c/b = -(π/2)/3 = -π/6（负值表示向左平移 π/6）

**垂直平移**：d = -2（向下平移 2 个单位）

**最大值**：d + |a| = -2 + 4 = 2

**最小值**：d - |a| = -2 - 4 = -6

---

**例题 2（由图像特征求函数表达式——修正版）**：一个正弦型函数的图像满足以下条件：振幅为 2，周期为 π，在 x = 0 处函数值为 1（中轴线位置），且正在上升，图像垂直平移使得中轴线为 y = 1。写出该函数的一个可能表达式。

**解**：

**步骤 1**：设函数为 y = a sin(bx + c) + d。

**步骤 2**：由振幅 2 得 |a| = 2，取 a = 2。

**步骤 3**：由周期 T = π 得 T = 2π/|b| = π，所以 |b| = 2，取 b = 2。

**步骤 4**：由中轴线 y = 1 得 d = 1。

**步骤 5**：由 x = 0 时 y = 1（中轴线上）且正在上升——说明此时正弦的自变量为 0（因为 sin 0 = 0 且在 0 附近上升）：

2 sin(2 × 0 + c) + 1 = 1 ⇒ 2 sin c + 1 = 1 ⇒ sin c = 0

sin c = 0 的解为 c = nπ。当 c = 0 时，y = 2 sin(2x) + 1，在 x = 0 处：
- y = 1（中轴线）
- 导数 y' = 4 cos(2x)，在 x = 0 处 y' = 4 > 0，正在上升 ✓

**答案**：y = 2 sin(2x) + 1

---

**例题 3（正切函数的渐近线）**：求函数 y = 3 tan(2x - π/3) + 1 的周期和在一个周期内的渐近线方程。

**解**：

**步骤 1**：求周期。对于 tan，T = π/|b| = π/2。

**步骤 2**：求渐近线。tan(u) 在 u = π/2 + nπ 处有渐近线。

令 2x - π/3 = π/2 + nπ：

2x = π/2 + π/3 + nπ = 3π/6 + 2π/6 + nπ = 5π/6 + nπ

x = 5π/12 + nπ/2

**步骤 3**：取 n = 0 和 n = 1（覆盖一个周期 π/2 内的两条渐近线）：

x = 5π/12, x = 5π/12 + π/2 = 5π/12 + 6π/12 = 11π/12

**答案**：周期为 π/2，渐近线为 x = 5π/12 + nπ/2 (n ∈ Z)

---

**例题 4（图像变换——从 y = sin x 到 y = 2 sin(3x) + 1）**：描述如何通过变换 y = sin x 的图像得到 y = 2 sin(3x) + 1 的图像。

**解**：

**步骤 1**：水平压缩。y = sin x → y = sin(3x)：将周期从 2π 压缩为 2π/3，频率变为原来的 3 倍。

**步骤 2**：垂直拉伸。y = sin(3x) → y = 2 sin(3x)：振幅从 1 变为 2，最大值从 1 变为 2，最小值从 -1 变为 -2。

**步骤 3**：垂直平移。y = 2 sin(3x) → y = 2 sin(3x) + 1：整个图像向上平移 1 个单位，新的中轴线为 y = 1。

**变换顺序**：先水平变换（周期），再垂直变换（振幅），最后垂直平移。

---

**例题 5（由图像求函数——已知点）**：一个余弦型函数 y = a cos(bx) + d 的图像经过点 (0, 5) 和 (π, -1)，且周期为 2π。求 a、b、d 的值。

**解**：

**步骤 1**：由周期 T = 2π 得 T = 2π/|b| = 2π，所以 |b| = 1，取 b = 1。

**步骤 2**：代入 (0, 5)：y = a cos(0) + d = a + d = 5

**步骤 3**：代入 (π, -1)：y = a cos(π) + d = -a + d = -1

**步骤 4**：解联立方程组：

a + d = 5
-a + d = -1

两式相加：2d = 4 ⇒ d = 2
代入第一式：a + 2 = 5 ⇒ a = 3

**答案**：a = 3，b = 1，d = 2，函数为 y = 3 cos x + 2

---

**例题 6（绘制图像要点）**：对于函数 y = 2 sin(x/2) - 1，在区间 [0, 4π] 内：
(a) 求振幅、周期和垂直平移
(b) 写出关键点的坐标
(c) 描述绘制图像的步骤

**解**：

(a)

- 振幅：|a| = 2
- 周期：T = 2π/|b| = 2π/(1/2) = 4π
- 垂直平移：d = -1（向下 1 个单位）
- 最大值：d + |a| = -1 + 2 = 1
- 最小值：d - |a| = -1 - 2 = -3
- 中轴线：y = -1

(b) 一个周期 [0, 4π] 内的 5 个关键点（间隔 T/4 = π）：

| x | 0 | π | 2π | 3π | 4π |
|---|----|----|----|----|----|
| x/2 | 0 | π/2 | π | 3π/2 | 2π |
| sin(x/2) | 0 | 1 | 0 | -1 | 0 |
| y = 2 sin(x/2) - 1 | -1 | 1 | -1 | -3 | -1 |

(c) **绘制步骤**：

1. 画出中轴线 y = -1（虚线）
2. 标出最大值 y = 1 和最小值 y = -3 的水平线（虚线）
3. 标出 5 个关键点：(0, -1)、(π, 1)、(2π, -1)、(3π, -3)、(4π, -1)
4. 用平滑的波浪线连接各点

---

**例题 7（正切图像的渐近线和关键点）**：在区间 [0, π] 内，找出函数 y = tan(2x - π/4) 的渐近线方程和与 x 轴的交点。

**解**：

**步骤 1**：求渐近线。tan u 在 u = π/2 + nπ 处有渐近线。

令 2x - π/4 = π/2 + nπ：

2x = π/2 + π/4 + nπ = 3π/4 + nπ

x = 3π/8 + nπ/2

在 [0, π] 内，n = 0 和 n = 1：

x = 3π/8, x = 3π/8 + π/2 = 3π/8 + 4π/8 = 7π/8

**步骤 2**：求与 x 轴的交点。令 y = 0：

tan(2x - π/4) = 0

tan u = 0 时 u = nπ：

2x - π/4 = nπ

2x = π/4 + nπ

x = π/8 + nπ/2

在 [0, π] 内，n = 0 和 n = 1：

x = π/8, x = π/8 + π/2 = π/8 + 4π/8 = 5π/8

**答案**：渐近线为 x = 3π/8 和 x = 7π/8；与 x 轴交点为 x = π/8 和 x = 5π/8

---

## 8.4 三角恒等式

### 8.4.1 三个基本勾股恒等式

**恒等式一：sin²θ + cos²θ = 1**

**推导**：在单位圆上，点 (cos θ, sin θ) 在圆 x² + y² = 1 上，代入即得：

(cos θ)² + (sin θ)² = 1

即 sin²θ + cos²θ = 1。

**恒等式二：sec²θ = 1 + tan²θ**

**推导**：将 sin²θ + cos²θ = 1 两边除以 cos²θ（假设 cos θ ≠ 0）：

sin²θ/cos²θ + cos²θ/cos²θ = 1/cos²θ

tan²θ + 1 = sec²θ

即 sec²θ = 1 + tan²θ。

**恒等式三：csc²θ = 1 + cot²θ**

**推导**：将 sin²θ + cos²θ = 1 两边除以 sin²θ（假设 sin θ ≠ 0）：

sin²θ/sin²θ + cos²θ/sin²θ = 1/sin²θ

1 + cot²θ = csc²θ

即 csc²θ = 1 + cot²θ。

> ✅ **考试提示**：这三个恒等式在考纲的**公式表**中提供，考试时可以直接引用。

### 8.4.2 二倍角公式

虽然考纲未明确列出二倍角公式，但这些公式可以从基本恒等式中推导出来，并且在解方程和证明恒等式中极为常用。

**sin(2θ) 的推导**：

从和角公式 sin(A + B) = sin A cos B + cos A sin B 出发，令 A = B = θ：

sin(2θ) = sin θ cos θ + cos θ sin θ = 2 sin θ cos θ

因此：

sin(2θ) = 2 sin θ cos θ

**cos(2θ) 的推导**：

从和角公式 cos(A + B) = cos A cos B - sin A sin B，令 A = B = θ：

cos(2θ) = cos θ cos θ - sin θ sin θ = cos²θ - sin²θ

再利用 sin²θ + cos²θ = 1，可以得到另外两种形式：

由 sin²θ = 1 - cos²θ 代入：

cos(2θ) = cos²θ - (1 - cos²θ) = 2 cos²θ - 1

由 cos²θ = 1 - sin²θ 代入：

cos(2θ) = (1 - sin²θ) - sin²θ = 1 - 2 sin²θ

因此 cos(2θ) 有三种等价形式：

cos(2θ) = cos²θ - sin²θ = 2 cos²θ - 1 = 1 - 2 sin²θ

**tan(2θ) 的推导**：

从和角公式 tan(A + B) = (tan A + tan B) / (1 - tan A tan B)，令 A = B = θ：

tan(2θ) = 2 tan θ / (1 - tan²θ)

即：

tan(2θ) = 2 tan θ / (1 - tan²θ)

### 8.4.3 半角公式（由二倍角公式反推）

从 cos(2θ) = 2 cos²θ - 1 解出 cos²θ：

2 cos²θ = 1 + cos(2θ) ⇒ cos²θ = (1 + cos(2θ))/2

从 cos(2θ) = 1 - 2 sin²θ 解出 sin²θ：

2 sin²θ = 1 - cos(2θ) ⇒ sin²θ = (1 - cos(2θ))/2

这两个公式在**积分**中非常重要——它们用来降低三角函数的幂次。

### 8.4.4 例题

---

**例题 1（利用恒等式求值）**：已知 cos θ = 3/5 且 θ 在第四象限，求 sin θ、tan θ、sin(2θ)、cos(2θ) 的值。

**解**：

**步骤 1**：由 sin²θ + cos²θ = 1 求 sin²θ。

sin²θ = 1 - cos²θ = 1 - (3/5)² = 1 - 9/25 = 16/25

**步骤 2**：确定 sin θ 的符号。θ 在第四象限，sin θ < 0。

sin θ = -√(16/25) = -4/5

**步骤 3**：求 tan θ。

tan θ = sin θ / cos θ = (-4/5) / (3/5) = -4/3

**步骤 4**：求 sin(2θ)。

sin(2θ) = 2 sin θ cos θ = 2 × (-4/5) × (3/5) = -24/25

**步骤 5**：求 cos(2θ)（用 cos²θ - sin²θ 形式）。

cos(2θ) = cos²θ - sin²θ = (3/5)² - (-4/5)² = 9/25 - 16/25 = -7/25

**答案**：sin θ = -4/5，tan θ = -4/3，sin(2θ) = -24/25，cos(2θ) = -7/25

---

**例题 2（化简表达式并用恒等式求值）**：化简 sin(2θ) / (1 - cos(2θ))，并用此结果求当 θ = π/6 时的值。

**解**：

**步骤 1**：代入二倍角公式化简。

sin(2θ) / (1 - cos(2θ)) = 2 sin θ cos θ / (1 - (1 - 2 sin²θ))

**步骤 2**：化简分母。

1 - cos(2θ) = 1 - (1 - 2 sin²θ) = 2 sin²θ

**步骤 3**：化简整个表达式。

(2 sin θ cos θ) / (2 sin²θ) = cos θ / sin θ = cot θ

**步骤 4**：代入 θ = π/6。

cot(π/6) = cos(π/6) / sin(π/6) = (√3/2) / (1/2) = √3

**答案**：化简结果为 cot θ，当 θ = π/6 时值为 √3

---

**例题 3（利用 sec²θ = 1 + tan²θ 化简）**：化简 (sec²θ - 1) / sec²θ。

**解**：

**方法一**：

(sec²θ - 1) / sec²θ = ((1 + tan²θ) - 1) / sec²θ = tan²θ / sec²θ

因为 tan θ = sin θ / cos θ，sec θ = 1 / cos θ：

tan²θ / sec²θ = (sin²θ/cos²θ) / (1/cos²θ) = sin²θ

**方法二**（更直接）：

(sec²θ - 1) / sec²θ = 1 - 1/sec²θ = 1 - cos²θ = sin²θ

**答案**：sin²θ

---

**例题 4（用 cos(2θ) 表示 4 sin²θ - 3 cos²θ）**：用 cos(2θ) 表示 4 sin²θ - 3 cos²θ。

**解**：

**步骤 1**：代入半角公式。

sin²θ = (1 - cos(2θ))/2， cos²θ = (1 + cos(2θ))/2

**步骤 2**：代入原式。

4 sin²θ - 3 cos²θ = 4 × (1 - cos(2θ))/2 - 3 × (1 + cos(2θ))/2

**步骤 3**：化简。

= 2(1 - cos(2θ)) - (3/2)(1 + cos(2θ))

= 2 - 2 cos(2θ) - 3/2 - (3/2) cos(2θ)

= (2 - 3/2) + (-2 - 3/2) cos(2θ)

= 1/2 - (7/2) cos(2θ)

**答案**：1/2 - (7/2) cos(2θ)

---

**例题 5（求证恒等式并求值）**：证明 sin⁴θ - cos⁴θ = sin²θ - cos²θ，并由此求当 θ = π/3 时的值。

**解**：

**证明**：

左边 = sin⁴θ - cos⁴θ = (sin²θ)² - (cos²θ)²

利用平方差公式：

= (sin²θ - cos²θ)(sin²θ + cos²θ)

因为 sin²θ + cos²θ = 1：

= (sin²θ - cos²θ) × 1 = sin²θ - cos²θ

左边 = 右边，恒等式得证。

**求值**：代入 θ = π/3。

sin²(π/3) - cos²(π/3) = (√3/2)² - (1/2)² = 3/4 - 1/4 = 1/2

**答案**：恒等式得证，θ = π/3 时值为 1/2

---

**例题 6（利用 csc²θ = 1 + cot²θ 解方程的准备）**：化简表达式 (csc²θ - cot²θ) / csc²θ。

**解**：

**步骤 1**：由 csc²θ = 1 + cot²θ 得 csc²θ - cot²θ = 1。

**步骤 2**：代入原式。

(csc²θ - cot²θ) / csc²θ = 1 / csc²θ = sin²θ

**答案**：sin²θ

---

## 8.5 解三角方程

### 8.5.1 解题总策略（复习）

解三角方程的核心流程如下：

```
原方程
   │
   ▼
是否含不同名的函数？──是──→ 用恒等式化为同名函数
   │                               │
   否                               ▼
   │                           化简后的方程
   ▼                               │
化为基本形式：sin x = k,            │
cos x = k, tan x = k               │
   │                               │
   ▼                               ▼
求参考角 α
   │
   ▼
根据 k 的符号确定解所在象限（对 tan 直接加周期）
   │
   ▼
写出给定区间内的所有解
   │
   ▼
检查定义域，排除无效解
```

> **核心思想**：无论多复杂的三角方程，最终目标都是通过恒等变换和代数运算，将其化简为一个或多个基本形式（sin x = k、cos x = k、tan x = k），然后利用参考角法系统性地求出所有解。

---

### 8.5.2 基本形式 sin x = k（-1 ≤ k ≤ 1）

#### 几何推导——从单位圆理解

在单位圆上，sin θ = y 表示终边与单位圆交点的纵坐标。因此，方程 sin x = k 等价于：**在单位圆上，寻找终边与水平线 y = k 相交的所有角度 x**。

**情形一**：当 0 < k < 1 时。

水平线 y = k 与单位圆相交于两个点（对称于 y 轴）：
- 一个在第一象限，对应的角为 α（锐角）
- 另一个在第二象限，对应的角为 π - α

为什么第二象限的解是 π - α？

我们可以用诱导公式来理解。在单位圆上，角 π - α 的终边与角 α 的终边关于 y 轴对称。因此，它们的 y 坐标相同：

sin(π - α) = sin α

当 sin α = |k| 时，sin(π - α) = |k|。而 k > 0，所以 sin(π - α) = k。

**情形二**：当 -1 < k < 0 时。

水平线 y = k 位于 x 轴下方，同样与单位圆相交于两个点：
- 一个在第三象限，对应的角为 π + α
- 另一个在第四象限，对应的角为 2π - α

**推导 π + α**：角 π + α 的终边与角 α 的终边关于原点对称。因此：

sin(π + α) = -sin α = -|k|

由于 k < 0，-|k| = k，所以 sin(π + α) = k。

**推导 2π - α**：角 2π - α 的终边与角 α 的终边关于 x 轴对称：

sin(2π - α) = -sin α = -|k| = k

#### 完整的解法步骤

**步骤 1**：检查可行性。确认 |k| ≤ 1。若 |k| > 1，则方程无解（因为 sin 的值域为 [-1, 1]）。

**步骤 2**：求参考角。

α = arcsin(|k|)， α ∈ [0, π/2]

参考角 α 是一个介于 0 和 π/2 之间的锐角（或边界角），表示终边与 x 轴之间的最小夹角。

**步骤 3**：根据 k 的符号确定解所在的象限。

| k 的符号 | 解所在的象限 | 对应的角 |
|-----------|-------------|---------|
| k > 0 | 第一、第二象限 | x = α, x = π - α |
| k = 0 | x 轴正负方向 | x = 0, x = π（在 [0, 2π) 内） |
| k < 0 | 第三、第四象限 | x = π + α, x = 2π - α |

**步骤 4**：写出通解。由于 sin 的周期为 2π，所有解可表示为：

x = x₀ + 2nπ， n ∈ Z

其中 x₀ 是步骤 3 中求出的基本解。

#### 特殊情况

**(a) k = 0**：sin x = 0 的解。

在 [0, 2π) 内，sin x = 0 发生在 x = 0 和 x = π。通解为：

x = nπ， n ∈ Z

**(b) k = 1**：sin x = 1 的解。

在 [0, 2π) 内，sin x = 1 只在 x = π/2 处成立。通解为：

x = π/2 + 2nπ， n ∈ Z

**(c) k = -1**：sin x = -1 的解。

在 [0, 2π) 内，sin x = -1 只在 x = 3π/2 处成立。通解为：

x = 3π/2 + 2nπ， n ∈ Z

#### 例题

---

**例题 1（sin x = k，k > 0 标准情形）**：在 0 ≤ x < 2π 范围内解方程 sin x = √3/2。

**解**：

**步骤 1**：确认可行性。√3/2 ≈ 0.866 ≤ 1，有解。

**步骤 2**：求参考角。α = arcsin(√3/2) = π/3。

**步骤 3**：k = √3/2 > 0，解在第一和第二象限。

第一象限：x = α = π/3

第二象限：x = π - α = π - π/3 = 2π/3

**步骤 4**：验证。sin(π/3) = √3/2 ✓，sin(2π/3) = sin(π/3) = √3/2 ✓

**答案**：x = π/3 和 x = 2π/3

---

**例题 2（sin x = k，k < 0 标准情形）**：在 0 ≤ x < 2π 范围内解方程 sin x = -1/2。

**解**：

**步骤 1**：确认可行性。|-1/2| = 1/2 ≤ 1，有解。

**步骤 2**：求参考角。α = arcsin(1/2) = π/6。

**步骤 3**：k = -1/2 < 0，解在第三和第四象限。

第三象限：x = π + α = π + π/6 = 7π/6

第四象限：x = 2π - α = 2π - π/6 = 11π/6

**步骤 4**：验证。sin(7π/6) = -sin(π/6) = -1/2 ✓，sin(11π/6) = -sin(π/6) = -1/2 ✓

**答案**：x = 7π/6 和 x = 11π/6

---

**例题 3（sin x = k，通解形式）**：求方程 sin x = √2/2 的通解。

**解**：

**步骤 1**：参考角 α = arcsin(√2/2) = π/4。

**步骤 2**：k > 0，基本解为：

x₁ = π/4， x₂ = π - π/4 = 3π/4

**步骤 3**：通解为基本解加上 2π 的整数倍：

x = π/4 + 2nπ 或 x = 3π/4 + 2nπ， n ∈ Z

**答案**：x = π/4 + 2nπ 或 x = 3π/4 + 2nπ（n ∈ Z）

---

**例题 4（sin x = k，k = 0 特殊情况）**：在 0 ≤ x < 2π 范围内解方程 sin x = 0。

**解**：

**方法一（单位圆法）**：在单位圆上，sin x = 0 意味着 y = 0，即终边在 x 轴上。在 [0, 2π) 内，x = 0 和 x = π。

**方法二（参考角法）**：k = 0，参考角 α = 0。

- 在 x 轴正半轴（可视为第一和第四象限的交界）：x = 0
- 在 x 轴负半轴（可视为第二和第三象限的交界）：x = π

**答案**：x = 0 和 x = π

---

**例题 5（sin x = k，k = ±1 特殊情况）**：在 0 ≤ x < 2π 范围内解方程 sin x = -1。

**解**：

在单位圆上，sin x = -1 意味着 y = -1，即终边与负 y 轴重合。

在 [0, 2π) 内，只有 x = 3π/2 满足条件。

**验证**：sin(3π/2) = -1 ✓

**答案**：x = 3π/2

---

**例题 6（sin x = k，非特殊角）**：在 0 ≤ x < 2π 范围内解方程 sin x = 0.4，结果保留三位有效数字。

**解**：

**步骤 1**：0.4 ≤ 1，有解。

**步骤 2**：求参考角。使用计算器（弧度模式）：

α = arcsin(0.4) ≈ 0.4115 弧度

**步骤 3**：k = 0.4 > 0，解在第一和第二象限。

第一象限：x₁ = α ≈ 0.412

第二象限：x₂ = π - α ≈ 3.1416 - 0.4115 = 2.7301 ≈ 2.73

**答案**：x ≈ 0.412 和 x ≈ 2.73（三位有效数字）

---

### 8.5.3 基本形式 cos x = k（-1 ≤ k ≤ 1）

#### 几何推导——从单位圆理解

在单位圆上，cos θ = x 表示终边与单位圆交点的横坐标。方程 cos x = k 等价于：**在单位圆上，寻找终边与竖直线 x = k 相交的所有角度 x**。

**情形一**：当 0 < k < 1 时。

竖直线 x = k 与单位圆相交于两个点（对称于 x 轴）：
- 一个在第一象限，对应的角为 α（锐角）
- 另一个在第四象限，对应的角为 2π - α（或 -α）

**推导 2π - α**：角 2π - α 的终边与角 α 的终边关于 x 轴对称：

cos(2π - α) = cos α = |k|

由于 cos 在第四象限为正，cos(2π - α) = |k| = k。

**情形二**：当 -1 < k < 0 时。

竖直线 x = k（位于 y 轴左侧）与单位圆相交于两点：
- 一个在第二象限，对应的角为 π - α
- 另一个在第三象限，对应的角为 π + α

**推导 π - α**：角 π - α 的终边与角 α 的终边关于 y 轴对称：

cos(π - α) = -cos α = -|k|

由于 k < 0，-|k| = k，所以 cos(π - α) = k。

**推导 π + α**：角 π + α 的终边与角 α 的终边关于原点对称：

cos(π + α) = -cos α = -|k| = k

#### 完整的解法步骤

**步骤 1**：检查可行性。确认 |k| ≤ 1。

**步骤 2**：求参考角。

α = arccos(|k|)， α ∈ [0, π]

注意：arccos 的值域是 [0, π]，这与 arcsin 不同。因此 α 直接取 arccos(|k|)，它一定在 [0, π] 内。

**步骤 3**：根据 k 的符号确定解所在的象限。

| k 的符号 | 解所在的象限 | 对应的角 |
|-----------|-------------|---------|
| k > 0 | 第一、第四象限 | x = α, x = 2π - α |
| k = 0 | y 轴正负方向 | x = π/2, x = 3π/2（在 [0, 2π) 内） |
| k < 0 | 第二、第三象限 | x = π - α, x = π + α |

**步骤 4**：写出通解。由于 cos 的周期为 2π，一个简洁的通解形式为：

x = ±α + 2nπ， n ∈ Z

其中：
- 取 + 号时对应第一象限（或第二象限，取决于 k 的符号）
- 取 - 号时对应第四象限（或第三象限）

#### 特殊情况

**(a) k = 0**：cos x = 0 的解。

在 [0, 2π) 内，cos x = 0 发生在 x = π/2 和 x = 3π/2。通解为：

x = π/2 + nπ， n ∈ Z

**(b) k = 1**：cos x = 1 的解。

在 [0, 2π) 内，cos x = 1 只在 x = 0 处成立。通解为：

x = 2nπ， n ∈ Z

**(c) k = -1**：cos x = -1 的解。

在 [0, 2π) 内，cos x = -1 只在 x = π 处成立。通解为：

x = π + 2nπ = (2n + 1)π， n ∈ Z

#### 对比 sin 和 cos 的解分布

| | sin x = k | cos x = k |
|--|-----------|-----------|
| k > 0 | 第一、二象限：α, π - α | 第一、四象限：α, 2π - α |
| k < 0 | 第三、四象限：π + α, 2π - α | 第二、三象限：π - α, π + α |
| 周期 | 2π | 2π |
| 通解简洁形式 | x = nπ + (-1)ⁿ α | x = ±α + 2nπ |

> **记忆技巧**：sin 的正解在“上”（第一、二象限），cos 的正解在“右”（第一、四象限）。这个“上”和“右”对应了单位圆上 y 和 x 坐标为正的区域。

#### 例题

---

**例题 1（cos x = k，k > 0 标准情形）**：在 0 ≤ x < 2π 范围内解方程 cos x = √2/2。

**解**：

**步骤 1**：确认可行性。√2/2 ≤ 1，有解。

**步骤 2**：求参考角。α = arccos(√2/2) = π/4。

**步骤 3**：k = √2/2 > 0，解在第一和第四象限。

第一象限：x = α = π/4

第四象限：x = 2π - α = 2π - π/4 = 7π/4

**步骤 4**：验证。cos(π/4) = √2/2 ✓，cos(7π/4) = cos(π/4) = √2/2 ✓

**答案**：x = π/4 和 x = 7π/4

---

**例题 2（cos x = k，k < 0 标准情形）**：在 0 ≤ x < 2π 范围内解方程 cos x = -1/2。

**解**：

**步骤 1**：|-1/2| = 1/2 ≤ 1，有解。

**步骤 2**：求参考角。α = arccos(1/2) = π/3。

**步骤 3**：k = -1/2 < 0，解在第二和第三象限。

第二象限：x = π - α = π - π/3 = 2π/3

第三象限：x = π + α = π + π/3 = 4π/3

**步骤 4**：验证。cos(2π/3) = -cos(π/3) = -1/2 ✓，cos(4π/3) = -cos(π/3) = -1/2 ✓

**答案**：x = 2π/3 和 x = 4π/3

---

**例题 3（cos x = k，通解形式）**：求方程 cos x = √3/2 的通解。

**解**：

**步骤 1**：参考角 α = arccos(√3/2) = π/6。

**步骤 2**：k > 0，基本解为：

x₁ = π/6， x₂ = 2π - π/6 = 11π/6

**步骤 3**：通解为：

x = ±π/6 + 2nπ， n ∈ Z

其中 x = π/6 + 2nπ 对应第一象限的解，x = -π/6 + 2nπ 对应第四象限的解。

**答案**：x = ±π/6 + 2nπ（n ∈ Z）

---

**例题 4（cos x = k，k = 0 特殊情况）**：在 0 ≤ x < 2π 范围内解方程 cos x = 0。

**解**：

**方法一（单位圆法）**：cos x = 0 意味着 x = 0，即终边在 y 轴上。在 [0, 2π) 内，x = π/2 和 x = 3π/2。

**方法二（参考角法）**：α = arccos(0) = π/2。

由于 k = 0，解在第二象限和第三象限之间（即 y 轴正方向和负方向）：

x = π/2 和 x = π + π/2 = 3π/2

或者直接用通解：x = π/2 + nπ，在 [0, 2π) 内取 n = 0, 1。

**答案**：x = π/2 和 x = 3π/2

---

**例题 5（cos x = k，k = -1 特殊情况）**：在 0 ≤ x < 2π 范围内解方程 cos x = -1。

**解**：

在单位圆上，cos x = -1 意味着 x = -1，即终边与负 x 轴重合。

在 [0, 2π) 内，只有 x = π 满足条件。

**验证**：cos π = -1 ✓

**答案**：x = π

---

**例题 6（cos x = k，非特殊角）**：在 0 ≤ x < 2π 范围内解方程 cos x = 0.6，结果保留三位有效数字。

**解**：

**步骤 1**：0.6 ≤ 1，有解。

**步骤 2**：求参考角。使用计算器（弧度模式）：

α = arccos(0.6) ≈ 0.9273 弧度

**步骤 3**：k = 0.6 > 0，解在第一和第四象限。

第一象限：x₁ = α ≈ 0.927

第四象限：x₂ = 2π - α ≈ 6.2832 - 0.9273 = 5.3559 ≈ 5.36

**答案**：x ≈ 0.927 和 x ≈ 5.36（三位有效数字）

---

**例题 7（cos 和 sin 的对比）**：比较方程 sin x = √3/2 和 cos x = √3/2 在 [0, 2π) 内的解。

**解**：

√3/2 ≈ 0.866，参考角 α = π/6（因为 sin(π/6) = 1/2……等等，sin(π/3) = √3/2，cos(π/6) = √3/2）。

所以对 sin x = √3/2：α = π/3

对 cos x = √3/2：α = π/6

| 方程 | 参考角 α | 解（[0, 2π)） |
|-----|---------|------------------|
| sin x = √3/2 | π/3 | π/3, 2π/3 |
| cos x = √3/2 | π/6 | π/6, 11π/6 |

**启示**：sin 和 cos 的解分布模式不同，需要注意区分。

---

### 8.5.4 基本形式 tan x = k（k ∈ R）

#### 与 sin 和 cos 的本质区别

正切函数 tan x = sin x / cos x 有三个重要特性，使得解 tan x = k 的方式与 sin 和 cos 不同：

1. **值域为全体实数**：k 可以取任意实数值，没有 -1 到 1 的限制
2. **周期为 π（而不是 2π）**：tan(x + π) = tan x，因此每隔 π 重复一次
3. **有垂直渐近线**：在 x = π/2 + nπ 处 tan x 无定义

#### 几何推导——从单位圆理解

在单位圆上，tan θ = y/x = sin θ / cos θ。从几何角度看，tan θ 也可以看作是**过点 (1, 0) 的竖直线与终边延长线的交点**的纵坐标。

方程 tan x = k 意味着寻找终边使得 y/x = k，即 y = kx。这等价于寻找终边与直线 y = kx 重合（或反向重合）的所有角度。

**关键观察**：如果 tan α = k（α 为锐角），那么：
- 在第一象限，x = α 满足条件
- 在第三象限，x = π + α 也满足条件，因为 y/x 的比值相同
- 更一般地，x = α + nπ 全部满足条件

这正是 tan 周期为 π 的几何体现。

#### 完整的解法步骤

**步骤 1**：求参考角。

α = arctan(|k|)， α ∈ (0, π/2)

**步骤 2**：确定主值（principal value）。

如果不需要分象限讨论，可以直接使用计算器求出 arctan(k) 的主值（在 -π/2 到 π/2 之间），然后加上 π 的整数倍。

**步骤 3**：写出通解。

x = arctan(k) + nπ， n ∈ Z

或者，如果使用参考角 α 和象限法：
- k > 0：第一象限 x = α，第三象限 x = π + α，通解 x = α + nπ
- k < 0：第二象限 x = π - α，第四象限 x = 2π - α，通解 x = -α + nπ（或 x = π - α + nπ）

**简化提示**：直接使用 x = arctan(k) + nπ 是最简洁的方法，不需要分象限讨论。

#### 定义域检查

tan x 在 x = π/2 + nπ 处无定义。如果解恰好等于这些值（理论上不会，因为 tan 在这些点趋向无穷大），需要排除。

#### 特殊情况

**(a) k = 0**：tan x = 0 的解。

tan x = 0 发生在 sin x = 0 且 cos x ≠ 0 时，即 x = nπ。

在 [0, 2π) 内：x = 0，x = π。

**(b) k 不存在（tan x 无定义）**：当 x = π/2 + nπ 时，tan x 无定义，cos x = 0。这种情况不包含在 tan x = k 的解中。

#### 例题

---

**例题 1（tan x = k，k > 0 标准情形）**：在 0 ≤ x < 2π 范围内解方程 tan x = √3。

**解**：

**方法一（参考角法）**：

**步骤 1**：α = arctan(√3) = π/3。

**步骤 2**：k = √3 > 0，通解为 x = π/3 + nπ。

**步骤 3**：在 [0, 2π) 内，取 n = 0, 1：

x = π/3， x = π/3 + π = 4π/3

**方法二（直接主值法）**：

arctan(√3) = π/3，通解 x = π/3 + nπ，在 [0, 2π) 内取 n = 0, 1。

**步骤 4**：验证。tan(π/3) = √3 ✓，tan(4π/3) = tan(π/3) = √3 ✓

**答案**：x = π/3 和 x = 4π/3

---

**例题 2（tan x = k，k < 0 标准情形）**：在 0 ≤ x < 2π 范围内解方程 tan x = -1。

**解**：

**方法一（参考角法）**：

**步骤 1**：α = arctan(1) = π/4。

**步骤 2**：k = -1 < 0，解在第二和第四象限。

第二象限：x = π - α = π - π/4 = 3π/4

第四象限：x = 2π - α = 2π - π/4 = 7π/4

通解：x = 3π/4 + nπ 或 x = -π/4 + nπ。

**方法二（直接主值法）**：

arctan(-1) = -π/4，通解 x = -π/4 + nπ。

在 [0, 2π) 内，取 n = 1, 2：

x = -π/4 + π = 3π/4， x = -π/4 + 2π = 7π/4

**步骤 3**：验证。tan(3π/4) = -1 ✓，tan(7π/4) = -1 ✓

**答案**：x = 3π/4 和 x = 7π/4

---

**例题 3（tan x = k，k = 0 特殊情况）**：在 0 ≤ x < 2π 范围内解方程 tan x = 0。

**解**：

**方法一**：tan x = 0 意味着 sin x = 0 且 cos x ≠ 0。

sin x = 0 在 [0, 2π) 内的解为 x = 0 和 x = π。

检查 cos x：cos 0 = 1 ≠ 0 ✓，cos π = -1 ≠ 0 ✓

**方法二**：arctan(0) = 0，通解 x = 0 + nπ = nπ。

在 [0, 2π) 内：x = 0，x = π。

**答案**：x = 0 和 x = π

---

**例题 4（tan x = k，确认解不包括渐近线）**：在 0 ≤ x < 2π 范围内解方程 tan x = 2，结果保留三位有效数字。

**解**：

**步骤 1**：求主值。使用计算器（弧度模式）：

arctan(2) ≈ 1.1071 弧度

**步骤 2**：通解 x = 1.1071 + nπ。

在 [0, 2π) 内：

| n | x | 是否在 [0, 2π) |
|---|-----|-------------------|
| 0 | 1.1071 | ✓ |
| 1 | 1.1071 + π ≈ 4.2487 | ✓ |
| 2 | 1.1071 + 2π ≈ 7.3903 | ✗（≥ 2π） |

**步骤 3**：检查定义域。tan x 的渐近线在 x = π/2 ≈ 1.5708 和 x = 3π/2 ≈ 4.7124。两个解 1.1071 和 4.2487 均不在渐近线上。

**答案**：x ≈ 1.11 和 x ≈ 4.25（三位有效数字）

---

**例题 5（tan x = k，非特殊角负值）**：在 0 ≤ x < 2π 范围内解方程 tan x = -0.5，结果保留三位有效数字。

**解**：

**步骤 1**：求主值。

arctan(-0.5) ≈ -0.4636 弧度

**步骤 2**：通解 x = -0.4636 + nπ。

在 [0, 2π) 内：

| n | x | 是否在 [0, 2π) |
|---|-----|-------------------|
| 1 | -0.4636 + π ≈ 2.6780 | ✓ |
| 2 | -0.4636 + 2π ≈ 5.8196 | ✓ |
| 0 | -0.4636 | ✗ |
| 3 | -0.4636 + 3π ≈ 8.9612 | ✗ |

**步骤 3**：检查渐近线。x = 2.6780 和 x = 5.8196 均不在 π/2 ≈ 1.5708 或 3π/2 ≈ 4.7124 附近。

**答案**：x ≈ 2.68 和 x ≈ 5.82（三位有效数字）

---

**例题 6（三种基本形式的对比总结）**：在 0 ≤ x < 2π 范围内，分别解以下三个方程，并对比解的数量和分布：
(a) sin x = 1/2
(b) cos x = 1/2
(c) tan x = 1/2

**解**：

**(a) sin x = 1/2**

参考角 α = arcsin(1/2) = π/6。

k > 0，第一、二象限：x = π/6，x = π - π/6 = 5π/6

**2 个解**。

**(b) cos x = 1/2**

参考角 α = arccos(1/2) = π/3。

k > 0，第一、四象限：x = π/3，x = 2π - π/3 = 5π/3

**2 个解**。

**(c) tan x = 1/2**

arctan(1/2) ≈ 0.4636，通解 x = 0.4636 + nπ。

在 [0, 2π) 内：n = 0 得 0.4636，n = 1 得 0.4636 + π ≈ 3.6052。

**2 个解**。

**对比总结**：

| 方程 | 参考角 | 解（弧度） | 解的数量 |
|------|-------|-----------|---------|
| sin x = 1/2 | π/6 | π/6, 5π/6 | 2 |
| cos x = 1/2 | π/3 | π/3, 5π/3 | 2 |
| tan x = 1/2 | 0.4636 | 0.4636, 3.6052 | 2 |

在 [0, 2π) 内，三种基本形式均有 2 个解（除非 k = ±1 或 k = 0 等特殊情况）。

---

### 8.5.5 含 sec、csc、cot 的基本方程

sec x、csc x、cot x 分别是 cos x、sin x、tan x 的倒数。解这类方程时，通常先取倒数转化为基本形式，但需要额外注意**定义域**。

#### 转化方法

| 方程形式 | 转化步骤 | 注意 |
|---------|---------|------|
| sec x = k | cos x = 1/k | k ≠ 0；cos x ≠ 0 |
| csc x = k | sin x = 1/k | k ≠ 0；sin x ≠ 0 |
| cot x = k | tan x = 1/k | k ≠ 0；sin x ≠ 0 |

#### 例题

---

**例题 1（sec x = k）**：在 0 ≤ x < 2π 范围内解方程 sec x = 2。

**解**：

**步骤 1**：转化为 cos x。sec x = 1 / cos x = 2，所以 cos x = 1/2。

**步骤 2**：解 cos x = 1/2。

参考角 α = arccos(1/2) = π/3。

k > 0，第一和第四象限：

x = π/3， x = 2π - π/3 = 5π/3

**步骤 3**：检查定义域。sec x 在 cos x = 0 处无定义。两个解均使 cos x = 1/2 ≠ 0，有效。

**答案**：x = π/3 和 x = 5π/3

---

**例题 2（csc x = k）**：在 0 ≤ x < 2π 范围内解方程 csc x = -2。

**解**：

**步骤 1**：csc x = 1 / sin x = -2，所以 sin x = -1/2。

**步骤 2**：解 sin x = -1/2。

参考角 α = arcsin(1/2) = π/6。

k < 0，第三和第四象限：

x = π + π/6 = 7π/6， x = 2π - π/6 = 11π/6

**步骤 3**：检查定义域。csc x 在 sin x = 0 处无定义。两个解均使 sin x = -1/2 ≠ 0，有效。

**答案**：x = 7π/6 和 x = 11π/6

---

**例题 3（cot x = k）**：在 0 ≤ x < 2π 范围内解方程 cot x = √3。

**解**：

**步骤 1**：cot x = 1 / tan x = √3，所以 tan x = 1/√3 = √3/3。

**步骤 2**：解 tan x = √3/3。

arctan(√3/3) = π/6，通解 x = π/6 + nπ。

在 [0, 2π) 内：

x = π/6， x = π/6 + π = 7π/6

**步骤 3**：检查定义域。cot x 在 sin x = 0 处无定义。两个解均使 sin x ≠ 0，有效。

**答案**：x = π/6 和 x = 7π/6

---

**例题 4（csc x = k，k = 1 特殊情况）**：在 0 ≤ x < 2π 范围内解方程 csc x = 1。

**解**：

**步骤 1**：csc x = 1 / sin x = 1，所以 sin x = 1。

**步骤 2**：解 sin x = 1。在 [0, 2π) 内，x = π/2。

**步骤 3**：检查定义域。csc x 在 sin x = 0 处无定义。x = π/2 使 sin x = 1 ≠ 0，有效。

**答案**：x = π/2

---

### 8.5.6 运用恒等式的方程（考纲重点）

当方程中包含不同名的三角函数或高次项时，需要先用恒等式统一函数名称或降低次数。这是考纲中明确要求的重点内容。

#### 常见转化策略大全

| 方程特征 | 转化方法 | 示例 |
|---------|---------|------|
| 含 tan 和 sec | 用 sec² = 1 + tan² 化为单一变量 | 2 sec² x + tan x - 3 = 0 |
| 含 cot 和 csc | 用 csc² = 1 + cot² 化为单一变量 | 3 csc² x - 2 cot² x = 4 |
| 含 cot 和 tan | 用 cot = 1/tan 相互转化 | 4 cot θ = tan θ |
| a sin(kθ) + b cos(kθ) = 0 | 两边除以 cos(kθ) 得 tan(kθ) = -b/a | 5 sin 3θ + 2 cos 3θ = 0 |
| 含 sin² 和 cos² | 用 sin² + cos² = 1 消去一个变量 | sin² x + cos x = 1 |
| 含 sin(2θ) 或 cos(2θ) | 用二倍角公式展开或降次 | cos 2θ + sin θ = 0 |
| 含 csc²(θ/2) 等复合角 | 换元 u = θ/2 | 3 csc²(θ/2) = 4 |

#### 详细推导与例题

---

**类型一：cot 与 tan 互化**

**例题 1（考纲举例）**：在 0 ≤ θ < 2π 范围内解方程 4 cot θ = tan θ。

**分析**：方程两边含有 cot 和 tan，它们是倒数关系。我们可以用 cot θ = 1/tan θ 将它们统一为 tan。

**解**：

**步骤 1**：代入 cot θ = 1/tan θ。

4 × (1 / tan θ) = tan θ

**步骤 2**：两边乘以 tan θ（注意：tan θ ≠ 0，否则左边无定义）。

4 = tan² θ

**步骤 3**：两边开平方。

tan θ = ±2

**步骤 4**：分别解两个方程。

**子情形一**：tan θ = 2。

α₁ = arctan(2) ≈ 1.1071。

通解 θ = 1.1071 + nπ。

在 [0, 2π) 内：n = 0 得 1.1071，n = 1 得 1.1071 + π ≈ 4.2487。

**子情形二**：tan θ = -2。

α₂ = arctan(-2) ≈ -1.1071。

通解 θ = -1.1071 + nπ。

在 [0, 2π) 内：n = 1 得 -1.1071 + π ≈ 2.0344，n = 2 得 -1.1071 + 2π ≈ 5.1760。

**步骤 5**：检查定义域。原方程中 cot θ 要求 sin θ ≠ 0（即 θ ≠ nπ），tan θ 要求 cos θ ≠ 0（即 θ ≠ π/2 + nπ）。

四个解均不在此列，全部有效。

**答案**：θ ∈ {1.1071, 2.0344, 4.2487, 5.1760}

---

**类型二：利用 sec² = 1 + tan²**

**例题 2（考纲举例）**：在 0 ≤ x < 2π 范围内解方程 2 sec² x + tan x - 3 = 0。

**分析**：方程同时包含 sec² 和 tan。利用恒等式 sec² x = 1 + tan² x，可以将方程转化为关于 tan x 的二次方程。

**解**：

**步骤 1**：代入 sec² x = 1 + tan² x。

2(1 + tan² x) + tan x - 3 = 0

**步骤 2**：展开整理。

2 + 2 tan² x + tan x - 3 = 0

2 tan² x + tan x - 1 = 0

**步骤 3**：令 u = tan x，解二次方程 2u² + u - 1 = 0。

因式分解：(2u - 1)(u + 1) = 0

u = 1/2 或 u = -1

即 tan x = 1/2 或 tan x = -1。

**步骤 4**：解 tan x = 1/2。

α₁ = arctan(1/2) ≈ 0.4636。

通解 x = 0.4636 + nπ。

在 [0, 2π) 内：n = 0 得 0.4636，n = 1 得 0.4636 + π ≈ 3.6052。

**步骤 5**：解 tan x = -1。

arctan(-1) = -π/4。

通解 x = -π/4 + nπ。

在 [0, 2π) 内：n = 1 得 -π/4 + π = 3π/4，n = 2 得 -π/4 + 2π = 7π/4。

**步骤 6**：检查定义域。sec x 在 cos x = 0（x = π/2 + nπ）处无定义。

四个解均不在此列，全部有效。

**答案**：x ∈ {0.4636, 3.6052, 3π/4, 7π/4}

---

**类型三：a sin(kθ) + b cos(kθ) = 0 型**

**例题 3（考纲举例）**：在 0 ≤ θ < 2π 范围内解方程 5 sin 3θ + 2 cos 3θ = 0。

**分析**：方程同时包含 sin 3θ 和 cos 3θ，且两项次数相同。两边除以 cos 3θ 可化为 tan 形式。但需要注意 cos 3θ = 0 的情况需要单独检查。

**解**：

**步骤 1**：移项。

5 sin 3θ = -2 cos 3θ

**步骤 2**：两边除以 cos 3θ（先假设 cos 3θ ≠ 0）。

5 tan 3θ = -2

tan 3θ = -2/5

**步骤 3**：解 tan 3θ = -2/5。

α = arctan(-2/5) ≈ -0.3805。

通解：3θ = -0.3805 + nπ，即 θ = -0.3805/3 + nπ/3 ≈ -0.1268 + nπ/3。

**步骤 4**：在 [0, 2π) 内取适当的 n 值。

| n | θ = -0.1268 + nπ/3 | 是否 ∈ [0, 2π) |
|---|---------------------|---------------------|
| 1 | -0.1268 + π/3 ≈ 0.9204 | ✓ |
| 2 | -0.1268 + 2π/3 ≈ 1.9676 | ✓ |
| 3 | -0.1268 + π ≈ 3.0148 | ✓ |
| 4 | -0.1268 + 4π/3 ≈ 4.0620 | ✓ |
| 5 | -0.1268 + 5π/3 ≈ 5.1092 | ✓ |
| 6 | -0.1268 + 2π ≈ 6.1564 | ✓ |
| 0 | -0.1268 | ✗（负） |
| 7 | -0.1268 + 7π/3 ≈ 7.2036 | ✗（≥ 2π） |

共 6 个解。

**步骤 5**：检查 cos 3θ = 0 的情况。

当 cos 3θ = 0 时，3θ = π/2 + nπ，即 θ = π/6 + nπ/3。

代入原方程左端：5 sin 3θ + 2 cos 3θ = 5 sin(π/2 + nπ) + 2 × 0 = 5(±1) = ±5 ≠ 0。

因此 cos 3θ = 0 的解不是原方程的解，无需额外添加。

**答案**：θ ∈ {0.9204, 1.9676, 3.0148, 4.0620, 5.1092, 6.1564}

---

**类型四：含 csc² 和复合角的方程**

**例题 4（考纲举例）**：在 0 ≤ θ < 2π 范围内解方程 3 csc²(θ/2) = 4。

**分析**：方程含 csc²（sin 的倒数的平方）和复合角 θ/2。需要先处理 csc，再处理复合角。

**解**：

**步骤 1**：用 csc = 1/sin 转化。

3 × (1 / sin²(θ/2)) = 4

**步骤 2**：整理。

sin²(θ/2) = 3/4

**步骤 3**：开平方，注意正负号。

sin(θ/2) = ±√3/2

**步骤 4**：先处理复合角。令 u = θ/2。

由于 θ ∈ [0, 2π)，u ∈ [0, π)。

**子情形一**：sin u = √3/2。

参考角 α = arcsin(√3/2) = π/3。

k > 0，解在第一和第二象限：

在 [0, π) 内：u = π/3，u = π - π/3 = 2π/3

注意第二象限的解 2π/3 在 [0, π) 内，有效。

**子情形二**：sin u = -√3/2。

k < 0，解在第三和第四象限。但 u ∈ [0, π) 只覆盖第一、二象限，所以在 [0, π) 内无解。

**步骤 5**：由 u = θ/2 得 θ = 2u。

θ = 2 × π/3 = 2π/3， θ = 2 × 2π/3 = 4π/3

**步骤 6**：检查定义域。csc(θ/2) 在 sin(θ/2) = 0 处无定义。两个解均使 sin(θ/2) = ±√3/2 ≠ 0，有效。

**答案**：θ = 2π/3 和 θ = 4π/3

---

**类型五：含 csc² 和 cot² 的方程**

**例题 5**：在 0 ≤ x < 2π 范围内解方程 csc² x - 2 cot² x = 1。

**分析**：方程含 csc² 和 cot²，可以用恒等式 csc² x = 1 + cot² x 统一变量。

**解**：

**步骤 1**：代入 csc² x = 1 + cot² x。

(1 + cot² x) - 2 cot² x = 1

**步骤 2**：化简。

1 + cot² x - 2 cot² x = 1

1 - cot² x = 1

-cot² x = 0

cot x = 0

**步骤 3**：cot x = 0 意味着 cos x = 0（且 sin x ≠ 0）。

cos x = 0 在 [0, 2π) 内的解为 x = π/2 和 x = 3π/2。

**步骤 4**：检查定义域。cot x 在 sin x = 0 处无定义。两个解均使 sin x = ±1 ≠ 0，有效。

**答案**：x = π/2 和 x = 3π/2

---

**类型六：含 sin² 和 cos 的方程（利用 sin² + cos² = 1）**

**例题 6**：在 0 ≤ x < 2π 范围内解方程 2 sin² x + 3 cos x = 0。

**分析**：方程同时含 sin² 和 cos。利用 sin² x = 1 - cos² x 可以将方程化为关于 cos x 的二次方程。

**解**：

**步骤 1**：代入 sin² x = 1 - cos² x。

2(1 - cos² x) + 3 cos x = 0

**步骤 2**：展开整理。

2 - 2 cos² x + 3 cos x = 0

-2 cos² x + 3 cos x + 2 = 0

两边乘以 -1：

2 cos² x - 3 cos x - 2 = 0

**步骤 3**：令 u = cos x，解二次方程 2u² - 3u - 2 = 0。

因式分解：(2u + 1)(u - 2) = 0

u = -1/2 或 u = 2

u = 2 超出 cos 的值域 [-1, 1]，舍去。

**步骤 4**：解 cos x = -1/2。

参考角 α = arccos(1/2) = π/3。

k < 0，解在第二和第三象限：

x = π - π/3 = 2π/3， x = π + π/3 = 4π/3

**答案**：x = 2π/3 和 x = 4π/3

---

**类型七：含 sin 和 sin² 的二次方程**

**例题 7**：在 0 ≤ x < 2π 范围内解方程 2 sin² x - sin x - 1 = 0。

**解**：

**步骤 1**：令 u = sin x，得二次方程 2u² - u - 1 = 0。

因式分解：(2u + 1)(u - 1) = 0

u = -1/2 或 u = 1

**步骤 2**：解 sin x = 1。

在 [0, 2π) 内：x = π/2。

**步骤 3**：解 sin x = -1/2。

参考角 α = arcsin(1/2) = π/6。

k < 0，第三和第四象限：

x = π + π/6 = 7π/6， x = 2π - π/6 = 11π/6

**答案**：x ∈ {π/2, 7π/6, 11π/6}

---

**类型八：含 cos(2θ) 的方程（用二倍角公式展开）**

**例题 8**：在 0 ≤ θ < 2π 范围内解方程 cos 2θ + sin θ = 0。

**分析**：方程含 cos 2θ 和 sin θ，角度不同。用二倍角公式 cos 2θ = 1 - 2 sin²θ 将 cos 2θ 展开为 sin θ 的表达式。

**解**：

**步骤 1**：代入 cos 2θ = 1 - 2 sin²θ。

(1 - 2 sin²θ) + sin θ = 0

**步骤 2**：整理为关于 sin θ 的二次方程。

-2 sin²θ + sin θ + 1 = 0

两边乘以 -1：

2 sin²θ - sin θ - 1 = 0

**步骤 3**：令 u = sin θ，解 2u² - u - 1 = 0。

因式分解：(2u + 1)(u - 1) = 0

u = -1/2 或 u = 1

**步骤 4**：解 sin θ = 1。

θ = π/2

**步骤 5**：解 sin θ = -1/2。

θ = π + π/6 = 7π/6， θ = 2π - π/6 = 11π/6

**答案**：θ ∈ {π/2, 7π/6, 11π/6}

---

**类型九：利用 cos 2θ 降次**

**例题 9**：在 0 ≤ x < 2π 范围内解方程 cos² x = 3/4。

**解法一（直接开方）**：

cos x = ±√3/2

解 cos x = √3/2：x = π/6，x = 11π/6

解 cos x = -√3/2：x = 5π/6，x = 7π/6

共 4 个解。

**解法二（用 cos 2θ 降次）**：

由 cos² x = (1 + cos 2x)/2：

(1 + cos 2x)/2 = 3/4

1 + cos 2x = 3/2

cos 2x = 1/2

令 u = 2x，u ∈ [0, 4π)。

解 cos u = 1/2，参考角 α = π/3。

k > 0，第一和第四象限。

在 [0, 2π) 内：u = π/3，u = 2π - π/3 = 5π/3

在 [2π, 4π) 内：u = π/3 + 2π = 7π/3，u = 5π/3 + 2π = 11π/3

由 x = u/2 得：

x = π/6，5π/6，7π/6，11π/6

两种方法结果一致。

**答案**：x ∈ {π/6, 5π/6, 7π/6, 11π/6}

---

**类型十：综合运用多种恒等式**

**例题 10**：在 0 ≤ x < 2π 范围内解方程 sec x + tan x = 1。

**分析**：方程同时含 sec x 和 tan x。将它们统一为 sin 和 cos，然后通过代数变换求解。

**解**：

**步骤 1**：将 sec x 和 tan x 用 sin 和 cos 表示。

1/cos x + sin x / cos x = 1

**步骤 2**：合并左边。

(1 + sin x) / cos x = 1

**步骤 3**：两边乘以 cos x（注意 cos x ≠ 0）。

1 + sin x = cos x

**步骤 4**：移项。1 + sin x - cos x = 0。这不太容易直接处理，我们换一种方法。

由 1 + sin x = cos x，两边平方：

(1 + sin x)² = cos² x

**步骤 5**：用 cos² x = 1 - sin² x 代入。

1 + 2 sin x + sin² x = 1 - sin² x

2 sin x + sin² x = - sin² x

2 sin x + 2 sin² x = 0

2 sin x (1 + sin x) = 0

**步骤 6**：sin x = 0 或 sin x = -1。

**步骤 7**：检查各候选解。

sin x = 0 在 [0, 2π) 内的解：x = 0，x = π。

代入原方程验证：
- x = 0：sec 0 + tan 0 = 1 + 0 = 1 ✓
- x = π：sec π + tan π = -1 + 0 = -1 ≠ 1 ✗（平方引入了增根）

sin x = -1 在 [0, 2π) 内的解：x = 3π/2。

代入原方程验证：
- x = 3π/2：sec(3π/2) 无定义（cos(3π/2) = 0）✗

**步骤 8**：唯一有效解为 x = 0。

**答案**：x = 0

---

> ⚠️ **重要提醒**：本题展示了平方可能引入增根，因此**平方后必须验根**。同时也展示了检查定义域的重要性。

---

### 8.5.7 解三角方程——常见错误与防范

| 错误类型 | 错误示例 | 正确做法 |
|---------|---------|---------|
| 忽略周期性 | 解 sin x = 1/2 只得到 π/6 | 正确定出两个解 π/6 和 5π/6 |
| 忽略换元后的周期加倍 | 解 cos 2x = 1/2 只找到 2 个解 | 2x 在 [0, 4π) 内，应有 4 个解 |
| 平方后不验根 | 解 sin x + cos x = 1 直接平方得到增根 | 平方后的解必须代入原方程验证 |
| 除以可能为零的表达式 | 解 5 sin 3θ + 2 cos 3θ = 0 忘记检查 cos 3θ = 0 | 先假设 cos 3θ ≠ 0，再单独验证 |
| 忽略定义域 | 解 sec x = 2 不检查 cos x ≠ 0 | 确保解不在 π/2 + nπ 处 |
| sin 和 cos 的解分布混淆 | 用 sin 的模式解 cos 方程 | sin k > 0 在一、二象限；cos k > 0 在一、四象限 |
| 忘记 tan 周期为 π | 解 tan x = 1 只得到 π/4 | tan 周期 π，通解为 π/4 + nπ |

---

### 8.5.8 解三角方程——方法总结流程图

```
                    ┌─────────────────────────────┐
                    │      给定的三角方程          │
                    └─────────────┬───────────────┘
                                  │
                    ┌─────────────▼───────────────┐
                    │ 方程是否包含不同名的函数？    │
                    └────────┬──────────┬─────────┘
                         是 │          │ 否
                   ┌────────▼──┐  ┌────▼─────┐
                   │ 用恒等式  │  │ 已为基本 │
                   │ 统一变量  │  │ 单一形式 │
                   └────────┬──┘  └────┬─────┘
                            │          │
                   ┌────────▼──────────▼───────┐
                   │ 化为基本形式              │
                   │ sin x = k / cos x = k     │
                   │ / tan x = k + 其他        │
                   └────────┬──────────────────┘
                            │
               ┌────────────▼────────────┐
               │ 选择解法                │
               └────────┬───────────────┘
                        │
         ┌──────────────┼──────────────┐
         ▼              ▼              ▼
   ┌─────────┐   ┌──────────┐   ┌──────────┐
   │ sin x=k │   │ cos x=k  │   │ tan x=k  │
   │ 参考角  │   │ 参考角   │   │ arctan(k)│
   │ α=arcsin│   │ α=arccos │   │ + nπ    │
   │ 分象限  │   │ 分象限   │   │          │
   └────┬────┘   └────┬─────┘   └────┬─────┘
        │             │              │
        └─────────────┼──────────────┘
                      ▼
          ┌──────────────────────┐
          │ 写出给定区间内的所有解 │
          └──────────┬───────────┘
                     ▼
          ┌──────────────────────┐
          │ 检查定义域，排除无效解 │
          └──────────────────────┘
```

**常用转化策略**：

| 方程特征 | 转化方法 |
|---------|---------|
| 含 sec、csc、cot | 转化为 sin、cos：sec = 1/cos 等 |
| 含 tan 和 sec | 用 sec² = 1 + tan² 化为单一变量 |
| 含 cot 和 csc | 用 csc² = 1 + cot² 化为单一变量 |
| 含 sin 和 cos 的二次式 | 用 sin² + cos² = 1 化为单一变量 |
| 含 a sin(kθ) + b cos(kθ) = 0 | 两边除以 cos(kθ) 得 tan(kθ) = -b/a |
| 含 sin(2θ) 或 cos(2θ) | 用二倍角公式展开或降次 |

### 8.5.6 注意事项

1. **定义域**：排除函数无定义的点。例如 tan x 在 x = π/2 + nπ 处无定义，sec x 同样。
2. **平方增根**：如果方程两边平方，可能引入增根，需要验根。
3. **两边乘以表达式**：如果乘以可能为零的表达式，可能会丢失解或引入增根。
4. **周期性**：注意在给定区间内，每个周期都会产生新的解。

### 8.5.7 例题

---

**例题 1（基本正弦方程——k > 0）**：在 0 ≤ x < 2π 范围内解方程 sin x = √3/2。

**解**：

**步骤 1**：求参考角。α = arcsin(√3/2) = π/3。

**步骤 2**：k = √3/2 > 0，解在第一和第二象限。

**步骤 3**：写出解。

第一象限：x = α = π/3

第二象限：x = π - α = π - π/3 = 2π/3

**答案**：x = π/3 和 x = 2π/3

---

**例题 2（基本正弦方程——k < 0）**：在 0 ≤ x < 2π 范围内解方程 sin x = -1/2。

**解**：

**步骤 1**：求参考角。α = arcsin(1/2) = π/6。

**步骤 2**：k = -1/2 < 0，解在第三和第四象限。

**步骤 3**：写出解。

第三象限：x = π + α = π + π/6 = 7π/6

第四象限：x = 2π - α = 2π - π/6 = 11π/6

**答案**：x = 7π/6 和 x = 11π/6

---

**例题 3（基本余弦方程）**：在 0 ≤ x < 2π 范围内解方程 cos x = -√2/2。

**解**：

**步骤 1**：求参考角。α = arccos(√2/2) = π/4。

**步骤 2**：k = -√2/2 < 0，解在第二和第三象限。

**步骤 3**：写出解。

第二象限：x = π - α = π - π/4 = 3π/4

第三象限：x = π + α = π + π/4 = 5π/4

**答案**：x = 3π/4 和 x = 5π/4

---

**例题 4（基本正切方程）**：在 0 ≤ x < 2π 范围内解方程 tan x = √3。

**解**：

**步骤 1**：求参考角。α = arctan(√3) = π/3。

**步骤 2**：tan 的周期为 π，通解为 x = π/3 + nπ。

**步骤 3**：在 [0, 2π) 内取 n = 0, 1：

x = π/3， x = π/3 + π = 4π/3

**答案**：x = π/3 和 x = 4π/3

---

**例题 5（含 cot 的方程——转化为 tan）**：在 0 ≤ x < 2π 范围内解方程 4 cot x = tan x。

**解**：

**步骤 1**：将 cot x = 1/tan x 代入。

4 / tan x = tan x

**步骤 2**：两边乘以 tan x（注意 tan x ≠ 0）。

4 = tan² x

**步骤 3**：所以 tan x = ±2。

**步骤 4**：求参考角。α = arctan(2)（非特殊角，保留小数）。

使用计算器：α ≈ 1.1071 弧度。

**步骤 5**：tan x = 2（正）：解在第一和第三象限。

x = α ≈ 1.1071， x = π + α ≈ 4.2487

**步骤 6**：tan x = -2（负）：解在第二和第四象限。

x = π - α ≈ 2.0344， x = 2π - α ≈ 5.1760

**步骤 7**：检查定义域。tan x ≠ 0，所有解均满足。

**答案**：x ∈ {1.1071, 2.0344, 4.2487, 5.1760}

---

**例题 6（利用 sec² = 1 + tan² 化为一元二次方程）**：在 0 ≤ x < 2π 范围内解方程 2 sec² x + tan x - 3 = 0。

**解**：

**步骤 1**：用恒等式 sec² x = 1 + tan² x 代入。

2(1 + tan² x) + tan x - 3 = 0

**步骤 2**：展开整理。

2 + 2 tan² x + tan x - 3 = 0

2 tan² x + tan x - 1 = 0

**步骤 3**：令 u = tan x，解二次方程。

2u² + u - 1 = 0

因式分解：(2u - 1)(u + 1) = 0

u = 1/2 或 u = -1

**步骤 4**：解 tan x = 1/2。

α₁ = arctan(1/2) ≈ 0.4636。

tan x > 0，解在第一和第三象限：

x₁ ≈ 0.4636， x₂ ≈ π + 0.4636 = 3.6052

**步骤 5**：解 tan x = -1。

α₂ = arctan(1) = π/4。

tan x < 0，解在第二和第四象限：

x₃ = π - π/4 = 3π/4， x₄ = 2π - π/4 = 7π/4

**步骤 6**：检查定义域。sec x 在 x = π/2 + nπ 处无定义。检查各解：

- 0.4636：cos(0.4636) ≠ 0 ✓
- 3.6052：cos(3.6052) ≠ 0 ✓
- 3π/4：cos(3π/4) ≠ 0 ✓
- 7π/4：cos(7π/4) ≠ 0 ✓

全部有效。

**答案**：x ∈ {0.4636, 3.6052, 3π/4, 7π/4}

---

**例题 7（a sin(kθ) + b cos(kθ) = 0 型）**：在 0 ≤ θ < 2π 范围内解方程 5 sin(3θ) + 2 cos(3θ) = 0。

**解**：

**步骤 1**：将含有 cos 的项移到右边。

5 sin(3θ) = -2 cos(3θ)

**步骤 2**：两边除以 cos(3θ)（注意 cos(3θ) ≠ 0 的情况需单独检查）。

5 tan(3θ) = -2

tan(3θ) = -2/5

**步骤 3**：求参考角。α = arctan(2/5) ≈ 0.3805。

**步骤 4**：tan(3θ) = -0.4（负），通解为 3θ = nπ - α（或 3θ = π n - α）。

更规范地：tan u = -0.4 的通解为 u = arctan(-0.4) + nπ = -α + nπ。

3θ = -α + nπ

θ = -α/3 + nπ/3

**步骤 5**：在 [0, 2π) 内取适当的 n 值。

α/3 ≈ 0.1268。

| n | θ = -α/3 + nπ/3 | 是否在 [0, 2π) |
|---|-----------------|-------------------|
| 1 | -α/3 + π/3 ≈ 1.0472 - 0.1268 ≈ 0.9204 | ✓ |
| 2 | -α/3 + 2π/3 ≈ 2.0944 - 0.1268 ≈ 1.9676 | ✓ |
| 3 | -α/3 + π ≈ 3.1416 - 0.1268 ≈ 3.0148 | ✓ |
| 4 | -α/3 + 4π/3 ≈ 4.1888 - 0.1268 ≈ 4.0620 | ✓ |
| 5 | -α/3 + 5π/3 ≈ 5.2360 - 0.1268 ≈ 5.1092 | ✓ |
| 6 | -α/3 + 2π ≈ 6.2832 - 0.1268 ≈ 6.1564 | ✓（< 2π） |
| 0 | -α/3 ≈ -0.1268 | ✗ |
| 7 | -α/3 + 7π/3 ≈ 7.3304 - 0.1268 ≈ 7.2036 | ✗（≥ 2π） |

**步骤 6**：检查 cos(3θ) = 0 的情况。

当 cos(3θ) = 0 时，3θ = π/2 + nπ，即 θ = π/6 + nπ/3。

代入原方程：5 sin(3θ) = 5 sin(π/2 + nπ) = 5(±1) ≠ 0，而 cos(3θ) = 0，所以 θ = π/6 + nπ/3 不是解。

**答案**：θ ∈ {0.9204, 1.9676, 3.0148, 4.0620, 5.1092, 6.1564}

---

**例题 8（含二次 sin 的方程）**：在 0 ≤ x < 2π 范围内解方程 2 sin² x - 3 sin x + 1 = 0。

**解**：

**步骤 1**：令 u = sin x，得二次方程。

2u² - 3u + 1 = 0

**步骤 2**：因式分解。

(2u - 1)(u - 1) = 0

**步骤 3**：u = 1/2 或 u = 1。

**情况 1**：sin x = 1。

x = π/2（在 [0, 2π) 内只有一个解，因为 sin x = 1 只在 x = π/2 处成立）。

**情况 2**：sin x = 1/2。

参考角 α = arcsin(1/2) = π/6。

k > 0，解在第一和第二象限：

x = π/6， x = π - π/6 = 5π/6

**答案**：x ∈ {π/6, π/2, 5π/6}

---

**例题 9（含 cos(2θ) 的方程——先换元再求解）**：在 0 ≤ θ < 2π 范围内解方程 cos(2θ) = 1/2。

**解**：

**步骤 1**：令 u = 2θ，则 u ∈ [0, 4π)。

解 cos u = 1/2。

**步骤 2**：参考角 α = arccos(1/2) = π/3。

k > 0，解在第一和第四象限：

在 [0, 2π) 内：u = π/3 和 u = 2π - π/3 = 5π/3

**步骤 3**：由于周期为 2π，在 [2π, 4π) 内还有两个解：

u = π/3 + 2π = 7π/3 和 u = 5π/3 + 2π = 11π/3

**步骤 4**：由 θ = u/2 得四个解：

θ = π/6， θ = 5π/6， θ = 7π/6， θ = 11π/6

**答案**：θ ∈ {π/6, 5π/6, 7π/6, 11π/6}

---

**例题 10（含 csc² 的方程）**：在 0 ≤ x < 2π 范围内解方程 3 csc² x - 4 = 0。

**解**：

**步骤 1**：整理方程。

3 csc² x = 4 ⇒ csc² x = 4/3

**步骤 2**：因为 csc x = 1/sin x，所以：

1 / sin² x = 4/3 ⇒ sin² x = 3/4

**步骤 3**：因此 sin x = ±√3/2。

**情况 1**：sin x = √3/2。

参考角 α = arcsin(√3/2) = π/3。

k > 0，解在第一和第二象限：

x = π/3， x = π - π/3 = 2π/3

**情况 2**：sin x = -√3/2。

参考角 α = π/3。

k < 0，解在第三和第四象限：

x = π + π/3 = 4π/3， x = 2π - π/3 = 5π/3

**步骤 4**：检查定义域。csc x 在 sin x = 0 处无定义。四个解均使 sin x ≠ 0，全部有效。

**答案**：x ∈ {π/3, 2π/3, 4π/3, 5π/3}

---

> ⚠️ **易错提醒**：
> 1. **忘记周期性**：在 [0, 2π) 内，sin 和 cos 最多有 2 个解，但经过换元（如 2θ）后，解的个数会增加
> 2. **忽略定义域**：tan、sec、csc、cot 在某些点无定义，这些点必须从解集中排除
> 3. **两边除以变量**：如例题 7 中除以 cos(3θ) 时，需要单独检查 cos(3θ) = 0 的情况
> 4. **符号错误**：使用 ASTC 法则时注意每个象限的符号

---

## 8.6 三角恒等式的证明

### 8.6.1 证明策略总览

证明三角恒等式没有固定的算法，但以下策略通常有效：

| 策略 | 适用场景 | 操作 |
|------|---------|------|
| **策略 1：从复杂端入手** | 两边不对称 | 选择项数更多、结构更复杂的一边进行化简 |
| **策略 2：统一化为 sin 和 cos** | 含 tan、sec、csc、cot | 用基本关系替换：tan = sin/cos，sec = 1/cos 等 |
| **策略 3：通分合并** | 分式加减 | 找到公分母，合并分子 |
| **策略 4：利用 sin² + cos² = 1** | 出现 1 或平方项 | 用恒等式替换或合并 |
| **策略 5：因式分解** | 分子分母可分解 | 提取公因式、平方差公式 |
| **策略 6：分子分母同乘共轭式** | 分母含 1 ± sin θ 或 1 ± cos θ | 乘以 1 ∓ sin θ 或 1 ∓ cos θ |
| **策略 7：利用二倍角公式** | 角度不一致 | 将 2θ 展开或降次 |

### 8.6.2 证明的书写规范

在书写证明过程时，应遵循以下规范：

1. 明确写出从哪一边开始（“左边 =” 或 “右边 =”）
2. 每一步变换都基于已知恒等式或代数运算
3. 最终得到与另一边完全相同的形式
4. 以“■”或“得证”结束

### 8.6.3 详细证明示例

---

**例题 1（策略：化为 sin 和 cos）**：证明 tan x + cot x = sec x csc x。

**证明**：

从左边开始：

tan x + cot x = sin x / cos x + cos x / sin x

通分，公分母为 sin x cos x：

= (sin² x + cos² x) / (sin x cos x)

由 sin² x + cos² x = 1：

= 1 / (sin x cos x)

再看右边：

sec x csc x = (1 / cos x) · (1 / sin x) = 1 / (sin x cos x)

左边 = 右边，恒等式得证。■

---

**例题 2（策略：通分合并）**：证明 sin θ / (1 + cos θ) + (1 + cos θ) / sin θ = 2 csc θ。

**证明**：

从左边开始，通分：

sin θ / (1 + cos θ) + (1 + cos θ) / sin θ
= [sin² θ + (1 + cos θ)²] / [sin θ (1 + cos θ)]

展开分子：

sin² θ + 1 + 2 cos θ + cos² θ

利用 sin² θ + cos² θ = 1 合并：

= (sin² θ + cos² θ) + 1 + 2 cos θ = 1 + 1 + 2 cos θ = 2 + 2 cos θ

提取公因式 2(1 + cos θ)：

= 2(1 + cos θ) / [sin θ (1 + cos θ)]

约去 1 + cos θ（注意 1 + cos θ ≠ 0）：

= 2 / sin θ = 2 csc θ

左边 = 右边，恒等式得证。■

---

**例题 3（策略：分子分母同乘共轭式）**：证明 (1 - sin θ) / cos θ = cos θ / (1 + sin θ)。

**证明**：

从左边开始，分子分母同乘以 1 + sin θ：

(1 - sin θ) / cos θ = [(1 - sin θ)(1 + sin θ)] / [cos θ (1 + sin θ)]

分子展开得 1 - sin² θ = cos² θ：

= cos² θ / [cos θ (1 + sin θ)]

约去 cos θ（假设 cos θ ≠ 0）：

= cos θ / (1 + sin θ)

左边 = 右边，恒等式得证。■

**另一种证法**（从右边开始）：

cos θ / (1 + sin θ) = cos θ (1 - sin θ) / [(1 + sin θ)(1 - sin θ)] = cos θ (1 - sin θ) / (1 - sin² θ)

= cos θ (1 - sin θ) / cos² θ = (1 - sin θ) / cos θ

同样得证。■

---

**例题 4（策略：利用 sec² = 1 + tan²）**：证明 sec² θ + csc² θ = sec² θ csc² θ。

**证明**：

从左边开始，将 sec 和 csc 转化为 sin 和 cos：

sec² θ + csc² θ = 1 / cos² θ + 1 / sin² θ

通分，公分母为 sin² θ cos² θ：

= (sin² θ + cos² θ) / (sin² θ cos² θ)

利用 sin² θ + cos² θ = 1：

= 1 / (sin² θ cos² θ)

再看右边：

sec² θ csc² θ = (1 / cos² θ) · (1 / sin² θ) = 1 / (sin² θ cos² θ)

左边 = 右边，恒等式得证。■

---

**例题 5（策略：因式分解 + 恒等式）**：证明 cos⁴ θ - sin⁴ θ = cos(2θ)。

**证明**：

从左边开始，利用平方差公式：

cos⁴ θ - sin⁴ θ = (cos² θ)² - (sin² θ)²

= (cos² θ - sin² θ)(cos² θ + sin² θ)

由 cos² θ + sin² θ = 1：

= (cos² θ - sin² θ) × 1 = cos² θ - sin² θ

由二倍角公式 cos(2θ) = cos² θ - sin² θ：

= cos(2θ)

左边 = 右边，恒等式得证。■

---

**例题 6（策略：利用 csc² = 1 + cot²）**：证明 (1 + tan² θ) / (1 + cot² θ) = tan² θ。

**证明**：

从左边开始，分子由 sec² θ = 1 + tan² θ，分母由 csc² θ = 1 + cot² θ：

(1 + tan² θ) / (1 + cot² θ) = sec² θ / csc² θ

将 sec 和 csc 转化为 sin 和 cos：

= (1/cos² θ) / (1/sin² θ) = sin² θ / cos² θ = tan² θ

左边 = 右边，恒等式得证。■

---

**例题 7（策略：二倍角公式）**：证明 sin(2θ) / (1 - cos(2θ)) = cot θ。

**证明**：

从左边开始，代入二倍角公式 sin(2θ) = 2 sin θ cos θ，cos(2θ) = 1 - 2 sin² θ：

sin(2θ) / (1 - cos(2θ)) = 2 sin θ cos θ / [1 - (1 - 2 sin² θ)]

化简分母：

= 2 sin θ cos θ / (2 sin² θ)

约去 2 sin θ（假设 sin θ ≠ 0）：

= cos θ / sin θ = cot θ

左边 = 右边，恒等式得证。■

---

**例题 8（综合策略）**：证明 sin x tan x + cos x = sec x。

> 这是考纲中明确列出的例题类型。

**证明**：

从左边开始，将 tan x 化为 sin x / cos x：

sin x tan x + cos x = sin x · (sin x / cos x) + cos x

= sin² x / cos x + cos x

将 cos x 写为 cos² x / cos x，通分：

= (sin² x + cos² x) / cos x

由 sin² x + cos² x = 1：

= 1 / cos x = sec x

左边 = 右边，恒等式得证。■

---

**例题 9（综合策略——含分式）**：证明 cos θ / (1 - tan θ) + sin θ / (1 - cot θ) = sin θ + cos θ。

**证明**：

从左边开始。先将 tan θ = sin θ / cos θ 和 cot θ = cos θ / sin θ 代入：

第一项：

cos θ / (1 - sin θ / cos θ) = cos θ / [(cos θ - sin θ) / cos θ] = cos θ · cos θ / (cos θ - sin θ) = cos² θ / (cos θ - sin θ)

第二项：

sin θ / (1 - cos θ / sin θ) = sin θ / [(sin θ - cos θ) / sin θ] = sin θ · sin θ / (sin θ - cos θ) = sin² θ / (sin θ - cos θ)

注意第二项的分母 sin θ - cos θ = -(cos θ - sin θ)。

因此左边为：

cos² θ / (cos θ - sin θ) + sin² θ / [-(cos θ - sin θ)]

= (cos² θ - sin² θ) / (cos θ - sin θ)

利用平方差公式：

= (cos θ - sin θ)(cos θ + sin θ) / (cos θ - sin θ)

约去 cos θ - sin θ（假设 cos θ ≠ sin θ）：

= cos θ + sin θ

左边 = 右边，恒等式得证。■

---

**例题 10（考纲举例题——第二种形式）**：证明 cos θ / (1 + sin θ) + (1 + sin θ) / cos θ = 2 sec θ。

**证明**：

从左边开始，通分：

cos θ / (1 + sin θ) + (1 + sin θ) / cos θ
= [cos² θ + (1 + sin θ)²] / [cos θ (1 + sin θ)]

展开分子：

cos² θ + 1 + 2 sin θ + sin² θ

利用 cos² θ + sin² θ = 1：

= (cos² θ + sin² θ) + 1 + 2 sin θ = 1 + 1 + 2 sin θ = 2 + 2 sin θ

提取公因式 2(1 + sin θ)：

= 2(1 + sin θ) / [cos θ (1 + sin θ)] = 2 / cos θ = 2 sec θ

左边 = 右边，恒等式得证。■

---

> **证明总结**：三角恒等式的证明本质上是一个“化简-转化”的过程。最重要的是熟悉三个基本恒等式和代数运算技巧，从较复杂的一边开始，逐步向另一边靠拢。如果一种方法行不通，试试从另一边开始，或者换一种转化策略。

---

## 本章知识结构总览

```
第8章：三角学（含弧度法）
│
├── 8.1 弧度制
│   ├── 定义：1 弧度 = 弧长等于半径时的圆心角
│   ├── 换算：180° = π 弧度
│   ├── 弧长公式：s = rθ（θ 必须为弧度）
│   ├── 扇形面积：A = ½ r²θ
│   └── 弓形面积：A = ½ r²(θ - sin θ)
│
├── 8.2 六个三角函数（任意角）
│   ├── 单位圆定义：sin θ = y, cos θ = x, tan θ = y/x
│   ├── sec θ = 1/cos θ, csc θ = 1/sin θ, cot θ = 1/tan θ
│   ├── 特殊角的值（0, π/6, π/4, π/3, π/2 等）
│   ├── ASTC 符号法则
│   └── 参考角法：求任意角三角函数值
│
├── 8.3 三角函数的图像
│   ├── y = sin x（周期 2π，值域 [-1,1]，奇函数）
│   ├── y = cos x（周期 2π，值域 [-1,1]，偶函数）
│   ├── y = tan x（周期 π，渐近线 x = π/2 + nπ）
│   ├── y = sec x, csc x, cot x 的图像
│   └── 变换：y = a sin(bx + c) + d 的参数分析
│
├── 8.4 三角恒等式
│   ├── sin²θ + cos²θ = 1
│   ├── sec²θ = 1 + tan²θ
│   ├── csc²θ = 1 + cot²θ
│   ├── 二倍角公式（推导及应用）
│   └── 半角公式（降次用）
│
├── 8.5 解三角方程
│   ├── 基本形式：sin x = k, cos x = k, tan x = k
│   ├── 利用恒等式转化（化为同名函数）
│   ├── 二次型方程（换元法）
│   ├── a sin(kθ) + b cos(kθ) = 0 型
│   └── 含复合角（如 cos(2θ) = k）的方程
│
└── 8.6 三角恒等式的证明
    ├── 策略 1：化为 sin 和 cos
    ├── 策略 2：通分合并
    ├── 策略 3：分子分母同乘共轭式
    ├── 策略 4：利用基本恒等式
    ├── 策略 5：因式分解
    └── 策略 6：利用二倍角公式
```

--- 
---

# 第 9 章：几何（直线与圆）

## 大纲对照

本章覆盖 Cambridge IGCSE Additional Mathematics 0606（2028–2030 考纲）以下内容：

| 考纲主题 | 本节对应 |
|----------|----------|
| **7. Straight-line graphs** – 直线方程、平行/垂直、中点、长度、垂直平分线 | 9.1 |
| **7.4** – 非线性关系线性化（y = Ax^n, y = Ab^x） | 9.2 |
| **8. Coordinate geometry of the circle** – 圆的方程、圆心与半径 | 9.3 |
| **8.2** – 直线与圆的相交（割线、切线、不相交） | 9.4 |
| **8.3** – 圆的切线（不使用微积分） | 9.4 |
| **8.4** – 两圆相交、相切、不相交、公共弦 | 9.5 |

---

## 引言

解析几何的核心思想是：**用代数方程描述几何图形**。一条直线或一个圆可以用一个坐标方程完全表示；两个图形之间的位置关系——是否相交、是否相切、距离是多少——都可以通过代数运算精确判断，而不需要尺规作图。

本章从最基本的直线方程开始，逐步建立完整的解析几何工具集：直线的方程形式与几何性质、圆的两种方程形式、直线与圆的位置关系（特别是切线的三种求法），以及两圆相交时的公共弦。此外，9.2 节介绍一种在科学实验中极其实用的技巧——**非线性关系的线性化**，它将幂函数和指数函数转化为直线形式以便分析。

每个小节都包含公式的完整推导和真题风格的例题。所有例题均采用 **Statement | Reason** 格式：每一步都先给出结论性陈述，再说明理由。

---

## 9.1 直线方程

### 9.1.1 斜率——直线的方向

**定义**：给定两点 A(x1, y1) 和 B(x2, y2)，直线 AB 的斜率 m 是纵坐标差与横坐标差的比值：

    m = (y2 - y1) / (x2 - x1)      (x1 ≠ x2)

**推导**：斜率衡量直线相对于水平轴的倾斜程度。设直线与 x 轴正方向的夹角为 θ（0° ≤ θ < 180°），则 m = tanθ。当 θ = 90° 时，直线竖直，tan 90° 未定义，因此竖直线没有斜率。

**几何含义**：
- m > 0：直线向右上方倾斜（θ 为锐角）。
- m < 0：直线向右下方倾斜（θ 为钝角）。
- m = 0：直线水平（θ = 0°）。
- m 未定义：直线竖直（θ = 90°）。

---

### 9.1.2 直线方程的三种形式

**形式 1：点斜式**

已知直线上一点 (x1, y1) 和斜率 m。设 (x, y) 为直线上任意一点。该点与已知点连线的斜率必须等于 m：

    (y - y1) / (x - x1) = m

两边乘以 (x - x1)，得到点斜式：

    y - y1 = m(x - x1)

**形式 2：斜截式**

在点斜式中，取已知点为直线与 y 轴的交点 (0, c)（c 称为 y 截距），代入得：

    y - c = m(x - 0)   ⇒   y = mx + c

这是最常用的直线方程形式，m 是斜率，c 是 y 截距。

**形式 3：一般式**

将直线方程的所有项移到等号一侧：

    Ax + By + C = 0

其中 A, B 不同时为零。当 B ≠ 0 时，可解出斜率：

    y = -(A/B)x - (C/B)   ⇒   m = -A/B

一般式的优势：它统一包含所有直线，包括竖直线（此时 B = 0，方程为 Ax + C = 0，即 x = -C/A）。

---

**示例 1**：一条直线经过点 (3, -2)，斜率为 4。求它的方程。

| Statement | Reason |
|-----------|--------|
| The point is (3, -2) and the gradient is 4. | Given. |
| Using the point-slope form y - y1 = m(x - x1). | This is the appropriate formula when a point and the gradient are known. |
| y - (-2) = 4(x - 3). | Substituting x1 = 3, y1 = -2, m = 4. |
| y + 2 = 4x - 12. | Expanding the brackets. |
| y = 4x - 14. | Subtracting 2 from both sides. |

The equation of the line is y = 4x - 14, or 4x - y - 14 = 0 in general form.

---

**示例 2**：一条直线经过点 (-1, 5) 和 (2, -1)。求它的方程。

| Statement | Reason |
|-----------|--------|
| Let (x1, y1) = (-1, 5) and (x2, y2) = (2, -1). | Two points on the line are given. |
| m = (-1 - 5) / (2 - (-1)) = -6 / 3 = -2. | Gradient formula m = (y2 - y1) / (x2 - x1). |
| Using y - y1 = m(x - x1) with (-1, 5). | Point-slope form requires one point and the gradient. |
| y - 5 = -2(x + 1). | Substituting m = -2, x1 = -1, y1 = 5. |
| y - 5 = -2x - 2. | Expanding the bracket. |
| y = -2x + 3. | Adding 5 to both sides. |

The equation is y = -2x + 3, or 2x + y - 3 = 0.

---

**示例 3**：将直线 3x - 2y + 6 = 0 化为斜截式，并指出斜率和 y 截距。

| Statement | Reason |
|-----------|--------|
| 3x - 2y + 6 = 0. | Given general form. |
| -2y = -3x - 6. | Moving 3x and 6 to the right-hand side. |
| y = (3/2)x + 3. | Dividing both sides by -2. |
| m = 3/2 and c = 3. | In y = mx + c, m is the gradient and c is the y-intercept. |

The gradient is 3/2 and the y-intercept is 3.

---

### 9.1.3 平行与垂直的条件

**平行线**

两条直线平行的几何含义是它们的方向完全相同。因此它们的斜率相等：

    m1 = m2

当两条直线都是竖直线时，它们的斜率都未定义，它们也互相平行。

**垂直线**

两条直线互相垂直时，一条直线旋转 90° 后与另一条重合。

**推导**：设两条直线的斜率分别为 m1 = tanθ1 和 m2 = tanθ2。若两直线垂直，则 θ2 = θ1 + 90°（或相反）。利用恒等式 tan(θ + 90°) = -cotθ：

    m2 = tan(θ1 + 90°) = -cotθ1 = -1 / tanθ1 = -1 / m1

因此：

    m1 · m2 = -1

特殊情况：水平线（m = 0）与竖直线（斜率未定义）互相垂直，此时乘积条件不适用，但可通过几何直观判断。

---

**示例 1**：判断直线 L1: y = 3x + 2 和 L2: 6x - 2y + 5 = 0 是否平行。

| Statement | Reason |
|-----------|--------|
| L1 has gradient m1 = 3. | Equation is in slope-intercept form y = mx + c. |
| L2: 6x - 2y + 5 = 0 ⇒ -2y = -6x - 5 ⇒ y = 3x + 5/2. | Rearranging to slope-intercept form. |
| m2 = 3. | The coefficient of x is the gradient. |
| m1 = m2 = 3. | Both gradients are equal. |
| Therefore L1 ∥ L2. | Parallel lines have equal gradients. |

---

**示例 2**：一条直线经过点 (2, -3) 且垂直于直线 2x + y = 5。求它的方程。

| Statement | Reason |
|-----------|--------|
| 2x + y = 5 ⇒ y = -2x + 5. | Rearranging to slope-intercept form. |
| The given line has gradient m1 = -2. | In y = mx + c, the coefficient of x is the gradient. |
| Let the required gradient be m2. | The required line is perpendicular to the given line. |
| m1 · m2 = -1 ⇒ (-2) m2 = -1 ⇒ m2 = 1/2. | Perpendicular lines satisfy m1 m2 = -1. |
| The line passes through (2, -3) with m = 1/2. | Using point-slope form y - y1 = m(x - x1). |
| y - (-3) = (1/2)(x - 2). | Substituting x1 = 2, y1 = -3, m = 1/2. |
| y + 3 = (1/2)x - 1 ⇒ y = (1/2)x - 4. | Simplifying. |

The equation is y = (1/2)x - 4, or x - 2y - 8 = 0.

---

**示例 3**：已知 A(1, 4)、B(3, 0)、C(5, 2)。判断三角形 ABC 是否为直角三角形。

| Statement | Reason |
|-----------|--------|
| m_AB = (0 - 4) / (3 - 1) = -4 / 2 = -2. | Gradient formula between A and B. |
| m_BC = (2 - 0) / (5 - 3) = 2 / 2 = 1. | Gradient formula between B and C. |
| m_AC = (2 - 4) / (5 - 1) = -2 / 4 = -1/2. | Gradient formula between A and C. |
| m_AB · m_AC = (-2) × (-1/2) = 1 ≠ -1. | Checking if AB ⟂ AC. |
| m_AB · m_BC = (-2) × 1 = -2 ≠ -1. | Checking if AB ⟂ BC. |
| m_BC · m_AC = 1 × (-1/2) = -1/2 ≠ -1. | Checking if BC ⟂ AC. |
| No pair of gradients satisfies m1 m2 = -1. | Therefore no two sides are perpendicular. |
| Triangle ABC is **not** a right-angled triangle. | A right-angled triangle requires one pair of perpendicular sides. |

---

### 9.1.4 中点公式

给定两点 A(x1, y1) 和 B(x2, y2)，线段 AB 的中点 M 的坐标是两端坐标的算术平均：

    M( (x1 + x2)/2 , (y1 + y2)/2 )

**推导**：设 M 的坐标为 (xM, yM)。向量 AM = (1/2) AB，因此 (xM - x1, yM - y1) = (1/2)(x2 - x1, y2 - y1)。解得 xM = (x1 + x2)/2，yM = (y1 + y2)/2。

---

**示例 1**：求 A(-3, 7) 和 B(5, -1) 的中点。

| Statement | Reason |
|-----------|--------|
| xM = (-3 + 5)/2 = 2/2 = 1. | Midpoint formula for x-coordinate. |
| yM = (7 + (-1))/2 = 6/2 = 3. | Midpoint formula for y-coordinate. |
| M = (1, 3). | The midpoint of AB. |

---

**示例 2**：已知 P(2, 5) 是线段 QR 的中点，且 Q(-1, 3)。求 R 的坐标。

| Statement | Reason |
|-----------|--------|
| Let R = (x, y). | Unknown coordinates of the endpoint. |
| (-1 + x)/2 = 2. | Midpoint formula for x, equating to 2. |
| -1 + x = 4 ⇒ x = 5. | Multiplying both sides by 2. |
| (3 + y)/2 = 5. | Midpoint formula for y, equating to 5. |
| 3 + y = 10 ⇒ y = 7. | Multiplying both sides by 2. |
| R = (5, 7). | The coordinates of the other endpoint. |

---

**示例 3**：A(2, 3)、B(6, -1)、C(4, 5) 是平行四边形的三个顶点。若 A 和 C 是对角顶点，求第四个顶点 D。

| Statement | Reason |
|-----------|--------|
| In a parallelogram, diagonals bisect each other. | Property of a parallelogram. |
| The midpoint of diagonal AC equals the midpoint of diagonal BD. | Diagonals share the same midpoint. |
| Midpoint of AC: ((2 + 4)/2, (3 + 5)/2) = (3, 4). | Midpoint formula. |
| Let D = (x, y). Then midpoint of BD is ((6 + x)/2, (-1 + y)/2). | Midpoint formula for BD. |
| (6 + x)/2 = 3 ⇒ 6 + x = 6 ⇒ x = 0. | Equating x-coordinates of midpoints. |
| (-1 + y)/2 = 4 ⇒ -1 + y = 8 ⇒ y = 9. | Equating y-coordinates of midpoints. |
| D = (0, 9). | The fourth vertex of the parallelogram. |

---

### 9.1.5 两点之间的距离

给定两点 A(x1, y1) 和 B(x2, y2)，线段 AB 的长度由勾股定理给出：

    AB = √[ (x2 - x1)² + (y2 - y1)² ]

**推导**：过 A 和 B 分别作水平线和竖直线，构成直角三角形。水平直角边长为 |x2 - x1|，竖直直角边长为 |y2 - y1|。由勾股定理，斜边长（即 AB）为 √[(x2 - x1)² + (y2 - y1)²]。

---

**示例 1**：求 A(-2, 5) 和 B(4, -3) 之间的距离。

| Statement | Reason |
|-----------|--------|
| AB = √[ (4 - (-2))² + (-3 - 5)² ]. | Distance formula. |
| = √[ 6² + (-8)² ]. | Simplifying inside the brackets. |
| = √[36 + 64] = √100 = 10. | Evaluating squares and summing. |

---

**示例 2**：点 P 在 x 轴上，且到 A(1, 4) 的距离为 5。求 P 的坐标。

| Statement | Reason |
|-----------|--------|
| Let P = (p, 0). | Any point on the x-axis has y = 0. |
| PA = √[ (p - 1)² + (0 - 4)² ] = 5. | Distance from P to A is given as 5. |
| (p - 1)² + 16 = 25. | Squaring both sides. |
| (p - 1)² = 9. | Subtracting 16 from both sides. |
| p - 1 = 3 or p - 1 = -3. | Taking square root (two possibilities). |
| p = 4 or p = -2. | Solving for p. |
| P = (4, 0) or P = (-2, 0). | Two points satisfy the condition. |

---

**示例 3**：证明 A(1, 2)、B(4, 6)、C(7, 2) 是一个等腰三角形。

| Statement | Reason |
|-----------|--------|
| AB = √[ (4 - 1)² + (6 - 2)² ] = √[9 + 16] = 5. | Distance formula for AB. |
| BC = √[ (7 - 4)² + (2 - 6)² ] = √[9 + 16] = 5. | Distance formula for BC. |
| AC = √[ (7 - 1)² + (2 - 2)² ] = √[36 + 0] = 6. | Distance formula for AC. |
| AB = BC = 5, but AB ≠ AC and BC ≠ AC. | Two sides are equal, the third is different. |
| Triangle ABC is isosceles with AB = BC. | An isosceles triangle has at least two equal sides. |

---

### 9.1.6 点到直线的距离

点 P(x0, y0) 到直线 Ax + By + C = 0 的垂直距离为：

    d = |Ax0 + By0 + C| / √(A² + B²)

**推导**：直线 L: Ax + By + C = 0 的法向量为 (A, B)。过 P 作 L 的垂线，垂足 H 可表示为 H = (x0 + tA, y0 + tB)，其中 t 是实数。由于 H 在 L 上，代入方程：

    A(x0 + tA) + B(y0 + tB) + C = 0
    Ax0 + By0 + C + t(A² + B²) = 0
    t = -(Ax0 + By0 + C) / (A² + B²)

距离 d = PH = √[(tA)² + (tB)²] = |t| √(A² + B²) = |Ax0 + By0 + C| / √(A² + B²)。

---

**示例 1**：求点 (2, -3) 到直线 3x - 4y + 5 = 0 的距离。

| Statement | Reason |
|-----------|--------|
| A = 3, B = -4, C = 5, x0 = 2, y0 = -3. | Identifying coefficients and point coordinates. |
| d = |3(2) + (-4)(-3) + 5| / √(3² + (-4)²). | Substituting into the distance formula. |
| = |6 + 12 + 5| / √(9 + 16) = 23 / 5. | Evaluating numerator and denominator. |
| d = 23/5 = 4.6. | The perpendicular distance from the point to the line. |

---

**示例 2**：求两条平行线 2x + 3y - 6 = 0 和 2x + 3y + 12 = 0 之间的距离。

| Statement | Reason |
|-----------|--------|
| On L1: 2x + 3y - 6 = 0, take x = 0 ⇒ 3y = 6 ⇒ y = 2. | Choosing a convenient point on the first line. |
| Point P(0, 2) lies on L1. | Substituting gives 0 + 6 - 6 = 0, which is true. |
| Distance from P to L2: 2x + 3y + 12 = 0 is required. | Parallel lines have constant separation. |
| d = |2(0) + 3(2) + 12| / √(2² + 3²). | Distance formula with P and L2. |
| = |0 + 6 + 12| / √(4 + 9) = 18 / √13. | Simplifying. |
| The distance between the two parallel lines is 18/√13. | This is the perpendicular distance between them. |

---

**示例 3**：点 (k, 4) 到直线 5x - 12y + 3 = 0 的距离为 2。求 k 的所有可能值。

| Statement | Reason |
|-----------|--------|
| d = |5k - 12(4) + 3| / √(5² + (-12)²) = 2. | Distance formula, equated to 2. |
| |5k - 48 + 3| / 13 = 2 ⇒ |5k - 45| / 13 = 2. | Simplifying numerator and denominator. |
| |5k - 45| = 26. | Multiplying both sides by 13. |
| 5k - 45 = 26 or 5k - 45 = -26. | Definition of absolute value. |
| 5k = 71 or 5k = 19. | Adding 45 to both sides. |
| k = 71/5 or k = 19/5. | Dividing by 5. |

---

### 9.1.7 垂直平分线

一条线段的垂直平分线是同时满足两个条件的直线：
1. **垂直于**该线段。
2. **经过**该线段的中点。

**求法步骤**：
1. 求线段 AB 的中点 M。
2. 求 AB 的斜率 m_AB，则垂直平分线的斜率为 -1/m_AB（若 m_AB ≠ 0）。
3. 用点斜式写出经过 M、斜率为 -1/m_AB 的直线。

---

**示例 1**：求连接 A(1, 3) 和 B(5, -1) 的线段的垂直平分线方程。

| Statement | Reason |
|-----------|--------|
| M = ((1 + 5)/2, (3 + (-1))/2) = (3, 1). | Midpoint formula. |
| m_AB = (-1 - 3) / (5 - 1) = -4 / 4 = -1. | Gradient of AB. |
| Perpendicular gradient = -1 / (-1) = 1. | Perpendicular gradient is the negative reciprocal. |
| Line through (3, 1) with gradient 1: y - 1 = 1(x - 3). | Point-slope form. |
| y = x - 2. | Simplifying. |
| The perpendicular bisector is y = x - 2. | In general form: x - y - 2 = 0. |

---

**示例 2**：点 P(2, 5) 和 Q(8, 3)。求 PQ 的垂直平分线与坐标轴的交点。

| Statement | Reason |
|-----------|--------|
| M = ((2 + 8)/2, (5 + 3)/2) = (5, 4). | Midpoint of PQ. |
| m_PQ = (3 - 5) / (8 - 2) = -2 / 6 = -1/3. | Gradient of PQ. |
| Perpendicular gradient = 3. | Negative reciprocal of -1/3. |
| Equation: y - 4 = 3(x - 5). | Point-slope form with (5, 4) and m = 3. |
| y = 3x - 11. | Simplifying to slope-intercept form. |
| x-intercept: set y = 0 ⇒ 0 = 3x - 11 ⇒ x = 11/3. | The line crosses the x-axis where y = 0. |
| y-intercept: set x = 0 ⇒ y = -11. | The line crosses the y-axis where x = 0. |
| The perpendicular bisector meets the axes at (11/3, 0) and (0, -11). | These are the required intersection points. |

---

**示例 3**：A(0, 0)、B(6, 2)、C(4, 8) 是三角形的顶点。求边 AB 的垂直平分线方程，并证明它经过 AC 的中点。

| Statement | Reason |
|-----------|--------|
| M_AB = ((0 + 6)/2, (0 + 2)/2) = (3, 1). | Midpoint of AB. |
| m_AB = (2 - 0) / (6 - 0) = 1/3. | Gradient of AB. |
| Perpendicular gradient = -3. | Negative reciprocal of 1/3. |
| Equation: y - 1 = -3(x - 3). | Point-slope form. |
| y = -3x + 10. | Simplifying. |
| Midpoint of AC: ((0 + 4)/2, (0 + 8)/2) = (2, 4). | Midpoint formula for AC. |
| Does (2, 4) satisfy y = -3x + 10? | LHS: 4, RHS: -3(2) + 10 = 4. |
| 4 = 4, so the point lies on the line. | Therefore the perpendicular bisector of AB passes through the midpoint of AC. |

---

## 9.2 非线性关系线性化

在科学实验中，两个变量之间往往不是线性关系，而是幂函数关系 y = Ax^n 或指数函数关系 y = Ab^x。通过适当的变量代换，我们可以将这些非线性关系**转化为直线形式**，然后用线性回归（计算斜率和截距）确定未知参数。

### 9.2.1 幂函数 y = Ax^n

对 y = Ax^n 两边取自然对数：

    ln y = ln(Ax^n) = ln A + ln(x^n) = ln A + n ln x

令 Y = ln y，X = ln x，则：

    Y = n X + ln A

这是一个关于 X 和 Y 的直线方程，斜率 m = n，Y 截距 c = ln A。

**实际操作**：对每组实验数据 (x, y)，计算 (ln x, ln y)；以 ln x 为横坐标、ln y 为纵坐标作图；读出斜率（即 n）和 Y 截距（即 ln A），再取指数得到 A。

### 9.2.2 指数函数 y = Ab^x

对 y = Ab^x 两边取自然对数：

    ln y = ln(Ab^x) = ln A + ln(b^x) = ln A + x ln b

令 Y = ln y，X = x（注意这里 X 就是原来的 x，不需要变换），则：

    Y = (ln b) X + ln A

这是一个关于 X 和 Y 的直线方程，斜率 m = ln b，Y 截距 c = ln A。

**实际操作**：对每组 (x, y)，计算 (x, ln y)；以 x 为横坐标、ln y 为纵坐标作图；读出斜率（即 ln b，取指数得 b）和 Y 截距（即 ln A，取指数得 A）。

---

**示例 1**：变量 x 和 y 满足 y = Ax^n。实验数据经 (ln x, ln y) 变换后得到一条直线，其斜率为 2.5，ln y 截距为 1.2。求 A 和 n。

| Statement | Reason |
|-----------|--------|
| Y = nX + ln A, where Y = ln y and X = ln x. | Linearised form of y = Ax^n. |
| The graph of Y against X has slope 2.5 and Y-intercept 1.2. | Given experimental results. |
| n = 2.5. | The slope equals n in the linearised equation. |
| ln A = 1.2 ⇒ A = e^{1.2}. | The Y-intercept equals ln A. |
| The relationship is y = e^{1.2} x^{2.5}. | Substituting the values of A and n. |

---

**示例 2**：变量 x 和 y 满足 y = Ab^x。实验数据经 (x, ln y) 变换后得到直线，斜率为 0.75，ln y 截距为 2.3。求 A 和 b。

| Statement | Reason |
|-----------|--------|
| Y = (ln b) X + ln A, where Y = ln y and X = x. | Linearised form of y = Ab^x. |
| ln b = 0.75 ⇒ b = e^{0.75}. | The slope equals ln b. |
| ln A = 2.3 ⇒ A = e^{2.3}. | The Y-intercept equals ln A. |
| y = e^{2.3} · (e^{0.75})^x = e^{2.3 + 0.75x}. | The exponential relationship. |

---

**示例 3**：已知 y = 5x³。将它线性化，并说明若以 ln x 为横坐标、ln y 为纵坐标作图，斜率和截距各是多少。

| Statement | Reason |
|-----------|--------|
| ln y = ln(5x³) = ln 5 + 3 ln x. | Taking natural log of both sides. |
| Y = 3X + ln 5, where Y = ln y, X = ln x. | The linearised equation. |
| The slope is 3. | This equals the exponent n. |
| The Y-intercept is ln 5 ≈ 1.609. | This equals ln A. |

---

## 9.3 圆的方程

圆是平面上到定点（圆心）的距离等于定长（半径）的所有点的集合。这个定义直接给出了圆的标准方程。

### 9.3.1 标准式

设圆心为 C(a, b)，半径为 r。对于圆上任意一点 P(x, y)，由距离公式有 PC = r：

    √[ (x - a)² + (y - b)² ] = r

两边平方，得到标准式：

    (x - a)² + (y - b)² = r²

圆心在原点时，a = b = 0，方程为 x² + y² = r²。

### 9.3.2 一般式

将标准式展开：

    x² - 2ax + a² + y² - 2by + b² = r²

移项并合并常数项：

    x² + y² - 2ax - 2by + (a² + b² - r²) = 0

令 g = -a，f = -b，c = a² + b² - r²，得到一般式：

    x² + y² + 2gx + 2fy + c = 0

从一般式反推圆心和半径：

- 圆心：(-g, -f)
- 半径：r = √(g² + f² - c)

**存在条件**：g² + f² - c > 0 表示实圆；= 0 表示点圆；< 0 表示虚圆（无实图形）。

---

**示例 1**：写出圆心为 (-3, 4)、半径为 6 的圆的方程。

| Statement | Reason |
|-----------|--------|
| (x - (-3))² + (y - 4)² = 6². | Standard form (x - a)² + (y - b)² = r². |
| (x + 3)² + (y - 4)² = 36. | Simplifying. |
| x² + 6x + 9 + y² - 8y + 16 = 36. | Expanding the brackets. |
| x² + y² + 6x - 8y - 11 = 0. | Collecting terms and subtracting 36. |

---

**示例 2**：已知圆的方程为 x² + y² - 10x + 4y + 13 = 0。求圆心和半径。

| Statement | Reason |
|-----------|--------|
| 2g = -10 ⇒ g = -5. | Comparing with x² + y² + 2gx + 2fy + c = 0. |
| 2f = 4 ⇒ f = 2. | Coefficient of y. |
| c = 13. | Constant term. |
| Centre = (-g, -f) = (5, -2). | Centre formula. |
| r = √(g² + f² - c) = √((-5)² + 2² - 13). | Radius formula. |
| = √(25 + 4 - 13) = √16 = 4. | Evaluating. |
| Centre is (5, -2) and radius is 4. | Final answer. |

---

**示例 3**：通过配方法将 x² + y² + 6x - 2y - 6 = 0 化为标准式，并求圆心和半径。

| Statement | Reason |
|-----------|--------|
| (x² + 6x) + (y² - 2y) = 6. | Grouping x and y terms, moving constant to RHS. |
| (x² + 6x + 9) + (y² - 2y + 1) = 6 + 9 + 1. | Completing the square: add (6/2)² = 9 and (-2/2)² = 1 to both sides. |
| (x + 3)² + (y - 1)² = 16. | Factorising the perfect squares. |
| Centre = (-3, 1) and radius = √16 = 4. | Reading from standard form (x - a)² + (y - b)² = r². |

---

## 9.4 圆与直线

### 9.4.1 位置关系的判别

将直线方程代入圆的方程，得到关于 x（或 y）的二次方程。该二次方程的判别式 Δ 决定交点个数：

- Δ > 0：两个不同的实根 ⇒ 两个交点（直线是**割线**）
- Δ = 0：一个重根 ⇒ 一个交点（直线是**切线**）
- Δ < 0：无实根 ⇒ 无交点（直线与圆**相离**）

### 9.4.2 切线的三种求法

**情形 1：已知切点 (x1, y1) 在圆上**

对于圆 (x - a)² + (y - b)² = r²，在点 (x1, y1) 处的切线方程为：

    (x1 - a)(x - a) + (y1 - b)(y - b) = r²

**推导**：圆心 C(a, b) 到切点 P(x1, y1) 的向量为 (x1 - a, y1 - b)。切线与半径 CP 垂直。设 Q(x, y) 为切线上任意一点，则向量 PQ = (x - x1, y - y1) 与 CP 的点积为零：

    (x1 - a)(x - x1) + (y1 - b)(y - y1) = 0

整理为 (x1 - a)(x - a) + (y1 - b)(y - b) = (x1 - a)² + (y1 - b)² = r²。

对于圆心在原点的圆 x² + y² = r²，切线简化为：

    x1 x + y1 y = r²

---

**示例 1（已知切点）**：圆 x² + y² = 25，求在点 (3, -4) 处的切线方程。

| Statement | Reason |
|-----------|--------|
| Centre is (0, 0), r² = 25, point is (3, -4). | Identifying from x² + y² = r² form. |
| Tangent formula: x1 x + y1 y = r². | Formula for a circle centred at the origin. |
| 3x + (-4)y = 25 ⇒ 3x - 4y = 25. | Substituting x1 = 3, y1 = -4, r² = 25. |
| 3x - 4y - 25 = 0. | The equation of the tangent in general form. |

---

**示例 2（已知切点）**：圆 (x - 2)² + (y + 1)² = 16，求在点 (6, -1) 处的切线方程。

| Statement | Reason |
|-----------|--------|
| Centre (a, b) = (2, -1), r² = 16, point (x1, y1) = (6, -1). | Given in standard form. |
| Formula: (x1 - a)(x - a) + (y1 - b)(y - b) = r². | Tangent at a point on the circle. |
| (6 - 2)(x - 2) + (-1 + 1)(y + 1) = 16. | Substituting values. |
| 4(x - 2) + 0 · (y + 1) = 16. | Simplifying. |
| 4x - 8 = 16 ⇒ 4x = 24 ⇒ x = 6. | Solving. |
| The tangent is the vertical line x = 6. | This is consistent: (6, -1) is the rightmost point of the circle. |

---

**情形 2：已知斜率 m**

对于圆心 (a, b)、半径 r 的圆，斜率为 m 的切线方程为：

    y - b = m(x - a) ± r √(1 + m²)

**推导**：设切线为 y = mx + k。圆心到直线的距离等于半径：

    |ma - b + k| / √(m² + 1) = r

解得 k = b - ma ± r √(m² + 1)。代入 y = mx + k 即得。

当圆心在原点时，简化为 y = mx ± r √(1 + m²)。

---

**示例 3（已知斜率）**：求圆 x² + y² = 9 的斜率为 2 的切线方程。

| Statement | Reason |
|-----------|--------|
| Centre (0, 0), r = 3, m = 2. | Given. |
| y = mx ± r √(1 + m²) = 2x ± 3 √(1 + 4). | Formula for tangent with given slope, centre at origin. |
| y = 2x ± 3√5. | Simplifying. |
| The two tangents are y = 2x + 3√5 and y = 2x - 3√5. | The ± gives two parallel tangents, one above and one below. |

---

**情形 3：从圆外一点 (x0, y0) 引切线**

解法：
1. 设切线斜率为 m，方程 y - y0 = m(x - x0)。
2. 化为一般式 mx - y + (y0 - mx0) = 0。
3. 令圆心到该直线的距离等于半径，解出 m。
4. 检查竖直线 x = x0 是否也是切线。

---

**示例 4（圆外一点）**：圆 x² + y² = 5 和圆外点 P(4, 3)。求从 P 引出的切线方程。

| Statement | Reason |
|-----------|--------|
| Centre (0, 0), radius r = √5. | Given circle. |
| Let the tangent be y - 3 = m(x - 4). | Point-slope form through P(4, 3). |
| mx - y + (3 - 4m) = 0. | Rearranging to general form. |
| |m(0) - 0 + (3 - 4m)| / √(m² + 1) = √5. | Distance from centre (0,0) to line equals radius. |
| |3 - 4m| = √5 √(m² + 1). | Multiplying both sides. |
| (3 - 4m)² = 5(m² + 1). | Squaring both sides. |
| 9 - 24m + 16m² = 5m² + 5. | Expanding. |
| 11m² - 24m + 4 = 0. | Collecting like terms. |
| (11m - 2)(m - 2) = 0 ⇒ m = 2/11 or m = 2. | Factorising. |
| For m = 2: y - 3 = 2(x - 4) ⇒ y = 2x - 5. | First tangent. |
| For m = 2/11: y - 3 = (2/11)(x - 4) ⇒ 11y - 33 = 2x - 8 ⇒ 2x - 11y + 25 = 0. | Second tangent. |
| Check x = 4: distance from (0,0) to x = 4 is 4 ≠ √5. | Vertical line is not a tangent. |
| The two tangents are y = 2x - 5 and 2x - 11y + 25 = 0. | Final answer. |

---

### 9.4.3 综合判断与求值

**示例 5**：直线 y = x + k 与圆 x² + y² = 8 相切。求 k 的值。

| Statement | Reason |
|-----------|--------|
| Substitute y = x + k into x² + y² = 8. | Finding intersection points. |
| x² + (x + k)² = 8. | Substituting. |
| x² + x² + 2kx + k² = 8. | Expanding. |
| 2x² + 2kx + (k² - 8) = 0. | Collecting terms. |
| For tangency, Δ = 0. | A tangent touches at exactly one point. |
| Δ = (2k)² - 4(2)(k² - 8) = 4k² - 8k² + 64. | Discriminant of the quadratic. |
| Δ = -4k² + 64 = 0. | Setting discriminant to zero. |
| k² = 16 ⇒ k = ±4. | Solving for k. |
| The line y = x + 4 or y = x - 4 is tangent to the circle. | Two parallel tangents with slope 1. |

---

**示例 6**：判断直线 y = 2x - 1 与圆 (x - 1)² + (y + 2)² = 5 的位置关系。

| Statement | Reason |
|-----------|--------|
| Centre (1, -2), radius r = √5. | From standard form. |
| Substitute y = 2x - 1: (x - 1)² + (2x - 1 + 2)² = 5. | Substituting into circle equation. |
| (x - 1)² + (2x + 1)² = 5. | Simplifying inside brackets. |
| x² - 2x + 1 + 4x² + 4x + 1 = 5. | Expanding. |
| 5x² + 2x + 2 = 5 ⇒ 5x² + 2x - 3 = 0. | Collecting terms. |
| Δ = 2² - 4(5)(-3) = 4 + 60 = 64 > 0. | Discriminant is positive. |
| Since Δ > 0, the line intersects the circle at two distinct points. | The line is a secant. |

---

## 9.5 两圆的位置关系

### 9.5.1 五种位置关系

设圆 C1 圆心 O1、半径 r1；圆 C2 圆心 O2、半径 r2；圆心距 d = O1O2。

| 关系 | 条件 | 示意图描述 |
|------|------|-----------|
| **外离** | d > r1 + r2 | 两圆无公共点，互不重叠 |
| **外切** | d = r1 + r2 | 两圆恰好相切于一点，在外部接触 |
| **相交** | |r1 - r2| < d < r1 + r2 | 两个公共点 |
| **内切** | d = |r1 - r2| | 两圆恰好相切于一点，一个在另一个内部 |
| **内含** | d < |r1 - r2| | 一个圆完全在另一个内部，无公共点 |
| **同心圆** | d = 0（且 r1 ≠ r2） | 圆心重合（属于内含的特例） |

### 9.5.2 公共弦（公弦）

当两圆相交于两点时，这两个交点的连线称为**公共弦**。

设两圆方程为：

    C1: x² + y² + 2g1x + 2f1y + c1 = 0
    C2: x² + y² + 2g2x + 2f2y + c2 = 0

交点同时满足两个方程。两式相减，x² + y² 项消去，得到一条直线：

    2(g1 - g2)x + 2(f1 - f2)y + (c1 - c2) = 0

因为两个交点都满足两圆方程，它们必然也满足相减后的方程，因此这条直线就是通过两个交点的直线——公共弦。当两圆相切时，该直线变为**公切线**。

---

**示例 1（判断位置关系）**：判断圆 C1: x² + y² = 4 和 C2: (x - 4)² + y² = 1 的位置关系。

| Statement | Reason |
|-----------|--------|
| C1: centre O1(0, 0), radius r1 = 2. | From standard form. |
| C2: centre O2(4, 0), radius r2 = 1. | From standard form. |
| d = √[(4 - 0)² + (0 - 0)²] = 4. | Distance between centres. |
| r1 + r2 = 2 + 1 = 3. | Sum of radii. |
| d = 4 > 3 = r1 + r2. | Since the centre distance exceeds the sum of radii. |
| The circles are **separate** (externally disjoint). | They have no common points. |

---

**示例 2（相切条件）**：圆 C1: x² + y² = 9 与 C2: (x - 5)² + y² = r² 外切。求 r。

| Statement | Reason |
|-----------|--------|
| C1: (0, 0), r1 = 3. C2: (5, 0), r2 = r. | Identifying centres and radii. |
| d = √[(5 - 0)² + 0²] = 5. | Distance between centres. |
| For external tangency: d = r1 + r2. | Definition of externally tangent circles. |
| 5 = 3 + r ⇒ r = 2. | Solving for r. |
| The radius of C2 must be 2. | So the circles touch at exactly one point. |

---

**示例 3（求公共弦）**：两圆 C1: x² + y² - 6x + 4y - 3 = 0 和 C2: x² + y² + 2x - 8y + 5 = 0 相交。求公共弦方程。

| Statement | Reason |
|-----------|--------|
| C1 - C2: (x² + y² - 6x + 4y - 3) - (x² + y² + 2x - 8y + 5) = 0. | Subtracting the equations eliminates x² + y². |
| -6x + 4y - 3 - 2x + 8y - 5 = 0. | Removing brackets and simplifying signs. |
| -8x + 12y - 8 = 0. | Collecting like terms. |
| Divide by -4: 2x - 3y + 2 = 0. | Simplifying. |
| The common chord is 2x - 3y + 2 = 0. | This line passes through both intersection points. |

---

## 9.6 综合例题（解答见章末）

以下例题综合运用本章的多个知识点。建议先独立尝试，再对照章末的详细解答。

---

**例题 1**：圆 C 的圆心在直线 y = 2x + 1 上，且经过点 A(1, 4) 和 B(3, 0)。求圆 C 的方程。

---

**例题 2**：已知直线 y = 2x + k 与圆 x² + y² - 2x + 4y - 4 = 0 相交于两个不同的点。求 k 的取值范围。

---

**例题 3**：圆 C1: (x - 1)² + (y - 3)² = 25 和圆 C2: (x + 2)² + (y - 7)² = 4。
(a) 判断两圆的位置关系。
(b) 若相交，求公共弦的方程。

---

**例题 4**：圆 x² + y² = 10 和圆外一点 P(5, 5)。求从 P 向该圆所作的两条切线方程。

---

**例题 5**：点 A(2, 5)、B(6, 1)、C(8, 5)。
(a) 求 AB 的垂直平分线方程。
(b) 求 BC 的垂直平分线方程。
(c) 证明这两条垂直平分线的交点就是过 A、B、C 三点的圆的圆心。

---

## 9.7 综合例题解答

### 例题 1 解答

| Statement | Reason |
|-----------|--------|
| Let the centre be (h, 2h + 1). | The centre lies on y = 2x + 1. |
| A(1, 4) and B(3, 0) are on the circle. | Given. |
| CA = CB (both equal the radius). | All points on a circle are equidistant from the centre. |
| (h - 1)² + (2h + 1 - 4)² = (h - 3)² + (2h + 1 - 0)². | Using distance formula: CA² = CB². |
| (h - 1)² + (2h - 3)² = (h - 3)² + (2h + 1)². | Simplifying y-differences. |
| h² - 2h + 1 + 4h² - 12h + 9 = h² - 6h + 9 + 4h² + 4h + 1. | Expanding all squares. |
| 5h² - 14h + 10 = 5h² - 2h + 10. | Collecting like terms on both sides. |
| -14h + 10 = -2h + 10 ⇒ -12h = 0 ⇒ h = 0. | Subtracting 5h² and 10 from both sides. |
| Centre = (0, 1). | Substituting h = 0 into (h, 2h + 1). |
| r² = (0 - 1)² + (1 - 4)² = 1 + 9 = 10. | Distance from centre to A(1, 4). |
| The circle equation is (x - 0)² + (y - 1)² = 10, i.e. x² + (y - 1)² = 10. | Final answer. |

---

### 例题 2 解答

| Statement | Reason |
|-----------|--------|
| x² + y² - 2x + 4y - 4 = 0 ⇒ (x - 1)² + (y + 2)² = 9. | Completing the square to find centre and radius. |
| Centre (1, -2), radius r = 3. | From standard form. |
| Substitute y = 2x + k: (x - 1)² + (2x + k + 2)² = 9. | Substituting into circle equation. |
| x² - 2x + 1 + 4x² + 4(k + 2)x + (k + 2)² = 9. | Expanding. |
| 5x² + [4(k + 2) - 2]x + [1 + (k + 2)² - 9] = 0. | Grouping x², x and constant terms. |
| 5x² + (4k + 6)x + (k² + 4k + 4 - 8) = 0. | Simplifying coefficients. |
| 5x² + (4k + 6)x + (k² + 4k - 4) = 0. | Final quadratic in x. |
| For two distinct intersections, Δ > 0. | A quadratic with Δ > 0 has two distinct real roots. |
| Δ = (4k + 6)² - 4(5)(k² + 4k - 4) > 0. | Discriminant condition. |
| 16k² + 48k + 36 - 20k² - 80k + 80 > 0. | Expanding. |
| -4k² - 32k + 116 > 0. | Collecting terms. |
| Divide by -4 (reverse inequality): k² + 8k - 29 < 0. | Note: dividing by a negative flips the inequality. |
| Roots of k² + 8k - 29 = 0: k = (-8 ± √(64 + 116)) / 2 = (-8 ± √180) / 2 = -4 ± 3√5. | Quadratic formula. |
| Since the quadratic in k opens upward, k² + 8k - 29 < 0 between the roots. | The inequality is satisfied for values between the roots. |
| -4 - 3√5 < k < -4 + 3√5. | The range of k for which the line intersects the circle at two points. |

---

### 例题 3 解答

**Part (a)**

| Statement | Reason |
|-----------|--------|
| C1: centre O1(1, 3), r1 = 5. | From (x - 1)² + (y - 3)² = 25. |
| C2: centre O2(-2, 7), r2 = 2. | From (x + 2)² + (y - 7)² = 4. |
| d = √[(1 - (-2))² + (3 - 7)²] = √[3² + (-4)²] = √(9 + 16) = 5. | Distance between centres. |
| r1 + r2 = 5 + 2 = 7, |r1 - r2| = 3. | Sum and difference of radii. |
| 3 < 5 < 7, i.e. |r1 - r2| < d < r1 + r2. | d lies between the difference and the sum. |
| Therefore the circles **intersect at two points**. | Condition for two intersections. |

**Part (b)**

| Statement | Reason |
|-----------|--------|
| C1 in general form: x² + y² - 2x - 6y - 15 = 0. | Expanding (x - 1)² + (y - 3)² = 25. |
| C2 in general form: x² + y² + 4x - 14y + 49 - 4 = 0 ⇒ x² + y² + 4x - 14y + 45 = 0. | Expanding (x + 2)² + (y - 7)² = 4. |
| Subtract C2 from C1: (-2x - 6y - 15) - (4x - 14y + 45) = 0. | x² + y² terms cancel. |
| -2x - 6y - 15 - 4x + 14y - 45 = 0 ⇒ -6x + 8y - 60 = 0. | Simplifying. |
| Divide by -2: 3x - 4y + 30 = 0. | The common chord equation. |

---

### 例题 4 解答

| Statement | Reason |
|-----------|--------|
| Centre (0, 0), radius r = √10. | Circle x² + y² = 10. |
| Let tangent have slope m, equation y - 5 = m(x - 5). | Point-slope form through P(5, 5). |
| mx - y + (5 - 5m) = 0. | General form. |
| Distance from (0,0) to line = |5 - 5m| / √(m² + 1) = √10. | Distance equals radius. |
| |5 - 5m| = √10 √(m² + 1). | Multiplying both sides. |
| (5 - 5m)² = 10(m² + 1). | Squaring both sides. |
| 25 - 50m + 25m² = 10m² + 10. | Expanding. |
| 15m² - 50m + 15 = 0. | Collecting terms. |
| Divide by 5: 3m² - 10m + 3 = 0. | Simplifying. |
| (3m - 1)(m - 3) = 0 ⇒ m = 3 or m = 1/3. | Factorising. |
| For m = 3: y - 5 = 3(x - 5) ⇒ y = 3x - 10. | First tangent. |
| For m = 1/3: y - 5 = (1/3)(x - 5) ⇒ 3y - 15 = x - 5 ⇒ x - 3y + 10 = 0. | Second tangent. |
| Check x = 5: distance from (0,0) to x = 5 is 5 ≠ √10. | Not a tangent. |
| The two tangents are y = 3x - 10 and x - 3y + 10 = 0. | Final answer. |

---

### 例题 5 解答

**Part (a)**

| Statement | Reason |
|-----------|--------|
| A(2, 5), B(6, 1). | Given. |
| Midpoint M_AB = ((2 + 6)/2, (5 + 1)/2) = (4, 3). | Midpoint formula. |
| m_AB = (1 - 5) / (6 - 2) = -4 / 4 = -1. | Gradient of AB. |
| Perpendicular gradient = 1. | Negative reciprocal of -1. |
| Equation: y - 3 = 1(x - 4) ⇒ y = x - 1. | Perpendicular bisector of AB. |

**Part (b)**

| Statement | Reason |
|-----------|--------|
| B(6, 1), C(8, 5). | Given. |
| Midpoint M_BC = ((6 + 8)/2, (1 + 5)/2) = (7, 3). | Midpoint formula. |
| m_BC = (5 - 1) / (8 - 6) = 4 / 2 = 2. | Gradient of BC. |
| Perpendicular gradient = -1/2. | Negative reciprocal of 2. |
| Equation: y - 3 = (-1/2)(x - 7). | Perpendicular bisector of BC. |
| y - 3 = (-1/2)x + 7/2 ⇒ y = (-1/2)x + 13/2. | Simplifying. |

**Part (c)**

| Statement | Reason |
|-----------|--------|
| Intersection of the two bisectors: x - 1 = (-1/2)x + 13/2. | Equating y from both equations. |
| x + (1/2)x = 13/2 + 1 ⇒ (3/2)x = 15/2 ⇒ x = 5. | Solving for x. |
| y = 5 - 1 = 4. | Substituting x = 5 into y = x - 1. |
| Intersection O = (5, 4). | The common point of the two perpendicular bisectors. |
| OA = √[(5 - 2)² + (4 - 5)²] = √(9 + 1) = √10. | Distance from O to A. |
| OB = √[(5 - 6)² + (4 - 1)²] = √(1 + 9) = √10. | Distance from O to B. |
| OC = √[(5 - 8)² + (4 - 5)²] = √(9 + 1) = √10. | Distance from O to C. |
| OA = OB = OC = √10. | O is equidistant from all three vertices. |
| Therefore O(5, 4) is the centre of the circle passing through A, B and C, with radius √10. | The perpendicular bisectors of any two chords of a circle intersect at the centre. |

---

## 9.8 本章总结

| 主题 | 核心公式 / 方法 |
|------|----------------|
| **直线方程** | 斜截式 y = mx + c，点斜式 y - y1 = m(x - x1)，一般式 Ax + By + C = 0 |
| **平行条件** | m1 = m2 |
| **垂直条件** | m1 · m2 = -1 |
| **中点公式** | ((x1 + x2)/2, (y1 + y2)/2) |
| **两点距离** | √[(x2 - x1)² + (y2 - y1)²] |
| **点到直线距离** | d = $|Ax0 + By0 + C|$ / √(A² + B²) |
| **垂直平分线** | 斜率 = -1/m_AB，过 AB 中点 |
| **线性化——幂函数** | y = Ax^n ⇒ ln y = n ln x + ln A |
| **线性化——指数函数** | y = Ab^x ⇒ ln y = (ln b)x + ln A |
| **圆的标准式** | (x - a)² + (y - b)² = r²，圆心 (a, b)，半径 r |
| **圆的一般式** | x² + y² + 2gx + 2fy + c = 0，圆心 (-g, -f)，半径 √(g² + f² - c) |
| **直线与圆** | 代入 → 二次方程 → Δ > 0 相交，Δ = 0 相切，Δ < 0 相离 |
| **切线（已知切点）** | (x1 - a)(x - a) + (y1 - b)(y - b) = r² |
| **切线（已知斜率）** | y - b = m(x - a) ± r √(1 + m²) |
| **两圆关系** | 比较 d 与 r1 + r2、|r1 - r2| |
| **公共弦** | 两圆方程相减所得直线 |

---
---
# 第10章 综合应用

## 考纲对照

本章对应考纲“第10章 综合应用”，包含以下两个核心板块：
- **10.1 运动学**：利用微分与积分研究位移、速度、加速度之间的关系，并能从运动图像中提取信息。
- **10.2 跨章节综合题**：将数列、向量、函数、三角、几何、微积分等知识融合，解决实际或数学情境中的复杂问题。

考纲强调“综合”，要求学生能够灵活调用前面各章的工具，尤其注重微积分在运动学中的直观应用，以及不同知识点之间的相互转化。

---

## 10.1 运动学（位移、速度、加速度，微分与积分，运动图像）

### 10.1.1 基本概念与关系

设质点沿直线运动，其位移 s(t) 是时间 t 的函数。则  
- 瞬时速度 v(t) = s'(t)；  
- 瞬时加速度 a(t) = v'(t) = s''(t)。

反过来，从加速度或速度积分可得：
v(t) = v(t₀) + ∫_{t₀}^{t} a(τ) dτ,    s(t) = s(t₀) + ∫_{t₀}^{t} v(τ) dτ.

**运动图像**：  
- s-t 图：切线斜率为速度，上凸表示减速（速度减小），下凸表示加速。  
- v-t 图：曲线下面积（定积分）表示位移；切线斜率为加速度。  
- a-t 图：曲线下面积表示速度变化量。

### 10.1.2 典型例题

**例题1**（基础微分关系）  
一个物体沿直线运动，其位移 s(t) = 2t³ - 9t² + 12t + 5（单位：m，t ≥ 0）。  
(1) 求物体的速度函数和加速度函数；  
(2) 求物体在 t=2 s 时的速度和加速度；  
(3) 物体何时静止（速度为零）？

**解**  
(1) v(t) = s'(t) = 6t² - 18t + 12 (m/s), a(t) = v'(t) = 12t - 18 (m/s²).

(2) v(2) = 6×4 - 18×2 + 12 = 24 - 36 + 12 = 0 (m/s), a(2) = 12×2 - 18 = 6 (m/s²).

(3) 解 v(t)=0：6t² - 18t + 12 = 0 ⇒ t² - 3t + 2 = 0 ⇒ (t-1)(t-2)=0, 故 t=1 s 或 t=2 s 时物体静止。

---

**例题2**（积分求位移与路程）  
一质点沿直线运动，速度函数为 v(t) = 3t² - 12t + 9（单位：m/s，t ≥ 0）。已知初始位移 s(0)=0。  
(1) 求位移函数 s(t)；  
(2) 求质点在前4秒内的位移和总路程。

**解**  
(1) s(t) = ∫ (3t² - 12t + 9) dt = t³ - 6t² + 9t + C, 由 s(0)=0 得 C=0，所以 s(t) = t³ - 6t² + 9t。

(2) 位移 = s(4)-s(0) = (64 - 96 + 36) - 0 = 4 m。  
求总路程需考虑速度的正负。解 v(t)=0：3t² - 12t + 9 = 0 ⇒ t² - 4t + 3 = 0 ⇒ t=1, t=3。  
速度符号：t∈[0,1) 时 v>0；t∈(1,3) 时 v<0；t∈(3,4] 时 v>0。  
路程 = ∫₀¹ v dt + ∫₁³ (-v) dt + ∫₃⁴ v dt。  
计算各段位移的绝对值：  
- [0,1]：s(1)-s(0) = 1-6+9 = 4 m  
- [1,3]：|s(3)-s(1)| = |(27-54+27) - 4| = |0-4| = 4 m  
- [3,4]：s(4)-s(3) = 4 - 0 = 4 m  
总路程 = 4+4+4 = 12 m。

---

**例题3**（运动图像分析）  
某物体做直线运动，其 v-t 图像如图所示（假设图线由三段直线组成）：  
- 0~2 s：斜率为 2 的直线，从 v=0 到 v=4；  
- 2~5 s：水平直线 v=4；  
- 5~7 s：斜率为 -2 的直线，从 v=4 到 v=0。  

(1) 画出对应的 a-t 图像；  
(2) 求物体在 0~7 s 内的位移和平均速度；  
(3) 求物体在 t=4 s 时的加速度。

**解**  
(1) a-t 图：  
- 0<t<2：a=2 m/s²（常数）；  
- 2<t<5：a=0；  
- 5<t<7：a=-2 m/s²。  
图像为三段水平线段。

(2) 位移 = v-t 图下面积（代数累加）：  
三角形1面积 = 0.5×2×4 = 4，矩形面积 = 3×4 = 12，三角形2面积 = 0.5×2×4 = 4，总和 = 20 m。  
平均速度 = 总位移 / 总时间 = 20/7 m/s。

(3) t=4 s 位于第二段（2~5 s），此时速度恒定，故加速度 a=0。

---

## 10.2 跨章节综合题

跨章节综合题常将函数、微积分、几何、三角、向量、数列等知识交织在一起，要求考生具有整体思维和灵活转换数学模型的能力。下面给出三个典型真题风格的例题。

### 例题4（函数与微分结合几何）

已知曲线 y = x³ - 3x² + 2x + 1。  
(1) 求曲线在点 (1,1) 处的切线方程；  
(2) 证明该切线也是曲线在某点处的法线，并求出该点坐标。

**解**  
(1) y' = 3x² - 6x + 2，在 x=1 处 y' = 3-6+2 = -1。  
切线斜率 k=-1，过 (1,1)：y-1 = -1(x-1) ⇒ y = -x+2。

(2) 若某点 (x₀, y₀) 处曲线的法线斜率为 -1/y'(x₀)，令其等于切线斜率 -1：-1/y'(x₀) = -1 ⇒ y'(x₀) = 1。  
解 3x₀² - 6x₀ + 2 = 1 ⇒ 3x₀² - 6x₀ + 1 = 0。  
得 x₀ = (6 ± √(36-12)) / 6 = 1 ± √6/3。  
已知 x=1 是切点，故另一解 x₀ = 1 + √6/3 或 1 - √6/3 对应的法线即为该切线。取 x₀ = 1 + √6/3，  
y₀ = (1 + √6/3)³ - 3(1 + √6/3)² + 2(1 + √6/3) + 1，  
计算略。因此切线也是曲线在另一点处的法线。

---

### 例题5（向量与三角综合）

一艘船在静水中的速度为 6 km/h，水流速度为 2 km/h，方向由西向东。船要到达正北方向的对岸，船头应朝哪个方向（与水流方向夹角）？船的实际速度大小是多少？

**解**  
建立坐标系：设水流方向为 x 轴正方向，北为 y 轴正方向。船相对于水的速度（船头方向）为 v_{b/w}，大小 6，方向与 x 轴夹角 θ（逆时针为正）。水流速度 v_w = (2,0)。  
实际速度 v_b = v_{b/w} + v_w = (6cosθ + 2, 6sinθ)。  
要求实际速度沿正北，即 x 分量为 0：6cosθ + 2 = 0 ⇒ cosθ = -1/3 ⇒ θ = arccos(-1/3) ≈ 109.47°。  
此时实际速度大小 = |6sinθ| = 6√(1 - 1/9) = 6√(8/9) = 4√2 ≈ 5.66 km/h。  
故船头应朝向北偏西 arccos(1/3) ≈ 70.53°。

---

### 例题6（数列与微积分综合）

某物体从静止开始做变加速直线运动，加速度 a(t) = 2e^{-0.5t}（m/s²）。  
(1) 求速度 v(t) 的表达式；  
(2) 证明当 t→∞ 时，速度趋近于一个常数，并求出这个常数；  
(3) 若将时间 [0, +∞) 等分为无穷多个长度为1的区间，各区间内位移的增量构成一个数列 {sₙ}，求该数列的通项公式，并判断级数 ∑_{n=1}^{∞} sₙ 是否收敛。

**解**  
(1) v(t) = ∫₀ᵗ a(τ) dτ = ∫₀ᵗ 2e^{-0.5τ} dτ = [-4e^{-0.5τ}]₀ᵗ = 4(1 - e^{-0.5t}) m/s。

(2) lim_{t→∞} v(t) = 4(1 - 0) = 4 m/s。说明物体最终趋近于匀速运动，速度为 4 m/s。

(3) 第 n 个时间区间 [n-1, n] 内的位移  
sₙ = ∫_{n-1}^{n} v(t) dt = ∫_{n-1}^{n} 4(1 - e^{-0.5t}) dt。  
计算：∫ 4 dt = 4t, ∫ 4e^{-0.5t} dt = -8e^{-0.5t},  
所以 sₙ = [4t + 8e^{-0.5t}]_{n-1}^{n} = 4n + 8e^{-0.5n} - [4(n-1) + 8e^{-0.5(n-1)}] = 4 + 8(e^{-0.5n} - e^{-0.5(n-1)}).  
化简：sₙ = 4 + 8e^{-0.5n}(1 - e^{0.5}) = 4 + 8e^{-0.5n}(1 - √e).  
由于 1 - √e < 0，故 sₙ < 4。  
级数 ∑_{n=1}^{∞} sₙ 的部分和 S_N = ∑_{n=1}^{N} sₙ = ∑_{n=1}^{N} 4 + 8(1-√e) ∑_{n=1}^{N} e^{-0.5n}.  
前者发散（4N → ∞），后者收敛（等比级数公比 e^{-0.5} < 1），故整体发散，即总路程无穷大（与物理直观一致，因速度趋于常数，无限时间下位移无限增加）。
