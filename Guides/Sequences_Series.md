# Sequences and Series Guide
## PART I: Core Definitions for Sequences and Series

| Term | Simple Definition | Key Intuition |
| :--- | :--- | :--- |
| **Sequence** ($a_n$) | An ordered **list of numbers** defined by a rule: $a_1, a_2, a_3, \ldots$ | The **ingredients** for the sum. |
| **Series** ($\sum a_n$) | The **sum** of all the terms in a sequence: $a_1 + a_2 + a_3 + \cdots$ | The **recipe** to find the total value. |
| **Partial Sum** ($s_N$) | The sum of the first $N$ terms: $s_N = a_1 + a_2 + \cdots + a_N$. | The **product so far**; a sequence itself. |
| **Convergence** (Series) | A series **converges** if the sequence of its partial sums ($s_N$) approaches a single, finite number $S$. | The total sum **settles down** to a fixed value. |
| **Divergence** (Series) | A series **diverges** if the sequence of its partial sums ($s_N$) does not approach a finite number (it might go to $\pm \infty$ or oscillate). | The total sum **flies off** or never stabilizes. |
| **Absolute Convergence (AC)** | A series $\sum a_n$ converges even when all terms are made positive (i.e., $\sum |a_n|$ converges). | Convergence is so strong that alternating signs are unnecessary. |
| **Conditional Convergence (CC)**| A series $\sum a_n$ converges only because of its alternating signs (i.e., $\sum a_n$ converges, but $\sum |a_n|$ diverges). | Convergence is fragile; it relies entirely on cancellation. |
| **Remainder/Error ($R_N$)** | The difference between the true sum $S$ and the partial sum $s_N$: $R_N = S - s_N$. | The **leftover amount** after adding the first $N$ terms. |

---

## PART II: The Intuitive Connection: Sequences are the *Ingredients* for Series

Think of the relationship like this:

| Concept | The Intuitive Role | What it Represents |
| :--- | :--- | :--- |
| **Sequence** ($a_n$) | The **Ingredient** (The terms) | A list of numbers that you are going to add up: $a_1, a_2, a_3, \ldots$ |
| **Series** ($\sum a_n$) | The **Recipe** (The Sum) | The instruction to add all the sequence terms together: $a_1 + a_2 + a_3 + \cdots$ |
| **Partial Sum** ($s_N$) | The **Product** (The Result so far) | The *sequence* of results you get by stopping the addition at $N$: $s_1, s_2, s_3, \ldots$ |

### The Logic of Convergence

The entire idea of a series converging relies on the relationship between two different sequences:

1.  **The Sequence of Terms ($a_n$):** This sequence must go to zero (as required by the Divergence Test).
    * **Intuition:** If the ingredients you are adding never get smaller, the total sum will obviously fly off to infinity. The terms *must* approach zero for the sum to have any chance of being finite.

2.  **The Sequence of Partial Sums ($s_N$):** This sequence must converge to a finite limit.
    * **Intuition:** The series converges if, as you add more and more ingredients, the total sum ($s_N$) stops changing significantly and settles down to one fixed number.

### The Two Crucial Limits 

A series, $\sum a_n$, converges **if and only if** the sequence of its partial sums, $s_N$, converges to a finite limit $S$.

$$\sum_{n=1}^\infty a_n = S \quad \iff \quad \lim_{N \to \infty} s_N = S$$

So, a series *is* a sequence—it's the **sequence of its partial sums ($s_N$)**—and we test its convergence by seeing if that new sequence $s_N$ converges.

This intuitive understanding reinforces why:
* **Divergence Test is First:** We check $\lim a_n$ first because if the ingredients don't go to zero, the recipe is immediately a disaster.
* **The Goal is $S$:** All the convergence tests are just indirect ways of checking whether that sequence of partial sums, $s_N$, is actually approaching a finite value $S$.

## PART III: Choosing a Convergence Test

The goal is to choose the **most efficient** test based on the **form** of the series term, $a_n$.

## 1. Initial Checks (The Must-Do's)

### 🛑 Check 1: The Divergence Test (Always First!)

| Test | Logic | Condition / Conclusion |
| :--- | :--- | :--- |
| **Divergence Test** | Are the terms even getting small enough to consider convergence? | Calculate $L = \lim_{n\to\infty} a_n$. If $L \ne 0$ (or $L$ DNE), the series **DIVERGES**. (If $L=0$, the test is inconclusive; proceed to Check 2). |

##### EXCEPTION: The Strategy of Skipping the Limit - Why the Divergence Test is Often "Skipped" for Factorials:**
For a complex factorial series like $2(f) \sum \frac{(2n)!}{(n!)^2}$, determining the limit $\lim_{n\to\infty} a_n$ **is nearly impossible without using the Ratio Test first.**

