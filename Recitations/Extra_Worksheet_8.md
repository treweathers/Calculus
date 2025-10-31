# Additional Practice Problems
***

## Rec 8 Practice Problems and Solutions with Review Notes

### 1. Sequences: Terms and Limits

Write the first four terms of the sequence $a_n$ and find $\lim_{n\to\infty} a_n$ if this limit exists. You may use the limit of the corresponding continuous function on the positive real numbers. If the limit does not exist, explain why it does not.

#### Review Notes on Sequences

* A **sequence** is an ordered list of numbers $\{a_1, a_2, a_3, \ldots\}$.
* A sequence **converges** to $L$ if $\lim_{n\to\infty} a_n = L$ (a finite number).
* **Divergence** occurs if the limit is $\infty$, $-\infty$, or does not exist (e.g., oscillation).

**General Steps for Sequences $\lim_{n \to \infty} a_n$:**

1.  **Calculate Terms:** Substitute $n=1, 2, 3, 4$ into the formula $a_n$ to find the first four terms.
2.  **Analyze Limit Form:** Examine $\lim_{n\to\infty} a_n$. If it's indeterminate ($\frac{\infty}{\infty}$, $\infty - \infty$, etc.), use algebraic techniques (like multiplying by the **conjugate**) or calculus tools (like **L'Hôpital's Rule** on the continuous version $f(x)$).
3.  **Evaluate:** Find the limit $L$.
4.  **Conclude:** State whether the sequence **converges** (to $L$) or **diverges**.

**(a)** $\{3n - 1\}_{n=1}^\infty$

**Solution 1(a):**
* The first four terms are: $2, 5, 8, 11$.
* The limit is $\lim_{n\to\infty} (3n - 1) = \infty$.
* The limit **does not exist** (diverges to $\infty$).

**(b)** $a_n = \frac{(-1)^{n+1}}{2^n}$, for $n=1, 2, 3, \ldots$

**Solution 1(b):**
* The first four terms are: $\frac{1}{2}, -\frac{1}{4}, \frac{1}{8}, -\frac{1}{16}$.
* The limit of the absolute value is $\lim_{n\to\infty} \left|\frac{(-1)^{n+1}}{2^n}\right| = \lim_{n\to\infty} \frac{1}{2^n} = 0$.
* The limit of the sequence is $\mathbf{0}$.

**(c)** $a_n = \sqrt{n+5} - \sqrt{n}$, for $n=1, 2, 3, \ldots$

**Solution 1(c):**
* The first four terms are: $\sqrt{6} - 1, \sqrt{7} - \sqrt{2}, \sqrt{8} - \sqrt{3}, 1$.
* Multiply by the conjugate: $a_n = \frac{5}{\sqrt{n+5} + \sqrt{n}}$.
* The limit is $\lim_{n\to\infty} \frac{5}{\sqrt{n+5} + \sqrt{n}} = \frac{5}{\infty} = \mathbf{0}$.

***

### 2. Converting Decimal to Rational Number

Find the rational number that has the decimal expansion $0.1\overline{23}$... (The bar is over $23$).

#### Review Notes on Rational Numbers and Decimals

* A **rational number** is a ratio $\frac{p}{q}$ of integers.
* Repeating decimals are always rational.

**General Steps for Decimal to Rational Conversion:**

1.  **Set $x$:** Let $x$ equal the decimal.
2.  **Shift Non-Repeating:** Multiply $x$ by $10^k$ (where $k$ is the count of non-repeating digits) to get the decimal point *just before* the repeating block starts. Call this **Eq. 1**.
3.  **Shift One Block:** Multiply $x$ by $10^{k+m}$ (where $m$ is the length of the repeating block) to get the decimal point *after* the first full repeating block. Call this **Eq. 2**.
4.  **Subtract:** Subtract (Eq. 1) from (Eq. 2) to eliminate the infinitely repeating tail.
5.  **Solve and Simplify:** Solve the resulting algebraic equation for $x$ and simplify the fraction.

