## Additional Practice Problems
***

### 1. Absolute, Conditional, and Divergence Tests

Determine whether the following series are **absolutely convergent (AC)**, **conditionally convergent (CC)**, or **divergent (D)**.

#### Review Notes on Absolute/Conditional Convergence

* **AC:** $\sum a_n$ converges if $\sum |a_n|$ converges (use $p$-Test or Comparison Tests).
* **CC:** $\sum a_n$ converges (often by **AST**), but $\sum |a_n|$ diverges.
* **Divergence Test:** If $\lim_{n\to\infty} a_n \ne 0$, the series diverges.

**Generalized Steps (AC/CC/D):**
1.  **Divergence Test:** Calculate $L = \lim_{n\to\infty} a_n$. If $L \ne 0$, the series **Diverges**. (Stop here.)
2.  **Absolute Convergence (AC):** Analyze $\sum |a_n|$. Use Ratio, Root, Comparison, or $p$-Test. If $\sum |a_n|$ converges, the original series is **Absolutely Convergent** (AC). (Stop here.)
3.  **Conditional Convergence (CC):** If $\sum |a_n|$ diverges, apply the Alternating Series Test (AST) to the original series (if it's alternating).
    * If the AST conditions are met ($\lim b_n=0$ and $b_n$ is decreasing), the series is **Conditionally Convergent** (CC).
    * If the AST conditions are not met, or if the series is not alternating, the series **Diverges**.

**(a)** $\sum_{n=1}^\infty \frac{(-1)^n}{(n^2+5)^{3/2}}$

**Solution 1(a):**
* **Absolute Convergence:** Consider $\sum |a_n| = \sum_{n=1}^\infty \frac{1}{(n^2+5)^{3/2}}$.
* Use **Limit Comparison Test (LCT)** with the convergent $p$-series $b_n = \frac{1}{(n^2)^{3/2}} = \frac{1}{n^3}$.
* $\lim_{n\to\infty} \frac{a_n}{b_n} = \lim_{n\to\infty} \frac{n^3}{(n^2+5)^{3/2}} = \lim_{n\to\infty} \left(\frac{n^2}{n^2+5}\right)^{3/2} = 1$.
* Since the limit is finite and positive, and $\sum b_n$ converges, $\sum |a_n|$ **converges**.
* **Answer:** **Absolutely Convergent (AC)**.

**(b)** $\sum_{n=1}^\infty \frac{(-1)^{n} \ln n}{n}$

**Solution 1(b):**
* **Absolute Convergence:** Consider $\sum |a_n| = \sum_{n=1}^\infty \frac{\ln n}{n}$.
* Use **Direct Comparison Test** with $\sum b_n = \sum \frac{1}{n}$. Since $\ln n > 1$ for $n \ge 3$, $\frac{\ln n}{n} > \frac{1}{n}$. Since the harmonic series $\sum \frac{1}{n}$ diverges, $\sum |a_n|$ **diverges**.
* **Conditional Convergence:** Apply the **Alternating Series Test (AST)** to $b_n = \frac{\ln n}{n}$.
    1. $\lim_{n\to\infty} b_n = 0$ (by L'Hôpital's Rule on $f(x)$).
    2. $f'(x) = \frac{1-\ln x}{x^2}$. Since $f'(x)<0$ for $x > e$, $b_n$ is decreasing for $n \ge 3$.
* The series converges by AST but not absolutely.
* **Answer:** **Conditionally Convergent (CC)**.

**(c)** $\sum_{n=1}^\infty \frac{(-1)^{n} \cdot n^2}{n^2+3}$

**Solution 1(c):**
* **Divergence Test:** Analyze the limit of the terms:
    $$\lim_{n\to\infty} a_n = \lim_{n\to\infty} \frac{(-1)^{n} n^2}{n^2+3}$$
* Since $\lim_{n\to\infty} |a_n| = \lim_{n\to\infty} \frac{n^2}{n^2+3} = 1$, the terms of the series oscillate between values close to 1 and -1.
* The limit $\lim_{n\to\infty} a_n$ **does not exist** (or is not zero).
* **Answer:** **Divergent (D)**.

**(d)** $\sum_{n=1}^\infty \frac{(-1)^{n} \cdot 5^n}{n!}$

**Solution 1(d):**
* **Absolute Convergence:** Use the **Ratio Test** on $|a_n| = \frac{5^n}{n!}$.
* $$L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n\to\infty} \left( \frac{5^{n+1}}{(n+1)!} \cdot \frac{n!}{5^n} \right) = \lim_{n\to\infty} \frac{5}{n+1} = 0$$
* Since $L = 0 < 1$, the series **converges absolutely**.
* **Answer:** **Absolutely Convergent (AC)**.

