# 🧮 Calculus II Final Review Sheet

## I. Series Basics & Convergence Tests (§11.2 – 11.6)

### 1. Partial Sums ($s_n$) vs. Terms ($a_n$)
If you are given the sum formula $s_n$:
* **Find $a_n$:** $a_n = s_n - s_{n-1}$.
* **Find the total sum:** $S = \lim_{n \to \infty} s_n$.

### 2. The Big Three Early Tests
* **Divergence Test**
    * **Condition:** $\lim_{n \to \infty} a_n \neq 0$
    * **Conclusion:** Series **Diverges**.

* **Geometric Series**
    * **Form:** $\sum ar^{n-1}$
    * **Condition:** Converges if $|r| < 1$.
    * **Sum Formula:** $S = \frac{a}{1-r}$

* **Telescoping Series**
    * **Condition:** Terms cancel out via partial fraction decomposition or subtraction.
    * **Method:** Write out the first few partial sums ($s_n$) and calculate $\lim_{n \to \infty} s_n$.

### 3. Integral Test & Remainder (§11.3)
**Conditions:** Function must be positive, continuous, and decreasing.  
**Rule:** $\sum a_n$ converges if and only if $\int_{1}^{\infty} f(x) \, dx$ converges.  
**Error Bound:** $R_n \leq \int_{n}^{\infty} f(x) \, dx$.

## 4. Convergence Test Summarized Test Reference

### Comparison, Ratio, and Root Tests (§11.4 – 11.6)
* **Comparison:** Compare "messy" series to $p$-series or geometric series.
* **Ratio Test:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$. $L < 1$ (Abs. Conv), $L > 1$ (Div), $L = 1$ (Inconclusive).
* **Root Test:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.

---

### Summarized Test Reference
1.  **Divergence Test:** If $\lim_{n \to \infty} a_n \neq 0$, then $\sum a_n$ **Diverges**.
2.  **Integral Test:** If $f(x)$ is positive, continuous, and decreasing, then $\sum_{n=k}^{\infty} a_n$ and $\int_{k}^{\infty} f(x) \, dx$ behave the same (both converge or both diverge).
3.  **Direct Comparison Test:** If $0 < a_n \leq b_n$:
    * $\sum b_n$ (larger series) converges $\implies \sum a_n$ converges.
    * $\sum a_n$ (smaller series) diverges $\implies \sum b_n$ diverges.
4.  **Limit Comparison Test (LCT):** * **Condition:** Let $L = \lim_{n \to \infty} \frac{a_n}{b_n}$. If $L$ is a finite, positive number ($L > 0$), then $\sum a_n$ and $\sum b_n$ either both converge or both diverge.
    * **Note:** Requires $a_n > 0$ and $b_n > 0$.
5.  **Ratio Test:** * **Condition:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$.
    * If $L < 1$, the series converges absolutely.
    * If $L > 1$, the series diverges.
    * If $L = 1$, the test is inconclusive.
6.  **Root Test:** * **Condition:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.
    * If $L < 1$, the series converges absolutely.
    * If $L > 1$, the series diverges.
    * If $L = 1$, the test is inconclusive.
7.  **Alternating Series Test (AST):** * **Applies to:** $\sum_{n=1}^{\infty} (-1)^n b_n$ or $\sum_{n=1}^{\infty} (-1)^{n-1} b_n$, where $b_n > 0$.
    * **Conditions for Convergence:** The series converges if **both** conditions are met:
        1.  $\lim_{n \to \infty} b_n = 0$
        2.  $b_{n+1} \leq b_n$ (the terms are decreasing in magnitude)
    * **Alternating Series Remainder:** The error $|R_N|$ in using $S_N$ to approximate the sum $S$ is bounded by the magnitude of the next term: $|R_N| = |S - S_N| \leq b_{N+1}$.

---
## 🧐 Comprehensive Convergence Test Checklist for $\sum a_n$

### Step 1: The Divergence Test (The First Check)
* **Goal:** To quickly determine if the series must diverge.
* **Check:** Calculate $\lim_{n \to \infty} a_n$.
* **Result:**
    * If $\lim_{n \to \infty} a_n \neq 0$ (or the limit does not exist), the series **diverges**. Stop here.
    * If $\lim_{n \to \infty} a_n = 0$, the test is inconclusive. Proceed to Step 2.

> **Note:** Skip the initial limit calculation and go straight to the Ratio/Root Test if $a_n$ contains factorials ($n!$) or exponents of $n$ (like $3^n$).

---

### Step 2: Test for Absolute Convergence
Absolute convergence means $\sum |a_n|$ converges. If it does, the original series $\sum a_n$ is automatically convergent.

1.  **Form the Absolute Series:** Consider the series of absolute values, $\sum |a_n|$.
2.  **Apply Tests for Absolute Convergence:**

#### A. Ratio Test or Root Test
> **Use for:** Terms involving $n!$, products of functions, or $n$ in the exponent.

* **Ratio Test:** $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$
* **Root Test:** $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$
* **Result:**
    * If $L < 1$, the series is **absolutely convergent**. Stop here.
    * If $L > 1$ or $L = \infty$, the series **diverges**. Stop here.
    * If $L = 1$, inconclusive. Try Comparison or Integral Test.

#### B. Comparison Tests
> **Use when:** $|a_n|$ looks similar to a known series (like a $p$-series or geometric series).

* **Direct Comparison Test (DCT):** Use if the inequality is simple.
    * *Example:* $n^2+5 > n^2 \implies \frac{1}{n^2+5} < \frac{1}{n^2}$.
* **Limit Comparison Test (LCT):** Best for rational or algebraic functions.
    * Calculate $L = \lim_{n \to \infty} \frac{|a_n|}{b_n}$. If $0 < L < \infty$, both series behave the same.

#### C. Integral Test
> **Use when:** $f(x)$ is continuous, positive, decreasing, and easily integrable (e.g., involves $\ln x$ or $u$-substitution).

* **Check:** $\sum |a_n|$ converges if and only if $\int_{1}^{\infty} f(x) \, dx$ is finite.

---

### Step 3: Test for Conditional Convergence (If Step 2 Fails)
Apply this **only** if $\sum |a_n|$ diverged but the original series $\sum a_n$ is an **Alternating Series**.

* **Apply Alternating Series Test (AST):** Check two conditions for $b_n = |a_n|$:
    1.  $b_n$ is decreasing ($b_{n+1} \leq b_n$).
    2.  $\lim_{n \to \infty} b_n = 0$.
* **Result:** If both are met, the series converges **conditionally**. If either fails, the series **diverges**.

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

### 3. Common Maclaurin Series/ **Known Maclaurin Series Details**
| Function | Sigma Notation | First Few Terms | ROC |
| :--- | :--- | :--- | :--- |
| Geometric | $\sum x^n$ | $1 + x + x^2 + x^3 + \dots$ | $R = 1$ |
| $e^x$ | $\sum \frac{x^n}{n!}$ | $1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots$ | $R = \infty$ |

---


---

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