**Solution 2:**
* Let $x = 0.1232323\ldots$.
* $10x = 1.232323\ldots$ (Shift non-repeating digit 1)
* $1000x = 123.232323\ldots$ (Shift one full repeating block 23)
* Subtract the two equations: $1000x - 10x = 123 - 1$, which simplifies to $990x = 122$.
* Solve for $x$: $x = \frac{122}{990}$.
* Simplify the fraction: $x = \mathbf{\frac{61}{495}}$.

***

### 3. Applications: Recursive Sequences and Limits

A forest has $P_0 = 500$ deer. Each year, a fixed fraction of $\mathbf{0.8}$ of the deer survive (after births and natural deaths), and $\mathbf{150}$ deer are added to the forest (stocked from a preserve). Calculate the number of deer in each of the first $\mathbf{3}$ years. Do not round to the nearest deer. Write a recursive formula for the number of deer after $n$ years, and determine the limit of $P_n$, as $n \to\infty$.

#### Review Notes on Recursive Sequences (First-Order Linear)

* **Recursive Formula:** $P_n = r P_{n-1} + d$.
* **Limit (Steady State):** If $|r| < 1$, the long-term population $L$ is found by solving $L = r L + d$, which gives $L = \frac{d}{1-r}$.

**General Steps for Recursive Limits:**

1.  **Calculate Terms:** Use the initial condition $P_0$ and the recursive formula to find $P_1, P_2, P_3, \ldots$
2.  **Write Formula:** Define the general recursive formula $P_n$ in terms of $P_{n-1}$ and the constants.
3.  **Find Limit Equation:** Assume the limit $L$ exists and substitute $L$ for both $P_n$ and $P_{n-1}$ in the recursive formula.
4.  **Solve for $L$:** Algebraically solve the resulting linear equation for $L$.

**Solution 3:**
* The number of deer in the first 3 years:
    * $P_1 = 0.8(500) + 150 = 550$
    * $P_2 = 0.8(550) + 150 = 590$
    * $P_3 = 0.8(590) + 150 = 622$
* The recursive formula is:
    * $P_n = 0.8 P_{n-1} + 150 \quad \text{for } n \ge 1, \text{ with } P_0 = 500$
* To find the limit $L$, set $L = 0.8L + 150$:
    * $L - 0.8L = 150$
    * $0.2L = 150$
    * $L = \mathbf{750}$

***

### 4. Partial Sums and Series Sum

If the $n$-th partial sum of a series $\sum_{n=1}^\infty a_n$ is $s_n = \frac{2n}{n + 1}$, find $a_1$, $a_2$, $a_n$ and the sum of the series $\sum_{n=1}^\infty a_n$.

#### Review Notes on Partial Sums and Series

* **Series Sum:** $S = \sum_{n=1}^\infty a_n = \lim_{n\to\infty} s_n$.
* **Terms:** $a_1 = s_1$ and $a_n = s_n - s_{n-1}$ for $n \ge 2$.

**General Steps for Series from Partial Sums:**

1.  **Find $a_1$:** Calculate $s_1$. This is $a_1$.
2.  **Find $a_2$:** Calculate $s_2$. Then $a_2 = s_2 - s_1$.
3.  **Find $a_n$:** Form the difference $s_n - s_{n-1}$ and simplify the resulting expression to get a formula for $a_n$ (for $n \ge 2$).
4.  **Find Sum:** Calculate $\lim_{n\to\infty} s_n$. This is the sum of the series.

**Solution 4:**
* Find $a_1$:
    * $a_1 = s_1 = \frac{2(1)}{1+1} = \mathbf{1}$.
* Find $a_2$:
    * $s_2 = \frac{2(2)}{2+1} = \frac{4}{3}$.
    * $a_2 = s_2 - s_1 = \frac{4}{3} - 1 = \mathbf{\frac{1}{3}}$.
* Find $a_n$ for $n \ge 2$:
    * $a_n = s_n - s_{n-1} = \frac{2n}{n+1} - \frac{2(n-1)}{n}$
    * $a_n = \frac{2n^2 - 2(n^2-1)}{n(n+1)} = \mathbf{\frac{2}{n(n+1)}}$
* Find the sum of the series:
    * $\sum_{n=1}^\infty a_n = \lim_{n\to\infty} s_n = \lim_{n\to\infty} \frac{2n}{n+1}$
    * $\lim_{n\to\infty} \frac{2}{1 + 1/n} = \mathbf{2}$

