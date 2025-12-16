# 🧮 Calculus II Final Review Sheet
# Calculus II: Midterm II Review Guide

## I. Series Basics & Convergence Tests (§11.2 – 11.6)

### 1. Partial Sums ($s_n$) vs. Terms ($a_n$)
If you are given the sum formula $s_n$:
* **Find $a_n$:** $a_n = s_n - s_{n-1}$.
* **Find the total sum:** $S = \lim_{n \to \infty} s_n$.

### 2. The Big Three Early Tests
| Test | Condition | Conclusion |
| :--- | :--- | :--- |
| **Divergence Test** | $\lim_{n \to \infty} a_n \neq 0$ | Series Diverges. |
| **Geometric Series** | $\sum ar^{n-1}$ | Converges if $|r| < 1$, Sum $S = \frac{a}{1-r}$. |
| **Telescoping Series** | Terms cancel out | Write out first few partial sums and take the limit. |

### 3. Integral Test & Remainder (§11.3)
**Conditions:** Function must be positive, continuous, and decreasing.  
**Rule:** $\sum a_n$ converges if and only if $\int_{1}^{\infty} f(x) \, dx$ converges.  
**Error Bound:** $R_n \leq \int_{n}^{\infty} f(x) \, dx$.

### 4. Convergence Test Summarized Test Reference Comparison, Ratio, and Root Tests (§11.4 – 11.6)
* **Comparison:** Compare "messy" series to $p$-series or geometric series.
* **Ratio Test:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$.
    * $L < 1$ (Abs. Conv), $L > 1$ (Div), $L = 1$ (Inconclusive).
* **Root Test:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.
1.  **Divergence Test:** If $\lim_{n \to \infty} a_n \neq 0$, then $\sum a_n$ Diverges.
2.  **Integral Test:** If $f(x)$ is positive, continuous, and decreasing, then $\sum_{n=k}^{\infty} a_n$ and $\int_{k}^{\infty} f(x) \, dx$ behave the same (**both converge or both diverge**).
3.  **Direct Comparison Test:** If $0 < a_n \leq b_n$:
    * $\sum b_n$ (larger series) **converges** $\implies \sum a_n$ **converges**.
    * $\sum a_n$ (smaller series) **diverges** $\implies \sum b_n$ **diverges**.
4.  **Limit Comparison Test (LCT):** If $L = \lim_{n \to \infty} \frac{a_n}{b_n}$ is finite and positive ($L > 0$), both behave the same.
* **Condition:** Let $L = \lim_{n\to\infty} \frac{a_n}{b_n}$. If $L$ is a **finite, positive number ($L>0$)**, then $\sum a_n$ and $\sum b_n$ **either both converge or both diverge**.
* **Note:** Requires $a_n > 0$ and $b_n > 0$.
6.  **Ratio Test:** $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$. Conv if $L < 1$, Div if $L > 1$.
* **Condition:** Calculate $L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right|$.
    * If $L < 1$, the series **converges absolutely**.
    * If $L > 1$, the series **diverges**.
    * If $L=1$, the test is **inconclusive**.
7.  **Root Test:** $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$. Conv if $L < 1$, Div if $L > 1$.
* **Condition:** Calculate $L = \lim_{n\to\infty} \sqrt[n]{|a_n|}$.
    * If $L < 1$, the series **converges absolutely**.
    * If $L > 1$, the series **diverges**.
    * If $L=1$, the test is **inconclusive**.
8.  **Alternating Series Test (AST):** For $\sum (-1)^n b_n$, converges if $b_n \to 0$ and $b_n$ is decreasing.
    * **Remainder:** $|R_N| = |S - S_N| \leq b_{N+1}$.
* **Applies to:** $\sum_{n=1}^\infty (-1)^{n}b_n$ or $\sum_{n=1}^\infty (-1)^{n-1}b_n$, where $b_n > 0$.
* **Conditions for Convergence:** The series converges if **both** conditions are met:
    1.  $\lim_{n\to\infty} b_n = 0$
    2.  $b_{n+1} \leq b_n$ (the terms are decreasing in magnitude)
