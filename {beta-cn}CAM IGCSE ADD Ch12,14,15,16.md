# 不定积分与求导：变化率视角
- 这份笔记由 LG-leo 整理和维护。如果你觉得这份笔记对你有帮助，欢迎在 GitHub 上关注我或给我一个 ⭐，这能帮助我持续产出更多免费的学习资源。
- 我的其他课程笔记：https://github.com/LG-leo?tab=repositories
- This note is maintained by LG-leo. If you find it helpful, feel free to follow me or leave a ⭐ on GitHub. It helps me keep producing more free study resources. Check out my other notes: https://github.com/LG-leo?tab=repositories
## 1. 变化率与导数的基本概念

导数表示函数在某一点的变化快慢。对于函数 y = f(x)，导数记作 dy/dx 或 f'(x)。

**物理意义**：如果 x 是时间，y 是位置，那么 dy/dx 就是速度。

**几何意义**：导数就是曲线切线的斜率。

### 1.1 幂函数的导数公式

$$
\frac{d}{dx} x^n = n x^{n-1}
$$

其中 n 是任意有理数。

**推导思路**  
从极限定义出发：  
$$
\frac{d}{dx} x^n = \lim_{h→0} \frac{(x+h)^n - x^n}{h}
$$  
利用二项式展开 (x+h)^n = x^n + n x^{n-1} h + ...，减去 x^n 后除以 h，再让 h→0，得到 n x^{n-1}。

**具体例子**  
- n=2：d/dx (x^2) = 2x  
- n=3：d/dx (x^3) = 3x^2  
- n= -1：d/dx (1/x) = -1/x^2  
- n= 1/2：d/dx (√x) = (1/2) x^{-1/2} = 1/(2√x)

### 1.2 常数倍与和差规则

$$
\frac{d}{dx} (c f(x)) = c f'(x)
$$

$$
\frac{d}{dx} (f(x) ± g(x)) = f'(x) ± g'(x)
$$

**例子**  
- d/dx (5x^3) = 15x^2  
- d/dx (x^4 - 3x^2 + 2x) = 4x^3 - 6x + 2

## 2. 不定积分：导数的逆运算

如果 F'(x) = f(x)，则 F(x) 是 f(x) 的一个原函数。不定积分表示所有原函数：

$$
\int f(x) dx = F(x) + C
$$

其中 C 是任意常数（因为常数的导数为零）。

### 2.1 幂函数的不定积分公式

当 n ≠ -1 时：

$$
\int x^n dx = \frac{x^{n+1}}{n+1} + C
$$

**验证**：对右边求导，得到 x^n。

**例子**  
- ∫ x^2 dx = x^3/3 + C  
- ∫ x^{-3} dx = x^{-2}/(-2) + C = -1/(2x^2) + C  
- ∫ √x dx = ∫ x^{1/2} dx = x^{3/2}/(3/2) + C = (2/3) x^{3/2} + C

当 n = -1 时：

$$
\int x^{-1} dx = \ln|x| + C
$$

因为 d/dx ln|x| = 1/x。

### 求导与不定积分对照表

| 函数 $f(x)$ | 导数 $f'(x)$ | 不定积分 $\int f(x) dx$ |
| :--- | :--- | :--- |
| $x^n \ (n \neq -1)$ | $n x^{n-1}$ | $x^{n+1}/(n+1) + C$ |
| $x^{-1}$ | $-1/x^2$ | $ln|x| + C$ |
| $e^x$ | $e^x$ | $e^x + C$ |
| $a^x \ (a>0)$ | $a^x ln a$ | $a^x / ln a + C$ |
| $ln|x|$ | $1/x$ | $x ln|x| - x + C$ |
| $log_a x$ | $1/(x ln a)$ | $(x ln|x| - x)/ln a + C$ |
| $sin x$ | $cos x$ | $-cos x + C$ |
| $cos x$ | $-sin x$ | $sin x + C$ |
| $tan x$ | $sec^2 x$ | $ln|sec x| + C$ |
| $cot x$ | $-csc^2 x$ | $ln|sin x| + C$ |
| $sec x$ | $sec x tan x$ | $ln|sec x + tan x| + C$ |
| $csc x$ | $-csc x cot x$ | $ln|csc x - cot x| + C$ |
| $arcsin x$ | $1/√(1-x^2)$ | $x arcsin x + √(1-x^2) + C$ |
| $arccos x$ | $-1/√(1-x^2)$ | $x arccos x - √(1-x^2) + C$ |
| $arctan x$ | $1/(1+x^2)$ | $x arctan x - (1/2) ln(1+x^2) + C$ |

### 运算规则

| 操作 | 求导 | 不定积分 |
| :--- | :--- | :--- |
| 常数倍 | $(c f)' = c f'$ | $\int c f dx = c \int f dx$ |
| 和差 | $(f ± g)' = f' ± g'$ | $\int (f ± g) dx = \int f dx ± \int g dx$ |
| 乘积 | $(f g)' = f' g + f g'$ | 分部积分：$\int f g' dx = f g - \int f' g dx$ |
| 商 | $(f/g)' = (f' g - f g')/g^2$ | 无直接公式 |
| 链式法则 | $[f(g(x))]' = f'(g(x)) g'(x)$ | 换元：$\int f'(g(x)) g'(x) dx = f(g(x)) + C$ |

### 2.2 线性性质

$$
\int (a f(x) + b g(x)) dx = a \int f(x) dx + b \int g(x) dx
$$

**例子**  
∫ (4x^3 - 2x + 5) dx = 4·(x^4/4) - 2·(x^2/2) + 5x + C = x^4 - x^2 + 5x + C

## 3. 变化率的常见应用场景

### 3.1 运动学中的速度与加速度

设位移为 s(t)，则  
速度 v(t) = ds/dt  
加速度 a(t) = dv/dt = d²s/dt²

