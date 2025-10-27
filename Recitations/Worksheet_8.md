# Part I: Review
***

## Practice Problems and Solutions with Review Notes

### 1. Sequences: Terms and Limits

Write the first four terms of the sequence $a_n$ and find $\lim_{n\to\infty} a_n$ if this limit exists. You may use the limit of the corresponding continuous function on the positive real numbers. If the limit does not exist, explain why it does not.

#### Review Notes on Sequences

* A **sequence** is an ordered list of numbers $\{a_1, a_2, a_3, \ldots, a_n, \ldots\}$.
* The **limit of a sequence**, $\lim_{n\to\infty} a_n = L$, means the terms get arbitrarily close to a single number $L$. If the limit is a finite number $L$, the sequence **converges** to $L$.
* **Divergence:** A sequence **diverges** if its limit is $\infty$, $-\infty$, or if it oscillates indefinitely (e.g., $a_n = (-1)^n$).
* **L'Hôpital's Rule:** If the sequence terms are defined by a continuous function $f(x)$ where $\lim_{x\to\infty} f(x)$ results in an indeterminate form ($\frac{\infty}{\infty}$ or $\frac{0}{0}$), you can use L'Hôpital's Rule on $f(x)$.

**(a)** $\{3n - 1\}_{n=1}^\infty$

**Solution 1(a):**
* **Terms:** $a_1=2$, $a_2=5$, $a_3=8$, $a_4=11$.
* **Limit:** $\lim_{n\to\infty} (3n - 1) = \infty$.
* **Answer:** The limit **does not exist** (diverges to $\infty$).

**(b)** $a_n = \frac{(-1)^{n+1}}{2^n}$, for $n=1, 2, 3, \ldots$

**Solution 1(b):**
* **Terms:** $a_1=\frac{1}{2}$, $a_2=-\frac{1}{4}$, $a_3=\frac{1}{8}$, $a_4=-\frac{1}{16}$.
* **Limit:** This is an **alternating sequence**. Since $\lim_{n\to\infty} \left|\frac{(-1)^{n+1}}{2^n}\right| = \lim_{n\to\infty} \frac{1}{2^n} = 0$, by the Squeeze Theorem (or absolute convergence), the sequence converges to $\mathbf{0}$.
* **Answer:** $\lim_{n\to\infty} a_n = \mathbf{0}$.

**(c)** $a_n = \sqrt{n+5} - \sqrt{n}$, for $n=1, 2, 3, \ldots$

**Solution 1(c):**
* **Terms:** $a_1=\sqrt{6}-1$, $a_2=\sqrt{7}-\sqrt{2}$, $a_3=\sqrt{8}-\sqrt{3}$, $a_4=1$.
* **Limit:** This is an indeterminate form $(\infty - \infty)$. Multiply by the **conjugate** to transform it:
    $$a_n = (\sqrt{n+5} - \sqrt{n}) \cdot \frac{\sqrt{n+5} + \sqrt{n}}{\sqrt{n+5} + \sqrt{n}} = \frac{(n+5) - n}{\sqrt{n+5} + \sqrt{n}} = \frac{5}{\sqrt{n+5} + \sqrt{n}}$$
    $$\lim_{n\to\infty} a_n = \lim_{n\to\infty} \frac{5}{\sqrt{n+5} + \sqrt{n}} = \frac{5}{\infty + \infty} = \mathbf{0}$$
* **Answer:** $\lim_{n\to\infty} a_n = \mathbf{0}$.

***

### 2. Converting Decimal to Rational Number

Find the rational number that has the decimal expansion $0.1\overline{23}$... (The bar is over $23$).

#### Review Notes on Rational Numbers and Decimals

