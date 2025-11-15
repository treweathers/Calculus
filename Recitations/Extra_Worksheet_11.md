
## 📋 Problem Set Guide

| Original Problem | New Similar Problem |
| :--- | :--- |
| **(1) Taylor Polynomial & Error:** Approximate $f(x) = x \ln(x)$ by $T_3(x)$ at $a=1$ in $[0.5, 1.5]$. Use Taylor's inequality to estimate the accuracy. | **(1) New Taylor Polynomial & Error:** Approximate $f(x) = \sin(x)$ by its Taylor polynomial of degree 4 at $a = \frac{\pi}{4}$ in the interval $[\frac{\pi}{8}, \frac{7\pi}{8}]$. Use Taylor's inequality to estimate the accuracy of the approximation $f(x) \approx T_4(x)$ when $x$ lies in the given interval. |
| **(2) Maclaurin by Definition & $R$:** Find the Maclaurin series expansion of $f(x) = \ln(1 + x)$ and $f(x) = 2^x$ using the definition. Find the radius of convergence ($R$) of each. | **(2) New Maclaurin by Definition & $R$:** Find the Maclaurin series expansion of $f(x) = \frac{1}{1-x}$ and of $f(x) = \sinh(x)$ using the definition of Maclaurin series. Find the radius of convergence of each. |
| **(3) Taylor Series & Interval:** Find the Taylor series expansion of $f(x) = \cos(x)$ at $a=\frac{\pi}{2}$ and its interval of convergence. | **(3) New Taylor Series & Interval:** Find the Taylor series expansion of $f(x) = \ln(x)$ at $a=2$ and its interval of convergence. |
| **(4) Integral as Series & Definite Integral:** Express $\int x^2 e^{-x^2} dx$ as an infinite series, then evaluate $\int_0^{0.5} x^2 e^{-x^2} dx$ to within $0.001$. | **(4) New Integral as Series & Definite Integral:** Express the indefinite integral $\int \frac{\sin(x)}{x} dx$ as an infinite series and then evaluate the definite integral $\int_0^{0.1} \frac{\sin(x)}{x} dx$ to within an accuracy of $0.0001$. |
| **(5) Limit by Power Series:** Use power series to evaluate $\lim_{x\to 0} \frac{x^3 - 3x + 3 \tan^{-1}(x)}{x^5}$. | **(5) New Limit by Power Series:** Use power series to evaluate the limit $\lim_{x\to 0} \frac{e^{x^2} - 1 - x^2}{x^4}$. |
| **(6) Sum of Series as Function:** Find the sum of the series $\sum_{n=1}^\infty \frac{(-1)^{n-1} 3^n}{n 5^n}$ as the value of a familiar function. | **(6) New Sum of Series as Function:** Find the sum of the series $\sum_{n=1}^\infty \frac{(-1)^{n} \pi^{2n+1}}{(2n+1)!}$ as the value of a familiar function. |

---

## 🧠 Additional Practice Problems

### 1. New Taylor Polynomial & Error (Approximation of $\sin(x)$)

**Problem:** Approximate $f(x) = \sin(x)$ by its Taylor polynomial of degree 4 ($T_4(x)$) at $a = \frac{\pi}{4}$ in the interval $[\frac{\pi}{8}, \frac{7\pi}{8}]$. Use Taylor's inequality to estimate the accuracy of the approximation $f(x) \approx T_4(x)$ when $x$ lies in the given interval.

**Steps Required:**
1.  Calculate $f^{(n)}(x)$ for $n=0$ to $n=4$.
2.  Evaluate $f^{(n)}(\frac{\pi}{4})$ for $n=0$ to $n=4$.
3.  Construct $T_4(x)$ using the Taylor formula.
4.  Determine the maximum value of the fifth derivative, $\mathbf{M} = \max |f^{(5)}(x)|$ on the interval $[\frac{\pi}{8}, \frac{7\pi}{8}]$.
5.  Apply Taylor's Inequality: $|R_4(x)| \le \frac{M}{5!} |x-a|^5$. Find the maximum error by maximizing $|x-a|^5$.

---