已知加速度求速度：  
$$
v(t) = \int a(t) dt + v_0
$$
已知速度求位移：  
$$
s(t) = \int v(t) dt + s_0
$$
其中 v_0 和 s_0 是初始条件。

**例题**  
质点加速度 a(t) = 3t^2 - 2，初速度 v(0)=1，求速度函数。

解：  
v(t) = ∫ (3t^2 - 2) dt = t^3 - 2t + C  
代入 t=0：0 - 0 + C = 1 ⇒ C=1  
所以 v(t) = t^3 - 2t + 1

再求位移，设初位移 s(0)=0：  
s(t) = ∫ v(t) dt = ∫ (t^3 - 2t + 1) dt = t^4/4 - t^2 + t + D  
代入 t=0：0 + D = 0 ⇒ D=0  
所以 s(t) = t^4/4 - t^2 + t

### 3.2 几何中的切线斜率

曲线 y = f(x) 在点 (x₀, f(x₀)) 的切线斜率为 f'(x₀)。  
已知斜率函数 k(x)，求曲线方程：  
$$
y = \int k(x) dx + C
$$
C 由曲线经过的点确定。

**例题**  
曲线上每点切线斜率为 2x+1，且过点 (1,3)，求曲线方程。

解：  
y = ∫ (2x+1) dx = x^2 + x + C  
代入 (1,3)：1 + 1 + C = 3 ⇒ C=1  
所以 y = x^2 + x + 1

### 3.3 经济中的边际函数

边际成本 MC(x) = C'(x)，总成本函数  
$$
C(x) = \int MC(x) dx + 固定成本
$$

**例题**  
某产品边际成本 MC(x) = 4x + 2，固定成本为 100，求总成本函数。

解：  
C(x) = ∫ (4x+2) dx = 2x^2 + 2x + K  
C(0)=100 ⇒ K=100  
所以 C(x) = 2x^2 + 2x + 100

## 4. 与多项式的组合

### 4.1 多项式求导

多项式 P(x) = a_n x^n + a_{n-1} x^{n-1} + ... + a₁ x + a₀ 的导数  
$$
P'(x) = n a_n x^{n-1} + (n-1) a_{n-1} x^{n-2} + ... + a₁
$$

**例子**  
d/dx (4x^5 - 3x^3 + 2x - 7) = 20x^4 - 9x^2 + 2

### 4.2 多项式积分

$$
\int (a_n x^n + ... + a₀) dx = \frac{a_n}{n+1} x^{n+1} + \frac{a_{n-1}}{n} x^n + ... + a₀ x + C
$$

**例子**  
∫ (3x^4 - 2x^2 + 5) dx = (3/5)x^5 - (2/3)x^3 + 5x + C

### 4.3 复合多项式（链式法则）

对于 y = (ax + b)^n，令 u = ax+b，则  
$$
\frac{dy}{dx} = \frac{dy}{du}·\frac{du}{dx} = n u^{n-1}·a = a n (ax+b)^{n-1}
$$

**例子**  
- y = (2x+1)^3，dy/dx = 3(2x+1)^2·2 = 6(2x+1)^2  
- y = (5-3x)^4，dy/dx = 4(5-3x)^3·(-3) = -12(5-3x)^3

对应积分（n ≠ -1）：  
$$
\int (ax+b)^n dx = \frac{1}{a}·\frac{(ax+b)^{n+1}}{n+1} + C
$$

**例子**  
∫ (3x-2)^5 dx = (1/3)·(3x-2)^6/6 + C = (3x-2)^6/18 + C

当 n = -1 时：  
$$
\int \frac{1}{ax+b} dx = \frac{1}{a} \ln|ax+b| + C
$$

### 4.4 变化率实例：匀加速运动

加速度 a 为常数，则  
v(t) = ∫ a dt = a t + v₀  
s(t) = ∫ v(t) dt = (1/2)a t^2 + v₀ t + s₀  
这里 s(t) 是二次多项式。

## 5. 与三角函数的组合

**注意**：以下直接使用 sin, cos, tan, sec, csc, cot，不加反斜杠。角度用弧度。

### 5.1 基本导数公式（表格）

| 函数 f(x) | 导数 f'(x) |
| :--- | :--- |
| sin x | cos x |
| cos x | - sin x |
| tan x | sec^2 x |
| cot x | - csc^2 x |
| sec x | sec x tan x |
| csc x | - csc x cot x |

**推导提示**：以 sin x 为例，利用极限 lim_{h→0} sin h / h = 1 和 lim_{h→0} (cos h - 1)/h = 0。

### 5.2 基本积分公式

$$
\int sin x dx = - cos x + C
$$

$$
\int cos x dx = sin x + C
$$

$$
\int sec^2 x dx = tan x + C
$$

$$
\int csc^2 x dx = - cot x + C
$$

$$
\int sec x \, tan x dx = sec x + C
$$

$$
\int csc x \, cot x dx = - csc x + C
$$

**验证**：对右边求导即得左边。

### 5.3 复合三角函数（链式法则）

对于 y = sin(ax+b)：  
$$
\frac{dy}{dx} = a cos(ax+b)
$$

类似：  
- d/dx cos(kx) = -k sin(kx)  
- d/dx tan(px+q) = p sec^2(px+q)

**例子**  
- y = sin(2x)，y' = 2 cos(2x)  
- y = cos(3x+1)，y' = -3 sin(3x+1)  
- y = tan(4x)，y' = 4 sec^2(4x)

对应积分：  
$$
\int sin(ax+b) dx = -\frac{1}{a} cos(ax+b) + C
$$
$$
\int cos(ax+b) dx = \frac{1}{a} sin(ax+b) + C
$$
$$
\int sec^2(ax+b) dx = \frac{1}{a} tan(ax+b) + C
$$

### 5.4 乘积法则与三角函数

$$
\frac{d}{dx} (u v) = u' v + u v'
$$