* A **rational number** is any number that can be expressed as the ratio $\frac{p}{q}$ of two integers, where $q \ne 0$.
* Rational numbers always have decimal expansions that either **terminate** (like $1/4 = 0.25$) or **repeat** (like $1/3 = 0.\overline{3}$).
* **Strategy for conversion:**
    1.  Set the decimal equal to $x$.
    2.  Multiply $x$ by $10^k$, where $k$ is the number of digits before the repeating block starts (to shift the non-repeating part left).
    3.  Multiply $x$ by $10^{k+m}$, where $m$ is the length of the repeating block (to shift one full repeating block left).
    4.  Subtract the two resulting equations to eliminate the infinitely repeating tail.
    5.  Solve for $x$ and simplify the fraction.

**Solution 2:**
Let $x = 0.1232323\ldots$
1.  Shift the non-repeating digit ($1$):
    $$10x = 1.232323\ldots$$
2.  Shift one full repeating block ($23$ has length 2):
    $$1000x = 123.232323\ldots$$
3.  Subtract (1) from (2):
    $$\begin{array}{rcl} 1000x &=& 123.232323\ldots \\ -10x &=& 1.232323\ldots \\ \hline 990x &=& 122 \end{array}$$
    $$x = \frac{122}{990}$$
4.  Simplify by dividing by 2:
    $$x = \mathbf{\frac{61}{495}}$$

***

### 3. Applications: Recursive Sequences and Limits

A forest has $P_0 = 500$ deer. Each year, a fixed fraction of $\mathbf{0.8}$ of the deer survive (after births and natural deaths), and $\mathbf{150}$ deer are added to the forest (stocked from a preserve). Calculate the number of deer in each of the first $\mathbf{3}$ years. Do not round to the nearest deer. Write a recursive formula for the number of deer after $n$ years, and determine the limit of $P_n$, as $n \to\infty$.

#### Review Notes on Recursive Sequences (First-Order Linear)

* A **recursive sequence** defines the next term based on the preceding term(s). The general form for this type of problem is $P_n = r P_{n-1} + d$, where $r$ is the survival/growth rate and $d$ is the constant addition/subtraction.
* **Limit (Steady State):** If $|r| < 1$, the limit $\lim_{n\to\infty} P_n$ exists and represents the long-term, **steady-state** population.
* **Finding the Limit $L$:** To find the limit, assume $\lim_{n\to\infty} P_n = L$ and $\lim_{n\to\infty} P_{n-1} = L$. Substitute $L$ into the recursive formula and solve:
    $$L = r L + d \implies L(1-r) = d \implies L = \frac{d}{1-r}$$

**Solution 3:**
* **First 3 Years:**
    * $P_1 = 0.8(500) + 150 = 400 + 150 = \mathbf{550}$
    * $P_2 = 0.8(550) + 150 = 440 + 150 = \mathbf{590}$
    * $P_3 = 0.8(590) + 150 = 472 + 150 = \mathbf{622}$
* **Recursive Formula:**
    $$P_n = 0.8 P_{n-1} + 150 \quad \text{for } n \ge 1, \text{ with } P_0 = 500$$
* **Limit:** Let $L = \lim_{n\to\infty} P_n$:
    $$L = 0.8 L + 150 \implies 0.2 L = 150 \implies L = 750$$
* **Answer:** $P_1 = \mathbf{550}$, $P_2 = \mathbf{590}$, $P_3 = \mathbf{622}$. Recursive formula: $P_n = 0.8 P_{n-1} + 150$. $\lim_{n\to\infty} P_n = \mathbf{750}$.

***

### 4. Partial Sums and Series Sum

If the $n$-th partial sum of a series $\sum_{n=1}^\infty a_n$ is $s_n = \frac{2n}{n + 1}$, find $a_1$, $a_2$, $a_n$ and the sum of the series $\sum_{n=1}^\infty a_n$.

#### Review Notes on Partial Sums and Series

* A **series** is the sum of the terms of a sequence: $\sum_{n=1}^\infty a_n = a_1 + a_2 + a_3 + \cdots$
* The **$n$-th partial sum**, $s_n$, is the sum of the first $n$ terms: $s_n = \sum_{k=1}^n a_k$.
* **Series Sum:** The **sum of the series** $S$ is the limit of the partial sums: $S = \sum_{n=1}^\infty a_n = \lim_{n\to\infty} s_n$. If this limit is a finite number, the series **converges**.
* **Finding the Terms $a_n$:** The relationship between the terms of the series and the partial sums is:
    * $a_1 = s_1$
    * $a_n = s_n - s_{n-1}$ for $n \ge 2$.

