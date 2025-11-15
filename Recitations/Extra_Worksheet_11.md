
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

## 🧠 Additional Practice Problems: Taylor and Maclaurin Series

### 1. New Taylor Polynomial & Error (Approximation of $\sin(x)$)

**Problem 1:** Approximate $f(x) = \sin(x)$ by its Taylor polynomial of degree 4 ($T_4(x)$) at $a = \frac{\pi}{4}$ in the interval $[\frac{\pi}{8}, \frac{7\pi}{8}]$. Use **Taylor's inequality** to estimate the accuracy of the approximation $f(x) \approx T_4(x)$ when $x$ lies in the given interval.

#### Review Notes on Taylor's Inequality

* **Taylor's Inequality:** Used to bound the remainder (error) $|R_n(x)| = |f(x) - T_n(x)|$.
* **Formula:** $|R_n(x)| \le \frac{M}{(n+1)!} |x-a|^{n+1}$, where $n$ is the degree of the polynomial.
* **M:** $M$ is the **maximum absolute value** of the next derivative, $|f^{(n+1)}(x)|$, on the interval $[x_{\min}, x_{\max}]$.

**Generalized Steps (Taylor Polynomial & Error):**
1.  **Calculate Derivatives:** Find $f^{(n)}(x)$ up to degree $n$.
2.  **Evaluate at Center ($a$):** Calculate $f^{(n)}(a)$.
3.  **Construct $T_n(x)$:** Substitute values into the Taylor formula.
4.  **Find $M$ (Error Bound):** Determine $M = \max |f^{(n+1)}(x)|$ on the given interval.
5.  **Calculate Max $|x-a|^{n+1}$:** Find the maximum distance from the center $a$ to the endpoints of the interval.
6.  **Apply Inequality:** Calculate the upper bound for the error $|R_n(x)|$.

**Solution 1:**

* **1. Calculate Derivatives (up to $n=5$):**
    * $f(x) = \sin(x)$
    * $f'(x) = \cos(x)$
    * $f''(x) = -\sin(x)$
    * $f'''(x) = -\cos(x)$
    * $f^{(4)}(x) = \sin(x)$
    * $f^{(5)}(x) = \cos(x)$ (Needed for the error bound $R_4$)

* **2. Evaluate at $a=\frac{\pi}{4}$:** (Recall $\sin(\frac{\pi}{4}) = \cos(\frac{\pi}{4}) = \frac{\sqrt{2}}{2}$)
    * $f(\frac{\pi}{4}) = \frac{\sqrt{2}}{2}$
    * $f'(\frac{\pi}{4}) = \frac{\sqrt{2}}{2}$
    * $f''(\frac{\pi}{4}) = -\frac{\sqrt{2}}{2}$
    * $f'''(\frac{\pi}{4}) = -\frac{\sqrt{2}}{2}$
    * $f^{(4)}(\frac{\pi}{4}) = \frac{\sqrt{2}}{2}$

* **3. Construct $T_4(x)$:**
    $$T_4(x) = \sum_{n=0}^4 \frac{f^{(n)}(\frac{\pi}{4})}{n!} (x-\frac{\pi}{4})^n$$
    $$T_4(x) = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2}(x-\frac{\pi}{4}) - \frac{\sqrt{2}}{4}(x-\frac{\pi}{4})^2 - \frac{\sqrt{2}}{12}(x-\frac{\pi}{4})^3 + \frac{\sqrt{2}}{48}(x-\frac{\pi}{4})^4$$

* **4. Find $M$ (Max $|f^{(5)}(x)|$):**
    * $f^{(5)}(x) = \cos(x)$.
    * The maximum value of $|\cos(x)|$ on any interval is $M=1$.
    * $M = \max_{\frac{\pi}{8} \le x \le \frac{7\pi}{8}} |\cos(x)| = 1$.