**例子**  
- y = x sin x，y' = 1·sin x + x·cos x = sin x + x cos x  
- y = x^2 cos x，y' = 2x cos x + x^2·(- sin x) = 2x cos x - x^2 sin x

### 5.5 商法则与三角函数

$$
\frac{d}{dx} \left( \frac{u}{v} \right) = \frac{u' v - u v'}{v^2}
$$

**例子**  
- y = sin x / x，y' = (x cos x - sin x)/x^2  
- y = tan x = sin x / cos x，利用商法则：  
  y' = (cos x·cos x - sin x·(- sin x))/cos^2 x = (cos^2 x + sin^2 x)/cos^2 x = 1/cos^2 x = sec^2 x

### 5.6 三角函数与多项式组合的积分（分部积分）

分部积分公式：  
$$
\int u dv = u v - \int v du
$$

**例1**：∫ x cos x dx  
令 u = x，dv = cos x dx，则 du = dx，v = sin x  
所以 ∫ x cos x dx = x sin x - ∫ sin x dx = x sin x + cos x + C

**例2**：∫ x sin x dx  
令 u = x，dv = sin x dx，则 du = dx，v = - cos x  
所以 ∫ x sin x dx = -x cos x + ∫ cos x dx = -x cos x + sin x + C

**例3**：∫ x^2 sin x dx（两次分部积分）  
先令 u = x^2，dv = sin x dx，则 du = 2x dx，v = - cos x  
得 ∫ x^2 sin x dx = -x^2 cos x + ∫ 2x cos x dx  
再计算 ∫ 2x cos x dx = 2(x sin x + cos x) + C₁  
所以 ∫ x^2 sin x dx = -x^2 cos x + 2x sin x + 2 cos x + C

### 5.7 三角函数幂的导数与积分

**导数**：  
- y = sin^3 x = (sin x)^3，则 y' = 3 sin^2 x · cos x  
- y = cos^4 x，则 y' = 4 cos^3 x · (- sin x) = -4 cos^3 x sin x

**积分**（换元法）：  
∫ sin^2 x cos x dx，令 u = sin x，du = cos x dx，得 ∫ u^2 du = u^3/3 + C = (1/3) sin^3 x + C

### 5.8 变化率实例：简谐振动

位移 x = A sin(ωt + φ)  
速度 v = dx/dt = Aω cos(ωt + φ)  
加速度 a = dv/dt = -Aω^2 sin(ωt + φ) = -ω^2 x

已知加速度 a(t) = -ω^2 A sin(ωt + φ)，积分求速度：  
v(t) = ∫ a dt = -ω^2 A ∫ sin(ωt+φ) dt = -ω^2 A·(-1/ω) cos(ωt+φ) + C = ω A cos(ωt+φ) + C  
由初始条件确定 C。

## 6. 与向量的组合

向量函数 r(t) = (x(t), y(t), z(t)) 的导数与积分逐分量进行。

### 6.1 导数

$$
\frac{d\mathbf{r}}{dt} = \left( \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right)
$$

### 6.2 不定积分

$$
\int \mathbf{r}(t) dt = \left( \int x(t) dt, \int y(t) dt, \int z(t) dt \right) + \mathbf{C}
$$
其中 C 是常向量。

### 6.3 位置、速度、加速度

在平面运动中，位置向量 r(t) = (x(t), y(t))。  
速度 v(t) = dr/dt  
加速度 a(t) = dv/dt

已知加速度求速度：  
$$
\mathbf{v}(t) = \int \mathbf{a}(t) dt + \mathbf{v}_0
$$
已知速度求位置：  
$$
\mathbf{r}(t) = \int \mathbf{v}(t) dt + \mathbf{r}_0
$$

**例题：抛体运动**  
加速度 a = (0, -g)，g 为重力加速度。  
v(t) = ∫ (0, -g) dt = (0, -g t) + (v_{0x}, v_{0y}) = (v_{0x}, v_{0y} - g t)  
r(t) = ∫ (v_{0x}, v_{0y} - g t) dt = (v_{0x} t, v_{0y} t - (1/2)g t^2) + (x₀, y₀)  
若初位置为 (0,0)，则 r(t) = (v_{0x} t, v_{0y} t - (1/2)g t^2)

### 6.4 向量与多项式组合

**例子**  
r(t) = (t^2, t^3, t)  
dr/dt = (2t, 3t^2, 1)  
∫ r(t) dt = (t^3/3, t^4/4, t^2/2) + C

### 6.5 向量与三角函数组合

**圆周运动**  
r(t) = (R cos(ωt), R sin(ωt))  
v(t) = (-Rω sin(ωt), Rω cos(ωt))  
a(t) = (-Rω^2 cos(ωt), -Rω^2 sin(ωt)) = -ω^2 r(t)

已知加速度 a(t) = (-ω^2 R cos(ωt), -ω^2 R sin(ωt))，积分求速度：  
v(t) = ( -ω^2 R ∫ cos(ωt) dt, -ω^2 R ∫ sin(ωt) dt ) = ( -ω R sin(ωt) + C₁, ω R cos(ωt) + C₂ )  
由初始条件确定 C₁, C₂。

### 6.6 向量与多项式、三角函数的混合

**例子**  
r(t) = (t sin t, t cos t)  
dr/dt = (sin t + t cos t, cos t - t sin t)

**积分**  
∫ r(t) dt = ( ∫ t sin t dt, ∫ t cos t dt ) = ( -t cos t + sin t, t sin t + cos t ) + C

### 6.7 数量积与向量积的导数

设 u(t) 和 v(t) 为向量函数，则  
$$
\frac{d}{dt} (\mathbf{u}·\mathbf{v}) = \mathbf{u}'·\mathbf{v} + \mathbf{u}·\mathbf{v}'
$$
$$
\frac{d}{dt} (\mathbf{u}×\mathbf{v}) = \mathbf{u}'×\mathbf{v} + \mathbf{u}×\mathbf{v}'
$$
这些公式在力学中常用，例如角动量 L = r × p 的导数等于力矩。