**(e)** $\sum_{n=1}^\infty \frac{(-1)^{n+1}}{\sqrt[3]{n}}$

**Solution 1(e):**
* **Absolute Convergence:** $\sum |a_n| = \sum \frac{1}{n^{1/3}}$. This is a $p$-series with $p=1/3 \le 1$, so the absolute series **diverges**.
* **Conditional Convergence:** Apply the **AST** to $b_n = 1/n^{1/3}$.
    1. $b_n$ is decreasing.
    2. $\lim_{n\to\infty} b_n = 0$.
* The series converges by AST but not absolutely.
* **Answer:** **Conditionally Convergent (CC)**.

***

### 2. Ratio, Root, Comparison, and Geometric Tests

Use ratio, root, comparison or divergence test to determine convergence/divergence. When possible, find the sum.

#### Review Notes on Advanced Convergence Tests

* **Ratio Test:** Use for factorials ($n!$) or terms with $n$ in the exponent and base ($3^n/n^3$). $L = \lim |\frac{a_{n+1}}{a_n}|$. Converges if $L<1$.
* **Root Test:** Use when the entire term is raised to the $n$-th power. $L = \lim \sqrt[n]{|a_n|}$. Converges if $L<1$.
* **Comparison/LCT:** Use for terms involving polynomials or roots (compare to a $p$-series).
* **Geometric Series:** $\sum ar^n$ converges if $|r|<1$. Sum is $S = \frac{\text{first term}}{1-r}$.

**Generalized Steps (Ratio, Root, Comparison):**
1.  **Ratio Test:** Calculate $L = \lim_{n\to\infty} |\frac{a_{n+1}}{a_n}|$. If $L<1$, converges. If $L>1$, diverges. (Use for $n!$ or $c^n$).
2.  **Root Test:** Calculate $L = \lim_{n\to\infty} \sqrt[n]{|a_n|}$. If $L<1$, converges. If $L>1$, diverges. (Use for $(f(n))^n$).
3.  **Comparison:** Choose a comparison series $\sum b_n$ (usually a $p$-series or Geometric series).
    * **LCT:** If $\lim a_n/b_n = c$ (where $c$ is finite and $c>0$), $\sum a_n$ and $\sum b_n$ share convergence. (Use for complicated polynomials).
    * **Direct:** Check if $0 \le a_n \le b_n$. If $\sum b_n$ converges, $\sum a_n$ converges. (Use for $\sin n, \cos n$ bounds).
4.  **Divergence Test:** If all else fails or $L=1$, check $\lim a_n$. If $\lim a_n \ne 0$, the series diverges.

**(a)** $\sum_{n=1}^\infty \left( \frac{3^n}{3^n+1} \right)$

**Solution 2(a):**
* **Divergence Test:**
    $$\lim_{n\to\infty} a_n = \lim_{n\to\infty} \frac{3^n}{3^n+1} = \lim_{n\to\infty} \frac{1}{1+1/3^n} = 1$$
* Since $\lim_{n\to\infty} a_n = 1 \ne 0$, the series **diverges**.

**(b)** $\sum_{n=2}^\infty \frac{1}{n \ln n}$

