## 📝 Comprehensive Calculus II Guide: Sequences, Series, & Power Series

### **I. Sequences ($\{a_n\}$) & Preliminary Tests**

| Concept | Condition/Test | Formula/Notes |
| :--- | :--- | :--- |
| **Limit** (Convergence) | Converges if $\lim_{n \to \infty} a_n = L$ (a finite number). |
| **Monotonic Convergence Thm.** | A bounded, monotonic sequence **must** converge. |
| **$n^{th}$-Term Test** (Divergence Test) | If $\lim_{n \to \infty} a_n \neq 0$, the series **Diverges**. |
| **CAUTION** | If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**. |

---

### **II. Fundamental Series Types ($\sum_{n=1}^\infty a_n$)**

| Series Type | General Form | Convergence Condition(s) | Key Test/Sum Formula |
| :--- | :--- | :--- | :--- |
| **Geometric Series** | $\sum_{n=0}^{\infty} ar^n$ | Converges if the common ratio $|r| < 1$. | Sum is $S = \frac{a}{1-r}$. |
| **$p$-Series** | $\sum_{n=1}^{\infty} \frac{1}{n^p}$ | Converges if the exponent **$p > 1$**. | Diverges if $p \le 1$. |
| **Harmonic Series** | $\sum_{n=1}^{\infty} \frac{1}{n}$ | **Always Diverges.** | Special case of $p$-series where $p=1$. |
| **Telescoping Series** | $\sum_{n=1}^{\infty} (b_n - b_{n+1})$ (after partial fractions) | Converges if $\lim_{N \to \infty} S_N$ exists. | Find $S_N$, then take $\lim_{N \to \infty} S_N$. |

---

### **III. Convergence Tests for $\sum_{n=1}^\infty a_n$**

| Test Name | When to Use | Condition for Convergence | Condition for Divergence |
| :--- | :--- | :--- | :--- |
| **Integral Test** | $a_n = f(n)$ is positive, continuous, and decreasing. | $\int_1^\infty f(x) \, dx$ converges. | $\int_1^\infty f(x) \, dx$ diverges. |
| **Limit Comparison Test (LCT)** | $a_n$ and $b_n$ are positive and similar. | $\lim_{n \to \infty} \frac{a_n}{b_n} = L > 0$. If $\sum b_n$ converges, so does $\sum a_n$. | $\lim_{n \to \infty} \frac{a_n}{b_n} = L > 0$. If $\sum b_n$ diverges, so does $\sum a_n$. |
| **Alternating Series Test (AST)** | Series alternates sign: $\sum (-1)^n b_n$ where $b_n > 0$. | Both must hold: 1) $\lim_{n \to \infty} b_n = 0$ **AND** 2) $b_{n+1} \le b_n$. | Fails either of the two conditions. |
| **Ratio Test** | $a_n$ involves factorials ($n!$) or exponents ($r^n$). | $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = L < 1$. | $L > 1$ or $L = \infty$. |
| **Root Test** | $a_n$ involves $n$-th power: $(\dots)^n$. | $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} = L < 1$. | $L > 1$ or $L = \infty$. |

> **Note:** If $L=1$ in the Ratio or Root Test, the test is **inconclusive**.

---

### **IV. Power Series, Taylor Series, and Maclaurin Series**

#### **A. Power Series and Convergence**

A power series centered at $a$ has the form $\sum_{n=0}^{\infty} c_n (x-a)^n$.

1.  **Radius of Convergence ($R$):** Found by applying the **Ratio Test** to $\sum_{n=0}^{\infty} \left| c_n (x-a)^n \right|$.
    $$\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = L \cdot |x-a|$$
    Set $L \cdot |x-a| < 1$ and solve for $|x-a| < R$.

2.  **Interval of Convergence (IOC):** The interval $(a-R, a+R)$, plus the two endpoints.
    * **Crucial Step:** The endpoints $x = a-R$ and $x = a+R$ **must** be tested individually using any of the convergence tests (AST, $p$-Series, etc.) to determine if the series converges at those points.

#### **B. Taylor and Maclaurin Series**

| Series Type | Definition (Formula) | Center |
| :--- | :--- | :--- |
| **Taylor Series** | $$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$$ | $x=a$ |
| **Maclaurin Series** | $$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$ | $x=0$ |

#### **C. Common Maclaurin Series**

| Function $f(x)$ | Maclaurin Series | IOC ($R$) |
| :--- | :--- | :--- |
| **Geometric** | $\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n$ | $(-1, 1)$, $R=1$ |
| **$e^x$** | $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\sin(x)$** | $\sin(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\cos(x)$** | $\cos(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\arctan(x)$** | $\arctan(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$ | $[-1, 1]$, $R=1$ |