## 7. 综合例题（变化率与多种组合）

### 7.1 多项式与三角函数复合的求导

**例** y = sin(3x^2)  
解：令 u = 3x^2，则 y = sin u，dy/dx = cos u·(6x) = 6x cos(3x^2)

**对应积分**  
∫ 6x cos(3x^2) dx = sin(3x^2) + C

### 7.2 多项式与三角函数的乘积（分部积分）

**例** ∫ x^2 cos x dx  
解：令 u = x^2，dv = cos x dx，则 du = 2x dx，v = sin x  
∫ x^2 cos x dx = x^2 sin x - ∫ 2x sin x dx  
再计算 ∫ 2x sin x dx = 2( -x cos x + sin x ) + C₁  
所以 ∫ x^2 cos x dx = x^2 sin x + 2x cos x - 2 sin x + C

### 7.3 向量与多项式的运动学

**例** 加速度 a(t) = (2t, 3)，初速度 v(0) = (1,0)，初位置 r(0) = (0,0)。求运动方程。

解：  
v(t) = ∫ (2t, 3) dt = (t^2, 3t) + (C₁, C₂)  
代入 t=0：(0,0) + (C₁, C₂) = (1,0) ⇒ C₁=1, C₂=0，所以 v(t) = (t^2+1, 3t)

r(t) = ∫ (t^2+1, 3t) dt = (t^3/3 + t, 3t^2/2) + (D₁, D₂)  
代入 t=0：(0,0) + (D₁, D₂) = (0,0) ⇒ D₁=0, D₂=0  
所以 r(t) = (t^3/3 + t, 1.5 t^2)

### 7.4 向量与三角函数的运动学

**例** 加速度 a(t) = (- sin t, - cos t)，初速度 v(0) = (0,1)，初位置 r(0) = (1,0)。求运动方程。

解：  
v(t) = ∫ (- sin t, - cos t) dt = (cos t, - sin t) + (C₁, C₂)  
代入 t=0：(1,0) + (C₁, C₂) = (0,1) ⇒ C₁=-1, C₂=1  
所以 v(t) = (cos t - 1, 1 - sin t)

r(t) = ∫ (cos t - 1, 1 - sin t) dt = (sin t - t, t + cos t) + (D₁, D₂)  
代入 t=0：(0-0, 0+1) + (D₁, D₂) = (1,0) ⇒ (0,1)+(D₁, D₂)=(1,0) ⇒ D₁=1, D₂=-1  
所以 r(t) = (sin t - t + 1, t + cos t - 1)

### 7.5 实际变化率问题：圆锥形水槽

一个圆锥形水槽，顶部半径 R，高 H，以恒定速率 k 注水。求水面上升速率 dh/dt 与时间 t 的关系。

解：体积 V = (1/3)π r^2 h，由相似三角形 r/h = R/H ⇒ r = (R/H)h  
代入得 V = (1/3)π (R^2/H^2) h^3  
对时间求导：dV/dt = π (R^2/H^2) h^2 (dh/dt)  
已知 dV/dt = k，所以  
$$
\frac{dh}{dt} = \frac{k H^2}{\pi R^2 h^2}
$$
分离变量：h^2 dh = [k H^2/(π R^2)] dt  
积分：∫ h^2 dh = ∫ [k H^2/(π R^2)] dt  
得 h^3/3 = [k H^2/(π R^2)] t + C  
若初始 h(0)=0，则 C=0，所以  
$$
h(t) = \sqrt[3]{\frac{3k H^2}{\pi R^2} t}
$$

## 8. 高阶导数与多次积分

### 8.1 高阶导数

二阶导数表示变化率的变化率（加速度）。  
$$
f''(x) = \frac{d}{dx} f'(x)
$$

**例子**  
- f(x) = x^3，f'(x)=3x^2，f''(x)=6x  
- f(x) = sin x，f'(x)=cos x，f''(x)=- sin x

### 8.2 多次积分

已知二阶导数，求原函数需要积分两次。

**例题**  
已知 d²y/dx² = 6x，且 y'(0)=1，y(0)=0，求 y(x)。

解：  
y'(x) = ∫ 6x dx = 3x^2 + C₁  
代入 x=0：0 + C₁ = 1 ⇒ C₁=1，所以 y'(x)=3x^2+1  
y(x) = ∫ (3x^2+1) dx = x^3 + x + C₂  
代入 x=0：0+0+C₂=0 ⇒ C₂=0，所以 y(x)=x^3+x

## 9. 微分近似（变化率的线性近似）

对于函数 y = f(x)，当 x 变化 Δx 很小时，  
$$
Δy ≈ f'(x) Δx
$$
这个公式用于误差估计。

**例题**  
测量圆半径 r = 5 cm，误差 Δr = 0.1 cm，求面积 A = π r^2 的误差。

解：dA/dr = 2π r，所以 ΔA ≈ 2π r Δr = 2π·5·0.1 = π ≈ 3.14 cm²

## 10. 参数方程中的变化率

参数方程 x = f(t)，y = g(t)，则  
$$
\frac{dy}{dx} = \frac{dy/dt}{dx/dt}
$$
（前提是 dx/dt ≠ 0）

**例题**  
x = t^2，y = sin t，求 dy/dx 在 t = π/2 处的值。

解：dx/dt = 2t，dy/dt = cos t  
dy/dx = cos t / (2t)  
当 t=π/2 时，cos(π/2)=0，所以 dy/dx = 0/(π) = 0

**不定积分在参数形式**通常需要转换为 x 的函数，但有时直接对 t 积分也可。

## 11. 隐函数中的变化率（简要）