**Solution 2(b):**
* **Integral Test:** Let $f(x) = \frac{1}{x \ln x}$. Conditions for the test are met for $x \ge 2$.
* Evaluate the improper integral (using $u = \ln x$):
    $$\int_2^\infty \frac{1}{x \ln x} dx = \lim_{t\to\infty} [\ln|\ln x|]_2^t = \lim_{t\to\infty} (\ln(\ln t) - \ln(\ln 2)) = \infty$$
* Since the integral diverges, the series **diverges**.

**(c)** $\sum_{n=1}^\infty \frac{n^2}{n^5+1}$

**Solution 2(c):**
* **Limit Comparison Test (LCT):** Compare with the convergent $p$-series $b_n = \frac{n^2}{n^5} = \frac{1}{n^3}$ ($p=3 > 1$).
* $$\lim_{n\to\infty} \frac{a_n}{b_n} = \lim_{n\to\infty} \frac{n^2/(n^5+1)}{1/n^3} = \lim_{n\to\infty} \frac{n^5}{n^5+1} = 1$$
* Since the limit is finite and positive, and $\sum b_n$ converges, the series **converges**.

**(d)** $\sum_{n=1}^\infty \frac{4+\sin n}{2^n}$

**Solution 2(d):**
* **Direct Comparison Test:** Since $-1 \le \sin n \le 1$, the numerator is bounded: $3 \le 4+\sin n \le 5$.
* Therefore, the terms $a_n$ are bounded by a geometric series:
    $$0 < \frac{4+\sin n}{2^n} \le \frac{5}{2^n}$$
* The comparison series $\sum b_n = \sum 5(\frac{1}{2})^n$ is a convergent geometric series ($r=1/2 < 1$).
* By the Direct Comparison Test, the series **converges (absolutely)**.

**(e)** $\sum_{n=1}^\infty \frac{n!}{(n+3)!}$

**Solution 2(e):**
* **Simplification/Telescoping:** Simplify the term:
    $$a_n = \frac{n!}{(n+3)(n+2)(n+1)n!} = \frac{1}{(n+3)(n+2)(n+1)}$$
* Since $a_n \approx 1/n^3$, it converges. (The exact sum is $1/12$, which is complex to derive without full PFD).
* **Answer:** **Convergent**.

**(f)** $\sum_{n=1}^\infty \frac{3^n \cdot n!}{n^n}$

**Solution 2(f):**
* **Ratio Test:** $|a_n| = \frac{3^n n!}{n^n}$.
* $$L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n\to\infty} \left( 3 \cdot \left(\frac{n}{n+1}\right)^n \right) = \frac{3}{e}$$
* Since $L = 3/e \approx 1.103 > 1$, the series **diverges**.

**(g)** $\sum_{n=0}^\infty \frac{4^{n+1}}{5^n}$

**Solution 2(g):**
* **Geometric Series:** Rewrite the term: $a_n = 4 \left(\frac{4}{5}\right)^n$.
* The ratio is $r = 4/5$. Since $|r| < 1$, the series **converges**.
* **Sum:** $S = \frac{a}{1-r} = \frac{4}{1 - 4/5} = \mathbf{20}$.
* **Answer:** **Convergent; sum** $\mathbf{= 20}$.

**(h)** $\sum_{n=1}^\infty \left(\frac{2n^2+1}{5n^2+n}\right)^n$

**Solution 2(h):**
* **Root Test:**
* $$L = \lim_{n\to\infty} \sqrt[n]{|a_n|} = \lim_{n\to\infty} \frac{2n^2+1}{5n^2+n} = \frac{2}{5}$$
* Since $L = 2/5 < 1$, the series **converges (absolutely)**.

**(i)** $\sum_{n=1}^\infty \frac{(n!)^2}{(2n)!}$

**Solution 2(i):**
* **Ratio Test:**
* $$L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n\to\infty} \left( \frac{(n+1)^2}{(2n+2)(2n+1)} \right) = \frac{1}{4}$$
* Since $L = 1/4 < 1$, the series **converges (absolutely)**.

***

