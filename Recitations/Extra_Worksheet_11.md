
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
I'd be happy to! Providing the full solution breakdown for each new problem will make this a complete guide for you.

Here are the six new practice problems with detailed, step-by-step solutions for each, mirroring the format and techniques of your original set.

---

## 🧠 Additional Practice Problems with Full Solutions

### 1. New Taylor Polynomial & Error (Approximation of $\sin(x)$)

**Problem:** Approximate $f(x) = \sin(x)$ by its Taylor polynomial of degree 4 ($T_4(x)$) at $a = \frac{\pi}{4}$ in the interval $[\frac{\pi}{8}, \frac{7\pi}{8}]$. Use Taylor's inequality to estimate the accuracy of the approximation $f(x) \approx T_4(x)$ when $x$ lies in the given interval.

#### Solution 1: Taylor Polynomial $T_4(x)$

| $n$ | $f^{(n)}(x)$ | $f^{(n)}(\frac{\pi}{4})$ | $\frac{f^{(n)}(\frac{\pi}{4})}{n!}$ | Term $c_n (x-a)^n$ |
| :--: | :---: | :---: | :---: | :---: |
| 0 | $\sin(x)$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ |
| 1 | $\cos(x)$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2} (x-\frac{\pi}{4})$ |
| 2 | $-\sin(x)$ | $-\frac{\sqrt{2}}{2}$ | $-\frac{\sqrt{2}}{4}$ | $-\frac{\sqrt{2}}{4} (x-\frac{\pi}{4})^2$ |
| 3 | $-\cos(x)$ | $-\frac{\sqrt{2}}{2}$ | $-\frac{\sqrt{2}}{12}$ | $-\frac{\sqrt{2}}{12} (x-\frac{\pi}{4})^3$ |
| 4 | $\sin(x)$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{48}$ | $\frac{\sqrt{2}}{48} (x-\frac{\pi}{4})^4$ |

$$T_4(x) = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} (x-\frac{\pi}{4}) - \frac{\sqrt{2}}{4} (x-\frac{\pi}{4})^2 - \frac{\sqrt{2}}{12} (x-\frac{\pi}{4})^3 + \frac{\sqrt{2}}{48} (x-\frac{\pi}{4})^4$$

#### Solution 2: Error Estimation (Taylor's Inequality)

Taylor's inequality states: $|R_4(x)| \le \frac{M}{5!} |x-a|^5$, where $M = \max |f^{(5)}(x)|$ on the given interval.

1.  **Find the 5th derivative:** $f^{(5)}(x) = \cos(x)$.
2.  **Find $M$:** We need the maximum value of $|\cos(x)|$ on the interval $[\frac{\pi}{8}, \frac{7\pi}{8}]$.
    * Since $|\cos(x)|$ is positive in the given range, we check the endpoints and the center:
        * The minimum magnitude occurs at the center $x=\frac{\pi}{4}$, $x=\frac{3\pi}{4}$.
        * The maximum magnitude occurs at the endpoints $\frac{\pi}{8}$ or $\frac{7\pi}{8}$.
    * Since $0 < \frac{\pi}{8} < \frac{\pi}{4}$, the maximum value of $\cos(x)$ on this interval is at the boundary $\frac{\pi}{8}$.
    * However, the maximum possible value for **any** derivative of $\sin(x)$ or $\cos(x)$ is $\mathbf{1}$.
    * Therefore, we can safely use $M=1$.
3.  **Find $\max |x-a|^5$**: The center is $a=\frac{\pi}{4}$. We check the distance to the endpoints:
    * $\left|\frac{\pi}{8} - \frac{\pi}{4}\right| = \left|-\frac{\pi}{8}\right| = \frac{\pi}{8}$
    * $\left|\frac{7\pi}{8} - \frac{\pi}{4}\right| = \left|\frac{7\pi - 2\pi}{8}\right| = \frac{5\pi}{8}$
    * The maximum distance is $\mathbf{\frac{5\pi}{8}}$.
4.  **Calculate the Error Bound:**
    $$|R_4(x)| \le \frac{1}{5!} \left(\frac{5\pi}{8}\right)^5 = \frac{1}{120} \left(\frac{5\pi}{8}\right)^5$$
    Using $\pi \approx 3.14159$:
    $$|R_4(x)| \le \frac{1}{120} (1.96349)^5 \approx \frac{1}{120} (30.007) \approx \mathbf{0.25006}$$