***

### 5. Convergence Tests for Series

Determine if the following series converge and, if so, find the sum. Use the geometric series, telescoping series, or divergence test if needed:

#### Review Notes on Series Convergence (Basic Tests)

* **Divergence Test:** If $\lim_{n\to\infty} a_n \ne 0$, the series $\sum a_n$ **diverges**.
* **Geometric Series:** $\sum ar^n$ converges if $|r|<1$. Sum is $S = \frac{a}{1-r}$.
* **Telescoping Series:** Look for a term that can be split using partial fraction decomposition or is already in the form $b_n - b_{n+k}$. The sum is $\lim_{n\to\infty} s_n$.

**General Steps for Basic Convergence Tests:**

1.  **Divergence Test:** Always check $\lim_{n\to\infty} a_n$. If it's non-zero, the series diverges.
2.  **Geometric Check:** If the series involves $r^n$, identify the common ratio $r$. If $|r|<1$, it converges; if $|r| \ge 1$, it diverges. Calculate the sum if it converges.
3.  **Telescoping Check:** If the series involves a difference of terms (often involving $n$ and $n+k$), write out $s_N$ to see if intermediate terms cancel. Find $\lim_{N\to\infty} s_N$.

**(a)** $\sum_{n=1}^\infty \frac{4n^2+1}{2n^2 - n}$

**Solution 5(a):**
* Apply the **Divergence Test**:
    * $\lim_{n\to\infty} a_n = \lim_{n\to\infty} \frac{4n^2+1}{2n^2 - n}$
    * $\lim_{n\to\infty} \frac{4 + 1/n^2}{2 - 1/n} = \frac{4}{2} = 2$
* Since $\lim_{n\to\infty} a_n = 2 \ne 0$, the series **diverges**.

**(b)** $\sum_{n=0}^\infty \frac{2^{2n}}{5^n}$

**Solution 5(b):**
* Rewrite the term: $a_n = \frac{(2^2)^n}{5^n} = \left(\frac{4}{5}\right)^n$.
* This is a **Geometric Series** with $a=1$ and ratio $r=\frac{4}{5}$.
* Since $|r| = \frac{4}{5} < 1$, the series **converges**.
* The sum is $S = \frac{a}{1-r} = \frac{1}{1 - 4/5} = \frac{1}{1/5} = \mathbf{5}$.

**(c)** $\sum_{n=1}^\infty \left(\frac{1}{n} - \frac{1}{n+3}\right)$

**Solution 5(c):**
* This is a **Telescoping Series**. Write the $N$-th partial sum $s_N$:
    * $s_N = \left(1 - \frac{1}{4}\right) + \left(\frac{1}{2} - \frac{1}{5}\right) + \left(\frac{1}{3} - \frac{1}{6}\right) + \left(\frac{1}{4} - \frac{1}{7}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+3}\right)$
* After cancellation, the remaining terms are:
    * $s_N = 1 + \frac{1}{2} + \frac{1}{3} - \frac{1}{N+1} - \frac{1}{N+2} - \frac{1}{N+3}$
* The sum is $S = \lim_{N\to\infty} s_N$:
    * $S = 1 + \frac{1}{2} + \frac{1}{3} - 0 - 0 - 0 = \frac{6+3+2}{6} = \mathbf{\frac{11}{6}}$
* The series **converges** to $\mathbf{\frac{11}{6}}$.

***

### 6. Integral Test and Remainder Estimation

**(a)** Use the integral test to determine if $\sum_{n=1}^\infty \frac{n}{n^4+1}$ is convergent.

#### Review Notes on The Integral Test

* **Conditions:** Test requires $f(x)$ to be **positive**, **continuous**, and **decreasing** for $x \ge N$.
* **Convergence:** $\sum a_n$ converges if and only if $\int_N^\infty f(x) dx$ converges.

**General Steps for Integral Test:**

1.  **Check Conditions:** Verify that $f(x)$ is positive, continuous, and decreasing for $x \ge N$ (usually $N=1$).
2.  **Evaluate Integral:** Calculate the improper integral $I = \int_{N}^\infty f(x) dx = \lim_{t\to\infty} \int_{N}^t f(x) dx$.
3.  **Conclude:** If $I$ is a finite number, the series converges. If $I$ is $\infty$, the series diverges.

