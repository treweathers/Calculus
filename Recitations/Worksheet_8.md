# Part I: Review
## Practice Problems and Solutions with Review Notes

### 1. Sequences: Terms and Limits

Write the first four terms of the sequence $a_n$ and find $\lim_{n\to\infty} a_n$ if this limit exists. You may use the limit of the corresponding continuous function on the positive real numbers. If the limit does not exist, explain why it does not.

#### Review Notes on Sequences

* A **sequence** is an ordered list of numbers $\{a_1, a_2, a_3, \ldots, a_n, \ldots\}$.
* The **limit of a sequence**, $\lim_{n\to\infty} a_n = L$, means the terms get arbitrarily close to a single number $L$. If the limit is a finite number $L$, the sequence **converges** to $L$.
* **Divergence:** A sequence **diverges** if its limit is $\infty$, $-\infty$, or if it oscillates indefinitely (e.g., $a_n = (-1)^n$).
* **L'Hôpital's Rule:** If the limit of the corresponding continuous function results in an indeterminate form ($\frac{\infty}{\infty}$ or $\frac{0}{0}$), you can use L'Hôpital's Rule.

**(a)** $\{3n - 1\}_{n=1}^\infty$

**Solution 1(a):**
The first four terms are:
$$a_1 = 3(1) - 1 = 2$$
$$a_2 = 3(2) - 1 = 5$$
$$a_3 = 3(3) - 1 = 8$$
$$a_4 = 3(4) - 1 = 11$$
The limit is:
$$\lim_{n\to\infty} (3n - 1) = \infty$$
The limit **does not exist** (diverges to $\infty$).

**(b)** $a_n = \frac{(-1)^{n+1}}{2^n}$, for $n=1, 2, 3, \ldots$

**Solution 1(b):**
The first four terms are:
$$a_1 = \frac{(-1)^{1+1}}{2^1} = \frac{1}{2}$$
$$a_2 = \frac{(-1)^{2+1}}{2^2} = -\frac{1}{4}$$
$$a_3 = \frac{(-1)^{3+1}}{2^3} = \frac{1}{8}$$
$$a_4 = \frac{(-1)^{4+1}}{2^4} = -\frac{1}{16}$$
The limit is:
$$\lim_{n\to\infty} \left|a_n\right| = \lim_{n\to\infty} \frac{1}{2^n} = 0$$
Since the limit of the absolute value is $0$, the limit of the sequence is $\mathbf{0}$.

**(c)** $a_n = \sqrt{n+5} - \sqrt{n}$, for $n=1, 2, 3, \ldots$

**Solution 1(c):**
The first four terms are:
$$a_1 = \sqrt{6} - 1$$
$$a_2 = \sqrt{7} - \sqrt{2}$$
$$a_3 = \sqrt{8} - \sqrt{3}$$
$$a_4 = \sqrt{9} - \sqrt{4} = 3 - 2 = 1$$
To find the limit, multiply by the conjugate:
$$a_n = (\sqrt{n+5} - \sqrt{n}) \cdot \frac{\sqrt{n+5} + \sqrt{n}}{\sqrt{n+5} + \sqrt{n}} = \frac{5}{\sqrt{n+5} + \sqrt{n}}$$
The limit is:
$$\lim_{n\to\infty} a_n = \lim_{n\to\infty} \frac{5}{\sqrt{n+5} + \sqrt{n}} = \frac{5}{\infty} = \mathbf{0}$$

***

### 2. Converting Decimal to Rational Number

Find the rational number that has the decimal expansion $0.1\overline{23}$... (The bar is over $23$).

#### Review Notes on Rational Numbers and Decimals

* A **rational number** is any number that can be expressed as the ratio $\frac{p}{q}$ of two integers, $q \ne 0$.
* Rational numbers always have decimal expansions that either **terminate** or **repeat**.
* **Strategy:** Use powers of 10 to align the decimal points so that subtracting two multiples of $x$ eliminates the repeating tail.

**Solution 2:**
Let $x = 0.1232323\ldots$
Multiply by $10$ to shift the non-repeating part ($1$):
$$10x = 1.232323\ldots \quad \text{(Eq. 1)}$$
Multiply by $10^3$ (since the repeat starts after 1 digit, and the repeat length is 2) to shift one full repeating block:
$$1000x = 123.232323\ldots \quad \text{(Eq. 2)}$$
Subtract Eq. 1 from Eq. 2:
$$1000x - 10x = 123.232323\ldots - 1.232323\ldots$$
$$990x = 122$$
Solve for $x$:
$$x = \frac{122}{990}$$
Simplify the fraction:
$$x = \mathbf{\frac{61}{495}}$$

***

