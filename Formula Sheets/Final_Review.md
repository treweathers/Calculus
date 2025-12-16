# 🧮 Calculus II Final Review Sheet
# 🧮 Calculus II Final Review Sheet

## Section 1: Midterm I Review (Integration Techniques)
*Refer to previous study guide for Integration by Parts, Trig Sub, and Partial Fractions.*

---

## ♾️ Section 2: Infinite Series

### I. Series Basics & Convergence Tests (§11.2 – 11.6)

#### 1. Partial Sums ($s_n$) vs. Terms ($a_n$)
If given the sum formula $s_n$:
* **Find $a_n$:** $a_n = s_n - s_{n-1}$
* **Find the total sum:** $S = \lim_{n \to \infty} s_n$

#### 2. The Big Three Early Tests
| Test | Condition | Conclusion |
| :--- | :--- | :--- |
| **Divergence Test** | $\lim_{n \to \infty} a_n \neq 0$ | Series **Diverges**. |
| **Geometric Series** | $\sum ar^{n-1}$ | Conv. if $|r| < 1$. Sum $S = \frac{a}{1-r}$. |
| **Telescoping Series** | Terms cancel | $S = \lim_{N \to \infty} s_N$ (Identify survivors). |

#### 3. Integral Test & Remainder (§11.3)
* **Conditions:** $f(x)$ must be positive, continuous, and decreasing on $[1, \infty)$.
* **Rule:** $\sum a_n$ converges if and only if $\int_1^{\infty} f(x) \, dx$ converges.
* **Error Bound:** $R_n \le \int_n^{\infty} f(x) \, dx$.


---

### 🧐 Comprehensive Convergence Test Checklist for $\sum a_n$

#### Step 1: The Divergence Test (The First Check)
Calculate $\lim_{n \to \infty} a_n$:
* If $\lim_{n \to \infty} a_n \neq 0$, the series **diverges**.
* If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**.

#### Step 2: Test for Absolute Convergence ($\sum |a_n|$)
1. **Ratio/Root Test:** (Best for $n!$ or $a^n$)
   * $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$ or $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$
   * $L < 1 \implies$ **Abs. Convergent**; $L > 1 \implies$ **Divergent**.
2. **Limit Comparison Test (LCT):** (Best for rational/algebraic functions)
   * Pick $b_n$ (dominant terms). $L = \lim_{n \to \infty} \frac{|a_n|}{b_n}$. 
   * If $0 < L < \infty$, both behave the same.
3. **Integral Test:** Use if $a_n$ is easily integrable (e.g., involves $\ln n$).

#### Step 3: Conditional Convergence (If Step 2 Fails)
If $\sum |a_n|$ diverges but the series is alternating ($\sum (-1)^n b_n$):
1. **Alternating Series Test (AST):**
   * If $b_{n+1} \le b_n$ and $\lim_{n \to \infty} b_n = 0$, the series **converges conditionally**.
   * **AST Remainder:** $|R_N| \le b_{N+1}$.

---

### II. Power Series & Representations (§11.8 – 11.9)

#### 1. Radius ($R$) and Interval ($I$) of Convergence
1. Apply **Ratio Test** to the whole term: $L = \lim_{n \to \infty} | \frac{a_{n+1}}{a_n} |$.
2. Solve $L < 1$ to find the inequality $|x - a| < R$.
3. **Endpoint Check:** Test $x = a-R$ and $x = a+R$ individually in the original $\sum a_n$.

#### 2. Geometric Template
$$\frac{1}{1-u} = \sum_{n=0}^{\infty} u^n, \quad |u| < 1$$

#### 📈 Hierarchy of Growth
$$\ln(n) \ll n^p \ll a^n \ll n! \ll n^n$$

---

### III. Taylor and Maclaurin Series (§11.10 – 11.11)

#### 1. General Formulas
* **Taylor Series (at $a$):** $\sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!} (x-a)^n$
* **Maclaurin Series (at $0$):** $\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!} x^n$

#### 2. Taylor’s Inequality (Accuracy)
$$|R_n(x)| \le \frac{M}{(n+1)!} |x - a|^{n+1}$$
* $M$ is the max value of $|f^{(n+1)}(t)|$ for $t$ between $x$ and $a$.

#### 3. Known Maclaurin Series
| Function | Sigma Notation | Expansion | ROC |
| :--- | :--- | :--- | :--- |
| $\frac{1}{1-x}$ | $\sum_{n=0}^{\infty} x^n$ | $1 + x + x^2 + \dots$ | $R=1$ |
| $e^x$ | $\sum_{n=0}^{\infty} \frac{x^n}{n!}$ | $1 + x + \frac{x^2}{2!} + \dots$ | $R=\infty$ |
| $\sin(x)$ | $\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}$ | $x - \frac{x^3}{3!} + \dots$ | $R=\infty$ |
| $\cos(x)$ | $\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$ | $1 - \frac{x^2}{2!} + \dots$ | $R=\infty$ |