| Factorial Series | The Strategy | The Rationale |
| :--- | :--- | :--- |
| **Simple Factorials** (e.g., $1/n!$) | $\lim a_n = 0$. (Easy) | $n!$ grows so fast it dominates everything, making the limit $0$. Divergence Test fails. |
| **Complex Factorials** (e.g., 2f) | **Skip $\lim a_n$ calculation** and go **immediately to the Ratio Test.** | You cannot easily determine the growth rate of $\frac{(2n)!}{(n!)^2}$ without calculating $L = \lim \frac{a_{n+1}}{a_n}$. The Ratio Test calculates the limit of the *ratio* of terms, which is often easier than the limit of the *terms* themselves. |

###### **In short:** When $a_n$ is complex and involves factorials, the Ratio Test is the most efficient (and often the *only* practical) way to analyze its behavior. We prioritize the Ratio Test because its calculation *also* reveals the convergence status.

---

1.  **Check Divergence:** What is $\lim_{n\to\infty} a_n$? (Hint: This limit is a classic form related to $e$.)
2.  **Choose the Test:** Based on the $n$-th power, which test is essential?
3.  **State the Conclusion:** What does the Divergence Test tell you here?
1.  **Check $\lim a_n$ (The Divergence Test):**
    * If $\lim_{n\to\infty} a_n \ne 0$, the series **DIVERGES**. **STOP.**

2.  **Check $\sum |a_n|$ (The Absolute Convergence Test):**
    * Use Ratio, Root, or Comparison Tests on the positive series $\sum |a_n|$.
    * If $\sum |a_n|$ converges, the original series is **Absolutely Convergent (AC)**. **STOP.**

3.  **Check AST (The Conditional Convergence Test):**
    * If $\sum |a_n|$ diverges, **THEN** proceed to the Alternating Series Test (AST) on $b_n$.
    * If AST conditions are met, the series is **Conditionally Convergent (CC)**.

### 🔍 Check 2: Special Forms (Easiest Tests)

| Series Form | Test | Logic | Condition / Conclusion |
| :--- | :--- | :--- | :--- |
| **Simple Power** $\sum \frac{1}{n^p}$ | **$p$-Series Test** | Does it match the form $\sum 1/n^p$? | **Converges** if $p > 1$. **Diverges** if $p \le 1$. |
| **Exponential** $\sum a r^n$ | **Geometric Series Test** | Does it match the form $\sum ar^n$? | **Converges** if $|r| < 1$. **Diverges** if $|r| \ge 1$. (Can also find the sum). |
| **Difference** $\sum (b_n - b_{n+1})$ | **Telescoping Test** | Can the term be rewritten as a difference that will cancel? | **Converges** if $\lim_{N\to\infty} s_N$ is finite. |

---

##### NOTE: Finding the Sum as a Clue
When a series problem asks you to **find the sum**, it is a very strong clue that the series belongs to one of the few categories for which an exact sum formula exists. 

| Series Type | Term Form ($a_n$) | Sum Formula ($S$) |
| :--- | :--- | :--- |
| **Geometric Series** | $a \cdot r^n$ | $S = \frac{a}{1-r}$ (if $|r| < 1$) |
| **Telescoping Series** | $f(n) - f(n+k)$ (after PFD) | $S = \lim_{N\to\infty} s_N$ (Found by canceling interior terms) |

If you determine convergence using LCT, Ratio, or Root Test, but the question demands the sum, you must backtrack and check for a Geometric or Telescoping form!

---


## 2. Main Tests (The Decision Matrix)

If the series doesn't fit a special form, look at the dominant term structure to decide between the major tests. 

| Series Term Structure | Recommended Test | Logic / Why Choose It |
| :--- | :--- | :--- |
| **Factorials** ($n!$) **or Mixed Exponentials** ($3^n/n!$) | **Ratio Test** | Factorials and most exponentials simplify beautifully under the ratio $\frac{a_{n+1}}{a_n}$. It cancels factorials entirely. |
| **Entire term raised to $n$** $\sum (f(n))^n$ | **Root Test** | The $n$-th root immediately eliminates the exponent, leaving a simple limit of $f(n)$. |
| **Alternating Signs** $\sum (-1)^n b_n$ | **Alternating Series Test (AST)** | If the series is alternating, this is **required** to check for conditional convergence. (Must still check $\sum |a_n|$ first!) |
| **Polynomials / Roots** $\frac{n^2+1}{n^4-3}$ | **Limit Comparison Test (LCT)** | This is the *safest* and most versatile test for rational/root functions. Choose $b_n$ by looking at the highest power terms. |
| **Complicated Denominator** $\frac{1}{n (\ln n)^2}$ | **Integral Test** | Use if the function $f(x)$ is easy to integrate but hard to compare (especially involving $\ln x$ or $\arctan x$). |
| **Bounded Numerator** $\frac{\sin n}{n^2}$ | **Direct Comparison Test** | Use when the numerator is clearly bounded (like $\sin n$ or $\cos n$), making it easy to create a larger, known convergent series (like $\sum 1/n^2$). |