对于隐式方程 F(x, y)=0，可对两边关于 x 求导，解出 dy/dx。

**例题**  
x^2 + y^2 = 25，求 dy/dx。

解：两边对 x 求导：2x + 2y (dy/dx) = 0 ⇒ dy/dx = -x/y

## 12. 最后提醒

- 求导时牢记链式法则、乘积法则、商法则。
- 积分时务必加上常数 C，除非是定积分。
- 变化率的核心是“瞬时变化”与“累积”的互逆关系。
- 向量函数的微积分只是标量微积分在分量上的推广。

（以上内容覆盖了多项式、三角函数、向量的求导与积分，以及变化率的各种应用场景，每一条公式和例题均已单独列出并配有简短解释，避免大段文字。）

# 微分与不定积分：变化率视角

## 1. 变化率与微分的概念

函数 y = f(x) 的导数表示 x 变化时 y 的变化快慢。

记作 dy/dx 或 f'(x)。

**物理意义**：如果 x 是时间，y 是位移，则 dy/dx 是速度。

**几何意义**：导数是曲线切线的斜率。

### 1.1 幂函数的微分公式

$$
\frac{d}{dx} x^n = n x^{n-1}
$$

n 为任意有理数。

**推导**：从极限定义出发。

$$
\frac{d}{dx} x^n = \lim_{h→0} \frac{(x+h)^n - x^n}{h}
$$

二项式展开 (x+h)^n = x^n + n x^{n-1} h + ... ，减去 x^n 后除以 h，再令 h→0。

**例子**

- n=2：d/dx (x^2) = 2x
- n=3：d/dx (x^3) = 3x^2
- n=-1：d/dx (1/x) = -1/x^2
- n=1/2：d/dx (√x) = (1/2) x^{-1/2} = 1/(2√x)

### 1.2 微分的线性性质

常数倍规则：

$$
\frac{d}{dx} (c f(x)) = c f'(x)
$$

和差规则：

$$
\frac{d}{dx} (f(x) ± g(x)) = f'(x) ± g'(x)
$$

**例子**

- d/dx (5x^3) = 15x^2
- d/dx (x^4 - 3x^2 + 2x) = 4x^3 - 6x + 2

### 1.3 高阶导数

二阶导数是一阶导数的导数，记作 f''(x) 或 d²y/dx²。

物理上，位移 s(t) 的一阶导是速度 v(t)，二阶导是加速度 a(t)。

**幂函数的高阶导数**