**Answer:** The accuracy of the approximation $f(x) \approx T_4(x)$ is estimated to be within **$0.25006$**.

---
---

### 2. New Maclaurin by Definition & Radius of Convergence ($R$)

**Problem:** Find the Maclaurin series expansion of $f(x) = \frac{1}{1-x}$ and of $f(x) = \sinh(x)$ using the **definition** of Maclaurin series. Find the radius of convergence of each.

#### Solution 1: $f(x) = \frac{1}{1-x}$

1.  **Calculate and Evaluate Derivatives at $a=0$:**
    * $f(x) = (1-x)^{-1} \implies f(0) = 1$
    * $f'(x) = 1(1-x)^{-2} \implies f'(0) = 1$
    * $f''(x) = 2(1-x)^{-3} \implies f''(0) = 2$
    * $f'''(x) = 6(1-x)^{-4} \implies f'''(0) = 6$
    * **Pattern:** $f^{(n)}(0) = n!$
2.  **Maclaurin Series:**
    $$\sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!} x^n = \sum_{n=0}^\infty \frac{n!}{n!} x^n = \sum_{n=0}^\infty x^n$$
    $$f(x) = 1 + x + x^2 + x^3 + \dots$$
3.  **Radius of Convergence ($R$):**
    Using the Ratio Test on $a_n = x^n$:
    $$L = \lim_{n \to \infty} \left| \frac{x^{n+1}}{x^n} \right| = \lim_{n \to \infty} |x| = |x|$$
    Convergence requires $L < 1$, so $|x| < 1$. $\mathbf{R=1}$.

#### Solution 2: $f(x) = \sinh(x)$

1.  **Calculate and Evaluate Derivatives at $a=0$:**
    * $f(x) = \sinh(x) \implies f(0) = 0$
    * $f'(x) = \cosh(x) \implies f'(0) = 1$
    * $f''(x) = \sinh(x) \implies f''(0) = 0$
    * $f'''(x) = \cosh(x) \implies f'''(0) = 1$
    * **Pattern:** Derivatives alternate between 0 and 1. The non-zero derivatives occur when $n$ is **odd**. For $n = 2k+1$, $f^{(2k+1)}(0) = 1$.
2.  **Maclaurin Series:** We only sum the odd terms ($n=2k+1$):
    $$\sum_{k=0}^\infty \frac{f^{(2k+1)}(0)}{(2k+1)!} x^{2k+1} = \sum_{k=0}^\infty \frac{1}{(2k+1)!} x^{2k+1}$$
    $$f(x) = x + \frac{x^3}{3!} + \frac{x^5}{5!} + \dots$$
3.  **Radius of Convergence ($R$):**
    Using the Ratio Test on $a_k = \frac{x^{2k+1}}{(2k+1)!}$:
    $$L = \lim_{k \to \infty} \left| \frac{a_{k+1}}{a_k} \right| = \lim_{k \to \infty} \left| \frac{x^{2(k+1)+1}}{(2(k+1)+1)!} \cdot \frac{(2k+1)!}{x^{2k+1}} \right|$$
    $$L = \lim_{k \to \infty} \left| \frac{x^2}{(2k+3)(2k+2)} \right| = 0$$
    Since $L=0 < 1$ for all values of $x$, the radius of convergence is $\mathbf{R=\infty}$.

---
---

### 3. New Taylor Series & Interval of Convergence

**Problem:** Find the Taylor series expansion of $f(x) = \ln(x)$ at $a=2$ and determine its interval of convergence.

#### Solution: Taylor Series Expansion

1.  **Derivatives and Evaluation at $a=2$:**
    | $n$ | $f^{(n)}(x)$ | $f^{(n)}(2)$ |
    | :--: | :---: | :---: |
    | 0 | $\ln(x)$ | $\ln(2)$ |
    | 1 | $x^{-1}$ | $\frac{1}{2}$ |
    | 2 | $-x^{-2}$ | $-\frac{1}{4}$ |
    | 3 | $2x^{-3}$ | $\frac{2}{8} = \frac{1}{4}$ |
    | 4 | $-6x^{-4}$ | $-\frac{6}{16} = -\frac{3}{8}$ |
    * **General Term ($n \ge 1$):** $f^{(n)}(x) = (-1)^{n-1} (n-1)! x^{-n}$.
    * **Coefficient Term ($n \ge 1$):** $\frac{f^{(n)}(2)}{n!} = \frac{(-1)^{n-1} (n-1)! 2^{-n}}{n!} = \frac{(-1)^{n-1}}{n 2^n}$.