---

## 3. The Alternating Series Protocol (AC vs CC)

If your series is alternating, you must follow this protocol *after* checking the Divergence Test:

| Step | Test / Logic | Conclusion |
| :--- | :--- | :--- |
| **Step A** | **Test Absolute Value** $\sum |a_n|$. Use the Ratio, Root, or Comparison Test on the positive series. | If $\sum |a_n|$ **CONVERGES**, the original series is **Absolutely Convergent (AC)**. (STOP) |
| **Step B** | If $\sum |a_n|$ **DIVERGES**, proceed to **AST** on $b_n$. | The series is not AC, but it might be saved by cancellation. |
| **Step C** | **Apply AST:** Check $\lim_{n\to\infty} b_n = 0$ AND $b_n$ is decreasing. | If AST passes, the series is **Conditionally Convergent (CC)**. If AST fails (and $\lim a_n = 0$ was $L=0$), the series **DIVERGES**. |

This systematic approach will ensure you never miss a classification and always choose the quickest route to the answer!

What problem would you like to run through this flowchart next?

## PART IV: References
### **I. Sequences ($\{a_n\}$) & Preliminary Tests**

| Concept | Condition/Test | Formula/Notes |
| :--- | :--- | :--- |
| **Limit** (Convergence) | Converges if $\lim_{n \to \infty} a_n = L$ (a finite number). |
| **Monotonic Convergence Thm.** | A bounded, monotonic sequence **must** converge. |
| **$n^{th}$-Term Test** (Divergence Test) | If $\lim_{n \to \infty} a_n \neq 0$, the series **Diverges**. |
| **CAUTION** | If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**. |

---

### **II. Fundamental Series Types ($\sum_{n=1}^\infty a_n$)**

| Series Type | General Form | Convergence Condition(s) | Key Test/Sum Formula |
| :--- | :--- | :--- | :--- |
| **Geometric Series** | $\sum_{n=0}^{\infty} ar^n$ | Converges if the common ratio $|r| < 1$. | Sum is $S = \frac{a}{1-r}$. |
| **$p$-Series** | $\sum_{n=1}^{\infty} \frac{1}{n^p}$ | Converges if the exponent **$p > 1$**. | Diverges if $p \le 1$. |
| **Harmonic Series** | $\sum_{n=1}^{\infty} \frac{1}{n}$ | **Always Diverges.** | Special case of $p$-series where $p=1$. |
| **Telescoping Series** | $\sum_{n=1}^{\infty} (b_n - b_{n+1})$ (after partial fractions) | Converges if $\lim_{N \to \infty} S_N$ exists. | Find $S_N$, then take $\lim_{N \to \infty} S_N$. |

---

### 🌟 Series Convergence Quick Reference (List Format)

#### 1. Geometric Series
* **General Form:** $\sum_{n=0}^{\infty} a r^n$
* **Convergence Condition:** Converges if $\boldsymbol{|r| < 1}$ (i.e., $-1 < r < 1$). Diverges if $|r| \ge 1$.
* **Key Formula:** When the series converges, the **Sum** is $\boldsymbol{S = \frac{a}{1-r}}$, where $a$ is the first term.

#### 2. $p$-Series
* **General Form:** $\sum_{n=1}^{\infty} \frac{1}{n^p}$
* **Convergence Condition:** Converges if $\boldsymbol{p > 1}$. Diverges if $p \le 1$.
* **Key Test:** Comparison of the exponent $p$ to 1.

#### 3. Harmonic Series
* **General Form:** $\sum_{n=1}^{\infty} \frac{1}{n}$
* **Convergence Condition:** **Always Diverges.**
* **Key Note:** This is the special case of the $p$-series where $p=1$.

#### 4. Telescoping Series
* **General Form:** $\sum_{n=1}^{\infty} (b_n - b_{n+1})$ (or a similar difference after partial fractions)
* **Convergence Condition:** Converges if the limit of the $(N+1)$-th term, $\lim_{N \to \infty} b_{N+1}$, exists (and is finite).
* **Key Formula:** The **Sum** is $S = b_1 - \lim_{N \to \infty} b_{N+1}$.