**Solution 4:**
* **$a_1$:** $a_1 = s_1 = \frac{2(1)}{1+1} = \frac{2}{2} = \mathbf{1}$.
* **$a_2$:** $a_2 = s_2 - s_1$. $s_2 = \frac{2(2)}{2+1} = \frac{4}{3}$. $a_2 = \frac{4}{3} - 1 = \mathbf{\frac{1}{3}}$.
* **$a_n$:** For $n \ge 2$, $a_n = s_n - s_{n-1}$:
    $$a_n = \frac{2n}{n+1} - \frac{2(n-1)}{n} = \frac{2n^2 - 2(n-1)(n+1)}{n(n+1)} = \frac{2n^2 - 2(n^2-1)}{n(n+1)} = \frac{2}{n(n+1)}$$
* **Sum of the Series:** The sum is $S = \lim_{n\to\infty} s_n$:
    $$S = \lim_{n\to\infty} \frac{2n}{n+1} = \lim_{n\to\infty} \frac{2}{1 + 1/n} = \mathbf{2}$$

***

### 5. Convergence Tests for Series

Determine if the following series converge and, if so, find the sum. Use the geometric series, telescoping series, or divergence test if needed:

#### Review Notes on Series Convergence (Basic Tests)

* **Divergence Test (The First Check):** If $\lim_{n\to\infty} a_n \ne 0$ or the limit does not exist, then $\sum a_n$ **diverges**. (If $\lim_{n\to\infty} a_n = 0$, the test is **inconclusive**—the series may converge or diverge.)
* **Geometric Series:** $\sum_{n=0}^\infty a r^n$.
    * Converges if $|r| < 1$. Sum is $S = \frac{a}{1-r}$.
    * Diverges if $|r| \ge 1$.
* **Telescoping Series:** A series where the partial sum $s_n$ simplifies because most of the terms **cancel out** in pairs. The series converges if $\lim_{n\to\infty} s_n$ is a finite value.

**(a)** $\sum_{n=1}^\infty \frac{4n^2+1}{2n^2 - n}$

**Solution 5(a):**
* **Test:** **Divergence Test**.
* Calculate the limit of the terms:
    $$\lim_{n\to\infty} a_n = \lim_{n\to\infty} \frac{4n^2+1}{2n^2 - n} = \frac{4}{2} = 2$$
* **Answer:** Since $\lim_{n\to\infty} a_n = 2 \ne 0$, the series **diverges**.

**(b)** $\sum_{n=0}^\infty \frac{2^{2n}}{5^n}$

**Solution 5(b):**
* **Test:** **Geometric Series**.
* Rewrite the term: $a_n = \frac{(2^2)^n}{5^n} = \left(\frac{4}{5}\right)^n$. This is a geometric series with $a=1$ and ratio $r=\frac{4}{5}$.
* **Sum:** Since $|r| = \frac{4}{5} < 1$, the series **converges**.
    $$\text{Sum} = \frac{a}{1-r} = \frac{1}{1 - 4/5} = \frac{1}{1/5} = \mathbf{5}$$

**(c)** $\sum_{n=1}^\infty \left(\frac{1}{n} - \frac{1}{n+3}\right)$

**Solution 5(c):**
* **Test:** **Telescoping Series**.
* Write the first few terms of the partial sum $s_N$:
    $$s_N = \left(1 - \frac{1}{4}\right) + \left(\frac{1}{2} - \frac{1}{5}\right) + \left(\frac{1}{3} - \frac{1}{6}\right) + \left(\frac{1}{4} - \frac{1}{7}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+3}\right)$$
* The terms $-\frac{1}{4}$ and $+\frac{1}{4}$ cancel, $-\frac{1}{5}$ and $+\frac{1}{5}$ cancel, and so on. Only the first three positive terms and the last three negative terms remain:
    $$s_N = 1 + \frac{1}{2} + \frac{1}{3} - \frac{1}{N+1} - \frac{1}{N+2} - \frac{1}{N+3}$$