f(x) = x^n
f'(x) = n x^{n-1}
f''(x) = n(n-1) x^{n-2}
f'''(x) = n(n-1)(n-2) x^{n-3}
...

**例子**

- f(x) = x^3，f'(x)=3x^2，f''(x)=6x，f'''(x)=6，更高阶为0。
- f(x) = sin x，f'(x)=cos x，f''(x)=-sin x，f'''(x)=-cos x，f''''(x)=sin x，周期循环。

## 2. 不定积分：微分的逆运算

如果 F'(x) = f(x)，则 F(x) 是 f(x) 的一个原函数。

不定积分表示所有原函数：

$$
\int f(x) dx = F(x) + C
$$

C 为任意常数（常数的导数为零）。

### 2.1 幂函数的不定积分公式

当 n ≠ -1 时：

$$
\int x^n dx = \frac{x^{n+1}}{n+1} + C
$$

**验证**：对右边求导得 x^n。

**例子**

- ∫ x^2 dx = x^3/3 + C
- ∫ x^{-3} dx = x^{-2}/(-2) + C = -1/(2x^2) + C
- ∫ √x dx = ∫ x^{1/2} dx = x^{3/2} / (3/2) + C = (2/3) x^{3/2} + C

当 n = -1 时：

$$
\int x^{-1} dx = \ln|x| + C
$$

因为 d/dx ln|x| = 1/x。

### 2.2 不定积分的线性性质

$$
\int (a f(x) + b g(x)) dx = a \int f(x) dx + b \int g(x) dx
$$

**例子**

∫ (4x^3 - 2x + 5) dx = 4·(x^4/4) - 2·(x^2/2) + 5x + C = x^4 - x^2 + 5x + C

### 2.3 从高阶导数求原函数（多次积分）

已知二阶导数，积分两次得到原函数，每次积分产生一个常数。

**例题**

已知 d²y/dx² = 6x，且 y'(0)=1，y(0)=0，求 y(x)。

解：

第一步：y'(x) = ∫ 6x dx = 3x^2 + C₁

代入 x=0：0 + C₁ = 1 ⇒ C₁=1，所以 y'(x)=3x^2+1

第二步：y(x) = ∫ (3x^2+1) dx = x^3 + x + C₂

代入 x=0：0+0+C₂=0 ⇒ C₂=0

所以 y(x) = x^3 + x

## 3. 变化率的常见应用

### 3.1 运动学中的速度与加速度

设位移 s(t) 是时间 t 的函数。

速度 v(t) = ds/dt

加速度 a(t) = dv/dt = d²s/dt²

已知加速度求速度：

$$
v(t) = \int a(t) dt + v_0
$$

已知速度求位移：

$$
s(t) = \int v(t) dt + s_0
$$

v₀, s₀ 是初速度和初位移。

**例题**

质点加速度 a(t) = 3t^2 - 2，初速度 v(0)=1，初位移 s(0)=0。

求 v(t) 和 s(t)。

解：

v(t) = ∫ (3t^2 - 2) dt = t^3 - 2t + C

代入 t=0：0 - 0 + C = 1 ⇒ C=1，所以 v(t)=t^3 - 2t + 1

s(t) = ∫ (t^3 - 2t + 1) dt = t^4/4 - t^2 + t + D

代入 t=0：0 + D = 0 ⇒ D=0，所以 s(t)=t^4/4 - t^2 + t

### 3.2 几何中的切线与法线

曲线 y = f(x) 在点 (x₀, f(x₀)) 的切线斜率 = f'(x₀)。

切线方程：

$$
y - f(x₀) = f'(x₀) (x - x₀)
$$

法线斜率 = -1/f'(x₀)（若 f'(x₀) ≠ 0）。

法线方程：

$$
y - f(x₀) = -\frac{1}{f'(x₀)} (x - x₀)
$$

已知斜率函数 k(x)，求曲线方程：

$$
y = \int k(x) dx + C
$$

C 由曲线经过的点确定。

**例题**

曲线上每点切线斜率为 2x+1，且过点 (1,3)，求曲线方程。

解：

y = ∫ (2x+1) dx = x^2 + x + C

代入 (1,3)：1+1+C=3 ⇒ C=1

所以 y = x^2 + x + 1

### 3.3 经济学中的边际函数

边际成本 MC(x) = C'(x)，总成本函数：

$$
C(x) = \int MC(x) dx + \text{固定成本}
$$

固定成本 = C(0)。

**例题**

边际成本 MC(x)=4x+2，固定成本为100，求总成本函数。

解：

C(x) = ∫ (4x+2) dx = 2x^2 + 2x + K

C(0)=100 ⇒ K=100

所以 C(x)=2x^2+2x+100

类似地，边际收益、边际利润也由微分定义，积分求总量。

### 3.4 微分近似（线性近似）

当 Δx 很小时：

$$
Δy ≈ f'(x) Δx
$$

用于误差估计。

**例题**

测量圆半径 r=5 cm，误差 Δr=0.1 cm，求面积 A=πr^2 的误差。

解：

dA/dr = 2πr

ΔA ≈ 2πr Δr = 2π·5·0.1 = π ≈ 3.14 cm²

## 4. 与多项式的组合

### 4.1 多项式求导

多项式 P(x) = a_n x^n + a_{n-1} x^{n-1} + ... + a₁ x + a₀

导数：

$$
P'(x) = n a_n x^{n-1} + (n-1) a_{n-1} x^{n-2} + ... + a₁
$$

常数项导数为0。

**例子**

d/dx (4x^5 - 3x^3 + 2x - 7) = 20x^4 - 9x^2 + 2

### 4.2 多项式不定积分

$$
\int (a_n x^n + ... + a₀) dx = \frac{a_n}{n+1} x^{n+1} + \frac{a_{n-1}}{n} x^n + ... + a₀ x + C
$$

**例子**

∫ (3x^4 - 2x^2 + 5) dx = (3/5)x^5 - (2/3)x^3 + 5x + C

### 4.3 复合多项式（链式法则）

对于 y = (ax+b)^n，令 u = ax+b，则：

$$
\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = n u^{n-1} \cdot a = a n (ax+b)^{n-1}
$$

**例子**

- y = (2x+1)^3，dy/dx = 3(2x+1)^2·2 = 6(2x+1)^2
- y = (5-3x)^4，dy/dx = 4(5-3x)^3·(-3) = -12(5-3x)^3

对应不定积分（n ≠ -1）：

$$
\int (ax+b)^n dx = \frac{1}{a} \cdot \frac{(ax+b)^{n+1}}{n+1} + C
$$

**例子**

∫ (3x-2)^5 dx = (1/3)·(3x-2)^6/6 + C = (3x-2)^6/18 + C

当 n = -1 时：

$$
\int \frac{1}{ax+b} dx = \frac{1}{a} \ln|ax+b| + C
$$

### 4.4 多项式变化率的实际例子：匀加速运动

加速度 a 为常数。

v(t) = ∫ a dt = a t + v₀

s(t) = ∫ v(t) dt = (1/2) a t^2 + v₀ t + s₀

这里 s(t) 是二次多项式，v(t) 是一次多项式，a 是常数。

### 4.5 高阶导数与多项式

每求一次导，次数降低1。例如：

f(x)=x^5
f'(x)=5x^4
f''(x)=20x^3
f'''(x)=60x^2
f''''(x)=120x
f'''''(x)=120
更高阶为0。

多次积分则升高次数，并产生多项式常数项。

## 5. 与三角函数的组合

注意：以下直接写 sin, cos, tan, sec, csc, cot，不加反斜杠。角度用弧度。

### 5.1 基本微分公式（表格）

| 函数 f(x) | 导数 f'(x) |
| :--- | :--- |
| sin x | cos x |
| cos x | - sin x |
| tan x | sec^2 x |
| cot x | - csc^2 x |
| sec x | sec x tan x |
| csc x | - csc x cot x |

**推导提示**：利用极限 lim_{h→0} sin h / h = 1 和 lim_{h→0} (cos h - 1)/h = 0。

### 5.2 基本不定积分公式

$$
\int sin x dx = - cos x + C
$$

$$
\int cos x dx = sin x + C
$$

$$
\int sec^2 x dx = tan x + C
$$

$$
\int csc^2 x dx = - cot x + C
$$

$$
\int sec x tan x dx = sec x + C
$$

$$
\int csc x cot x dx = - csc x + C
$$

**验证**：对右边求导即得左边。

### 5.3 复合三角函数（链式法则）

对于 y = sin(ax+b)：

$$
\frac{dy}{dx} = a cos(ax+b)
$$

类似：

d/dx cos(kx) = -k sin(kx)

d/dx tan(px+q) = p sec^2(px+q)

**例子**

- y = sin(2x)，y' = 2 cos(2x)
- y = cos(3x+1)，y' = -3 sin(3x+1)
- y = tan(4x)，y' = 4 sec^2(4x)

对应不定积分：

$$
\int sin(ax+b) dx = -\frac{1}{a} cos(ax+b) + C
$$

$$
\int cos(ax+b) dx = \frac{1}{a} sin(ax+b) + C
$$

$$
\int sec^2(ax+b) dx = \frac{1}{a} tan(ax+b) + C
$$