### 3. Alternating Series Remainder Estimation

Show that $\sum_{n=1}^\infty \frac{(-1)^n}{n \cdot 2^n}$ is convergent and find the sum within $\mathbf{0.005}$ accuracy.

#### Review Notes on Alternating Series Remainder

* **Convergence:** Must satisfy the AST (decreasing $b_n$ and $\lim b_n=0$).
* **Error Bound:** The remainder $R_N$ is bounded by the first neglected term: $R_N \le b_{N+1}$.
* **Goal:** Find $N$ such that $b_{N+1} < \text{Error}$.

**Generalized Steps (AST Remainder):**
1.  **Verify AST:** Confirm $b_n$ is positive, decreasing, and $\lim b_n = 0$.
2.  **Set Inequality:** Set the remainder bound $b_{N+1}$ less than the required accuracy ($\epsilon$).
3.  **Solve for $N$:** Test integer values of $N$ until the inequality is satisfied. The lowest such $N$ is the answer.
4.  **Calculate $s_N$:** If required, calculate the partial sum using the first $N$ terms.

**Solution 3:**
* **Convergence:** The series converges by the AST since $b_n = \frac{1}{n \cdot 2^n}$ is positive, decreasing, and $\lim_{n\to\infty} b_n = 0$.
* **Find $N$:** Set $b_{N+1} < 0.005$.
    $$\frac{1}{(N+1) \cdot 2^{N+1}} < 0.005$$
* Test values for $N$ show $b_6 \approx 0.002604$.
* The smallest integer $N$ is **$5$**.
* **Calculate $s_5$:**
    $$s_5 = -\frac{1}{2} + \frac{1}{8} - \frac{1}{24} + \frac{1}{64} - \frac{1}{160} \approx \mathbf{-0.3860}$$
* **Answer:** $N=5$ gives error $< 0.005$. Estimated sum $\approx \mathbf{-0.3860}$.

***

### 4. Estimating Series Sums (Integral Test Remainder)

Use the sum of the first $\mathbf{5}$ terms to estimate $S$ of $\sum_{n=1}^\infty \frac{1}{n^3}$ and bound the error.

#### Review Notes on Integral Test Remainder

* **Sum Bound:** For a convergent series where $f(x)$ is continuous, positive, and decreasing:
    $$s_N + \int_{N+1}^\infty f(x) dx \le S \le s_N + \int_{N}^\infty f(x) dx$$

**Generalized Steps (Integral Remainder):**
1.  **Verify Conditions:** Ensure $f(x)$ is positive, continuous, and decreasing.
2.  **Evaluate Integrals:** Calculate the improper integrals $\int_{N}^\infty f(x) dx$ and $\int_{N+1}^\infty f(x) dx$.
3.  **Calculate $s_N$:** Sum the first $N$ terms.
4.  **Form Inequality:** Substitute results into the Sum Bound inequality.

**Solution 4:**
* $N=5$ and $f(x) = x^{-3}$.
* **Calculate $s_5$:**
    $$s_5 = 1 + \frac{1}{8} + \frac{1}{27} + \frac{1}{64} + \frac{1}{125} \approx \mathbf{1.18567}$$
* **Calculate Integrals:** $\int x^{-3} dx = -\frac{1}{2x^2}$.
    * **Lower Bound $\int_{6}^\infty f(x) dx$:** $\frac{1}{72} \approx 0.01389$
    * **Upper Bound $\int_{5}^\infty f(x) dx$:** $\frac{1}{50} = 0.02$
* **Bound the Error (Remainder $R_5$):**
    $$0.01389 \le R_5 \le 0.02$$
* **Bound the Sum ($S$):**
    $$1.18567 + 0.01389 \le S \le 1.18567 + 0.02$$
    $$\mathbf{1.19956} \le S \le \mathbf{1.20567}$$
* **Answer:** Estimated sum $s_5 \approx 1.18567$. The total sum $S$ is bounded by $\mathbf{[1.19956, 1.20567]}$.
