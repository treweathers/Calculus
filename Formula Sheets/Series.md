## Series Reference Chart (Calculus II)

| Series Type | General Form | Convergence Condition(s) | Key Test/Note |
| :--- | :--- | :--- | :--- |
| **Geometric Series** | $\sum_{n=0}^{\infty} ar^n = a + ar + ar^2 + \dots$ | Converges if the absolute value of the common ratio, $|r|$, is **less than 1** ($|r| < 1$). | Sum is $S = \frac{a}{1-r}$ when it converges. |
| **$p$-Series** | $\sum_{n=1}^{\infty} \frac{1}{n^p}$ | Converges if the exponent **$p$ is greater than 1** ($p > 1$). | Diverges if $p \le 1$. |
| **Harmonic Series** | $\sum_{n=1}^{\infty} \frac{1}{n}$ | **Always Diverges** | This is the specific case of the $p$-series where $p=1$. |
| **Alternating Series** | $\sum_{n=1}^{\infty} (-1)^{n-1} a_n$ or $\sum_{n=1}^{\infty} (-1)^{n} a_n$, where $a_n > 0$. | Converges if: 1. $a_{n+1} \le a_n$ (terms are non-increasing), AND 2. $\lim_{n \to \infty} a_n = 0$. | Use the **Alternating Series Test (AST)**. |
| **Telescoping Series** | $\sum_{n=1}^{\infty} (b_n - b_{n+1})$ (or similar form after partial fraction decomposition). | Converges if the limit of the partial sums, $\lim_{N \to \infty} S_N$, exists. | Check convergence by evaluating the limit of the **$N$-th partial sum ($S_N$)** after terms cancel. |
| **Taylor/Maclaurin Series** | $\sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$ (Taylor), or $\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$ (Maclaurin, where $a=0$). | Depends on the specific function $f(x)$ and interval of convergence. | Represents a function $f(x)$ as a power series centered at $a$. |
| **General Series** | $\sum_{n=1}^{\infty} a_n$ | Varies; use one of the convergence tests (e.g., Ratio, Root, Comparison, Integral Test). | First, check the **$n$-th Term Test for Divergence** ($\lim_{n \to \infty} a_n \ne 0 \implies$ Diverges). |

***

### Quick Notes on Convergence Tests

While the chart above focuses on specific *types* of series, remember that **Convergence Tests** are used to determine if a *General Series* converges or diverges. The main tests usually covered are:

* **$n$-th Term Test for Divergence**: If $\lim_{n \to \infty} a_n \ne 0$, the series diverges. (If the limit is $0$, the test is inconclusive).
* **Integral Test**: For a series with positive, decreasing terms, the series and the integral $\int_{1}^{\infty} f(x) dx$ either both converge or both diverge.
* **Comparison Tests (Direct and Limit)**: Compare the given series to a known series (like a $p$-series or Geometric series).
* **Ratio Test**: Useful for series involving factorials ($n!$) or exponentials.
* **Root Test**: Useful for series where the entire term is raised to the $n$-th power.
* **Alternating Series Test (AST)**: Used specifically for alternating series (as noted in the chart).