---

## 🧊 Section 3: 3D Geometry & Vectors

### 1. Vector Operations
* **Magnitude:** $|\vec{v}| = \sqrt{v_1^2 + v_2^2 + v_3^2}$
* **Dot Product:** $\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + u_3v_3 = |\vec{u}||\vec{v}|\cos(\theta)$
* **Cross Product:** $\vec{u} \times \vec{v} = \langle u_2v_3-u_3v_2, u_3v_1-u_1v_3, u_1v_2-u_2v_1 \rangle$
* **Area of Parallelogram:** $A = |\vec{u} \times \vec{v}|$
* **Volume of Parallelepiped:** $V = |\vec{u} \cdot (\vec{v} \times \vec{w})|$

### 2. Lines and Planes
* **Line Equation:** $\vec{r}(t) = P_0 + t\vec{v}$
* **Plane Equation:** $a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$ (where $\vec{n} = \langle a,b,c \rangle$)
* **Distance (Point to Plane):** $D = \frac{|ax_1 + by_1 + cz_1 + d|}{\sqrt{a^2 + b^2 + c^2}}$

### 3. The Parallelogram Law
$$|\vec{u} + \vec{v}|^2 + |\vec{u} - \vec{v}|^2 = 2|\vec{u}|^2 + 2|\vec{v}|^2$$
## Section 1: See Study Guide from Midterm I

## ♾️ Section 2: Infinite Series
# Calculus II: Midterm II Review Guide

## I. Series Basics & Convergence Tests (§11.2 – 11.6)

### 1. Partial Sums ($s_n$) vs. Terms ($a_n$)
If you are given the sum formula $s_n$:
* **Find $a_n$:** $a_n = s_n - s_{n-1}$.
* **Find the total sum:** $S = \lim_{n \to \infty} s_n$.

### 2. The Big Three Early Tests
| Test | Condition | Conclusion |
| :--- | :--- | :--- |
| **Divergence Test** | $\lim_{n \to \infty} a_n \neq 0$ | Series **Diverges**. |
| **Geometric Series** | $\sum ar^{n-1}$ | Converges if $|r| < 1$. Sum $S = \frac{a}{1-r}$. |
| **Telescoping Series** | Terms cancel out | Write out first few partial sums and take the limit. |

### 3. Integral Test & Remainder (§11.3)
* **Conditions:** Function must be positive, continuous, and decreasing.
* **Rule:** $\sum a_n$ converges if and only if $\int_1^{\infty} f(x) dx$ converges.
* **Error Bound:** $R_n \leq \int_n^{\infty} f(x) dx$.

### 4. Comparison, Ratio, and Root Tests (§11.4 – 11.6)
* **Comparison:** Compare "messy" series to $p$-series or geometric series.
* **Ratio Test:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$.
    * $L < 1$ (Abs. Conv), $L > 1$ (Div), $L = 1$ (Inconclusive).
* **Root Test:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.

---

## 🧐 Comprehensive Convergence Test Checklist for $\sum a_n$

### Step 1: The **Divergence Test** (The First Check)

* **Goal:** To quickly determine if the series must **diverge**.
* **Check:** Calculate $\lim_{n \to \infty} a_n$.
* **Result:**
    * If $\lim_{n \to \infty} a_n \neq 0$ (or the limit does not exist), then the series **diverges**. Stop here.
    * If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**. Proceed to Step 2. (Note: Skip this initial limit calculation and go straight to the **Ratio/Root Test** if $a_n$ contains factorials or exponents of $n$).

---

### Step 2: Test for **Absolute Convergence**

Absolute convergence means the series $\sum |a_n|$ converges. If this series converges, the original series $\sum a_n$ is absolutely convergent and therefore converges.

* **Form the Absolute Series:** Consider the series of absolute values, $\sum |a_n|$.
* **Apply Tests for Absolute Convergence:** Use one of the following tests on $\sum |a_n|$:

#### A. **Ratio Test** or **Root Test** (For terms involving $n!$, products of functions, or $n$ in the exponent)

* **Ratio Test:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$.
* **Root Test:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.
* **Result (for either test):**
    * If $L < 1$, the series $\sum |a_n|$ **converges**, so $\sum a_n$ is **absolutely convergent** (and therefore convergent). Stop here.
    * If $L > 1$ or $L = \infty$, the series **diverges**. Stop here.
    * If $L = 1$, the test is **inconclusive**. Try a Comparison or Integral Test.

#### B. **Comparison Tests** (Useful when $|a_n|$ is similar to a known series)

* **Use when taking the absolute value is helpful:** This is particularly helpful when $|a_n|$ simplifies to a known convergent or divergent series (like a $p$-series or Geometric series).