---

#### Algebraic Manipulation Needed (Example): Geometric Series
The series is:
$$\sum_{n=0}^\infty 2^n \cdot 3^{-2n+1}$$

Here are the key exponential rules you need to apply, along with the steps to rewrite the term $\left(2^n \cdot 3^{-2n+1}\right)$, without calculating the final result:

#### **Step-by-Step Guide to Rewriting the Series Term**

| Rule to Apply  | General Form | Application to $3^{-2n+1}$ |
| :--- | :--- | :--- |
| **Product Rule for Exponents** | $b^{x+y} = b^x \cdot b^y$ | Rewrite the term with the sum in the exponent as a product: $3^{-2n+1} = 3^{-2n} \cdot 3^1$. |
| **Negative Exponent Rule** | $b^{-x} = \frac{1}{b^x}$ | Apply this to the term with the negative exponent: $3^{-2n} = \frac{1}{3^{2n}}$. |
| **Power of a Power Rule** | $b^{xy} = (b^x)^y$ | Rewrite the term with a multiple of $n$ in the exponent to isolate $n$: $3^{2n} = (3^2)^n$. |

---

#### **Action Steps (for example)**
1.  **Separate the Constant Factor ($3^1$):** Use the **Product Rule** to split the term $3^{-2n+1}$ into a product of a constant and a term involving $n$.
2.  **Handle the Negative Exponent:** Use the **Negative Exponent Rule** to move the term involving $-2n$ from the numerator to the denominator (or write it as a fraction).
3.  **Isolate $n$ in the Exponent:** Use the **Power of a Power Rule** on the base of the resulting term so that the exponent becomes *exactly* $n$. (e.g., $b^{kn} = (b^k)^n$).
4.  **Combine Terms with Exponent $n$:** Once both the $2^n$ term and the rewritten $3^{(\ldots)n}$ term both have the same exponent $n$, combine them using the rule $a^n b^n = (ab)^n$.
5.  **Identify $a$ and $r$:** The result will be in the form $a \cdot r^n$, allowing you to clearly identify the initial constant ($a$) and the common ratio ($r$).


#### What Determines the Number of Terms Before Cancellation: Telescoping Series
The number of terms you calculate is simply the number required to confirm which terms at the beginning *do not* have a corresponding negative term to cancel them. For a difference of $k$, the **first $k$ positive terms** will survive the cancellation. It's all about how far apart the indices are in the difference $b_n - b_{n+k}$.

The number of terms you need to write out before the cancellation pattern is established depends entirely on the **difference in the indices** within the terms of the series.

In short, you must expand until the largest negative index term is matched by a subsequent positive index term.

#### 1. The Simple Case (Difference of 1)

In the problem we just solved, the term was in the form:

$$a_n = b_n - b_{n+1}$$

The difference in the index is **$1$**. 

* $b_8$ is the first positive term.
* The term $b_8$ will be cancelled by the $b_n$ in the term $b_8 - b_{n}$ where $n=8$. Wait, no, that's incorrect.
* The first negative term is $-b_9$ (from $n=8$).
* The first subsequent positive term is $+b_9$ (from $n=9$).

Because the terms $\pm b_k$ are adjacent, only the first positive term ($b_8$) and the last negative term ($-b_{N+1}$) remain. You only needed to write out two terms ($n=8$ and $n=9$) to see the pattern.

#### 2. The Complex Case (Difference of $k > 1$)

If the term were written in the form:

$$a_n = b_n - b_{n+k} \quad (\text{where } k > 1)$$

The difference in the index is $k$. In this case, you must write out $k$ terms (or $k+1$ terms) to see the full pattern.

**Example: If $a_n = b_n - b_{n+3}$ (Difference of 3)**

You would need to write out terms for $n=1, 2, 3, 4, \dots$

$$s_N = \underbrace{(b_1 - b_4)}_{n=1} + \underbrace{(b_2 - b_5)}_{n=2} + \underbrace{(b_3 - b_6)}_{n=3} + \underbrace{(b_4 - b_7)}_{n=4} + \cdots$$

* $b_1, b_2, b_3$ remain (the first three terms).
* The first term to cancel is $b_4$ (it cancels the $-b_4$ from $n=1$).
* Therefore, you need to write enough terms until the first negative term that cancels appears, which often requires $k+1$ terms in the expansion to be certain.

---

### **III. Convergence Tests for $\sum_{n=1}^\infty a_n$**