2.  **Taylor Series:**
    The $n=0$ term is $f(2) = \ln(2)$.
    $$f(x) = \ln(2) + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n 2^n} (x-2)^n$$

#### Solution: Interval of Convergence

1.  **Ratio Test:** Apply the Ratio Test to the series $\sum_{n=1}^\infty a_n$, where $a_n = \frac{(-1)^{n-1}}{n 2^n} (x-2)^n$.
    $$L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n \to \infty} \left| \frac{(-1)^{n}}{(n+1) 2^{n+1}} (x-2)^{n+1} \cdot \frac{n 2^n}{(-1)^{n-1} (x-2)^n} \right|$$
    $$L = \lim_{n \to \infty} \left| \frac{n}{n+1} \cdot \frac{1}{2} (x-2) \right| = \frac{1}{2} |x-2|$$
    For convergence, $L < 1$: $\frac{1}{2} |x-2| < 1 \implies |x-2| < 2$. The radius is $\mathbf{R=2}$.
    The open interval is $0 < x < 4$.

2.  **Check Endpoints:**
    * **At $x=4$**: $\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n 2^n} (4-2)^n = \sum_{n=1}^\infty \frac{(-1)^{n-1} 2^n}{n 2^n} = \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n}$. This is the alternating harmonic series, which **converges** (by AST).
    * **At $x=0$**: $\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n 2^n} (0-2)^n = \sum_{n=1}^\infty \frac{(-1)^{n-1} (-2)^n}{n 2^n} = \sum_{n=1}^\infty \frac{(-1)^{n-1} (-1)^n 2^n}{n 2^n}$
        $$= \sum_{n=1}^\infty \frac{(-1)^{2n-1}}{n} = \sum_{n=1}^\infty \frac{-1}{n} = -\sum_{n=1}^\infty \frac{1}{n}$$
        This is the negative of the harmonic series, which **diverges**.

**Answer:** The Taylor series is $f(x) = \ln(2) + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n 2^n} (x-2)^n$, and the interval of convergence is $\mathbf{(0, 4]}$.

---
---

### 4. New Integral as Series & Definite Integral Approximation

**Problem:** Express the indefinite integral $\int \frac{\sin(x)}{x} dx$ as an infinite series and then evaluate the definite integral $\int_0^{0.1} \frac{\sin(x)}{x} dx$ to within an accuracy of $\mathbf{0.0001}$.

#### Solution 1: Infinite Series Representation

1.  **Series for $\sin(x)$:**
    $$\sin(x) = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$$
2.  **Series for $\frac{\sin(x)}{x}$:** Divide by $x$ (valid for $x \ne 0$):
    $$\frac{\sin(x)}{x} = \sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n+1)!} = 1 - \frac{x^2}{3!} + \frac{x^4}{5!} - \frac{x^6}{7!} + \dots$$
3.  **Indefinite Integral:** Integrate term-by-term:
    $$\int \frac{\sin(x)}{x} dx = C + \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1) \cdot (2n+1)!}$$
    $$\int \frac{\sin(x)}{x} dx = C + x - \frac{x^3}{3 \cdot 3!} + \frac{x^5}{5 \cdot 5!} - \frac{x^7}{7 \cdot 7!} + \dots$$

#### Solution 2: Definite Integral Approximation

We evaluate the definite integral at the limits $[0, 0.1]$:
$$\int_0^{0.1} \frac{\sin(x)}{x} dx = \left[ \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1) (2n+1)!} \right]_0^{0.1} = \sum_{n=0}^\infty \frac{(-1)^n (0.1)^{2n+1}}{(2n+1) (2n+1)!}$$

