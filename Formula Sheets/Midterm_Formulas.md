## 📚 Series Formula Sheet

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

#### **4. Binomial Series**

* **Formula:** For $(1+x)^k$, where $k$ is any real number:
    $$(1+x)^k = \sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \frac{k(k-1)(k-2)}{3!}x^3 + \dots$$
* **Binomial Coefficient:** The generalized binomial coefficient is defined as:
    $$\binom{k}{n} = \frac{k(k-1)(k-2)\dots(k-n+1)}{n!}$$
* **I.O.C.:** $(-1, 1)$. (If $k$ is a non-negative integer, the series is a finite polynomial and converges for all $x$).