| Test Name | When to Use | Condition for Convergence | Condition for Divergence |
| :--- | :--- | :--- | :--- |
| **Direct Comparison Test (DCT)** | $a_n$ and $b_n$ are **positive** and a clear **term-by-term inequality** $0 \leq a_n \leq b_n$ or $0 \leq b_n \leq a_n$ can be established (eventually). | **If $0 \leq a_n \leq b_n$** for all $n$ (eventually) **AND $\sum b_n$ converges, then $\sum a_n$ converges.**  | **If $0 \leq b_n \leq a_n$** for all $n$ (eventually) **AND $\sum b_n$ diverges, then $\sum a_n$ diverges.**  |
| Integral Test | $a_n = f(n)$ is **positive, continuous, and decreasing.** | $\int_{1}^{\infty} f(x) \, dx$ converges. | $\int_{1}^{\infty} f(x) \, dx$ diverges. |
| Limit Comparison Test (LCT) | $a_n$ and $b_n$ are **positive** and **algebraically similar** (e.g., rational functions or similar dominant terms). | $\lim_{n \to \infty} \frac{a_n}{b_n} = L$, where $0 < L < \infty$. If $\sum b_n$ converges, so does $\sum a_n$. | $\lim_{n \to \infty} \frac{a_n}{b_n} = L$, where $0 < L < \infty$. If $\sum b_n$ diverges, so does $\sum a_n$. |
| Alternating Series Test (AST) | Series **alternates sign**: $\sum (-1)^n b_n$ where $b_n > 0$. | Both must hold: 1) $\lim_{n \to \infty} b_n = 0$ **AND** 2) $b_{n+1} \leq b_n$ (eventually). | Fails either of the two conditions. |
| Ratio Test | $a_n$ involves **factorials** ($n!$) or **exponents** ($r^n$). | $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| < 1$. | $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| > 1$ or $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = \infty$. |
| Root Test | $a_n$ involves an **$n$-th power**: $(\dots)^n$. | $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} < 1$. | $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} > 1$ or $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} = \infty$. |

---

That's an insightful question! Factorials often look intimidating in convergence tests, but they are actually a big hint that you should use the **Ratio Test**. The key is that factorials have a property that leads to massive simplification when you take the ratio of consecutive terms.

---

## 💡 Factorials: Simplification in the Ratio Test

| Factorial Ratio | Full Expansion | Final Simplification |
| :--- | :--- | :--- |
| $\frac{(n+1)!}{n!}$ | $\frac{(n+1) \cdot n!}{n!}$ | $n+1$ |
| $\frac{n!}{(n+1)!}$ | $\frac{n!}{(n+1) \cdot n!}$ | $\frac{1}{n+1}$ |
| $\frac{(2n+2)!}{(2n)!}$ | $\frac{(2n+2)(2n+1)(2n)!}{(2n)!}$ | $(2n+2)(2n+1)$ |
| $\frac{(2n)!}{(2n+2)!}$ | $\frac{(2n)!}{(2n+2)(2n+1)(2n)!}$ | $\frac{1}{(2n+2)(2n+1)}$ |

Whenever you see a factorial in a series, your first instinct should be to reach for the **Ratio Test**, as it is specifically designed to exploit these cancellation properties.

### **IV. Power Series, Taylor Series, and Maclaurin Series**

#### **A. Power Series and Convergence**

A power series centered at $a$ has the form $\sum_{n=0}^{\infty} c_n (x-a)^n$.

1.  **Radius of Convergence ($R$):** Found by applying the **Ratio Test** to $\sum_{n=0}^{\infty} \left| c_n (x-a)^n \right|$.
    $$\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = L \cdot |x-a|$$
    Set $L \cdot |x-a| < 1$ and solve for $|x-a| < R$.

2.  **Interval of Convergence (IOC):** The interval $(a-R, a+R)$, plus the two endpoints.
    * **Crucial Step:** The endpoints $x = a-R$ and $x = a+R$ **must** be tested individually using any of the convergence tests (AST, $p$-Series, etc.) to determine if the series converges at those points.

#### **B. Taylor and Maclaurin Series**

| Series Type | Definition (Formula) | Center |
| :--- | :--- | :--- |
| **Taylor Series** | $$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$$ | $x=a$ |
| **Maclaurin Series** | $$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$ | $x=0$ |

#### **C. Common Maclaurin Series**

| Function $f(x)$ | Maclaurin Series | IOC ($R$) |
| :--- | :--- | :--- |
| **Geometric** | $\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n$ | $(-1, 1)$, $R=1$ |
| **$e^x$** | $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\sin(x)$** | $\sin(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\cos(x)$** | $\cos(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\arctan(x)$** | $\arctan(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$ | $[-1, 1]$, $R=1$ |