* **Alternating Series Remainder:** The error $|R_N|$ in using $S_N$ to approximate the sum $S$ is bounded by the magnitude of the next term: $|R_N| = |S - S_N| \leq b_{N+1}$.
---

## 🧐 Comprehensive Convergence Test Checklist for $\sum a_n$

### Step 1: The Divergence Test (The First Check)
**Goal:** To quickly determine if the series must diverge.  
**Check:** Calculate $\lim_{n \to \infty} a_n$.  
**Result:**
* If $\lim_{n \to \infty} a_n \neq 0$ (or the limit does not exist), then the series diverges. **Stop here.**
* If $\lim_{n \to \infty} a_n = 0$, the test is inconclusive. Proceed to Step 2. (Note: Skip this initial limit calculation and go straight to the Ratio/Root Test if $a_n$ contains factorials or exponents of $n$).

### Step 2: Test for Absolute Convergence
Absolute convergence means the series $\sum |a_n|$ converges. If this series converges, the original series $\sum a_n$ is absolutely convergent and therefore converges.

1.  **Form the Absolute Series:** Consider the series of absolute values, $\sum |a_n|$.
2.  **Apply Tests for Absolute Convergence:** Use one of the following tests on $\sum |a_n|$:

#### A. Ratio Test or Root Test
(For terms involving $n!$, products of functions, or $n$ in the exponent)
* **Ratio Test:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$.
* **Root Test:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.
* **Result:**
    * If $L < 1$, the series $\sum |a_n|$ converges, so $\sum a_n$ is absolutely convergent. **Stop here.**
    * If $L > 1$ or $L = \infty$, the series diverges. **Stop here.**
    * If $L = 1$, inconclusive. Try Comparison or Integral Test.

#### B. Comparison Tests
(Useful when $|a_n|$ is similar to a known series)
* **Direct Comparison Test (DCT):** Use if the inequality is simple (e.g., $n^2+5 > n^2 \implies \frac{1}{n^2+5} < \frac{1}{n^2}$). Requires finding a convergent $b_n \geq |a_n|$ or divergent $d_n \leq |a_n|$.
* **Limit Comparison Test (LCT):** Most common for rational/algebraic functions. Calculate $L = \lim_{n \to \infty} \frac{|a_n|}{b_n}$. If $0 < L < \infty$, then $\sum |a_n|$ and $\sum b_n$ share the same behavior.

#### C. Integral Test
(Used when $f(x)$ is continuous, positive, decreasing, and easily integrable)
* **Check:** Consider $f(x) = |a_x|$. The series $\sum |a_n|$ converges if and only if $\int_{1}^{\infty} f(x) \, dx$ is finite.

### Step 3: Test for Conditional Convergence (If Step 2 Fails)
This applies if $\sum |a_n|$ diverged but the original $\sum a_n$ is an **Alternating Series** (e.g., $\sum (-1)^n b_n$).
* **Apply Alternating Series Test (AST):** Check two conditions for $b_n = |a_n|$:
    1. $b_n$ is decreasing ($b_{n+1} \leq b_n$).
    2. $\lim_{n \to \infty} b_n = 0$.
* **Result:** If both met, the series converges **conditionally**. If the test fails, the series **diverges**.

---

## II. Power Series & Representations (§11.8 – 11.9)

### 1. Radius ($R$) and Interval ($I$) of Convergence
1.  Apply the **Ratio Test** to the whole term (including $x$).
2.  Set $L < 1$ and solve for $|x - a| < R$.
3.  **Endpoint Check:** You must test $x = a-R$ and $x = a+R$ separately.

### 2. Geometric Power Series
Use the template:
$$\frac{1}{1-u} = \sum_{n=0}^{\infty} u^n, \quad |u| < 1$$

### Analysis Tip: The "Hierarchy of Growth"
$$\ln(n) \ll n^p \ll a^n \ll n! \ll n^n$$
---

## III. Taylor and Maclaurin Series (§11.10 – 11.11)