### 5.4 乘积法则与三角函数

$$
\frac{d}{dx} (u v) = u' v + u v'
$$

**例子**

- y = x sin x，y' = 1·sin x + x·cos x = sin x + x cos x
- y = x^2 cos x，y' = 2x cos x + x^2·(- sin x) = 2x cos x - x^2 sin x

### 5.5 商法则与三角函数

$$
\frac{d}{dx} \left( \frac{u}{v} \right) = \frac{u' v - u v'}{v^2}
$$

**例子**

- y = sin x / x，y' = (x cos x - sin x)/x^2
- y = tan x = sin x / cos x，利用商法则：
  y' = (cos x·cos x - sin x·(- sin x))/cos^2 x = (cos^2 x + sin^2 x)/cos^2 x = 1/cos^2 x = sec^2 x

### 5.6 三角函数与多项式组合的不定积分（分部积分）

分部积分公式：

$$
\int u dv = u v - \int v du
$$

**例1**：∫ x cos x dx

令 u = x，dv = cos x dx，则 du = dx，v = sin x

∫ x cos x dx = x sin x - ∫ sin x dx = x sin x + cos x + C

**例2**：∫ x sin x dx

令 u = x，dv = sin x dx，则 du = dx，v = - cos x

∫ x sin x dx = -x cos x + ∫ cos x dx = -x cos x + sin x + C

**例3**：∫ x^2 sin x dx（两次分部积分）

先令 u = x^2，dv = sin x dx，则 du = 2x dx，v = - cos x

∫ x^2 sin x dx = -x^2 cos x + ∫ 2x cos x dx

再计算 ∫ 2x cos x dx = 2(x sin x + cos x) + C₁

所以 ∫ x^2 sin x dx = -x^2 cos x + 2x sin x + 2 cos x + C

### 5.7 三角函数幂的微分与积分

**微分**

- y = sin^3 x = (sin x)^3，y' = 3 sin^2 x · cos x
- y = cos^4 x，y' = 4 cos^3 x · (- sin x) = -4 cos^3 x sin x

**积分（换元法）**

∫ sin^2 x cos x dx：令 u = sin x，du = cos x dx，得 ∫ u^2 du = u^3/3 + C = (1/3) sin^3 x + C

∫ cos^2 x sin x dx：令 u = cos x，du = - sin x dx，得 -∫ u^2 du = -u^3/3 + C = - (1/3) cos^3 x + C

### 5.8 三角函数的二阶导数

- sin x：一阶 cos x，二阶 - sin x
- cos x：一阶 - sin x，二阶 - cos x
- tan x：一阶 sec^2 x，二阶 2 sec^2 x tan x

简谐振动：位移 x = A sin(ωt+φ)，速度 v = Aω cos(ωt+φ)，加速度 a = -Aω^2 sin(ωt+φ) = -ω^2 x。

## 6. 与向量的组合

向量函数 r(t) = (x(t), y(t), z(t))。

### 6.1 向量函数的微分

$$
\frac{d\mathbf{r}}{dt} = \left( \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right)
$$

高阶导数类似：

$$
\frac{d^2\mathbf{r}}{dt^2} = \left( \frac{d^2x}{dt^2}, \frac{d^2y}{dt^2}, \frac{d^2z}{dt^2} \right)
$$

### 6.2 向量函数的不定积分

$$
\int \mathbf{r}(t) dt = \left( \int x(t) dt, \int y(t) dt, \int z(t) dt \right) + \mathbf{C}
$$

其中 C 是常向量。

### 6.3 位置、速度、加速度的向量形式

位置 r(t) = (x(t), y(t))

速度 v(t) = dr/dt

加速度 a(t) = dv/dt = d²r/dt²

已知加速度求速度：

$$
\mathbf{v}(t) = \int \mathbf{a}(t) dt + \mathbf{v}_0
$$

已知速度求位置：

$$
\mathbf{r}(t) = \int \mathbf{v}(t) dt + \mathbf{r}_0
$$

v₀, r₀ 是常向量。

**例题：抛体运动**

加速度 a = (0, -g)，g 为重力加速度。

v(t) = ∫ (0, -g) dt = (0, -g t) + (v₀x, v₀y) = (v₀x, v₀y - g t)

r(t) = ∫ (v₀x, v₀y - g t) dt = (v₀x t, v₀y t - (1/2)g t^2) + (x₀, y₀)

若初位置为 (0,0)，则 r(t) = (v₀x t, v₀y t - (1/2)g t^2)

### 6.4 向量与多项式组合

**例子**

r(t) = (t^2, t^3, t)

dr/dt = (2t, 3t^2, 1)

∫ r(t) dt = (t^3/3, t^4/4, t^2/2) + C

### 6.5 向量与三角函数组合

**圆周运动**

r(t) = (R cos(ωt), R sin(ωt))

v(t) = (-Rω sin(ωt), Rω cos(ωt))

a(t) = (-Rω^2 cos(ωt), -Rω^2 sin(ωt)) = -ω^2 r(t)

已知加速度 a(t) = (-ω^2 R cos(ωt), -ω^2 R sin(ωt))，积分求速度：

v(t) = ( -ω^2 R ∫ cos(ωt) dt, -ω^2 R ∫ sin(ωt) dt ) = ( -ω R sin(ωt) + C₁, ω R cos(ωt) + C₂ )

由初始条件确定 C₁, C₂。

### 6.6 向量与多项式、三角函数的混合

**例子**

r(t) = (t sin t, t cos t)

dr/dt = (sin t + t cos t, cos t - t sin t)

∫ r(t) dt = ( ∫ t sin t dt, ∫ t cos t dt ) = ( -t cos t + sin t, t sin t + cos t ) + C

### 6.7 数量积与向量积的微分

设 u(t), v(t) 为向量函数。