1.  **Accuracy Requirement:** We need error $|R_N| < 0.0001$. This is an alternating series, so we use the Alternating Series Estimation Theorem: $|R_N| \le b_{N+1}$.
2.  **Test Terms ($b_n$):** We seek the first term whose magnitude is less than $0.0001$.
    * **$n=0$ term ($b_1$):** $\frac{(0.1)^1}{1 \cdot 1!} = 0.1$
    * **$n=1$ term ($b_2$):** $\frac{(0.1)^3}{3 \cdot 3!} = \frac{0.001}{18} \approx 0.00005555$
3.  **Conclusion:** Since the magnitude of the $n=1$ term ($b_2$) is $\approx 0.00005555$, which is less than $0.0001$, we only need to use the sum of the **first two terms** (the $n=0$ and $n=1$ terms) for the required accuracy.

4.  **Calculate Approximation $S_2$:**
    $$S_2 = (\text{n=0 term}) - (\text{n=1 term})$$
    $$S_2 = 0.1 - 0.000055555\dots$$
    $$S_2 \approx 0.099944444$$

**Answer:** The definite integral is approximately $\mathbf{0.0999}$ (to four decimal places).

---
---

### 5. New Limit by Power Series

**Problem:** Use power series to evaluate the limit $\lim_{x\to 0} \frac{e^{x^2} - 1 - x^2}{x^4}$.

#### Solution: Evaluating the Limit

1.  **Series for $e^u$:**
    $$e^u = 1 + u + \frac{u^2}{2!} + \frac{u^3}{3!} + \dots$$
2.  **Series for $e^{x^2}$:** Substitute $u=x^2$:
    $$e^{x^2} = 1 + x^2 + \frac{(x^2)^2}{2!} + \frac{(x^2)^3}{3!} + \dots = 1 + x^2 + \frac{x^4}{2!} + \frac{x^6}{3!} + \dots$$
3.  **Substitute into the Numerator:**
    $$\text{Numerator} = e^{x^2} - 1 - x^2$$
    $$\text{Numerator} = \left(1 + x^2 + \frac{x^4}{2!} + \frac{x^6}{3!} + \dots\right) - 1 - x^2$$
    $$\text{Numerator} = \frac{x^4}{2!} + \frac{x^6}{3!} + \frac{x^8}{4!} + \dots$$
4.  **Evaluate the Limit:** Divide the numerator by the denominator $x^4$:
    $$\frac{e^{x^2} - 1 - x^2}{x^4} = \frac{\frac{x^4}{2!} + \frac{x^6}{3!} + \frac{x^8}{4!} + \dots}{x^4}$$
    $$\frac{e^{x^2} - 1 - x^2}{x^4} = \frac{1}{2!} + \frac{x^2}{3!} + \frac{x^4}{4!} + \dots$$
    Now, take the limit as $x \to 0$:
    $$\lim_{x\to 0} \left( \frac{1}{2!} + \frac{x^2}{3!} + \frac{x^4}{4!} + \dots \right)$$
    As $x \to 0$, all terms containing $x$ go to zero.

$$\text{Limit} = \frac{1}{2!} = \mathbf{\frac{1}{2}}$$

---
---

### 6. New Sum of Series as Familiar Function Value

**Problem:** Find the sum of the series $\sum_{n=0}^\infty \frac{(-1)^{n} \pi^{2n+1}}{(2n+1)!}$ as the value of a familiar function.

#### Solution: Identifying the Function

1.  **Identify the Series Type:** The series contains alternating signs $(-1)^n$, odd powers of $x$ (or $\pi$) in the numerator, and factorials of those odd numbers in the denominator $((2n+1)!)$. This is the characteristic form of the Maclaurin series for **$\sin(u)$**.
2.  **Standard $\sin(u)$ Series:**
    $$\sin(u) = \sum_{n=0}^\infty \frac{(-1)^n u^{2n+1}}{(2n+1)!}$$
3.  **Compare:** Compare the given series to the standard form:
    $$\sum_{n=0}^\infty \frac{(-1)^{n} \mathbf{\pi}^{2n+1}}{(2n+1)!} \quad \text{vs.} \quad \sum_{n=0}^\infty \frac{(-1)^n \mathbf{u}^{2n+1}}{(2n+1)!}$$
    By direct comparison, the value $\mathbf{u}$ must be $\mathbf{\pi}$.
4.  **Conclusion:** The sum of the series is the value of the sine function evaluated at $u=\pi$:
    $$\text{Sum} = \sin(\pi)$$

$$\text{Sum} = \mathbf{0}$$