* **5. Calculate Max $|x-a|^5$:**
    * Center is $a = \frac{\pi}{4} \approx 0.785$.
    * Endpoints are $x_1 = \frac{\pi}{8} \approx 0.393$ and $x_2 = \frac{7\pi}{8} \approx 2.749$.
    * Max distance occurs at the right endpoint: $|x_2 - a| = |\frac{7\pi}{8} - \frac{\pi}{4}| = |\frac{5\pi}{8}|$.
    * Max distance at the left endpoint: $|x_1 - a| = |\frac{\pi}{8} - \frac{\pi}{4}| = |-\frac{\pi}{8}|$.
    * The maximum distance is $\mathbf{|\frac{5\pi}{8}|} \approx 1.9635$.
    * $\max |x-\frac{\pi}{4}|^5 = (\frac{5\pi}{8})^5 \approx 31.839$.

* **6. Apply Inequality:**
    $$|R_4(x)| \le \frac{M}{5!} |x-a|^5 \le \frac{1}{120} \left( \frac{5\pi}{8} \right)^5 \approx \frac{31.839}{120} \approx \mathbf{0.265}$$

**Answer:** The accuracy of the approximation is estimated to be **$\approx 0.265$**.

***

### 2. New Maclaurin by Definition & Radius of Convergence ($R$)

**Problem 2:** Find the Maclaurin series expansion of $f(x) = \frac{1}{1-x}$ and of $f(x) = \sinh(x)$ using the **definition** of Maclaurin series. Find the radius of convergence of each.

#### Review Notes on Maclaurin by Definition

* **Definition:** $f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!} x^n$.
* **Goal:** Find a general formula for the coefficient $c_n = \frac{f^{(n)}(0)}{n!}$.
* **Radius of Convergence ($R$):** Determined by the Ratio Test, $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$, where $L < 1$.

**Generalized Steps (Maclaurin by Definition):**
1.  **Derivatives at 0:** Calculate $f^{(n)}(0)$ for $n=0, 1, 2, \dots$ until a pattern emerges.
2.  **General Term:** Write the formula for $c_n = \frac{f^{(n)}(0)}{n!}$.
3.  **Series:** Write the series $\sum c_n x^n$.
4.  **Ratio Test:** Apply the Ratio Test to find $R$.

**Solution 2: Part A: $f(x) = \frac{1}{1-x}$**

* **1. Derivatives at 0:**
    * $f(x) = (1-x)^{-1} \implies f(0) = 1$
    * $f'(x) = (1-x)^{-2} \implies f'(0) = 1$
    * $f''(x) = 2(1-x)^{-3} \implies f''(0) = 2$
    * $f'''(x) = 6(1-x)^{-4} \implies f'''(0) = 6$
    * $f^{(n)}(0) = n!$

* **2. General Term and 3. Series:**
    $$c_n = \frac{f^{(n)}(0)}{n!} = \frac{n!}{n!} = 1$$
    $$\frac{1}{1-x} = \sum_{n=0}^\infty \frac{1}{n!} n! x^n = \sum_{n=0}^\infty x^n$$

* **4. Radius of Convergence ($R$):**
    $$L = \lim_{n \to \infty} \left| \frac{x^{n+1}}{x^n} \right| = |x|$$
    For convergence, $L < 1 \implies |x| < 1$.
    **Answer (A):** $\sum_{n=0}^\infty x^n$; **$R=1$**.

**Solution 2: Part B: $f(x) = \sinh(x)$**

* **1. Derivatives at 0:**
    * $f(x) = \sinh(x) \implies f(0) = 0$
    * $f'(x) = \cosh(x) \implies f'(0) = 1$
    * $f''(x) = \sinh(x) \implies f''(0) = 0$
    * $f'''(x) = \cosh(x) \implies f'''(0) = 1$
    * **Pattern:** $f^{(n)}(0) = 1$ if $n$ is odd, and $0$ if $n$ is even. (Let $n=2k+1$ for odd terms.)

* **2. General Term and 3. Series:**
    The series only contains odd powers of $x$. We substitute $n=2k+1$.
    $$c_n = \begin{cases} \frac{1}{n!} & \text{if } n \text{ is odd} \\ 0 & \text{if } n \text{ is even} \end{cases}$$
    $$\sinh(x) = \sum_{k=0}^\infty \frac{1}{(2k+1)!} x^{2k+1}$$