$$
\frac{d}{dt} (\mathbf{u}·\mathbf{v}) = \mathbf{u}'·\mathbf{v} + \mathbf{u}·\mathbf{v}'
$$

$$
\frac{d}{dt} (\mathbf{u}×\mathbf{v}) = \mathbf{u}'×\mathbf{v} + \mathbf{u}×\mathbf{v}'
$$

这些公式在力学中常用，例如角动量 L = r × p 的导数等于力矩。

## 7. 综合例题

### 7.1 多项式与三角函数复合的微分

**例**：y = sin(3x^2)

解：令 u = 3x^2，y = sin u

dy/dx = cos u * 6x = 6x cos(3x^2)

**对应积分**：∫ 6x cos(3x^2) dx = sin(3x^2) + C

### 7.2 多项式与三角函数乘积的积分

**例**：∫ x^2 cos x dx

解：令 u = x^2，dv = cos x dx，则 du = 2x dx，v = sin x

∫ x^2 cos x dx = x^2 sin x - ∫ 2x sin x dx

再计算 ∫ 2x sin x dx = 2(-x cos x + sin x) + C₁

所以 ∫ x^2 cos x dx = x^2 sin x + 2x cos x - 2 sin x + C

### 7.3 向量与多项式的运动学

**例**：加速度 a(t) = (2t, 3)，初速度 v(0) = (1,0)，初位置 r(0) = (0,0)。求运动方程。

解：

v(t) = ∫ (2t, 3) dt = (t^2, 3t) + (C₁, C₂)

代入 t=0：(0,0)+(C₁,C₂)=(1,0) ⇒ C₁=1, C₂=0，所以 v(t) = (t^2+1, 3t)

r(t) = ∫ (t^2+1, 3t) dt = (t^3/3 + t, 3t^2/2) + (D₁, D₂)

代入 t=0：(0,0)+(D₁,D₂)=(0,0) ⇒ D₁=0, D₂=0

所以 r(t) = (t^3/3 + t, 1.5 t^2)

### 7.4 向量与三角函数的运动学

**例**：加速度 a(t) = (- sin t, - cos t)，初速度 v(0) = (0,1)，初位置 r(0) = (1,0)。求运动方程。

解：

v(t) = ∫ (- sin t, - cos t) dt = (cos t, - sin t) + (C₁, C₂)

代入 t=0：(1,0)+(C₁,C₂)=(0,1) ⇒ C₁=-1, C₂=1，所以 v(t) = (cos t - 1, 1 - sin t)

r(t) = ∫ (cos t - 1, 1 - sin t) dt = (sin t - t, t + cos t) + (D₁, D₂)

代入 t=0：(0-0, 0+1)+(D₁,D₂)=(1,0) ⇒ (0,1)+(D₁,D₂)=(1,0) ⇒ D₁=1, D₂=-1

所以 r(t) = (sin t - t + 1, t + cos t - 1)

### 7.5 实际变化率问题：圆锥形水槽

一个圆锥形水槽，顶部半径 R，高 H，以恒定速率 k 注水。求水面上升速率 dh/dt 与时间 t 的关系。

解：

体积 V = (1/3)π r^2 h

由相似三角形 r/h = R/H ⇒ r = (R/H) h

代入得 V = (1/3)π (R^2/H^2) h^3

对时间求导：dV/dt = π (R^2/H^2) h^2 (dh/dt)

已知 dV/dt = k，所以

$$
\frac{dh}{dt} = \frac{k H^2}{\pi R^2 h^2}
$$

分离变量：h^2 dh = [k H^2/(π R^2)] dt

积分：∫ h^2 dh = ∫ [k H^2/(π R^2)] dt

得 h^3/3 = [k H^2/(π R^2)] t + C

若初始 h(0)=0，则 C=0，所以

$$
h(t) = \sqrt[3]{\frac{3k H^2}{\pi R^2} t}
$$

## 8. 隐函数与参数方程中的微分

### 8.1 隐函数求导

对于隐式方程 F(x, y)=0，两边对 x 求导，解出 dy/dx。

**例题**：x^2 + y^2 = 25，求 dy/dx。

解：两边对 x 求导：2x + 2y (dy/dx) = 0 ⇒ dy/dx = -x/y

### 8.2 参数方程求导

参数方程 x = f(t)，y = g(t)，则

$$
\frac{dy}{dx} = \frac{dy/dt}{dx/dt}
$$

前提 dx/dt ≠ 0。

**例题**：x = t^2，y = sin t，求 dy/dx 在 t = π/2 处的值。

解：dx/dt = 2t，dy/dt = cos t

dy/dx = cos t / (2t)

当 t = π/2 时，cos(π/2)=0，所以 dy/dx = 0/(π) = 0

不定积分在参数形式中通常需要转换为 x 的函数，但有时可直接对 t 积分。

## 9. 微分与积分的互逆关系总结

- 微分是求瞬时变化率，不定积分是累积变化量。
- 对函数先微分再积分，得原函数加常数。
- 对函数先积分再微分，回到原函数。
- 高阶导数与多次积分对应。

## 10. 最后提醒

- 求导时牢记链式法则、乘积法则、商法则。
- 积分时务必加上常数 C。
- 变化率的核心是“瞬时变化”与“累积”的互逆关系。
- 向量函数的微分和积分是标量微积分在分量上的推广。
- 多练习复合函数、隐函数、参数方程以及物理应用。

<!-- 
感谢使用这份笔记！如果你觉得它对你有帮助，请回到 GitHub 仓库页面点一个 ⭐，
这能帮助更多同学发现这个项目。仓库地址：https://github.com/LG-leo/IG0606ADD-with-CAM-coursebook-NOTE
-->
<!-- 
Thanks for using this note! If you find it helpful, please go back to the GitHub repository page and leave a ⭐.
It helps other students discover this project. Repository link: https://github.com/LG-leo/IG0606ADD-with-CAM-coursebook-NOTE
-->