**Solution 6(a):**
* The function $f(x) = \frac{x}{x^4+1}$ meets the conditions for $x \ge 1$.
* Evaluate the integral using substitution $u = x^2$:
    * $\int_1^\infty \frac{x}{x^4+1} dx = \lim_{t\to\infty} \left[ \frac{1}{2} \arctan(x^2) \right]_1^t$
    * $= \frac{1}{2} \left( \lim_{t\to\infty} \arctan(t^2) - \arctan(1) \right)$
    * $= \frac{1}{2} \left( \frac{\pi}{2} - \frac{\pi}{4} \right) = \frac{\pi}{8}$
* Since the integral converges to $\frac{\pi}{8}$, the series **converges** by the Integral Test.

That is a very astute observation! You are right—I did not create a specific parallel practice problem for a series like $\sum \frac{\ln n}{n^2}$, which typically uses the **Comparison Tests**. My apologies; let's fix that immediately.

Here is the supplementary practice problem and review notes for using a comparison test on a series involving $\ln n$ terms:

***

### 6. (b) Supplementary Practice Problem

Determine if the series $\sum_{n=1}^\infty \frac{\ln n}{n^{3/2}}$ is convergent.

#### Review Notes on Comparison Tests (for terms involving $\ln n$)

* When dealing with $\frac{\ln n}{n^p}$ where $p > 1$, the series is often **convergent**.
* The key is to compare it to a convergent $p$-series, $\sum \frac{1}{n^q}$, where $q$ is chosen such that $1 < q < p$.
* For any $\epsilon > 0$, the function $\ln n$ grows slower than $n^\epsilon$. That is, $\ln n < n^\epsilon$ for sufficiently large $n$.
* **Strategy:** Find a $q$ such that $q < p$, and use the fact that the $\ln n$ term can be absorbed into the denominator's power.

**General Steps for Comparison with $\ln n$:**

1.  **Choose $\epsilon$:** Select a small $\epsilon > 0$ such that $p - \epsilon > 1$.
2.  **Comparison:** Use the inequality $\ln n < n^\epsilon$ for large $n$.
3.  **Check Comparison Series:** Verify that $\sum \frac{1}{n^{p-\epsilon}}$ is a convergent $p$-series.
4.  **Conclude:** Use the **Direct Comparison Test**.

***

#### Review Notes on Remainder Estimation

* **Remainder Bound:** For a convergent series meeting the Integral Test conditions, the remainder $R_N = S - s_N$ is bounded by $\int_{N}^\infty f(x) dx$.
* **Goal:** To ensure $R_N < \text{Error}$, solve the inequality $\int_{N}^\infty f(x) dx < \text{Error}$.

**General Steps for Remainder Estimation:**

1.  **Confirm Convergence:** Use the Integral Test to confirm the series converges.
2.  **Calculate Remainder Integral:** Evaluate the improper integral from $N$ to $\infty$: $I_N = \int_{N}^\infty f(x) dx$.
3.  **Set Inequality:** Set the remainder bound $I_N$ less than the desired error ($\text{Error}$).
4.  **Solve for $N$:** Use logarithms (if necessary) to solve the inequality for $N$. Round up to the next integer.

**Solution 6(c):**
* **Convergence:** The integral test shows convergence (using $u=-x^2$):
    * $\int_1^\infty x e^{-x^2} dx = \left[ -\frac{1}{2} e^{-x^2} \right]_1^\infty = \frac{1}{2e}$
    * The series **converges**.
* **Remainder Estimation:** Set $\int_{N}^\infty x e^{-x^2} dx < 0.001$.
    * $\int_{N}^\infty x e^{-x^2} dx = \left[ -\frac{1}{2} e^{-x^2} \right]_N^\infty = \frac{1}{2} e^{-N^2}$
* Solve the inequality:
    * $\frac{1}{2} e^{-N^2} < 0.001 \implies e^{-N^2} < 0.002$
    * $-N^2 < \ln(0.002) \approx -6.2146$
    * $N^2 > 6.2146 \implies N > 2.4929$
* The smallest integer $N$ is $\mathbf{3}$.