### 3. Applications: Recursive Sequences and Limits

A forest has $P_0 = 500$ deer. Each year, a fixed fraction of $\mathbf{0.8}$ of the deer survive (after births and natural deaths), and $\mathbf{150}$ deer are added to the forest (stocked from a preserve). Calculate the number of deer in each of the first $\mathbf{3}$ years. Do not round to the nearest deer. Write a recursive formula for the number of deer after $n$ years, and determine the limit of $P_n$, as $n \to\infty$.

#### Review Notes on Recursive Sequences (First-Order Linear)

* **Recursive Formula:** $P_n = r P_{n-1} + d$, where $r$ is the rate (0.8) and $d$ is the constant addition (150).
* **Limit (Steady State):** If $|r| < 1$, the limit $L$ exists and is found by solving $L = r L + d$.

**Solution 3:**
The number of deer in the first 3 years:
$$P_1 = 0.8(500) + 150 = 400 + 150 = \mathbf{550}$$
$$P_2 = 0.8(550) + 150 = 440 + 150 = \mathbf{590}$$
$$P_3 = 0.8(590) + 150 = 472 + 150 = \mathbf{622}$$
The recursive formula is:
$$P_n = 0.8 P_{n-1} + 150 \quad \text{for } n \ge 1, \text{ with } P_0 = 500$$
To find the limit $L$, set $L = 0.8L + 150$:
$$L - 0.8L = 150$$
$$0.2L = 150$$
$$L = \frac{150}{0.2} = \mathbf{750}$$

***

### 4. Partial Sums and Series Sum

If the $n$-th partial sum of a series $\sum_{n=1}^\infty a_n$ is $s_n = \frac{2n}{n + 1}$, find $a_1$, $a_2$, $a_n$ and the sum of the series $\sum_{n=1}^\infty a_n$.

#### Review Notes on Partial Sums and Series

* The **sum of the series** $S$ is $\lim_{n\to\infty} s_n$.
* The terms $a_n$ relate to the partial sums $s_n$ as: $a_n = s_n - s_{n-1}$ for $n \ge 2$, and $a_1 = s_1$.

**Solution 4:**
Find $a_1$:
$$a_1 = s_1 = \frac{2(1)}{1+1} = \mathbf{1}$$
Find $a_2$:
$$s_2 = \frac{2(2)}{2+1} = \frac{4}{3}$$
$$a_2 = s_2 - s_1 = \frac{4}{3} - 1 = \mathbf{\frac{1}{3}}$$
Find $a_n$ for $n \ge 2$:
$$a_n = s_n - s_{n-1} = \frac{2n}{n+1} - \frac{2(n-1)}{n}$$
$$a_n = \frac{2n^2 - 2(n-1)(n+1)}{n(n+1)} = \frac{2n^2 - 2(n^2-1)}{n(n+1)}$$
$$a_n = \frac{2n^2 - 2n^2 + 2}{n(n+1)} = \mathbf{\frac{2}{n(n+1)}}$$
Find the sum of the series:
$$\sum_{n=1}^\infty a_n = \lim_{n\to\infty} s_n = \lim_{n\to\infty} \frac{2n}{n+1}$$
$$\lim_{n\to\infty} \frac{2}{1 + 1/n} = \mathbf{2}$$

***

### 5. Convergence Tests for Series

Determine if the following series converge and, if so, find the sum. Use the geometric series, telescoping series, or divergence test if needed:

#### Review Notes on Series Convergence (Basic Tests)

* **Divergence Test (The First Check):** If $\lim_{n\to\infty} a_n \ne 0$, the series **diverges**.
* **Geometric Series:** $\sum a r^n$ converges if $|r| < 1$. Sum is $S = \frac{a}{1-r}$.
* **Telescoping Series:** Terms cancel in the partial sum $s_n$, and the sum is $\lim_{n\to\infty} s_n$.

**(a)** $\sum_{n=1}^\infty \frac{4n^2+1}{2n^2 - n}$

**Solution 5(a):**
Apply the **Divergence Test** by calculating the limit of the terms:
$$\lim_{n\to\infty} a_n = \lim_{n\to\infty} \frac{4n^2+1}{2n^2 - n}$$
$$\lim_{n\to\infty} \frac{4 + 1/n^2}{2 - 1/n} = \frac{4}{2} = 2$$
Since $\lim_{n\to\infty} a_n = 2 \ne 0$, the series **diverges**.

**(b)** $\sum_{n=0}^\infty \frac{2^{2n}}{5^n}$

