## 📚 Sequences and Series Formula Sheet & Guide

### **I. Sequences ($\{a_n\}$)**

| Concept | Condition/Test | Formula/Notes |
| :--- | :--- | :--- |
| **Limit** | Converges if... | $\lim_{n \to \infty} a_n = L$ (a finite number) |
| **Divergence** | Diverges if... | $\lim_{n \to \infty} a_n = \pm \infty$ or does not exist (DNE) |
| **Monotonic** | Increasing | $a_{n+1} \geq a_n$ for all $n$ |
| | Decreasing | $a_{n+1} \leq a_n$ for all $n$ |
| **Bounded** | Bounded Above | $a_n \leq M$ for some number $M$ |
| | Bounded Below | $a_n \geq m$ for some number $m$ |
| **Key Theorem** | Monotonic Sequence Thm. | A bounded, monotonic sequence **must** converge. |

### **II. Series ($\sum_{n=1}^\infty a_n$)**

| Type of Series | Formula/Condition | Notes/Convergence |
| :--- | :--- | :--- |
| **Geometric Series** | $\sum_{n=0}^\infty ar^n$ | Converges if $|r| < 1$. Sum is $S = \frac{a}{1-r}$ |
| **Telescoping Series** | Terms cancel out (use partial fractions) | Converges to the limit of the partial sums $\lim_{N \to \infty} S_N$ |
| **$p$-Series** | $\sum_{n=1}^\infty \frac{1}{n^p}$ | Converges if $p > 1$. Diverges if $p \leq 1$. |
| **Harmonic Series** | $\sum_{n=1}^\infty \frac{1}{n}$ | A special case of $p$-series ($p=1$). **Always Diverges.** |

### **III. Convergence Tests**

| Name of Test | When to Use | Conclusion/Condition |
| :--- | :--- | :--- |
| **$n^{th}$-Term Test** (Divergence Test) | *Always* your first check. | If $\lim_{n \to \infty} a_n \neq 0$, the series **Diverges**. **CAUTION:** If the limit *is* $0$, the test is inconclusive! |
| **Integral Test** | For $a_n = f(n)$ where $f(x)$ is positive, continuous, and decreasing. | $\sum a_n$ converges if and only if $\int_1^\infty f(x) \, dx$ converges. |
| **Comparison Test** | For series with all positive terms, similar to a $p$-series or geometric series. | **$0 < a_n \leq b_n$:** If $\sum b_n$ converges, then $\sum a_n$ converges. **$0 < b_n \leq a_n$:** If $\sum b_n$ diverges, then $\sum a_n$ diverges. |
| **Limit Comparison Test** | For series similar to a known series (LCT is often easier than CT). | $\lim_{n \to \infty} \frac{a_n}{b_n} = L$ where $L$ is a finite, positive number ($L>0$). Then $\sum a_n$ and $\sum b_n$ **both do the same thing** (both converge or both diverge). |
| **Alternating Series Test (AST)** | For series with alternating signs, e.g., $\sum (-1)^n b_n$ where $b_n > 0$. | Converges if **both** conditions are met: 1) $\lim_{n \to \infty} b_n = 0$ **AND** 2) $b_{n+1} \leq b_n$ (terms are decreasing). |
| **Ratio Test** | When $a_n$ involves factorials ($n!$) or powers of $n$ in the exponent ($2^n$). | $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = L$: If $L < 1$, **Converges Absolutely**. If $L > 1$, **Diverges**. If $L = 1$, **Inconclusive**. |
| **Root Test** | When $a_n$ involves the entire expression raised to the power of $n$. | $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} = L$: If $L < 1$, **Converges Absolutely**. If $L > 1$, **Diverges**. If $L = 1$, **Inconclusive**. |

### **IV. Absolute vs. Conditional Convergence**

| Type of Convergence | Definition |
| :--- | :--- |
| **Absolute Convergence** | $\sum a_n$ converges **and** $\sum \left| a_n \right|$ converges. |
| **Conditional Convergence** | $\sum a_n$ converges (by AST) **but** $\sum \left| a_n \right|$ diverges. |