* **Sum:** The sum is $S = \lim_{N\to\infty} s_N$:
    $$S = 1 + \frac{1}{2} + \frac{1}{3} - 0 - 0 - 0 = \frac{6+3+2}{6} = \mathbf{\frac{11}{6}}$$
* **Answer:** The series **converges** to $\mathbf{\frac{11}{6}}$.

***

### 6. Integral Test and Remainder Estimation

**(a)** Use the integral test to determine if $\sum_{n=1}^\infty \frac{n}{n^4+1}$ is convergent.

#### Review Notes on The Integral Test

* **Conditions:** The Integral Test can be applied to a series $\sum_{n=N}^\infty a_n$ if the function $f(x)$ such that $f(n)=a_n$ is **positive**, **continuous**, and **decreasing** for $x \ge N$.
* **Conclusion:** The series $\sum_{n=N}^\infty a_n$ **converges** if and only if the improper integral $\int_N^\infty f(x) dx$ **converges** (is a finite number).

**Solution 6(a):**
* The function $f(x) = \frac{x}{x^4+1}$ is positive, continuous, and decreasing for $x \ge 1$.
* We evaluate the integral using **u-substitution** ($u=x^2$, $du=2xdx$):
    $$\int_1^\infty \frac{x}{x^4+1} dx = \lim_{t\to\infty} \int_1^t \frac{x}{x^4+1} dx = \lim_{t\to\infty} \left[ \frac{1}{2} \arctan(x^2) \right]_1^t$$
    $$= \frac{1}{2} \left( \lim_{t\to\infty} \arctan(t^2) - \arctan(1) \right) = \frac{1}{2} \left( \frac{\pi}{2} - \frac{\pi}{4} \right) = \frac{\pi}{8}$$
* **Answer:** Since the integral converges to $\frac{\pi}{8}$, the series **converges** by the Integral Test.

**(b)** Show that $\sum_{n=1}^\infty n e^{-n^2}$ is convergent and determine a number $N$ so that $s_N$, the partial sum of the first $N$ terms, is within $\mathbf{0.001}$ of the value of the series.

#### Review Notes on Remainder Estimation

* **Remainder Definition:** The remainder $R_N$ is the error when approximating the series sum $S$ by the partial sum $s_N$: $R_N = S - s_N = \sum_{n=N+1}^\infty a_n$.
* **Integral Test Remainder Estimate:** If the series satisfies the Integral Test conditions, the remainder is bounded by:
    $$\int_{N+1}^\infty f(x) dx \le R_N \le \int_{N}^\infty f(x) dx$$
    To find $N$ such that $R_N < \text{Error}$, you typically solve the simpler inequality:
    $$\int_{N}^\infty f(x) dx < \text{Error}$$

**Solution 6(b):**
* **Convergence:**
    $$\int_1^\infty x e^{-x^2} dx = \left[ -\frac{1}{2} e^{-x^2} \right]_1^\infty = -\frac{1}{2} (0 - e^{-1}) = \frac{1}{2e}$$
    Since the integral converges, the series **converges**.
* **Remainder Estimation:** We need $R_N < 0.001$. We solve for $N$ using the remainder bound:
    $$\int_{N}^\infty x e^{-x^2} dx < 0.001$$
    $$\left[ -\frac{1}{2} e^{-x^2} \right]_N^\infty = 0 - \left(-\frac{1}{2} e^{-N^2}\right) = \frac{1}{2} e^{-N^2}$$
    Set the inequality:
    $$\frac{1}{2} e^{-N^2} < 0.001 \implies e^{-N^2} < 0.002$$
    Take the natural log:
    $$-N^2 < \ln(0.002) \approx -6.2146$$
    $$N^2 > 6.2146 \implies N > 2.4929$$
* **Answer:** The series **converges**. The smallest integer $N$ is $\mathbf{3}$.

Part II: Practice