**Solution 5(b):**
Rewrite the term to identify the geometric ratio $r$:
$$a_n = \frac{(2^2)^n}{5^n} = \left(\frac{4}{5}\right)^n$$
This is a **Geometric Series** with $a=1$ (since the index starts at $n=0$) and $r=\frac{4}{5}$.
Since $|r| = \frac{4}{5} < 1$, the series **converges**.
The sum is:
$$\text{Sum} = \frac{a}{1-r} = \frac{1}{1 - 4/5} = \frac{1}{1/5} = \mathbf{5}$$

**(c)** $\sum_{n=1}^\infty \left(\frac{1}{n} - \frac{1}{n+3}\right)$

**Solution 5(c):**
This is a **Telescoping Series**. Write the $N$-th partial sum $s_N$:
$$s_N = \left(1 - \frac{1}{4}\right) + \left(\frac{1}{2} - \frac{1}{5}\right) + \left(\frac{1}{3} - \frac{1}{6}\right) + \left(\frac{1}{4} - \frac{1}{7}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+3}\right)$$
After cancellation, only the first three positive terms and the last three negative terms remain:
$$s_N = 1 + \frac{1}{2} + \frac{1}{3} - \frac{1}{N+1} - \frac{1}{N+2} - \frac{1}{N+3}$$
The sum is $\lim_{N\to\infty} s_N$:
$$\text{Sum} = \lim_{N\to\infty} \left(1 + \frac{1}{2} + \frac{1}{3} - 0 - 0 - 0\right)$$
$$\text{Sum} = 1 + \frac{1}{2} + \frac{1}{3} = \frac{6+3+2}{6} = \mathbf{\frac{11}{6}}$$
The series **converges** to $\mathbf{\frac{11}{6}}$.

***

### 6. Integral Test and Remainder Estimation

**(a)** Use the integral test to determine if $\sum_{n=1}^\infty \frac{n}{n^4+1}$ is convergent.

#### Review Notes on The Integral Test

* **Conditions:** The function $f(x)$ corresponding to $a_n$ must be **positive**, **continuous**, and **decreasing** for $x \ge N$.
* **Conclusion:** $\sum a_n$ converges if and only if $\int_N^\infty f(x) dx$ converges (is a finite number).

**Solution 6(a):**
The function $f(x) = \frac{x}{x^4+1}$ meets the conditions for $x \ge 1$.
Evaluate the improper integral:
$$\int_1^\infty \frac{x}{x^4+1} dx = \lim_{t\to\infty} \int_1^t \frac{x}{x^4+1} dx$$
Use $u = x^2$, $du = 2x dx$:
$$= \lim_{t\to\infty} \left[ \frac{1}{2} \arctan(x^2) \right]_1^t$$
$$= \frac{1}{2} \left( \lim_{t\to\infty} \arctan(t^2) - \arctan(1) \right)$$
$$= \frac{1}{2} \left( \frac{\pi}{2} - \frac{\pi}{4} \right) = \frac{\pi}{8}$$
Since the integral converges to $\frac{\pi}{8}$, the series **converges** by the Integral Test.

**(b)** Show that $\sum_{n=1}^\infty n e^{-n^2}$ is convergent and determine a number $N$ so that $s_N$, the partial sum of the first $N$ terms, is within $\mathbf{0.001}$ of the value of the series.

#### Review Notes on Remainder Estimation

* **Integral Test Remainder Estimate:** $R_N = S - s_N$, where $R_N \le \int_{N}^\infty f(x) dx$.
* To find $N$, solve $\int_{N}^\infty f(x) dx < \text{Error}$.

**Solution 6(b):**
**Convergence:** Evaluate the improper integral using $u = -x^2$, $du = -2x dx$:
$$\int_1^\infty x e^{-x^2} dx = \left[ -\frac{1}{2} e^{-x^2} \right]_1^\infty$$
$$= -\frac{1}{2} \left( \lim_{t\to\infty} e^{-t^2} - e^{-1} \right) = -\frac{1}{2} (0 - e^{-1}) = \frac{1}{2e}$$
Since the integral converges, the series **converges**.
**Remainder Estimation:** Set the bound $\int_{N}^\infty x e^{-x^2} dx < 0.001$:
$$\left[ -\frac{1}{2} e^{-x^2} \right]_N^\infty = 0 - \left(-\frac{1}{2} e^{-N^2}\right) = \frac{1}{2} e^{-N^2}$$
Solve the inequality:
$$\frac{1}{2} e^{-N^2} < 0.001$$
$$e^{-N^2} < 0.002$$
Take the natural log of both sides:
$$-N^2 < \ln(0.002) \approx -6.2146$$
$$N^2 > 6.2146$$
$$N > \sqrt{6.2146} \approx 2.4929$$
Since $N$ must be an integer, the smallest value is $\mathbf{3}$.

Part II: Practice
