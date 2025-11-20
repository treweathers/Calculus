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

### III. Convergence Tests for $\sum a_n$


## Quick Convergence Test Reference

Start by applying the **Divergence Test** ($\lim a_n$): if the limit isn't zero, the series diverges—stop. If the limit is zero, proceed to test for **Absolute Convergence** by considering $\sum |a_n|$. For this series, use the **Ratio** or **Root Test** (good for factorials/powers), the **Comparison Tests** (use **Limit Comparison** for rational functions; **Direct Comparison** only if the inequality is obvious), or the **Integral Test** (if $f(x)$ is decreasing and positive, and $f(x)$ is easily integrable, like $\frac{1}{x \ln x}$). If the absolute series converges, the original series converges. If the absolute series diverges, and the original series is alternating, apply the **Alternating Series Test** to check for **Conditional Convergence**.

---

## 🧐 Comprehensive Convergence Test Checklist for $\sum a_n$

### Step 1: The **Divergence Test** (The First Check)

* **Goal:** To quickly determine if the series must **diverge**.
* **Check:** Calculate $\lim_{n \to \infty} a_n$.
* **Result:**
    * If $\lim_{n \to \infty} a_n \neq 0$ (or the limit does not exist), then the series **diverges**. Stop here.
    * If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**. Proceed to Step 2. (Note: Skip this initial limit calculation and go straight to the **Ratio/Root Test** if $a_n$ contains factorials or exponents of $n$).

---

### Step 2: Test for **Absolute Convergence**

Absolute convergence means the series $\sum |a_n|$ converges. If this series converges, the original series $\sum a_n$ is absolutely convergent and therefore converges.

* **Form the Absolute Series:** Consider the series of absolute values, $\sum |a_n|$.
* **Apply Tests for Absolute Convergence:** Use one of the following tests on $\sum |a_n|$:

#### A. **Ratio Test** or **Root Test** (For terms involving $n!$, products of functions, or $n$ in the exponent)

* **Ratio Test:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$.
* **Root Test:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.
* **Result (for either test):**
    * If $L < 1$, the series $\sum |a_n|$ **converges**, so $\sum a_n$ is **absolutely convergent** (and therefore convergent). Stop here.
    * If $L > 1$ or $L = \infty$, the series **diverges**. Stop here.
    * If $L = 1$, the test is **inconclusive**. Try a Comparison or Integral Test.

#### B. **Comparison Tests** (Useful when $|a_n|$ is similar to a known series)

* **Use when taking the absolute value is helpful:** This is particularly helpful when $|a_n|$ simplifies to a known convergent or divergent series (like a $p$-series or Geometric series).

* **Direct Comparison Test (DCT):**
    * **Use:** Only if the required **inequality is simple and obvious** (e.g., $n^2+5 > n^2 \implies \frac{1}{n^2+5} < \frac{1}{n^2}$).
    * **Requires:** Finding a convergent series $\sum b_n$ such that $|a_n| \le b_n$, or a divergent series $\sum d_n$ such that $|a_n| \ge d_n$.

* **Limit Comparison Test (LCT):**
    * **Use:** **Most commonly** for rational or algebraic functions. It's much easier as it avoids proving inequalities.
    * **Requires:** Find a known series $\sum b_n$ (usually the simplified dominant terms). Calculate $L = \lim_{n \to \infty} \frac{|a_n|}{b_n}$. If $0 < L < \infty$, then $\sum |a_n|$ and $\sum b_n$ have the **same convergence behavior**.

#### C. **Integral Test** (Used when $f(x)$ is continuous, positive, decreasing, and easily integrable)

* **Where it fits in:** The Integral Test is a comparison tool, best used when the term $a_n$ contains terms like $\ln n$ or complex functions that integrate cleanly using $u$-substitution.
* **Check:** Consider $f(x) = |a_x|$. The series $\sum |a_n|$ converges if and only if the improper integral $\int_1^\infty f(x) dx$ **converges** (is a finite number). If the integral **diverges**, the series also **diverges**. 

---

### Step 3: Test for **Conditional Convergence** (If Step 2 Fails)

This step only applies if:
1.  The series $\sum |a_n|$ **diverged** in Step 2.
2.  The original series $\sum a_n$ is an **Alternating Series** (terms must alternate sign, e.g., $\sum (-1)^n b_n$).

* **When the series fails absolute convergence tests:** This is precisely when you apply the **Alternating Series Test (AST)**—only if the series is alternating and you've confirmed $\sum |a_n|$ diverges.
* **Apply the Alternating Series Test:** For the series $\sum (-1)^n b_n$ (where $b_n = |a_n|$ is positive), check two conditions:
    1.  $b_n$ is **decreasing** (i.e., $b_{n+1} \le b_n$ for all $n$).
    2.  $\lim_{n \to \infty} b_n = 0$.
* **Result:** If **both conditions are met**, the series $\sum a_n$ **converges conditionally**.
* **Final Result:** If the series $\sum |a_n|$ **diverged** AND the **Alternating Series Test failed**, the series $\sum a_n$ **diverges**.

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

## Series Formula Sheet
---

## Chart of Common Maclaurin Series

| Function $f(x)$ | Maclaurin Series $\sum_{n=0}^\infty c_n x^n$ | I.O.C. |
| :--- | :--- | :--- |
| $\frac{1}{1 - x}$ (Geometric) | $\sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \dots$ | $(-1, 1)$ |
| $e^x$ | $\sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots$ | $(-\infty, \infty)$ |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $(-\infty, \infty)$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $(-\infty, \infty)$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $(-1, 1]$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $[-1, 1]$ |
| $(1+x)^k$ (Binomial) | **$\sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \dots$** | **$(-1, 1)$**$^\dagger$ |

---

$^\dagger$ **Note on Binomial Series I.O.C.:** The interval of convergence is $(-1, 1)$ for any real number $k$ that is not a non-negative integer. If $k$ is a non-negative integer (like $k=2$), the series becomes a finite polynomial and converges for all $x$ ($-\infty, \infty$).

---

### **Generalized Binomial Coefficient**

For reference, the generalized binomial coefficient is defined as:

$$\binom{k}{n} = \frac{k(k-1)(k-2) \dots (k-n+1)}{n!}$$

This definition is used for the coefficient of the $x^n$ term in the Binomial Series expansion of $(1+x)^k$.

#### **4. Binomial Series**

* **Formula:** For $(1+x)^k$, where $k$ is any real number:
    $$(1+x)^k = \sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \frac{k(k-1)(k-2)}{3!}x^3 + \dots$$
* **Binomial Coefficient:** The generalized binomial coefficient is defined as:
    $$\binom{k}{n} = \frac{k(k-1)(k-2)\dots(k-n+1)}{n!}$$
* **I.O.C.:** $(-1, 1)$. (If $k$ is a non-negative integer, the series is a finite polynomial and converges for all $x$).
