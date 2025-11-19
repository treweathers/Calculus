## Series Formula Sheet

---

That's an essential series to include! The **Binomial Series** is a key expansion that allows you to handle fractional and negative exponents.

Here is the updated chart with the Binomial Series entry, using the detailed formula and conventions you provided.

---

## 📋 Chart of Common Maclaurin Series

| Function $f(x)$ | Maclaurin Series $\sum_{n=0}^\infty c_n x^n$ | I.O.C. |
| :--- | :--- | :--- |
| $\frac{1}{1 - x}$ (Geometric) | $\sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \dots$ | $(-1, 1)$ |
| $e^x$ | $\sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots$ | $(-\infty, \infty)$ |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $(-\infty, \infty)$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $(-\infty, \infty)$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $(-1, 1]$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $[-1, 1]$ |
| **$(1+x)^k$ (Binomial)** | **$\sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \dots$** | **$(-1, 1)$**$^\dagger$ |

$^\dagger$ **Note:** The interval of convergence is $(-1, 1)$ unless $k$ is a non-negative integer, in which case the series is finite and converges for all $x$.

---

$^\dagger$ **Note on Binomial Series I.O.C.:** The interval of convergence is $(-1, 1)$ for any real number $k$ that is not a non-negative integer. If $k$ is a non-negative integer (like $k=2$), the series becomes a finite polynomial and converges for all $x$ ($-\infty, \infty$).

---

### **Generalized Binomial Coefficient**

For reference, the generalized binomial coefficient is defined as:
$$\begin{pmatrix} k \\ n \end{pmatrix} = \frac{k(k-1)(k-2) \dots (k-n+1)}{n!}$$

Would you like to review any of the other sections of your study guide, or is there another concept you'd like to add?
