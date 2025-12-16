# Calculus II: Midterm II Review Guide

## I. Sequences and Decimal Conversion (§11.1)

### 1. Limits of Sequences
To find if a sequence $\{a_n\}$ converges:
* **The Goal:** Find $L = \lim_{n \to \infty} a_n$.
* **Method:** Treat $n$ as $x$ and use L'Hôpital's Rule if you encounter $\frac{\infty}{\infty}$.
* **Analysis:** If $L$ is a finite number, it **converges**. If it is $\pm \infty$ or oscillates, it **diverges**.

### 2. Recursive Sequences and Fish Populations
For a population $P_n$ where $P_n = rP_{n-1} + d$:
* **Finding terms:** Plug $P_0$ into the formula to find $P_1$, then $P_1$ to find $P_2$.
* **Finding the Limit ($L$):** If the limit exists, then as $n \to \infty$, $P_n \approx P_{n-1} \approx L$.
* **Equation:** Solve $L = rL + d$.
* **Shortcut:** $L = \frac{d}{1-r}$.

### 3. Decimal to Rational Number
To turn $0.\overline{12}$ into a fraction:
1.  Let $x = 0.1212...$
2.  Multiply $x$ by $10^k$ to move the decimal to the start of the repeating block.
3.  Multiply $x$ by $10^{k+m}$ to move the decimal one full block further.
4.  Subtract the two equations to cancel the infinite decimal and solve for $x$.

---

## II. Series Basics & Convergence Tests (§11.2 – 11.6)

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

## III. Power Series & Representations (§11.8 – 11.9)

### 1. Radius ($R$) and Interval ($I$) of Convergence
1.  Apply the **Ratio Test** to the whole term (including $x$).
2.  Set $L < 1$ and solve for $|x - a| < R$.
3.  **Endpoint Check:** You must test $x = a-R$ and $x = a+R$ separately.

### 2. Geometric Power Series
Use the template:
$$\frac{1}{1-u} = \sum_{n=0}^{\infty} u^n, \quad |u| < 1$$

---

## IV. Taylor and Maclaurin Series (§11.10 – 11.11)

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

---

### Analysis Tip: The "Hierarchy of Growth"
$$\ln(n) \ll n^p \ll a^n \ll n! \ll n^n$$
