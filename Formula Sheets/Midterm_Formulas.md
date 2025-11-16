## 📚 Series Formula Sheet

---

### II. Common Known Series

#### **1. Geometric Series**
* **General Form:** $\sum_{n=1}^\infty ar^{n-1} = a + ar + ar^2 + \dots$
* **Condition for Convergence:** $|r| < 1$.
* **Sum ($S$):** If it converges (for $n \geq 1$), $S = \frac{a}{1-r}$.

#### **2. $p$-Series**
* **General Form:** $\sum_{n=1}^\infty \frac{1}{n^p} = 1 + \frac{1}{2^p} + \frac{1}{3^p} + \dots$
* **Condition for Convergence:** $p > 1$.
* **Note:** No simple general formula for the sum $S$.

#### **3. Standard Harmonic Series**
* **General Form:** $\sum_{n=1}^\infty \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \dots$
* **Convergence:** Always **Diverges** (This is the $p$-Series case where $p=1$).
* **Sum ($S$):** N/A.

#### **4. Alternating Harmonic Series**
* **General Form:** $\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \dots$
* **Convergence:** Converges (by AST).
* **Sum ($S$):** $S = \ln(2)$.

#### **5. Telescoping Series**
* **General Form:** $\sum_{n=1}^\infty (b_n - b_{n+1})$
* **Condition for Convergence:** Converges if $\lim_{n\to\infty} b_{n+1}$ exists.
* **Sum ($S$):** $S = b_1 - \lim_{n\to\infty} b_{n+1}$.

---

Does this structure provide the clarity you were looking for?
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

#### **2. Taylor and Maclaurin Series & Chart of Common Maclaurin Series**

* **Taylor Series** of a function $f(x)$ centered at $a$:
    $$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!} (x-a)^n$$
* **Maclaurin Series:** A Taylor series centered at $a=0$:
    $$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!} x^n$$

| Function $f(x)$ | Maclaurin Series $\sum_{n=0}^\infty c_n x^n$ | I.O.C. |
| :--- | :--- | :--- |
| $\frac{1}{1-x}$ (Geometric) | $\sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \dots$ | $(-1, 1)$ |
| $e^x$ | $\sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots$ | $(-\infty, \infty)$ |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $(-\infty, \infty)$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $(-\infty, \infty)$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $(-1, 1]$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $[-1, 1]$ |