* **4. Radius of Convergence ($R$):**
    We use the Ratio Test on the terms $a_k$ (where $k$ is the index):
    $$L = \lim_{k \to \infty} \left| \frac{a_{k+1}}{a_k} \right| = \lim_{k \to \infty} \left| \frac{x^{2(k+1)+1}}{(2(k+1)+1)!} \cdot \frac{(2k+1)!}{x^{2k+1}} \right|$$
    $$L = \lim_{k \to \infty} \left| \frac{x^2}{(2k+3)(2k+2)} \right| = |x^2| \cdot 0 = 0$$
    Since $L=0$ is always $< 1$, the series converges for all $x$.
    **Answer (B):** $\sum_{n=0}^\infty \frac{x^{2n+1}}{(2n+1)!}$; **$R=\infty$**.

***

### 3. New Taylor Series & Interval of Convergence

**Problem 3:** Find the Taylor series expansion of $f(x) = \ln(x)$ at $a=2$ and determine its interval of convergence.

#### Review Notes on Taylor Series & Interval

* **Series Formula:** $f(x) = f(a) + \sum_{n=1}^\infty \frac{f^{(n)}(a)}{n!} (x-a)^n$.
* **Interval of Convergence (IOC):** Found by the **Ratio Test** for the radius $R$, followed by a **check of the endpoints**.

**Generalized Steps (Taylor Series & Interval):**
1.  **Derivatives at $a$:** Find $f(a)$ and $f^{(n)}(a)$ for $n \ge 1$ to find the general term.
2.  **Series:** Write the Taylor series.
3.  **Ratio Test:** Use the Ratio Test to find $R$ and the open IOC.
4.  **Endpoint Check:** Substitute the endpoints into the series and use convergence tests (like $p$-Test or AST) to see if the series converges there.

**Solution 3:**

* **1. Derivatives at $a=2$:**
    * $f(x) = \ln(x) \implies f(2) = \ln(2)$
    * $f'(x) = x^{-1} \implies f'(2) = 2^{-1}$
    * $f''(x) = -x^{-2} \implies f''(2) = -2^{-2}$
    * $f'''(x) = 2x^{-3} \implies f'''(2) = 2 \cdot 2^{-3}$
    * $f^{(n)}(x) = (-1)^{n-1} (n-1)! x^{-n}$ for $n \ge 1$.
    * $f^{(n)}(2) = (-1)^{n-1} (n-1)! 2^{-n}$ for $n \ge 1$.

* **2. Series:**
    $$f(x) = f(2) + \sum_{n=1}^\infty \frac{f^{(n)}(2)}{n!} (x-2)^n$$
    $$f(x) = \ln(2) + \sum_{n=1}^\infty \frac{(-1)^{n-1} (n-1)! 2^{-n}}{n!} (x-2)^n$$
    $$f(x) = \ln(2) + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n \cdot 2^n} (x-2)^n$$

* **3. Ratio Test (Find $R$ and Open IOC):**
    Let $a_n = \frac{(-1)^{n-1}}{n \cdot 2^n} (x-2)^n$.
    $$L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n \to \infty} \left| \frac{(x-2)^{n+1}}{(n+1) 2^{n+1}} \cdot \frac{n 2^n}{(x-2)^n} \right|$$
    $$L = \lim_{n \to \infty} \left| (x-2) \cdot \frac{n}{n+1} \cdot \frac{1}{2} \right| = \frac{|x-2|}{2}$$
    For convergence, $L < 1 \implies \frac{|x-2|}{2} < 1 \implies |x-2| < 2$.
    Thus, $\mathbf{R=2}$. The open interval is $2-2 < x < 2+2 \implies (0, 4)$.