* **Direct Comparison Test (DCT):**
    * **Use:** Only if the required **inequality is simple and obvious** (e.g., $n^2+5 > n^2 \implies \frac{1}{n^2+5} < \frac{1}{n^2}$).
    * **Requires:** Finding a convergent series $\sum b_n$ such that $|a_n| \le b_n$, or a divergent series $\sum d_n$ such that $|a_n| \ge d_n$.

* **Limit Comparison Test (LCT):**
    * **Use:** **Most commonly** for rational or algebraic functions. It's much easier as it avoids proving inequalities.
    * **Requires:** Find a known series $\sum b_n$ (usually the simplified dominant terms). Calculate $L = \lim_{n \to \infty} \frac{|a_n|}{b_n}$. If $0 < L < \infty$, then $\sum |a_n|$ and $\sum b_n$ have the **same convergence behavior**.

#### C. **Integral Test** (Used when $f(x)$ is continuous, positive, decreasing, and easily integrable)

* **Where it fits in:** The Integral Test is a comparison tool, best used when the term $a_n$ contains terms like $\ln n$ or complex functions that integrate cleanly using $u$-substitution.
* **Check:** Consider $f(x) = |a_x|$. The series $\sum |a_n|$ converges if and only if the improper integral $\int_1^\infty f(x) dx$ **converges** (is a finite number). If the integral **diverges**, the series also **diverges**. 

---

### Step 3: Test for **Conditional Convergence** (If Step 2 Fails)

This step only applies if:
1.  The series $\sum |a_n|$ **diverged** in Step 2.
2.  The original series $\sum a_n$ is an **Alternating Series** (terms must alternate sign, e.g., $\sum (-1)^n b_n$).

* **When the series fails absolute convergence tests:** This is precisely when you apply the **Alternating Series Test (AST)**—only if the series is alternating and you've confirmed $\sum |a_n|$ diverges.
* **Apply the Alternating Series Test:** For the series $\sum (-1)^n b_n$ (where $b_n = |a_n|$ is positive), check two conditions:
    1.  $b_n$ is **decreasing** (i.e., $b_{n+1} \le b_n$ for all $n$).
    2.  $\lim_{n \to \infty} b_n = 0$.
* **Result:** If **both conditions are met**, the series $\sum a_n$ **converges conditionally**.
* **Final Result:** If the series $\sum |a_n|$ **diverged** AND the **Alternating Series Test failed**, the series $\sum a_n$ **diverges**.

#### **1. Divergence Test ($n$-th Term Test)**
* **Condition:** If $\lim_{n\to\infty} a_n \neq 0$ (or DNE), then $\sum a_n$ **Diverges**.
* **Note:** If $\lim_{n\to\infty} a_n = 0$, the test is **inconclusive**.

#### **2. Integral Test**
* **Condition:** If $f(x)$ is positive, continuous, and decreasing on $[k, \infty)$, then $\sum_{n=k}^\infty a_n$ and $\int_k^\infty f(x) dx$ either **both converge or both diverge**.

#### **3. Comparison Test (Direct)**
* **Conditions:** Let $0 < a_n \leq b_n$.
    * If the larger series $\sum b_n$ **converges**, then $\sum a_n$ **converges**.
    * If the smaller series $\sum a_n$ **diverges**, then $\sum b_n$ **diverges**.
* **Note:** Requires non-negative terms.

#### **4. Limit Comparison Test (LCT)**
* **Condition:** Let $L = \lim_{n\to\infty} \frac{a_n}{b_n}$. If $L$ is a **finite, positive number ($L>0$)**, then $\sum a_n$ and $\sum b_n$ **either both converge or both diverge**.
* **Note:** Requires $a_n > 0$ and $b_n > 0$.

#### **5. Ratio Test**
* **Condition:** Calculate $L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right|$.
    * If $L < 1$, the series **converges absolutely**.
    * If $L > 1$, the series **diverges**.
    * If $L=1$, the test is **inconclusive**.

#### **6. Root Test**
* **Condition:** Calculate $L = \lim_{n\to\infty} \sqrt[n]{|a_n|}$.
    * If $L < 1$, the series **converges absolutely**.
    * If $L > 1$, the series **diverges**.
    * If $L=1$, the test is **inconclusive**.

#### **7. Alternating Series Test (AST)**
* **Applies to:** $\sum_{n=1}^\infty (-1)^{n}b_n$ or $\sum_{n=1}^\infty (-1)^{n-1}b_n$, where $b_n > 0$.
* **Conditions for Convergence:** The series converges if **both** conditions are met:
    1.  $\lim_{n\to\infty} b_n = 0$
    2.  $b_{n+1} \leq b_n$ (the terms are decreasing in magnitude)
* **Alternating Series Remainder:** The error $|R_N|$ in using $S_N$ to approximate the sum $S$ is bounded by the magnitude of the next term: $|R_N| = |S - S_N| \leq b_{N+1}$.

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