### 1. General Formula
* **Taylor (at $a$):** $\sum \frac{f^{(n)}(a)}{n!} (x-a)^n$
* **Maclaurin (at $0$):** $\sum \frac{f^{(n)}(0)}{n!} x^n$

### 2. Taylor’s Inequality (Accuracy)
$$|R_n(x)| \leq \frac{M}{(n+1)!} |x - a|^{n+1}$$
* **$M$** is the max value of $|f^{(n+1)}(t)|$ for $t$ between $x$ and $a$.

### 3. Common Maclaurin Series
| Function | Series | Convergence |
| :--- | :--- | :--- |
| $e^x$ | $\sum \frac{x^n}{n!}$ | $R = \infty$ |
| $\sin(x)$ | $\sum (-1)^n \frac{x^{2n+1}}{(2n+1)!}$ | $R = \infty$ |
| $\cos(x)$ | $\sum (-1)^n \frac{x^{2n}}{(2n)!}$ | $R = \infty$ |

### **Known Maclaurin Series**
| Function | Sigma Notation (Power Series) | First Few Terms | ROC |
| --- | --- | --- | --- |
| **Geometric** | Σ xⁿ | 1 + x + x² + x³ + ... | R = 1 |
| **eˣ** | Σ xⁿ / n! | 1 + x + x²/2! + x³/3! + ... | R = ∞ |

---

## 🧊 Section 3: 3D Geometry & Vectors
## 🧊 Section 3: 3D Geometry & Vectors

### Vector Operations
* **Magnitude:** $|\mathbf{v}| = \sqrt{v_1^2 + v_2^2 + v_3^2}$
* **Unit Vector:** $\mathbf{u} = \frac{\mathbf{v}}{|\mathbf{v}|}$
* **Dot Product:** $\mathbf{u} \cdot \mathbf{v} = u_1v_1 + u_2v_2 + u_3v_3$
* **Cross Product:** $\mathbf{u} \times \mathbf{v} = \langle u_2v_3 - u_3v_2, u_3v_1 - u_1v_3, u_1v_2 - u_2v_1 \rangle$
* **Area of Parallelogram:** $|\mathbf{u} \times \mathbf{v}|$
* **Volume of Parallelepiped:** $|\mathbf{u} \cdot (\mathbf{v} \times \mathbf{w})|$

### Lines and Planes
* **Line Equation:** $\mathbf{r}(t) = P_0 + t\langle d_1, d_2, d_3 \rangle$
* **Plane Equation:** $a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$
    * *Note: $\langle a, b, c \rangle$ is the Normal Vector.*
* **Distance (Point to Plane):** $D = \frac{|ax_1 + by_1 + cz_1 + d|}{\sqrt{a^2 + b^2 + c^2}}$

### The Parallelogram Law
**Formula:** $|\mathbf{u} + \mathbf{v}|^2 + |\mathbf{u} - \mathbf{v}|^2 = 2|\mathbf{u}|^2 + 2|\mathbf{v}|^2$

### **Vector Operations**
* **Magnitude:** |v| = √(v₁² + v₂² + v₃²)
* **Unit Vector:** v / |v|
* **Dot Product:** u₁v₁ + u₂v₂ + u₃v₃
* **Cross Product:** ⟨u₂v₃-u₃v₂, u₃v₁-u₁v₃, u₁v₂-u₂v₁⟩
* **Area of Parallelogram:** Magnitude of the cross product: |u × v|
* **Volume of Parallelepiped:** Absolute value of triple product: |u · (v × w)|

### **Lines and Planes**
* **Line Equation:** r(t) = P₀ + t⟨d₁, d₂, d₃⟩
* **Plane Equation:** a(x - x₀) + b(y - y₀) + c(z - z₀) = 0
  * *Note:* ⟨a, b, c⟩ is the Normal Vector.
* **Distance (Point to Plane):** D = |ax₁ + by₁ + cz₁ + d| / √(a² + b² + c²)

### **The Parallelogram Law**
* **Formula:** |u + v|² + |u - v|² = 2|u|² + 2|v|²

---