* **4. Endpoint Check:**
    * **At $x=4$:** Substitute $x=4$ into the series:
        $$\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n \cdot 2^n} (4-2)^n = \sum_{n=1}^\infty \frac{(-1)^{n-1} 2^n}{n \cdot 2^n} = \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n}$$
        This is the alternating harmonic series, which **converges** (by AST).
    * **At $x=0$:** Substitute $x=0$ into the series:
        $$\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n \cdot 2^n} (0-2)^n = \sum_{n=1}^\infty \frac{(-1)^{n-1} (-2)^n}{n \cdot 2^n} = \sum_{n=1}^\infty \frac{(-1)^{n-1} (-1)^n 2^n}{n \cdot 2^n} = \sum_{n=1}^\infty \frac{-1}{n}$$
        This is the negative harmonic series, which **diverges** ($p=1$).

**Answer:** The Taylor series is $\ln(2) + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n \cdot 2^n} (x-2)^n$. The interval of convergence is $\mathbf{(0, 4]}$.

***

### 4. New Integral as Series & Definite Integral Approximation

**Problem 4:** Express the indefinite integral $\int \frac{\sin(x)}{x} dx$ as an infinite series and then evaluate the definite integral $\int_0^{0.1} \frac{\sin(x)}{x} dx$ to within an accuracy of **$0.0001$**.

#### Review Notes on Integral Approximation

* **$\sin(x)$ Series:** $\sin(x) = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!}$
* **Integration:** Integrate the series term-by-term.
* **Error Bound:** For the resulting alternating series, $|R_N| \le b_{N+1}$.

**Generalized Steps (Integral Approximation):**
1.  **Series for Integrand:** Start with a known series and manipulate it (substitution, multiplication, division) to find the series for the integrand.
2.  **Integration:** Integrate the series term-by-term.
3.  **Error Check:** Set the first neglected term $b_{N+1}$ less than the required accuracy ($\epsilon$).
4.  **Calculate Sum:** Sum the required number of terms $S_N$ and round to satisfy the accuracy.

**Solution 4:**

* **1. Series for Integrand $\frac{\sin(x)}{x}$:**
    $$\sin(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \dots = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!}$$
    $$\frac{\sin(x)}{x} = 1 - \frac{x^2}{3!} + \frac{x^4}{5!} - \frac{x^6}{7!} + \dots = \sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n+1)!}$$

* **2. Integration (Indefinite and Definite):**
    $$\int \frac{\sin(x)}{x} dx = C + \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)! (2n+1)}$$
    $$\int_0^{0.1} \frac{\sin(x)}{x} dx = \left[ \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)! (2n+1)} \right]_0^{0.1} = \sum_{n=0}^\infty \frac{(-1)^n (0.1)^{2n+1}}{(2n+1)! (2n+1)}$$

* **3. Error Check ($\epsilon = 0.0001$):**
    We need $|R_N| \le b_{N+1} < 0.0001$.
    $$b_n = \frac{(0.1)^{2n+1}}{(2n+1)! (2n+1)}$$
    * **$n=0$ Term:** $b_0 = \frac{(0.1)^1}{1! \cdot 1} = 0.1$
    * **$n=1$ Term:** $b_1 = \frac{(0.1)^3}{3! \cdot 3} = \frac{0.001}{18} \approx 0.0000555$
    * Since $\mathbf{b_1 \approx 0.0000555 < 0.0001}$, we only need the terms up to $n=0$ (the first term). The error in using $S_1$ is bounded by $b_1$.

* **4. Calculate Sum (using $n=0$):**
    $$S_1 = a_0 = \frac{(-1)^0 (0.1)^{1}}{1! \cdot 1} = 0.1$$

**Answer:** The indefinite integral is $C + \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)! (2n+1)}$. The definite integral approximation is $\mathbf{0.1000}$ (since the error is less than $0.0001$, or more precisely, $0.0999$ if we use $a_0+a_1 \approx 0.099944$).

***

### 5. New Limit by Power Series

**Problem 5:** Use power series to evaluate the limit $\lim_{x\to 0} \frac{e^{x^2} - 1 - x^2}{x^4}$.

#### Review Notes on Limits by Power Series