### 2. New Maclaurin by Definition & Radius of Convergence ($R$)

**Problem:** Find the Maclaurin series expansion of $f(x) = \frac{1}{1-x}$ and of $f(x) = \sinh(x)$ using the **definition** of Maclaurin series. Find the radius of convergence of each.

**Steps Required (for each function):**
1.  Calculate $f^{(n)}(x)$ for the first few derivatives ($n=0, 1, 2, 3, \dots$).
2.  Evaluate $f^{(n)}(0)$ to find the pattern for the general term.
3.  Substitute $f^{(n)}(0)$ into the Maclaurin formula $\sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!} x^n$.
4.  Use the **Ratio Test** on the resulting series to find the radius of convergence $R$.

---

### 3. New Taylor Series & Interval of Convergence

**Problem:** Find the Taylor series expansion of $f(x) = \ln(x)$ at $a=2$ and determine its interval of convergence.

**Steps Required:**
1.  Calculate $f^{(n)}(x)$ for the first few derivatives and find a formula for the general term $f^{(n)}(x)$.
2.  Evaluate $f^{(n)}(2)$ to find the general coefficient $\frac{f^{(n)}(2)}{n!}$.
3.  Write the Taylor series: $\sum_{n=0}^\infty \frac{f^{(n)}(2)}{n!} (x-2)^n$.
4.  Use the **Ratio Test** to find the radius of convergence $R$ and the open interval of convergence.
5.  **Check the endpoints** of the interval to determine whether the series converges at those points, giving the full interval of convergence.

---

### 4. New Integral as Series & Definite Integral Approximation

**Problem:** Express the indefinite integral $\int \frac{\sin(x)}{x} dx$ as an infinite series and then evaluate the definite integral $\int_0^{0.1} \frac{\sin(x)}{x} dx$ to within an accuracy of **$0.0001$**.

**Steps Required:**
1.  Recall the Maclaurin series for $\sin(x)$.
2.  Divide the $\sin(x)$ series by $\mathbf{x}$ to get the series for the integrand $\frac{\sin(x)}{x}$.
3.  Integrate the resulting series term-by-term to express $\int \frac{\sin(x)}{x} dx$ as an infinite series.
4.  Evaluate the integrated series at the limits $[0, 0.1]$ to get an **alternating series**.
5.  Use the **Alternating Series Estimation Theorem** to find the minimum number of terms needed such that the magnitude of the first neglected term ($b_{N+1}$) is less than the error tolerance $\mathbf{0.0001}$.
6.  Calculate the partial sum $S_N$ to get the final approximation.

---

### 5. New Limit by Power Series

**Problem:** Use power series to evaluate the limit $\lim_{x\to 0} \frac{e^{x^2} - 1 - x^2}{x^4}$.

**Steps Required:**
1.  Recall the Maclaurin series for $\mathbf{e^u}$.
2.  Substitute $\mathbf{u=x^2}$ into the $e^u$ series to find the series for $e^{x^2}$.
3.  Substitute the $e^{x^2}$ series into the numerator: $e^{x^2} - 1 - x^2$. (The first two terms should cancel).
4.  Divide the simplified numerator series by the denominator $\mathbf{x^4}$.
5.  Evaluate the limit as $x \to 0$ (the result will be the constant term of the resulting series).

---

### 6. New Sum of Series as Familiar Function Value

**Problem:** Find the sum of the series $\sum_{n=0}^\infty \frac{(-1)^{n} \pi^{2n+1}}{(2n+1)!}$ as the value of a familiar function.

**Steps Required:**
1.  Recall the Maclaurin series formula for a familiar function that uses $\frac{(-1)^{n}}{(\text{odd}!)}$. The only standard one is $\mathbf{\sin(u)}$.
2.  Compare the given series to the standard series for $\sin(u)$:
    $$\sin(u) = \sum_{n=0}^\infty \frac{(-1)^n u^{2n+1}}{(2n+1)!}$$
3.  Identify the value of **$u$** by matching the power of $u$ with the power of $\pi$ in the given series.
4.  The sum of the series is $\mathbf{\sin(u)}$.
