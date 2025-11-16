## 📚 Series Formula Sheet

### I. Fundamental Definitions & Notation

* **Series:** A series is the sum of the terms of a sequence, written as $\sum_{n=1}^\infty a_n = a_1 + a_2 + a_3 + \dots$.
* **$N$-th Partial Sum ($S_N$):** This is the sum of the first $N$ terms: $S_N = \sum_{n=1}^N a_n = a_1 + a_2 + \dots + a_N$.
* **Sum of a Series ($S$):** The series converges if the limit of the partial sums exists and is finite: $S = \lim_{N\to\infty} S_N$. If this limit does not exist, the series **diverges**.
* **Absolute Convergence:** A series $\sum a_n$ converges **absolutely** if the series of absolute values, $\sum_{n=1}^\infty |a_n|$, converges. (Absolute convergence $\implies$ Convergence).
* **Conditional Convergence:** A series $\sum a_n$ converges, but the series $\sum |a_n|$ diverges. (Applies only to alternating series).
* **Remainder in Taylor Series ($R_N(x)$):** The error when approximating $f(x)$ with the $N$-th degree Taylor polynomial $P_N(x)$: $R_N(x) = f(x) - P_N(x)$.

---

### II. Common Known Series

#### **1. Geometric Series**
* **General Form:** $\sum_{n=1}^\infty ar^{n-1} = a + ar + ar^2 + \dots$
* **Condition for Convergence:** $|r| < 1$.
* **Sum ($S$):** If it converges (for $n \geq 1$), $S = \frac{a}{1-r}$.

#### **2. $p$-Series**
* **General Form:** $\sum_{n=1}^\infty \frac{1}{n^p} = 1 + \frac{1}{2^p} + \frac{1}{3^p} + \dots$
* **Condition for Convergence:** $p > 1$.
* **Harmonic Series:** The case where $p=1$ ($\sum_{n=1}^\infty \frac{1}{n}$) always **Diverges**.

#### **3. Alternating Harmonic Series**
* **General Form:** $\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \dots$
* **Convergence:** Converges (by AST).
* **Sum ($S$):** $S = \ln(2)$.

#### **4. Telescoping Series**
* **General Form:** $\sum_{n=1}^\infty (b_n - b_{n+1})$
* **Condition for Convergence:** Converges if $\lim_{n\to\infty} b_{n+1}$ exists.
* **Sum ($S$):** $S = b_1 - \lim_{n\to\infty} b_{n+1}$.

---

### III. Convergence Tests for $\sum a_n$

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

---

### IV. Power Series, Taylor, and Maclaurin Series

#### **1. Power Series Formulas**

A power series centered at $a$ has the form:
$$\sum_{n=0}^\infty c_n (x-a)^n = c_0 + c_1(x-a) + c_2(x-a)^2 + \dots$$

* **Radius of Convergence ($R$):** Found using the Ratio or Root Test. The series converges for $|x-a| < R$.
    * If $\lim_{n\to\infty} \left| \frac{c_{n+1}}{c_n} \right| = L$, then $R = \frac{1}{L}$.
    * If the limit is $0$, $R=\infty$. If the limit is $\infty$, $R=0$.
* **Interval of Convergence (I.O.C.):** The interval $(a-R, a+R)$. **The endpoints $x=a-R$ and $x=a+R$ must be checked separately** using a convergence test.
* **Differentiation:** You can differentiate a power series term-by-term. The radius $R$ is unchanged, but convergence at the endpoints may change:
    $$\frac{d}{dx} \left[ \sum_{n=0}^\infty c_n (x-a)^n \right] = \sum_{n=1}^\infty n c_n (x-a)^{n-1}$$
* **Integration:** You can integrate a power series term-by-term. The radius $R$ is unchanged, but convergence at the endpoints may change:
    $$\int \left[ \sum_{n=0}^\infty c_n (x-a)^n \right] dx = C + \sum_{n=0}^\infty \frac{c_n}{n+1} (x-a)^{n+1}$$

#### **2. Taylor and Maclaurin Series**

* **Taylor Series** of a function $f(x)$ centered at $a$:
    $$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!} (x-a)^n$$
* **Maclaurin Series:** A Taylor series centered at $a=0$:
    $$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!} x^n$$

#### **3. Chart of Common Maclaurin Series**

| Function $f(x)$ | Maclaurin Series $\sum_{n=0}^\infty c_n x^n$ | I.O.C. |
| :--- | :--- | :--- |
| $\frac{1}{1-x}$ (Geometric) | $\sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \dots$ | $(-1, 1)$ |
| $e^x$ | $\sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots$ | $(-\infty, \infty)$ |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $(-\infty, \infty)$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $(-\infty, \infty)$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $(-1, 1]$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $[-1, 1]$ |

#### **4. Binomial Series**

* **Formula:** For $(1+x)^k$, where $k$ is any real number:
    $$(1+x)^k = \sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \frac{k(k-1)(k-2)}{3!}x^3 + \dots$$
* **Binomial Coefficient:** The generalized binomial coefficient is defined as:
    $$\binom{k}{n} = \frac{k(k-1)(k-2)\dots(k-n+1)}{n!}$$
* **I.O.C.:** $(-1, 1)$. (If $k$ is a non-negative integer, the series is a finite polynomial and converges for all $x$).