* **Key Series:** $e^u = 1 + u + \frac{u^2}{2!} + \frac{u^3}{3!} + \dots$
* **Method:** Substitute the series into the expression and simplify the numerator by canceling low-order terms. The limit is then the coefficient of the lowest remaining power of $x$.

**Generalized Steps (Limit by Power Series):**
1.  **Substitute Series:** Replace the function with its Maclaurin series.
2.  **Simplify Numerator:** Cancel terms that are outside the summation (in this case, $1$ and $x^2$).
3.  **Divide by Denominator:** Divide every term in the series by the denominator's power of $x$ (in this case, $x^4$).
4.  **Evaluate Limit:** As $x \to 0$, all terms containing a positive power of $x$ vanish, leaving only the constant term.

**Solution 5:**

* **1. Substitute Series ($e^{x^2}$):**
    Let $u = x^2$.
    $$e^{x^2} = 1 + x^2 + \frac{(x^2)^2}{2!} + \frac{(x^2)^3}{3!} + \dots = 1 + x^2 + \frac{x^4}{2} + \frac{x^6}{6} + \dots$$

* **2. Simplify Numerator ($e^{x^2} - 1 - x^2$):**
    $$e^{x^2} - 1 - x^2 = \left( 1 + x^2 + \frac{x^4}{2} + \frac{x^6}{6} + \dots \right) - 1 - x^2$$
    $$e^{x^2} - 1 - x^2 = \frac{x^4}{2} + \frac{x^6}{6} + \frac{x^8}{24} + \dots$$

* **3. Divide by Denominator ($x^4$):**
    $$\frac{e^{x^2} - 1 - x^2}{x^4} = \frac{\frac{x^4}{2} + \frac{x^6}{6} + \frac{x^8}{24} + \dots}{x^4}$$
    $$\frac{e^{x^2} - 1 - x^2}{x^4} = \frac{1}{2} + \frac{x^2}{6} + \frac{x^4}{24} + \dots$$

* **4. Evaluate Limit:**
    $$\lim_{x\to 0} \left( \frac{1}{2} + \frac{x^2}{6} + \frac{x^4}{24} + \dots \right)$$
    As $x \to 0$, all terms with $x$ go to zero.

**Answer:** $\mathbf{\frac{1}{2}}$

***

### 6. New Sum of Series as Familiar Function Value

**Problem 6:** Find the sum of the series $\sum_{n=0}^\infty \frac{(-1)^{n} \pi^{2n+1}}{(2n+1)!}$ as the value of a familiar function.

#### Review Notes on Sum of Series

* **Goal:** Identify the form of the series and match it to one of the standard Maclaurin series (e.g., $e^x, \sin x, \cos x, \ln(1+x)$).
* **Substitution:** Determine the value of the variable $u$ that was substituted into the standard series to produce the given series. The sum is $f(u)$.

**Generalized Steps (Sum of Series):**
1.  **Identify Template:** Determine which standard Maclaurin series template matches the coefficients and power terms.
2.  **Match Variable:** Compare the $x^k$ term in the template with the $\pi^k$ term in the given series to find the value of $x$.
3.  **Evaluate Function:** The sum is the value of the function evaluated at that specific $x$.

**Solution 6:**

* **1. Identify Template:** The given series uses $\mathbf{(-1)^n}$ in the numerator and $\mathbf{(2n+1)!}$ in the denominator, and only has **odd** powers. This perfectly matches the Maclaurin series for $\mathbf{\sin(x)}$.
    $$\sin(x) = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!}$$

* **2. Match Variable:**
    * Given series: $\sum_{n=0}^\infty \frac{(-1)^{n} \mathbf{\pi}^{2n+1}}{(2n+1)!}$
    * Template series: $\sum_{n=0}^\infty \frac{(-1)^{n} \mathbf{x}^{2n+1}}{(2n+1)!}$
    * By comparison, the variable is $\mathbf{x = \pi}$.

* **3. Evaluate Function:**
    The sum of the series is equal to $\sin(\pi)$.

**Answer:** $\sin(\pi) = \mathbf{0}$.
